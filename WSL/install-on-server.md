---
title: 在 Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308792"
---
# <a name="windows-server-installation-guide"></a><span data-ttu-id="f4770-104">Windows Server 安装指南</span><span class="sxs-lookup"><span data-stu-id="f4770-104">Windows Server Installation Guide</span></span>

> <span data-ttu-id="f4770-105">适用于 Windows Server 2019 及更高版本</span><span class="sxs-lookup"><span data-stu-id="f4770-105">Applies to Windows Server 2019 and later</span></span>

<span data-ttu-id="f4770-106">在//Build2017 上, Microsoft 宣布 windows [Server 上将提供](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)适用于 Linux 的 windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="f4770-106">At //Build2017, Microsoft announced that Windows Subsystem for Linux will be [available on Windows Server](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/).</span></span>  <span data-ttu-id="f4770-107">这些说明介绍了如何在 Windows Server 1709 和更高版本上运行适用于 Linux 的 Windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="f4770-107">These instructions walk through running the Windows Subsystem for Linux on Windows Server 1709 and later.</span></span>

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="f4770-108">启用适用于 Linux 的 Windows 子系统 (WSL)</span><span class="sxs-lookup"><span data-stu-id="f4770-108">Enable the Windows Subsystem for Linux (WSL)</span></span>

<span data-ttu-id="f4770-109">在 Windows 上运行 Linux 发行版之前, 必须启用 "适用于 Linux 的 Windows 子系统" 可选功能, 然后重新启动。</span><span class="sxs-lookup"><span data-stu-id="f4770-109">Before you can run Linux distros on Windows, you must enable the "Windows Subsystem for Linux" optional feature and reboot.</span></span>

1. <span data-ttu-id="f4770-110">以管理员身份打开 PowerShell 并运行:</span><span class="sxs-lookup"><span data-stu-id="f4770-110">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="f4770-111">出现提示时, 请重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="f4770-111">Restart your computer when prompted.</span></span> <span data-ttu-id="f4770-112">**需要重新启动**才能确保 WSL 可以启动受信任的执行环境。</span><span class="sxs-lookup"><span data-stu-id="f4770-112">**This reboot is required** in order to ensure that WSL can initiate a trusted execution environment.</span></span>

## <a name="download-a-linux-distro"></a><span data-ttu-id="f4770-113">下载 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="f4770-113">Download a Linux distro</span></span>

<span data-ttu-id="f4770-114">按照[以下说明](install-manual.md)下载最喜爱的 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="f4770-114">Follow [these instructions](install-manual.md) to download your favorite Linux distribution.</span></span>

## <a name="extract-and-install-a-linux-distro"></a><span data-ttu-id="f4770-115">提取并安装 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="f4770-115">Extract and install a Linux distro</span></span>
<span data-ttu-id="f4770-116">下载发行版后, 请提取其内容, 并手动安装发行版:</span><span class="sxs-lookup"><span data-stu-id="f4770-116">Now that you've downloaded a distro, extract its contents and manually install the distro:</span></span>

1. <span data-ttu-id="f4770-117">`<distro>.appx`提取包的内容, 例如, 使用 PowerShell:</span><span class="sxs-lookup"><span data-stu-id="f4770-117">Extract the `<distro>.appx` package's contents, e.g. using PowerShell:</span></span>

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. <span data-ttu-id="f4770-118">运行发行版启动器以完成安装, 并在名为`<distro>.exe`的目标文件夹中运行发行版启动器应用程序。</span><span class="sxs-lookup"><span data-stu-id="f4770-118">Run the distro launcher To complete installation, run the distro launcher application in the target folder, named `<distro>.exe`.</span></span> <span data-ttu-id="f4770-119">例如: `ubuntu.exe`等。</span><span class="sxs-lookup"><span data-stu-id="f4770-119">For example: `ubuntu.exe`, etc.</span></span>

    ![Windows Server 上的扩展 Ubuntu 发行版](media/server-appx-expand.png)

    > <span data-ttu-id="f4770-121">**疑难解答**</span><span class="sxs-lookup"><span data-stu-id="f4770-121">**Troubleshooting**</span></span>
    > * <span data-ttu-id="f4770-122">**安装失败, 出现错误 0x8007007e**:当你的系统不支持 WSL 时, 会出现此错误。</span><span class="sxs-lookup"><span data-stu-id="f4770-122">**Installation failed with error 0x8007007e**: This error occurs when your system doesn't support WSL.</span></span> <span data-ttu-id="f4770-123">请确保：</span><span class="sxs-lookup"><span data-stu-id="f4770-123">Make sure that:</span></span>
    >   * <span data-ttu-id="f4770-124">你正在运行 Windows 版本16215或更高版本。</span><span class="sxs-lookup"><span data-stu-id="f4770-124">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="f4770-125">[检查生成](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="f4770-125">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
    >   * <span data-ttu-id="f4770-126">已启用适用于 Linux 的 Windows 子系统可选组件, 并已重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="f4770-126">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="f4770-127">[请确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="f4770-127">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
    
3. <span data-ttu-id="f4770-128">向 Windows 环境路径 (`C:\Users\Administrator\Ubuntu`此示例中为) 添加发行版路径, 例如, 使用 Powershell:</span><span class="sxs-lookup"><span data-stu-id="f4770-128">Add your distro path to the Windows environment PATH (`C:\Users\Administrator\Ubuntu` in this example), e.g. using Powershell:</span></span>
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    <span data-ttu-id="f4770-129">你现在可以通过键入`<distro>.exe`从任何路径启动发行版。</span><span class="sxs-lookup"><span data-stu-id="f4770-129">You can now launch your distro from any path by typing `<distro>.exe`.</span></span> <span data-ttu-id="f4770-130">例如：`ubuntu.exe`</span><span class="sxs-lookup"><span data-stu-id="f4770-130">For example: `ubuntu.exe`</span></span>

<span data-ttu-id="f4770-131">安装 Linux 发行版后, 必须先[初始化新的发行版实例](initialize-distro.md), 然后才能使用发行版。</span><span class="sxs-lookup"><span data-stu-id="f4770-131">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) before using your distro.</span></span>
