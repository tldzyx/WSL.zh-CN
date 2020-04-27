---
title: Windows 与 Linux 的互操作性
description: 介绍 Windows 与适用于 Linux 的 Windows 子系统上运行的 Linux 分发版之间的互操作性。
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269797"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a>适用于 Linux 的 Windows 子系统与 Windows 的互操作性

> **已针对 Fall Creators Update 更新。**  
如果你运行的是创意者更新或周年更新，请跳转到[创意者/周年更新部分](interop.md#creators-update-and-anniversary-update)。

适用于 Linux 的 Windows 子系统 (WSL) 正在持续改进 Windows 与 Linux 之间的集成。  你可以：

1. 从 Linux 控制台调用 Windows 二进制文件。
1. 从 Windows 控制台调用 Linux 二进制文件。
1. **Windows 预览体验成员内部版本 17063+** 在 Linux 与 Windows 之间共享环境变量。

这可以在 Windows 与 WSL 之间提供无缝的体验。  [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)中提供了技术详细信息。

## <a name="run-linux-tools-from-a-windows-command-line"></a>从 Windows 命令行运行 Linux 工具

使用 `wsl.exe <command>` 从 Windows 命令提示符（CMD 或 PowerShell）运行 Linux 二进制文件。

以这种方式调用二进制文件：

1. 使用当前 CMD 或 PowerShell 提示符中提到的同一工作目录。
1. 以 WSL 默认用户的身份运行。
1. 拥有与调用方进程和终端相同的 Windows 管理权限。

例如：

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

`wsl.exe` 后面的 Linux 命令的处理方式与 WSL 中运行的任何命令的处理方式类似。  可以执行 sudo、管道处理和文件重定向等操作。

使用 sudo 的示例：

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

混合 WSL 和 Windows 命令的示例：

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

传入 `wsl.exe` 的命令将按原样转发到 WSL 进程。  文件路径必须以 WSL 格式指定。

使用路径的示例：

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a>从 WSL 运行 Windows 工具

WSL 可以使用 `[binary name].exe` 直接从 WSL 命令行调用 Windows 二进制文件。  例如， `notepad.exe`。  为使 Windows 可执行文件更易于运行，Windows 路径将包含在 Fall Creators Update 中的 Linux `$PATH` 内。

以这种方式运行的应用程序具有以下属性：

1. 按 WSL 命令提示保留工作目录（大部分情况下是这样 -- 下面所述的情况除外）。
1. 拥有与 WSL 进程相同的权限。
1. 以活动 Windows 用户的身份运行。
1. 显示在 Windows 任务管理器中，就如同直接从 CMD 提示符执行的一样。

示例：

``` BASH
$ notepad.exe
```

在 WSL 中运行的 Windows 可执行文件的处理方式类似于本机 Linux 可执行文件 - 管道处理、重定向，甚至后台处理都可按预期方式工作。

使用管道的示例：

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

使用混合 Windows 和 WSL 命令的示例：

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

Windows 二进制文件必须包含文件扩展名，匹配文件大小写，并且可执行。  包含批处理脚本的不可执行文件。  `dir` 等 CMD 本机命令可与 `cmd.exe /C` 命令一起运行。

示例：

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

参数将按原样传递到 Windows 二进制文件。

例如，以下命令将在 `C:\temp\foo.txt` 中打开 `notepad.exe`：

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

不支持使用 WSL 中的 Windows 应用程序修改位于 VolFs 中的文件（不是在 `/mnt/<x>` 下的文件）。

默认情况下，WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录，但如果工作目录位于 VolFs 中，则会回退到实例创建目录。

例如，`wsl.exe` 最初是从 `C:\temp` 启动的，而当前 WSL 目录已更改为用户的主目录。  如果从用户的主目录调用 `notepad.exe`，WSL 将自动还原到 `C:\temp`（notepad.exe 工作目录）：

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

## <a name="share-environment-variables-between-windows-and-wsl"></a>在 Windows 与 WSL 之间共享环境变量

> 在 Windows 预览体验成员内部版本 17063 和更高版本中可用。

在 17063 以前，只有 WSL 可访问的 Windows 环境变量是 `PATH`（因此可以从 WSL 下启动 Win32 可执行文件）。

从 17063 开始，WSL 和 Windows 共享 `WSLENV`（为了桥接在 WSL 上运行的 Windows 和 Linux 分发版而创建的特殊环境变量）。

`WSLENV` 的属性：

* 它是共享的；它同时在 Windows 和 WSL 环境中存在。
* 它是要在 Windows 与 WSL 之间共享的环境变量列表。
* 它可以设置环境变量的格式，使其能够在 Windows 和 WSL 中正常运行。

`WSLENV` 中的四个标志可以影响该环境变量的转换方式。

`WSLENV` 标志：

* `/p` - 在 WSL/Linux 样式路径与 Win32 路径之间转换路径。
* `/l` - 指示环境变量是路径列表。
* `/u` - 指示仅当从 Win32 运行 WSL 时，才应包含此环境变量。
* `/w` - 指示仅当从 WSL 运行 Win32 时，才应包含此环境变量。

可按需组合标志。

## <a name="disable-interop"></a>禁用互操作

用户可以使用 root 身份运行以下命令，禁用针对单个 WSL 会话运行 Windows 二进制文件的功能。

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

若要重新启用 Windows 二进制文件，请退出所有 WSL 会话并重新运行 bash.exe，或者以 root 身份运行以下命令：

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

每次切换 WSL 会话后，禁用互操作的结果不会持久保留 -- 启动新会话后，会再次启用互操作。

## <a name="creators-update-and-anniversary-update"></a>创意者更新和周年更新

尽管 Fall Creators Update 以前的互操作体验与近来的互操作体验类似，但它们存在很多重大差别。

总结：

* `bash.exe` 已弃用，现已由 `wsl.exe` 取代。
* 在 `-c` 中不需要指定用于运行单个命令的 `wsl.exe` 选项。
* Windows 路径包含在 WSL `$PATH` 中

禁用互操作的过程未有变化。

### <a name="invoking-wsl-from-the-windows-command-line"></a>从 Windows 命令行调用 WSL

可以从 Windows 命令提示符或 PowerShell 调用 Linux 二进制文件。  以这种方式调用的二进制文件具有以下属性：

1. 使用 CMD 或 PowerShell 提示符中提到的同一工作目录。
1. 以 WSL 默认用户的身份运行。
1. 拥有与调用方进程和终端相同的 Windows 管理权限。

示例：

```console
C:\temp> bash -c "ls -la"
```

以这种方式调用的 Linux 命令的处理方式与任何其他 Windows 应用程序类似。  可按预期方式执行输入、管道处理和文件重定向等操作。

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

传入 `bash -c` 的 WSL 命令将按原样转发到 WSL 进程。  必须以 WSL 格式指定文件路径，并且必须谨慎转义相关字符。 示例：

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a>从 WSL 调用 Windows 二进制文件

适用于 Linux 的 Windows 子系统可以直接从 WSL 命令行调用 Windows 二进制文件。  以这种方式运行的应用程序具有以下属性：

1. 按 WSL 命令提示保留工作目录，但下面所述的情况除外。
1. 拥有与 `bash.exe` 进程相同的权限。 
1. 以活动 Windows 用户的身份运行。
1. 显示在 Windows 任务管理器中，就如同直接从 CMD 提示符执行的一样。

示例：

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

在 WSL 中，这些可执行文件的处理方式类似于本机 Linux 可执行文件。  这意味着，可按预期方式将目录添加到 Linux 路径，以及在命令之间进行管道处理。  示例：

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

Windows 二进制文件必须包含文件扩展名，匹配文件大小写，并且可执行。  不可执行文件（包括批处理脚本）和 `dir` 等命令可与 `/mnt/c/Windows/System32/cmd.exe /C` 命令一起运行。

示例：

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

参数将按原样传递到 Windows 二进制文件。  

例如，以下命令将在 `C:\temp\foo.txt` 中打开 `notepad.exe`：

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

不支持使用 Windows 应用程序修改位于 VolFs 中的文件（不是在 `/mnt/<x>` 下的文件）。  默认情况下，WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录，但如果工作目录位于 VolFs 中，则会回退到实例创建目录。

例如，`bash.exe` 最初是从 `C:\temp` 启动的，而当前 WSL 目录已更改为用户的主目录。  如果从用户的主目录调用 `notepad.exe`，WSL 将自动还原到 `C:\temp`（notepad.exe 工作目录）：

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
