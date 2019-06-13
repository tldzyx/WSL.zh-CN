---
title: 手动下载用于 Linux (WSL) 发行版的 Windows 子系统
description: 有关如何手动下载 Linux 分发版的 Windows 子系统的说明。
keywords: BashOnWindows，bash、 wsl、 windows、 linux，WSL，适用于 windows 子系统的 windows 子系统、 发行版、 ubuntu、 openSUSE、 SLES，debian、 kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 669c017c97aba70c107484b32acd99296265d84a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035033"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>手动下载 Linux 发行版包的 Windows 子系统

有几种方案在其中可能不能 （或希望） 以，安装 WSL Linux 发行版通过 Microsoft Store。 具体而言，您可能运行的 Windows Server 或 Long-Term Servicing (LTSB/LTSC) 桌面 Microsoft Store 或你公司的网络策略和/或管理员不允许在环境中的 Microsoft Store 的使用情况不支持的 OS SKU。

在这些情况下，而 WSL 自身可用，如何你下载和安装的 Linux 发行版在 WSL 中，如果您不能访问应用商店？

> 注意：**命令行 shell 环境包括 Cmd、 PowerShell 和 Linux/WSL 发行版不允许运行 Windows 10 S 模式**。 存在此限制是为了确保 S 模式提供的完整性和安全性目标：读取[此文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)有关详细信息。

## <a name="downloading-distros"></a>下载发行版

如果 Microsoft Store 应用不可用，您可以下载并手动安装的 Linux 发行版通过单击以下链接：
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL 的 fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

这将导致`<distro>.appx`包下载到您选择的文件夹。 请按照[安装说明](#installing-your-distro)安装下载的 distro(s)。

## <a name="downloading-distros-via-the-command-line"></a>通过命令行下载发行版
如果您愿意，也可以下载你首选的 distro(s) 通过命令行：

 ### <a name="download-using-powershell"></a>使用 PowerShell 下载
 若要下载使用 PowerShell 的发行版，请使用[Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet。 下面是示例说明下载 Ubuntu 16.04。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 如果下载所需时间较长时间，通过设置将关闭进度栏 `$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>使用 curl 下载
Windows 10 Spring 2018 更新 （或更高版本） 包括热门[curl 命令行实用程序](https://curl.haxx.se/)调用命令行中的 web 请求 (即 HTTP GET、 POST、 PUT、 等命令)。 可以使用`curl.exe`下载在更高版本的发行版：

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

在上述示例中，`curl.exe`执行 (不只是`curl`) 以确保，在 PowerShell 中，实际 curl 可执行文件调用，不别名的 PowerShell curl [Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)

> 注意：使用`curl`可能更可取，如果您需要调用/脚本使用 Cmd shell 中的下载步骤和/或`.bat`  /  `.cmd`脚本。

## <a name="installing-your-distro"></a>安装发行版
有关如何安装已下载的 distro(s) 的说明，请参阅[Windows 桌面](install-win10.md)或[Windows Server](install-on-server.md)安装说明。
