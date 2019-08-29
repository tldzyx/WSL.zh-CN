---
title: 管理 Linux 分发版
description: 参考列出和配置在适用于 Linux 的 Windows 子系统上运行的多个 Linux 发行版。
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu、wsl、wslconfig
author: scooley
ms.author: scooley
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: ca65cf6fde3e0ba4750ffc44f5aec542be6cfabf
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122704"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="907b3-104">管理和配置适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="907b3-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="907b3-105">适用于 Windows 10 秋季创意者更新及更高版本。</span><span class="sxs-lookup"><span data-stu-id="907b3-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="907b3-106">请参阅更新的[安装指南](./install_guide.md), 尝试新的管理功能, 并开始从 Microsoft 应用商店运行多个 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="907b3-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="907b3-107">运行 WSL 的方式</span><span class="sxs-lookup"><span data-stu-id="907b3-107">Ways to run WSL</span></span>

<span data-ttu-id="907b3-108">使用适用于 Linux 的 Windows 子系统运行 Linux 的方法有很多种。</span><span class="sxs-lookup"><span data-stu-id="907b3-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="907b3-109">`[distro]`, 例如`ubuntu`</span><span class="sxs-lookup"><span data-stu-id="907b3-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="907b3-110">`wsl.exe` 或 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="907b3-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="907b3-111">`wsl [command]` 或 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="907b3-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="907b3-112">应使用哪种方法取决于所执行的操作。</span><span class="sxs-lookup"><span data-stu-id="907b3-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="907b3-113">通过发行版启动 WSL</span><span class="sxs-lookup"><span data-stu-id="907b3-113">Launch WSL by distribution</span></span>

<span data-ttu-id="907b3-114">使用它的特定于发行版的应用程序运行发行版会在其自己的控制台窗口中启动该发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![从 "开始" 菜单启动 WSL](media/start-launch.png)

<span data-ttu-id="907b3-116">这与在 Microsoft 应用商店中单击 "启动" 是相同的。</span><span class="sxs-lookup"><span data-stu-id="907b3-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![从 Microsoft 应用商店启动 WSL](media/store-launch.png)

<span data-ttu-id="907b3-118">还可以通过运行 `[distribution].exe`，从命令行运行发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="907b3-119">以这种方式从命令行运行发行版的缺点是，它会自动将你的工作目录从当前目录更改为发行版的主目录。</span><span class="sxs-lookup"><span data-stu-id="907b3-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="907b3-120">**示例：**</span><span class="sxs-lookup"><span data-stu-id="907b3-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="907b3-121">wsl 和 wsl [command]</span><span class="sxs-lookup"><span data-stu-id="907b3-121">wsl and wsl [command]</span></span>

<span data-ttu-id="907b3-122">从命令行运行 WSL 的最佳方法是使用 `wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="907b3-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="907b3-123">**示例：**</span><span class="sxs-lookup"><span data-stu-id="907b3-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="907b3-124">`wsl` 不仅保留了当前的工作目录，还允许你随 Windows 命令运行单个命令。</span><span class="sxs-lookup"><span data-stu-id="907b3-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="907b3-125">**示例：**</span><span class="sxs-lookup"><span data-stu-id="907b3-125">**Example:**</span></span>

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

<span data-ttu-id="907b3-126">**示例：**</span><span class="sxs-lookup"><span data-stu-id="907b3-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="907b3-127">管理多个 Linux 发行版</span><span class="sxs-lookup"><span data-stu-id="907b3-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="907b3-128">Windows 10 版本 1903 及更高版本</span><span class="sxs-lookup"><span data-stu-id="907b3-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="907b3-129">可使用 `wsl.exe` 来管理适用于 Linux 的 Windows 子系统 (WSL) 中的发行版，包括列出可用的发行版，设置默认发行版和卸载发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="907b3-130">每个 Linux 发行版独立地管理其自己的配置。</span><span class="sxs-lookup"><span data-stu-id="907b3-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="907b3-131">若要查看特定于发行版的命令，请运行 `[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="907b3-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="907b3-132">例如：`ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="907b3-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="907b3-133">列出发行版</span><span class="sxs-lookup"><span data-stu-id="907b3-133">List distributions</span></span>

<span data-ttu-id="907b3-134">`wsl -l`,`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="907b3-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="907b3-135">列出 WSL 可用的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="907b3-136">如果已列出某个发行版，则表示它已安装并可供使用。</span><span class="sxs-lookup"><span data-stu-id="907b3-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="907b3-137">列出所有发行版，包括当前不可用的发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="907b3-138">它们可能正在安装、正在卸载或处于断开状态。</span><span class="sxs-lookup"><span data-stu-id="907b3-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="907b3-139">列出当前正在运行的所有发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="907b3-140">设置默认发行版</span><span class="sxs-lookup"><span data-stu-id="907b3-140">Set a default distribution</span></span>

<span data-ttu-id="907b3-141">默认 WSL 发行版是在命令行上运行 `wsl` 时所运行的发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="907b3-142">`wsl -s <DistributionName>`， `wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="907b3-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="907b3-143">将默认发行版设置为 `<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="907b3-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="907b3-144">**示例：**</span><span class="sxs-lookup"><span data-stu-id="907b3-144">**Example:**</span></span>  
<span data-ttu-id="907b3-145">`wsl -s Ubuntu` 会将我的默认发行版设置为 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="907b3-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="907b3-146">现在，当我运行 `wsl npm init` 时，它将在 Ubuntu 中运行。</span><span class="sxs-lookup"><span data-stu-id="907b3-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="907b3-147">如果我运行 `wsl`，它将打开一个 Ubuntu 会话。</span><span class="sxs-lookup"><span data-stu-id="907b3-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="907b3-148">注销并重新安装分发</span><span class="sxs-lookup"><span data-stu-id="907b3-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="907b3-149">虽然可以通过 Microsoft store 安装 Linux 分发版, 但无法通过应用商店卸载。</span><span class="sxs-lookup"><span data-stu-id="907b3-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="907b3-150">WSL Config 允许注销/卸载发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="907b3-151">注销后仍然可以重新安装发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="907b3-152">**警告：** 注销后，与该发行版相关的所有数据、设置和软件将永久丢失。</span><span class="sxs-lookup"><span data-stu-id="907b3-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="907b3-153">从 Store 重新安装将安装发行版的干净副本。</span><span class="sxs-lookup"><span data-stu-id="907b3-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="907b3-154">从 WSL 中注销发行版，以便可以重新安装或清除它。</span><span class="sxs-lookup"><span data-stu-id="907b3-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="907b3-155">例如：`wsl --unregister Ubuntu` 会从 WSL 中可用的发行版中删除 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="907b3-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="907b3-156">当我运行 `wsl --list` 时，它不会被列出。</span><span class="sxs-lookup"><span data-stu-id="907b3-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="907b3-157">若要重新安装，请在 Microsoft Store 中查找发行版，并选择"启动。</span><span class="sxs-lookup"><span data-stu-id="907b3-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="907b3-158">以特定用户身份运行</span><span class="sxs-lookup"><span data-stu-id="907b3-158">Run as a specific user</span></span>

<span data-ttu-id="907b3-159">`wsl -u <Username>`， `wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="907b3-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="907b3-160">以指定用户的身份运行 WSL。</span><span class="sxs-lookup"><span data-stu-id="907b3-160">Run WSL as the specified user.</span></span> <span data-ttu-id="907b3-161">请注意，用户必须存在于 WSL 发行版内。</span><span class="sxs-lookup"><span data-stu-id="907b3-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="907b3-162">运行特定的发行版</span><span class="sxs-lookup"><span data-stu-id="907b3-162">Run a specific distribution</span></span>

<span data-ttu-id="907b3-163">`wsl --d <DistributionName>`， `wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="907b3-163">`wsl --d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="907b3-164">运行指定的 WSL 发行版。可用于将命令发送到特定发行版，而无需更改默认值。</span><span class="sxs-lookup"><span data-stu-id="907b3-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="907b3-165">早于 Windows 10 版本1903的版本</span><span class="sxs-lookup"><span data-stu-id="907b3-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="907b3-166">WSL Config (`wslconfig.exe`) 是一个命令行工具，用于管理在适用于 Linux 的 Windows 子系统 (WSL) 上运行的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="907b3-167">通过它，可列出可用的发行版，设置默认发行版以及卸载发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="907b3-168">虽然 WSL Config 对跨越或协调发行版的设置很有帮助，但每个 Linux 发行版都独立管理自己的配置。</span><span class="sxs-lookup"><span data-stu-id="907b3-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="907b3-169">若要查看特定于发行版的命令，请运行 `[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="907b3-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="907b3-170">例如：`ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="907b3-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="907b3-171">若要查看 wslconfig 的所有可用选项, 请运行:`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="907b3-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="907b3-172">列出发行版</span><span class="sxs-lookup"><span data-stu-id="907b3-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="907b3-173">列出 WSL 可用的 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="907b3-174">如果已列出某个发行版，则表示它已安装并可供使用。</span><span class="sxs-lookup"><span data-stu-id="907b3-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="907b3-175">列出所有发行版，包括当前不可用的发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="907b3-176">它们可能正在安装、正在卸载或处于断开状态。</span><span class="sxs-lookup"><span data-stu-id="907b3-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="907b3-177">设置默认发行版</span><span class="sxs-lookup"><span data-stu-id="907b3-177">Set a default distribution</span></span>

<span data-ttu-id="907b3-178">默认 WSL 发行版是在命令行上运行 `wsl` 时所运行的发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="907b3-179">将默认发行版设置为 `<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="907b3-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="907b3-180">**示例：**</span><span class="sxs-lookup"><span data-stu-id="907b3-180">**Example:**</span></span>  
<span data-ttu-id="907b3-181">`wslconfig /setdefault Ubuntu` 会将我的默认发行版设置为 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="907b3-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="907b3-182">现在，当我运行 `wsl npm init` 时，它将在 Ubuntu 中运行。</span><span class="sxs-lookup"><span data-stu-id="907b3-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="907b3-183">如果我运行 `wsl`，它将打开一个 Ubuntu 会话。</span><span class="sxs-lookup"><span data-stu-id="907b3-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="907b3-184">注销并重新安装分发</span><span class="sxs-lookup"><span data-stu-id="907b3-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="907b3-185">虽然可以通过 Microsoft store 安装 Linux 分发版, 但无法通过应用商店卸载。</span><span class="sxs-lookup"><span data-stu-id="907b3-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="907b3-186">WSL Config 允许注销/卸载发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="907b3-187">注销后仍然可以重新安装发行版。</span><span class="sxs-lookup"><span data-stu-id="907b3-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="907b3-188">**警告：** 注销后，与该发行版相关的所有数据、设置和软件将永久丢失。</span><span class="sxs-lookup"><span data-stu-id="907b3-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="907b3-189">从 Store 重新安装将安装发行版的干净副本。</span><span class="sxs-lookup"><span data-stu-id="907b3-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="907b3-190">从 WSL 中注销发行版，以便可以重新安装或清除它。</span><span class="sxs-lookup"><span data-stu-id="907b3-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="907b3-191">例如：`wslconfig /unregister Ubuntu` 会从 WSL 中可用的发行版中删除 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="907b3-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="907b3-192">当我运行 `wslconfig /list` 时，它不会被列出。</span><span class="sxs-lookup"><span data-stu-id="907b3-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="907b3-193">若要重新安装，请在 Microsoft Store 中查找发行版，并选择"启动。</span><span class="sxs-lookup"><span data-stu-id="907b3-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="907b3-194">设置 WSL 启动设置</span><span class="sxs-lookup"><span data-stu-id="907b3-194">Set WSL launch settings</span></span>

> <span data-ttu-id="907b3-195">**适用于 Windows 预览体验内部版本 17093 及更高版本**</span><span class="sxs-lookup"><span data-stu-id="907b3-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="907b3-196">自动配置 WSL 中的某些功能，每次使用 `wsl.conf` 启动子系统时都会应用这些功能。</span><span class="sxs-lookup"><span data-stu-id="907b3-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="907b3-197">现在，这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="907b3-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="907b3-198">`wsl.conf` 在每个 Linux 发行版中都位于`/etc/wsl.conf`。</span><span class="sxs-lookup"><span data-stu-id="907b3-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="907b3-199">如果文件不在该位置，你可以自行创建。</span><span class="sxs-lookup"><span data-stu-id="907b3-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="907b3-200">WSL 将检测该文件是否存在，并读取其内容。</span><span class="sxs-lookup"><span data-stu-id="907b3-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="907b3-201">如果文件缺失或格式不正确 （即，标记格式不正确），WSL 仍将正常启动。</span><span class="sxs-lookup"><span data-stu-id="907b3-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="907b3-202">下面是一个示例 `wsl.conf` 文件，可以将其添加到发行版中：</span><span class="sxs-lookup"><span data-stu-id="907b3-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="907b3-203">配置选项</span><span class="sxs-lookup"><span data-stu-id="907b3-203">Configuration Options</span></span>

<span data-ttu-id="907b3-204">为了与 .ini 约定保持一致，键 (key) 在一个节 (section) 下声明。</span><span class="sxs-lookup"><span data-stu-id="907b3-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="907b3-205">WSL 支持两个节 (section)：`automount`和`network`。</span><span class="sxs-lookup"><span data-stu-id="907b3-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="907b3-206">装载</span><span class="sxs-lookup"><span data-stu-id="907b3-206">automount</span></span>

<span data-ttu-id="907b3-207">节 (Section)：`[automount]`</span><span class="sxs-lookup"><span data-stu-id="907b3-207">Section: `[automount]`</span></span>


| <span data-ttu-id="907b3-208">键</span><span class="sxs-lookup"><span data-stu-id="907b3-208">key</span></span>        | <span data-ttu-id="907b3-209">value</span><span class="sxs-lookup"><span data-stu-id="907b3-209">value</span></span>                          | <span data-ttu-id="907b3-210">default</span><span class="sxs-lookup"><span data-stu-id="907b3-210">default</span></span>      | <span data-ttu-id="907b3-211">本票</span><span class="sxs-lookup"><span data-stu-id="907b3-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="907b3-212">enabled</span><span class="sxs-lookup"><span data-stu-id="907b3-212">enabled</span></span>    | <span data-ttu-id="907b3-213">boolean</span><span class="sxs-lookup"><span data-stu-id="907b3-213">boolean</span></span>                        | <span data-ttu-id="907b3-214">真</span><span class="sxs-lookup"><span data-stu-id="907b3-214">true</span></span>         | <span data-ttu-id="907b3-215">`true` 固定驱动器 （即</span><span class="sxs-lookup"><span data-stu-id="907b3-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="907b3-216">`C:/` 或 `D:/`）会自动装载 `/mnt` 下的 DrvF。</span><span class="sxs-lookup"><span data-stu-id="907b3-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="907b3-217">`false` 表示驱动器不会自动装载，但你仍然可以手动或通过 `fstab` 装载它们。</span><span class="sxs-lookup"><span data-stu-id="907b3-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="907b3-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="907b3-218">mountFsTab</span></span> | <span data-ttu-id="907b3-219">boolean</span><span class="sxs-lookup"><span data-stu-id="907b3-219">boolean</span></span>                        | <span data-ttu-id="907b3-220">真</span><span class="sxs-lookup"><span data-stu-id="907b3-220">true</span></span>         | <span data-ttu-id="907b3-221">`true` - 设置为在 WSL 启动时处理 `/etc/fstab`。</span><span class="sxs-lookup"><span data-stu-id="907b3-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="907b3-222">/etc/fstab 是一个文件，可以在其中声明其他文件系统，如 SMB 共享。</span><span class="sxs-lookup"><span data-stu-id="907b3-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="907b3-223">因此，可以在启动时自动将这些文件系统安装在 WSL 中。</span><span class="sxs-lookup"><span data-stu-id="907b3-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="907b3-224">root</span><span class="sxs-lookup"><span data-stu-id="907b3-224">root</span></span>       | <span data-ttu-id="907b3-225">字符串</span><span class="sxs-lookup"><span data-stu-id="907b3-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="907b3-226">设置自动装载固定驱动器的目录。</span><span class="sxs-lookup"><span data-stu-id="907b3-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="907b3-227">例如，如果你在的 WSL 中的 `/windir/` 有一个目录并且指定它作为 root，则可能会看到固定驱动器装载在 `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="907b3-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="907b3-228">options</span><span class="sxs-lookup"><span data-stu-id="907b3-228">options</span></span>    | <span data-ttu-id="907b3-229">以逗号分隔的值列表</span><span class="sxs-lookup"><span data-stu-id="907b3-229">comma-separated list of values</span></span> | <span data-ttu-id="907b3-230">空字符串</span><span class="sxs-lookup"><span data-stu-id="907b3-230">empty string</span></span> | <span data-ttu-id="907b3-231">此值会追加到默认 DrvFs 装载选项字符串。</span><span class="sxs-lookup"><span data-stu-id="907b3-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="907b3-232">**只能指定 DrvFs 特定的选项。**</span><span class="sxs-lookup"><span data-stu-id="907b3-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="907b3-233">不支持二进制装载通常会将分析成一个标志的选项。</span><span class="sxs-lookup"><span data-stu-id="907b3-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="907b3-234">如果要显式指定这些选项，则必须在 /etc/fstab 中包括想对其执行此操作的每个驱动器。</span><span class="sxs-lookup"><span data-stu-id="907b3-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="907b3-235">默认情况下，WSL 将 uid 和 gid 设置为默认用户的值（在 Ubuntu 发行版中，默认用户使用 uid = 1000，gid = 1000 创建）。</span><span class="sxs-lookup"><span data-stu-id="907b3-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="907b3-236">如果用户通过此键显式指定 gid 或 uid 选项，则将覆盖关联的值。否则，将始终追加默认值。</span><span class="sxs-lookup"><span data-stu-id="907b3-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="907b3-237">否则, 将始终追加默认值。</span><span class="sxs-lookup"><span data-stu-id="907b3-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="907b3-238">**注意：** 这些选项用作所有自动装载的驱动器的装载选项。</span><span class="sxs-lookup"><span data-stu-id="907b3-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="907b3-239">要想仅更改特定驱动器的选项，请改用 /etc/fstab。</span><span class="sxs-lookup"><span data-stu-id="907b3-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

#### <a name="network"></a><span data-ttu-id="907b3-240">网络</span><span class="sxs-lookup"><span data-stu-id="907b3-240">network</span></span>

<span data-ttu-id="907b3-241">节 (section) 标签： `[network]`</span><span class="sxs-lookup"><span data-stu-id="907b3-241">Section label: `[network]`</span></span>

| <span data-ttu-id="907b3-242">键</span><span class="sxs-lookup"><span data-stu-id="907b3-242">key</span></span> | <span data-ttu-id="907b3-243">value</span><span class="sxs-lookup"><span data-stu-id="907b3-243">value</span></span> | <span data-ttu-id="907b3-244">default</span><span class="sxs-lookup"><span data-stu-id="907b3-244">default</span></span> | <span data-ttu-id="907b3-245">本票</span><span class="sxs-lookup"><span data-stu-id="907b3-245">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="907b3-246">generateHosts</span><span class="sxs-lookup"><span data-stu-id="907b3-246">generateHosts</span></span> | <span data-ttu-id="907b3-247">boolean</span><span class="sxs-lookup"><span data-stu-id="907b3-247">boolean</span></span> | `true` | <span data-ttu-id="907b3-248">`true`设置要生成`/etc/hosts`的 WSL。</span><span class="sxs-lookup"><span data-stu-id="907b3-248">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="907b3-249">`hosts`文件包含主机名对应的 IP 地址的静态映射。</span><span class="sxs-lookup"><span data-stu-id="907b3-249">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="907b3-250">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="907b3-250">generateResolvConf</span></span> | <span data-ttu-id="907b3-251">boolean</span><span class="sxs-lookup"><span data-stu-id="907b3-251">boolean</span></span> | `true` | <span data-ttu-id="907b3-252">`true`将 WSL 设置为`/etc/resolv.conf`生成。</span><span class="sxs-lookup"><span data-stu-id="907b3-252">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="907b3-253">`resolv.conf`包含能够将给定主机名解析为其 IP 地址的 DNS 列表。</span><span class="sxs-lookup"><span data-stu-id="907b3-253">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="907b3-254">交互</span><span class="sxs-lookup"><span data-stu-id="907b3-254">interop</span></span>

<span data-ttu-id="907b3-255">节 (section) 标签： `[interop]`</span><span class="sxs-lookup"><span data-stu-id="907b3-255">Section label: `[interop]`</span></span>

<span data-ttu-id="907b3-256">这些选项适用于预览体验内部版本 17713 及更高版本。</span><span class="sxs-lookup"><span data-stu-id="907b3-256">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="907b3-257">键</span><span class="sxs-lookup"><span data-stu-id="907b3-257">key</span></span> | <span data-ttu-id="907b3-258">value</span><span class="sxs-lookup"><span data-stu-id="907b3-258">value</span></span> | <span data-ttu-id="907b3-259">default</span><span class="sxs-lookup"><span data-stu-id="907b3-259">default</span></span> | <span data-ttu-id="907b3-260">本票</span><span class="sxs-lookup"><span data-stu-id="907b3-260">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="907b3-261">enabled</span><span class="sxs-lookup"><span data-stu-id="907b3-261">enabled</span></span> | <span data-ttu-id="907b3-262">boolean</span><span class="sxs-lookup"><span data-stu-id="907b3-262">boolean</span></span> | `true` | <span data-ttu-id="907b3-263">设置此项将确定 WSL 是否将支持启动 Windows 进程。</span><span class="sxs-lookup"><span data-stu-id="907b3-263">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="907b3-264">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="907b3-264">appendWindowsPath</span></span> | <span data-ttu-id="907b3-265">boolean</span><span class="sxs-lookup"><span data-stu-id="907b3-265">boolean</span></span> | `true` | <span data-ttu-id="907b3-266">设置此项将确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。</span><span class="sxs-lookup"><span data-stu-id="907b3-266">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
