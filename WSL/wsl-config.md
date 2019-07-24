---
title: 管理 Linux 发行版
description: 参考列出和配置在适用于 Linux 的 Windows 子系统上运行的多个 Linux 分发。
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu、wsl、wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: 0c9f9315b17d5156aa111e7619ee25534653b27e
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499277"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理和配置适用于 Linux 的 Windows 子系统

> 适用于 Windows 10 秋季创意者更新及更高版本。  请参阅更新的[安装指南](./install_guide.md), 尝试新的管理功能, 并开始从 Microsoft 应用商店运行多个 Linux 分发版。

## <a name="ways-to-run-wsl"></a>运行 WSL 的方式

有多种方法可通过适用于 Linux 的 Windows 子系统运行 Linux。

1. `[distro]`, 例如`ubuntu`
1. `wsl.exe` 或 `bash.exe`
1. `wsl [command]` 或 `bash -c [command]`

应使用哪种方法取决于所执行的操作。

### <a name="launch-wsl-by-distribution"></a>按分发启动 WSL

使用发行版特定的应用程序运行分发时, 会在其自己的控制台窗口中启动该分发。

![从 "开始" 菜单启动 WSL](media/start-launch.png)

这与在 Microsoft 应用商店中单击 "启动" 是相同的。

![从 Microsoft 应用商店启动 WSL](media/store-launch.png)

还可以通过运行`[distribution].exe`从命令行运行分发。

以这种方式从命令行运行分发的缺点是, 它会自动将工作目录从当前目录更改为分发的主目录。

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

从命令行运行 WSL 的最佳方式是使用`wsl.exe`。

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

不只`wsl`是保留当前的工作目录, 它允许您在 Windows 命令的两侧运行单个命令。

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


## <a name="managing-multiple-linux-distributions"></a>管理多个 Linux 分发

### <a name="windows-10-version-1903-and-later"></a>Windows 10 版本1903及更高版本

你可以使用`wsl.exe`在适用于 Linux 的 Windows 子系统 (WSL) 中管理你的分发版, 其中包括列出可用的分发、设置默认分发和卸载分发。

每个 Linux 分发独立管理自己的配置。 若要查看特定于分发的命令`[distro.exe] /?`, 请运行。  例如，`ubuntu /?`。

#### <a name="list-distributions"></a>列出分布

`wsl -l`,`wsl --list`  
列出可用于 WSL 的可用 Linux 分发版。  如果列出了分发版, 则它已安装并可供使用。

`wsl --list --all`   
列出所有分发, 包括当前不可用的分发。  它们可能正在安装、卸载或处于损坏状态。  

`wsl --list --running`   
列出当前正在运行的所有分发版。

#### <a name="set-a-default-distribution"></a>设置默认分布

默认的 WSL 分布是在命令行上运行`wsl`时运行的分发。

`wsl -s <DistributionName>`， `wsl --setdefault <DistributionName>`

将默认分布设置为`<DistributionName>`。

**示例：**  
`wsl -s Ubuntu`会将我的默认分发设置为 Ubuntu。  现在, 运行`wsl npm init`时, 它将在 Ubuntu 中运行。  如果运行`wsl`它, 将打开 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>注销并重新安装发行版

虽然可以通过 Microsoft store 安装 Linux 分发版, 但无法通过应用商店卸载。  WSL Config 允许注销/卸载分发。

取消注册还允许重新安装分发。

> **警告：** 注销后, 与该分发关联的所有数据、设置和软件都将永久丢失。  从存储重新安装将安装分发的干净副本。

`wsl --unregister <DistributionName>`  
从 WSL 中注销分发, 以便能够重新安装或清理。

例如: `wsl --unregister Ubuntu`将从 WSL 中提供的分发中删除 Ubuntu。  运行`wsl --list`时, 不会列出。

若要重新安装, 请在 Microsoft 应用商店中找到分发版, 然后选择 "启动"。

#### <a name="run-as-a-specific-user"></a>以特定用户身份运行

`wsl -u <Username>`， `wsl --user <Username>`

以指定的用户身份运行 WSL。 请注意, 用户必须存在于 WSL 分发中。

#### <a name="run-a-specific-distribution"></a>运行特定分发

`wsl --d <DistributionName>`， `wsl --distribution <DistributionName>`

运行 WSL 的指定分发, 可用于将命令发送到特定的分发, 无需更改默认值。

### <a name="versions-earlier-than-windows-10-version-1903"></a>早于 Windows 10 版本1903的版本

WSL Config (`wslconfig.exe`) 是一个命令行工具, 用于管理在适用于 linux 的 Windows 子系统 (WSL) 上运行的 linux 分发。  它允许列出可用的分发、设置默认分发和卸载分发。

尽管 WSL Config 对于跨或协调分布的设置很有帮助, 但每个 Linux 发行版都独立管理自己的配置。  若要查看特定于分发的命令`[distro.exe] /?`, 请运行。  例如，`ubuntu /?`。

若要查看 wslconfig 的所有可用选项, 请运行:`wslconfig /?`

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

#### <a name="list-distributions"></a>列出分布

`wslconfig /list`  
列出可用于 WSL 的可用 Linux 分发版。  如果列出了分发版, 则它已安装并可供使用。

`wslconfig /list /all`  
列出所有分发, 包括当前不可用的分发。  它们可能正在安装、卸载或处于损坏状态。  

#### <a name="set-a-default-distribution"></a>设置默认分布

默认的 WSL 分布是在命令行上运行`wsl`时运行的分发。

`wslconfig /setdefault <DistributionName>`

将默认分布设置为`<DistributionName>`。

**示例：**  
`wslconfig /setdefault Ubuntu`会将我的默认分发设置为 Ubuntu。  现在, 运行`wsl npm init`时, 它将在 Ubuntu 中运行。  如果运行`wsl`它, 将打开 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>注销并重新安装发行版

虽然可以通过 Microsoft store 安装 Linux 分发版, 但无法通过应用商店卸载。  WSL Config 允许注销/卸载分发。

取消注册还允许重新安装分发。

> **警告：** 注销后, 与该分发关联的所有数据、设置和软件都将永久丢失。  从存储重新安装将安装分发的干净副本。

`wslconfig /unregister <DistributionName>`  
从 WSL 中注销分发, 以便能够重新安装或清理。

例如: `wslconfig /unregister Ubuntu`将从 WSL 中提供的分发中删除 Ubuntu。  运行`wslconfig /list`时, 不会列出。

若要重新安装, 请在 Microsoft 应用商店中找到分发版, 然后选择 "启动"。

## <a name="set-wsl-launch-settings"></a>设置 WSL 启动设置

> **Windows 预览体验内部版本17093及更高版本中可用**

自动配置 WSL 中的某些功能, 这些功能将在每次使用`wsl.conf`启动子系统时应用。 

目前, 这包括自动装载选项和网络配置。

`wsl.conf`位于中`/etc/wsl.conf`的每个 Linux 分发中。 如果文件不存在, 您可以自行创建。 WSL 将检测文件是否存在, 并读取其内容。 如果文件丢失或格式不正确 (即标记格式不正确), WSL 将继续正常启动。

下面是可以添加`wsl.conf`到发行版的示例文件:

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

为了保持 .ini 约定, 密钥在部分下声明。 

WSL 支持两个部分`automount` : `network`和。

#### <a name="automount"></a>装载

区`[automount]`


| 键        | value                          | default      | 本票                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| enabled    | boolean                        | true         | `true`导致固定驱动器 (即 `C:/`或`D:/`) 自动装载到下`/mnt`的 DrvFs。  `false`表示不会自动装入驱动器, 但你仍然可以手动或通过`fstab`手动装载它们。                                                                                                             |
| mountFsTab | boolean                        | true         | `true`要`/etc/fstab`在 WSL start 上处理的设置。 /etc/fstab 是一个文件, 你可以在其中声明其他文件系统, 例如 SMB 共享。 因此, 可以在启动时在 WSL 中自动装入这些文件系统。                                                                                                                |
| root       | String                         | `/mnt/`      | 设置固定驱动器将自动装载到的目录。 例如, 如果在`/windir/` WSL 中有一个目录, 并将其指定为根, 则会看到你的固定驱动器已装载到`/windir/c`                                                                                              |
| 选项    | 以逗号分隔的值列表 | 空字符串 | 此值将追加到默认的 DrvFs 装载选项字符串。 **只能指定 DrvFs 特定的选项。** 装载二进制文件通常会分析为标志的选项不受支持。 如果要显式指定这些选项, 则必须在/etc/fstab 中包含要为其执行此操作的每个驱动器。 |

默认情况下, WSL 会将 uid 和 gid 设置为默认用户的值 (在 Ubuntu 发行版中, 使用 uid = 1000, gid = 1000 创建默认用户)。 如果用户通过此键显式指定了 gid 或 uid 选项, 将覆盖相关值。 否则, 将始终追加默认值。

**注意：** 这些选项应用为所有自动装入驱动器的装载选项。 若要仅更改特定驱动器的选项, 请改用/etc/fstab。

#### <a name="network"></a>网络

节标签:`[network]`

| 键 | value | default | 本票|
|:----|:----|:----|:----|
| generateHosts | boolean | `true` | `true`设置要生成`/etc/hosts`的 WSL。 `hosts`文件包含主机名对应的 IP 地址的静态映射。 |
| generateResolvConf | boolean | `true` | `true`将 WSL 设置为`/etc/resolv.conf`生成。 `resolv.conf`包含能够将给定主机名解析为其 IP 地址的 DNS 列表。 | 

#### <a name="interop"></a>交互

节标签:`[interop]`

内部版本17713及更高版本中提供了这些选项。

| 键 | value | default | 本票|
|:----|:----|:----|:----|
| enabled | boolean | `true` | 设置此项将确定 WSL 是否将支持启动 Windows 进程。 |
| appendWindowsPath | boolean | `true` | 设置此项将确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。 | 
