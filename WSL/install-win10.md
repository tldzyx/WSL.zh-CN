---
title: Windows 子系统适用于 Linux (WSL) 上 Windows 10 上安装
description: 适用于 Windows 10 上的 Linux 安装说明 Windows 子系统。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063285"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a><span data-ttu-id="e3fc2-104">Linux 安装指南适用于 Windows 10 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="e3fc2-104">Windows Subsystem for Linux Installation Guide for Windows 10</span></span>

## <a name="install-the-windows-subsystem-for-linux"></a><span data-ttu-id="e3fc2-105">安装适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="e3fc2-105">Install the Windows Subsystem for Linux</span></span>

<span data-ttu-id="e3fc2-106">在之前安装 WSL 任何 Linux 发行版，您必须确保"Windows 子系统为 Linux"已启用可选功能：</span><span class="sxs-lookup"><span data-stu-id="e3fc2-106">Before installing any Linux distros for WSL, you must ensure that the "Windows Subsystem for Linux" optional feature is enabled:</span></span>

1. <span data-ttu-id="e3fc2-107">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="e3fc2-107">Open PowerShell as Administrator and run:</span></span>
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. <span data-ttu-id="e3fc2-108">重新启动计算机时提示。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-108">Restart your computer when prompted.</span></span>

## <a name="install-your-linux-distribution-of-choice"></a><span data-ttu-id="e3fc2-109">安装所选的 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="e3fc2-109">Install your Linux Distribution of Choice</span></span>
<span data-ttu-id="e3fc2-110">若要下载并安装你首选的 distro(s)，您具有三个选项：</span><span class="sxs-lookup"><span data-stu-id="e3fc2-110">To download and install your preferred distro(s), you have three choices:</span></span>
1. <span data-ttu-id="e3fc2-111">下载并安装来自 Windows 应用商店 （见下文）</span><span class="sxs-lookup"><span data-stu-id="e3fc2-111">Download and install from the Windows Store (see below)</span></span>
1. <span data-ttu-id="e3fc2-112">从命令行/脚本下载并安装 ([读取手动安装说明](install-manual.md))</span><span class="sxs-lookup"><span data-stu-id="e3fc2-112">Download and install from the Command-Line/Script ([read the manual installation instructions](install-manual.md))</span></span>
1. <span data-ttu-id="e3fc2-113">下载和手动解压缩并安装 (适用于 Windows Server-[此处的说明](install-on-server.md))</span><span class="sxs-lookup"><span data-stu-id="e3fc2-113">Download and manually unpack and install (for Windows Server - [instructions here](install-on-server.md))</span></span>

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a><span data-ttu-id="e3fc2-114">Windows 10 Fall Creators Update 及更高版本：从 Microsoft Store 安装</span><span class="sxs-lookup"><span data-stu-id="e3fc2-114">Windows 10 Fall Creators Update and later: Install from the Microsoft Store</span></span>

> <span data-ttu-id="e3fc2-115">本部分是为 Windows 生成 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-115">This section is for Windows build 16215 or later.</span></span>  <span data-ttu-id="e3fc2-116">请按照这些步骤[检查你的生成](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-116">Follow these steps to [check your build](troubleshooting.md#check-your-build-number).</span></span> 

1. <span data-ttu-id="e3fc2-117">打开 Microsoft Store，然后选择你喜爱的 Linux 分发。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-117">Open the Microsoft Store and choose your favorite Linux distribution.</span></span>

    ![在 Windows 应用商店中的 Linux 发行版的视图](media/store.png)

    <span data-ttu-id="e3fc2-119">以下链接将打开每个分布区的 Windows 应用商店页：</span><span class="sxs-lookup"><span data-stu-id="e3fc2-119">The following links will open the Windows store page for each distribution:</span></span>

    * [<span data-ttu-id="e3fc2-120">Ubuntu</span><span class="sxs-lookup"><span data-stu-id="e3fc2-120">Ubuntu</span></span>](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [<span data-ttu-id="e3fc2-121">OpenSUSE</span><span class="sxs-lookup"><span data-stu-id="e3fc2-121">OpenSUSE</span></span>](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [<span data-ttu-id="e3fc2-122">SLES</span><span class="sxs-lookup"><span data-stu-id="e3fc2-122">SLES</span></span>](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [<span data-ttu-id="e3fc2-123">Kali Linux</span><span class="sxs-lookup"><span data-stu-id="e3fc2-123">Kali Linux</span></span>](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [<span data-ttu-id="e3fc2-124">Debian GNU/Linux</span><span class="sxs-lookup"><span data-stu-id="e3fc2-124">Debian GNU/Linux</span></span>](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. <span data-ttu-id="e3fc2-125">从发行版的页上，选择"Get"</span><span class="sxs-lookup"><span data-stu-id="e3fc2-125">From the distro's page, select "Get"</span></span>

    ![在 Windows 应用商店中的 Linux 发行版的视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a><span data-ttu-id="e3fc2-127">完成初始化的发行版</span><span class="sxs-lookup"><span data-stu-id="e3fc2-127">Complete initialization of your distro</span></span>
<span data-ttu-id="e3fc2-128">安装 Linux 发行版后，您必须[初始化新的发行版实例](initialize-distro.md)一次，然后才能使用。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-128">Now that your Linux distro is installed, you must [initialize your new distro instance](initialize-distro.md) once, before it can be used.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e3fc2-129">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="e3fc2-129">Troubleshooting:</span></span> 

<span data-ttu-id="e3fc2-130">以下是相关的错误的建议修补程序。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-130">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="e3fc2-131">请参阅[WSL 故障排除页](troubleshooting.md)其他常见的错误和其解决方案。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-131">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

* <span data-ttu-id="e3fc2-132">**安装失败，出现错误 0x80070003**</span><span class="sxs-lookup"><span data-stu-id="e3fc2-132">**Installation failed with error 0x80070003**</span></span>
    * <span data-ttu-id="e3fc2-133">系统驱动器上仅运行于 Linux 的 Windows 子系统 (通常这是你`C:`驱动器)。</span><span class="sxs-lookup"><span data-stu-id="e3fc2-133">The Windows Subsystem for Linux only runs on your system drive (usually this is your `C:` drive).</span></span> <span data-ttu-id="e3fc2-134">请确保发行版都存储在您的系统驱动器上：</span><span class="sxs-lookup"><span data-stu-id="e3fc2-134">Make sure that distros are stored on your system drive:</span></span>  
    * <span data-ttu-id="e3fc2-135">打开**设置** -> **存储** -> **更多的存储设置：保存新内容的更改**
    ![的系统设置的图片 c： 驱动器上安装应用](media/AppStorage.png)</span><span class="sxs-lookup"><span data-stu-id="e3fc2-135">Open **Settings** -> **Storage** -> **More Storage Settings: Change where new content is saved**
![Picture of system settings to install apps on C: drive](media/AppStorage.png)</span></span>
