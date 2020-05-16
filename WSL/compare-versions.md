---
title: 适用于 Linux 的 Windows 子系统概述
description: 了解适用于 Linux 的 Windows 子系统及其不同版本和使用方式。
keywords: BashOnWindows, bash, wsl, windows, windows 子系统, gnu, linux, ubuntu, debian, suse, windows 10, UX 更改, WSL 2, linux 内核, 网络应用程序, localhost, IPv6, 虚拟硬件磁盘, VHD, VHD 限制, VHD 错误
ms.date: 05/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 299caaaeb1bac60d2af780dfdd10a64b218ab1f1
ms.sourcegitcommit: 1b6191351bbf9e95f3c28fc67abe4bf1bcfd3336
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/13/2020
ms.locfileid: "83270851"
---
# <a name="comparing-wsl-2-and-wsl-1"></a><span data-ttu-id="f5b71-104">比较 WSL 2 和 WSL 1</span><span class="sxs-lookup"><span data-stu-id="f5b71-104">Comparing WSL 2 and WSL 1</span></span>

<span data-ttu-id="f5b71-105">将适用于 Linux 的 Windows 子系统更新到新版本的主要目标是，**提高文件系统性能**并支持**完全的系统调用兼容性**。</span><span class="sxs-lookup"><span data-stu-id="f5b71-105">The primary goals of updating the Windows Subsystem for Linux to a new version are to **increase file system performance** and support **full system call compatibility**.</span></span> 

<span data-ttu-id="f5b71-106">WSL 2 使用最新、最强大的虚拟化技术在轻量级实用工具虚拟机 (VM) 中运行 Linux 内核。</span><span class="sxs-lookup"><span data-stu-id="f5b71-106">WSL 2 uses the latest and greatest in virtualization technology to run a Linux kernel inside of a lightweight utility virtual machine (VM).</span></span> <span data-ttu-id="f5b71-107">但是，WSL 2 不是传统的 VM 体验。</span><span class="sxs-lookup"><span data-stu-id="f5b71-107">However, WSL 2 is not a traditional VM experience.</span></span> <span data-ttu-id="f5b71-108">[了解有关 WSL 2 体系结构的详细信息](#wsl-2-architecture)。</span><span class="sxs-lookup"><span data-stu-id="f5b71-108">[Learn more about the WSL 2 architecture](#wsl-2-architecture).</span></span>

## <a name="comparing-features"></a><span data-ttu-id="f5b71-109">比较功能</span><span class="sxs-lookup"><span data-stu-id="f5b71-109">Comparing features</span></span>

<span data-ttu-id="f5b71-110">功能</span><span class="sxs-lookup"><span data-stu-id="f5b71-110">Feature</span></span> | <span data-ttu-id="f5b71-111">WSL 1</span><span class="sxs-lookup"><span data-stu-id="f5b71-111">WSL 1</span></span> | <span data-ttu-id="f5b71-112">WSL 2</span><span class="sxs-lookup"><span data-stu-id="f5b71-112">WSL 2</span></span>
--- | --- | ---
 <span data-ttu-id="f5b71-113">Windows 和 Linux 之间的集成</span><span class="sxs-lookup"><span data-stu-id="f5b71-113">Integration between Windows and Linux</span></span>| ✅|✅
 <span data-ttu-id="f5b71-114">启动时间短</span><span class="sxs-lookup"><span data-stu-id="f5b71-114">Fast boot times</span></span>| ✅ | ✅
 <span data-ttu-id="f5b71-115">占用的资源量少</span><span class="sxs-lookup"><span data-stu-id="f5b71-115">Small resource foot print</span></span>| ✅ |✅
 <span data-ttu-id="f5b71-116">托管 VM</span><span class="sxs-lookup"><span data-stu-id="f5b71-116">Managed VM</span></span>| ❌ | ✅
 <span data-ttu-id="f5b71-117">完整的 Linux 内核</span><span class="sxs-lookup"><span data-stu-id="f5b71-117">Full Linux Kernel</span></span>| ❌ |✅
 <span data-ttu-id="f5b71-118">完全的系统调用兼容性</span><span class="sxs-lookup"><span data-stu-id="f5b71-118">Full system call compatibility</span></span>| ❌ | ✅
 <span data-ttu-id="f5b71-119">与 VM Ware 和 VirtualBox 一起运行</span><span class="sxs-lookup"><span data-stu-id="f5b71-119">Runs with VM Ware and VirtualBox</span></span>| ✅ |❌
 <span data-ttu-id="f5b71-120">跨 OS 文件系统的性能</span><span class="sxs-lookup"><span data-stu-id="f5b71-120">Performance across OS file systems</span></span>| ✅ | ❌

<span data-ttu-id="f5b71-121">已在使用 WSL 1 并且想要升级到 WSL 2？</span><span class="sxs-lookup"><span data-stu-id="f5b71-121">Already using WSL 1 and want to upgrade to WSL 2?</span></span> <span data-ttu-id="f5b71-122">请按照说明[更新到 WSL 2](./install-win10.md#update-to-wsl-2)！</span><span class="sxs-lookup"><span data-stu-id="f5b71-122">Follow the instructions to [update to WSL 2](./install-win10.md#update-to-wsl-2)!</span></span>

<span data-ttu-id="f5b71-123">只有 Windows 10 版本 2004 的内部版本 19041 或更高版本中才提供 WSL 2。</span><span class="sxs-lookup"><span data-stu-id="f5b71-123">WSL 2 is only available in Windows 10, Version 2004, Build 19041 or higher.</span></span> <span data-ttu-id="f5b71-124">需要[更新 Windows 版本](ms-settings:windowsupdate)并在“Release Preview”圈中[加入 Windows 预览体验计划](https://insider.windows.com/insidersigninboth/)，直到公开发行版在五月下旬推出。</span><span class="sxs-lookup"><span data-stu-id="f5b71-124">You will need to [update your Windows version](ms-settings:windowsupdate) and [join the Windows Insider program](https://insider.windows.com/insidersigninboth/) on the "Release Preview" ring until the public release in late May.</span></span>

## <a name="use-the-linux-file-system-for-faster-performance"></a><span data-ttu-id="f5b71-125">使用 Linux 文件系统以提高性能</span><span class="sxs-lookup"><span data-stu-id="f5b71-125">Use the Linux file system for faster performance</span></span>

<span data-ttu-id="f5b71-126">为了进行优化以实现最快的性能速度，请确保将项目文件存储在 Linux 文件系统（而非 Windows 文件系统）中。</span><span class="sxs-lookup"><span data-stu-id="f5b71-126">In order to optimize for the fastest performance speed, be sure to store your project files in the Linux file system (not the Windows file system).</span></span>

<span data-ttu-id="f5b71-127">例如，在存储 WSL 项目文件时：</span><span class="sxs-lookup"><span data-stu-id="f5b71-127">For example, when storing your WSL project files:</span></span>

* <span data-ttu-id="f5b71-128">使用 Linux 文件系统根目录：`\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="f5b71-128">Use the Linux file system root directory: `\\wsl$\Ubuntu-18.04\home\<user name>\Project`</span></span>
* <span data-ttu-id="f5b71-129">而不使用 Windows 文件系统根目录：`C:\Users\<user name>\Project`</span><span class="sxs-lookup"><span data-stu-id="f5b71-129">Not the Windows file system root directory: `C:\Users\<user name>\Project`</span></span>

<span data-ttu-id="f5b71-130">通过 WSL 分发版（如 Ubuntu）使用的项目文件必须位于 Linux 根文件系统中，才能利用更快的文件系统访问速度。</span><span class="sxs-lookup"><span data-stu-id="f5b71-130">Project files that you are working with using a WSL distribution (like Ubuntu) must be in the Linux root file system to take advantage of faster file system access.</span></span>

<span data-ttu-id="f5b71-131">可以使用 Windows 应用和工具（如文件资源管理器）访问 Linux 根文件系统。</span><span class="sxs-lookup"><span data-stu-id="f5b71-131">You can access your Linux root file system with Windows apps and tools like File Explorer.</span></span> <span data-ttu-id="f5b71-132">尝试打开 Linux 分发版（如 Ubuntu），通过输入以下命令确保你位于 Linux 主目录中：`cd ~`。</span><span class="sxs-lookup"><span data-stu-id="f5b71-132">Try opening a Linux distribution (like Ubuntu), be sure that you are in the Linux home directory by entering this command: `cd ~`.</span></span> <span data-ttu-id="f5b71-133">然后通过输入 `explorer.exe .`（不要忘记尾部的句点）  ，在文件资源管理器中打开 Linux 文件系统。</span><span class="sxs-lookup"><span data-stu-id="f5b71-133">Then open your Linux file system in File Explorer by entering *(don't forget the period at the end)*: `explorer.exe .`</span></span>

## <a name="exceptions-for-using-wsl-1-rather-than-wsl-2"></a><span data-ttu-id="f5b71-134">例外情况（使用 WSL 1 而不是 WSL 2）</span><span class="sxs-lookup"><span data-stu-id="f5b71-134">Exceptions for using WSL 1 rather than WSL 2</span></span>

<span data-ttu-id="f5b71-135">我们建议使用 WSL 2，因为它提供更快的性能和100% 的系统调用兼容性。</span><span class="sxs-lookup"><span data-stu-id="f5b71-135">We recommend that you use WSL 2 as it offers faster performance and 100% system call compatibility.</span></span> <span data-ttu-id="f5b71-136">但是，在某些特定情况下，你可能会更倾向于使用 WSL 1。</span><span class="sxs-lookup"><span data-stu-id="f5b71-136">However, there are a few specific scenarios where you might prefer using WSL 1.</span></span> <span data-ttu-id="f5b71-137">在以下情况下，请考虑使用 WSL 1：</span><span class="sxs-lookup"><span data-stu-id="f5b71-137">Consider using WSL 1 if:</span></span>

* <span data-ttu-id="f5b71-138">你的项目文件必须存储在 Windows 文件系统中。</span><span class="sxs-lookup"><span data-stu-id="f5b71-138">Your project files must be stored in the Windows file system.</span></span>
  * <span data-ttu-id="f5b71-139">如果你将使用 WSL Linux 分发版来访问 Windows 文件系统上的项目文件，并且这些文件无法存储在 Linux 文件系统上，那么，通过使用 WSL 1，你将跨 OS 文件系统实现更快的性能。</span><span class="sxs-lookup"><span data-stu-id="f5b71-139">If you will be using your WSL Linux distribution to access project files on the Windows file system, and these files cannot be stored on the Linux file system, you will achieve faster performance across the OS files systems by using WSL 1.</span></span>
* <span data-ttu-id="f5b71-140">一个项目要求对相同的文件使用 Windows 和 Linux 工具进行交叉编译。</span><span class="sxs-lookup"><span data-stu-id="f5b71-140">A project which requires cross-compilation using both Windows and Linux tools on the same files.</span></span>
  * <span data-ttu-id="f5b71-141">在 WSL 1 中，跨 Windows 和 Linux 操作系统的文件性能比 WSL 2 中更快，因此如果要使用 Windows 应用程序来访问 Linux 文件，则目前通过 WSL 1 可实现更快的性能。</span><span class="sxs-lookup"><span data-stu-id="f5b71-141">File performance across the Windows and Linux operating systems is faster in WSL 1 than WSL 2, so if you are using Windows applications to access Linux files, you will currently achieve faster performance with WSL 1.</span></span>

> [!NOTE]
> <span data-ttu-id="f5b71-142">请考虑尝试 VS Code [远程 WSL 扩展](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl)，以便使你不仅能够使用 Linux 命令行工具将项目文件存储在 Linux 文件系统上，而且还可以使用 Windows 上的 VS Code 在 Internet 浏览器中创作、编辑、调试或运行项目，而不会造成任何与跨 Linux 和 Windows 文件系统工作相关联的性能下降。</span><span class="sxs-lookup"><span data-stu-id="f5b71-142">Consider trying the VS Code [Remote WSL Extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-wsl) to enable you to store your project files on the Linux file system, using Linux command line tools, but also using VS Code on Windows to author, edit, debug, or run your project in an internet browser without any of the performance slow-downs associated with working across the Linux and Windows file systems.</span></span> <span data-ttu-id="f5b71-143">[了解详细信息](https://code.visualstudio.com/docs/remote/wsl)。</span><span class="sxs-lookup"><span data-stu-id="f5b71-143">[Learn more](https://code.visualstudio.com/docs/remote/wsl).</span></span>

## <a name="wsl-2-architecture"></a><span data-ttu-id="f5b71-144">WSL 2 体系结构</span><span class="sxs-lookup"><span data-stu-id="f5b71-144">WSL 2 architecture</span></span>

<span data-ttu-id="f5b71-145">传统的 VM 体验可能启动速度慢，是独立的，消耗大量资源，需要你花费时间进行管理。</span><span class="sxs-lookup"><span data-stu-id="f5b71-145">A traditional VM experience can be slow to boot up, is isolated, consumes lots of resources, and requires your time to manage it.</span></span> <span data-ttu-id="f5b71-146">WSL 2 没有这些属性。</span><span class="sxs-lookup"><span data-stu-id="f5b71-146">WSL 2 does not have these attributes.</span></span>

<span data-ttu-id="f5b71-147">WSL 2 有 WSL 1 的优点，包括 Windows 和 Linux 之间的无缝集成，启动时间短，资源占用量少，并且无需 VM 配置或管理。</span><span class="sxs-lookup"><span data-stu-id="f5b71-147">WSL 2 provides the benefits of WSL 1, including seamless integration between Windows and Linux, fast boot times, a small resource footprint, and requires no VM configuration or management.</span></span> <span data-ttu-id="f5b71-148">虽然 WSL 2 确实使用 VM，但 VM 是在幕后管理和运行的，因此你将具有与 WSL 1 相同的用户体验。</span><span class="sxs-lookup"><span data-stu-id="f5b71-148">While WSL 2 does use a VM, it is managed and run behind the scenes, leaving you with the same user experience as WSL 1.</span></span>

### <a name="full-linux-kernel"></a><span data-ttu-id="f5b71-149">完整的 Linux 内核</span><span class="sxs-lookup"><span data-stu-id="f5b71-149">Full Linux kernel</span></span>

<span data-ttu-id="f5b71-150">WSL 2 中的 Linux 内核是 Microsoft 根据最新的稳定版分支（基于 kernel.org 上提供的源代码）构建的。此内核已专门针对 WSL 2 进行了调整，针对大小和性能进行了优化，以便在 Windows 上提供良好的 Linux 体验。</span><span class="sxs-lookup"><span data-stu-id="f5b71-150">The Linux kernel in WSL 2 is built by Microsoft from the latest stable branch, based on the source available at kernel.org. This kernel has been specially tuned for WSL 2, optimizing for size and performance to provide an amazing Linux experience on Windows.</span></span> <span data-ttu-id="f5b71-151">内核将由 Windows 更新提供服务，这意味着你将获得最新的安全修补程序和内核改进功能，而无需自行管理它。</span><span class="sxs-lookup"><span data-stu-id="f5b71-151">The kernel will be serviced by Windows updates, which means you will get the latest security fixes and kernel improvements without needing to manage it yourself.</span></span>

<span data-ttu-id="f5b71-152">[WSL 2 Linux 内核是开源的](https://github.com/microsoft/WSL2-Linux-Kernel)。</span><span class="sxs-lookup"><span data-stu-id="f5b71-152">The [WSL 2 Linux kernel is open source](https://github.com/microsoft/WSL2-Linux-Kernel).</span></span> <span data-ttu-id="f5b71-153">如果你想要了解详细信息，请查看由构建该内核的团队撰写的博客文章[随 Windows 一起提供 Linux 内核](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)。</span><span class="sxs-lookup"><span data-stu-id="f5b71-153">If you'd like to learn more, check out the blog post [Shipping a Linux Kernel with Windows](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/) written by the team that built it.</span></span>

### <a name="increased-file-io-performance"></a><span data-ttu-id="f5b71-154">提升了文件 IO 性能</span><span class="sxs-lookup"><span data-stu-id="f5b71-154">Increased file IO performance</span></span>

<span data-ttu-id="f5b71-155">在使用 WSL 2 的情况下，文件密集型操作（如 git 克隆、npm 安装、apt 更新、apt 升级等）的速度都明显更快。</span><span class="sxs-lookup"><span data-stu-id="f5b71-155">File intensive operations like git clone, npm install, apt update, apt upgrade, and more are all be noticeably faster with WSL 2.</span></span>

<span data-ttu-id="f5b71-156">实际的速度提升将取决于你运行的应用以及它与文件系统的交互方式。</span><span class="sxs-lookup"><span data-stu-id="f5b71-156">The actual speed increase will depend on which app you're running and how it is interacting with the file system.</span></span> <span data-ttu-id="f5b71-157">在对压缩的 tarball 进行解包时，WSL 2 的初始版本的运行速度比 WSL 1 快达 20 倍，在各种项目上使用 git 克隆、npm 安装和 cmake 时，大约快 2-5 倍。</span><span class="sxs-lookup"><span data-stu-id="f5b71-157">Initial versions of WSL 2 run up to 20x faster compared to WSL 1 when unpacking a zipped tarball, and around 2-5x faster when using git clone, npm install and cmake on various projects.</span></span>

### <a name="full-system-call-compatibility"></a><span data-ttu-id="f5b71-158">完全的系统调用兼容性</span><span class="sxs-lookup"><span data-stu-id="f5b71-158">Full system call compatibility</span></span>

<span data-ttu-id="f5b71-159">Linux 二进制文件使用系统调用来执行访问文件、请求内存、创建进程等功能。</span><span class="sxs-lookup"><span data-stu-id="f5b71-159">Linux binaries use system calls to perform functions such as accessing files, requesting memory, creating processes, and more.</span></span> <span data-ttu-id="f5b71-160">虽然 WSL 1 使用的是由 WSL 团队构建的转换层，但 WSL 2 包括了自己的 Linux 内核，具有完全的系统调用兼容性。</span><span class="sxs-lookup"><span data-stu-id="f5b71-160">Whereas WSL 1 used a translation layer that was built by the WSL team, WSL 2 includes its own Linux kernel with full system call compatibility.</span></span> <span data-ttu-id="f5b71-161">优点包括：</span><span class="sxs-lookup"><span data-stu-id="f5b71-161">Benefits include:</span></span>

* <span data-ttu-id="f5b71-162">可以在 WSL 内部运行的一组全新应用，例如 **[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** 等。</span><span class="sxs-lookup"><span data-stu-id="f5b71-162">A whole new set of apps that you can run inside of WSL, such as **[Docker](https://code.visualstudio.com/blogs/2020/03/02/docker-in-wsl2)** and more.</span></span>

* <span data-ttu-id="f5b71-163">对 Linux 内核的任何更新都立即可供使用。</span><span class="sxs-lookup"><span data-stu-id="f5b71-163">Any updates to the Linux kernel are immediately ready for use.</span></span> <span data-ttu-id="f5b71-164">（无需等待 WSL 团队实现更新并添加更改）。</span><span class="sxs-lookup"><span data-stu-id="f5b71-164">(You don't have to wait for the WSL team to implement updates and add the changes).</span></span>

### <a name="wsl-2-uses-a-smaller-amount-of-memory-on-startup"></a><span data-ttu-id="f5b71-165">WSL 2 在启动时使用的内存量更少</span><span class="sxs-lookup"><span data-stu-id="f5b71-165">WSL 2 uses a smaller amount of memory on startup</span></span>

<span data-ttu-id="f5b71-166">WSL 2 在实际 Linux 内核上使用轻量级实用工具 VM，内存占用量很小。</span><span class="sxs-lookup"><span data-stu-id="f5b71-166">WSL 2 uses a lightweight utility VM on a real Linux kernel with a small memory footprint.</span></span> <span data-ttu-id="f5b71-167">该实用工具将在启动时分配虚拟地址支持的内存。</span><span class="sxs-lookup"><span data-stu-id="f5b71-167">The utility will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="f5b71-168">它已经过配置，在启动时使用的内存占比小于 WSL 1 所需的内存占比。</span><span class="sxs-lookup"><span data-stu-id="f5b71-168">It is configured to start with a smaller proportion of your total memory that what was required for WSL 1.</span></span>

## <a name="accessing-network-applications"></a><span data-ttu-id="f5b71-169">访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="f5b71-169">Accessing network applications</span></span>

### <a name="accessing-linux-networking-apps-from-windows-localhost"></a><span data-ttu-id="f5b71-170">从 Windows (localhost) 访问 Linux 网络应用</span><span class="sxs-lookup"><span data-stu-id="f5b71-170">Accessing Linux networking apps from Windows (localhost)</span></span>

<span data-ttu-id="f5b71-171">如果要在 Linux 分发版中构建网络应用（例如，在 NodeJS 或 SQL server 上运行的应用），可以使用 `localhost` 从 Windows 应用（如 Edge 或 Chrome Internet 浏览器）访问它（就像往常一样）。</span><span class="sxs-lookup"><span data-stu-id="f5b71-171">If you are building a networking app (for example an app running on a NodeJS or SQL server) in your Linux distribution, you can access it from a Windows app (like your Edge or Chrome internet browser) using `localhost` (just like you normally would).</span></span>

<span data-ttu-id="f5b71-172">但是，如果运行的是较旧版本的 Windows（版本 18945 或更低版本），则需要获取 Linux 主机 VM 的 IP 地址（或[更新到最新的 Windows 版本](ms-settings:windowsupdate)）。</span><span class="sxs-lookup"><span data-stu-id="f5b71-172">However, if you are running an older version of Windows (Build 18945 or less), you will need to get the IP address of the Linux host VM (or [update to the latest Windows version](ms-settings:windowsupdate)).</span></span>

<span data-ttu-id="f5b71-173">若要查找为 Linux 分发版提供支持的虚拟机的 IP 地址，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="f5b71-173">To find the IP address of the virtual machine powering your Linux distribution:</span></span>

* <span data-ttu-id="f5b71-174">在 WSL 分发版（即 Ubuntu）中运行以下命令：`ip addr`</span><span class="sxs-lookup"><span data-stu-id="f5b71-174">From your WSL distribution (ie Ubuntu), run the command: `ip addr`</span></span>
* <span data-ttu-id="f5b71-175">查找并复制 `eth0` 接口的 `inet` 值下的地址。</span><span class="sxs-lookup"><span data-stu-id="f5b71-175">Find and copy the address under the `inet` value of the `eth0` interface.</span></span>
* <span data-ttu-id="f5b71-176">如果已安装 grep 工具，请通过使用以下命令筛选输出来更轻松地查找此地址：`ip addr | grep eth0`</span><span class="sxs-lookup"><span data-stu-id="f5b71-176">If you have the grep tool installed, find this more easily by filtering the output with the command: `ip addr | grep eth0`</span></span>
* <span data-ttu-id="f5b71-177">使用此 IP 地址连接到 Linux 服务器。</span><span class="sxs-lookup"><span data-stu-id="f5b71-177">Connect to your Linux server using this IP address.</span></span>

<span data-ttu-id="f5b71-178">下图显示了一个示例，该示例使用 Edge 浏览器连接到 Node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="f5b71-178">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-networking-apps-from-linux-host-ip"></a><span data-ttu-id="f5b71-180">从 Linux（主机 IP）访问 Windows 网络应用</span><span class="sxs-lookup"><span data-stu-id="f5b71-180">Accessing Windows networking apps from Linux (host IP)</span></span>

<span data-ttu-id="f5b71-181">如果要从 Linux 分发版（即 Ubuntu）访问 Windows 上运行的网络应用（例如，在 NodeJS 或 SQL 服务器上运行的应用），则需要使用主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="f5b71-181">If you want to access a networking app running on Windows (for example an app running on a NodeJS or SQL server) from your Linux distribution (ie Ubuntu), then you need to use the IP address of your host machine.</span></span> <span data-ttu-id="f5b71-182">虽然这不是一种常见方案，但你可以执行以下步骤来使其可行。</span><span class="sxs-lookup"><span data-stu-id="f5b71-182">While this is not a common scenario, you can follow these steps to make it work.</span></span>
    - <span data-ttu-id="f5b71-183">通过在 Linux 分发版中运行以下命令来获取主机的 IP 地址：`cat /etc/resolv.conf`</span><span class="sxs-lookup"><span data-stu-id="f5b71-183">Obtain the IP address of your host machine by running this command from your Linux distribution: `cat /etc/resolv.conf`</span></span>
    - <span data-ttu-id="f5b71-184">复制以下词语后面的 IP 地址：`nameserver`。</span><span class="sxs-lookup"><span data-stu-id="f5b71-184">Copy the IP address following the term: `nameserver`.</span></span>
    - <span data-ttu-id="f5b71-185">使用复制的 IP 地址连接到任何 Windows 服务器。</span><span class="sxs-lookup"><span data-stu-id="f5b71-185">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="f5b71-186">下图显示了一个示例，该示例说明如何通过 curl 连接到在 Windows 中运行的 Node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="f5b71-186">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span>

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

### <a name="additional-networking-considerations"></a><span data-ttu-id="f5b71-188">其他网络注意事项</span><span class="sxs-lookup"><span data-stu-id="f5b71-188">Additional networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="f5b71-189">通过远程 IP 地址进行连接</span><span class="sxs-lookup"><span data-stu-id="f5b71-189">Connecting via remote IP addresses</span></span>

<span data-ttu-id="f5b71-190">当使用远程 IP 地址连接到应用程序时，它们将被视为来自局域网 (LAN) 的连接。</span><span class="sxs-lookup"><span data-stu-id="f5b71-190">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="f5b71-191">这意味着你需要确保你的应用程序可以接受 LAN 连接。</span><span class="sxs-lookup"><span data-stu-id="f5b71-191">This means that you will need to make sure your application can accept LAN connections.</span></span>

<span data-ttu-id="f5b71-192">例如，你可能需要将应用程序绑定到 `0.0.0.0` 而非 `127.0.0.1`。</span><span class="sxs-lookup"><span data-stu-id="f5b71-192">For example, you may need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="f5b71-193">以使用 Flask 的 Python 应用为例，可以通过以下命令执行此操作：`app.run(host='0.0.0.0')`。</span><span class="sxs-lookup"><span data-stu-id="f5b71-193">In the example of a Python app using Flask, this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="f5b71-194">进行这些更改时请注意安全性，因为这将允许来自你的 LAN 的连接。</span><span class="sxs-lookup"><span data-stu-id="f5b71-194">Please keep security in mind when making these changes as this will allow connections from your LAN.</span></span>

#### <a name="accessing-a-wsl-2-distribution-from-your-local-area-network-lan"></a><span data-ttu-id="f5b71-195">从局域网 (LAN) 访问 WSL 2 分发版</span><span class="sxs-lookup"><span data-stu-id="f5b71-195">Accessing a WSL 2 distribution from your local area network (LAN)</span></span>

<span data-ttu-id="f5b71-196">当使用 WSL 1 分发版时，如果计算机设置为可供 LAN 访问，那么在 WSL 中运行的应用程序也可供在 LAN 中访问。</span><span class="sxs-lookup"><span data-stu-id="f5b71-196">When using a WSL 1 distribution, if your computer was set up to be accessed by your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span>

<span data-ttu-id="f5b71-197">这不是 WSL 2 中的默认情况。</span><span class="sxs-lookup"><span data-stu-id="f5b71-197">This isn't the default case in WSL 2.</span></span> <span data-ttu-id="f5b71-198">WSL 2 有一个带有其自己独一无二的 IP 地址的虚拟化以太网适配器。</span><span class="sxs-lookup"><span data-stu-id="f5b71-198">WSL 2 has a virtualized ethernet adapter with its own unique IP address.</span></span> <span data-ttu-id="f5b71-199">目前，若要启用此工作流，你需要执行与常规虚拟机相同的步骤。</span><span class="sxs-lookup"><span data-stu-id="f5b71-199">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="f5b71-200">（我们正在寻找改善此体验的方法。）</span><span class="sxs-lookup"><span data-stu-id="f5b71-200">(We are looking into ways to improve this experience.)</span></span>

#### <a name="ipv6-access"></a><span data-ttu-id="f5b71-201">IPv6 访问</span><span class="sxs-lookup"><span data-stu-id="f5b71-201">IPv6 access</span></span>

<span data-ttu-id="f5b71-202">WSL2 分发版目前无法访问纯 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="f5b71-202">WSL 2 distributions currently cannot reach IPv6-only addresses.</span></span> <span data-ttu-id="f5b71-203">我们正在致力于添加此功能。</span><span class="sxs-lookup"><span data-stu-id="f5b71-203">We are working on adding this feature.</span></span>

## <a name="expanding-the-size-of-your-wsl-2-virtual-hardware-disk"></a><span data-ttu-id="f5b71-204">扩展 WSL 2 虚拟硬件磁盘的大小</span><span class="sxs-lookup"><span data-stu-id="f5b71-204">Expanding the size of your WSL 2 Virtual Hardware Disk</span></span>

<span data-ttu-id="f5b71-205">WSL 2 使用虚拟硬件磁盘 (VHD) 来存储 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="f5b71-205">WSL 2 uses a Virtual Hardware Disk (VHD) to store your Linux files.</span></span> <span data-ttu-id="f5b71-206">如果达到其最大大小，则可能需要对其进行扩展。</span><span class="sxs-lookup"><span data-stu-id="f5b71-206">If you reach its max size you may need to expand it.</span></span>

<span data-ttu-id="f5b71-207">WSL 2 VHD 使用 ext4 文件系统。</span><span class="sxs-lookup"><span data-stu-id="f5b71-207">The WSL 2 VHD uses the ext4 file system.</span></span> <span data-ttu-id="f5b71-208">此 VHD 会自动调整大小以满足你的存储需求，并且其最大大小为 256GB。</span><span class="sxs-lookup"><span data-stu-id="f5b71-208">This VHD automatically resizes to meet your storage needs and has an initial maximum size of 256GB.</span></span> <span data-ttu-id="f5b71-209">如果你的分发版大小增长到大于 256GB，则会显示错误，指出磁盘空间不足。</span><span class="sxs-lookup"><span data-stu-id="f5b71-209">If your distribution grows in size to be greater than 256GB, you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="f5b71-210">可以通过扩展 VHD 大小来纠正此错误。</span><span class="sxs-lookup"><span data-stu-id="f5b71-210">You can fix this error by expanding the VHD size.</span></span>

<span data-ttu-id="f5b71-211">若要将最大 VHD 大小扩展到超过 256GB，请执行以下操作：</span><span class="sxs-lookup"><span data-stu-id="f5b71-211">To expand your maximum VHD size beyond 256GB:</span></span>

1. <span data-ttu-id="f5b71-212">使用 `wsl --shutdown` 命令终止所有 WSL 实例</span><span class="sxs-lookup"><span data-stu-id="f5b71-212">Terminate all WSL instances using the command: `wsl --shutdown`</span></span>

2. <span data-ttu-id="f5b71-213">查找你的分发版安装包名称（“PackageFamilyName”）</span><span class="sxs-lookup"><span data-stu-id="f5b71-213">Find your distribution installation package name ('PackageFamilyName')</span></span>
    * <span data-ttu-id="f5b71-214">使用 PowerShell（其中，“distro”是分发版名称）输入以下命令：</span><span class="sxs-lookup"><span data-stu-id="f5b71-214">Using PowerShell (where 'distro' is your distribution name) enter the command:</span></span>
    * `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`

3. <span data-ttu-id="f5b71-215">找到 WSL 2 安装使用的 VHD 文件 `fullpath`，这将是你的 `pathToVHD`：</span><span class="sxs-lookup"><span data-stu-id="f5b71-215">Locate the VHD file `fullpath` used by your WSL 2 installation, this will be your `pathToVHD`:</span></span>
     * `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`

4. <span data-ttu-id="f5b71-216">通过完成以下命令调整 WSL 2 VHD 的大小：</span><span class="sxs-lookup"><span data-stu-id="f5b71-216">Resize your WSL 2 VHD by completing the following commands:</span></span>
   * <span data-ttu-id="f5b71-217">以管理员权限打开 Windows 命令提示，然后输入：</span><span class="sxs-lookup"><span data-stu-id="f5b71-217">Open Windows Command Prompt with admin privileges and enter:</span></span>
      * `diskpart`
      * `Select vdisk file="<pathToVHD>"`
      * `expand vdisk maximum="<sizeInMegaBytes>"`

5. <span data-ttu-id="f5b71-218">启动 WSL 分发版（例如 Ubuntu）。</span><span class="sxs-lookup"><span data-stu-id="f5b71-218">Launch your WSL distribution (Ubuntu, for example).</span></span>

6. <span data-ttu-id="f5b71-219">通过从 Linux 分发版命令行运行以下命令，让 WSL 知道它可以扩展其文件系统的大小：</span><span class="sxs-lookup"><span data-stu-id="f5b71-219">Make WSL aware that it can expand its file system's size by running these commands from your Linux distribution command line:</span></span>
    * `sudo mount -t devtmpfs none /dev`
    * `mount | grep ext4`
    * <span data-ttu-id="f5b71-220">复制此项的名称，该名称类似于：`/dev/sdXX`（X 表示任何其他字符）</span><span class="sxs-lookup"><span data-stu-id="f5b71-220">Copy the name of this entry, which will look like: `/dev/sdXX` (with the X representing any other character)</span></span>
    * `sudo resize2fs /dev/sdXX`
    * <span data-ttu-id="f5b71-221">使用前面复制的值。</span><span class="sxs-lookup"><span data-stu-id="f5b71-221">Use the value you copied earlier.</span></span> <span data-ttu-id="f5b71-222">可能还需要安装 resize2fs：`apt install resize2fs`</span><span class="sxs-lookup"><span data-stu-id="f5b71-222">You may also need to install resize2fs: `apt install resize2fs`</span></span>

> [!NOTE]
> <span data-ttu-id="f5b71-223">通常情况下，不要使用 Windows 工具或编辑器来修改、移动或访问 AppData 文件夹中与 WSL 相关的文件。</span><span class="sxs-lookup"><span data-stu-id="f5b71-223">In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="f5b71-224">这样做可能会导致 Linux 分发版损坏。</span><span class="sxs-lookup"><span data-stu-id="f5b71-224">Doing so could cause your Linux distribution to become corrupted.</span></span>
