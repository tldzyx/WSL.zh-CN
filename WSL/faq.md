---
title: 常见问题 (FAQ)
description: 有关适用于 Linux 的 Windows 子系统的常见问题。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: e3376f8dff83262577bc52fb3ac368b70b21d922
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122767"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a>有关适用于 Linux 的 Windows 子系统的常见问题

## <a name="what-is-windows-subsystem-for-linux-wsl"></a>什么是适用于 Linux 的 Windows 子系统 (WSL)？
适用于 Linux 的 Windows 子系统 (WSL) 是一项新的 Windows 10 功能, 使你能够直接在 Windows 上运行本机 Linux 命令行工具, 以及传统的 Windows 桌面和新式应用程序。

有关更多详细信息, 请参阅 "[关于页面](./about.md)，了解更多详细信息。

## <a name="who-is-wsl-for"></a>谁适合使用 WSL？
这主要是一种面向开发人员的工具, 尤其是 web 开发人员和使用开源项目的用户。 这允许需要/需要使用 Bash、通用 Linux 工具 (`sed`、 `awk`等) 的用户和许多 Linux 优先工具 (Ruby、Python 等) 在 Windows 上使用工具链。

## <a name="what-can-i-do-with-wsl"></a>我可以用 WSL 做些什么？
WSL 提供了一个名为 Bash 的应用程序, 该应用程序在启动时将打开运行 Bash shell 的 Windows 控制台。 使用 Bash, 你可以运行命令行 Linux 工具和应用。 例如, 键入`lsb_release -a`并按 enter, 将看到当前正在运行的 Linux 发行版的详细信息:

![发行版详细信息的屏幕截图](media/distro.png)

你还可以从 Linux Bash shell 内访问本地计算机的文件系统–你会发现在该`/mnt`文件夹下装入本地驱动器。 例如, 你`C:`的驱动器安装在下面`/mnt/c`:  

![装载的 C 驱动器的屏幕截图](media/ls.png)

## <a name="what-is-bash"></a>什么是 Bash？
[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是一种流行的基于文本的 shell 和命令语言。 它是 Ubuntu 和其他 Linux 发行版以及 macOS 中包含的默认 shell。 用户在 shell 中键入命令以执行脚本和/或运行命令和工具来完成许多任务。

## <a name="how-does-this-work"></a>这是如何实现的？
请查看我们的[博客](https://blogs.msdn.microsoft.com/wsl/), 了解基础技术的详细信息。

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a>为什么使用 WSL 而不是虚拟机中的 Linux？
WSL 所需的资源 (CPU、内存和存储) 比完整虚拟机少。 WSL 还允许您通过 Windows 命令行、桌面和应用商店应用程序运行 Linux 命令行工具和应用程序, 以及从 Linux 内访问 Windows 文件。 这使您可以在您需要时对同一组文件使用 Windows 应用和 Linux 命令行工具。

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a>我为什么要在 Linux 上而不是在 Windows 上使用 Ruby？
构建一些跨平台工具, 假设它们的运行环境的行为类似于 Linux。 例如, 某些工具假设它们能够访问非常长的文件路径, 或者存在特定的文件/文件夹。 这通常会导致 Windows 出现问题, 这些问题通常与 Linux 的行为不同。

许多语言 (例如 Ruby 和 node) 通常在 Windows 上移植到和运行良好。 但是, 并不是所有的 Ruby Gem 或 node/NPM 库所有者都将其库移植到支持 Windows, 许多都具有特定于 Linux 的依赖项。 这通常会导致使用此类工具和库生成的系统不能在 Windows 上生成, 有时运行时错误或不需要的行为。

这只是导致许多人要求 Microsoft 改进 Windows 命令行工具的一些问题, 并使我们与合作伙伴合作, 使本机 Bash 和 Linux 命令行工具能够在 Windows 上运行。

## <a name="what-does-this-mean-for-powershell"></a>对于 PowerShell 而言, 这意味着什么？
使用 OSS 项目时, 在许多情况下, 从 PowerShell 提示符中删除 Bash 非常有用。 Bash 支持是互补的, 在 Windows 上增强了命令行的价值, 使 PowerShell 和 PowerShell 社区能够利用其他常用技术。

有关详细信息, 请参阅 PowerShell 团队博客[--Bash for Windows:为什么它非常出色, 它对 PowerShell 意味着什么](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)

## <a name="can-i-run-all-linux-apps-in-wsl"></a>能否在 WSL 中运行所有 Linux 应用？
不！ WSL 是一种工具, 旨在使需要用户在 Windows 上运行 Bash 和核心 Linux 命令行工具的用户。 

WSL 不支持 GUI 桌面或应用程序 (例如, GNOME、KDE 等)  

此外, 即使您能够运行多个常用的服务器应用程序 (例如 Redis), 我们也不建议使用 WSL 来托管生产服务– Microsoft 提供了多种解决方案, 用于在 Azure、Hyper-v 和 Docker 中运行生产 Linux 工作负荷。 

## <a name="what-windows-skus-is-wsl-included-in"></a>WSL 包含在哪些 Windows Sku？
windows 10 周年和创意者更新或更高版本的 Windows 的桌面版本中提供了适用于 Linux 的 windows 子系统。

从秋季创意者更新开始, WSL 将在 Windows 的桌面和服务器 Sku 上可用。

## <a name="what-processors-does-wsl-support"></a>WSL 支持哪些处理器？
WSL 支持 x64 和 ARM Cpu。

## <a name="how-do-i-access-my-c-drive"></a>如何实现访问我的 C: 驱动器？
将自动创建本地计算机上的硬盘驱动器的装入点, 并提供对 Windows filesystem 的轻松访问。 
 
**/mnt/\<驱动器号 >/**
 
示例用法是`cd /mnt/c`访问 c:\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a>如何实现将 Windows 文件用于 Linux 应用？

WSL 的一个优点是, 可以通过 Windows 和 Linux 应用或工具访问你的文件。 

WSL 将计算机的固定驱动器装载到 Linux `/mnt/<drive>`发行版中的文件夹下。 例如, 你`C:`的驱动器安装在`/mnt/c/` 

使用已装载的驱动器, 你可以在中编辑代码 (例如`C:\dev\myproj\` , 使用[Visual Studio](https://visualstudio.microsoft.com/vs/) /或[VS Code](https://code.visualstudio.com/)), 并`/mnt/c/dev/myproj`通过访问相同的文件, 在 Linux 中生成/测试该代码。

> **重要说明**:使用 WSL 的一个重要限制是, 不支持直接访问/更改 Linux 发行版文件系统中的文件。 请参阅：[不要使用 Windows 应用和工具更改 Linux 文件](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a>Linux 驱动器中的文件是否与装载的 Windows 驱动器不同？

1. Linux 根下的文件 (即`/`) 由 WSL 控制, 它模拟 Linux 特定的行为, 包括但不限于:
   * 包含无效 Windows 文件名字符的文件
   * 为非管理员用户创建的符号链接
   * 通过 chmod 和 chown 更改文件属性
   * 文件/文件夹区分大小写

2. 装入驱动器中的文件由 Windows 控制, 并具有以下行为:
   * 支持区分大小写
   * 所有权限都设置为 "最佳" 反映 Windows 权限

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a>为什么在运行 apt 时出现如此多的错误-获取升级？
某些包使用我们尚未实现的功能。 `udev`例如, 尚不支持, 并导致几个`apt-get upgrade`错误。

若要解决与相关`udev`的问题, 请执行以下步骤:

1. 将以下项写入`/usr/sbin/policy-rc.d`到中, 并保存所做的更改。

    ```bash
    #!/bin/sh
    exit 101
    ```

2. 向添加执行权限`/usr/sbin/policy-rc.d`

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. 运行以下命令

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a>如何实现卸载 WSL 分发？

在1709之前的版本 (16299) 上, 打开命令提示符并运行:
  ```batchfile
  lxrun /uninstall /full
  ```
  
通过右键单击 "应用" 磁贴并单击 "卸载", 或使用[ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)通过 PowerShell, 可以像任何其他 Windows 应用一样卸载从应用商店安装的 WSL 分发。

## <a name="why-does-ping-generate-permission-denied-errors"></a>Ping 为什么会生成权限被拒绝错误？
在 WSL 生成 < 14926 中, ping 必需的 WSL 通过提升的控制台运行。 此问题已在版本14926和更高版本中解决。

## <a name="how-do-i-run-an-openssh-server"></a>如何实现运行 OpenSSH 服务器？
Windows 中的管理员权限需要在 WSL 中运行 OpenSSH。 若要运行 OpenSSH 服务器, 请在 Windows 上的 Ubuntu 上以管理员身份运行 Bash, 或从具有管理员权限的 CMD/PowerShell 提示符运行 bash。

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a>为什么当我尝试安装时会出现 "错误:0x80040306 "？
WSL 不支持在旧控制台中运行。 关闭旧版控制台:

1. 打开 WSL、PowerShell 或 Cmd
1. 右键单击标题栏-> 属性-> 取消选中 "使用旧版控制台"
1. 单击“确定”

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a>为什么会出现 "错误:升级 Windows 后, 0x80040154 "
Windows 更新期间可能禁用了 "适用于 Linux 的 Windows 子系统" 功能。 如果出现这种情况, 则必须重新启用 Windows 功能。 有关启用 "适用于 Linux 的 Windows 子系统" 功能的说明, 请参阅[安装指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

## <a name="how-do-i-change-the-display-language-of-wsl"></a>如何实现更改 WSL 的显示语言？
WSL 安装将尝试自动更改 Ubuntu 区域设置以与 Windows 安装的区域设置相匹配。 如果不想要此行为, 可以在安装完成后运行此命令来更改 Ubuntu 区域设置。 要使此更改生效, 您必须重新启动 bash。

下面的示例将区域设置更改为 en-us:
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a>为什么无法从 WSL 访问 internet？
某些用户已报告在 WSL 中阻止 internet 访问的特定防火墙应用程序的问题。 报告的防火墙包括:

1. Kaspersky 等
1. AVG
1. Avast

在某些情况下, 关闭防火墙允许进行访问。 在某些情况下, 只需安装防火墙即可阻止访问。

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a>如何实现从 Windows 中的 WSL 访问端口？
WSL 共享 Windows 的 IP 地址, 因为它在 Windows 上运行。 因此, 你可以访问 localhost 上的任何端口 (例如, 如果你的 web 内容位于端口 1234 https://localhost:1234 上, 你可以进入 Windows 浏览器中)。

## <a name="how-can-i-back-up-my-wsl-distros"></a>如何备份我的 WSL 发行版？

Windows 版本1809及更高版本中提供了备份发行版的最佳方式。 你可以使用`wsl --export`命令将整个分发导出到 tarball。 然后, 可以使用`wsl --import`命令将此发行版导入 WSL, 使你能够备份和保存 WSL 分发的状态。 

请注意, 备份 Appdata 文件夹 (如 Windows 备份) 中的文件的传统备份服务不会损坏 Linux 文件。 



## <a name="where-can-i-provide-feedback"></a>在哪里可以提供反馈？

可以通过多个渠道共享反馈和提问:反馈和问题应定向到:
* [GitHub 问题跟踪](https://github.com/Microsoft/BashOnWindows/issues)器
* 我们的[命令行 UserVoice 门户](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)
* 我们的[命令行团队博客](https://blogs.msdn.microsoft.com/commandline/)
* 通过 Twitter。 请在 Twitter 上关注[@richturn_ms](https://twitter.com/richturn_MS)以了解新闻，更新等。
