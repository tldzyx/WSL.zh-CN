---
title: 安装适用于 Linux (WSL) 在 Windows 10 上的 Windows 子系统
description: 适用于 Windows 10 上的 Linux 安装说明 Windows 子系统。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: d30a5883d648e084193659e997c55d203eb5a735
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035051"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="2a158-104">Linux 安装指南适用于 Windows 10 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="2a158-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="2a158-105">安装适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="2a158-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="2a158-106">在之前安装 WSL 任何 Linux 发行版，您必须确保"Windows 子系统为 Linux"已启用可选功能：</span><span class="sxs-lookup"><span data-stu-id="2a158-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="2a158-107">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="2a158-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="2a158-108">重新启动计算机时提示。</span><span class="sxs-lookup"><span data-stu-id="2a158-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="2a158-109">安装所选的 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="2a158-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="2a158-110">若要下载并安装你首选的 distro(s)，您具有三个选项：</span><span class="sxs-lookup"><span data-stu-id="2a158-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="2a158-111">下载并安装来自 Windows 应用商店 （见下文）</span><span class="sxs-lookup"><span data-stu-id="2a158-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="2a158-112">从命令行/脚本下载并安装 ([读取手动安装说明](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="2a158-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="2a158-113">下载和手动解压缩并安装 (适用于 Windows Server-[此处的说明](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="2a158-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="2a158-114">Windows 10 Fall Creators Update 及更高版本：从 Microsoft Store 安装</span><span class="sxs-lookup"><span data-stu-id="2a158-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="2a158-115">本部分是为 Windows 生成 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="2a158-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="2a158-116">请按照这些步骤[检查你的生成](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="2a158-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="2a158-117">打开 Microsoft Store，然后选择你喜爱的 Linux 分发。</span><span class="sxs-lookup"><span data-stu-id="2a158-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![在 Windows 应用商店中的 Linux 发行版的视图](media/store.png)

    <span data-ttu-id="2a158-119">以下链接将打开每个分布区的 Windows 应用商店页：</span><span class="sxs-lookup"><span data-stu-id="2a158-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="2a158-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="2a158-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="2a158-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="2a158-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="2a158-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="2a158-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="2a158-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="2a158-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="2a158-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="2a158-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="2a158-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="2a158-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="2a158-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="2a158-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="2a158-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="2a158-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="2a158-128">WSL 的 fedora Remix</span><span class="sxs-lookup"><span data-stu-id="2a158-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="2a158-129">WLinux</span><span class="sxs-lookup"><span data-stu-id="2a158-129">WLinux</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="2a158-130">WLinux 企业</span><span class="sxs-lookup"><span data-stu-id="2a158-130">WLinux Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="2a158-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="2a158-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="2a158-132">从发行版的页上，选择"Get"</span><span class="sxs-lookup"><span data-stu-id="2a158-132">From the distro's page, select "Get"</span></span>

    ![在 Windows 应用商店中的 Linux 发行版的视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="2a158-134">完成初始化的发行版</span><span class="sxs-lookup"><span data-stu-id="2a158-134">Complete initialization of your distro</span></span>
<span data-ttu-id="2a158-135">安装 Linux 发行版后，您必须[初始化新的发行版实例](initialize-distro.md)一次，然后才能使用。</span><span class="sxs-lookup"><span data-stu-id="2a158-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="2a158-136">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="2a158-136">Troubleshooting:</span></span> 

<span data-ttu-id="2a158-137">以下是相关的错误的建议修补程序。</span><span class="sxs-lookup"><span data-stu-id="2a158-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="2a158-138">请参阅[WSL 故障排除页](troubleshooting.md)其他常见的错误和其解决方案。</span><span class="sxs-lookup"><span data-stu-id="2a158-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="2a158-139">**安装失败，出现错误 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="2a158-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="2a158-140">系统驱动器上仅运行于 Linux 的 Windows 子系统 (通常这是你`C:`驱动器)。</span><span class="sxs-lookup"><span data-stu-id="2a158-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="2a158-141">请确保发行版都存储在您的系统驱动器上：</span><span class="sxs-lookup"><span data-stu-id="2a158-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="2a158-142">打开**设置** -> **存储** -> **更多的存储设置：保存新内容的更改**
    ![的系统设置的图片 c： 驱动器上安装应用](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="2a158-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="2a158-143">**失败，出现错误 0x8007019e WslRegisterDistribution**</span><span class="sxs-lookup"><span data-stu-id="2a158-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="2a158-144">未启用 Linux 可选组件的 Windows 子系统：</span><span class="sxs-lookup"><span data-stu-id="2a158-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="2a158-145">打开**Control Panel** -> **程序和功能**-> \* \* 打开或关闭 Windows 功能 \* \*-> 检查**适用于 Linux 的 Windows 子系统**或使用在本文开头所述的 PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="2a158-145">Open **Control Panel** -> **Programs and Features** -> \*\*Turn Windows Feature on or off \*\* -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
