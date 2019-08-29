---
title: Linux 用户帐户和权限
description: 用于 Linux 的 Windows 子系统的用户帐户和权限管理参考。
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu、用户帐户
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: de18c128854ef9a39a26551db2ea0aee97b8ab4f
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122683"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的用户帐户和权限

创建 Linux 用户是在 WSL 上设置新的 Linux 分发版的第一步。  你创建的第一个用户帐户会自动配置几个特殊属性:

1. 这是你的默认用户-在启动时将自动登录。
1. 默认情况下, 它是 Linux 管理员 (sudo 组的成员)。

在适用于 Linux 的 Windows 子系统上运行的每个 Linux 分发都有其自己的 Linux 用户帐户和密码。  每当添加分发、重新安装或重置时, 都必须配置 Linux 用户帐户。  Linux 用户帐户不仅每个分发都是独立的, 它们也独立于你的 Windows 用户帐户。

## <a name="resetting-your-linux-password"></a>重置 Linux 密码

如果有权访问 Linux 用户帐户并了解当前密码, 请使用该分发版的 Linux 密码重置工具 (最有可能`passwd`) 进行更改。

如果这不是一个选项, 则可能可以通过重置默认用户来重置密码。

WSL 提供了一个默认的用户标记, 用于标识在启动 WSL 时自动登录的用户帐户。  由于许多分发都包含命令, 可将默认用户设置为 root, 还可以将默认用户更改为根用户, 而将默认用户更改为 root 是密码重置等功能的便利工具。

### <a name="for-creators-update-and-earlier"></a>用于创意者更新及更早版本
如果运行的是 Windows 10 创意者更新或更早版本, 可以通过运行以下命令来更改默认 Bash 用户:

1. 将默认用户更改为`root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 运行`bash.exe`以立即`root`登录:

    ```console
    C:\> bash.exe
    ```

1. 使用分发的 password 命令重置密码, 并关闭 Linux 控制台:

    ```BASH
    $ passwd username
    $ exit
    ```

1. 在 Windows CMD 中, 将默认用户重置回你的普通 Linux 用户帐户:

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>适用于秋季创意者更新及更高版本
若要查看哪些命令可用于特定的分发, 请`[distro.exe] /?`运行。
    
例如, 安装了 Ubuntu:

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

使用 Ubuntu 的分步说明:

1. 打开 CMD
1. 将默认 Linux 用户设置为`root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. 启动 Linux 分发 (`ubuntu`)。  你将自动登录为`root`:

1. 使用`passwd`命令重置密码:

    ```BASH
    $ passwd username
    ```

1. 在 Windows CMD 中, 将默认用户重置回普通 Linux 用户帐户。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>权限

当涉及 WSL 中的权限时, 请记住两个重要概念:

1. Windows 权限模型控制进程对 Windows 资源的权限
2. Linux 权限模型控制进程对 Linux 资源的权限

在 WSL 上运行 Linux 时, Linux 将具有与启动它的进程相同的 Windows 权限。 可以通过以下两个权限级别之一启动 Linux:

* 正常 (非提升):Linux 以已登录用户的权限运行
* 提升/管理员:通过提升的/管理员 Windows 权限运行的 Linux

> 由于提升的进程可以访问/修改系统范围内的设置和系统范围/受保护的数据, 因此请**避免**启动提升的进程, 除非你绝对需要它们是 Windows 或 Linux 应用程序/工具/shell!

上述 Windows 权限与 Linux 实例中的权限无关:Linux "Root 权限" 仅影响用户在 Linux 环境中 & filesystem 的权限;它们不会影响授予的 Windows 特权。 因此, 以 root 身份运行 Linux 进程 (例如 via `sudo`) 仅授予在 Linux 环境中处理管理员权限。

示例：    
具有 Windows 管理员权限的 bash 会话可能会`cd /mnt/c/Users/Administrator`在没有管理员权限的 bash 会话中看到 "权限被拒绝" 错误。

在 Linux 中, `sudo cd /mnt/c/Users/Administrator`键入不会授予对管理员目录的访问权限, 因为 windows 中的权限由 windows 管理。

Linux 环境中的 linux 权限模型很重要, 在该环境中, 用户拥有基于当前 Linux 用户的权限。

**示例：**  
Sudo 组中的用户可以运行`sudo apt update`。
