---
title: 手动下载适用于 Linux 的 Windows 子系统 (WSL) 发行版
description: 有关如何手动下载适用于 Linux 的 Windows 子系统分发的说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, WSL, windows 子系统, 发行版, ubuntu, openSUSE, SLES, debian, kali
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: ded81ec9672d75203e0d289c551c86cd90bde606
ms.sourcegitcommit: 9175a28f04573f25338358faf61d73b1a5d1ade6
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/06/2019
ms.locfileid: "68832093"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a>手动下载适用于 Linux 的 Windows 子系统发行版包

在多种情况下, 你可能无法 (或不想) 通过 Microsoft Store 安装 WSL Linux 发行版。 具体而言, 你可能运行的是不支持 Microsoft Store 或公司网络策略和/或管理员在你的环境中不允许 Microsoft Store 使用的 Windows Server 或长期服务 (LTSC) 桌面操作系统 SKU。

在这些情况下, 虽然 WSL 本身可用, 但如果你无法访问应用商店, 如何下载并在 WSL 中安装 Linux 发行版？

> 注意:**不允许在 Windows 10 S 模式上运行命令行 shell 环境, 包括 Cmd、PowerShell 和 Linux/WSL 发行版**。 存在此限制是为了确保模式提供的完整性和安全性目标:有关详细信息, 请阅读[此文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)。

## <a name="downloading-distros"></a>下载发行版

如果 Microsoft Store 应用不可用, 则可以通过单击以下链接下载并手动安装 Linux 发行版:
* [Ubuntu 18.04](https://aka.ms/wsl-ubuntu-1804)
* [Ubuntu 18.04 ARM](https://aka.ms/wsl-ubuntu-1804-arm)
* [Ubuntu 16.04](https://aka.ms/wsl-ubuntu-1604)
* [Debian GNU/Linux](https://aka.ms/wsl-debian-gnulinux)
* [Kali Linux](https://aka.ms/wsl-kali-linux-new)
* [OpenSUSE Leap 42](https://aka.ms/wsl-opensuse-42)
* [SUSE Linux Enterprise Server 12](https://aka.ms/wsl-sles-12)
* [WSL 的 Fedora Remix](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

这会导致`<distro>.appx`包下载到你选择的文件夹。 按照[安装说明](#Installing-your-distro)安装下载的发行版。

## <a name="downloading-distros-via-the-command-line"></a>通过命令行下载发行版
如果愿意, 也可以通过命令行下载首选的发行版:

 ### <a name="download-using-powershell"></a>使用 PowerShell 下载
 若要使用 PowerShell 下载发行版, 请使用[WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet。 下面是下载 Ubuntu 16.04 的示例说明。

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> 如果下载需要很长时间, 请通过设置来关闭进度栏`$ProgressPreference = 'SilentlyContinue'`

### <a name="download-using-curl"></a>使用卷下载
Windows 10 春季2018更新 (或更高版本) 包含可从命令行调用 web 请求 (例如 HTTP GET、POST、PUT 等命令) 的常用[卷命令行实用程序](https://curl.haxx.se/)。 您可以使用`curl.exe`下载上述发行版:

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

在上面的示例中`curl.exe` , 执行了 (而`curl`不只是) 以确保调用了实卷可执行文件, 而不是调用[WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)的 powershell 卷别名。

> 注意:使用`curl` Cmd shell 和/或`.bat`  /  `.cmd`脚本时, 使用可能更可取。

## <a name="installing-your-distro"></a>安装发行版
如果使用的是 Windows 10, 则可以使用 PowerShell 安装发行版。 只需导航到包含上面下载的发行版的文件夹, 并在该目录中运行以下命令`app_name` , 其中是发行版文件的名称。  
```Powershell
Add-AppxPackage .\app_name.appx
```

如果使用的是 Windows server, 可以在[Windows server](install-on-server.md)文档页上找到安装说明。

安装发行版后, 请参阅[Intilization 步骤](initialize-distro.md)页, 初始化新的发行版。
