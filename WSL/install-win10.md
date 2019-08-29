---
title: 在 Windows 10 上安装适用于 Linux 的 Windows 子系统 (WSL)
description: Windows 10 上适用于 Linux 的 Windows 子系统的安装说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, debian, suse, windows 10, 安装
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122769"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="ccc7d-104">适用于 Linux 的 windows 子系统安装指南 (适用于 Windows 10)</span><span class="sxs-lookup"><span data-stu-id="ccc7d-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="ccc7d-105">安装适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="ccc7d-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="ccc7d-106">在安装任何 Linux 发行版 for WSL 之前, 必须确保已启用 "适用于 Linux 的 Windows 子系统" 可选功能:</span><span class="sxs-lookup"><span data-stu-id="ccc7d-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="ccc7d-107">以管理员身份打开 PowerShell 并运行:</span><span class="sxs-lookup"><span data-stu-id="ccc7d-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="ccc7d-108">出现提示时重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="ccc7d-109">安装所选的 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="ccc7d-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="ccc7d-110">若要下载并安装首选发行版, 你有三种选择:</span><span class="sxs-lookup"><span data-stu-id="ccc7d-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="ccc7d-111">从 Microsoft Store 下载并安装（见下文）</span><span class="sxs-lookup"><span data-stu-id="ccc7d-111">Download and install from the Microsoft Store (see below)</span></span>
1. <span data-ttu-id="ccc7d-112">从命令行/脚本下载并安装（[阅读手动安装说明](install-manual.md)）</span><span class="sxs-lookup"><span data-stu-id="ccc7d-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="ccc7d-113">下载并手动解压缩，然后进行安装（适用于 Windows Server - [此处提供说明](install-on-server.md)）</span><span class="sxs-lookup"><span data-stu-id="ccc7d-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="ccc7d-114">Windows 10 秋季创意者更新及更高版本:从 Microsoft Store 安装</span><span class="sxs-lookup"><span data-stu-id="ccc7d-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="ccc7d-115">此部分适用于 Windows 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="ccc7d-116">请按照相关步骤[检查你的版本](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="ccc7d-117">打开 Microsoft Store，然后选择你喜爱的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store 中的 Linux 发行版的视图](media/store.png)

    <span data-ttu-id="ccc7d-119">以下链接将打开每个分发的 Microsoft store 页面:</span><span class="sxs-lookup"><span data-stu-id="ccc7d-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="ccc7d-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ccc7d-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="ccc7d-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="ccc7d-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="ccc7d-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="ccc7d-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="ccc7d-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="ccc7d-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="ccc7d-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="ccc7d-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="ccc7d-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="ccc7d-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="ccc7d-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="ccc7d-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="ccc7d-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="ccc7d-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="ccc7d-128">WSL 的 Fedora Remix</span><span class="sxs-lookup"><span data-stu-id="ccc7d-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="ccc7d-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="ccc7d-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="ccc7d-130">Pengwin 企业</span><span class="sxs-lookup"><span data-stu-id="ccc7d-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="ccc7d-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="ccc7d-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="ccc7d-132">在发行版的页面上, 选择 "Get"</span><span class="sxs-lookup"><span data-stu-id="ccc7d-132">From the distro's page, select "Get"</span></span>

    ![Microsoft 应用商店中的 Linux 发行版的视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="ccc7d-134">完成发行版的初始化</span><span class="sxs-lookup"><span data-stu-id="ccc7d-134">Complete initialization of your distro</span></span>
<span data-ttu-id="ccc7d-135">安装 Linux 发行版后，必须先[初始化新的发行版实例](initialize-distro.md)一次，然后才能使用它。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="ccc7d-136">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="ccc7d-136">Troubleshooting:</span></span> 

<span data-ttu-id="ccc7d-137">以下是相关的错误和建议的修补措施。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="ccc7d-138">有关其他常见错误及其解决方案，请参阅 [WSL 故障排除页](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="ccc7d-139">**安装失败, 出现错误0x80070003**</span><span class="sxs-lookup"><span data-stu-id="ccc7d-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="ccc7d-140">适用于 Linux 的 Windows 子系统仅在系统驱动器（通常为 `C:` 驱动器）上运行。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="ccc7d-141">请确保发行版存储在系统驱动器上：</span><span class="sxs-lookup"><span data-stu-id="ccc7d-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="ccc7d-142">打开“设置”->“存储”->“更多存储设置: 更改新内容的保存位置”更改保存\*\*
    新内容的位置,以在C:驱动器上安装应用程序的系统设置图片![](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="ccc7d-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="ccc7d-143">**WslRegisterDistribution 失败, 出现错误0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="ccc7d-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="ccc7d-144">未启用适用于 Linux 的 Windows 子系统可选组件:</span><span class="sxs-lookup"><span data-stu-id="ccc7d-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="ccc7d-145">打开 "**控制面板" "**  -> **程序和功能** ->  **" "打开或关闭 windows" 功能**-> 检查**适用于 Linux 的 windows 子系统**或使用本文开头提到的 PowerShell cmdlet。</span><span class="sxs-lookup"><span data-stu-id="ccc7d-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
