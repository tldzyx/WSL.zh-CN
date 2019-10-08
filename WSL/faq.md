---
title: 常见问题 (FAQ)
description: 有关适用于 Linux 的 Windows 子系统的常见问题解答。
keywords: BashOnWindows, bash, wsl, windows, windows 子系统, windowssubsystem, faq
ms.date: 9/4/2018
ms.topic: article
ms.assetid: 129101ed-b88a-43c2-b6a2-cd2c4ff6fee1
ms.localizationpriority: high
ms.openlocfilehash: 911bde69540bb8bb7a5ee40d8a9f4d6995f4fdaa
ms.sourcegitcommit: 3f35034581456a2008aa5ed1b623715dfef64608
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "71934905"
---
# <a name="frequently-asked-questions-about-windows-subsystem-for-linux"></a><span data-ttu-id="db191-104">有关适用于 Linux 的 Windows 子系统的常见问题解答</span><span class="sxs-lookup"><span data-stu-id="db191-104">Frequently Asked Questions about Windows Subsystem for Linux</span></span>

## <a name="what-is-windows-subsystem-for-linux-wsl"></a><span data-ttu-id="db191-105">什么是适用于 Linux 的 Windows 子系统 (WSL)？</span><span class="sxs-lookup"><span data-stu-id="db191-105">What is Windows Subsystem for Linux (WSL)?</span></span>
<span data-ttu-id="db191-106">适用于 Linux 的 Windows 子系统 (WSL) 是新增的 Windows 10 功能，使用它可以直接在 Windows 上运行本机 Linux 命令行工具，并可以运行传统的 Windows 桌面和新式 Store 应用。</span><span class="sxs-lookup"><span data-stu-id="db191-106">The Windows Subsystem for Linux (WSL) is a new Windows 10 feature that enables you to run native Linux command-line tools directly on Windows, alongside your traditional Windows desktop and modern store apps.</span></span>

<span data-ttu-id="db191-107">请参阅[“关于”页](./about.md)了解更多详细信息。</span><span class="sxs-lookup"><span data-stu-id="db191-107">See the [about page](./about.md) for more details.</span></span>

## <a name="who-is-wsl-for"></a><span data-ttu-id="db191-108">WSL 面向哪些用户？</span><span class="sxs-lookup"><span data-stu-id="db191-108">Who is WSL for?</span></span>
<span data-ttu-id="db191-109">WSL 是主要面向开发人员的工具 -- 尤其是 Web 开发人员，以及处理和使用开源项目的开发人员。</span><span class="sxs-lookup"><span data-stu-id="db191-109">This is primarily a tool for developers -- especially web developers and those who work on or with open source projects.</span></span> <span data-ttu-id="db191-110">想要/需要使用 Bash、常用 Linux 工具（`sed`、`awk` 等）和许多 Linux 优先工具（Ruby、Python 等）的用户可以通过 WSL 在 Windows 上使用其工具链。</span><span class="sxs-lookup"><span data-stu-id="db191-110">This allows those who want/need to use Bash, common Linux tools (`sed`, `awk`, etc.) and many Linux-first tools (Ruby, Python, etc.) to use their toolchain on Windows.</span></span>

## <a name="what-can-i-do-with-wsl"></a><span data-ttu-id="db191-111">WSL 有哪些作用？</span><span class="sxs-lookup"><span data-stu-id="db191-111">What can I do with WSL?</span></span>
<span data-ttu-id="db191-112">WSL 提供一个名为 Bash.exe 的应用程序，启动该应用程序后，会打开一个运行 Bash shell 的 Windows 控制台。</span><span class="sxs-lookup"><span data-stu-id="db191-112">WSL provides an application called Bash.exe that, when started, opens a Windows console running the Bash shell.</span></span> <span data-ttu-id="db191-113">使用 Bash 可以运行命令行 Linux 工具和应用。</span><span class="sxs-lookup"><span data-stu-id="db191-113">Using Bash, you can run command-line Linux tools and apps.</span></span> <span data-ttu-id="db191-114">例如，键入 `lsb_release -a` 并按 Enter 后，将会看到当前正在运行的 Linux 分发版的详细信息：</span><span class="sxs-lookup"><span data-stu-id="db191-114">For example, type `lsb_release -a` and hit enter; you’ll see details of the Linux distro currently running:</span></span>

![分发版详细信息的屏幕截图](media/distro.png)

<span data-ttu-id="db191-116">还可以从 Linux Bash shell 内部访问本地计算机的文件系统 – 将会看到 `/mnt` 文件夹下装载的本地驱动器。</span><span class="sxs-lookup"><span data-stu-id="db191-116">You can also access your local machine’s filesystem from within the Linux Bash shell – you’ll find your local drives mounted under the `/mnt` folder.</span></span> <span data-ttu-id="db191-117">例如，你的 `C:` 驱动器装载在 `/mnt/c` 下：</span><span class="sxs-lookup"><span data-stu-id="db191-117">For example, your `C:` drive is mounted under `/mnt/c`:</span></span>  

![装载的 C 驱动器的屏幕截图](media/ls.png)

## <a name="what-is-bash"></a><span data-ttu-id="db191-119">什么是 Bash？</span><span class="sxs-lookup"><span data-stu-id="db191-119">What is Bash?</span></span>
<span data-ttu-id="db191-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 是一个流行的基于文本的 shell，并且是一种命令语言。</span><span class="sxs-lookup"><span data-stu-id="db191-120">[Bash](https://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) is a popular text-based shell and command-language.</span></span> <span data-ttu-id="db191-121">它是包含在 Ubuntu、其他 Linux 分发版和 macOS 中的默认 shell。</span><span class="sxs-lookup"><span data-stu-id="db191-121">It is the default shell included within Ubuntu and other Linux distros, and in macOS.</span></span> <span data-ttu-id="db191-122">用户在 shell 中键入命令，即可执行脚本和/或运行命令与工具来完成许多任务。</span><span class="sxs-lookup"><span data-stu-id="db191-122">Users type commands into a shell to execute scripts and/or run commands and tools to accomplish many tasks.</span></span>

## <a name="how-does-this-work"></a><span data-ttu-id="db191-123">WSL 的工作原理是怎样的？</span><span class="sxs-lookup"><span data-stu-id="db191-123">How does this work?</span></span>
<span data-ttu-id="db191-124">请查看我们的[博客](https://blogs.msdn.microsoft.com/wsl/)，其中详细介绍了底层技术。</span><span class="sxs-lookup"><span data-stu-id="db191-124">Check out our [blog](https://blogs.msdn.microsoft.com/wsl/) where we go into detail about the underlying technology.</span></span>

## <a name="why-would-i-use-wsl-rather-than-linux-in-a-vm"></a><span data-ttu-id="db191-125">在 VM 中为何要使用 WSL 而不是 Linux？</span><span class="sxs-lookup"><span data-stu-id="db191-125">Why would I use WSL rather than Linux in a VM?</span></span>
<span data-ttu-id="db191-126">WSL 所需的资源（CPU、内存和存储）少于完整虚拟机所需的资源。</span><span class="sxs-lookup"><span data-stu-id="db191-126">WSL requires fewer resources (CPU, memory, and storage) than a full virtual machine.</span></span> <span data-ttu-id="db191-127">WSL 还允许结合 Windows 命令行、桌面和 Store 应用运行 Linux 命令行工具与应用，并允许从 Linux 内部访问 Windows 文件。</span><span class="sxs-lookup"><span data-stu-id="db191-127">WSL also allows you to run Linux command-line tools and apps alongside your Windows command-line, desktop and store apps, and to access your Windows files from within Linux.</span></span> <span data-ttu-id="db191-128">这样，你便可以根据需要针对相同的文件集使用 Windows 应用和 Linux 命令行工具。</span><span class="sxs-lookup"><span data-stu-id="db191-128">This enables you to use Windows apps and Linux command-line tools on the same set of files if you wish.</span></span>

## <a name="why-would-i-use-for-example-ruby-on-linux-instead-of-on-windows"></a><span data-ttu-id="db191-129">举例而言，我为何要在 Linux（而不是 Windows）上使用 Ruby？</span><span class="sxs-lookup"><span data-stu-id="db191-129">Why would I use, for example, Ruby on Linux instead of on Windows?</span></span>
<span data-ttu-id="db191-130">生成某些跨平台工具时，已假设其运行环境的行为类似于 Linux。</span><span class="sxs-lookup"><span data-stu-id="db191-130">Some cross-platform tools were built assuming that the environment in which they run behaves like Linux.</span></span> <span data-ttu-id="db191-131">例如，某些工具假设它们能够访问很长的文件路径，或者特定的文件/文件夹存在。</span><span class="sxs-lookup"><span data-stu-id="db191-131">For example, some tools assume that they are able to access very long file paths or that specific files/folders exist.</span></span> <span data-ttu-id="db191-132">这通常会在 Windows 上导致出现问题，因为 Windows 的行为通常与 Linux 不同。</span><span class="sxs-lookup"><span data-stu-id="db191-132">This often causes problems on Windows which often behaves differently from Linux.</span></span>

<span data-ttu-id="db191-133">许多语言（例如 Ruby 和 Node）通常已移植到 Windows，并且可以在 Windows 上非常顺利地运行。</span><span class="sxs-lookup"><span data-stu-id="db191-133">Many languages like Ruby and node are often ported to, and run great, on Windows.</span></span> <span data-ttu-id="db191-134">但是，并非所有 Ruby Gem 或 Node/NPM 库所有者都会移植其库来支持 Windows，而许多库都与 Linux 之间存在特定的依赖关系。</span><span class="sxs-lookup"><span data-stu-id="db191-134">However, not all of the Ruby Gem or node/NPM library owners port their libraries to support Windows, and many have Linux-specific dependencies.</span></span> <span data-ttu-id="db191-135">这经常导致使用此类工具和库生成的系统在 Windows 上遭遇到生成错误（有时是运行时错误），或者出现不需要的行为。</span><span class="sxs-lookup"><span data-stu-id="db191-135">This can often result in systems built using such tools and libraries suffering from build and sometimes runtime errors or unwanted behaviors on Windows.</span></span>

<span data-ttu-id="db191-136">这只是导致许多人要求 Microsoft 改进 Windows 命令行工具的一部分问题，也正是这些问题促使我们与 Canonical 展开合作，使得本机 Bash 和 Linux 命令行工具能够在 Windows 上运行。</span><span class="sxs-lookup"><span data-stu-id="db191-136">These are just some of issues that caused many people to ask Microsoft to improve Windows’ command-line tools and what drove us to partner with Canonical to enable native Bash and Linux command-line tools to run on Windows.</span></span>

## <a name="what-does-this-mean-for-powershell"></a><span data-ttu-id="db191-137">这对于 PowerShell 而言意味着什么？</span><span class="sxs-lookup"><span data-stu-id="db191-137">What does this mean for PowerShell?</span></span>
<span data-ttu-id="db191-138">处理 OSS 项目时，在很多情况下，从 PowerShell 提示符切换到 Bash 极其有用。</span><span class="sxs-lookup"><span data-stu-id="db191-138">While working with OSS projects, there are numerous scenarios where it’s immensely useful to drop into Bash from a PowerShell prompt.</span></span> <span data-ttu-id="db191-139">Bash 支持是互补性的，可以增强 Windows 上的命令行的价值，使 PowerShell 和 PowerShell 社区能够利用其他流行技术。</span><span class="sxs-lookup"><span data-stu-id="db191-139">Bash support is complementary and strengthens the value of the command-line on Windows, allowing PowerShell and the PowerShell community to leverage other popular technologies.</span></span>

<span data-ttu-id="db191-140">请参阅 PowerShell 团队博客了解详细信息 -- [Bash for Windows：Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)（为何它如此出色，它对 PowerShell 而言意味着什么）</span><span class="sxs-lookup"><span data-stu-id="db191-140">Read more on the PowerShell team blog -- [Bash for Windows: Why it’s awesome and what it means for PowerShell](https://blogs.msdn.microsoft.com/powershell/2016/04/01/bash-for-windows-why-its-awesome-and-what-it-means-for-powershell/)</span></span>

## <a name="can-i-run-all-linux-apps-in-wsl"></a><span data-ttu-id="db191-141">在 WSL 中是否可以运行所有 Linux 应用？</span><span class="sxs-lookup"><span data-stu-id="db191-141">Can I run ALL Linux apps in WSL?</span></span>
<span data-ttu-id="db191-142">不是！</span><span class="sxs-lookup"><span data-stu-id="db191-142">No!</span></span> <span data-ttu-id="db191-143">WSL 工具的目的是使用户能够视需要在 Windows 上运行 Bash 和核心 Linux 命令行工具。</span><span class="sxs-lookup"><span data-stu-id="db191-143">WSL is a tool aimed at enabling users who need them to run Bash and core Linux command-line tools on Windows.</span></span> 

<span data-ttu-id="db191-144">WSL 并**不**旨在支持 GUI 桌面或应用程序（例如 Gnome、KDE 等）。</span><span class="sxs-lookup"><span data-stu-id="db191-144">WSL does **not** aim to support GUI desktops or applications (e.g. Gnome, KDE, etc.)</span></span>  

<span data-ttu-id="db191-145">此外，尽管你可以运行许多流行的服务器应用程序（例如 Redis），但我们不建议使用 WSL 来托管生产服务 – Microsoft 提供多种解决方案用于在 Azure、Hyper-V 和 Docker 中运行生产 Linux 工作负荷。</span><span class="sxs-lookup"><span data-stu-id="db191-145">Also, even though you will be able to run many popular server applications (e.g. Redis), we do not recommend WSL for hosting production services – Microsoft offers a variety of solutions for running production Linux workloads in Azure, Hyper-V, and Docker.</span></span> 

## <a name="what-windows-skus-is-wsl-included-in"></a><span data-ttu-id="db191-146">WSL 包含在哪些 Windows SKU 中？</span><span class="sxs-lookup"><span data-stu-id="db191-146">What Windows SKUs is WSL included in?</span></span>
<span data-ttu-id="db191-147">适用于 Windows 10 周年更新和创意者更新或更高版本的 Windows 桌面版中提供了适用于 Linux 的 Windows 子系统。</span><span class="sxs-lookup"><span data-stu-id="db191-147">Windows Subsystem for Linux is available on the desktop version of Windows for Windows 10 Anniversary and Creators update or later.</span></span>

<span data-ttu-id="db191-148">从 Fall Creators Update 开始，WSL 将在 Windows 桌面版和服务器版 SKU 中提供。</span><span class="sxs-lookup"><span data-stu-id="db191-148">Beginning in the Fall Creators update WSL will be available on both the desktop and server SKUs of Windows.</span></span>

## <a name="what-processors-does-wsl-support"></a><span data-ttu-id="db191-149">WSL 支持哪些处理器？</span><span class="sxs-lookup"><span data-stu-id="db191-149">What processors does WSL support?</span></span>
<span data-ttu-id="db191-150">WSL 支持 x64 和 ARM CPU。</span><span class="sxs-lookup"><span data-stu-id="db191-150">WSL supports x64 and ARM CPUs.</span></span>

## <a name="how-do-i-access-my-c-drive"></a><span data-ttu-id="db191-151">如何访问我的 C: 驱动器？</span><span class="sxs-lookup"><span data-stu-id="db191-151">How do I access my C: drive?</span></span>
<span data-ttu-id="db191-152">系统会自动为本地计算机上的硬盘驱动器创建装入点，通过这些装入点可以轻松访问 Windows 文件系统。</span><span class="sxs-lookup"><span data-stu-id="db191-152">Mount points for hard drives on the local machine are automatically created and provide easy access to the Windows filesystem.</span></span> 
 
<span data-ttu-id="db191-153">**/mnt/\<驱动器号>/**</span><span class="sxs-lookup"><span data-stu-id="db191-153">**/mnt/\<drive letter>/**</span></span>
 
<span data-ttu-id="db191-154">示例用法：运行 `cd /mnt/c` 访问 c:</span><span class="sxs-lookup"><span data-stu-id="db191-154">Example usage would be `cd /mnt/c` to access c:</span></span>\

## <a name="how-do-i-use-a-windows-file-with-a-linux-app"></a><span data-ttu-id="db191-155">如何在 Linux 应用中使用 Windows 文件？</span><span class="sxs-lookup"><span data-stu-id="db191-155">How do I use a Windows file with a Linux app?</span></span>

<span data-ttu-id="db191-156">WSL 的优势之一是可以通过 Windows 和 Linux 应用或工具访问文件。</span><span class="sxs-lookup"><span data-stu-id="db191-156">One of the benefits of WSL is being able to access your files via both Windows and Linux apps or tools.</span></span> 

<span data-ttu-id="db191-157">WSL 将计算机的固定驱动器装载到 Linux 分发版中的 `/mnt/<drive>` 文件夹下。</span><span class="sxs-lookup"><span data-stu-id="db191-157">WSL mounts your machine's fixed drives under the `/mnt/<drive>` folder in your Linux distros.</span></span> <span data-ttu-id="db191-158">例如，你的 `C:` 驱动器装载在 `/mnt/c/` 下</span><span class="sxs-lookup"><span data-stu-id="db191-158">For example, your `C:` drive is mounted under `/mnt/c/`</span></span> 

<span data-ttu-id="db191-159">例如，使用装载的驱动器，可以使用 [Visual Studio](https://visualstudio.microsoft.com/vs/) 或 [VS Code](https://code.visualstudio.com/) 编辑 `C:\dev\myproj\` 中的代码，并通过 `/mnt/c/dev/myproj` 访问相同的文件，在 Linux 中生成/测试该代码。</span><span class="sxs-lookup"><span data-stu-id="db191-159">Using your mounted drives, you can edit code in, for example, `C:\dev\myproj\` using [Visual Studio](https://visualstudio.microsoft.com/vs/) / or [VS Code](https://code.visualstudio.com/), and build/test that code in Linux by accessing the same files via `/mnt/c/dev/myproj`.</span></span>

> <span data-ttu-id="db191-160">**重要说明**：使用 WSL 的一个重要限制是，不支持使用 Windows 应用或工具直接访问/更改 Linux 分发版文件系统中的文件。</span><span class="sxs-lookup"><span data-stu-id="db191-160">**IMPORTANT NOTE**: One of the key limitations of using WSL is that directly accessing/changing files in your Linux distros' filesystem using Windows apps or tools is not supported.</span></span> <span data-ttu-id="db191-161">请参阅：[不要使用 Windows 应用和工具更改 Linux 文件](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span><span class="sxs-lookup"><span data-stu-id="db191-161">See: [Do not change Linux files using Windows apps and tools](https://blogs.msdn.microsoft.com/commandline/2016/11/17/do-not-change-linux-files-using-windows-apps-and-tools/)</span></span>

## <a name="are-files-in-the-linux-drive-different-from-the-mounted-windows-drive"></a><span data-ttu-id="db191-162">Linux 驱动器中的文件是否不同于装载的 Windows 驱动器中的文件？</span><span class="sxs-lookup"><span data-stu-id="db191-162">Are files in the Linux drive different from the mounted Windows drive?</span></span>

1. <span data-ttu-id="db191-163">Linux 根目录（即 `/`）下的文件由模拟 Linux 特定行为的 WSL 控制，控制的内容和操作包括但不限于：</span><span class="sxs-lookup"><span data-stu-id="db191-163">Files under the Linux root (i.e. `/`) are controlled by WSL which mimics Linux specific behavior, including but not limited to:</span></span>
   * <span data-ttu-id="db191-164">包含无效 Windows 文件名字符的文件</span><span class="sxs-lookup"><span data-stu-id="db191-164">Files which contain invalid Windows filename characters</span></span>
   * <span data-ttu-id="db191-165">为非管理员用户创建的符号链接</span><span class="sxs-lookup"><span data-stu-id="db191-165">Symlinks created for non-admin users</span></span>
   * <span data-ttu-id="db191-166">通过 chmod 和 chown 更改文件属性</span><span class="sxs-lookup"><span data-stu-id="db191-166">Changing file attributes through chmod and chown</span></span>
   * <span data-ttu-id="db191-167">文件/文件夹的区分大小写状态</span><span class="sxs-lookup"><span data-stu-id="db191-167">File/folder case sensitivity</span></span>

2. <span data-ttu-id="db191-168">装载的驱动器中的文件由 Windows 控制，并具有以下行为：</span><span class="sxs-lookup"><span data-stu-id="db191-168">Files in mounted drives are controlled by Windows and have the following behaviors:</span></span>
   * <span data-ttu-id="db191-169">支持区分大小写</span><span class="sxs-lookup"><span data-stu-id="db191-169">Support case sensitivity</span></span>
   * <span data-ttu-id="db191-170">设置的所有权限可以最好地反映 Windows 权限</span><span class="sxs-lookup"><span data-stu-id="db191-170">All permissions are set to best reflect the Windows permissions</span></span>

## <a name="why-are-there-so-many-errors-when-i-run-apt-get-upgrade"></a><span data-ttu-id="db191-171">运行 apt-get upgrade 时为何会出现大量的错误？</span><span class="sxs-lookup"><span data-stu-id="db191-171">Why are there so many errors when I run apt-get upgrade?</span></span>
<span data-ttu-id="db191-172">某些包使用我们尚未实现的功能。</span><span class="sxs-lookup"><span data-stu-id="db191-172">Some packages use features that we haven't implemented yet.</span></span> <span data-ttu-id="db191-173">例如，`udev` 尚不受支持，会导致多个 `apt-get upgrade` 错误。</span><span class="sxs-lookup"><span data-stu-id="db191-173">`udev`, for example, isn't supported yet and causes several `apt-get upgrade` errors.</span></span>

<span data-ttu-id="db191-174">若要解决与 `udev` 相关的问题，请执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="db191-174">To fix issues related to `udev`, follow the following steps:</span></span>

1. <span data-ttu-id="db191-175">将以下内容写入 `/usr/sbin/policy-rc.d` 并保存更改。</span><span class="sxs-lookup"><span data-stu-id="db191-175">Write the following to `/usr/sbin/policy-rc.d` and save your changes.</span></span>

    ```bash
    #!/bin/sh
    exit 101
    ```

2. <span data-ttu-id="db191-176">将执行权限添加到 `/usr/sbin/policy-rc.d`</span><span class="sxs-lookup"><span data-stu-id="db191-176">Add execute permissions to `/usr/sbin/policy-rc.d`</span></span>

    ```bash
    chmod +x /usr/sbin/policy-rc.d
    ```
  
2. <span data-ttu-id="db191-177">运行以下命令</span><span class="sxs-lookup"><span data-stu-id="db191-177">Run the following commands</span></span>

    ```bash
    dpkg-divert --local --rename --add /sbin/initctl
    ln -s /bin/true /sbin/initctl
    ```

## <a name="how-do-i-uninstall-a-wsl-distribution"></a><span data-ttu-id="db191-178">如何卸载 WSL 分发版？</span><span class="sxs-lookup"><span data-stu-id="db191-178">How do I uninstall a WSL Distribution?</span></span>

<span data-ttu-id="db191-179">在 1709 (16299) 以前的内部版本中，打开命令提示符并运行：</span><span class="sxs-lookup"><span data-stu-id="db191-179">On builds prior to 1709 (16299) open a command prompt and run:</span></span>
  ```batchfile
  lxrun /uninstall /full
  ```
  
<span data-ttu-id="db191-180">可以像卸载任何其他 Windows 应用一样来卸载从 Store 安装的 WSL 分发版：右键单击应用磁贴并单击“卸载”，或者通过 PowerShell 使用 [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx)。</span><span class="sxs-lookup"><span data-stu-id="db191-180">WSL distributions installed from the store can be uninstalled like any other Windows app, by right-clicking on the app tile and clicking Uninstall, or via PowerShell using the [`Remove-AppxPackage` cmdlet](https://technet.microsoft.com/en-us/library/hh856038.aspx).</span></span>

## <a name="why-does-ping-generate-permission-denied-errors"></a><span data-ttu-id="db191-181">ping 命令为何生成权限被拒绝错误？</span><span class="sxs-lookup"><span data-stu-id="db191-181">Why does ping generate permission denied errors?</span></span>
<span data-ttu-id="db191-182">在低于 14926 的 WSL 内部版本中，ping 要求通过权限提升的控制台运行 WSL。</span><span class="sxs-lookup"><span data-stu-id="db191-182">In WSL builds < 14926, ping required WSL to run via an elevated Console.</span></span> <span data-ttu-id="db191-183">此问题已在内部版本 14926 和更高版本中得到解决。</span><span class="sxs-lookup"><span data-stu-id="db191-183">This issue was fixed in Build 14926 and later.</span></span>

## <a name="how-do-i-run-an-openssh-server"></a><span data-ttu-id="db191-184">如何运行 OpenSSH 服务器？</span><span class="sxs-lookup"><span data-stu-id="db191-184">How do I run an OpenSSH server?</span></span>
<span data-ttu-id="db191-185">在 WSL 中运行 OpenSSH 需要拥有 Windows 中的管理员特权。</span><span class="sxs-lookup"><span data-stu-id="db191-185">Administrator privileges in Windows are required to run OpenSSH in WSL.</span></span> <span data-ttu-id="db191-186">若要运行 OpenSSH 服务器，请以管理员身份运行 Windows 上的 Ubuntu Bash，或使用管理员特权从 CMD/PowerShell 提示符运行 bash.exe。</span><span class="sxs-lookup"><span data-stu-id="db191-186">To run an OpenSSH server, run Bash on Ubuntu on Windows as an administrator, or run bash.exe from a CMD/PowerShell prompt with administrator privileges.</span></span>

## <a name="why-do-i-get-error-0x80040306-when-i-try-to-install"></a><span data-ttu-id="db191-187">尝试安装时，为何会出现“错误:0x80040306”？</span><span class="sxs-lookup"><span data-stu-id="db191-187">Why do I get "Error: 0x80040306" when I try to install?</span></span>
<span data-ttu-id="db191-188">WSL 不支持在旧版控制台中运行。</span><span class="sxs-lookup"><span data-stu-id="db191-188">WSL does not support running in a legacy console.</span></span> <span data-ttu-id="db191-189">若要关闭旧版控制台：</span><span class="sxs-lookup"><span data-stu-id="db191-189">To turn off legacy console:</span></span>

1. <span data-ttu-id="db191-190">打开 WSL、PowerShell 或 Cmd</span><span class="sxs-lookup"><span data-stu-id="db191-190">Open WSL, PowerShell, or Cmd</span></span>
1. <span data-ttu-id="db191-191">右键单击标题栏 -> 选择“属性”-> 取消选中“使用旧版控制台”</span><span class="sxs-lookup"><span data-stu-id="db191-191">Right click title bar -> Properties -> Uncheck "Use legacy console"</span></span>
1. <span data-ttu-id="db191-192">单击“确定”</span><span class="sxs-lookup"><span data-stu-id="db191-192">Click OK</span></span>

## <a name="why-do-i-get-error-0x80040154-when-i-run-bashexe-after-upgrading-windows"></a><span data-ttu-id="db191-193">在升级 Windows 后运行 bash.exe 时，为何会出现“错误:0x80040154”？</span><span class="sxs-lookup"><span data-stu-id="db191-193">Why do I get "Error: 0x80040154" when I run bash.exe after upgrading Windows?</span></span>
<span data-ttu-id="db191-194">在 Windows 更新期间可能禁用了“适用于 Linux 的 Windows 子系统”功能。</span><span class="sxs-lookup"><span data-stu-id="db191-194">The "Windows Subsystem for Linux" feature may be disabled during a Windows update.</span></span> <span data-ttu-id="db191-195">如果出现这种情况，则必须重新启用 Windows 功能。</span><span class="sxs-lookup"><span data-stu-id="db191-195">If this happens the Windows feature must be re-enabled.</span></span> <span data-ttu-id="db191-196">在[安装指南](https://docs.microsoft.com/en-us/windows/wsl/install-win10#install-the-windows-subsystem-for-linux)中可以找到有关启用“适用于 Linux 的 Windows 子系统”功能的说明。</span><span class="sxs-lookup"><span data-stu-id="db191-196">Instructions for enabling the "Windows Subsystem for Linux" feature can be found in the [Installation Guide](https://docs.microsoft.com/en-us/windows/wsl/install-win10#install-the-windows-subsystem-for-linux).</span></span>

## <a name="how-do-i-change-the-display-language-of-wsl"></a><span data-ttu-id="db191-197">如何更改 WSL 的显示语言？</span><span class="sxs-lookup"><span data-stu-id="db191-197">How do I change the display language of WSL?</span></span>
<span data-ttu-id="db191-198">WSL 安装会尝试自动更改 Ubuntu 区域设置，使之与 Windows 安装的区域设置相匹配。</span><span class="sxs-lookup"><span data-stu-id="db191-198">WSL install will try to automatically change the Ubuntu locale to match the locale of your Windows install.</span></span> <span data-ttu-id="db191-199">如果你不希望出现此行为，可以在安装完成后，运行此命令来更改 Ubuntu 区域设置。</span><span class="sxs-lookup"><span data-stu-id="db191-199">If you do not want this behavior you can run this command to change the Ubuntu locale after install completes.</span></span> <span data-ttu-id="db191-200">必须重新启动 bash.exe 才能使此项更改生效。</span><span class="sxs-lookup"><span data-stu-id="db191-200">You will have to relaunch bash.exe for this change to take effect.</span></span>

<span data-ttu-id="db191-201">以下示例将区域设置更改为 en-US：</span><span class="sxs-lookup"><span data-stu-id="db191-201">The below example changes to locale to en-US:</span></span>
```bash
sudo update-locale LANG=en_US.UTF8
```

## <a name="why-do-i-not-have-internet-access-from-wsl"></a><span data-ttu-id="db191-202">为何无法从 WSL 进行 Internet 访问？</span><span class="sxs-lookup"><span data-stu-id="db191-202">Why do I not have internet access from WSL?</span></span>
<span data-ttu-id="db191-203">某些用户已报告特定的防火墙应用程序会阻止 WSL 中的 Internet 访问的问题。</span><span class="sxs-lookup"><span data-stu-id="db191-203">Some users have reported issues with specific firewall applications blocking internet access in WSL.</span></span> <span data-ttu-id="db191-204">报告的防火墙包括：</span><span class="sxs-lookup"><span data-stu-id="db191-204">The firewalls reported are:</span></span>

1. <span data-ttu-id="db191-205">Kaspersky</span><span class="sxs-lookup"><span data-stu-id="db191-205">Kaspersky</span></span>
1. <span data-ttu-id="db191-206">AVG</span><span class="sxs-lookup"><span data-stu-id="db191-206">AVG</span></span>
1. <span data-ttu-id="db191-207">Avast</span><span class="sxs-lookup"><span data-stu-id="db191-207">Avast</span></span>

<span data-ttu-id="db191-208">在某些情况下，关闭防火墙即可进行访问。</span><span class="sxs-lookup"><span data-stu-id="db191-208">In some cases turning off the firewall allows for access.</span></span> <span data-ttu-id="db191-209">在某些情况下，只需让安装的防火墙在表面上阻止访问。</span><span class="sxs-lookup"><span data-stu-id="db191-209">In some cases simply having the firewall installed looks to block access.</span></span>

## <a name="how-do-i-access-a-port-from-wsl-in-windows"></a><span data-ttu-id="db191-210">如何从 Windows 中的 WSL 访问某个端口？</span><span class="sxs-lookup"><span data-stu-id="db191-210">How do I access a port from WSL in Windows?</span></span>
<span data-ttu-id="db191-211">WSL 共享 Windows 的 IP 地址，因为它在 Windows 上运行。</span><span class="sxs-lookup"><span data-stu-id="db191-211">WSL shares the IP address of Windows, as it is running on Windows.</span></span> <span data-ttu-id="db191-212">因此，你可以访问 localhost 上的任何端口。例如，如果你在端口 1234 上提供 Web 内容，可以在 Windows 浏览器中输入 https://localhost:1234 。</span><span class="sxs-lookup"><span data-stu-id="db191-212">As such you can access any ports on localhost e.g. if you had web content on port 1234 you could https://localhost:1234 into your Windows browser.</span></span>

## <a name="how-can-i-back-up-my-wsl-distros"></a><span data-ttu-id="db191-213">如何备份 WSL 分发版？</span><span class="sxs-lookup"><span data-stu-id="db191-213">How can I back up my WSL distros?</span></span>

<span data-ttu-id="db191-214">Windows 版本 1809 和更高版本中提供了备份分发版的最佳方式。</span><span class="sxs-lookup"><span data-stu-id="db191-214">The best way to backup your distros is available in Windows Version 1809 and later.</span></span> <span data-ttu-id="db191-215">可以使用 `wsl --export` 命令将整个分发版导出到 tarball。</span><span class="sxs-lookup"><span data-stu-id="db191-215">You can export your entire distribution to a tarball using the `wsl --export` command.</span></span> <span data-ttu-id="db191-216">然后，可以使用 `wsl --import` 命令将此分发版导入回到 WSL，从而可以备份和保存 WSL 分发版的状态。</span><span class="sxs-lookup"><span data-stu-id="db191-216">You can then import this distro back into WSL using the `wsl --import` command, allowing you to backup and save states of your WSL distributions.</span></span> 

<span data-ttu-id="db191-217">请注意，用于备份 Appdata 文件夹中的文件的传统备份服务（例如 Windows 备份）不会损坏 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="db191-217">Please note that traditional backup services that backup files in your Appdata folders (like Windows Backup) will not corrupt your Linux files.</span></span> 



## <a name="where-can-i-provide-feedback"></a><span data-ttu-id="db191-218">可以在何处提供反馈？</span><span class="sxs-lookup"><span data-stu-id="db191-218">Where can I provide feedback?</span></span>

<span data-ttu-id="db191-219">可以通过多个渠道分享反馈和提问：反馈和问题将定向到：</span><span class="sxs-lookup"><span data-stu-id="db191-219">You can share feedback and ask questions through multiple channels: Feedback and questions should be directed to:</span></span>
* <span data-ttu-id="db191-220">我们的 [GitHub 问题跟踪器](https://github.com/Microsoft/BashOnWindows/issues)</span><span class="sxs-lookup"><span data-stu-id="db191-220">Our [GitHub issue tracker](https://github.com/Microsoft/BashOnWindows/issues)</span></span>
* <span data-ttu-id="db191-221">我们的[命令行 UserVoice 门户](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span><span class="sxs-lookup"><span data-stu-id="db191-221">Our [command-line UserVoice portal](https://wpdev.uservoice.com/forums/266908-command-prompt/filters/top)</span></span>
* <span data-ttu-id="db191-222">我们的[命令行团队博客](https://blogs.msdn.microsoft.com/commandline/)</span><span class="sxs-lookup"><span data-stu-id="db191-222">Our [command-line team blog](https://blogs.msdn.microsoft.com/commandline/)</span></span>
* <span data-ttu-id="db191-223">通过 Twitter。</span><span class="sxs-lookup"><span data-stu-id="db191-223">Via Twitter.</span></span> <span data-ttu-id="db191-224">请关注 Twitter 上的 [@richturn_ms](https://twitter.com/richturn_MS) 来了解最新信息、更新等。</span><span class="sxs-lookup"><span data-stu-id="db191-224">Please follow [@richturn_ms](https://twitter.com/richturn_MS) on Twitter to learn of news, updates, etc.</span></span>
