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
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="05c8e-104">手动下载 Linux 发行版包的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="05c8e-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="05c8e-105">有几种方案在其中可能不能 （或希望） 以，安装 WSL Linux 发行版通过 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="05c8e-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="05c8e-106">具体而言，您可能运行的 Windows Server 或 Long-Term Servicing (LTSB/LTSC) 桌面 Microsoft Store 或你公司的网络策略和/或管理员不允许在环境中的 Microsoft Store 的使用情况不支持的 OS SKU。</span><span class="sxs-lookup"><span data-stu-id="05c8e-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSB/LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="05c8e-107">在这些情况下，而 WSL 自身可用，如何你下载和安装的 Linux 发行版在 WSL 中，如果您不能访问应用商店？</span><span class="sxs-lookup"><span data-stu-id="05c8e-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="05c8e-108">注意：**命令行 shell 环境包括 Cmd、 PowerShell 和 Linux/WSL 发行版不允许运行 Windows 10 S 模式**。</span><span class="sxs-lookup"><span data-stu-id="05c8e-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="05c8e-109">存在此限制是为了确保 S 模式提供的完整性和安全性目标：读取[此文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)有关详细信息。</span><span class="sxs-lookup"><span data-stu-id="05c8e-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="05c8e-110">下载发行版</span><span class="sxs-lookup"><span data-stu-id="05c8e-110">Downloading distros</span></span>

<span data-ttu-id="05c8e-111">如果 Microsoft Store 应用不可用，您可以下载并手动安装的 Linux 发行版通过单击以下链接：</span><span class="sxs-lookup"><span data-stu-id="05c8e-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="05c8e-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="05c8e-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="05c8e-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="05c8e-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="05c8e-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="05c8e-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="05c8e-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="05c8e-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="05c8e-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="05c8e-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux)
* [<span data-ttu-id="05c8e-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="05c8e-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="05c8e-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="05c8e-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="05c8e-119">WSL 的 fedora Remix</span><span class="sxs-lookup"><span data-stu-id="05c8e-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="05c8e-120">这将导致`<distro>.appx`包下载到您选择的文件夹。</span><span class="sxs-lookup"><span data-stu-id="05c8e-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="05c8e-121">请按照[安装说明](#installing-your-distro)安装下载的 distro(s)。</span><span class="sxs-lookup"><span data-stu-id="05c8e-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="05c8e-122">通过命令行下载发行版</span><span class="sxs-lookup"><span data-stu-id="05c8e-122">Downloading distros via the command line</span></span>
<span data-ttu-id="05c8e-123">如果您愿意，也可以下载你首选的 distro(s) 通过命令行：</span><span class="sxs-lookup"><span data-stu-id="05c8e-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="05c8e-124">使用 PowerShell 下载</span><span class="sxs-lookup"><span data-stu-id="05c8e-124">Download using PowerShell</span></span>
 <span data-ttu-id="05c8e-125">若要下载使用 PowerShell 的发行版，请使用[Invoke-webrequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="05c8e-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="05c8e-126">下面是示例说明下载 Ubuntu 16.04。</span><span class="sxs-lookup"><span data-stu-id="05c8e-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="05c8e-127">如果下载所需时间较长时间，通过设置将关闭进度栏 `$ProgressPreference = 'SilentlyContinue'`</span><span class="sxs-lookup"><span data-stu-id="05c8e-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="05c8e-128">使用 curl 下载</span><span class="sxs-lookup"><span data-stu-id="05c8e-128">Download using curl</span></span>
<span data-ttu-id="05c8e-129">Windows 10 Spring 2018 更新 （或更高版本） 包括热门[curl 命令行实用程序](https://curl.haxx.se/)调用命令行中的 web 请求 (即 HTTP GET、 POST、 PUT、 等命令)。</span><span class="sxs-lookup"><span data-stu-id="05c8e-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="05c8e-130">可以使用`curl.exe`下载在更高版本的发行版：</span><span class="sxs-lookup"><span data-stu-id="05c8e-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="05c8e-131">在上述示例中，`curl.exe`执行 (不只是`curl`) 以确保，在 PowerShell 中，实际 curl 可执行文件调用，不别名的 PowerShell curl [Invoke-webrequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span><span class="sxs-lookup"><span data-stu-id="05c8e-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/en-us/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="05c8e-132">注意：使用`curl`可能更可取，如果您需要调用/脚本使用 Cmd shell 中的下载步骤和/或`.bat`  /  `.cmd`脚本。</span><span class="sxs-lookup"><span data-stu-id="05c8e-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="05c8e-133">安装发行版</span><span class="sxs-lookup"><span data-stu-id="05c8e-133">Installing your distro</span></span>
<span data-ttu-id="05c8e-134">有关如何安装已下载的 distro(s) 的说明，请参阅[Windows 桌面](install-win10.md)或[Windows Server](install-on-server.md)安装说明。</span><span class="sxs-lookup"><span data-stu-id="05c8e-134">For instructions on how to install your downloaded distro(s), please refer to the [Windows Desktop](install-win10.md) or [Windows Server](install-on-server.md) installation instructions.</span></span>
