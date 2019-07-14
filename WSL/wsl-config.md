---
title: 管理 Linux 发行版
description: 参考列出和配置在适用于 Linux 的 Windows 子系统上运行的多个 Linux 发行版。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 wsl.conf、 wslconfig 适用于 windows 子系统
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: a4f9649805051d9c1367fd5b0a5fe541d2d1e168
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040862"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理和配置适用于 Linux 的 Windows 子系统

> 适用于 Windows 10 Fall Creators Update 及更高版本。  请参阅我们已更新[安装指南](./install_guide.md)尝试新的管理功能并开始从 Windows 应用商店中运行多个 Linux 分发版。

## <a name="ways-to-run-wsl"></a>运行 WSL 方法

使用适用于 Linux 的 Windows 子系统运行 Linux 的方法有很多种。

1. `[distro]`例如 `ubuntu`
1. `wsl.exe` 或 `bash.exe`
1. `wsl [command]` 或 `bash -c [command]`

应使用哪种方法取决于你正在执行的操作。

### <a name="launch-wsl-by-distribution"></a>通过发行版启动 WSL

使用它的特定于发行版的应用程序运行发行版会在其自己的控制台窗口中启动该发行版。

![从开始菜单启动 WSL](media/start-launch.png)

它等同于在 Windows 应用商店中单击"启动"。

![启动从 Windows 应用商店的 WSL](media/store-launch.png)

您还可以通过运行`[distribution].exe`从命令行运行发行版。

以这种方式从命令行运行发行版的缺点是，它会自动将您的工作目录从当前目录更改为发行版的主目录。

**示例：**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a>wsl 和 wsl [command]

从命令行运行 WSL 的最佳方法是使用`wsl.exe`。

**示例：**

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

`wsl`不仅保留了当前的工作目录，还允许您沿着 Windows 命令运行单个命令。

**示例：**

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

**示例：**

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a>管理多个 Linux 发行版

### <a name="windows-10-version-1903-and-later"></a>Windows 10 版本 1903 及更高版本

您可以使用`wsl.exe`来管理适用于 Linux 的 Windows 子系统（WSL）中的发行版，包括列出可用的发行版，设置默认发行版和卸载发行版。

每个 Linux 发行版独立地管理其自己的配置。若要查看特定于发行版的命令，运行`[distro.exe] /?`。例如，`ubuntu /?`。

#### <a name="list-distributions"></a>列出发行版

`wsl -l` , `wsl --list`  
列出 WSL 可用的 Linux 发行版。如果列出了发行版，则表示已安装并可供使用。

`wsl --list --all`   
列出所有发行版，包括当前不可用的发行版。他们可能正在安装，卸载或处于损坏状态。

`wsl --list --running`   
列出当前正在运行的所有发行版。

#### <a name="set-a-default-distribution"></a>设置默认发行版

默认 WSL 发行版是在命令行上运行`wsl`时所运行的发行版。

`wsl -s <DistributionName>`， `wsl --setdefault <DistributionName>`

将默认发行版设置为`<DistributionName>`。

**示例：**  
`wsl -s Ubuntu` 会将我的默认发行版设置为 Ubuntu。现在，当我运行`wsl npm init`时，它将在 Ubuntu 中运行。如果我运行`wsl`，它将打开一个 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>注销并重新安装发行版

虽然可以通过 Microsoft Store 安装 Linux 发行版，但无法通过商店卸载它们。 WSL Config 允许注销/卸载发行版。

注销后仍然可以重新安装发行版。

> **警告：** 注销后，与该发行版相关的所有数据，设置和软件将永久丢失。从商店重新安装将安装发行版的干净副本。

`wsl --unregister <DistributionName>`  
从 WSL 中注销发行版，以便可以重新安装或清除它。

例如：`wsl -unregister Ubuntu`会从 WSL 中可用的发行版中删除 Ubuntu。当我运行`wsl --list`时，它不会被列出。

若要重新安装，请在 Microsoft Store 中查找发行版，并选择"启动"。

#### <a name="run-as-a-specific-user"></a>以特定用户身份运行

`wsl -u <Username>`， `wsl --user <Username>`

以指定用户身份运行 WSL 。请注意，用户必须存在于 WSL 发行版内。

#### <a name="run-a-specific-distribution"></a>运行特定的发行版

`wsl --d <DistributionName>`， `wsl --distribution <DistributionName>`

运行指定的 WSL 发行版，可用于将命令发送到特定发行版，而无需更改默认值。

### <a name="versions-earlier-than-windows-10-version-1903"></a>版本早于 Windows 10 版本 1903

WSL 配置 (`wslconfig.exe`) 是一个命令行工具，用于管理在适用于 Linux 的 Windows 子系统（WSL）上运行的 Linux 发行版。它允许您列出可用的发行版，设置默认发行版和卸载发行版。

虽然 WSL Config 对跨越或协调发行版的设置很有帮助，但每个 Linux 发行版都独立管理自己的配置。若要查看特定于发行版的命令，请运行`[distro.exe] /?`。例如，`ubuntu /?`。

若要查看 wslconfig 所有可用的选项，请运行：  `wslconfig /?`

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a>列出发行版

`wslconfig /list`  
列出 WSL 可用的 Linux 发行版。如果列出了发行版，则表示已安装并可供使用。

`wslconfig /list /all`  
列出所有发行版，包括当前不可用的发行版。他们可能正在安装，卸载或处于损坏状态。

#### <a name="set-a-default-distribution"></a>设置默认发行版

默认 WSL 发行版是在命令行上运行`wsl`时所运行的发行版。

`wslconfig /setdefault <DistributionName>`

将默认发行版设置为`<DistributionName>`。

**示例：**  
`wslconfig /setdefault Ubuntu` 会将我的默认发行版设置为 Ubuntu。现在，当我运行`wsl npm init`时，它将在 Ubuntu 中运行。如果我运行`wsl`，它将打开一个 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>注销并重新安装发行版

虽然可以通过 Microsoft Store 安装 Linux 发行版，但无法通过商店卸载它们。 WSL Config 允许注销/卸载发行版。

注销后仍然可以重新安装发行版。

> **警告：** 注销后，与该发行版相关的所有数据，设置和软件将永久丢失。从商店重新安装将安装发行版的干净副本。

`wslconfig /unregister <DistributionName>`  
从 WSL 中注销发行版，以便可以重新安装或清除它。

例如：`wslconfig /unregister Ubuntu`会从 WSL 中可用的发行版中删除 Ubuntu。当我运行`wslconfig /list`时，它不会被列出。

若要重新安装，请在 Microsoft Store 中查找发行版，并选择"启动"。

## <a name="set-wsl-launch-settings"></a>设置 WSL 启动设置

> **可在 Windows 预览体验 build 17093 及更高版本中使用**

自动配置 WSL 中的某些功能，每次使用`wsl.conf`启动子系统时都会应用这些功能。

现在，这包括自动挂载选项和网络配置。

`wsl.conf` 在每个 Linux 发行版中都位于`/etc/wsl.conf`。 如果不存在该文件，您可以自行创建它。 WSL 将检测该文件，并将读取其内容。 如果文件缺失或格式不正确 （即，标记格式不正确），WSL 仍将正常启动。

下面是一个示例`wsl.conf`文件，可以将其添加到你的发行版中：

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a>配置选项

配置选项为了与.ini约定保持一致，键（key）在一个节（section）下声明。

WSL 支持两个节（section）：`automount`和`network`。

#### <a name="automount"></a>自动挂载

节（Section）： `[automount]`


| 键        | value                          | default      | 说明                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`导致固定驱动器（即`C:/`或`D:/`）与`/mnt`下的DrvF自动挂载。  `false`表示驱动器不会自动挂载，但您仍然可以手动或通过`fstab`挂载它们。                                                                                                             |
| mountFsTab | boolean                        | true         | `true`设置要在 WSL 启动时处理的`/etc/fstab`。 `/etc/fstab`是一个文件，您可以在其中声明其他文件系统，如 SMB 共享。 因此，您可以在启动时自动将这些文件系统安装在 WSL 中。                                                                                                                |
| root       | 字符串                         | `/mnt/` | 设置自动挂载固定驱动器的目录。 例如，如果你在的 WSL 中有一个目录`/windir/`并且你指定它作为 root，你可能会看到你的固定驱动器挂载在`/windir/c`                                                                                              |
| options    | 以逗号分隔的值列表 | 空字符串 | 此值追加到默认 DrvFs 装入选项字符串。 **可以指定仅特定于 DrvFs 的选项。** 不支持二进制装入通常会将分析成一个标志的选项。 如果你想要显式指定这些选项，则必须包括你想要这样做在 /etc/fstab 中每个的驱动器。 |

默认情况下，WSL 将 uid 和 gid 设置为默认用户的值（在 Ubuntu 发行版中，默认用户使用 uid = 1000，gid = 1000 创建）。如果用户通过此键明确指定 gid 或 uid 选项，则将覆盖关联的值。否则，将始终追加默认值。

**注意：** 这些选项适用于所有自动挂载的驱动器的挂载选项。 要仅更改特定驱动器的选项，请改用`/etc/fstab`。

#### <a name="network"></a>网络

节标签（Section label）： `[network]`

| 键 | value | default | 说明|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` 设置生成的 WSL `/etc/hosts`。 `hosts`文件包含的主机名对应的 IP 地址的静态映射。 |
| generateResolvConf | boolean | `true` | `true` 设置生成的 WSL `/etc/resolv.conf`。 `resolv.conf`包含能够将给定主机名解析为其 IP 地址的 DNS 列表。 | 

#### <a name="interop"></a>互操作

节标签（Section label）： `[interop]`

Insider Build 17713 及更高版本中提供了这些选项。

| 键 | value | default | 说明|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 此键的设置将确定 WSL 是否支持启动 Windows 进程。 |
| appendWindowsPath | boolean | `true` | 此键的设置将确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。 | 
