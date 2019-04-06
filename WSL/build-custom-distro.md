---
title: 为 WSL 构建的自定义 Linux 发行版
description: 了解如何创建适用于 Linux 的 Windows 子系统的自定义的 Linux 分发版。
keywords: BashOnWindows，bash、 wsl、 windows、 windows 子系统、 发行版、 自定义
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063255"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="154f0-104">创建的自定义 Linux 发行版，适用于 WSL</span><span class="sxs-lookup"><span data-stu-id="154f0-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="154f0-105">若要生成的 Microsoft Store WSL 发行版包和/或创建自定义 Linux 发行版程序包以进行旁加载，请使用我们开放源代码 WSL 示例。</span><span class="sxs-lookup"><span data-stu-id="154f0-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="154f0-106">您可以找到[发行版启动器存储库](https://github.com/Microsoft/WSL-DistroLauncher)GitHub 上。</span><span class="sxs-lookup"><span data-stu-id="154f0-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="154f0-107">此项目启用：</span><span class="sxs-lookup"><span data-stu-id="154f0-107">This project enables:</span></span>
* <span data-ttu-id="154f0-108">Linux 分发 maintainer 打包和提交在 WSL 运行一个 appx 作为一种 Linux 分发</span><span class="sxs-lookup"><span data-stu-id="154f0-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="154f0-109">开发人员能够创建自定义可以是旁的加载到其开发计算机上的 Linux 分发</span><span class="sxs-lookup"><span data-stu-id="154f0-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="154f0-110">后台</span><span class="sxs-lookup"><span data-stu-id="154f0-110">Background</span></span>
<span data-ttu-id="154f0-111">我们为 WSL 作为 UWP 应用程序可以通过 Microsoft Store 分发的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="154f0-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="154f0-112">你可以安装这些应用程序，然后将在 WSL-位于 Windows 内核的子系统上运行。</span><span class="sxs-lookup"><span data-stu-id="154f0-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="154f0-113">早期的博客文章中所述，此传送机制具有诸多优点。</span><span class="sxs-lookup"><span data-stu-id="154f0-113">This delivery mechanism has many benefits as discussed in an earlier blog post.</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="154f0-114">旁加载自定义 Linux 发行版包</span><span class="sxs-lookup"><span data-stu-id="154f0-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="154f0-115">可以在你的个人计算机上为旁加载应用程序中创建自定义的 Linux 发行版包。</span><span class="sxs-lookup"><span data-stu-id="154f0-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="154f0-116">请注意，除非您作为分发 maintainer 提交后，不会自定义包通过 Microsoft Store 中分发。</span><span class="sxs-lookup"><span data-stu-id="154f0-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="154f0-117">若要设置在计算机旁加载应用程序，你将需要"面向开发人员"下的系统设置中启用此功能。</span><span class="sxs-lookup"><span data-stu-id="154f0-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="154f0-118">请务必包含开发人员模式或所选旁加载应用</span><span class="sxs-lookup"><span data-stu-id="154f0-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="154f0-119">对于 Linux 发行版维护人员</span><span class="sxs-lookup"><span data-stu-id="154f0-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="154f0-120">若要提交到应用商店，你将需要与我们通过发布审批。</span><span class="sxs-lookup"><span data-stu-id="154f0-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="154f0-121">如果您是希望添加到 Microsoft Store 分发的 Linux 分发所有者，请联系wslpartners@microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="154f0-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="154f0-122">入门</span><span class="sxs-lookup"><span data-stu-id="154f0-122">Getting Started</span></span>
<span data-ttu-id="154f0-123">按照上的说明[发行版启动器 GitHub 存储库](https://github.com/Microsoft/WSL-DistroLauncher)创建自定义的 Linux 发行版包。</span><span class="sxs-lookup"><span data-stu-id="154f0-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="154f0-124">团队博客</span><span class="sxs-lookup"><span data-stu-id="154f0-124">Team Blogs</span></span>
*  [<span data-ttu-id="154f0-125">打开 Linux 分发 Maintainer 和旁加载自定义 Linux 分发版溯源 WSL 示例</span><span class="sxs-lookup"><span data-stu-id="154f0-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="154f0-126">命令行的博客</span><span class="sxs-lookup"><span data-stu-id="154f0-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="154f0-127">提供反馈</span><span class="sxs-lookup"><span data-stu-id="154f0-127">Provide Feedback</span></span>
* [<span data-ttu-id="154f0-128">发行版启动器 Gitub 存储库</span><span class="sxs-lookup"><span data-stu-id="154f0-128">Distro Launcher Gitub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="154f0-129">GitHub 问题跟踪程序 WSL</span><span class="sxs-lookup"><span data-stu-id="154f0-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="154f0-130">命令行 UserVoice 门户</span><span class="sxs-lookup"><span data-stu-id="154f0-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
