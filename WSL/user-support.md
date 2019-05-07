---
title: Linux 用户帐户和权限
description: 用户帐户和权限管理与适用于 Linux 的 Windows 子系统的参考资料。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 用户帐户的 windows 子系统
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063595"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a>用户帐户和适用于 Linux 的 Windows 子系统权限

创建 Linux 用户是设置新的 Linux 分发上 WSL 的第一步。  您创建的第一个用户帐户可通过几个特殊属性自动配置：

1. 它是默认用户--它登录自动启动。
1. Linux 管理员 （sudo 组的成员） 默认情况下它。

在适用于 Linux 的 Windows 子系统上运行每个 Linux 分发版都有自己的 Linux 用户帐户和密码。  必须将配置添加分发、 重新安装，或重置任何时间的 Linux 用户帐户。  Linux 用户帐户不只是每个分布区独立，它们也是独立于您的 Windows 用户帐户。

## <a name="resetting-your-linux-password"></a>重置 Linux 密码

如果您为 Linux 用户帐户具有访问权限并且知道当前的密码，将其更改使用 Linux 密码重置该分发-最可能的工具`passwd`。

如果这是未一个选项，具体取决于分发，你可以通过重置默认用户重置密码。

WSL 提供了默认用户标记以标识哪些用户帐户自动登录时启动 WSL。  由于许多分发包括命令，以对根和根用户的默认用户设置与设置密码，更改为根的默认用户是一个方便的工具，密码重置之类的内容。

### <a name="for-creators-update-and-earlier"></a>针对创意者更新及更早版本
如果您在运行 Windows 10 创意者更新或更早版本，可以通过运行以下命令更改默认 Bash 用户：

1. 更改到的默认用户`root`:

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. 运行`bash.exe`现在以用户身份登录到`root`:

    ```console
    C:\> bash.exe
    ```

1. 重置密码使用的分布时密码命令，然后关闭 Linux 控制台：

    ```BASH
    $ passwd username
    $ exit
    ```

1. 从 Windows 命令行重置回正常的 Linux 用户帐户的默认用户：

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a>Fall Creators Update 及更高版本
若要查看哪些命令适用于特定的分发，请运行`[distro.exe] /?`。
    
例如，使用 Ubuntu 安装：

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

通过逐步介绍了如何使用 Ubuntu 单步：

1. 打开 CMD
1. 默认 Linux 用户设置为`root`:

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. 启动你的 Linux 分发 (`ubuntu`)。  自动将以用户身份登录`root`:

1. 重置应用密码使用`passwd`命令：

    ```BASH
    $ passwd username
    ```

1. 从 Windows 命令行重置回正常的 Linux 用户帐户的默认用户。

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a>权限

有两个在 WSL 中的权限时，需要注意的重要概念：

1. Windows 权限模型控制 Windows 资源的进程的权限
2. Linux 权限模型控制 Linux 资源的进程的权限

在 WSL 中运行 Linux，Linux 会将它启动的进程相同的 Windows 权限。 Linux 可以启动两个权限级别之一：

* 正常 （非提升）：使用的登录的用户权限运行的 Linux
* 提升/管理员：使用提升/管理的 Windows 权限运行的 Linux

> 因为，提升的进程可以更改/损坏系统范围的设置和数据，和可以访问/修改受保护的文件和文件夹，**避免**启动提升的进程，除非绝对必要的-无论是 Windows 或Linux 应用程序/tools/shell ！

更高版本的 Windows 权限是独立的 Linux 实例中的权限：Linux"Root 权限"只影响在 Linux 环境和文件系统; 中的用户的权限它们将不会影响对授予的 Windows 特权。 因此，以根身份运行 Linux 进程 (例如通过`sudo`) 仅处理在 Linux 环境中的管理员权限的授予。

**示例：**    
具有 Windows 管理员权限的 Bash 会话可以访问`cd /mnt/c/Users/Administrator`没有管理员权限会看到"权限被拒绝"错误而 Bash 会话。

在 Linux 中，键入`sudo cd /mnt/c/Users/Administrator`将授予对管理员的目录访问权限，因为 Windows 内的权限管理的 Windows。

Linux 权限模型很重要时在用户具有基于当前的 Linux 用户的权限在 Linux 环境中。

**示例：**  
Sudo 组中的用户可能会运行`sudo apt update`。
