---
title: 更新 WSL 2 Linux 内核
description: 有关如何手动更新 WSL 2 Linux 内核的说明
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.localizationpriority: high
ms.custom: seodec18
ms.openlocfilehash: f7fce13c2acc65e3afa2cc56873e40bc55a460bc
ms.sourcegitcommit: 506272bd7fc1cbda7e32146d54a8bdd02af3e0c4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/13/2020
ms.locfileid: "79319707"
---
# <a name="updating-the-wsl-2-linux-kernel"></a><span data-ttu-id="8efe6-104">更新 WSL 2 Linux 内核</span><span class="sxs-lookup"><span data-stu-id="8efe6-104">Updating the WSL 2 Linux kernel</span></span>

<span data-ttu-id="8efe6-105">若要手动更新 WSL 2 内的 Linux 内核，请按照以下步骤执行操作。</span><span class="sxs-lookup"><span data-stu-id="8efe6-105">To manually update the Linux kernel inside of WSL 2 please follow these steps.</span></span> 

## <a name="download-the-linux-kernel-update-package"></a><span data-ttu-id="8efe6-106">下载 Linux 内核更新包</span><span class="sxs-lookup"><span data-stu-id="8efe6-106">Download the Linux kernel update package</span></span>

<span data-ttu-id="8efe6-107">请单击[此链接](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)下载适用于 AMD64 计算机的最新 WSL2 Linux 内核更新包。</span><span class="sxs-lookup"><span data-stu-id="8efe6-107">Please click on [this link](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi) to download the latest WSL2 Linux kernel update package for AMD64 machines.</span></span>

> [!NOTE] 
> <span data-ttu-id="8efe6-108">如果使用的是 ARM64 计算机，请下载[此包](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)。</span><span class="sxs-lookup"><span data-stu-id="8efe6-108">If you're using an ARM64 machine, please download [this package](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi) instead.</span></span>

## <a name="install-the-linux-kernel-update-package"></a><span data-ttu-id="8efe6-109">安装 Linux 内核更新包</span><span class="sxs-lookup"><span data-stu-id="8efe6-109">Install the Linux kernel update package</span></span>

<span data-ttu-id="8efe6-110">若要安装 Linux 内核更新包，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="8efe6-110">To install the Linux kernel update package:</span></span>

    1. <span data-ttu-id="8efe6-111">运行上一步中下载的更新包。</span><span class="sxs-lookup"><span data-stu-id="8efe6-111">Run the update package downloaded in the previous step.</span></span>
    2. <span data-ttu-id="8efe6-112">系统将提示你提供提升的权限，选择“是”以批准此安装。</span><span class="sxs-lookup"><span data-stu-id="8efe6-112">You will be prompted for elevated permissions, select ‘yes’ to approve this installation.</span></span>
    3. <span data-ttu-id="8efe6-113">安装完成后，便可以开始使用 WSL2 了！</span><span class="sxs-lookup"><span data-stu-id="8efe6-113">Once the installation is complete, you are ready to begin using WSL2!</span></span>

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a><span data-ttu-id="8efe6-114">有关更新 WSL2 Linux 内核的未来计划</span><span class="sxs-lookup"><span data-stu-id="8efe6-114">Future plans for updating the WSL2 Linux kernel</span></span>

<span data-ttu-id="8efe6-115">有关这些更改的详细信息，请阅读 [Windows 命令行博客](https://aka.ms/cliblog)上的[这篇博客文章](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)。</span><span class="sxs-lookup"><span data-stu-id="8efe6-115">For more info on these changes, please read [this blog post](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004) on the [Windows Command Line Blog](https://aka.ms/cliblog).</span></span>
