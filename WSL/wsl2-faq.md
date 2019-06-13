---
title: WSL 2 方面的常见问题
description: Frequently Asked Questions about Windows 子系统适用于 Linux 2
keywords: BashOnWindows，bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038087"
---
# <a name="wsl-2-faq"></a><span data-ttu-id="bc25c-104">WSL 2 常见问题</span><span class="sxs-lookup"><span data-stu-id="bc25c-104">WSL 2 FAQ</span></span>

<span data-ttu-id="bc25c-105">下面是一组常见问题 (FAQ) Windows 子系统 Linux 2。</span><span class="sxs-lookup"><span data-stu-id="bc25c-105">Below is a list of frequently asked questions (FAQ) about the Windows Subsystem for Linux 2.</span></span>

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a><span data-ttu-id="bc25c-106">WSL 2 是否使用 HYPER-V？</span><span class="sxs-lookup"><span data-stu-id="bc25c-106">Does WSL 2 use Hyper-V?</span></span> <span data-ttu-id="bc25c-107">它将在 Windows 10 家庭版？</span><span class="sxs-lookup"><span data-stu-id="bc25c-107">Will it be available on Windows 10 Home?</span></span>

<span data-ttu-id="bc25c-108">WSL 2 将在所有 Sku 上可用的 WSL 是目前不可用，包括 Windows 10 家庭版。</span><span class="sxs-lookup"><span data-stu-id="bc25c-108">WSL 2 will be available on all SKUs where WSL is currently available, including Windows 10 Home.</span></span>

<span data-ttu-id="bc25c-109">最新版本的 WSL 使用 HYPER-V 体系结构用于支持其虚拟化。</span><span class="sxs-lookup"><span data-stu-id="bc25c-109">The newest version of WSL uses Hyper-V architecture to enable its virtualization.</span></span> <span data-ttu-id="bc25c-110">此体系结构可在一个可选组件，是 HYPER-V 功能的子集。</span><span class="sxs-lookup"><span data-stu-id="bc25c-110">This architecture will be available in an optional component that is a subset of the Hyper-V feature.</span></span> <span data-ttu-id="bc25c-111">此可选组件将在所有 Sku 上可用。</span><span class="sxs-lookup"><span data-stu-id="bc25c-111">This optional component will be available on all SKUs.</span></span> <span data-ttu-id="bc25c-112">您有望看到更多详细信息这种体验即将随着我们更接近于 WSL 2 版本。</span><span class="sxs-lookup"><span data-stu-id="bc25c-112">You can expect to see more details about this experience soon as we get closer to the WSL 2 release.</span></span>

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a><span data-ttu-id="bc25c-113">WSL 1 会受到什么影响？</span><span class="sxs-lookup"><span data-stu-id="bc25c-113">What will happen to WSL 1?</span></span> <span data-ttu-id="bc25c-114">将放弃它？</span><span class="sxs-lookup"><span data-stu-id="bc25c-114">Will it be abandoned?</span></span>

<span data-ttu-id="bc25c-115">我们目前尚未计划不推荐使用的 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="bc25c-115">We currently have no plans to deprecate WSL 1.</span></span> <span data-ttu-id="bc25c-116">您可以运行 WSL 1 和 WSL 2 发行版本并排显示，并可以升级和降级任何发行版在任何时间。</span><span class="sxs-lookup"><span data-stu-id="bc25c-116">You can run WSL 1 and WSL 2 distros side by side, and can upgrade and downgrade any distro at any time.</span></span> <span data-ttu-id="bc25c-117">将 WSL 2 添加为新的体系结构提供了更好的平台为 WSL 团队提供功能，使 WSL 令人惊叹的方式在 Windows 中运行的 Linux 环境。</span><span class="sxs-lookup"><span data-stu-id="bc25c-117">Adding WSL 2 as a new architecture presents a better platform for the WSL team to deliver features that make WSL an amazing way to run a Linux environment in Windows.</span></span>

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a><span data-ttu-id="bc25c-118">我是否能够运行 WSL 2 和 VMware 或 VirtualBox 等其他第三方虚拟化工具？</span><span class="sxs-lookup"><span data-stu-id="bc25c-118">Will I be able to run WSL 2 and other 3rd party virtualization tools such as VMware, or VirtualBox?</span></span>

<span data-ttu-id="bc25c-119">HYPER-V 是在使用中，这意味着它们将不能启用 WSL 2 时运行，则无法使用某些第三方应用程序。</span><span class="sxs-lookup"><span data-stu-id="bc25c-119">Some 3rd party applications cannot work when Hyper-V is in use, which means they will not be able to run when WSL 2 is enabled.</span></span> <span data-ttu-id="bc25c-120">遗憾的是，此时间包括 VMware 和 VirtualBox VirtualBox 6 之前的版本 (发布于 2018 年 12 月 6.0.0 VirtualBox[现在支持为回退执行核心 Windows 主机上的 HYPER-V] [ 1]!)</span><span class="sxs-lookup"><span data-stu-id="bc25c-120">Unfortunately, this does include VMware, and versions of VirtualBox before VirtualBox 6 (VirtualBox 6.0.0 released in December 2018 [now supports Hyper-V as a fallback execution core on a Windows host][1]!)</span></span>

<span data-ttu-id="bc25c-121">我们正在调查的方法，帮助解决此问题。</span><span class="sxs-lookup"><span data-stu-id="bc25c-121">We are investigating ways to help resolve this issue.</span></span> <span data-ttu-id="bc25c-122">例如，我们公开了一组 Api 调用[虚拟机监控程序平台][ 2] ，可以使用第三方虚拟化提供程序，使其软件与 HYPER-V 的兼容</span><span class="sxs-lookup"><span data-stu-id="bc25c-122">For example, we expose a set of APIs called [Hypervisor Platform][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s.</span></span> <span data-ttu-id="bc25c-123">这使应用程序使用 HYPER-V 体系结构如其仿真[Google Android 仿真器][3]，和 6 和更高版本的 VirtualBox 均现在与 HYPER-V 兼容。</span><span class="sxs-lookup"><span data-stu-id="bc25c-123">This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3], and VirtualBox 6 and above which are both now compatible with Hyper-V.</span></span>

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a><span data-ttu-id="bc25c-124">可以访问 WSL 2 中的 GPU？</span><span class="sxs-lookup"><span data-stu-id="bc25c-124">Can I access the GPU in WSL 2?</span></span> <span data-ttu-id="bc25c-125">是否有计划以提高硬件支持？</span><span class="sxs-lookup"><span data-stu-id="bc25c-125">Are there plans to increase hardware support?</span></span>

<span data-ttu-id="bc25c-126">在 WSL 2 硬件访问的初始版本中支持将受到限制，例如： 你将不能访问 GPU，串行或 USBs。</span><span class="sxs-lookup"><span data-stu-id="bc25c-126">In initial releases of WSL 2 hardware access support will be limited, e.g: you will be unable to access the GPU, serial or USBs .</span></span> <span data-ttu-id="bc25c-127">但是，添加更好的设备支持是我们积压工作上高，因为这将很多更多的使用情况下打开面向开发人员想要对与这些设备进行交互。</span><span class="sxs-lookup"><span data-stu-id="bc25c-127">However, adding better device support is high on our backlog, as this opens many more use cases for developers that wish to interact with these devices.</span></span> <span data-ttu-id="bc25c-128">在此期间，可以始终使用串行端口和 USB 访问 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="bc25c-128">In the meantime, you can always use WSL 1 which has serial port and USB access.</span></span> <span data-ttu-id="bc25c-129">请继续关注此博客和 twitter，随时了解最新功能到 insider WSL 团队成员生成，并会在你想要与之交互的设备上提供反馈 ！</span><span class="sxs-lookup"><span data-stu-id="bc25c-129">Please stay tuned to this blog and WSL team members on Twitter to stay informed about the latest features coming to insider builds and reach out to give us feedback on what devices you’d like to interact with!</span></span>

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a><span data-ttu-id="bc25c-130">WSL 2 能够使用网络应用程序？</span><span class="sxs-lookup"><span data-stu-id="bc25c-130">Will WSL 2 be able to use networking applications?</span></span>

<span data-ttu-id="bc25c-131">是的一般情况下应用程序的网络将更快并更好地工作，因为我们有完整的系统调用兼容性。</span><span class="sxs-lookup"><span data-stu-id="bc25c-131">Yes, in general networking applications will be faster and work better since we have full system call compatibility.</span></span> <span data-ttu-id="bc25c-132">但是，新的体系结构使用虚拟化网络组件。</span><span class="sxs-lookup"><span data-stu-id="bc25c-132">However, the new architecture uses virtualized networking components.</span></span> <span data-ttu-id="bc25c-133">这意味着，在初始预览版中生成 WSL 2 将更类似行为与虚拟机，例如：WSL 2 将具有与主机计算机不同的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="bc25c-133">This means that in initial preview builds WSL 2 will behave more similarly to a virtual machine, e.g: WSL 2 will have a different IP address than the host machine.</span></span> <span data-ttu-id="bc25c-134">我们致力于 WSL 2 感觉与 WSL 1 相同，包括提高我们网络的故事。</span><span class="sxs-lookup"><span data-stu-id="bc25c-134">We are committed to making WSL 2 feel the same as WSL 1, and that includes improving our networking story.</span></span> <span data-ttu-id="bc25c-135">我们预计会快速可以例如在 Linux 或 Windows 使用 localhost 访问网络的所有应用中添加的改进。</span><span class="sxs-lookup"><span data-stu-id="bc25c-135">We expect to add improvements as quickly as we are able to, such as accessing all networking apps from Linux or Windows using localhost.</span></span> <span data-ttu-id="bc25c-136">我们将发布我们网络的情景和改进有关详细信息如临近 WSL 2 的版本。</span><span class="sxs-lookup"><span data-stu-id="bc25c-136">We will be posting more details about our networking story and improvements as we approach the release of WSL 2.</span></span>

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a><span data-ttu-id="bc25c-137">可以在虚拟机中运行 WSL 2？</span><span class="sxs-lookup"><span data-stu-id="bc25c-137">Can I run WSL 2 in a virtual machine?</span></span>

<span data-ttu-id="bc25c-138">是的！</span><span class="sxs-lookup"><span data-stu-id="bc25c-138">Yes!</span></span> <span data-ttu-id="bc25c-139">您需要确保虚拟机具有嵌套虚拟化启用。</span><span class="sxs-lookup"><span data-stu-id="bc25c-139">You need to make sure that the virtual machine has nested virtualization enabled.</span></span> <span data-ttu-id="bc25c-140">通过使用管理员权限的 PowerShell 窗口中运行以下命令，可以在 HYPER-V 中启用此：</span><span class="sxs-lookup"><span data-stu-id="bc25c-140">This can be enabled in Hyper-V by running the following command in a PowerShell window with Administrator privileges:</span></span>

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

<span data-ttu-id="bc25c-141">请务必替换&lt;VMName&gt;与虚拟机的名称。</span><span class="sxs-lookup"><span data-stu-id="bc25c-141">Make sure to replace '&lt;VMName&gt;' with the name of your virtual machine.</span></span>

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/