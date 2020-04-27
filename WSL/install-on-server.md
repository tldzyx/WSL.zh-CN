---
title: 在 Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256390"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="ff98b-104">Windows Server 安装指南</span><span class="sxs-lookup"><span data-stu-id="ff98b-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="ff98b-105">适用于 Windows Server 2019 及更高版本</span><span class="sxs-lookup"><span data-stu-id="ff98b-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="ff98b-106">在 //Build2017 时，Microsoft 宣布适用于 Linux 的 Windows 子系统将[在 Windows Server 上可用](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。</span><span class="sxs-lookup"><span data-stu-id="ff98b-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="ff98b-107">这些说明将介绍如何在 Windows Server 1709 及更高版本上运行适用于 Linux 的 Windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="ff98b-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="ff98b-108">启用适用于 Linux 的 Windows 子系统 (WSL)</span><span class="sxs-lookup"><span data-stu-id="ff98b-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="ff98b-109">必须启用“适用于 Linux 的 Windows 子系统”可选功能并重启，然后才能在 Windows 上运行 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="ff98b-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="ff98b-110">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="ff98b-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="ff98b-111">出现提示时，重启计算机。</span><span class="sxs-lookup"><span data-stu-id="ff98b-111">Restart your computer when prompted.</span></span> <span data-ttu-id="ff98b-112">为了确保 WSL 可以启动可信的执行环境，**必须进行此重启**。</span><span class="sxs-lookup"><span data-stu-id="ff98b-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="ff98b-113">下载 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="ff98b-113">Download a Linux distro</span></span>

<span data-ttu-id="ff98b-114">按照[这些说明](install-manual.md)下载你最喜爱的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="ff98b-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="ff98b-115">提取并安装 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="ff98b-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="ff98b-116">下载发行版后，请提取其内容，并手动安装该发行版：</span><span class="sxs-lookup"><span data-stu-id="ff98b-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="ff98b-117">提取 `<distro>.appx` 包的内容，例如，使用 PowerShell：</span><span class="sxs-lookup"><span data-stu-id="ff98b-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. <span data-ttu-id="ff98b-118">运行发行版启动器来完成安装，请在名为 `<distro>.exe` 的目标文件夹中运行发行版启动器应用程序。</span><span class="sxs-lookup"><span data-stu-id="ff98b-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="ff98b-119">例如：`ubuntu.exe`，等等。</span><span class="sxs-lookup"><span data-stu-id="ff98b-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server 上展开的 Ubuntu 发行版](media/server-appx-expand.png)

    > <span data-ttu-id="ff98b-121">**疑难解答**</span><span class="sxs-lookup"><span data-stu-id="ff98b-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="ff98b-122">**安装失败并出现错误 0x8007007e**：当系统不支持 WSL 时会出现此错误。</span><span class="sxs-lookup"><span data-stu-id="ff98b-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="ff98b-123">请确保：</span><span class="sxs-lookup"><span data-stu-id="ff98b-123">Make sure that:</span></span>
    >   * <span data-ttu-id="ff98b-124">运行 Windows 内部版本 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ff98b-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="ff98b-125">[检查内部版本](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="ff98b-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="ff98b-126">已启用“适用于 Linux 的 Windows 子系统”可选组件，并已重启计算机。</span><span class="sxs-lookup"><span data-stu-id="ff98b-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="ff98b-127">[确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="ff98b-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="ff98b-128">将你的发行版路径添加到 Windows 环境 PATH 中（在本例中为 `C:\Users\Administrator\Ubuntu`），例如，使用 Powershell：</span><span class="sxs-lookup"><span data-stu-id="ff98b-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="ff98b-129">现在，你可以从任何路径通过键入 `<distro>.exe` 来启动你的发行版。</span><span class="sxs-lookup"><span data-stu-id="ff98b-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="ff98b-130">例如：`ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="ff98b-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="ff98b-131">安装你的 Linux 发行版后，必须先[初始化新的发行版实例](initialize-distro.md)，然后才能使用该发行版。</span><span class="sxs-lookup"><span data-stu-id="ff98b-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
