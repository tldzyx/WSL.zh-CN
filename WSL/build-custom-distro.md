---
title: 为 WSL 生成自定义 Linux 发行版
description: 了解如何为适用于 Linux 的 Windows 子系统创建自定义 Linux 分发版。
keywords: BashOnWindows、bash、wsl、windows、windows 子系统、发行版、custom
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: 181badd4ee2f69e904099c12b54dfbdf3a37e294
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269702"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a><span data-ttu-id="85afd-104">为 WSL 创建自定义 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="85afd-104">Creating a Custom Linux Distro for WSL</span></span>

<span data-ttu-id="85afd-105">使用我们的开源 WSL 示例生成用于 Microsoft Store 的 WSL 发行版包和/或创建用于旁加载的自定义 Linux 发行版程序包。</span><span class="sxs-lookup"><span data-stu-id="85afd-105">Use our open source WSL sample to build WSL distro packages for the Microsoft Store and/or to create custom Linux distro packages for sideloading.</span></span> <span data-ttu-id="85afd-106">可在 GitHub 上找到[发行版启动器](https://github.com/Microsoft/WSL-DistroLauncher)存储库。</span><span class="sxs-lookup"><span data-stu-id="85afd-106">You can find the [distro launcher repo](https://github.com/Microsoft/WSL-DistroLauncher) on GitHub.</span></span>

<span data-ttu-id="85afd-107">此项目可实现以下功能：</span><span class="sxs-lookup"><span data-stu-id="85afd-107">This project enables:</span></span>
* <span data-ttu-id="85afd-108">Linux 分发维护人员，用于打包并提交 Linux 分发版，作为在 WSL 上运行的 appx</span><span class="sxs-lookup"><span data-stu-id="85afd-108">Linux distribution maintainers to package and submit a Linux distribution as an appx that runs on WSL</span></span>
* <span data-ttu-id="85afd-109">开发人员创建可在其开发计算机上旁加载的自定义 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="85afd-109">Developers to create custom Linux distributions that can be sideloaded onto their dev machine</span></span>

## <a name="background"></a><span data-ttu-id="85afd-110">后台</span><span class="sxs-lookup"><span data-stu-id="85afd-110">Background</span></span>
<span data-ttu-id="85afd-111">我们通过 Microsoft Store 将 Linux 发行版 for WSL 分发为 UWP 应用程序。</span><span class="sxs-lookup"><span data-stu-id="85afd-111">We distribute Linux distros for WSL as UWP applications through the Microsoft Store.</span></span> <span data-ttu-id="85afd-112">可以安装那些随后在 WSL 上运行的应用程序-位于 Windows 内核中的子系统。</span><span class="sxs-lookup"><span data-stu-id="85afd-112">You can install those applications that will then run on WSL - the subsystem that sits in the Windows kernel.</span></span> <span data-ttu-id="85afd-113">此交付机制具有许多好处，如[更早的博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/)中所述。</span><span class="sxs-lookup"><span data-stu-id="85afd-113">This delivery mechanism has many benefits as discussed in an [earlier blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/10/ubuntu-now-available-from-the-windows-store/).</span></span>

## <a name="sideloading-a-custom-linux-distro-package"></a><span data-ttu-id="85afd-114">旁加载自定义 Linux 发行版包</span><span class="sxs-lookup"><span data-stu-id="85afd-114">Sideloading a Custom Linux Distro Package</span></span>
<span data-ttu-id="85afd-115">可以在个人计算机上创建自定义 Linux 发行版包作为应用程序旁加载。</span><span class="sxs-lookup"><span data-stu-id="85afd-115">You can create a custom Linux distro package as an application to sideload on your personal machine.</span></span> <span data-ttu-id="85afd-116">请注意，除非你作为分发维护程序提交，否则不会通过 Microsoft Store 分发自定义包。</span><span class="sxs-lookup"><span data-stu-id="85afd-116">Please note that your custom package would not be distributed through the Microsoft Store unless you submit as a distribution maintainer.</span></span>
<span data-ttu-id="85afd-117">若要将计算机设置为旁加载应用，需要在 "For 开发人员" 下的 "系统设置" 中启用此项。</span><span class="sxs-lookup"><span data-stu-id="85afd-117">To set up your machine to sideload apps, you will need to enable this in the system settings under “For Developers”.</span></span>  <span data-ttu-id="85afd-118">请确保已选择 "开发人员模式" 或 "旁加载应用"</span><span class="sxs-lookup"><span data-stu-id="85afd-118">Be sure to either have developer mode, or sideload apps selected</span></span>

## <a name="for-linux-distro-maintainers"></a><span data-ttu-id="85afd-119">适用于 Linux 发行版维护人员</span><span class="sxs-lookup"><span data-stu-id="85afd-119">For Linux Distro Maintainers</span></span>
<span data-ttu-id="85afd-120">若要提交到应用商店，你将需要与我们合作来接收发布批准。</span><span class="sxs-lookup"><span data-stu-id="85afd-120">To submit to the Store, you will need to work with us to receive publishing approval.</span></span> <span data-ttu-id="85afd-121">如果你是有兴趣向 Microsoft Store 添加分发的 Linux 分发所有者，请联系wslpartners@microsoft.com。</span><span class="sxs-lookup"><span data-stu-id="85afd-121">If you are a Linux distribution owner interested in adding your distribution to the Microsoft Store, please contact wslpartners@microsoft.com.</span></span>

## <a name="getting-started"></a><span data-ttu-id="85afd-122">入门</span><span class="sxs-lookup"><span data-stu-id="85afd-122">Getting Started</span></span>
<span data-ttu-id="85afd-123">按照[发行版启动器 GitHub](https://github.com/Microsoft/WSL-DistroLauncher)存储库中的说明创建自定义 Linux 发行版包。</span><span class="sxs-lookup"><span data-stu-id="85afd-123">Follow the instructions on the [Distro Launcher GitHub repo](https://github.com/Microsoft/WSL-DistroLauncher) to create a custom Linux distro package.</span></span>

 
## <a name="team-blogs"></a><span data-ttu-id="85afd-124">团队博客</span><span class="sxs-lookup"><span data-stu-id="85afd-124">Team Blogs</span></span>
*  [<span data-ttu-id="85afd-125">打开适用于 Linux 分发维护人员和旁加载自定义 Linux 分发的 WSL 示例</span><span class="sxs-lookup"><span data-stu-id="85afd-125">Open Sourcing a WSL Sample for Linux Distribution Maintainers and Sideloading Custom Linux Distributions</span></span>](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [<span data-ttu-id="85afd-126">命令行博客</span><span class="sxs-lookup"><span data-stu-id="85afd-126">Command-Line blog</span></span>](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a><span data-ttu-id="85afd-127">提供反馈</span><span class="sxs-lookup"><span data-stu-id="85afd-127">Provide Feedback</span></span>
* [<span data-ttu-id="85afd-128">发行版启动器 GitHub 存储库</span><span class="sxs-lookup"><span data-stu-id="85afd-128">Distro Launcher GitHub repo</span></span>](https://github.com/Microsoft/WSL-DistroLauncher)
* [<span data-ttu-id="85afd-129">适用于 WSL 的 GitHub 问题跟踪器</span><span class="sxs-lookup"><span data-stu-id="85afd-129">GitHub issue tracker for WSL</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="85afd-130">命令行 UserVoice 门户</span><span class="sxs-lookup"><span data-stu-id="85afd-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
