---
title: 管理 Linux 分发版
description: 有关列出和配置在适用于 Linux 的 Windows 子系统上运行的多个 Linux 分发版的参考文章。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999400"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a>管理和配置适用于 Linux 的 Windows 子系统

> 适用于 Windows 10 Fall Creators Update 和更高版本。  若要试用新的管理功能并开始从 Microsoft Store 运行多个 Linux 分发版，请参阅更新的[安装指南](./install_guide.md)。

## <a name="ways-to-run-wsl"></a>WSL 的运行方式

可通过多种方式配合适用于 Linux 的 Windows 子系统运行 Linux。

1. `[distro]`，例如 `ubuntu`
1. `wsl.exe` 或 `bash.exe`
1. `wsl [command]` 或 `bash -c [command]`

要使用的方法取决于执行的操作。

### <a name="launch-wsl-by-distribution"></a>按分发版启动 WSL

使用特定于分发版的应用程序运行某个分发版会在其自身的控制台窗口中将它启动。

![从“开始”菜单启动 WSL](media/start-launch.png)

这相当于在 Microsoft Store 中单击“启动”。

![从 Microsoft Store 启动 WSL](media/store-launch.png)

还可以在命令行中运行 `[distribution].exe` 来运行分发版。

以这种方式从命令行运行分发版的缺点是，会自动将工作目录从当前目录更改为分发版的主目录。

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

### <a name="wsl-and-wsl-command"></a>wsl 和 wsl [命令]

从命令行运行 WSL 的最佳方式是使用 `wsl.exe`。

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

这样，`wsl` 不仅可以保留当前工作目录，而且还允许结合 Windows 命令运行单个命令。

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

### <a name="windows-10-version-1903-and-later"></a>Windows 10 版本 1903 和更高版本

可以使用 `wsl.exe` 管理适用于 Linux 的 Windows 子系统 (WSL) 中的分发版，包括列出可用分发版、设置默认分发版，以及卸载分发版。

每个 Linux 分发版独立管理自身的配置。 若要查看特定于分发版的命令，请运行 `[distro.exe] /?`。  例如 `ubuntu /?`。

#### <a name="list-distributions"></a>列出分发版

`wsl -l`、`wsl --list`  
列出可用于 WSL 的 Linux 分发版。  如果列出了某个分发版，表示该分发版已安装且可供使用。

`wsl --list --all`   
列出所有分发版，包括当前不可用的分发版。  这些分发版可能正在安装、卸载或处于损坏状态。  

`wsl --list --running`   
列出当前正在运行的所有分发版。

#### <a name="set-a-default-distribution"></a>设置默认分发版

默认 WSL 分布版是在命令行中运行 `wsl` 时运行的分发版。

`wsl -s <DistributionName>`、`wsl --setdefault <DistributionName>`

将默认分发版设置为 `<DistributionName>`。

**示例：**  
`wsl -s Ubuntu` 会将我的默认分发版设置为 Ubuntu。  现在，当我运行 `wsl npm init` 时，该分发版将在 Ubuntu 中运行。  如果我运行 `wsl`，它会打开 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>取消注册和重新安装分发版

尽管可以通过 Microsoft Store 安装 Linux 分发版，但无法通过 Store 将其卸载。  可以通过 WSL Config 来取消注册/卸载分发版。

取消注册后，还可以重新安装分发版。

> **警告：** 取消注册后，与该分发版关联的所有数据、设置和软件将永久丢失。  从 Store 重新安装会安装分发版的干净副本。

`wsl --unregister <DistributionName>`  
从 WSL 中取消注册分发版，以便能够重新安装或清理它。

例如：`wsl --unregister Ubuntu` 将从可用于 WSL 的分发版中删除 Ubuntu。  运行 `wsl --list` 时，不再会列出 Ubuntu。

若要重新安装，请在 Microsoft Store 中找到该分发版，然后选择“启动”。

#### <a name="run-as-a-specific-user"></a>以特定用户的身份运行

`wsl -u <Username>`、`wsl --user <Username>`

以指定用户的身份运行 WSL。 请注意，该用户必须存在于 WSL 分发版中。

#### <a name="run-a-specific-distribution"></a>运行特定的分发版

`wsl -d <DistributionName>`、`wsl --distribution <DistributionName>`

运行 WSL 的指定分发版。可用于将命令发送到特定的分发版，而无需更改默认值。

### <a name="versions-earlier-than-windows-10-version-1903"></a>低于 Windows 10 版本 1903 的版本

WSL Config (`wslconfig.exe`) 是一个命令行工具，用于管理在适用于 Linux 的 Windows 子系统 (WSL) 上运行的 Linux 分发版。  使用该工具可以列出可用分发版、设置默认分发和卸载分发版。

尽管 WSL Config 对于跨越或协调分发版的设置有帮助，但每个 Linux 分发版会独立管理自身的配置。  若要查看特定于分发版的命令，请运行 `[distro.exe] /?`。  例如 `ubuntu /?`。

若要查看 wslconfig 的所有可用选项，请运行：`wslconfig /?`

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

#### <a name="list-distributions"></a>列出分发版

`wslconfig /list`  
列出可用于 WSL 的 Linux 分发版。  如果列出了某个分发版，表示该分发版已安装且可供使用。

`wslconfig /list /all`  
列出所有分发版，包括当前不可用的分发版。  这些分发版可能正在安装、卸载或处于损坏状态。  

#### <a name="set-a-default-distribution"></a>设置默认分发版

默认 WSL 分布版是在命令行中运行 `wsl` 时运行的分发版。

`wslconfig /setdefault <DistributionName>`

将默认分发版设置为 `<DistributionName>`。

**示例：**  
`wslconfig /setdefault Ubuntu` 会将我的默认分发版设置为 Ubuntu。  现在，当我运行 `wsl npm init` 时，该分发版将在 Ubuntu 中运行。  如果我运行 `wsl`，它会打开 Ubuntu 会话。

#### <a name="unregister-and-reinstall-a-distribution"></a>取消注册和重新安装分发版

尽管可以通过 Microsoft Store 安装 Linux 分发版，但无法通过 Store 将其卸载。  可以通过 WSL Config 来取消注册/卸载分发版。

取消注册后，还可以重新安装分发版。

> **警告：** 取消注册后，与该分发版关联的所有数据、设置和软件将永久丢失。  从 Store 重新安装会安装分发版的干净副本。

`wslconfig /unregister <DistributionName>`  
从 WSL 中取消注册分发版，以便能够重新安装或清理它。

例如：`wslconfig /unregister Ubuntu` 将从可用于 WSL 的分发版中删除 Ubuntu。  运行 `wslconfig /list` 时，不再会列出 Ubuntu。

若要重新安装，请在 Microsoft Store 中找到该分发版，然后选择“启动”。

## <a name="set-wsl-launch-settings"></a>设置 WSL 启动设置

> **在 Windows 预览体验成员内部版本 17093 和更高版本中可用**

使用 `wsl.conf` 自动配置 WSL 中每次启动子系统时要应用的某些功能。 

目前，这包括自动装载选项和网络配置。

`wsl.conf` 位于每个 Linux 分发版的 `/etc/wsl.conf` 中。 如果该文件不存在，你可以自行创建。 WSL 会检测该文件是否存在，并读取其内容。 如果该文件缺失或格式不正确（即，标记格式不正确），WSL 将继续如常启动。

下面是可以添加到分发版中的示例 `wsl.conf` 文件：

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

为了遵守 .ini 约定，键将在某个节下声明。 

WSL 支持两个节：`automount` 和 `network`。

#### <a name="automount"></a>automount

节：`[automount]`


| 键        | value                          | default      | 备注                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 已启用    | 布尔值                        | true         | `true` 导致固定驱动器（即 `C:/` 或 `D:/`）自动装载到 DrvFs 中的 `/mnt` 下。  `false` 表示驱动器不会自动装载，但你仍可以手动或通过 `fstab` 装载驱动器。                                                                                                             |
| mountFsTab | 布尔值                        | true         | `true` 设置启动 WSL 时要处理的 `/etc/fstab`。 /etc/fstab 是可在其中声明其他文件系统的文件，类似于 SMB 共享。 因此，在启动时，可以在 WSL 中自动装载这些文件系统。                                                                                                                |
| root       | 字符串                         | `/mnt/`      | 设置固定驱动器要自动装载到的目录。 例如，如果 WSL 中的某个目录位于 `/windir/`，而你将该目录指定为根目录，则固定驱动器预期会装载到 `/windir/c`                                                                                              |
| 选项    | 逗号分隔值列表 | 空字符串 | 此值将追加到默认的 DrvFs 装载选项字符串。 **只能指定特定于 DrvFs 的选项。** 通常由装载二进制文件分析成标志的选项不受支持。 若要显式指定这些选项，必须在 /etc/fstab 中包含要对其执行此操作的每个驱动器。 |

默认情况下，WSL 会将 uid 和 gid 设置为默认用户的值（在 Ubuntu 分发版中，默认用户是使用 uid=1000,gid=1000 创建的）。 如果用户通过此键显式指定了 gid 或 uid 选项，将覆盖关联的值。 否则，将始终追加默认值。

**注意：** 对于所有自动装载的驱动器，这些选项将应用为装载选项。 如果只想更改特定驱动器的选项，请改用 /etc/fstab。

##### <a name="mount-options"></a>装载选项

为 Windows 驱动器 (DrvFs) 设置不同的装载选项可以控制为 Windows 文件计算文件权限的方式。 你可使用以下选项：

| 键 | 描述 | 默认 |
|:----|:----|:----|
|uid| 用于所有文件的所有者的用户 ID | WSL 发行版的默认用户 ID（第一次安装时，此项默认为 1000）
|gid| 用于所有文件的所有者的组 ID | WSL 发行版的默认组 ID（第一次安装时，此项默认为 1000）
|umask | 要对所有文件和目录排除的权限的八进制掩码 | 000
|fmask | 要对所有文件排除的权限的八进制掩码 | 000
|dmask | 要对所有目录排除的权限的八进制掩码 | 000

**注意：** 权限掩码在应用到文件或目录之前通过一个逻辑或操作进行设置。 

#### <a name="network"></a>网络

节标签：`[network]`

| 键 | value | default | 备注|
|:----|:----|:----|:----|
| generateHosts | 布尔值 | `true` | `true` 将 WSL 设置为生成 `/etc/hosts`。 `hosts` 文件包含主机名对应的 IP 地址的静态映射。 |
| generateResolvConf | 布尔值 | `true` | `true` 将 WSL 设置为生成 `/etc/resolv.conf`。 `resolv.conf` 包含能够将给定主机名解析为其 IP 地址的 DNS 列表。 | 

#### <a name="interop"></a>interop

节标签：`[interop]`

这些选项在预览体验成员内部版本 17713 和更高版本中可用。

| 键 | value | default | 备注|
|:----|:----|:----|:----|
| 已启用 | 布尔值 | `true` | 设置此键可确定 WSL 是否支持启动 Windows 进程。 |
| appendWindowsPath | 布尔值 | `true` | 设置此键可确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。 | 
