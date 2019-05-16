---
title: 常见问题 (FAQ)
description: Frequently Asked Questions about Windows 子系统适用于 Linux。
keywords: BashOnWindows、 bash、 wsl、 windows、 windowssubsystem、 常见问题
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 80675d8452b626ebe1d235774167c5ff27e4b44d
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063265"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="b0a6a-104">Frequently Asked Questions about Windows 子系统适用于 Linux</span><span class="sxs-lookup"><span data-stu-id="b0a6a-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="b0a6a-105">什么是 Windows 子系统用于 Linux (WSL)？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="b0a6a-106">Windows 子系统用于 Linux (WSL) 是一个新的 Windows 10 功能，使您能够直接在 Windows 上运行本机 Linux 命令行工具，以及传统 Windows 桌面和新式应用商店应用。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="b0a6a-107">请参阅[有关页面](./about.md)的更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="b0a6a-108">有关 WSL 是谁？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-108">Who is WSL for?</span></span>
<span data-ttu-id="b0a6a-109">这是开发人员-尤其是 web 开发人员和工作或使用开放源代码项目的员工的主要工具。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="b0a6a-110">这允许那些希望/需要使用 Bash，常见的 Linux 工具 (`sed`，`awk`等) 和许多 Linux 第一个工具 （Ruby、 Python 等） 在 Windows 上使用其工具链。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="b0a6a-111">使用 WSL 可以做什么？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-111">What can I do with WSL?</span></span>
<span data-ttu-id="b0a6a-112">WSL 提供应用程序 Bash.exe，启动时调用，此时会打开一个 Windows 控制台运行的 Bash shell。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="b0a6a-113">使用 Bash，可以运行 Linux 的命令行工具和应用程序。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="b0a6a-114">例如，键入`lsb_release -a`并按 enter，可以看到当前正在运行的 Linux 发行版的详细信息：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![发行版的详细信息的屏幕截图](media/distro.png)

<span data-ttu-id="b0a6a-116">您还可以访问从 Linux Bash shell 中的本地计算机的文件系统-您会发现您的本地驱动器装载在`/mnt`文件夹。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="b0a6a-117">例如，你`C:`驱动器装载在`/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="b0a6a-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![加载的 C 驱动器的屏幕截图](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="b0a6a-119">什么是 Bash？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-119">What is Bash?</span></span>
<span data-ttu-id="b0a6a-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是一种流行的基于文本的外壳和命令语言。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="b0a6a-121">它是包含在 Ubuntu 和其他 Linux 发行版中，并在 macOS 中的默认外壳。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="b0a6a-122">用户键入到 shell 中执行脚本和/或运行命令和工具来完成许多任务的命令。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="b0a6a-123">这是如何实现的？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-123">How does this work?</span></span>
<span data-ttu-id="b0a6a-124">请查看我们[博客](https://blogs.msdn.microsoft.com/wsl/)我们进入有关基础技术的详细信息。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="b0a6a-125">为什么要使用 WSL 而不是 Linux VM 中？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="b0a6a-126">WSL 需要较少的资源 （CPU、 内存和存储） 比完整的虚拟机。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="b0a6a-127">WSL 还允许您运行 Linux 命令行工具和应用程序和 Windows 命令行中，桌面和应用商店应用，以及访问 Windows 文件从 Linux 中。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="b0a6a-128">这样，如果你想在同一组文件上使用 Windows 应用和 Linux 命令行工具。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="b0a6a-129">为什么要使用，例如，而不是在 Windows 上的 Linux 上的 Ruby？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="b0a6a-130">假设运行它们的环境的行为类似于 Linux 生成一些跨平台工具。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="b0a6a-131">例如，一些工具假定他们可访问非常长文件路径或特定的文件/文件夹存在。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="b0a6a-132">这通常会造成问题在通常的行为的 Windows 上以不同的方式从 Linux。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="b0a6a-133">许多语言，如 Ruby 和节点通常是移植到，并在 Windows 上运行很好。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="b0a6a-134">但是，并非所有节点/NPM 库所有者的 Ruby Gem 的端口及其库来支持 Windows，并且许多具有特定于 Linux 的依赖项。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="b0a6a-135">通常，这可能导致系统使用此类工具和库生成和有时运行时错误或不需要的行为在 Windows 上遇到问题生成。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="b0a6a-136">这些是只是一些导致许多人提出 Microsoft 以提高 Windows 的命令行工具和什么促使我们与 Canonical 启用本机 Bash 和 Linux 命令行工具在 Windows 上运行的问题。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="b0a6a-137">适用于 PowerShell，这意味着什么？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="b0a6a-138">同时使用 OSS 项目时，有许多方案是非常有用，放入 Bash 从 PowerShell 提示。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="b0a6a-139">Bash 支持是补充并增强了 Windows，从而允许 PowerShell 和 PowerShell 社区利用其他常用技术上的命令行中的值。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="b0a6a-140">详细了解的 PowerShell 团队博客- [Bash Windows:为什么这真的非常棒和 PowerShell 的含义](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="b0a6a-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="b0a6a-141">在 WSL 运行所有 Linux 应用</span><span class="sxs-lookup"><span data-stu-id="b0a6a-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="b0a6a-142">不！</span><span class="sxs-lookup"><span data-stu-id="b0a6a-142">No!</span></span> <span data-ttu-id="b0a6a-143">WSL 是旨在使用户需要使用这些运行 Bash 和 core 在 Windows 上的 Linux 命令行工具的工具。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="b0a6a-144">WSL does**不**旨在支持 GUI 桌面或应用程序 （例如 Gnome，KDE，等等。）</span><span class="sxs-lookup"><span data-stu-id="b0a6a-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="b0a6a-145">此外，即使你将能够运行许多常用的服务器应用程序 (例如 Redis)，我们不建议用于托管生产服务 WSL – Microsoft 提供了多种解决方案，用于运行生产 Linux 工作负荷在 Azure 中，HYPER-V 和 Docker。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="b0a6a-146">WSL 中包括哪些 Windows Sku？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="b0a6a-147">适用于 Linux 的 Windows 子系统是在桌面版本的 Windows 的 Windows 10 周年版及创意者更新或更高版本上可用。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="b0a6a-148">从开始 Fall Creators update WSL 将在桌面和服务器 Windows Sku 上可用。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="b0a6a-149">WSL 支持哪些处理器？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-149">What processors does WSL support?</span></span>
<span data-ttu-id="b0a6a-150">WSL 支持 x64 和 ARM Cpu。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="b0a6a-151">如何访问我的 c： 驱动器？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-151">How do I access my C: drive?</span></span>
<span data-ttu-id="b0a6a-152">在本地计算机上的硬盘驱动器的装入点自动创建，并可以轻松访问 Windows 文件系统。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="b0a6a-153">**/mnt/\<驱动器号 > /**</span><span class="sxs-lookup"><span data-stu-id="b0a6a-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="b0a6a-154">用法示例为`cd /mnt/c`访问 c:\\</span><span class="sxs-lookup"><span data-stu-id="b0a6a-154">Example usage would be `cd /mnt/c` to access c:\\</span></span>

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="b0a6a-155">如何使用 Linux 应用使用 Windows 文件？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="b0a6a-156">WSL 的优势之一能够访问你通过 Windows 和 Linux 应用程序或工具的文件。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="b0a6a-157">WSL 装载用的计算机的固定的驱动器`/mnt/<drive>`Linux 发行版中的文件夹。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="b0a6a-158">例如，你`C:`下装载驱动器 `/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="b0a6a-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="b0a6a-159">使用你已装载的驱动器，你可以编辑代码中，例如，`C:\dev\myproj\`使用[Visual Studio](https://visualstudio.microsoft.com/vs/) / 或[VS Code](https://code.visualstudio.com/)，并生成/测试 Linux 中的代码的访问通过的相同文件`\mnt\c\dev\myproj`。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `\mnt\c\dev\myproj`.</span></span>

> <span data-ttu-id="b0a6a-160">**重要说明**:使用 WSL 的主要限制之一是，不支持直接访问/更改使用 Windows 应用程序或工具的 Linux 发行版的文件系统中的文件。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="b0a6a-161">请参阅：[不会更改使用 Windows 应用程序和工具的 Linux 文件](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="b0a6a-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="b0a6a-162">是在 Linux 驱动器中的文件不同于已装载的 Windows 驱动器？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="b0a6a-163">Linux 根下的文件 (即`/`) 受 WSL 模拟 Linux 特定行为，包括但不是限于：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="b0a6a-164">包含无效 Windows 文件名字符的文件</span><span class="sxs-lookup"><span data-stu-id="b0a6a-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="b0a6a-165">为非管理员用户创建的符号链接</span><span class="sxs-lookup"><span data-stu-id="b0a6a-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="b0a6a-166">更改通过 chmod 和 chown 文件属性</span><span class="sxs-lookup"><span data-stu-id="b0a6a-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="b0a6a-167">文件/文件夹区分大小写</span><span class="sxs-lookup"><span data-stu-id="b0a6a-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="b0a6a-168">已装载的驱动器中的文件由 Windows 控制，并具有以下行为：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="b0a6a-169">支持区分大小写</span><span class="sxs-lookup"><span data-stu-id="b0a6a-169">Support case sensitivity</span></span>
   * <span data-ttu-id="b0a6a-170">所有权限都设置为最能反映 Windows 权限</span><span class="sxs-lookup"><span data-stu-id="b0a6a-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="b0a6a-171">为什么有这么多的错误时运行的 apt-get 升级？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="b0a6a-172">某些包使用我们尚未实现的功能。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="b0a6a-173">`udev`例如，尚不支持并导致多`apt-get upgrade`错误。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="b0a6a-174">若要修复与相关的问题`udev`，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="b0a6a-175">写入到以下`/usr/sbin/policy-rc.d`并保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="b0a6a-176">添加将执行权限 `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="b0a6a-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="b0a6a-177">运行以下命令</span><span class="sxs-lookup"><span data-stu-id="b0a6a-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="b0a6a-178">如何卸载 WSL 分发？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="b0a6a-179">在生成之前 1709 (版本 16299) 打开命令提示符并运行：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="b0a6a-180">通过右键单击应用磁贴上，单击卸载，或者通过 PowerShell 使用从应用商店安装 WSL 分发可以卸载其他任何 Windows 应用一样[ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="b0a6a-181">Ping 为什么生成权限被拒绝错误？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="b0a6a-182">在 WSL 中生成 < 14926，ping 所需 WSL 中通过权限提升的控制台运行。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="b0a6a-183">此问题已修复生成 14926 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="b0a6a-184">如何运行 OpenSSH 服务器？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="b0a6a-185">在 Windows 中的管理员权限才可在 WSL 中运行 OpenSSH。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="b0a6a-186">若要运行的 OpenSSH 服务器，在作为管理员，Windows 上运行 Ubuntu 上的 Bash 或 CMD/PowerShell 提示符下使用管理员特权运行 bash.exe。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="b0a6a-187">为何收到"错误：0x80040306"当我尝试安装？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="b0a6a-188">WSL 不支持旧版控制台中运行。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="b0a6a-189">若要关闭旧版控制台：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="b0a6a-190">打开 WSL、 PowerShell 或 Cmd</span><span class="sxs-lookup"><span data-stu-id="b0a6a-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="b0a6a-191">右键单击标题栏-> 属性-> 取消选中"使用传统控制台"</span><span class="sxs-lookup"><span data-stu-id="b0a6a-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="b0a6a-192">单击“确定”</span><span class="sxs-lookup"><span data-stu-id="b0a6a-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="b0a6a-193">为何收到"错误：0x80040154"当我运行 bash.exe 升级 Windows 之后？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="b0a6a-194">"Windows 子系统适用于 Linux"功能可能会禁用在 Windows 更新过程。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="b0a6a-195">如果发生这种情况必须在重新启用 Windows 功能。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="b0a6a-196">有关启用"Windows 子系统适用于 Linux"功能的说明可在[安装指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="b0a6a-197">如何更改显示语言的 WSL？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="b0a6a-198">WSL 安装将尝试自动更改 Ubuntu 区域设置，以便与 Windows 安装程序的区域设置匹配。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="b0a6a-199">如果您不需要此行为可以运行此命令以安装完成后更改 Ubuntu 区域设置。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="b0a6a-200">必须重新启动 bash.exe 此更改才会生效。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="b0a6a-201">下面的示例更改为 EN-US 区域设置：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="b0a6a-202">为什么不具有 internet 访问 WSL</span><span class="sxs-lookup"><span data-stu-id="b0a6a-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="b0a6a-203">某些用户与特定的防火墙应用程序阻止 internet 访问在 WSL 中的报告的问题。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="b0a6a-204">防火墙报告是：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="b0a6a-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="b0a6a-205">Kaspersky</span></span>
1. <span data-ttu-id="b0a6a-206">AVG</span><span class="sxs-lookup"><span data-stu-id="b0a6a-206">AVG</span></span>
1. <span data-ttu-id="b0a6a-207">Avast</span><span class="sxs-lookup"><span data-stu-id="b0a6a-207">Avast</span></span>

<span data-ttu-id="b0a6a-208">在某些情况下关闭防火墙允许访问。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="b0a6a-209">只需时安装防火墙的某些情况下看起来以阻止访问。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="b0a6a-210">如何从 Windows 在 WSL 访问端口？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="b0a6a-211">WSL 共享运行在 Windows 上的 Windows，IP 地址。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="b0a6a-212">这种情况下可以访问本地主机上的任何端口例如有 web 内容上的端口 1234 可以 https://localhost:1234Windows 浏览器中。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="b0a6a-213">其中提供反馈？</span><span class="sxs-lookup"><span data-stu-id="b0a6a-213">Where can I provide feedback?</span></span>

<span data-ttu-id="b0a6a-214">可以分享反馈并通过多个通道提问：反馈和问题应定向到：</span><span class="sxs-lookup"><span data-stu-id="b0a6a-214">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="b0a6a-215">我们[GitHub 问题跟踪程序](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="b0a6a-215">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="b0a6a-216">我们[命令行 UserVoice 门户](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="b0a6a-216">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="b0a6a-217">我们[命令行团队博客](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="b0a6a-217">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="b0a6a-218">通过 Twitter。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-218">Via Twitter.</span></span> <span data-ttu-id="b0a6a-219">请按照[ @richturn_ms ](https://twitter.com/richturn_MS) twitter，若要了解的新闻、 更新，等等。</span><span class="sxs-lookup"><span data-stu-id="b0a6a-219">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
