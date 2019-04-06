---
title: Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 windows server 的 windows 子系统
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063615"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="aee69-104">Windows Server 安装指南</span><span class="sxs-lookup"><span data-stu-id="aee69-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="aee69-105">适用于 Windows Server 2019 和更高版本</span><span class="sxs-lookup"><span data-stu-id="aee69-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="aee69-106">在 / / Build2017，Microsoft 宣布将适用于 Linux 的 Windows 子系统[可在 Windows Server 上](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。</span><span class="sxs-lookup"><span data-stu-id="aee69-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="aee69-107">这些说明了解如何运行适用于 Linux 的 Windows Server 1709 及更高版本的 Windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="aee69-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="aee69-108">适用于 Linux (WSL) 启用的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="aee69-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="aee69-109">您可以在 Windows 上运行的 Linux 发行版之前，必须启用"Windows 子系统适用于 Linux"可选功能，并重新启动。</span><span class="sxs-lookup"><span data-stu-id="aee69-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="aee69-110">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="aee69-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="aee69-111">重新启动计算机时提示。</span><span class="sxs-lookup"><span data-stu-id="aee69-111">Restart your computer when prompted.</span></span> <span data-ttu-id="aee69-112">**需要此重新启动后**为了确保 WSL 可以启动的可信的执行环境。</span><span class="sxs-lookup"><span data-stu-id="aee69-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="aee69-113">下载的 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="aee69-113">Download a Linux distro</span></span>

<span data-ttu-id="aee69-114">请按照[这些说明](install-manual.md)若要下载你最喜爱的 Linux 分发。</span><span class="sxs-lookup"><span data-stu-id="aee69-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="aee69-115">提取和安装的 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="aee69-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="aee69-116">既然您已经下载发行版，提取其内容，并手动安装发行版：</span><span class="sxs-lookup"><span data-stu-id="aee69-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="aee69-117">提取`<distro>.appx`包的内容，例如，使用 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="aee69-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. <span data-ttu-id="aee69-118">运行发行版启动器要完成安装，请运行发行版启动器应用程序目标文件夹中名为`<distro>.exe`。</span><span class="sxs-lookup"><span data-stu-id="aee69-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="aee69-119">例如： `ubuntu.exe`，等等。</span><span class="sxs-lookup"><span data-stu-id="aee69-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server 上的展开的 Ubuntu 发行版](media/server-appx-expand.png)

    > **<span data-ttu-id="aee69-121">疑难解答</span><span class="sxs-lookup"><span data-stu-id="aee69-121">Troubleshooting</span></span>**
    > * <span data-ttu-id="aee69-122">**安装失败，出现错误 0x8007007e**:您的系统不支持 WSL 时发生此错误。</span><span class="sxs-lookup"><span data-stu-id="aee69-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="aee69-123">请确保：</span><span class="sxs-lookup"><span data-stu-id="aee69-123">Make sure that:</span></span>
    >   * <span data-ttu-id="aee69-124">正在运行 Windows 生成 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="aee69-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="aee69-125">[检查你的生成](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="aee69-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="aee69-126">Linux 可选组件的 Windows 子系统，并重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="aee69-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="aee69-127">[请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="aee69-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="aee69-128">将你的发行版路径添加到 Windows 环境路径 (`C:\Users\Administrator\Ubuntu`在此示例中)，例如，使用 Powershell:</span><span class="sxs-lookup"><span data-stu-id="aee69-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="aee69-129">现在可以启动任何路径从发行版，通过键入`<distro>.exe`。</span><span class="sxs-lookup"><span data-stu-id="aee69-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="aee69-130">例如：</span><span class="sxs-lookup"><span data-stu-id="aee69-130">For example:</span></span> `ubuntu.exe`

<span data-ttu-id="aee69-131">安装 Linux 发行版后，您必须[初始化新的发行版实例](initialize-distro.md)之前使用发行版。</span><span class="sxs-lookup"><span data-stu-id="aee69-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
