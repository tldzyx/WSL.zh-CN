---
title: Windows 与 Linux 的互操作性
description: 介绍 Windows 在适用于 Linux 的 Windows 子系统上运行的 Linux 分发的互操作性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: e4608c25c6bcc63413d53b2c808c16fe2a62dd5c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2019
ms.locfileid: "67040814"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>适用于 Linux 的 windows 子系统与 Windows 的互操作性

> **更新了秋季创意者更新。**  
如果正在运行创建者更新或周年周年更新, 请跳转到 "[创建者/周年更新" 部分](interop.md#creators-update-and-anniversary-update)。

适用于 Linux 的 Windows 子系统 (WSL) 不断改进 Windows 和 Linux 的集成。  你可以：

1. 从 Linux 控制台调用 Windows 二进制文件。
1. 从 Windows 控制台调用 Linux 二进制文件。
1. **Windows 预览体验内部版本 17063 +** 在 Linux 和 Windows 之间共享环境变量。

这在 Windows 和 WSL 之间提供了无缝体验。  [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)上的技术详细信息。

## <a name="run-linux-tools-from-a-windows-command-line"></a>从 Windows 命令行运行 Linux 工具

使用`wsl.exe <command>`从 Windows 命令提示符 (CMD 或 PowerShell) 运行 Linux 二进制文件。

以这种方式调用的二进制文件:

1. 使用与当前 CMD 或 PowerShell 提示符相同的工作目录。
1. 以 WSL 默认用户身份运行。
1. 具有与调用进程和终端相同的 Windows 管理权限。

例如：

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

以下`wsl.exe` Linux 命令的处理方式类似于在 WSL 中运行的任何命令。  例如, sudo、管道和文件重定向的工作方式。

使用 sudo 的示例:

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

混合 WSL 和 Windows 命令的示例:

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

传入的命令`wsl.exe`将在不进行修改的情况下转发到 WSL 进程。  文件路径必须以 WSL 格式指定。

路径示例:

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>从 WSL 运行 Windows 工具

WSL 可以使用`[binary name].exe`从 WSL 命令行直接调用 Windows 二进制文件。  例如，`notepad.exe` 。  为了使 windows 可执行文件更易于运行, windows 路径包含在`$PATH`秋季创意者更新中。

以这种方式运行的应用程序具有以下属性:

1. 将工作目录保留为 WSL 命令提示符 (大多数情况下, 以下说明除外)。
1. 具有与 WSL 进程相同的权限。
1. 以活动 Windows 用户身份运行。
1. 在 Windows 任务管理器中显示, 就像直接从 CMD 提示符执行一样。

例如：

``` BASH
$ notepad.exe
```

在 WSL 中运行的 Windows 可执行文件的处理方式类似于本机 Linux 可执行文件-管道、重定向, 甚至后台处理按预期工作。

使用管道的示例:

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

使用混合窗口和 WSL 命令的示例:

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 二进制文件必须包含文件扩展名, 与文件大小写匹配, 并可执行。  包括批处理脚本的不可执行文件。  CMD 本机命令 ( `dir`如) 可以通过`cmd.exe /C`命令运行。

示例：

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

参数被传递到未修改的 Windows 二进制文件。

例如, 以下命令将在中`C:\temp\foo.txt` `notepad.exe`打开:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

不支持在 WSL 中使用 Windows 应用程序`/mnt/<x>`修改位于 VolFs (不受下的文件) 上的文件。

默认情况下, WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录, 但如果工作目录在 VolFs 上, 则将回退到实例创建目录。

例如,`wsl.exe`最初从`C:\temp`开始, 当前的 WSL 目录更改为用户的主目录。  当`notepad.exe`从用户的主目录调用时, WSL 将自动还原为`C:\temp` notepad.exe 工作目录:

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>在 Windows 和 WSL 之间共享环境变量

> 在 Windows 有问必答版本17063及更高版本中可用。

在17063之前, 只有 WSL 可以访问的 Windows 环境变量是`PATH` (因此, 你可以从 WSL 下启动 Win32 可执行文件)。

从17063、WSL 和 Windows 共享`WSLENV`开始, 创建了一个特殊的环境变量, 用于在 WSL 上运行的 Windows 和 Linux 发行版。

`WSLENV`属性:

* 它是共享的;它存在于 Windows 和 WSL 环境中。
* 它是要在 Windows 和 WSL 之间共享的环境变量的列表。
* 它可以设置环境变量的格式, 以便在 Windows 和 WSL 中正常工作。

中`WSLENV`提供了四个标志来影响如何转换该环境变量。

`WSLENV`随意

* `/p`-翻译 WSL/Linux 样式路径和 Win32 路径之间的路径。
* `/l`-指示环境变量是路径的列表。
* `/u`-指示此环境变量只应在从 Win32 运行 WSL 时包括在内。
* `/w`-指示此环境变量只应在从 WSL 运行 Win32 时包括在内。

可以根据需要组合标志。

## <a name="disable-interop"></a>禁用互操作

用户可以通过以 root 身份运行以下命令, 禁止为单个 WSL 会话运行 Windows 二进制文件的功能。

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

若要重新启用 Windows 二进制文件, 请退出所有 WSL 会话并重新运行 bash, 或以 root 身份运行以下命令:

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

禁用互操作不会在 WSL 会话之间保留--启动新会话时将再次启用互操作。

## <a name="creators-update-and-anniversary-update"></a>创意者更新和周年周年更新

尽管互操作体验前期编写者更新类似于最新的互操作体验, 但有很多重大差别。

总结：

* `bash.exe`已弃用并已替换为`wsl.exe`。
* `-c`不需要`wsl.exe`用于运行单个命令的选项。
* Windows 路径包含在 WSL 中。`$PATH`

禁用互操作的过程保持不变。

### <a name="invoking-wsl-from-the-windows-command-line"></a>从 Windows 命令行调用 WSL

可以从 Windows 命令提示符或 PowerShell 调用 Linux 二进制文件。  以这种方式调用的二进制文件具有以下属性:

1. 使用与 CMD 或 PowerShell 提示符相同的工作目录。
1. 以 WSL 默认用户身份运行。
1. 具有与调用进程和终端相同的 Windows 管理权限。

例如：

```console
C:\temp> bash -c "ls -la"
```

以这种方式调用的 Linux 命令的处理方式与任何其他 Windows 应用程序一样。  输入、管道和文件重定向等功能按预期方式工作。

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

传递给`bash -c`的 WSL 命令将在不进行修改的情况下转发到 WSL 进程。  文件路径必须以 WSL 格式指定, 必须小心才能转义相关字符。 例如：

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>从 WSL 调用 Windows 二进制文件

适用于 Linux 的 Windows 子系统可以直接从 WSL 命令行调用 Windows 二进制文件。  以这种方式运行的应用程序具有以下属性:

1. 除了下面所述的方案之外, 将工作目录保留为 WSL 命令提示符。
1. 与该`bash.exe`进程具有相同的权限权限。 
1. 以活动 Windows 用户身份运行。
1. 在 Windows 任务管理器中显示, 就像直接从 CMD 提示符执行一样。

例如：

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

在 WSL 中, 这些可执行文件的处理方式类似于本机 Linux 可执行文件。  这意味着将目录添加到 Linux 路径, 并按预期方式在命令之间进行管道操作。  示例：

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 二进制文件必须包含文件扩展名, 与文件大小写匹配, 并可执行。  可执行文件 (包括批处理脚本) 和`dir`命令 (如) `/mnt/c/Windows/System32/cmd.exe /C`可以通过命令运行。

示例：

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

参数被传递到未修改的 Windows 二进制文件。  

例如, 以下命令将在中`C:\temp\foo.txt` `notepad.exe`打开:

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

不支持使用 Windows 应用程序修改位于 VolFs `/mnt/<x>`(不在下) 的文件。  默认情况下, WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录, 但如果工作目录在 VolFs 上, 则将回退到实例创建目录。

例如,`bash.exe`最初从`C:\temp`开始, 当前的 WSL 目录更改为用户的主目录。  当`notepad.exe`从用户的主目录调用时, WSL 将自动还原为`C:\temp` notepad.exe 工作目录:

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
