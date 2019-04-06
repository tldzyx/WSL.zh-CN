---
title: Windows 与 Linux 的互操作性
description: 介绍在 Windows 子系统上运行适用于 Linux 的 Linux 分发版 Windows 的互操作性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063245"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>Windows 与 Linux 互操作性的 Windows 子系统

> **更新的 Fall Creators Update。**  
如果您运行创意者更新或周年更新，请跳转到[创建者/周年更新部分](interop.md#creators-update-and-anniversary-update)。

Windows 子系统用于 Linux (WSL) 在不断改进 Windows 和 Linux 之间的集成。  你可以：

1. 调用从 Linux 控制台的 Windows 二进制文件。
1. 调用 Windows 控制台中的 Linux 二进制文件。
1. **Windows 预览体验成员版本 17063 +** 共享 Linux 和 Windows 之间的环境变量。

这提供了 Windows 和 WSL 之间无缝的体验。  技术详细信息位于[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)。

## <a name="run-linux-tools-from-a-windows-command-line"></a>从 Windows 命令行运行 Linux 工具

从 Windows 命令提示符 （CMD 或 PowerShell） 使用运行 Linux 的二进制文件`wsl.exe <command>`。

在这种方式中调用的二进制文件：

1. 为当前的 CMD 或 PowerShell 提示符下使用相同的工作目录。
1. WSL 默认用户身份运行。
1. 具有与调用进程和终端相同的 Windows 管理权限。

例如：

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

以下 Linux 命令`wsl.exe`处理就像在 WSL 中运行任何命令处理。  Sudo、 管道和文件重定向等工作。

使用 sudo 的示例：

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

混合使用 WSL 和 Windows 命令的示例：

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

这些命令传递到`wsl.exe`转发到 WSL 过程无需修改即可。  必须在 WSL 格式指定文件路径。

路径示例：

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>WSL 从运行 Windows 工具

WSL 可以调用 Windows 二进制文件直接从 WSL 命令行使用`[binary name].exe`。  例如，`notepad.exe`。  若要使 Windows 可执行文件更轻松地运行，Windows 路径包括在 Linux `$PATH` Fall Creators Update 中。

此方式运行的应用程序具有以下属性：

1. 保留工作目录为 WSL 命令提示符 （大多数情况下-异常如下说明）。
1. 具有相同的权限权限作为 WSL 进程。
1. 作为活动的 Windows 用户运行。
1. Windows 任务管理器中显示像直接在命令提示符处执行。

例如：

``` BASH
$ notepad.exe
```

为本机 Linux 可执行文件-通过管道传递重定向，并按预期方式甚至后台处理的工作类似方式处理在 WSL 中运行的 Windows 可执行文件。

使用管道的示例：

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

使用混合的 Windows 和 WSL 命令的示例：

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 二进制文件必须包括文件扩展名、 匹配文件的情况下，并可执行文件。  非可执行文件包括批处理脚本。  CMD 本机命令，如`dir`可以使用运行`cmd.exe /C`命令。

示例：

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

参数传递给 Windows 二进制以未修改形式。

例如，以下命令将打开`C:\temp\foo.txt`在`notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

修改位于 VolFs 上的文件 (文件不在`/mnt/<x>`) 与 Windows 应用程序在 WSL 中的不支持。

默认情况下，WSL 尝试保留的工作目录的 Windows 二进制数作为当前 WSL 目录，但将回退到的实例创建目录的工作目录是否在 VolFs。

作为示例;`wsl.exe`从最初启动`C:\temp`而当前 WSL 目录更改为用户的主页。  当`notepad.exe`称为用户的主目录中，从 WSL 将自动恢复为`C:\temp`为 notepad.exe 的工作目录：

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a>Windows 和 WSL 之间共享环境变量

> 在 Windows 预览体验成员版本 17063 及更高版本中可用。

在 17063 之前, 仅 Windows 环境变量可访问 WSL 是`PATH`（因此，可以启动从 WSL 下的 Win32 可执行文件）。

从 17063，WSL 和 Windows 共享`WSLENV`，创建桥接在 WSL 上运行的 Windows 和 Linux 发行版的特殊环境变量。

属性的`WSLENV`:

* 共享;它在 Windows 和 WSL 环境中存在。
* 它是用于 Windows 和 WSL 之间共享的环境变量的列表。
* 它可以设置环境变量中正常运行 Windows 和 WSL 的格式。

中提供了四个标志`WSLENV`来影响如何转换该环境变量。

`WSLENV` 标志：

* `/p` -将转换 WSL/Linux 样式的路径和 Win32 路径之间的路径。
* `/l` -指示环境变量是路径的列表。
* `/u` -指示从 Win32 运行 WSL 时只应包含此环境变量。
* `/w` -指示从 WSL 运行 Win32 时只应包含此环境变量。

根据需要可以结合标志。

## <a name="disable-interop"></a>禁用互操作

用户可能会禁止以根身份运行以下命令为单一的 WSL 会话中运行 Windows 的二进制文件：

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

若要重新启用 Windows 二进制文件退出所有 WSL 会话并重新运行 bash.exe 或以 root 身份运行以下命令：

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

禁用互操作将不会保留 WSL 会话之间--启动新会话时将再次启用互操作。

## <a name="creators-update-and-anniversary-update"></a>创意者更新及周年更新

互操作体验预 Fall Creators Update 是类似于较新的互操作体验，尽管有一些主要差异 handfull。

总结：

* `bash.exe` 已弃用，替换为`wsl.exe`。
* `-c` 选项为运行单个命令不需要与`wsl.exe`。
* Windows 路径包括在 WSL `$PATH`

禁用互操作的过程保持不变。

### <a name="invoking-wsl-from-the-windows-command-line"></a>从 Windows 命令行调用 WSL

可以从 Windows 命令提示符处或从 PowerShell 调用 Linux 二进制文件。  在这种方式中调用的二进制文件具有以下属性：

1. 为 CMD 或 PowerShell 提示符使用相同的工作目录。
1. WSL 默认用户身份运行。
1. 具有与调用进程和终端相同的 Windows 管理权限。

例如：

```console
C:\temp> bash -c "ls -la"
```

Linux 命令，在这种方式中调用任何其他 Windows 应用程序一样处理。  例如输入、 管道和文件重定向操作按预期方式工作。

示例：

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

WSL 命令传递到`bash -c`转发到 WSL 过程无需修改即可。  必须在 WSL 格式指定文件路径，并且必须特别注意相关字符进行转义。 例如：

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>调用 Windows 二进制文件从 WSL

适用于 Linux 的 Windows 子系统可以调用 Windows 二进制文件直接从 WSL 命令行。  此方式运行的应用程序具有以下属性：

1. 如下所述的方案中除 WSL 命令提示符下作为保留的工作目录。
1. 具有相同的权限权限`bash.exe`过程。 
1. 作为活动的 Windows 用户运行。
1. Windows 任务管理器中显示像直接在命令提示符处执行。

例如：

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

在 WSL，这些可执行文件的处理类似于本机 Linux 可执行文件。  这意味着将目录添加到 Linux 路径并通过管道将命令的工作原理之间按预期方式。  示例：

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 二进制文件必须包括文件扩展名、 匹配文件的情况下，并可执行文件。  非可执行文件包括批处理脚本和命令等`dir`可以使用运行`/mnt/c/Windows/System32/cmd.exe /C`命令。

示例：

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

参数传递给 Windows 二进制以未修改形式。  

例如，以下命令将打开`C:\temp\foo.txt`在`notepad.exe`:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

修改位于 VolFs 上的文件 (文件不在`/mnt/<x>`) 与 Windows 应用程序不支持。  默认情况下，WSL 尝试保留的工作目录的 Windows 二进制数作为当前 WSL 目录，但将回退到的实例创建目录的工作目录是否在 VolFs。

作为示例;`bash.exe`从最初启动`C:\temp`而当前 WSL 目录更改为用户的主页。  当`notepad.exe`称为用户的主目录中，从 WSL 将自动恢复为`C:\temp`为 notepad.exe 的工作目录：

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
