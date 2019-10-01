---
title: Linux 用户帐户和权限
description: 适用于 Linux 的 Windows 子系统的用户帐户和权限管理参考。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, 用户帐户
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d8434283e459ae25637fac0c0b1877ca07d9a255
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269715"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的用户帐户和权限

创建 Linux 用户是在 WSL 上设置新 Linux 分发版的第一步。  系统将为创建的第一个用户帐户自动配置几个特殊属性：

1. 它是你的默认用户 - 启动时它会自动登录。
1. 默认情况下，它是 Linux 管理员（sudo 组的成员）。

在适用于 Linux 的 Windows 子系统上运行的每个 Linux 分发版都有其自身的 Linux 用户帐户和密码。  每当添加分发版、重新安装或重置时，都必须配置一个 Linux 用户帐户。  Linux 用户帐户不仅是每个分发版中的独立帐户，而且也独立于 Windows 用户帐户。

## <a name="resetting-your-linux-password"></a>重置 Linux 密码

如果你有权访问 Linux 用户帐户并知道自己的当前密码，请使用该分发版的 Linux 密码重置工具（很有可能是 `passwd`）更改此密码。

如果无法做到这一点，也许可以根据所用的分发版，通过重置默认用户来重置密码。

WSL 提供一个默认用户标记用于确定在启动 WSL 时要自动登录哪个用户帐户。  由于许多分发包都包含了用于将默认用户设置为 root 以及未设置密码的 root 用户的命令，因此，将默认用户更改为 root 是密码重置等操作的便捷方式。

### <a name="for-creators-update-and-earlier"></a>对于创意者更新和更低版本
如果运行的是 Windows 10 创意者更新或更低版本，可以运行以下命令来更改默认 Bash 用户：

1. 将默认用户更改为 `root`：

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 运行 `bash.exe`，立即以 `root` 身份登录：

    ```console
    C:\> bash.exe
    ```

1. 使用分发版的 password 命令重置密码，并关闭 Linux 控制台：

    ```BASH
    $ passwd username
    $ exit
    ```

1. 在 Windows CMD 中，将默认用户重置回到普通的 Linux 用户帐户：

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>对于 Fall Creators Update 和更高版本
若要查看哪些命令适用于特定的分发版，请运行 `[distro.exe] /?`。
    
例如，在安装了 Ubuntu 的情况下：

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

有关使用 Ubuntu 的分步说明：

1. 打开 CMD
1. 将默认 Linux 用户设置为 `root`：

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. 启动 Linux 分发版 (`ubuntu`)。  你将自动以 `root` 身份登录：

1. 使用 `passwd` 命令重置密码：

    ```BASH
    $ passwd username
    ```

1. 在 Windows CMD 中，将默认用户重置回到普通的 Linux 用户帐户。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>权限

在 WSL 中的权限方面，请注意两个重要概念：

1. Windows 权限模型控制进程对 Windows 资源的权限
2. Linux 权限模型控制进程对 Linux 资源的权限

在 WSL 上运行 Linux 时，Linux 拥有的 Windows 权限与启动 Linux 的进程的权限相同。 可使用以下两个权限级别之一启动 Linux：

* 正常（未提升）：Linux 将以登录用户的权限运行
* 提升/管理员：Linux 以提升的/管理员 Windows 权限运行

> 由于权限提升的进程可以访问/修改（因而可能会损坏）系统范围的设置和系统范围/受保护的数据，因此，除非绝对必要，否则请**避免**启动权限提升的进程 - 不管它们是 Windows 还是 Linux 应用程序/工具/shell！

上述 Windows 权限独立于 Linux 实例中的权限：Linux“Root 特权”只影响用户在 Linux 环境和文件系统中的权限；它们不影响授予的 Windows 特权。 因此，以 root 身份运行 Linux 进程（例如，通过 `sudo`）只在 Linux 环境中为该进程授予管理员权限。

示例  ：    
拥有 Windows 管理员特权的 Bash 会话可以访问 `cd /mnt/c/Users/Administrator`，而没有管理员特权的 Bash 会话将出现“权限被拒绝”错误。

在 Linux 中，键入 `sudo cd /mnt/c/Users/Administrator` 不会授予对管理员目录的访问权限，因为 Windows 中的权限由 Windows 管理。

在用户的权限取决于当前 Linux 用户的 Linux 环境中，Linux 权限模型非常重要。

**示例：**  
sudo 组中的用户可以运行 `sudo apt update`。
