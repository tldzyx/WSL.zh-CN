---
title: 管理 Linux 分发版
description: 引用列出和配置在 Windows 子系统上运行适用于 Linux 的多个 Linux 分发版。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 wsl.conf、 wslconfig 适用于 windows 子系统
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.openlocfilehash: c806552750f413fcb75f989d868a57cc939af64a
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063495"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="7b521-104">管理和配置适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="7b521-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="7b521-105">适用于 Windows 10 Fall Creators Update 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="7b521-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="7b521-106">请参阅我们已更新[安装指南](./install_guide.md)尝试新的管理功能并开始从 Windows 应用商店中运行多个 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Windows Store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="7b521-107">运行 WSL 方法</span><span class="sxs-lookup"><span data-stu-id="7b521-107">Ways to run WSL</span></span>

<span data-ttu-id="7b521-108">有许多方法来运行 Linux 的 Windows 子系统 for Linux。</span><span class="sxs-lookup"><span data-stu-id="7b521-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="7b521-109">`[distro]` ie `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="7b521-109">`[distro]` ie `ubuntu`</span></span>
1. <span data-ttu-id="7b521-110">`wsl.exe` 或 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="7b521-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="7b521-111">`wsl [command]` 或 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="7b521-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="7b521-112">应使用哪种方法取决于你正在执行的操作。</span><span class="sxs-lookup"><span data-stu-id="7b521-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="7b521-113">启动分发 WSL</span><span class="sxs-lookup"><span data-stu-id="7b521-113">Launch WSL by distribution</span></span>

<span data-ttu-id="7b521-114">运行分发使用它的特定于发行版的应用程序将启动其自己的控制台窗口中的分发。</span><span class="sxs-lookup"><span data-stu-id="7b521-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![从开始菜单启动 WSL](media/start-launch.png)

<span data-ttu-id="7b521-116">它等同于在 Windows 应用商店中单击"启动"。</span><span class="sxs-lookup"><span data-stu-id="7b521-116">It is the same as clicking "Launch" in the Windows Store.</span></span>

![启动从 Windows 应用商店的 WSL](media/store-launch.png)

<span data-ttu-id="7b521-118">您还可以运行分布从命令行运行`[distribution].exe`。</span><span class="sxs-lookup"><span data-stu-id="7b521-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="7b521-119">从这种方式中的命令行运行分发的缺点是，它将自动更改你的工作目录当前目录中为分发的主目录。</span><span class="sxs-lookup"><span data-stu-id="7b521-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="7b521-120">**示例：**</span><span class="sxs-lookup"><span data-stu-id="7b521-120">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> ubuntu

scooley@scooley-elmer:~$ pwd
/home/scooley
scooley@scooley-elmer:~$ exit
logout

PS C:\Users\sarah>
```

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="7b521-121">wsl 和 wsl [command]</span><span class="sxs-lookup"><span data-stu-id="7b521-121">wsl and wsl [command]</span></span>

<span data-ttu-id="7b521-122">若要从命令行运行 WSL 的最佳方法使用`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="7b521-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="7b521-123">**示例：**</span><span class="sxs-lookup"><span data-stu-id="7b521-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="7b521-124">不只是`wsl`就地保留当前工作目录，它允许您运行单个命令沿端 Windows 命令。</span><span class="sxs-lookup"><span data-stu-id="7b521-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="7b521-125">**示例：**</span><span class="sxs-lookup"><span data-stu-id="7b521-125">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-Date

Sunday, March 11, 2018 7:54:05 PM

PS C:\Users\sarah> wsl
scooley@scooley-elmer:/mnt/c/Users/sarah$ date
Sun Mar 11 19:56:57 DST 2018
scooley@scooley-elmer:/mnt/c/Users/sarah$ exit
logout

PS C:\Users\sarah> wsl date
Sun Mar 11 19:55:47 DST 2018
```

<span data-ttu-id="7b521-126">**示例：**</span><span class="sxs-lookup"><span data-stu-id="7b521-126">**Example:**</span></span>

```console
PS C:\Users\sarah> Get-VM

Name            State CPUUsage(%) MemoryAssigned(M) Uptime   Status
----            ----- ----------- ----------------- ------   ------
Server17093     Off   0           0                 00:00:00 Opera...
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
Windows         Off   0           0                 00:00:00 Opera...


PS C:\Users\sarah> Get-VM | wsl grep "Ubuntu"
Ubuntu          Off   0           0                 00:00:00 Opera...
Ubuntu (bionic) Off   0           0                 00:00:00 Opera...
PS C:\Users\sarah>
```


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="7b521-127">管理多个 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="7b521-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="7b521-128">Windows 10 版本 1903年及更高版本</span><span class="sxs-lookup"><span data-stu-id="7b521-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="7b521-129">可以使用`wsl.exe`来管理 Windows 子系统中你分发的 Linux (WSL)，包括列出可用的分发版以及设置一个默认值的分布，卸载分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="7b521-130">每个 Linux 分发版独立地管理其自己的配置。</span><span class="sxs-lookup"><span data-stu-id="7b521-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="7b521-131">若要查看特定于分发的命令，运行`[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="7b521-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="7b521-132">例如，`ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="7b521-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="7b521-133">列表分发版</span><span class="sxs-lookup"><span data-stu-id="7b521-133">List distributions</span></span>

<span data-ttu-id="7b521-134">`wsl -l` , `wsl --list`</span><span class="sxs-lookup"><span data-stu-id="7b521-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="7b521-135">列出了可用于 WSL 提供 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="7b521-136">如果列出的分发，它已安装并且可供使用。</span><span class="sxs-lookup"><span data-stu-id="7b521-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="7b521-137">列出所有分布区，包括那些不是当前可用。</span><span class="sxs-lookup"><span data-stu-id="7b521-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="7b521-138">它们可能是正在安装，卸载，或处于中断状态。</span><span class="sxs-lookup"><span data-stu-id="7b521-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="7b521-139">列出当前正在运行的所有分布区。</span><span class="sxs-lookup"><span data-stu-id="7b521-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="7b521-140">设置默认分发</span><span class="sxs-lookup"><span data-stu-id="7b521-140">Set a default distribution</span></span>

<span data-ttu-id="7b521-141">默认 WSL 分发是运行在运行时`wsl`命令行上。</span><span class="sxs-lookup"><span data-stu-id="7b521-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="7b521-142">`wsl -s <DistributionName>`， `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="7b521-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="7b521-143">设置为默认分发`<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="7b521-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="7b521-144">**示例：**</span><span class="sxs-lookup"><span data-stu-id="7b521-144">**Example:**</span></span>  
<span data-ttu-id="7b521-145">`wsl -s Ubuntu` 将我的默认分发到 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="7b521-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="7b521-146">现在，当我运行`wsl npm init`它将在 Ubuntu 中运行。</span><span class="sxs-lookup"><span data-stu-id="7b521-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="7b521-147">如果我运行`wsl`会打开一个 Ubuntu 会话。</span><span class="sxs-lookup"><span data-stu-id="7b521-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="7b521-148">注销并重新安装分发</span><span class="sxs-lookup"><span data-stu-id="7b521-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="7b521-149">Linux 分发版可以通过 Windows 安装时存储，则它们无法卸载通过应用商店。</span><span class="sxs-lookup"><span data-stu-id="7b521-149">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="7b521-150">WSL 配置允许分发要注销/卸载。</span><span class="sxs-lookup"><span data-stu-id="7b521-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="7b521-151">取消注册还允许分发版必须重新安装。</span><span class="sxs-lookup"><span data-stu-id="7b521-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="7b521-152">**警告：** 后已注销，则所有数据、 设置和与该分发的软件都将永久丢失。</span><span class="sxs-lookup"><span data-stu-id="7b521-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="7b521-153">从存储区重新安装将安装全新的分布。</span><span class="sxs-lookup"><span data-stu-id="7b521-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="7b521-154">注销 WSL 从分发，因此可以重新安装或清理。</span><span class="sxs-lookup"><span data-stu-id="7b521-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="7b521-155">例如：`wsl -unregister Ubuntu`将 Ubuntu 移除在 WSL 中可用的分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-155">For example: `wsl -unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="7b521-156">当我运行`wsl --list`不会列出。</span><span class="sxs-lookup"><span data-stu-id="7b521-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="7b521-157">若要重新安装，请在 Windows 应用商店中查找分布，并选择"启动"。</span><span class="sxs-lookup"><span data-stu-id="7b521-157">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="7b521-158">以特定用户身份运行</span><span class="sxs-lookup"><span data-stu-id="7b521-158">Run as a specific user</span></span>

<span data-ttu-id="7b521-159">`wsl -u <Username>`， `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="7b521-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="7b521-160">为指定的用户运行 WSL。</span><span class="sxs-lookup"><span data-stu-id="7b521-160">Run WSL as the specified user.</span></span> <span data-ttu-id="7b521-161">请注意该用户必须存在于内部 WSL 分发。</span><span class="sxs-lookup"><span data-stu-id="7b521-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="7b521-162">运行特定的分发版</span><span class="sxs-lookup"><span data-stu-id="7b521-162">Run a specific distribution</span></span>

<span data-ttu-id="7b521-163">`wsl --d <DistributionName>`， `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="7b521-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="7b521-164">运行 WSL 在指定的分发，可用于将命令发送到特定分发中，而无需更改默认的。</span><span class="sxs-lookup"><span data-stu-id="7b521-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="7b521-165">版本早于 Windows 10 版本 1903</span><span class="sxs-lookup"><span data-stu-id="7b521-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="7b521-166">WSL 配置 (`wslconfig.exe`) 是用于管理 Linux 分发版的 Linux (WSL) 在 Windows 子系统上运行的命令行工具。</span><span class="sxs-lookup"><span data-stu-id="7b521-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="7b521-167">它允许您列表可用发行版中，设置一个默认值的分布，并卸载分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="7b521-168">S p a n 或协调分发的设置有助于 WSL 配置时，每个 Linux 分发版独立地管理其自己的配置。</span><span class="sxs-lookup"><span data-stu-id="7b521-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="7b521-169">若要查看特定于分发的命令，运行`[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="7b521-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="7b521-170">例如，`ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="7b521-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="7b521-171">若要查看 wslconfig 所有可用的选项，请运行：  `wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="7b521-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

```console
wslconfig.exe
Performs administrative operations on Windows Subsystem for Linux

Usage:
    /l, /list [/all] - Lists registered distributions.
        /all - Optionally list all distributions, including distributions that
               are currently being installed or uninstalled.
    /s, /setdefault <DistributionName> - Sets the specified distribution as the default.
    /u, /unregister <DistributionName> - Unregisters a distribution.
```

#### <a name="list-distributions"></a><span data-ttu-id="7b521-172">列表分发版</span><span class="sxs-lookup"><span data-stu-id="7b521-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="7b521-173">列出了可用于 WSL 提供 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="7b521-174">如果列出的分发，它已安装并且可供使用。</span><span class="sxs-lookup"><span data-stu-id="7b521-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="7b521-175">列出所有分布区，包括那些不是当前可用。</span><span class="sxs-lookup"><span data-stu-id="7b521-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="7b521-176">它们可能是正在安装，卸载，或处于中断状态。</span><span class="sxs-lookup"><span data-stu-id="7b521-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="7b521-177">设置默认分发</span><span class="sxs-lookup"><span data-stu-id="7b521-177">Set a default distribution</span></span>

<span data-ttu-id="7b521-178">默认 WSL 分发是运行在运行时`wsl`命令行上。</span><span class="sxs-lookup"><span data-stu-id="7b521-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="7b521-179">设置为默认分发`<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="7b521-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="7b521-180">**示例：**</span><span class="sxs-lookup"><span data-stu-id="7b521-180">**Example:**</span></span>  
<span data-ttu-id="7b521-181">`wslconfig /setdefault Ubuntu` 将我的默认分发到 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="7b521-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="7b521-182">现在，当我运行`wsl npm init`它将在 Ubuntu 中运行。</span><span class="sxs-lookup"><span data-stu-id="7b521-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="7b521-183">如果我运行`wsl`会打开一个 Ubuntu 会话。</span><span class="sxs-lookup"><span data-stu-id="7b521-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="7b521-184">注销并重新安装分发</span><span class="sxs-lookup"><span data-stu-id="7b521-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="7b521-185">Linux 分发版可以通过 Windows 安装时存储，则它们无法卸载通过应用商店。</span><span class="sxs-lookup"><span data-stu-id="7b521-185">While Linux distributions can be installed through the Windows store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="7b521-186">WSL 配置允许分发要注销/卸载。</span><span class="sxs-lookup"><span data-stu-id="7b521-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="7b521-187">取消注册还允许分发版必须重新安装。</span><span class="sxs-lookup"><span data-stu-id="7b521-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="7b521-188">**警告：** 后已注销，则所有数据、 设置和与该分发的软件都将永久丢失。</span><span class="sxs-lookup"><span data-stu-id="7b521-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="7b521-189">从存储区重新安装将安装全新的分布。</span><span class="sxs-lookup"><span data-stu-id="7b521-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="7b521-190">注销 WSL 从分发，因此可以重新安装或清理。</span><span class="sxs-lookup"><span data-stu-id="7b521-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="7b521-191">例如：`wslconfig /unregister Ubuntu`将 Ubuntu 移除在 WSL 中可用的分发版。</span><span class="sxs-lookup"><span data-stu-id="7b521-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="7b521-192">当我运行`wslconfig /list`不会列出。</span><span class="sxs-lookup"><span data-stu-id="7b521-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="7b521-193">若要重新安装，请在 Windows 应用商店中查找分布，并选择"启动"。</span><span class="sxs-lookup"><span data-stu-id="7b521-193">To reinstall, find the distribution in the Windows Store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="7b521-194">设置 WSL 启动设置</span><span class="sxs-lookup"><span data-stu-id="7b521-194">Set WSL launch settings</span></span>

> <span data-ttu-id="7b521-195">**可在 Windows 预览体验生成 17093 及更高版本**</span><span class="sxs-lookup"><span data-stu-id="7b521-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="7b521-196">每次启动子系统使用将应用的 WSL 中自动配置的特定功能`wsl.conf`。</span><span class="sxs-lookup"><span data-stu-id="7b521-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="7b521-197">权限现在，这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="7b521-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="7b521-198">`wsl.conf` 位于中的每个 Linux 分发`/etc/wsl.conf`。</span><span class="sxs-lookup"><span data-stu-id="7b521-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="7b521-199">如果不存在该文件，您可以自行创建它。</span><span class="sxs-lookup"><span data-stu-id="7b521-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="7b521-200">WSL 将检测存在该文件，并将读取其内容。</span><span class="sxs-lookup"><span data-stu-id="7b521-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="7b521-201">如果文件缺失或格式不正确 （即，不正确标记格式设置），WSL 仍将正常启动。</span><span class="sxs-lookup"><span data-stu-id="7b521-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="7b521-202">下面是一个示例`wsl.conf`文件可以添加到你的发行版：</span><span class="sxs-lookup"><span data-stu-id="7b521-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

```console
# Enable extra metadata options by default
[automount]
enabled = true
root = /windir/
options = "metadata,umask=22,fmask=11"
mountFsTab = false

# Enable DNS – even though these are turned on by default, we’ll specify here just to be explicit.
[network]
generateHosts = true
generateResolvConf = true
```

### <a name="configuration-options"></a><span data-ttu-id="7b521-203">配置选项</span><span class="sxs-lookup"><span data-stu-id="7b521-203">Configuration Options</span></span>

<span data-ttu-id="7b521-204">为了.ini 约定保持密钥声明部分下。</span><span class="sxs-lookup"><span data-stu-id="7b521-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="7b521-205">WSL 支持两个部分：`automount`和`network`。</span><span class="sxs-lookup"><span data-stu-id="7b521-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="7b521-206">自动装载</span><span class="sxs-lookup"><span data-stu-id="7b521-206">automount</span></span>

<span data-ttu-id="7b521-207">部分中： `[automount]`</span><span class="sxs-lookup"><span data-stu-id="7b521-207">Section: `[automount]`</span></span>


| <span data-ttu-id="7b521-208">键</span><span class="sxs-lookup"><span data-stu-id="7b521-208">key</span></span>        | <span data-ttu-id="7b521-209">value</span><span class="sxs-lookup"><span data-stu-id="7b521-209">value</span></span>                          | <span data-ttu-id="7b521-210">default</span><span class="sxs-lookup"><span data-stu-id="7b521-210">default</span></span>      | <span data-ttu-id="7b521-211">说明</span><span class="sxs-lookup"><span data-stu-id="7b521-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7b521-212">enabled</span><span class="sxs-lookup"><span data-stu-id="7b521-212">enabled</span></span>    | <span data-ttu-id="7b521-213">boolean</span><span class="sxs-lookup"><span data-stu-id="7b521-213">boolean</span></span>                        | <span data-ttu-id="7b521-214">true</span><span class="sxs-lookup"><span data-stu-id="7b521-214">true</span></span>         | <span data-ttu-id="7b521-215">`true` 固定驱动器 （即的原因</span><span class="sxs-lookup"><span data-stu-id="7b521-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="7b521-216">`C:/` 或`D:/`) 以将其自动装入与 DrvFs 下`/mnt`。</span><span class="sxs-lookup"><span data-stu-id="7b521-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="7b521-217">`false` 表示不会自动装载驱动器，但您仍无法装载它们，手动或通过`fstab`。</span><span class="sxs-lookup"><span data-stu-id="7b521-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="7b521-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="7b521-218">mountFsTab</span></span> | <span data-ttu-id="7b521-219">boolean</span><span class="sxs-lookup"><span data-stu-id="7b521-219">boolean</span></span>                        | <span data-ttu-id="7b521-220">true</span><span class="sxs-lookup"><span data-stu-id="7b521-220">true</span></span>         | <span data-ttu-id="7b521-221">`true` 设置`/etc/fstab`要处理在 WSL 启动。</span><span class="sxs-lookup"><span data-stu-id="7b521-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="7b521-222">/etc/fstab 是您可以在其中声明其他文件系统，如 SMB 共享的文件。</span><span class="sxs-lookup"><span data-stu-id="7b521-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="7b521-223">因此，你可以向上装载自动在开始上的 WSL 中这些文件系统。</span><span class="sxs-lookup"><span data-stu-id="7b521-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="7b521-224">根</span><span class="sxs-lookup"><span data-stu-id="7b521-224">root</span></span>       | <span data-ttu-id="7b521-225">字符串</span><span class="sxs-lookup"><span data-stu-id="7b521-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="7b521-226">设置固定的驱动器会将其自动装入的目录。</span><span class="sxs-lookup"><span data-stu-id="7b521-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="7b521-227">例如，如果您有一个目录中在 WSL`/windir/`和指定，作为根，你会希望看到固定的驱动器装载在 `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="7b521-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="7b521-228">选项</span><span class="sxs-lookup"><span data-stu-id="7b521-228">options</span></span>    | <span data-ttu-id="7b521-229">以逗号分隔的值列表</span><span class="sxs-lookup"><span data-stu-id="7b521-229">comma-separated list of values</span></span> | <span data-ttu-id="7b521-230">空字符串</span><span class="sxs-lookup"><span data-stu-id="7b521-230">empty string</span></span> | <span data-ttu-id="7b521-231">此值追加到默认 DrvFs 装入选项字符串。</span><span class="sxs-lookup"><span data-stu-id="7b521-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="7b521-232">**可以指定仅特定于 DrvFs 的选项。**</span><span class="sxs-lookup"><span data-stu-id="7b521-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="7b521-233">不支持二进制装入通常会将分析成一个标志的选项。</span><span class="sxs-lookup"><span data-stu-id="7b521-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="7b521-234">如果你想要显式指定这些选项，则必须包括你想要这样做在 /etc/fstab 中每个的驱动器。</span><span class="sxs-lookup"><span data-stu-id="7b521-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="7b521-235">默认情况下，WSL 设置 uid 和 gid 的值的默认用户 (在 Ubuntu 发行版中的默认用户创建与 uid = 1000，gid = 1000年)。</span><span class="sxs-lookup"><span data-stu-id="7b521-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="7b521-236">如果用户指定了此密钥通过显式 gid 或 uid 选项，将覆盖相关联的值。</span><span class="sxs-lookup"><span data-stu-id="7b521-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="7b521-237">否则，将始终追加的默认值。</span><span class="sxs-lookup"><span data-stu-id="7b521-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="7b521-238">**注意：** 这些选项将应用作为所有自动加载的驱动器装载选项。</span><span class="sxs-lookup"><span data-stu-id="7b521-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="7b521-239">若要更改特定驱动器的选项，请改为使用 /etc/fstab。</span><span class="sxs-lookup"><span data-stu-id="7b521-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="7b521-240">网络</span><span class="sxs-lookup"><span data-stu-id="7b521-240">network</span></span>

<span data-ttu-id="7b521-241">章节标签： `[network]`</span><span class="sxs-lookup"><span data-stu-id="7b521-241">Section label: `[network]`</span></span>

| <span data-ttu-id="7b521-242">键</span><span class="sxs-lookup"><span data-stu-id="7b521-242">key</span></span> | <span data-ttu-id="7b521-243">value</span><span class="sxs-lookup"><span data-stu-id="7b521-243">value</span></span> | <span data-ttu-id="7b521-244">default</span><span class="sxs-lookup"><span data-stu-id="7b521-244">default</span></span> | <span data-ttu-id="7b521-245">说明</span><span class="sxs-lookup"><span data-stu-id="7b521-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="7b521-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="7b521-246">generateHosts</span></span> | <span data-ttu-id="7b521-247">boolean</span><span class="sxs-lookup"><span data-stu-id="7b521-247">boolean</span></span> | `true` | <span data-ttu-id="7b521-248">`true` 设置生成的 WSL `/etc/hosts`。</span><span class="sxs-lookup"><span data-stu-id="7b521-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="7b521-249">`hosts`文件包含的主机名对应的 IP 地址的静态映射。</span><span class="sxs-lookup"><span data-stu-id="7b521-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="7b521-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="7b521-250">generateResolvConf</span></span> | <span data-ttu-id="7b521-251">boolean</span><span class="sxs-lookup"><span data-stu-id="7b521-251">boolean</span></span> | `true` | <span data-ttu-id="7b521-252">`true` 设置生成的 WSL `/etc/resolv.conf`。</span><span class="sxs-lookup"><span data-stu-id="7b521-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="7b521-253">`resolv.conf`包含能够将给定主机名解析为其 IP 地址的 DNS 列表。</span><span class="sxs-lookup"><span data-stu-id="7b521-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="7b521-254">互操作</span><span class="sxs-lookup"><span data-stu-id="7b521-254">interop</span></span>

<span data-ttu-id="7b521-255">章节标签： `[interop]`</span><span class="sxs-lookup"><span data-stu-id="7b521-255">Section label: `[interop]`</span></span>

<span data-ttu-id="7b521-256">这些选项是可用在内部生成 17713 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="7b521-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="7b521-257">键</span><span class="sxs-lookup"><span data-stu-id="7b521-257">key</span></span> | <span data-ttu-id="7b521-258">value</span><span class="sxs-lookup"><span data-stu-id="7b521-258">value</span></span> | <span data-ttu-id="7b521-259">default</span><span class="sxs-lookup"><span data-stu-id="7b521-259">default</span></span> | <span data-ttu-id="7b521-260">说明</span><span class="sxs-lookup"><span data-stu-id="7b521-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="7b521-261">enabled</span><span class="sxs-lookup"><span data-stu-id="7b521-261">enabled</span></span> | <span data-ttu-id="7b521-262">boolean</span><span class="sxs-lookup"><span data-stu-id="7b521-262">boolean</span></span> | `true` | <span data-ttu-id="7b521-263">此键的设置将确定是否支持 WSL 启动 Windows 进程。</span><span class="sxs-lookup"><span data-stu-id="7b521-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="7b521-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="7b521-264">appendWindowsPath</span></span> | <span data-ttu-id="7b521-265">boolean</span><span class="sxs-lookup"><span data-stu-id="7b521-265">boolean</span></span> | `true` | <span data-ttu-id="7b521-266">此键的设置将确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。</span><span class="sxs-lookup"><span data-stu-id="7b521-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
