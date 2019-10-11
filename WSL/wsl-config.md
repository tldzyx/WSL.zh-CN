---
title: 管理 Linux 分发版
description: 有关列出和配置在适用于 Linux 的 Windows 子系统上运行的多个 Linux 分发版的参考文章。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 02/7/2018
ms.topic: article
ms.assetid: 7ca59bd7-d9d3-4f6d-8b92-b8faa9bcf250
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e69810625d08baf734683ff06231f79132ce1519
ms.sourcegitcommit: e1cc2fe4de0fa03d5aea14f6b328f1bb9d0c59be
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/07/2019
ms.locfileid: "71999400"
---
# <a name="manage-and-configure-windows-subsystem-for-linux"></a><span data-ttu-id="8539c-104">管理和配置适用于 Linux 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="8539c-104">Manage and configure Windows Subsystem for Linux</span></span>

> <span data-ttu-id="8539c-105">适用于 Windows 10 Fall Creators Update 和更高版本。</span><span class="sxs-lookup"><span data-stu-id="8539c-105">Applies to Windows 10 Fall Creators Update and later.</span></span>  <span data-ttu-id="8539c-106">若要试用新的管理功能并开始从 Microsoft Store 运行多个 Linux 分发版，请参阅更新的[安装指南](./install_guide.md)。</span><span class="sxs-lookup"><span data-stu-id="8539c-106">See our updated [installation guide](./install_guide.md) to try new management features and start running multiple Linux distributions from the Microsoft store.</span></span>

## <a name="ways-to-run-wsl"></a><span data-ttu-id="8539c-107">WSL 的运行方式</span><span class="sxs-lookup"><span data-stu-id="8539c-107">Ways to run WSL</span></span>

<span data-ttu-id="8539c-108">可通过多种方式配合适用于 Linux 的 Windows 子系统运行 Linux。</span><span class="sxs-lookup"><span data-stu-id="8539c-108">There are many ways to run Linux with the Windows Subsystem for Linux.</span></span>

1. <span data-ttu-id="8539c-109">`[distro]`，例如 `ubuntu`</span><span class="sxs-lookup"><span data-stu-id="8539c-109">`[distro]`, for example `ubuntu`</span></span>
1. <span data-ttu-id="8539c-110">`wsl.exe` 或 `bash.exe`</span><span class="sxs-lookup"><span data-stu-id="8539c-110">`wsl.exe` or `bash.exe`</span></span>
1. <span data-ttu-id="8539c-111">`wsl [command]` 或 `bash -c [command]`</span><span class="sxs-lookup"><span data-stu-id="8539c-111">`wsl [command]` or `bash -c [command]`</span></span>

<span data-ttu-id="8539c-112">要使用的方法取决于执行的操作。</span><span class="sxs-lookup"><span data-stu-id="8539c-112">Which method you should use depends on what you're doing.</span></span>

### <a name="launch-wsl-by-distribution"></a><span data-ttu-id="8539c-113">按分发版启动 WSL</span><span class="sxs-lookup"><span data-stu-id="8539c-113">Launch WSL by distribution</span></span>

<span data-ttu-id="8539c-114">使用特定于分发版的应用程序运行某个分发版会在其自身的控制台窗口中将它启动。</span><span class="sxs-lookup"><span data-stu-id="8539c-114">Running a distribution using it's distro-specific application launches that distribution in it's own console window.</span></span>

![从“开始”菜单启动 WSL](media/start-launch.png)

<span data-ttu-id="8539c-116">这相当于在 Microsoft Store 中单击“启动”。</span><span class="sxs-lookup"><span data-stu-id="8539c-116">It is the same as clicking "Launch" in the Microsoft store.</span></span>

![从 Microsoft Store 启动 WSL](media/store-launch.png)

<span data-ttu-id="8539c-118">还可以在命令行中运行 `[distribution].exe` 来运行分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-118">You can also run the distribution from the command line by running `[distribution].exe`.</span></span>

<span data-ttu-id="8539c-119">以这种方式从命令行运行分发版的缺点是，会自动将工作目录从当前目录更改为分发版的主目录。</span><span class="sxs-lookup"><span data-stu-id="8539c-119">The disadvantage of running a distribution from the command line in this way is that it will automatically change your working directory from the current directory to the distribution's home directory.</span></span>

<span data-ttu-id="8539c-120">**示例：**</span><span class="sxs-lookup"><span data-stu-id="8539c-120">**Example:**</span></span>

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

### <a name="wsl-and-wsl-command"></a><span data-ttu-id="8539c-121">wsl 和 wsl [命令]</span><span class="sxs-lookup"><span data-stu-id="8539c-121">wsl and wsl [command]</span></span>

<span data-ttu-id="8539c-122">从命令行运行 WSL 的最佳方式是使用 `wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="8539c-122">The best way to run WSL from the command line is using `wsl.exe`.</span></span>

<span data-ttu-id="8539c-123">**示例：**</span><span class="sxs-lookup"><span data-stu-id="8539c-123">**Example:**</span></span>

```console
PS C:\Users\sarah> pwd

Path
----
C:\Users\sarah

PS C:\Users\sarah> wsl

scooley@scooley-elmer:/mnt/c/Users/sarah$ pwd
/mnt/c/Users/sarah
```

<span data-ttu-id="8539c-124">这样，`wsl` 不仅可以保留当前工作目录，而且还允许结合 Windows 命令运行单个命令。</span><span class="sxs-lookup"><span data-stu-id="8539c-124">Not only does `wsl` keep the current working directory in place, it lets you run a single command along side Windows commands.</span></span>

<span data-ttu-id="8539c-125">**示例：**</span><span class="sxs-lookup"><span data-stu-id="8539c-125">**Example:**</span></span>

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

<span data-ttu-id="8539c-126">**示例：**</span><span class="sxs-lookup"><span data-stu-id="8539c-126">**Example:**</span></span>

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


## <a name="managing-multiple-linux-distributions"></a><span data-ttu-id="8539c-127">管理多个 Linux 分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-127">Managing multiple Linux Distributions</span></span>

### <a name="windows-10-version-1903-and-later"></a><span data-ttu-id="8539c-128">Windows 10 版本 1903 和更高版本</span><span class="sxs-lookup"><span data-stu-id="8539c-128">Windows 10 Version 1903 and later</span></span>

<span data-ttu-id="8539c-129">可以使用 `wsl.exe` 管理适用于 Linux 的 Windows 子系统 (WSL) 中的分发版，包括列出可用分发版、设置默认分发版，以及卸载分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-129">You can use `wsl.exe` to manage your distributions in the Windows Subsystem for Linux (WSL), including listing available distributions, setting a default distribution, and uninstalling distributions.</span></span>

<span data-ttu-id="8539c-130">每个 Linux 分发版独立管理自身的配置。</span><span class="sxs-lookup"><span data-stu-id="8539c-130">Each Linux distribution independently manages its own configurations.</span></span> <span data-ttu-id="8539c-131">若要查看特定于分发版的命令，请运行 `[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="8539c-131">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="8539c-132">例如 `ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="8539c-132">For example `ubuntu /?`.</span></span>

#### <a name="list-distributions"></a><span data-ttu-id="8539c-133">列出分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-133">List distributions</span></span>

<span data-ttu-id="8539c-134">`wsl -l`、`wsl --list`</span><span class="sxs-lookup"><span data-stu-id="8539c-134">`wsl -l` , `wsl --list`</span></span>  
<span data-ttu-id="8539c-135">列出可用于 WSL 的 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-135">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="8539c-136">如果列出了某个分发版，表示该分发版已安装且可供使用。</span><span class="sxs-lookup"><span data-stu-id="8539c-136">If a distribution is listed, it's installed and ready to use.</span></span>

`wsl --list --all`   
<span data-ttu-id="8539c-137">列出所有分发版，包括当前不可用的分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-137">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="8539c-138">这些分发版可能正在安装、卸载或处于损坏状态。</span><span class="sxs-lookup"><span data-stu-id="8539c-138">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

`wsl --list --running`   
<span data-ttu-id="8539c-139">列出当前正在运行的所有分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-139">Lists all distributions that are currently running.</span></span>

#### <a name="set-a-default-distribution"></a><span data-ttu-id="8539c-140">设置默认分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-140">Set a default distribution</span></span>

<span data-ttu-id="8539c-141">默认 WSL 分布版是在命令行中运行 `wsl` 时运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-141">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

<span data-ttu-id="8539c-142">`wsl -s <DistributionName>`、`wsl --setdefault <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="8539c-142">`wsl -s <DistributionName>`, `wsl --setdefault <DistributionName>`</span></span>

<span data-ttu-id="8539c-143">将默认分发版设置为 `<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="8539c-143">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="8539c-144">**示例：**</span><span class="sxs-lookup"><span data-stu-id="8539c-144">**Example:**</span></span>  
<span data-ttu-id="8539c-145">`wsl -s Ubuntu` 会将我的默认分发版设置为 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="8539c-145">`wsl -s Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="8539c-146">现在，当我运行 `wsl npm init` 时，该分发版将在 Ubuntu 中运行。</span><span class="sxs-lookup"><span data-stu-id="8539c-146">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="8539c-147">如果我运行 `wsl`，它会打开 Ubuntu 会话。</span><span class="sxs-lookup"><span data-stu-id="8539c-147">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="8539c-148">取消注册和重新安装分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-148">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="8539c-149">尽管可以通过 Microsoft Store 安装 Linux 分发版，但无法通过 Store 将其卸载。</span><span class="sxs-lookup"><span data-stu-id="8539c-149">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="8539c-150">可以通过 WSL Config 来取消注册/卸载分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-150">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="8539c-151">取消注册后，还可以重新安装分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-151">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="8539c-152">**警告：** 取消注册后，与该分发版关联的所有数据、设置和软件将永久丢失。</span><span class="sxs-lookup"><span data-stu-id="8539c-152">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="8539c-153">从 Store 重新安装会安装分发版的干净副本。</span><span class="sxs-lookup"><span data-stu-id="8539c-153">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wsl --unregister <DistributionName>`  
<span data-ttu-id="8539c-154">从 WSL 中取消注册分发版，以便能够重新安装或清理它。</span><span class="sxs-lookup"><span data-stu-id="8539c-154">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="8539c-155">例如：`wsl --unregister Ubuntu` 将从可用于 WSL 的分发版中删除 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="8539c-155">For example: `wsl --unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="8539c-156">运行 `wsl --list` 时，不再会列出 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="8539c-156">When I run `wsl --list` it will not be listed.</span></span>

<span data-ttu-id="8539c-157">若要重新安装，请在 Microsoft Store 中找到该分发版，然后选择“启动”。</span><span class="sxs-lookup"><span data-stu-id="8539c-157">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

#### <a name="run-as-a-specific-user"></a><span data-ttu-id="8539c-158">以特定用户的身份运行</span><span class="sxs-lookup"><span data-stu-id="8539c-158">Run as a specific user</span></span>

<span data-ttu-id="8539c-159">`wsl -u <Username>`、`wsl --user <Username>`</span><span class="sxs-lookup"><span data-stu-id="8539c-159">`wsl -u <Username>`, `wsl --user <Username>`</span></span>

<span data-ttu-id="8539c-160">以指定用户的身份运行 WSL。</span><span class="sxs-lookup"><span data-stu-id="8539c-160">Run WSL as the specified user.</span></span> <span data-ttu-id="8539c-161">请注意，该用户必须存在于 WSL 分发版中。</span><span class="sxs-lookup"><span data-stu-id="8539c-161">Please note that user must exist inside of the WSL distribution.</span></span>

#### <a name="run-a-specific-distribution"></a><span data-ttu-id="8539c-162">运行特定的分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-162">Run a specific distribution</span></span>

<span data-ttu-id="8539c-163">`wsl -d <DistributionName>`、`wsl --distribution <DistributionName>`</span><span class="sxs-lookup"><span data-stu-id="8539c-163">`wsl -d <DistributionName>`, `wsl --distribution <DistributionName>`</span></span>

<span data-ttu-id="8539c-164">运行 WSL 的指定分发版。可用于将命令发送到特定的分发版，而无需更改默认值。</span><span class="sxs-lookup"><span data-stu-id="8539c-164">Run a specified distribution of WSL, can be used to send commands to a specific distribution without having to change your default.</span></span>

### <a name="versions-earlier-than-windows-10-version-1903"></a><span data-ttu-id="8539c-165">低于 Windows 10 版本 1903 的版本</span><span class="sxs-lookup"><span data-stu-id="8539c-165">Versions Earlier than Windows 10 Version 1903</span></span>

<span data-ttu-id="8539c-166">WSL Config (`wslconfig.exe`) 是一个命令行工具，用于管理在适用于 Linux 的 Windows 子系统 (WSL) 上运行的 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-166">WSL Config (`wslconfig.exe`) is a command-line tool for managing Linux distributions running on the Windows Subsystem for Linux (WSL).</span></span>  <span data-ttu-id="8539c-167">使用该工具可以列出可用分发版、设置默认分发和卸载分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-167">It lets you list available distributions, set a default distribution, and uninstall distributions.</span></span>

<span data-ttu-id="8539c-168">尽管 WSL Config 对于跨越或协调分发版的设置有帮助，但每个 Linux 分发版会独立管理自身的配置。</span><span class="sxs-lookup"><span data-stu-id="8539c-168">While WSL Config is helpful for settings that span or coordinate distributions, each Linux distribution independently manages its own configurations.</span></span>  <span data-ttu-id="8539c-169">若要查看特定于分发版的命令，请运行 `[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="8539c-169">To see distribution-specific commands, run `[distro.exe] /?`.</span></span>  <span data-ttu-id="8539c-170">例如 `ubuntu /?`。</span><span class="sxs-lookup"><span data-stu-id="8539c-170">For example `ubuntu /?`.</span></span>

<span data-ttu-id="8539c-171">若要查看 wslconfig 的所有可用选项，请运行：`wslconfig /?`</span><span class="sxs-lookup"><span data-stu-id="8539c-171">To see all available options for wslconfig, run:  `wslconfig /?`</span></span>

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

#### <a name="list-distributions"></a><span data-ttu-id="8539c-172">列出分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-172">List distributions</span></span>

`wslconfig /list`  
<span data-ttu-id="8539c-173">列出可用于 WSL 的 Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-173">Lists available Linux distributions available to WSL.</span></span>  <span data-ttu-id="8539c-174">如果列出了某个分发版，表示该分发版已安装且可供使用。</span><span class="sxs-lookup"><span data-stu-id="8539c-174">If a distribution is listed, it's installed and ready to use.</span></span>

`wslconfig /list /all`  
<span data-ttu-id="8539c-175">列出所有分发版，包括当前不可用的分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-175">Lists all distributions, including ones that aren't currently usable.</span></span>  <span data-ttu-id="8539c-176">这些分发版可能正在安装、卸载或处于损坏状态。</span><span class="sxs-lookup"><span data-stu-id="8539c-176">They may be in the process of installing, uninstalling, or are in a broken state.</span></span>  

#### <a name="set-a-default-distribution"></a><span data-ttu-id="8539c-177">设置默认分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-177">Set a default distribution</span></span>

<span data-ttu-id="8539c-178">默认 WSL 分布版是在命令行中运行 `wsl` 时运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-178">The default WSL distribution is the one that runs when you run `wsl` on a command line.</span></span>

`wslconfig /setdefault <DistributionName>`

<span data-ttu-id="8539c-179">将默认分发版设置为 `<DistributionName>`。</span><span class="sxs-lookup"><span data-stu-id="8539c-179">Sets the default distribution to `<DistributionName>`.</span></span>

<span data-ttu-id="8539c-180">**示例：**</span><span class="sxs-lookup"><span data-stu-id="8539c-180">**Example:**</span></span>  
<span data-ttu-id="8539c-181">`wslconfig /setdefault Ubuntu` 会将我的默认分发版设置为 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="8539c-181">`wslconfig /setdefault Ubuntu` would set my default distribution to Ubuntu.</span></span>  <span data-ttu-id="8539c-182">现在，当我运行 `wsl npm init` 时，该分发版将在 Ubuntu 中运行。</span><span class="sxs-lookup"><span data-stu-id="8539c-182">Now when I run `wsl npm init` it will run in Ubuntu.</span></span>  <span data-ttu-id="8539c-183">如果我运行 `wsl`，它会打开 Ubuntu 会话。</span><span class="sxs-lookup"><span data-stu-id="8539c-183">If I run `wsl` it will open an Ubuntu session.</span></span>

#### <a name="unregister-and-reinstall-a-distribution"></a><span data-ttu-id="8539c-184">取消注册和重新安装分发版</span><span class="sxs-lookup"><span data-stu-id="8539c-184">Unregister and reinstall a distribution</span></span>

<span data-ttu-id="8539c-185">尽管可以通过 Microsoft Store 安装 Linux 分发版，但无法通过 Store 将其卸载。</span><span class="sxs-lookup"><span data-stu-id="8539c-185">While Linux distributions can be installed through the Microsoft store, they can't be uninstalled through the store.</span></span>  <span data-ttu-id="8539c-186">可以通过 WSL Config 来取消注册/卸载分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-186">WSL Config allows distributions to be unregistered/uninstalled.</span></span>

<span data-ttu-id="8539c-187">取消注册后，还可以重新安装分发版。</span><span class="sxs-lookup"><span data-stu-id="8539c-187">Unregistering also allows distributions to be reinstalled.</span></span>

> <span data-ttu-id="8539c-188">**警告：** 取消注册后，与该分发版关联的所有数据、设置和软件将永久丢失。</span><span class="sxs-lookup"><span data-stu-id="8539c-188">**Caution:** Once unregistered, all data, settings, and software associated with that distribution will be permanently lost.</span></span>  <span data-ttu-id="8539c-189">从 Store 重新安装会安装分发版的干净副本。</span><span class="sxs-lookup"><span data-stu-id="8539c-189">Reinstalling from the store will install a clean copy of the distribution.</span></span>

`wslconfig /unregister <DistributionName>`  
<span data-ttu-id="8539c-190">从 WSL 中取消注册分发版，以便能够重新安装或清理它。</span><span class="sxs-lookup"><span data-stu-id="8539c-190">Unregisters the distribution from WSL so it can be reinstalled or cleaned up.</span></span>

<span data-ttu-id="8539c-191">例如：`wslconfig /unregister Ubuntu` 将从可用于 WSL 的分发版中删除 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="8539c-191">For example: `wslconfig /unregister Ubuntu` would remove Ubuntu from the distributions available in WSL.</span></span>  <span data-ttu-id="8539c-192">运行 `wslconfig /list` 时，不再会列出 Ubuntu。</span><span class="sxs-lookup"><span data-stu-id="8539c-192">When I run `wslconfig /list` it will not be listed.</span></span>

<span data-ttu-id="8539c-193">若要重新安装，请在 Microsoft Store 中找到该分发版，然后选择“启动”。</span><span class="sxs-lookup"><span data-stu-id="8539c-193">To reinstall, find the distribution in the Microsoft store and select "Launch".</span></span>

## <a name="set-wsl-launch-settings"></a><span data-ttu-id="8539c-194">设置 WSL 启动设置</span><span class="sxs-lookup"><span data-stu-id="8539c-194">Set WSL launch settings</span></span>

> <span data-ttu-id="8539c-195">**在 Windows 预览体验成员内部版本 17093 和更高版本中可用**</span><span class="sxs-lookup"><span data-stu-id="8539c-195">**Available in Windows Insider Build 17093 and later**</span></span>

<span data-ttu-id="8539c-196">使用 `wsl.conf` 自动配置 WSL 中每次启动子系统时要应用的某些功能。</span><span class="sxs-lookup"><span data-stu-id="8539c-196">Automatically configure certain functionality in WSL that will be applied every time you launch the subsystem using `wsl.conf`.</span></span> 

<span data-ttu-id="8539c-197">目前，这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="8539c-197">Right now, this includes automount options and network configuration.</span></span>

<span data-ttu-id="8539c-198">`wsl.conf` 位于每个 Linux 分发版的 `/etc/wsl.conf` 中。</span><span class="sxs-lookup"><span data-stu-id="8539c-198">`wsl.conf` is located in each Linux distribution in `/etc/wsl.conf`.</span></span> <span data-ttu-id="8539c-199">如果该文件不存在，你可以自行创建。</span><span class="sxs-lookup"><span data-stu-id="8539c-199">If the file is not there, you can create it yourself.</span></span> <span data-ttu-id="8539c-200">WSL 会检测该文件是否存在，并读取其内容。</span><span class="sxs-lookup"><span data-stu-id="8539c-200">WSL will detect the existence of the file and will read its contents.</span></span> <span data-ttu-id="8539c-201">如果该文件缺失或格式不正确（即，标记格式不正确），WSL 将继续如常启动。</span><span class="sxs-lookup"><span data-stu-id="8539c-201">If the file is missing or malformed (that is, improper markup formatting), WSL will continue to launch as normal.</span></span>

<span data-ttu-id="8539c-202">下面是可以添加到分发版中的示例 `wsl.conf` 文件：</span><span class="sxs-lookup"><span data-stu-id="8539c-202">Here is a sample `wsl.conf` file you could add into your distros:</span></span>

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

### <a name="configuration-options"></a><span data-ttu-id="8539c-203">配置选项</span><span class="sxs-lookup"><span data-stu-id="8539c-203">Configuration Options</span></span>

<span data-ttu-id="8539c-204">为了遵守 .ini 约定，键将在某个节下声明。</span><span class="sxs-lookup"><span data-stu-id="8539c-204">In keeping with .ini conventions, keys are declared under a section.</span></span> 

<span data-ttu-id="8539c-205">WSL 支持两个节：`automount` 和 `network`。</span><span class="sxs-lookup"><span data-stu-id="8539c-205">WSL supports two sections: `automount` and `network`.</span></span>

#### <a name="automount"></a><span data-ttu-id="8539c-206">automount</span><span class="sxs-lookup"><span data-stu-id="8539c-206">automount</span></span>

<span data-ttu-id="8539c-207">节：`[automount]`</span><span class="sxs-lookup"><span data-stu-id="8539c-207">Section: `[automount]`</span></span>


| <span data-ttu-id="8539c-208">键</span><span class="sxs-lookup"><span data-stu-id="8539c-208">key</span></span>        | <span data-ttu-id="8539c-209">value</span><span class="sxs-lookup"><span data-stu-id="8539c-209">value</span></span>                          | <span data-ttu-id="8539c-210">default</span><span class="sxs-lookup"><span data-stu-id="8539c-210">default</span></span>      | <span data-ttu-id="8539c-211">备注</span><span class="sxs-lookup"><span data-stu-id="8539c-211">notes</span></span>                                                                                                                                                                                                                                                                                                                          |
|:-----------|:-------------------------------|:-------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8539c-212">已启用</span><span class="sxs-lookup"><span data-stu-id="8539c-212">enabled</span></span>    | <span data-ttu-id="8539c-213">布尔值</span><span class="sxs-lookup"><span data-stu-id="8539c-213">boolean</span></span>                        | <span data-ttu-id="8539c-214">true</span><span class="sxs-lookup"><span data-stu-id="8539c-214">true</span></span>         | <span data-ttu-id="8539c-215">`true` 导致固定驱动器（即</span><span class="sxs-lookup"><span data-stu-id="8539c-215">`true` causes fixed drives (i.e</span></span> <span data-ttu-id="8539c-216">`C:/` 或 `D:/`）自动装载到 DrvFs 中的 `/mnt` 下。</span><span class="sxs-lookup"><span data-stu-id="8539c-216">`C:/` or `D:/`) to be automatically mounted with DrvFs under `/mnt`.</span></span>  <span data-ttu-id="8539c-217">`false` 表示驱动器不会自动装载，但你仍可以手动或通过 `fstab` 装载驱动器。</span><span class="sxs-lookup"><span data-stu-id="8539c-217">`false` means drives won’t be mounted automatically, but you could still mount them manually or via `fstab`.</span></span>                                                                                                             |
| <span data-ttu-id="8539c-218">mountFsTab</span><span class="sxs-lookup"><span data-stu-id="8539c-218">mountFsTab</span></span> | <span data-ttu-id="8539c-219">布尔值</span><span class="sxs-lookup"><span data-stu-id="8539c-219">boolean</span></span>                        | <span data-ttu-id="8539c-220">true</span><span class="sxs-lookup"><span data-stu-id="8539c-220">true</span></span>         | <span data-ttu-id="8539c-221">`true` 设置启动 WSL 时要处理的 `/etc/fstab`。</span><span class="sxs-lookup"><span data-stu-id="8539c-221">`true` sets `/etc/fstab` to be processed on WSL start.</span></span> <span data-ttu-id="8539c-222">/etc/fstab 是可在其中声明其他文件系统的文件，类似于 SMB 共享。</span><span class="sxs-lookup"><span data-stu-id="8539c-222">/etc/fstab is a file where you can declare other filesystems, like an SMB share.</span></span> <span data-ttu-id="8539c-223">因此，在启动时，可以在 WSL 中自动装载这些文件系统。</span><span class="sxs-lookup"><span data-stu-id="8539c-223">Thus, you can mount these filesystems automatically in WSL on start up.</span></span>                                                                                                                |
| <span data-ttu-id="8539c-224">root</span><span class="sxs-lookup"><span data-stu-id="8539c-224">root</span></span>       | <span data-ttu-id="8539c-225">字符串</span><span class="sxs-lookup"><span data-stu-id="8539c-225">String</span></span>                         | `/mnt/`      | <span data-ttu-id="8539c-226">设置固定驱动器要自动装载到的目录。</span><span class="sxs-lookup"><span data-stu-id="8539c-226">Sets the directory where fixed drives will be automatically mounted.</span></span> <span data-ttu-id="8539c-227">例如，如果 WSL 中的某个目录位于 `/windir/`，而你将该目录指定为根目录，则固定驱动器预期会装载到 `/windir/c`</span><span class="sxs-lookup"><span data-stu-id="8539c-227">For example, if you have a directory in WSL at `/windir/` and you specify that as the root, you would expect to see your fixed drives mounted at `/windir/c`</span></span>                                                                                              |
| <span data-ttu-id="8539c-228">选项</span><span class="sxs-lookup"><span data-stu-id="8539c-228">options</span></span>    | <span data-ttu-id="8539c-229">逗号分隔值列表</span><span class="sxs-lookup"><span data-stu-id="8539c-229">comma-separated list of values</span></span> | <span data-ttu-id="8539c-230">空字符串</span><span class="sxs-lookup"><span data-stu-id="8539c-230">empty string</span></span> | <span data-ttu-id="8539c-231">此值将追加到默认的 DrvFs 装载选项字符串。</span><span class="sxs-lookup"><span data-stu-id="8539c-231">This value is appended to the default DrvFs mount options string.</span></span> <span data-ttu-id="8539c-232">**只能指定特定于 DrvFs 的选项。**</span><span class="sxs-lookup"><span data-stu-id="8539c-232">**Only DrvFs-specific options can be specified.**</span></span> <span data-ttu-id="8539c-233">通常由装载二进制文件分析成标志的选项不受支持。</span><span class="sxs-lookup"><span data-stu-id="8539c-233">Options that the mount binary would normally parse into a flag are not supported.</span></span> <span data-ttu-id="8539c-234">若要显式指定这些选项，必须在 /etc/fstab 中包含要对其执行此操作的每个驱动器。</span><span class="sxs-lookup"><span data-stu-id="8539c-234">If you want to explicitly specify those options, you must include every drive for which you want to do so in /etc/fstab.</span></span> |

<span data-ttu-id="8539c-235">默认情况下，WSL 会将 uid 和 gid 设置为默认用户的值（在 Ubuntu 分发版中，默认用户是使用 uid=1000,gid=1000 创建的）。</span><span class="sxs-lookup"><span data-stu-id="8539c-235">By default, WSL sets the uid and gid to the value of the default user (in Ubuntu distro, the default user is created with uid=1000,gid=1000).</span></span> <span data-ttu-id="8539c-236">如果用户通过此键显式指定了 gid 或 uid 选项，将覆盖关联的值。</span><span class="sxs-lookup"><span data-stu-id="8539c-236">If the user specifies a gid or uid option explicitly via this key, the associated value will be overwritten.</span></span> <span data-ttu-id="8539c-237">否则，将始终追加默认值。</span><span class="sxs-lookup"><span data-stu-id="8539c-237">Otherwise, the default value will always be appended.</span></span>

<span data-ttu-id="8539c-238">**注意：** 对于所有自动装载的驱动器，这些选项将应用为装载选项。</span><span class="sxs-lookup"><span data-stu-id="8539c-238">**Note:** These options are applied as the mount options for all automatically mounted drives.</span></span> <span data-ttu-id="8539c-239">如果只想更改特定驱动器的选项，请改用 /etc/fstab。</span><span class="sxs-lookup"><span data-stu-id="8539c-239">To change the options for a specific drive only, use /etc/fstab instead.</span></span>

##### <a name="mount-options"></a><span data-ttu-id="8539c-240">装载选项</span><span class="sxs-lookup"><span data-stu-id="8539c-240">Mount options</span></span>

<span data-ttu-id="8539c-241">为 Windows 驱动器 (DrvFs) 设置不同的装载选项可以控制为 Windows 文件计算文件权限的方式。</span><span class="sxs-lookup"><span data-stu-id="8539c-241">Setting different mount options for Windows drives (DrvFs) can control how file permissions are calculated for Windows files.</span></span> <span data-ttu-id="8539c-242">你可使用以下选项：</span><span class="sxs-lookup"><span data-stu-id="8539c-242">The following options are available:</span></span>

| <span data-ttu-id="8539c-243">键</span><span class="sxs-lookup"><span data-stu-id="8539c-243">Key</span></span> | <span data-ttu-id="8539c-244">描述</span><span class="sxs-lookup"><span data-stu-id="8539c-244">Description</span></span> | <span data-ttu-id="8539c-245">默认</span><span class="sxs-lookup"><span data-stu-id="8539c-245">Default</span></span> |
|:----|:----|:----|
|<span data-ttu-id="8539c-246">uid</span><span class="sxs-lookup"><span data-stu-id="8539c-246">uid</span></span>| <span data-ttu-id="8539c-247">用于所有文件的所有者的用户 ID</span><span class="sxs-lookup"><span data-stu-id="8539c-247">The User ID used for the owner of all files</span></span> | <span data-ttu-id="8539c-248">WSL 发行版的默认用户 ID（第一次安装时，此项默认为 1000）</span><span class="sxs-lookup"><span data-stu-id="8539c-248">The default User ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="8539c-249">gid</span><span class="sxs-lookup"><span data-stu-id="8539c-249">gid</span></span>| <span data-ttu-id="8539c-250">用于所有文件的所有者的组 ID</span><span class="sxs-lookup"><span data-stu-id="8539c-250">The Group ID used for the owner of all files</span></span> | <span data-ttu-id="8539c-251">WSL 发行版的默认组 ID（第一次安装时，此项默认为 1000）</span><span class="sxs-lookup"><span data-stu-id="8539c-251">The default group ID of your WSL distro (On first installation this defaults to 1000)</span></span>
|<span data-ttu-id="8539c-252">umask</span><span class="sxs-lookup"><span data-stu-id="8539c-252">umask</span></span> | <span data-ttu-id="8539c-253">要对所有文件和目录排除的权限的八进制掩码</span><span class="sxs-lookup"><span data-stu-id="8539c-253">An octal mask of permissions to exclude for all files and directories</span></span> | <span data-ttu-id="8539c-254">000</span><span class="sxs-lookup"><span data-stu-id="8539c-254">000</span></span>
|<span data-ttu-id="8539c-255">fmask</span><span class="sxs-lookup"><span data-stu-id="8539c-255">fmask</span></span> | <span data-ttu-id="8539c-256">要对所有文件排除的权限的八进制掩码</span><span class="sxs-lookup"><span data-stu-id="8539c-256">An octal mask of permissions to exclude for all files</span></span> | <span data-ttu-id="8539c-257">000</span><span class="sxs-lookup"><span data-stu-id="8539c-257">000</span></span>
|<span data-ttu-id="8539c-258">dmask</span><span class="sxs-lookup"><span data-stu-id="8539c-258">dmask</span></span> | <span data-ttu-id="8539c-259">要对所有目录排除的权限的八进制掩码</span><span class="sxs-lookup"><span data-stu-id="8539c-259">An octal mask of permissions to exclude for all directories</span></span> | <span data-ttu-id="8539c-260">000</span><span class="sxs-lookup"><span data-stu-id="8539c-260">000</span></span>

<span data-ttu-id="8539c-261">**注意：** 权限掩码在应用到文件或目录之前通过一个逻辑或操作进行设置。</span><span class="sxs-lookup"><span data-stu-id="8539c-261">**Note:** The permission masks are put through a logical OR operation before being applied to files or directories.</span></span> 

#### <a name="network"></a><span data-ttu-id="8539c-262">网络</span><span class="sxs-lookup"><span data-stu-id="8539c-262">network</span></span>

<span data-ttu-id="8539c-263">节标签：`[network]`</span><span class="sxs-lookup"><span data-stu-id="8539c-263">Section label: `[network]`</span></span>

| <span data-ttu-id="8539c-264">键</span><span class="sxs-lookup"><span data-stu-id="8539c-264">key</span></span> | <span data-ttu-id="8539c-265">value</span><span class="sxs-lookup"><span data-stu-id="8539c-265">value</span></span> | <span data-ttu-id="8539c-266">default</span><span class="sxs-lookup"><span data-stu-id="8539c-266">default</span></span> | <span data-ttu-id="8539c-267">备注</span><span class="sxs-lookup"><span data-stu-id="8539c-267">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="8539c-268">generateHosts</span><span class="sxs-lookup"><span data-stu-id="8539c-268">generateHosts</span></span> | <span data-ttu-id="8539c-269">布尔值</span><span class="sxs-lookup"><span data-stu-id="8539c-269">boolean</span></span> | `true` | <span data-ttu-id="8539c-270">`true` 将 WSL 设置为生成 `/etc/hosts`。</span><span class="sxs-lookup"><span data-stu-id="8539c-270">`true` sets WSL to generate `/etc/hosts`.</span></span> <span data-ttu-id="8539c-271">`hosts` 文件包含主机名对应的 IP 地址的静态映射。</span><span class="sxs-lookup"><span data-stu-id="8539c-271">The `hosts` file contains a static map of hostnames corresponding IP address.</span></span> |
| <span data-ttu-id="8539c-272">generateResolvConf</span><span class="sxs-lookup"><span data-stu-id="8539c-272">generateResolvConf</span></span> | <span data-ttu-id="8539c-273">布尔值</span><span class="sxs-lookup"><span data-stu-id="8539c-273">boolean</span></span> | `true` | <span data-ttu-id="8539c-274">`true` 将 WSL 设置为生成 `/etc/resolv.conf`。</span><span class="sxs-lookup"><span data-stu-id="8539c-274">`true` set WSL to generate `/etc/resolv.conf`.</span></span> <span data-ttu-id="8539c-275">`resolv.conf` 包含能够将给定主机名解析为其 IP 地址的 DNS 列表。</span><span class="sxs-lookup"><span data-stu-id="8539c-275">The `resolv.conf` contains a DNS list that are capable of resolving a given hostname to its IP address.</span></span> | 

#### <a name="interop"></a><span data-ttu-id="8539c-276">interop</span><span class="sxs-lookup"><span data-stu-id="8539c-276">interop</span></span>

<span data-ttu-id="8539c-277">节标签：`[interop]`</span><span class="sxs-lookup"><span data-stu-id="8539c-277">Section label: `[interop]`</span></span>

<span data-ttu-id="8539c-278">这些选项在预览体验成员内部版本 17713 和更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="8539c-278">These options are available in Insider Build 17713 and later.</span></span>

| <span data-ttu-id="8539c-279">键</span><span class="sxs-lookup"><span data-stu-id="8539c-279">key</span></span> | <span data-ttu-id="8539c-280">value</span><span class="sxs-lookup"><span data-stu-id="8539c-280">value</span></span> | <span data-ttu-id="8539c-281">default</span><span class="sxs-lookup"><span data-stu-id="8539c-281">default</span></span> | <span data-ttu-id="8539c-282">备注</span><span class="sxs-lookup"><span data-stu-id="8539c-282">notes</span></span>|
|:----|:----|:----|:----|
| <span data-ttu-id="8539c-283">已启用</span><span class="sxs-lookup"><span data-stu-id="8539c-283">enabled</span></span> | <span data-ttu-id="8539c-284">布尔值</span><span class="sxs-lookup"><span data-stu-id="8539c-284">boolean</span></span> | `true` | <span data-ttu-id="8539c-285">设置此键可确定 WSL 是否支持启动 Windows 进程。</span><span class="sxs-lookup"><span data-stu-id="8539c-285">Setting this key will determine whether WSL will support launching Windows processes.</span></span> |
| <span data-ttu-id="8539c-286">appendWindowsPath</span><span class="sxs-lookup"><span data-stu-id="8539c-286">appendWindowsPath</span></span> | <span data-ttu-id="8539c-287">布尔值</span><span class="sxs-lookup"><span data-stu-id="8539c-287">boolean</span></span> | `true` | <span data-ttu-id="8539c-288">设置此键可确定 WSL 是否会将 Windows 路径元素添加到 $PATH 环境变量。</span><span class="sxs-lookup"><span data-stu-id="8539c-288">Setting this key will determine whether WSL will add Windows path elements to the $PATH environment variable.</span></span> | 
