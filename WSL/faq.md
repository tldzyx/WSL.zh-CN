---
title: 常见问题 (FAQ)
description: 适用于 Linux 的 Windows 子系统的常见问题。
keywords: BashOnWindows、 bash、 wsl、 windows、 windowssubsystem、 常见问题
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 07461f7db4a351f5b79ab0c5179d3d917ef1bdf7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035067"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的常见问题

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>什么是适用于 Linux 的 Windows 子系统 (WSL)？
适用于 Linux 的 Windows 子系统 (WSL) 是一个新的 Windows 10 功能，使您能够直接在 Windows 上运行原生 Linux 命令行工具，以及传统 Windows 桌面和新式应用商店应用。

请参阅[关于页面](./about.md)，了解更多详细信息。

## <a name="who-is-wsl-for"></a>谁适合使用 WSL？
这是主要适合开发人员使用的工具，尤其是 Web 开发人员以及参与或涉及开源项目的开发人员。 通过它，那些想要/需要使用 Bash、常用 Linux 工具（sed、awk 等）和许多 Linux 优先工具（Ruby、 Python 等）的人可以在 Windows 上使用他们的工具链。

## <a name="what-can-i-do-with-wsl"></a>使用 WSL 可以做什么？
WSL 提供了一个名为 Bash.exe 的应用程序，它在启动时会打开一个运行 Bash shell 的 Windows 控制台。使用 Bash，可以运行 Linux 的命令行工具和应用程序。 例如，键入`lsb_release -a`并按 enter，可以看到当前正在运行的 Linux 发行版的详细信息：

![发行版的详细信息的屏幕截图](media/distro.png)

您还可以从 Linux Bash shell 访问本地计算机的文件系统 - 您会发现您的本地驱动器挂载在`/mnt`文件夹。 例如，`C:`驱动器挂载在`/mnt/c`下:  

![加载的 C 驱动器的屏幕截图](media/ls.png)

## <a name="what-is-bash"></a>什么是 Bash？
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是一种流行的基于文本的 shell 和命令语言。它是 Ubuntu 和其他 Linux 发行版以及 macOS 中包含的默认 shell。 用户在 shell 中键入命令以执行脚本和/或运行命令和工具来完成许多任务。

## <a name="how-does-this-work"></a>这是如何实现的？
请查看我们的[博客](https://blogs.msdn.microsoft.com/wsl/)，里面详细介绍了基础技术。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>为什么要使用 WSL 而不是在 VM 中使用 Linux？
WSL 需要较少的资源 （CPU、 内存和存储） 比完整的虚拟机。 WSL 还允许您运行 Linux 命令行工具和应用程序和 Windows 命令行中，桌面和应用商店应用，以及访问 Windows 文件从 Linux 中。 这样，如果你想在同一组文件上使用 Windows 应用和 Linux 命令行工具。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>为什么要使用，例如，而不是在 Windows 上的 Linux 上的 Ruby？
假设运行它们的环境的行为类似于 Linux 生成一些跨平台工具。 例如，一些工具假定他们可访问非常长文件路径或特定的文件/文件夹存在。 这通常会造成问题在通常的行为的 Windows 上以不同的方式从 Linux。

许多语言，如 Ruby 和节点通常是移植到，并在 Windows 上运行很好。 但是，并非所有节点/NPM 库所有者的 Ruby Gem 的端口及其库来支持 Windows，并且许多具有特定于 Linux 的依赖项。 通常，这可能导致系统使用此类工具和库生成和有时运行时错误或不需要的行为在 Windows 上遇到问题生成。

这些是只是一些导致许多人提出 Microsoft 以提高 Windows 的命令行工具和什么促使我们与 Canonical 启用本机 Bash 和 Linux 命令行工具在 Windows 上运行的问题。

## <a name="what-does-this-mean-for-powershell"></a>适用于 PowerShell，这意味着什么？
同时使用 OSS 项目时，有许多方案是非常有用，放入 Bash 从 PowerShell 提示。 Bash 支持是补充并增强了 Windows，从而允许 PowerShell 和 PowerShell 社区利用其他常用技术上的命令行中的值。

详细了解的 PowerShell 团队博客- [Bash Windows:为什么这真的非常棒和 PowerShell 的含义](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>在 WSL 运行所有 Linux 应用
不！ WSL 是旨在使用户需要使用这些运行 Bash 和 core 在 Windows 上的 Linux 命令行工具的工具。 

WSL does**不**旨在支持 GUI 桌面或应用程序 （例如 Gnome，KDE，等等。）  

此外，即使你将能够运行许多常用的服务器应用程序 (例如 Redis)，我们不建议用于托管生产服务 WSL – Microsoft 提供了多种解决方案，用于运行生产 Linux 工作负荷在 Azure 中，HYPER-V 和 Docker。 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL 中包括哪些 Windows Sku？
适用于 Linux 的 Windows 子系统是在桌面版本的 Windows 的 Windows 10 周年版及创意者更新或更高版本上可用。

从开始 Fall Creators update WSL 将在桌面和服务器 Windows Sku 上可用。

## <a name="what-processors-does-wsl-support"></a>WSL 支持哪些处理器？
WSL 支持 x64 和 ARM CPU。

## <a name="how-do-i-access-my-c-drive"></a>如何访问我的 c： 驱动器？
在本地计算机上的硬盘驱动器的装入点自动创建，并可以轻松访问 Windows 文件系统。 
 
**/mnt/\<驱动器号 > /**
 
用法示例为`cd /mnt/c`访问 c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>如何使用 Linux 应用使用 Windows 文件？

WSL 的优势之一能够访问你通过 Windows 和 Linux 应用程序或工具的文件。 

WSL 装载用的计算机的固定的驱动器`/mnt/<drive>`Linux 发行版中的文件夹。 例如，你`C:`下装载驱动器 `/mnt/c/` 

使用你已装载的驱动器，你可以编辑代码中，例如，`C:\dev\myproj\`使用[Visual Studio](https://visualstudio.microsoft.com/vs/) / 或[VS Code](https://code.visualstudio.com/)，并生成/测试 Linux 中的代码的访问通过的相同文件`/mnt/c/dev/myproj`。

> **重要说明**:使用 WSL 的主要限制之一是，不支持直接访问/更改使用 Windows 应用程序或工具的 Linux 发行版的文件系统中的文件。 请参阅：[不会更改使用 Windows 应用程序和工具的 Linux 文件](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>是在 Linux 驱动器中的文件不同于已装载的 Windows 驱动器？

1. Linux 根下的文件 (即`/`) 受 WSL 模拟 Linux 特定行为，包括但不是限于：
   * 包含无效 Windows 文件名字符的文件
   * 为非管理员用户创建的符号链接
   * 更改通过 chmod 和 chown 文件属性
   * 文件/文件夹区分大小写

2. 已装载的驱动器中的文件由 Windows 控制，并具有以下行为：
   * 支持区分大小写
   * 所有权限都设置为最能反映 Windows 权限

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>为什么有这么多的错误时运行的 apt-get 升级？
某些包使用我们尚未实现的功能。 `udev`例如，尚不支持并导致多`apt-get upgrade`错误。

若要修复与相关的问题`udev`，请执行以下步骤：

1. 写入到以下`/usr/sbin/policy-rc.d`并保存所做的更改。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 添加将执行权限 `/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 运行以下命令

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>如何卸载 WSL 分发？

在生成之前 1709 (版本 16299) 打开命令提示符并运行：
  ```batchfile
  lxrun /uninstall /full
  ```
  
通过右键单击应用磁贴上，单击卸载，或者通过 PowerShell 使用从应用商店安装 WSL 分发可以卸载其他任何 Windows 应用一样[ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。

## <a name="why-does-ping-generate-permission-denied-errors"></a>Ping 为什么生成权限被拒绝错误？
在 WSL 中生成 < 14926，ping 所需 WSL 中通过权限提升的控制台运行。 此问题已修复生成 14926 及更高版本。

## <a name="how-do-i-run-an-openssh-server"></a>如何运行 OpenSSH 服务器？
在 Windows 中的管理员权限才可在 WSL 中运行 OpenSSH。 若要运行的 OpenSSH 服务器，在作为管理员，Windows 上运行 Ubuntu 上的 Bash 或 CMD/PowerShell 提示符下使用管理员特权运行 bash.exe。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>为何收到"错误：0x80040306"当我尝试安装？
WSL 不支持旧版控制台中运行。 若要关闭旧版控制台：

1. 打开 WSL、 PowerShell 或 Cmd
1. 右键单击标题栏-> 属性-> 取消选中"使用传统控制台"
1. 单击“确定”

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>为何收到"错误：0x80040154"当我运行 bash.exe 升级 Windows 之后？
"Windows 子系统适用于 Linux"功能可能会禁用在 Windows 更新过程。 如果发生这种情况必须在重新启用 Windows 功能。 有关启用"Windows 子系统适用于 Linux"功能的说明可在[安装指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>如何更改显示语言的 WSL？
WSL 安装将尝试自动更改 Ubuntu 区域设置，以便与 Windows 安装程序的区域设置匹配。 如果您不需要此行为可以运行此命令以安装完成后更改 Ubuntu 区域设置。 必须重新启动 bash.exe 此更改才会生效。

下面的示例更改为 EN-US 区域设置：
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>为什么不具有 internet 访问 WSL
某些用户与特定的防火墙应用程序阻止 internet 访问在 WSL 中的报告的问题。 防火墙报告是：

1. Kaspersky
1. AVG
1. Avast

在某些情况下关闭防火墙允许访问。 只需时安装防火墙的某些情况下看起来以阻止访问。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>如何从 Windows 在 WSL 访问端口？
WSL 共享运行在 Windows 上的 Windows，IP 地址。 这种情况下可以访问本地主机上的任何端口例如有 web 内容上的端口 1234 可以 https://localhost:1234Windows 浏览器中。

## <a name="where-can-i-provide-feedback"></a>在哪里可以提供反馈？

您可以通过多种渠道分享反馈和提出问题：反馈和问题应在以下位置提出：
* 我们的[GitHub 问题跟踪程序](https://github.com/Microsoft/BashOnWindows/issues)
* 我们的[命令行 UserVoice 门户](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* 我们的[命令行团队博客](https://blogs.msdn.microsoft.com/commandline/)
* 通过 Twitter。请在 Twitter 上关注[ @richturn_ms ](https://twitter.com/richturn_MS)以了解新闻，更新等。
