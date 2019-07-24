---
title: WSL 2 常见问题
description: 有关适用于 Linux 2 的 Windows 子系统的常见问题
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a74f5e3f5879d0af274d2e2b10aaf05e95a97a6f
ms.sourcegitcommit: e16097a3d863bbda8c4655054f154415cdd7f2f5
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/05/2019
ms.locfileid: "67587144"
---
# <a name="wsl-2-faq"></a><span data-ttu-id="3a580-104">WSL 2 常见问题</span><span class="sxs-lookup"><span data-stu-id="3a580-104">WSL 2 FAQ</span></span>

<span data-ttu-id="3a580-105">下面是有关适用于 Linux 2 的 Windows 子系统的常见问题 (FAQ) 列表。</span><span class="sxs-lookup"><span data-stu-id="3a580-105">Below is a list of frequently asked questions (FAQ) about the Windows Subsystem for Linux 2.</span></span>

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a><span data-ttu-id="3a580-106">WSL 2 是否使用 Hyper-v？</span><span class="sxs-lookup"><span data-stu-id="3a580-106">Does WSL 2 use Hyper-V?</span></span> <span data-ttu-id="3a580-107">它是否可用于 Windows 10 家庭版？</span><span class="sxs-lookup"><span data-stu-id="3a580-107">Will it be available on Windows 10 Home?</span></span>

<span data-ttu-id="3a580-108">WSL 2 将在所有 WSL 当前可用的 Sku 上可用, 包括 Windows 10 家庭版。</span><span class="sxs-lookup"><span data-stu-id="3a580-108">WSL 2 will be available on all SKUs where WSL is currently available, including Windows 10 Home.</span></span>

<span data-ttu-id="3a580-109">最新版本的 WSL 使用 Hyper-v 体系结构来实现其虚拟化。</span><span class="sxs-lookup"><span data-stu-id="3a580-109">The newest version of WSL uses Hyper-V architecture to enable its virtualization.</span></span> <span data-ttu-id="3a580-110">此体系结构将出现在 "虚拟机平台" 可选组件中。</span><span class="sxs-lookup"><span data-stu-id="3a580-110">This architecture will be available in the 'Virtual Machine Platform' optional component.</span></span> <span data-ttu-id="3a580-111">此可选组件将在所有 Sku 上可用。</span><span class="sxs-lookup"><span data-stu-id="3a580-111">This optional component will be available on all SKUs.</span></span> <span data-ttu-id="3a580-112">当我们更深入地了解 WSL 2 版本时, 可以看到更多有关此体验的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3a580-112">You can expect to see more details about this experience soon as we get closer to the WSL 2 release.</span></span>

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a><span data-ttu-id="3a580-113">WSL 1 将发生什么情况？</span><span class="sxs-lookup"><span data-stu-id="3a580-113">What will happen to WSL 1?</span></span> <span data-ttu-id="3a580-114">是否放弃？</span><span class="sxs-lookup"><span data-stu-id="3a580-114">Will it be abandoned?</span></span>

<span data-ttu-id="3a580-115">目前没有计划弃用 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="3a580-115">We currently have no plans to deprecate WSL 1.</span></span> <span data-ttu-id="3a580-116">你可以并行运行 WSL 1 和 WSL 2 发行版, 还可以随时升级和降级任何发行版。</span><span class="sxs-lookup"><span data-stu-id="3a580-116">You can run WSL 1 and WSL 2 distros side by side, and can upgrade and downgrade any distro at any time.</span></span> <span data-ttu-id="3a580-117">将 WSL 2 添加为新的体系结构, 为 WSL 团队提供了一个更好的平台, 使其能够提供 WSL 一种令人惊叹的方式在 Windows 中运行 Linux 环境的功能。</span><span class="sxs-lookup"><span data-stu-id="3a580-117">Adding WSL 2 as a new architecture presents a better platform for the WSL team to deliver features that make WSL an amazing way to run a Linux environment in Windows.</span></span>

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a><span data-ttu-id="3a580-118">我是否能够运行 WSL 2 和其他第三方虚拟化工具 (如 VMware) 或 VirtualBox？</span><span class="sxs-lookup"><span data-stu-id="3a580-118">Will I be able to run WSL 2 and other 3rd party virtualization tools such as VMware, or VirtualBox?</span></span>

<span data-ttu-id="3a580-119">当使用 Hyper-v 时, 某些第三方应用程序无法正常工作, 这意味着当启用 WSL 2 时, 这些应用程序将无法运行。</span><span class="sxs-lookup"><span data-stu-id="3a580-119">Some 3rd party applications cannot work when Hyper-V is in use, which means they will not be able to run when WSL 2 is enabled.</span></span> <span data-ttu-id="3a580-120">遗憾的是, 在2018年12月6日发布的 VirtualBox 6.0.0 之前, 这包括 VMware 和 VirtualBox 的版本,[现在支持在 Windows 主机上将 hyper-v 作为回退执行核心][1]!)</span><span class="sxs-lookup"><span data-stu-id="3a580-120">Unfortunately, this does include VMware, and versions of VirtualBox before VirtualBox 6 (VirtualBox 6.0.0 released in December 2018 [now supports Hyper-V as a fallback execution core on a Windows host][1]!)</span></span>

<span data-ttu-id="3a580-121">我们正在研究帮助解决此问题的方法。</span><span class="sxs-lookup"><span data-stu-id="3a580-121">We are investigating ways to help resolve this issue.</span></span> <span data-ttu-id="3a580-122">例如, 我们公开一组称为[虚拟机监控程序平台][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s. This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3]的 api, 以及 VirtualBox 6 及更高版本, 它们现在都与 hyper-v 兼容。</span><span class="sxs-lookup"><span data-stu-id="3a580-122">For example, we expose a set of APIs called [Hypervisor Platform][2] that third-party virtualization providers can use to make their software compatible with Hyper-V’s. This lets applications use the Hyper-V architecture for their emulation such as [the Google Android Emulator][3], and VirtualBox 6 and above which are both now compatible with Hyper-V.</span></span>

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a><span data-ttu-id="3a580-123">能否在 WSL 2 中访问 GPU？</span><span class="sxs-lookup"><span data-stu-id="3a580-123">Can I access the GPU in WSL 2?</span></span> <span data-ttu-id="3a580-124">是否计划增加硬件支持？</span><span class="sxs-lookup"><span data-stu-id="3a580-124">Are there plans to increase hardware support?</span></span>

<span data-ttu-id="3a580-125">在 WSL 2 的初始版本中, 将限制硬件访问支持, 例如: 你将无法访问 GPU、串行或 USBs。</span><span class="sxs-lookup"><span data-stu-id="3a580-125">In initial releases of WSL 2 hardware access support will be limited, e.g: you will be unable to access the GPU, serial or USBs .</span></span> <span data-ttu-id="3a580-126">但是, 在积压工作 (backlog) 上添加更好的设备支持更高, 因为这会为希望与这些设备进行交互的开发人员打开更多用例。</span><span class="sxs-lookup"><span data-stu-id="3a580-126">However, adding better device support is high on our backlog, as this opens many more use cases for developers that wish to interact with these devices.</span></span> <span data-ttu-id="3a580-127">同时, 你始终可以使用具有串行端口和 USB 访问权限的 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="3a580-127">In the meantime, you can always use WSL 1 which has serial port and USB access.</span></span> <span data-ttu-id="3a580-128">请继续关注此博客并 WSL Twitter 上的团队成员, 随时了解即将到来的内部版本的最新功能, 并向我们提供有关你想要与之交互的设备的反馈!</span><span class="sxs-lookup"><span data-stu-id="3a580-128">Please stay tuned to this blog and WSL team members on Twitter to stay informed about the latest features coming to insider builds and reach out to give us feedback on what devices you’d like to interact with!</span></span>

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a><span data-ttu-id="3a580-129">WSL 2 是否能够使用网络应用程序？</span><span class="sxs-lookup"><span data-stu-id="3a580-129">Will WSL 2 be able to use networking applications?</span></span>

<span data-ttu-id="3a580-130">是的, 在常规网络应用程序中, 可以更快、更好地工作, 因为我们具有完全的系统调用兼容性。</span><span class="sxs-lookup"><span data-stu-id="3a580-130">Yes, in general networking applications will be faster and work better since we have full system call compatibility.</span></span> <span data-ttu-id="3a580-131">但是, 新的体系结构使用虚拟化的网络组件。</span><span class="sxs-lookup"><span data-stu-id="3a580-131">However, the new architecture uses virtualized networking components.</span></span> <span data-ttu-id="3a580-132">这意味着, 在初始预览版本中, WSL 2 的行为将更类似于虚拟机, 例如:WSL 2 的 IP 地址将与主机不同。</span><span class="sxs-lookup"><span data-stu-id="3a580-132">This means that in initial preview builds WSL 2 will behave more similarly to a virtual machine, e.g: WSL 2 will have a different IP address than the host machine.</span></span> <span data-ttu-id="3a580-133">我们承诺使 WSL 2 感觉与 WSL 1 相同, 这包括改善我们的网络故事。</span><span class="sxs-lookup"><span data-stu-id="3a580-133">We are committed to making WSL 2 feel the same as WSL 1, and that includes improving our networking story.</span></span> <span data-ttu-id="3a580-134">我们希望尽快添加改进, 如使用 localhost 从 Linux 或 Windows 访问所有网络应用。</span><span class="sxs-lookup"><span data-stu-id="3a580-134">We expect to add improvements as quickly as we are able to, such as accessing all networking apps from Linux or Windows using localhost.</span></span> <span data-ttu-id="3a580-135">我们将在 WSL 2 的发布时, 公布有关网络故事和改进的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="3a580-135">We will be posting more details about our networking story and improvements as we approach the release of WSL 2.</span></span>

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a><span data-ttu-id="3a580-136">能否在虚拟机中运行 WSL 2？</span><span class="sxs-lookup"><span data-stu-id="3a580-136">Can I run WSL 2 in a virtual machine?</span></span>

<span data-ttu-id="3a580-137">可以！</span><span class="sxs-lookup"><span data-stu-id="3a580-137">Yes!</span></span> <span data-ttu-id="3a580-138">你需要确保虚拟机已启用嵌套虚拟化。</span><span class="sxs-lookup"><span data-stu-id="3a580-138">You need to make sure that the virtual machine has nested virtualization enabled.</span></span> <span data-ttu-id="3a580-139">在 Hyper-v 中, 可以通过使用管理员权限在 PowerShell 窗口中运行以下命令来启用此功能:</span><span class="sxs-lookup"><span data-stu-id="3a580-139">This can be enabled in Hyper-V by running the following command in a PowerShell window with Administrator privileges:</span></span>

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

<span data-ttu-id="3a580-140">请确保将 "&lt;VMName&gt;" 替换为虚拟机的名称。</span><span class="sxs-lookup"><span data-stu-id="3a580-140">Make sure to replace '&lt;VMName&gt;' with the name of your virtual machine.</span></span>

## <a name="can-i-use-wslconf-in-wsl-2"></a><span data-ttu-id="3a580-141">能否在 WSL 2 中使用 wsl？</span><span class="sxs-lookup"><span data-stu-id="3a580-141">Can I use wsl.conf in WSL 2?</span></span>

<span data-ttu-id="3a580-142">WSL 2 支持 WSL 1 使用的同一个 WSL 文件。</span><span class="sxs-lookup"><span data-stu-id="3a580-142">WSL 2 supports the same wsl.conf file that WSL 1 uses.</span></span> <span data-ttu-id="3a580-143">这意味着, 在 WSL 1 发行版中设置的任何配置选项 (如 automounting Windows 驱动器、启用或禁用互操作、更改 Windows 驱动器将装载到的目录等) 都将在 WSL 2 内部工作。</span><span class="sxs-lookup"><span data-stu-id="3a580-143">This means that any configuration options that you had set in a WSL 1 distro, such as automounting Windows drives, enabling or disabling interop, changing the directory where Windows drives will be mounted, etc. will all work inside of WSL 2.</span></span> <span data-ttu-id="3a580-144">可在[发行版管理](./wsl-config.md)页的 WSL 中了解有关配置选项的详细信息。</span><span class="sxs-lookup"><span data-stu-id="3a580-144">You can learn more about the configuration options in WSL in the [Distro Management](./wsl-config.md) page.</span></span> 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/