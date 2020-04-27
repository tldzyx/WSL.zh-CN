---
title: 在 Windows 10 上安装适用于 Linux 的 Windows 子系统 (WSL)
description: 有关在 Windows 10 上安装适用于 Linux 的 Windows 子系统的说明。
keywords: BashOnWindows, bash, wsl, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "74200236"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="04b9c-104">适用于 Linux 的 Windows 子系统安装指南 (Windows 10)</span><span class="sxs-lookup"><span data-stu-id="04b9c-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="04b9c-105">安装适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="04b9c-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="04b9c-106">在安装适用于 WSL 的任何 Linux 分发版之前，必须确保已启用“适用于 Linux 的 Windows 子系统”可选功能：</span><span class="sxs-lookup"><span data-stu-id="04b9c-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="04b9c-107">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="04b9c-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="04b9c-108">出现提示时，重启计算机。</span><span class="sxs-lookup"><span data-stu-id="04b9c-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="04b9c-109">安装所选的 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="04b9c-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="04b9c-110">若要下载并安装首选的分发版，可以选择三种做法：</span><span class="sxs-lookup"><span data-stu-id="04b9c-110">To download and install your preferred distro(s), you have three choices:</span></span>
* <span data-ttu-id="04b9c-111">从 Microsoft Store 下载并安装（参阅下文）</span><span class="sxs-lookup"><span data-stu-id="04b9c-111">Download and install from the Microsoft Store (see below)</span></span>
* <span data-ttu-id="04b9c-112">从命令行/脚本下载并安装（[阅读手动安装说明](install-manual.md)）</span><span class="sxs-lookup"><span data-stu-id="04b9c-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
* <span data-ttu-id="04b9c-113">下载并手动解压缩和安装（适用于 Windows Server - [参阅此处的说明](install-on-server.md)）</span><span class="sxs-lookup"><span data-stu-id="04b9c-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="04b9c-114">Windows 10 Fall Creators Update 和更高版本：从 Microsoft Store 安装</span><span class="sxs-lookup"><span data-stu-id="04b9c-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="04b9c-115">本部分适用于 Windows 内部版本 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="04b9c-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="04b9c-116">遵循以下步骤[检查内部版本](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="04b9c-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="04b9c-117">打开 Microsoft Store，并选择你偏好的 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="04b9c-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![Microsoft Store 中的 Linux 分发版视图](media/store.png)

    <span data-ttu-id="04b9c-119">单击以下链接会打开每个分发版的 Microsoft Store 页面：</span><span class="sxs-lookup"><span data-stu-id="04b9c-119">The following links will open the Microsoft store page for each distribution:</span></span>

    * [<span data-ttu-id="04b9c-120">Ubuntu 16.04 LTS</span><span class="sxs-lookup"><span data-stu-id="04b9c-120">Ubuntu 16.04 LTS</span></span>](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [<span data-ttu-id="04b9c-121">Ubuntu 18.04 LTS</span><span class="sxs-lookup"><span data-stu-id="04b9c-121">Ubuntu 18.04 LTS</span></span>](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [<span data-ttu-id="04b9c-122">OpenSUSE Leap 15</span><span class="sxs-lookup"><span data-stu-id="04b9c-122">OpenSUSE Leap 15</span></span>](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [<span data-ttu-id="04b9c-123">OpenSUSE Leap 42</span><span class="sxs-lookup"><span data-stu-id="04b9c-123">OpenSUSE Leap 42</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="04b9c-124">SUSE Linux Enterprise Server 12</span><span class="sxs-lookup"><span data-stu-id="04b9c-124">SUSE Linux Enterprise Server 12</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="04b9c-125">SUSE Linux Enterprise Server 15</span><span class="sxs-lookup"><span data-stu-id="04b9c-125">SUSE Linux Enterprise Server 15</span></span>](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [<span data-ttu-id="04b9c-126">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="04b9c-126">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="04b9c-127">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="04b9c-127">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [<span data-ttu-id="04b9c-128">Fedora Remix for WSL</span><span class="sxs-lookup"><span data-stu-id="04b9c-128">Fedora Remix for WSL</span></span>](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [<span data-ttu-id="04b9c-129">Pengwin</span><span class="sxs-lookup"><span data-stu-id="04b9c-129">Pengwin</span></span>](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [<span data-ttu-id="04b9c-130">Pengwin Enterprise</span><span class="sxs-lookup"><span data-stu-id="04b9c-130">Pengwin Enterprise</span></span>](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [<span data-ttu-id="04b9c-131">Alpine WSL</span><span class="sxs-lookup"><span data-stu-id="04b9c-131">Alpine WSL</span></span>](https://www.microsoft.com/store/apps/9p804crf0395)

1. <span data-ttu-id="04b9c-132">在分发版的页面中，选择“获取”</span><span class="sxs-lookup"><span data-stu-id="04b9c-132">From the distro's page, select "Get"</span></span>

    ![Microsoft Store 中的 Linux 分发版视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="04b9c-134">完成分发版的初始化</span><span class="sxs-lookup"><span data-stu-id="04b9c-134">Complete initialization of your distro</span></span>
<span data-ttu-id="04b9c-135">安装 Linux 分发版后，必须先[初始化新的分发版实例](initialize-distro.md)一次才能使用该分发版。</span><span class="sxs-lookup"><span data-stu-id="04b9c-135">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="04b9c-136">故障排除：</span><span class="sxs-lookup"><span data-stu-id="04b9c-136">Troubleshooting:</span></span> 

<span data-ttu-id="04b9c-137">下面是相关的错误和建议的修复措施。</span><span class="sxs-lookup"><span data-stu-id="04b9c-137">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="04b9c-138">有关其他常见错误及其解决方法，请参阅 [WSL 故障排除页](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="04b9c-138">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="04b9c-139">**安装失败并出现错误 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="04b9c-139">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="04b9c-140">适用于 Linux 的 Windows 子系统只能在系统驱动器（通常是 `C:` 驱动器）中运行。</span><span class="sxs-lookup"><span data-stu-id="04b9c-140">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="04b9c-141">请确保将分发版存储在系统驱动器上：</span><span class="sxs-lookup"><span data-stu-id="04b9c-141">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="04b9c-142">打开“设置”->“存储”->“更多存储设置：    更改新内容的保存位置”
    ![用于在 C: 驱动器中安装应用的系统设置屏幕截图](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="04b9c-142">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
    
    
 * <span data-ttu-id="04b9c-143">**WslRegisterDistribution 失败并出现错误 0x8007019e**</span><span class="sxs-lookup"><span data-stu-id="04b9c-143">**WslRegisterDistribution failed with error 0x8007019e**</span></span>   
  * <span data-ttu-id="04b9c-144">未启用“适用于 Linux 的 Windows 子系统”可选组件：</span><span class="sxs-lookup"><span data-stu-id="04b9c-144">The Windows Subsystem for Linux optional component is not enabled:</span></span> 
   * <span data-ttu-id="04b9c-145">打开“控制面板” -> “程序和功能” -> “打开或关闭 Windows 功能”-> 选中“适用于 Linux 的 Windows 子系统”，或使用本文开头所述的 PowerShell cmdlet。    </span><span class="sxs-lookup"><span data-stu-id="04b9c-145">Open **Control Panel** -> **Programs and Features** -> **Turn Windows Feature on or off** -> Check **Windows Subsystem for Linux** or using the PowerShell cmdlet mentioned at the begining of this article.</span></span>
