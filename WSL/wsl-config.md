---
title: 管理 Linux 分发版
description: 引用列出和配置在 Windows 子系统上运行适用于 Linux 的多个 Linux 分发版。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 wsl.conf、 wslconfig 适用于 windows 子系统
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063495"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理和配置适用于 Linux 的 Windows 子系统

> 适用于 Windows 10 Fall Creators Update 及更高版本。  请参阅我们已更新[安装指南](./install_guide.md)尝试新的管理功能并开始从 Windows 应用商店中运行多个 Linux 分发版。

## <a name="ways-to-run-wsl"></a>运行 WSL 方法

有许多方法来运行 Linux 的 Windows 子系统 for Linux。

1. `[distro]` ie `ubuntu`
1. `wsl.exe` 或 `bash.exe`
1. `wsl [command]` 或 `bash -c [command]`

应使用哪种方法取决于你正在执行的操作。

### <a name="launch-wsl-by-distribution"></a>启动分发 WSL

运行分发使用它的特定于发行版的应用程序将启动其自己的控制台窗口中的分发。

![从开始菜单启动 WSL](media/start-launch.png)

它等同于在 Windows 应用商店中单击"启动"。

![启动从 Windows 应用商店的 WSL](media/store-launch.png)

您还可以运行分布从命令行运行`[distribution].exe`。

从这种方式中的命令行运行分发的缺点是，它将自动更改你的工作目录当前目录中为分发的主目录。

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

若要从命令行运行 WSL 的最佳方法使用`wsl.exe`。

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

不只是`wsl`就地保留当前工作目录，它允许您运行单个命令沿端 Windows 命令。

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


## <a name="managing-multiple-linux-distributions"></a>管理多个 Linux 分发版

### <a name="windows-10-version-1903-and-later"></a>Windows 10 版本 1903年及更高版本

可以使用`wsl.exe`来管理 Windows 子系统中你分发的 Linux (WSL)，包括列出可用的分发版以及设置一个默认值的分布，卸载分发版。

每个 Linux 分发版独立地管理其自己的配置。 若要查看特定于分发的命令，运行`[distro.exe] /?`。  例如，`ubuntu /?`。

#### <a name="list-distributions"></a>列表分发版

`wsl -l` , `wsl --list`  
列出了可用于 WSL 提供 Linux 分发版。  如果列出的分发，它已安装并且可供使用。

`wsl --list --all`   
列出所有分布区，包括那些不是当前可用。  它们可能是正在安装，卸载，或处于中断状态。  

`wsl --list --running`   
列出当前正在运行的所有分布区。

#### <a name="set-a-default-distribution"></a>设置默认分发

默认 WSL 分发是运行在运行时`wsl`命令行上。

`wsl -s <DistributionName>`， `wsl --setdefault <DistributionName>`

设置为默认分发`<DistributionName>`。

**示例：**  
`wsl -s Ubuntu` 将我的默认分发到 Ubuntu。  现在，当我运行`wsl npm init`它将在 Ubuntu 中运行。  如果我运行`wsl`会打开一个 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>注销并重新安装分发

Linux 分发版可以通过 Windows 安装时存储，则它们无法卸载通过应用商店。  WSL 配置允许分发要注销/卸载。

取消注册还允许分发版必须重新安装。

> **警告：** 后已注销，则所有数据、 设置和与该分发的软件都将永久丢失。  从存储区重新安装将安装全新的分布。

`wsl --unregister <DistributionName>`  
注销 WSL 从分发，因此可以重新安装或清理。

例如：`wsl -unregister Ubuntu`将 Ubuntu 移除在 WSL 中可用的分发版。  当我运行`wsl --list`不会列出。

若要重新安装，请在 Windows 应用商店中查找分布，并选择"启动"。

#### <a name="run-as-a-specific-user"></a>以特定用户身份运行

`wsl -u <Username>`， `wsl --user <Username>`

为指定的用户运行 WSL。 请注意该用户必须存在于内部 WSL 分发。

#### <a name="run-a-specific-distribution"></a>运行特定的分发版

`wsl --d <DistributionName>`， `wsl --distribution <DistributionName>`

运行 WSL 在指定的分发，可用于将命令发送到特定分发中，而无需更改默认的。

### <a name="versions-earlier-than-windows-10-version-1903"></a>版本早于 Windows 10 版本 1903

WSL 配置 (`wslconfig.exe`) 是用于管理 Linux 分发版的 Linux (WSL) 在 Windows 子系统上运行的命令行工具。  它允许您列表可用发行版中，设置一个默认值的分布，并卸载分发版。

S p a n 或协调分发的设置有助于 WSL 配置时，每个 Linux 分发版独立地管理其自己的配置。  若要查看特定于分发的命令，运行`[distro.exe] /?`。  例如，`ubuntu /?`。

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

#### <a name="list-distributions"></a>列表分发版

`wslconfig /list`  
列出了可用于 WSL 提供 Linux 分发版。  如果列出的分发，它已安装并且可供使用。

`wslconfig /list /all`  
列出所有分布区，包括那些不是当前可用。  它们可能是正在安装，卸载，或处于中断状态。  

#### <a name="set-a-default-distribution"></a>设置默认分发

默认 WSL 分发是运行在运行时`wsl`命令行上。

`wslconfig /setdefault <DistributionName>`

设置为默认分发`<DistributionName>`。

**示例：**  
`wslconfig /setdefault Ubuntu` 将我的默认分发到 Ubuntu。  现在，当我运行`wsl npm init`它将在 Ubuntu 中运行。  如果我运行`wsl`会打开一个 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>注销并重新安装分发

Linux 分发版可以通过 Windows 安装时存储，则它们无法卸载通过应用商店。  WSL 配置允许分发要注销/卸载。

取消注册还允许分发版必须重新安装。

> **警告：** 后已注销，则所有数据、 设置和与该分发的软件都将永久丢失。  从存储区重新安装将安装全新的分布。

`wslconfig /unregister <DistributionName>`  
注销 WSL 从分发，因此可以重新安装或清理。

例如：`wslconfig /unregister Ubuntu`将 Ubuntu 移除在 WSL 中可用的分发版。  当我运行`wslconfig /list`不会列出。

若要重新安装，请在 Windows 应用商店中查找分布，并选择"启动"。

## <a name="set-wsl-launch-settings"></a>设置 WSL 启动设置

> **可在 Windows 预览体验生成 17093 及更高版本**

每次启动子系统使用将应用的 WSL 中自动配置的特定功能`wsl.conf`。 

权限现在，这包括自动装载选项和网络配置。

`wsl.conf` 位于中的每个 Linux 分发`/etc/wsl.conf`。 如果不存在该文件，您可以自行创建它。 WSL 将检测存在该文件，并将读取其内容。 如果文件缺失或格式不正确 （即，不正确标记格式设置），WSL 仍将正常启动。

下面是一个示例`wsl.conf`文件可以添加到你的发行版：

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

为了.ini 约定保持密钥声明部分下。 

WSL 支持两个部分：`automount`和`network`。

#### <a name="automount"></a>自动装载

部分中： `[automount]`


| 键        | value                          | default      | 说明                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true` 固定驱动器 （即的原因 `C:/` 或`D:/`) 以将其自动装入与 DrvFs 下`/mnt`。  `false` 表示不会自动装载驱动器，但您仍无法装载它们，手动或通过`fstab`。                                                                                                             |
| mountFsTab | boolean                        | true         | `true` 设置`/etc/fstab`要处理在 WSL 启动。 /etc/fstab 是您可以在其中声明其他文件系统，如 SMB 共享的文件。 因此，你可以向上装载自动在开始上的 WSL 中这些文件系统。                                                                                                                |
| 根       | 字符串                         | `/mnt/`      | 设置固定的驱动器会将其自动装入的目录。 例如，如果您有一个目录中在 WSL`/windir/`和指定，作为根，你会希望看到固定的驱动器装载在 `/windir/c`                                                                                              |
| 选项    | 以逗号分隔的值列表 | 空字符串 | 此值追加到默认 DrvFs 装入选项字符串。 **可以指定仅特定于 DrvFs 的选项。** 不支持二进制装入通常会将分析成一个标志的选项。 如果你想要显式指定这些选项，则必须包括你想要这样做在 /etc/fstab 中每个的驱动器。 |

默认情况下，WSL 设置 uid 和 gid 的值的默认用户 (在 Ubuntu 发行版中的默认用户创建与 uid = 1000，gid = 1000年)。 如果用户指定了此密钥通过显式 gid 或 uid 选项，将覆盖相关联的值。 否则，将始终追加的默认值。

**注意：** 这些选项将应用作为所有自动加载的驱动器装载选项。 若要更改特定驱动器的选项，请改为使用 /etc/fstab。

#### <a name="network"></a>网络

章节标签： `[network]`

| 键 | value | default | 说明|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true` 设置生成的 WSL `/etc/hosts`。 `hosts`文件包含的主机名对应的 IP 地址的静态映射。 |
| generateResolvConf | boolean | `true` | `true` 设置生成的 WSL `/etc/resolv.conf`。 `resolv.conf`包含能够将给定主机名解析为其 IP 地址的 DNS 列表。 | 

#### <a name="interop"></a>互操作

章节标签： `[interop]`

这些选项是可用在内部生成 17713 及更高版本。

| 键 | value | default | 说明|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 此键的设置将确定是否支持 WSL 启动 Windows 进程。 |
| appendWindowsPath | boolean | `true` | 此键的设置将确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。 | 
