---
title: 常见问题 (FAQ)
description: 有关适用于 Linux 的 Windows 子系统的常见问题。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、faq
author: taraj
ms.author: taraj
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.openlocfilehash: 2bbcec661146fcb570209fd895e6543657e98996
ms.sourcegitcommit: 939fe561d178454219adbee96c0ad3f768db2208
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2019
ms.locfileid: "67237388"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="933b7-104">有关适用于 Linux 的 Windows 子系统的常见问题</span><span class="sxs-lookup"><span data-stu-id="933b7-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="933b7-105">什么是适用于 Linux 的 Windows 子系统 (WSL)？</span><span class="sxs-lookup"><span data-stu-id="933b7-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="933b7-106">适用于 Linux 的 Windows 子系统 (WSL) 是一项新的 Windows 10 功能, 使你能够直接在 Windows 上运行原生 Linux 命令行工具, 以及传统的 Windows 桌面和新式应用程序。</span><span class="sxs-lookup"><span data-stu-id="933b7-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="933b7-107">有关更多详细信息, 请参阅 "[关于页面](./about.md)，了解更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="933b7-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="933b7-108">谁适合使用 WSL？</span><span class="sxs-lookup"><span data-stu-id="933b7-108">Who is WSL for?</span></span>
<span data-ttu-id="933b7-109">这主要是一种面向开发人员的工具, 尤其是 web 开发人员和使用开源项目的用户。</span><span class="sxs-lookup"><span data-stu-id="933b7-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="933b7-110">这允许需要/需要使用 Bash、通用 Linux 工具 (`sed`、 `awk`等) 的用户和许多 Linux 优先工具 (Ruby、Python 等) 在 Windows 上使用工具链。</span><span class="sxs-lookup"><span data-stu-id="933b7-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="933b7-111">我可以对 WSL 做些什么？</span><span class="sxs-lookup"><span data-stu-id="933b7-111">What can I do with WSL?</span></span>
<span data-ttu-id="933b7-112">WSL 提供了一个名为 Bash 的应用程序, 该应用程序在启动时将打开运行 Bash shell 的 Windows 控制台。</span><span class="sxs-lookup"><span data-stu-id="933b7-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="933b7-113">使用 Bash, 你可以运行命令行 Linux 工具和应用。</span><span class="sxs-lookup"><span data-stu-id="933b7-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="933b7-114">例如, 键入`lsb_release -a`并按 enter, 将看到当前正在运行的 Linux 发行版的详细信息:</span><span class="sxs-lookup"><span data-stu-id="933b7-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![发行版详细信息的屏幕截图](media/distro.png)

<span data-ttu-id="933b7-116">你还可以从 Linux Bash shell 内访问本地计算机的文件系统–你会发现在该`/mnt`文件夹下装入本地驱动器。</span><span class="sxs-lookup"><span data-stu-id="933b7-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="933b7-117">例如, 你`C:`的驱动器安装在下面`/mnt/c`:</span><span class="sxs-lookup"><span data-stu-id="933b7-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![装载的 C 驱动器的屏幕截图](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="933b7-119">什么是 Bash？</span><span class="sxs-lookup"><span data-stu-id="933b7-119">What is Bash?</span></span>
<span data-ttu-id="933b7-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29)是一种流行的基于文本的 shell 和命令语言。</span><span class="sxs-lookup"><span data-stu-id="933b7-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="933b7-121">它是 Ubuntu 和其他 Linux 发行版以及 macOS 中包含的默认 shell。</span><span class="sxs-lookup"><span data-stu-id="933b7-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="933b7-122">用户在 shell 中键入命令以执行脚本和/或运行命令和工具来完成许多任务。</span><span class="sxs-lookup"><span data-stu-id="933b7-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="933b7-123">这是如何实现的？</span><span class="sxs-lookup"><span data-stu-id="933b7-123">How does this work?</span></span>
<span data-ttu-id="933b7-124">请查看我们的[博客](https://blogs.msdn.microsoft.com/wsl/), 了解基础技术的详细信息。</span><span class="sxs-lookup"><span data-stu-id="933b7-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="933b7-125">为什么使用 WSL 而不是虚拟机中的 Linux？</span><span class="sxs-lookup"><span data-stu-id="933b7-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="933b7-126">WSL 所需的资源 (CPU、内存和存储) 比完整虚拟机少。</span><span class="sxs-lookup"><span data-stu-id="933b7-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="933b7-127">WSL 还允许您通过 Windows 命令行、桌面和应用商店应用程序运行 Linux 命令行工具和应用程序, 以及从 Linux 内访问 Windows 文件。</span><span class="sxs-lookup"><span data-stu-id="933b7-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="933b7-128">这使您可以在您需要时对同一组文件使用 Windows 应用和 Linux 命令行工具。</span><span class="sxs-lookup"><span data-stu-id="933b7-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="933b7-129">我为什么要在 Linux 上而不是在 Windows 上使用 Ruby？</span><span class="sxs-lookup"><span data-stu-id="933b7-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="933b7-130">构建一些跨平台工具, 假设它们的运行环境的行为类似于 Linux。</span><span class="sxs-lookup"><span data-stu-id="933b7-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="933b7-131">例如, 某些工具假设它们能够访问非常长的文件路径, 或者存在特定的文件/文件夹。</span><span class="sxs-lookup"><span data-stu-id="933b7-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="933b7-132">这通常会导致 Windows 出现问题, 这些问题通常与 Linux 的行为不同。</span><span class="sxs-lookup"><span data-stu-id="933b7-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="933b7-133">许多语言 (例如 Ruby 和 node) 通常在 Windows 上移植到和运行良好。</span><span class="sxs-lookup"><span data-stu-id="933b7-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="933b7-134">但是, 并不是所有的 Ruby Gem 或 node/NPM 库所有者都将其库移植到支持 Windows, 许多都具有特定于 Linux 的依赖项。</span><span class="sxs-lookup"><span data-stu-id="933b7-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="933b7-135">这通常会导致使用此类工具和库生成的系统不能在 Windows 上生成, 有时运行时错误或不需要的行为。</span><span class="sxs-lookup"><span data-stu-id="933b7-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="933b7-136">这只是导致许多人要求 Microsoft 改进 Windows 命令行工具的一些问题, 并使我们与合作伙伴合作, 使本机 Bash 和 Linux 命令行工具能够在 Windows 上运行。</span><span class="sxs-lookup"><span data-stu-id="933b7-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="933b7-137">对于 PowerShell 而言, 这意味着什么？</span><span class="sxs-lookup"><span data-stu-id="933b7-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="933b7-138">使用 OSS 项目时, 在许多情况下, 从 PowerShell 提示符中删除 Bash 非常有用。</span><span class="sxs-lookup"><span data-stu-id="933b7-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="933b7-139">Bash 支持是互补的, 在 Windows 上增强了命令行的价值, 使 PowerShell 和 PowerShell 社区能够利用其他常用技术。</span><span class="sxs-lookup"><span data-stu-id="933b7-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="933b7-140">有关详细信息, 请参阅 PowerShell 团队博客[--Bash for Windows:为什么它非常出色, 它对 PowerShell 意味着什么](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span><span class="sxs-lookup"><span data-stu-id="933b7-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="933b7-141">能否在 WSL 中运行所有 Linux 应用？</span><span class="sxs-lookup"><span data-stu-id="933b7-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="933b7-142">不！</span><span class="sxs-lookup"><span data-stu-id="933b7-142">No!</span></span> <span data-ttu-id="933b7-143">WSL 是一种工具, 旨在使需要用户在 Windows 上运行 Bash 和核心 Linux 命令行工具的用户。</span><span class="sxs-lookup"><span data-stu-id="933b7-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="933b7-144">WSL 不支持 GUI 桌面或应用程序 (例如, GNOME、KDE 等)</span><span class="sxs-lookup"><span data-stu-id="933b7-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="933b7-145">此外, 即使您能够运行多个常用的服务器应用程序 (例如 Redis), 我们也不建议使用 WSL 来托管生产服务– Microsoft 提供了多种解决方案, 用于在 Azure、Hyper-v 和 Docker 中运行生产 Linux 工作负荷。</span><span class="sxs-lookup"><span data-stu-id="933b7-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="933b7-146">WSL 包含哪些 Windows Sku？</span><span class="sxs-lookup"><span data-stu-id="933b7-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="933b7-147">适用于 windows 10 周年和创意者更新或更高版本的 Windows 的桌面版本中提供了适用于 Linux 的 windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="933b7-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="933b7-148">从秋季创意者更新开始, WSL 将在 Windows 的桌面和服务器 Sku 上可用。</span><span class="sxs-lookup"><span data-stu-id="933b7-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="933b7-149">WSL 支持哪些处理器？</span><span class="sxs-lookup"><span data-stu-id="933b7-149">What processors does WSL support?</span></span>
<span data-ttu-id="933b7-150">WSL 支持 x64 和 ARM CPU。</span><span class="sxs-lookup"><span data-stu-id="933b7-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="933b7-151">如何实现访问我的 C: 驱动器？</span><span class="sxs-lookup"><span data-stu-id="933b7-151">How do I access my C: drive?</span></span>
<span data-ttu-id="933b7-152">将自动创建本地计算机上的硬盘驱动器的装入点, 并提供对 Windows filesystem 的轻松访问。</span><span class="sxs-lookup"><span data-stu-id="933b7-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="933b7-153">**/mnt/\<驱动器号 >/**</span><span class="sxs-lookup"><span data-stu-id="933b7-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="933b7-154">示例用法是`cd /mnt/c`访问 c:</span><span class="sxs-lookup"><span data-stu-id="933b7-154">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="933b7-155">如何实现将 Windows 文件用于 Linux 应用？</span><span class="sxs-lookup"><span data-stu-id="933b7-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="933b7-156">WSL 的一个优点是, 可以通过 Windows 和 Linux 应用或工具访问你的文件。</span><span class="sxs-lookup"><span data-stu-id="933b7-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="933b7-157">WSL 将计算机的固定驱动器装载到 Linux `/mnt/<drive>`发行版中的文件夹下。</span><span class="sxs-lookup"><span data-stu-id="933b7-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="933b7-158">例如, 你`C:`的驱动器安装在`/mnt/c/`</span><span class="sxs-lookup"><span data-stu-id="933b7-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="933b7-159">使用已装载的驱动器, 你可以在中编辑代码 (例如`C:\dev\myproj\` , 使用[Visual Studio](https://visualstudio.microsoft.com/vs/) /或[VS Code](https://code.visualstudio.com/)), 并`/mnt/c/dev/myproj`通过访问相同的文件, 在 Linux 中生成/测试该代码。</span><span class="sxs-lookup"><span data-stu-id="933b7-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="933b7-160">**重要说明**:使用 WSL 的一个重要限制是, 不支持直接访问/更改 Linux 发行版文件系统中的文件。</span><span class="sxs-lookup"><span data-stu-id="933b7-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="933b7-161">请参阅：[不要使用 Windows 应用和工具更改 Linux 文件](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="933b7-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="933b7-162">Linux 驱动器中的文件是否与装载的 Windows 驱动器不同？</span><span class="sxs-lookup"><span data-stu-id="933b7-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="933b7-163">Linux 根下的文件 (即`/`) 由 WSL 控制, 它模拟 Linux 特定的行为, 包括但不限于:</span><span class="sxs-lookup"><span data-stu-id="933b7-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="933b7-164">包含无效 Windows 文件名字符的文件</span><span class="sxs-lookup"><span data-stu-id="933b7-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="933b7-165">为非管理员用户创建的符号链接</span><span class="sxs-lookup"><span data-stu-id="933b7-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="933b7-166">通过 chmod 和 chown 更改文件属性</span><span class="sxs-lookup"><span data-stu-id="933b7-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="933b7-167">文件/文件夹区分大小写</span><span class="sxs-lookup"><span data-stu-id="933b7-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="933b7-168">装入驱动器中的文件由 Windows 控制, 并具有以下行为:</span><span class="sxs-lookup"><span data-stu-id="933b7-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="933b7-169">支持区分大小写</span><span class="sxs-lookup"><span data-stu-id="933b7-169">Support case sensitivity</span></span>
   * <span data-ttu-id="933b7-170">所有权限都设置为 "最佳" 反映 Windows 权限</span><span class="sxs-lookup"><span data-stu-id="933b7-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="933b7-171">为什么在运行 apt 时出现如此多的错误-获取升级？</span><span class="sxs-lookup"><span data-stu-id="933b7-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="933b7-172">某些包使用我们尚未实现的功能。</span><span class="sxs-lookup"><span data-stu-id="933b7-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="933b7-173">`udev`例如, 尚不支持, 并导致几个`apt-get upgrade`错误。</span><span class="sxs-lookup"><span data-stu-id="933b7-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="933b7-174">若要解决与相关`udev`的问题, 请执行以下步骤:</span><span class="sxs-lookup"><span data-stu-id="933b7-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="933b7-175">将以下项写入`/usr/sbin/policy-rc.d`到中, 并保存所做的更改。</span><span class="sxs-lookup"><span data-stu-id="933b7-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="933b7-176">向添加执行权限`/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="933b7-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="933b7-177">运行以下命令</span><span class="sxs-lookup"><span data-stu-id="933b7-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="933b7-178">如何实现卸载 WSL 分发？</span><span class="sxs-lookup"><span data-stu-id="933b7-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="933b7-179">在1709之前的版本 (16299) 上, 打开命令提示符并运行:</span><span class="sxs-lookup"><span data-stu-id="933b7-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="933b7-180">通过右键单击 "应用" 磁贴并单击 "卸载", 或使用[ `Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)通过 PowerShell, 可以像任何其他 Windows 应用一样卸载从应用商店安装的 WSL 分发。</span><span class="sxs-lookup"><span data-stu-id="933b7-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="933b7-181">Ping 为什么会生成权限被拒绝错误？</span><span class="sxs-lookup"><span data-stu-id="933b7-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="933b7-182">在 WSL 生成 < 14926 中, ping 必需的 WSL 通过提升的控制台运行。</span><span class="sxs-lookup"><span data-stu-id="933b7-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="933b7-183">此问题已在版本14926和更高版本中解决。</span><span class="sxs-lookup"><span data-stu-id="933b7-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="933b7-184">如何实现运行 OpenSSH 服务器？</span><span class="sxs-lookup"><span data-stu-id="933b7-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="933b7-185">Windows 中的管理员权限需要在 WSL 中运行 OpenSSH。</span><span class="sxs-lookup"><span data-stu-id="933b7-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="933b7-186">若要运行 OpenSSH 服务器, 请在 Windows 上的 Ubuntu 上以管理员身份运行 Bash, 或从具有管理员权限的 CMD/PowerShell 提示符运行 bash。</span><span class="sxs-lookup"><span data-stu-id="933b7-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="933b7-187">为什么会出现 "错误:0x80040306 "我尝试安装？</span><span class="sxs-lookup"><span data-stu-id="933b7-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="933b7-188">WSL 不支持在旧控制台中运行。</span><span class="sxs-lookup"><span data-stu-id="933b7-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="933b7-189">关闭旧版控制台:</span><span class="sxs-lookup"><span data-stu-id="933b7-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="933b7-190">打开 WSL、PowerShell 或 Cmd</span><span class="sxs-lookup"><span data-stu-id="933b7-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="933b7-191">右键单击标题栏-> 属性-> 取消选中 "使用旧版控制台"</span><span class="sxs-lookup"><span data-stu-id="933b7-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="933b7-192">单击“确定”</span><span class="sxs-lookup"><span data-stu-id="933b7-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="933b7-193">为什么会出现 "错误:升级 Windows 后, 0x80040154 "</span><span class="sxs-lookup"><span data-stu-id="933b7-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="933b7-194">Windows 更新期间可能禁用了 "适用于 Linux 的 Windows 子系统" 功能。</span><span class="sxs-lookup"><span data-stu-id="933b7-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="933b7-195">如果出现这种情况, 则必须重新启用 Windows 功能。</span><span class="sxs-lookup"><span data-stu-id="933b7-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="933b7-196">有关启用 "适用于 Linux 的 Windows 子系统" 功能的说明, 请参阅[安装指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。</span><span class="sxs-lookup"><span data-stu-id="933b7-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-guihttps://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="933b7-197">如何实现更改 WSL 的显示语言？</span><span class="sxs-lookup"><span data-stu-id="933b7-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="933b7-198">WSL 安装将尝试自动更改 Ubuntu 区域设置以与 Windows 安装的区域设置相匹配。</span><span class="sxs-lookup"><span data-stu-id="933b7-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="933b7-199">如果不想要此行为, 可以在安装完成后运行此命令来更改 Ubuntu 区域设置。</span><span class="sxs-lookup"><span data-stu-id="933b7-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="933b7-200">要使此更改生效, 您必须重新启动 bash。</span><span class="sxs-lookup"><span data-stu-id="933b7-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="933b7-201">下面的示例将区域设置更改为 en-us:</span><span class="sxs-lookup"><span data-stu-id="933b7-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="933b7-202">为什么无法从 WSL 访问 internet？</span><span class="sxs-lookup"><span data-stu-id="933b7-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="933b7-203">某些用户已报告在 WSL 中阻止 internet 访问的特定防火墙应用程序的问题。</span><span class="sxs-lookup"><span data-stu-id="933b7-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="933b7-204">报告的防火墙包括:</span><span class="sxs-lookup"><span data-stu-id="933b7-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="933b7-205">Kaspersky 等</span><span class="sxs-lookup"><span data-stu-id="933b7-205">Kaspersky</span></span>
1. <span data-ttu-id="933b7-206">AVG</span><span class="sxs-lookup"><span data-stu-id="933b7-206">AVG</span></span>
1. <span data-ttu-id="933b7-207">Avast</span><span class="sxs-lookup"><span data-stu-id="933b7-207">Avast</span></span>

<span data-ttu-id="933b7-208">在某些情况下, 关闭防火墙允许进行访问。</span><span class="sxs-lookup"><span data-stu-id="933b7-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="933b7-209">在某些情况下, 只需安装防火墙即可阻止访问。</span><span class="sxs-lookup"><span data-stu-id="933b7-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="933b7-210">如何实现从 Windows 中的 WSL 访问端口？</span><span class="sxs-lookup"><span data-stu-id="933b7-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="933b7-211">WSL 共享 Windows 的 IP 地址, 因为它在 Windows 上运行。</span><span class="sxs-lookup"><span data-stu-id="933b7-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="933b7-212">因此, 你可以访问 localhost 上的任何端口 (例如, 如果你的 web 内容位于端口 1234 https://localhost:1234 上, 你可以进入 Windows 浏览器中)。</span><span class="sxs-lookup"><span data-stu-id="933b7-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="933b7-213">如何备份我的 WSL 发行版？</span><span class="sxs-lookup"><span data-stu-id="933b7-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="933b7-214">Windows 版本1809及更高版本中提供了备份发行版的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="933b7-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="933b7-215">你可以使用`wsl --export`命令将整个分发导出到 tarball。</span><span class="sxs-lookup"><span data-stu-id="933b7-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="933b7-216">然后, 可以使用`wsl --import`命令将此发行版导入 WSL, 使你能够备份和保存 WSL 分发的状态。</span><span class="sxs-lookup"><span data-stu-id="933b7-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="933b7-217">请注意, 备份 Appdata 文件夹 (如 Windows 备份) 中的文件的传统备份服务不会损坏 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="933b7-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="933b7-218">在哪里可以提供反馈？</span><span class="sxs-lookup"><span data-stu-id="933b7-218">Where can I provide feedback?</span></span>

<span data-ttu-id="933b7-219">可以通过多个渠道共享反馈和提问:反馈和问题应定向到:</span><span class="sxs-lookup"><span data-stu-id="933b7-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="933b7-220">[GitHub 问题跟踪](https://github.com/Microsoft/BashOnWindows/issues)器</span><span class="sxs-lookup"><span data-stu-id="933b7-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="933b7-221">我们的[命令行 UserVoice 门户](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="933b7-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="933b7-222">我们的[命令行团队博客](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="933b7-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="933b7-223">通过 Twitter。</span><span class="sxs-lookup"><span data-stu-id="933b7-223">Via Twitter.</span></span> <span data-ttu-id="933b7-224">请在 Twitter 上关注[@richturn_ms](https://twitter.com/richturn_MS)以了解新闻，更新等。</span><span class="sxs-lookup"><span data-stu-id="933b7-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
