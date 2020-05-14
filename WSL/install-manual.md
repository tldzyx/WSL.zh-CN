---
title: 手动下载适用于 Linux 的 Windows 子系统 (WSL) 发行版
description: 有关如何手动下载适用于 Linux 的 Windows 子系统发行版的说明。
keywords: BashOnWindows, bash, wsl, Windows, 适用于 Linux 的 Windows 子系统, WSL, windows 子系统, 发行版, ubuntu, openSUSE, SLES, debian, kali
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: b1720d01d492f1dccce8c2e1d2ff430f7769a42e
ms.sourcegitcommit: 3fb40fd65b34a5eb26b213a0df6a3b2746b7a9b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/12/2020
ms.locfileid: "83235823"
---
# <a name="manually-download-windows-subsystem-for-linux-distro-packages"></a><span data-ttu-id="b9025-104">手动下载适用于 Linux 的 Windows 子系统发行版包</span><span class="sxs-lookup"><span data-stu-id="b9025-104">Manually download Windows Subsystem for Linux distro packages</span></span>

<span data-ttu-id="b9025-105">在许多情况下，你可能无法（或不想）通过 Microsoft Store 安装 WSL Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="b9025-105">There are several scenarios in which you may not be able (or want) to, install WSL Linux distros via the Microsoft Store.</span></span> <span data-ttu-id="b9025-106">具体而言，你可能正在运行不支持 Microsoft Store 的 Windows Server 或长期服务 (LTSC) 桌面操作系统 SKU，或者你的公司网络策略和/或管理员不允许在你的环境中使用 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="b9025-106">Specifically, you may be running a Windows Server or Long-Term Servicing (LTSC) desktop OS SKU that doesn't support Microsoft Store, or your corporate network policies and/or admins to not permit Microsoft Store usage in your environment.</span></span>

<span data-ttu-id="b9025-107">在这些情况下，虽然 WSL 本身可用，但如果你无法访问应用商店，如何下载并在 WSL 中安装 Linux 发行版？</span><span class="sxs-lookup"><span data-stu-id="b9025-107">In these cases, while WSL itself is available, how do you download and install Linux distros in WSL if you can't access the store?</span></span>

> <span data-ttu-id="b9025-108">注意：**命令行 shell 环境（包括 Cmd、PowerShell 和 Linux/WSL 发行版）不允许在 Windows 10 S 模式下运行**。</span><span class="sxs-lookup"><span data-stu-id="b9025-108">Note: **Command-line shell environments including Cmd, PowerShell, and Linux/WSL distros are not permitted to run on Windows 10 S Mode**.</span></span> <span data-ttu-id="b9025-109">存在此限制是为了确保 S 模式提供的完整性和安全目标：有关详细信息，请参阅[此文章](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/)。</span><span class="sxs-lookup"><span data-stu-id="b9025-109">This restriction exists in order to ensure the integrity and safety goals that S Mode delivers: Read [this post](https://blogs.msdn.microsoft.com/commandline/2017/05/18/will-linux-distros-run-on-windows-10-s/) for more information.</span></span>

## <a name="downloading-distros"></a><span data-ttu-id="b9025-110">下载发行版</span><span class="sxs-lookup"><span data-stu-id="b9025-110">Downloading distros</span></span>

<span data-ttu-id="b9025-111">如果 Microsoft Store 应用不可用，则可以通过单击以下链接来下载并手动安装 Linux 发行版：</span><span class="sxs-lookup"><span data-stu-id="b9025-111">If the Microsoft Store app is not available, you can download and manually install Linux distros by clicking these links:</span></span>
* [<span data-ttu-id="b9025-112">Ubuntu 18.04</span><span class="sxs-lookup"><span data-stu-id="b9025-112">Ubuntu 18.04</span></span>](https://aka.ms/wsl-ubuntu-1804)
* [<span data-ttu-id="b9025-113">Ubuntu 18.04 ARM</span><span class="sxs-lookup"><span data-stu-id="b9025-113">Ubuntu 18.04 ARM</span></span>](https://aka.ms/wsl-ubuntu-1804-arm)
* [<span data-ttu-id="b9025-114">Ubuntu 16.04</span><span class="sxs-lookup"><span data-stu-id="b9025-114">Ubuntu 16.04</span></span>](https://aka.ms/wsl-ubuntu-1604)
* [<span data-ttu-id="b9025-115">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="b9025-115">Debian GNU/Linux</span></span>](https://aka.ms/wsl-debian-gnulinux)
* [<span data-ttu-id="b9025-116">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="b9025-116">Kali Linux</span></span>](https://aka.ms/wsl-kali-linux-new)
* [<span data-ttu-id="b9025-117">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="b9025-117">OpenSUSE Leap 42</span></span>](https://aka.ms/wsl-opensuse-42)
* [<span data-ttu-id="b9025-118">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="b9025-118">SUSE Linux Enterprise Server 12</span></span>](https://aka.ms/wsl-sles-12)
* [<span data-ttu-id="b9025-119">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="b9025-119">Fedora Remix for WSL</span></span>](https://github.com/WhitewaterFoundry/WSLFedoraRemix/releases/)

<span data-ttu-id="b9025-120">这将导致 `<distro>.appx` 包下载到你选择的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b9025-120">This will cause the `<distro>.appx` packages to download to a folder of your choosing.</span></span> <span data-ttu-id="b9025-121">按照[安装说明](#installing-your-distro)来安装你下载的发行版。</span><span class="sxs-lookup"><span data-stu-id="b9025-121">Follow the [installation instructions](#installing-your-distro) to install your downloaded distro(s).</span></span>

## <a name="downloading-distros-via-the-command-line"></a><span data-ttu-id="b9025-122">通过命令行下载发行版</span><span class="sxs-lookup"><span data-stu-id="b9025-122">Downloading distros via the command line</span></span>
<span data-ttu-id="b9025-123">如果愿意，也可以通过命令行下载你首选的发行版：</span><span class="sxs-lookup"><span data-stu-id="b9025-123">If you prefer, you can also download your preferred distro(s) via the command line:</span></span>

 ### <a name="download-using-powershell"></a><span data-ttu-id="b9025-124">使用 PowerShell 下载</span><span class="sxs-lookup"><span data-stu-id="b9025-124">Download using PowerShell</span></span>
 <span data-ttu-id="b9025-125">若要使用 PowerShell 下载发行版，请使用 [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet。</span><span class="sxs-lookup"><span data-stu-id="b9025-125">To download distros using PowerShell, use the [Invoke-WebRequest](https://msdn.microsoft.com/powershell/reference/5.1/microsoft.powershell.utility/invoke-webrequest) cmdlet.</span></span> <span data-ttu-id="b9025-126">下面是用于下载 Ubuntu 16.04 的示例说明。</span><span class="sxs-lookup"><span data-stu-id="b9025-126">Here's a sample instruction to download Ubuntu 16.04.</span></span>

```powershell
Invoke-WebRequest -Uri https://aka.ms/wsl-ubuntu-1604 -OutFile Ubuntu.appx -UseBasicParsing
```

> [!TIP]
> <span data-ttu-id="b9025-127">如果下载需要很长时间，请通过设置 `$ProgressPreference = 'SilentlyContinue'` 来关闭进度栏</span><span class="sxs-lookup"><span data-stu-id="b9025-127">If the download is taking a long time, turn off the progress bar by setting `$ProgressPreference = 'SilentlyContinue'`</span></span>

### <a name="download-using-curl"></a><span data-ttu-id="b9025-128">使用 curl 下载</span><span class="sxs-lookup"><span data-stu-id="b9025-128">Download using curl</span></span>
<span data-ttu-id="b9025-129">Windows 10 Spring 2018 更新（或更高版本）包括了流行的 [curl 命令行实用程序](https://curl.haxx.se/)，你可以使用它从命令行调用 web 请求（即 HTTP GET、POST、PUT 等命令）。</span><span class="sxs-lookup"><span data-stu-id="b9025-129">Windows 10 Spring 2018 Update (or later) includes the popular [curl command-line utility](https://curl.haxx.se/) with which you can invoke web requests (i.e. HTTP GET, POST, PUT, etc. commands) from the command line.</span></span> <span data-ttu-id="b9025-130">可以使用 `curl.exe` 下载上述发行版：</span><span class="sxs-lookup"><span data-stu-id="b9025-130">You can use `curl.exe` to download the above distros:</span></span>

```console
curl.exe -L -o ubuntu-1604.appx https://aka.ms/wsl-ubuntu-1604
```

<span data-ttu-id="b9025-131">在上面的示例中，将执行 `curl.exe`（而不仅仅是 `curl`），以确保在 PowerShell 中调用真正的 curl 可执行文件，而不是调用 [Invoke WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6) 的 PowerShell curl 别名</span><span class="sxs-lookup"><span data-stu-id="b9025-131">In the above example, `curl.exe` is executed (not just `curl`) to ensure that, in PowerShell, the real curl executable is invoked, not the PowerShell curl alias for [Invoke-WebRequest](https://docs.microsoft.com/powershell/module/microsoft.powershell.utility/invoke-webrequest?view=powershell-6)</span></span>

> <span data-ttu-id="b9025-132">注意：如果必须使用 Cmd shell 和/或 `.bat` / `.cmd` 脚本来调用/编写下载步骤，则使用 `curl` 可能更好。</span><span class="sxs-lookup"><span data-stu-id="b9025-132">Note: Using `curl` might be preferable if you have to invoke/script download steps using Cmd shell and/or `.bat` / `.cmd` scripts.</span></span>

## <a name="installing-your-distro"></a><span data-ttu-id="b9025-133">安装发行版</span><span class="sxs-lookup"><span data-stu-id="b9025-133">Installing your distro</span></span>
<span data-ttu-id="b9025-134">如果使用的是 Windows 10，则可以使用 PowerShell 安装发行版。</span><span class="sxs-lookup"><span data-stu-id="b9025-134">If you're using Windows 10 you can install your distro with PowerShell.</span></span> <span data-ttu-id="b9025-135">只需导航到包含从上面下载的发行版的文件夹，然后在该目录中运行以下命令，其中，`app_name` 是 distro.appx 文件的名称。</span><span class="sxs-lookup"><span data-stu-id="b9025-135">Simply navigate to folder containing the distro downloaded from above, and in that directory run the following command where `app_name` is the name of your distro .appx file.</span></span>  
```Powershell
Add-AppxPackage .\app_name.appx
```

<span data-ttu-id="b9025-136">如果使用的是 Windows server，可以在 [Windows Server](install-on-server.md) 文档页上找到安装说明。</span><span class="sxs-lookup"><span data-stu-id="b9025-136">If you are using Windows server you can find the install instructions on the [Windows Server](install-on-server.md) documentation page.</span></span>

<span data-ttu-id="b9025-137">在安装发行版后，请参阅[初始化步骤](initialize-distro.md)页来初始化新的发行版。</span><span class="sxs-lookup"><span data-stu-id="b9025-137">Once your distro is installed please refer to the [Initialization Steps](initialize-distro.md) page to initialize your new distro.</span></span>
