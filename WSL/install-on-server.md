---
title: 在 Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows，bash，wsl，windows，适用于 linux 的 windows 子系统，windowssubsystem，ubuntu，windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 51a2e3f3443ed9b1ba3d8ab79977f22839ee0283
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269785"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="9a4dc-104">Windows Server 安装指南</span><span class="sxs-lookup"><span data-stu-id="9a4dc-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="9a4dc-105">适用于 Windows Server 2019 及更高版本</span><span class="sxs-lookup"><span data-stu-id="9a4dc-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="9a4dc-106">在 //Build2017，Microsoft 宣布适用于 Linux 的 Windows 子系统[将在 Windows Server 上提供](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="9a4dc-107">这些说明将介绍如何在 Windows Server 1709 及更高版本上运行适用于 Linux 的 Windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="9a4dc-108">启用适用于 Linux 的 Windows 子系统 (WSL)</span><span class="sxs-lookup"><span data-stu-id="9a4dc-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="9a4dc-109">在 Windows 上运行 Linux 发行版之前，您必须启用“适用于 Linux 的 Windows 的子系统”可选功能并重新启动。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="9a4dc-110">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="9a4dc-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="9a4dc-111">出现提示时重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-111">Restart your computer when prompted.</span></span> <span data-ttu-id="9a4dc-112">**必须重新启动**，这是为了确保 WSL 可以启动受信任的执行环境。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="9a4dc-113">下载 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="9a4dc-113">Download a Linux distro</span></span>

<span data-ttu-id="9a4dc-114">请按照[这些说明](install-manual.md)下载您最喜爱的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="9a4dc-115">提取并安装 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="9a4dc-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="9a4dc-116">下载发行版后，请提取其内容，并手动安装发行版：</span><span class="sxs-lookup"><span data-stu-id="9a4dc-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="9a4dc-117">`<distro>.appx`提取包的内容，例如，使用 PowerShell：</span><span class="sxs-lookup"><span data-stu-id="9a4dc-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="9a4dc-118">运行发行版启动器以完成安装，并在名为`<distro>.exe`的目标文件夹中运行发行版启动器应用程序。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="9a4dc-119">例如： `ubuntu.exe`等。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server 上的扩展 Ubuntu 发行版](media/server-appx-expand.png)

    > <span data-ttu-id="9a4dc-121">**疑难解答**</span><span class="sxs-lookup"><span data-stu-id="9a4dc-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="9a4dc-122">**安装失败，出现错误 0x8007007e**：当你的系统不支持 WSL 时，会出现此错误。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="9a4dc-123">请确保：</span><span class="sxs-lookup"><span data-stu-id="9a4dc-123">Make sure that:</span></span>
    >   * <span data-ttu-id="9a4dc-124">正在运行 Windows build 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="9a4dc-125">[检查你的版本号](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="9a4dc-126">适用于 Linux 的 Windows 子系统可选组件已启用，并重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="9a4dc-127">[请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="9a4dc-128">将你的发行版路径添加到 Windows 环境路径 (在此示例中为`C:\Users\Administrator\Ubuntu`)，例如，使用 Powershell:</span><span class="sxs-lookup"><span data-stu-id="9a4dc-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="9a4dc-129">您现在可以通过键入`<distro>.exe`从任何路径启动发行版。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="9a4dc-130">例如： `ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="9a4dc-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="9a4dc-131">安装 Linux 发行版后，您必须在使用发行版之前[初始化新的发行版实例](initialize-distro.md)。</span><span class="sxs-lookup"><span data-stu-id="9a4dc-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
