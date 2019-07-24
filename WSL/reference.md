---
title: 适用于 Linux 的 Windows 子系统命令参考
description: 管理适用于 Linux 的 Windows 子系统的命令列表
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307657"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="ec728-104">适用于 Linux 的 Windows 子系统的命令参考</span><span class="sxs-lookup"><span data-stu-id="ec728-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="ec728-105">与适用于 Linux 的 Windows 子系统交互的最佳方式是使用`wsl.exe`命令。</span><span class="sxs-lookup"><span data-stu-id="ec728-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 

## `wsl.exe` 

<span data-ttu-id="ec728-106">下面是在使用 Windows 版本1903时使用`wsl.exe`的所有选项的列表。</span><span class="sxs-lookup"><span data-stu-id="ec728-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

* <span data-ttu-id="ec728-107">用于运行 Linux 二进制文件的参数:</span><span class="sxs-lookup"><span data-stu-id="ec728-107">Arguments for running Linux binaries:</span></span>

    * <span data-ttu-id="ec728-108">如果未提供命令行, wsl 将启动默认 shell。</span><span class="sxs-lookup"><span data-stu-id="ec728-108">If no command line is provided, wsl.exe launches the default shell.</span></span>

    * <span data-ttu-id="ec728-109">--exec,-e<CommandLine></span><span class="sxs-lookup"><span data-stu-id="ec728-109">--exec, -e <CommandLine></span></span>
        * <span data-ttu-id="ec728-110">执行指定的命令, 而不使用默认的 Linux shell。</span><span class="sxs-lookup"><span data-stu-id="ec728-110">Execute the specified command without using the default Linux shell.</span></span>

    * --
        * <span data-ttu-id="ec728-111">按原样传递剩余的命令行。</span><span class="sxs-lookup"><span data-stu-id="ec728-111">Pass the remaining command line as is.</span></span>

* <span data-ttu-id="ec728-112">选项：</span><span class="sxs-lookup"><span data-stu-id="ec728-112">Options:</span></span>
    * <span data-ttu-id="ec728-113">--分发,-d<Distro></span><span class="sxs-lookup"><span data-stu-id="ec728-113">--distribution, -d <Distro></span></span>
        * <span data-ttu-id="ec728-114">运行指定的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-114">Run the specified distribution.</span></span>

    * <span data-ttu-id="ec728-115">--user,-u<UserName></span><span class="sxs-lookup"><span data-stu-id="ec728-115">--user, -u <UserName></span></span>
        * <span data-ttu-id="ec728-116">以指定用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="ec728-116">Run as the specified user.</span></span>

* <span data-ttu-id="ec728-117">用于管理适用于 Linux 的 Windows 子系统的参数:</span><span class="sxs-lookup"><span data-stu-id="ec728-117">Arguments for managing Windows Subsystem for Linux:</span></span>

    * <span data-ttu-id="ec728-118">--export <Distro><FileName></span><span class="sxs-lookup"><span data-stu-id="ec728-118">--export <Distro> <FileName></span></span>
        * <span data-ttu-id="ec728-119">将分发导出到 tar 文件。</span><span class="sxs-lookup"><span data-stu-id="ec728-119">Exports the distribution to a tar file.</span></span>
        <span data-ttu-id="ec728-120">文件名可以是-标准输出。</span><span class="sxs-lookup"><span data-stu-id="ec728-120">The filename can be - for standard output.</span></span>

    * <span data-ttu-id="ec728-121">--import <Distro> <InstallLocation>[Options <FileName> ]</span><span class="sxs-lookup"><span data-stu-id="ec728-121">--import <Distro> <InstallLocation> <FileName> [Options]</span></span>
        * <span data-ttu-id="ec728-122">导入指定的 tar 文件作为新的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-122">Imports the specified tar file as a new distribution.</span></span>
        <span data-ttu-id="ec728-123">文件名可以是-标准输入。</span><span class="sxs-lookup"><span data-stu-id="ec728-123">The filename can be - for standard input.</span></span>

        * <span data-ttu-id="ec728-124">选项：</span><span class="sxs-lookup"><span data-stu-id="ec728-124">Options:</span></span>
            * <span data-ttu-id="ec728-125">--version <Version>指定要用于新分发的版本。</span><span class="sxs-lookup"><span data-stu-id="ec728-125">--version <Version> Specifies the version to use for the new distribution.</span></span>

    * <span data-ttu-id="ec728-126">--list,-l [Options]</span><span class="sxs-lookup"><span data-stu-id="ec728-126">--list, -l [Options]</span></span>
        * <span data-ttu-id="ec728-127">列出分布。</span><span class="sxs-lookup"><span data-stu-id="ec728-127">Lists distributions.</span></span>

        * <span data-ttu-id="ec728-128">选项：</span><span class="sxs-lookup"><span data-stu-id="ec728-128">Options:</span></span>
            * <span data-ttu-id="ec728-129">--all</span><span class="sxs-lookup"><span data-stu-id="ec728-129">--all</span></span>
                * <span data-ttu-id="ec728-130">列出所有分发, 包括当前正在安装或卸载的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

            * <span data-ttu-id="ec728-131">--正在运行</span><span class="sxs-lookup"><span data-stu-id="ec728-131">--running</span></span>
                * <span data-ttu-id="ec728-132">仅列出当前正在运行的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-132">List only distributions that are currently running.</span></span>

    * <span data-ttu-id="ec728-133">--set-默认值,-s<Distro></span><span class="sxs-lookup"><span data-stu-id="ec728-133">--set-default, -s <Distro></span></span>
        * <span data-ttu-id="ec728-134">将分布设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="ec728-134">Sets the distribution as the default.</span></span>

    * <span data-ttu-id="ec728-135">--set-默认-版本<Version></span><span class="sxs-lookup"><span data-stu-id="ec728-135">--set-default-version <Version></span></span>
        * <span data-ttu-id="ec728-136">更改新分发版的默认安装版本。</span><span class="sxs-lookup"><span data-stu-id="ec728-136">Changes the default install version for new distributions.</span></span>

    * <span data-ttu-id="ec728-137">--set-版本<Distro><Version></span><span class="sxs-lookup"><span data-stu-id="ec728-137">--set-version <Distro> <Version></span></span>
        * <span data-ttu-id="ec728-138">更改指定分发的版本。</span><span class="sxs-lookup"><span data-stu-id="ec728-138">Changes the version of the specified distribution.</span></span>

    * <span data-ttu-id="ec728-139">--terminate,-t<Distro></span><span class="sxs-lookup"><span data-stu-id="ec728-139">--terminate, -t <Distro></span></span>
        * <span data-ttu-id="ec728-140">终止指定的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-140">Terminates the specified distribution.</span></span>

    * <span data-ttu-id="ec728-141">--取消注册<Distro></span><span class="sxs-lookup"><span data-stu-id="ec728-141">--unregister <Distro></span></span>
        * <span data-ttu-id="ec728-142">注销分布。</span><span class="sxs-lookup"><span data-stu-id="ec728-142">Unregisters the distribution.</span></span>

    * <span data-ttu-id="ec728-143">--help</span><span class="sxs-lookup"><span data-stu-id="ec728-143">--help</span></span>
        * <span data-ttu-id="ec728-144">显示用法信息。</span><span class="sxs-lookup"><span data-stu-id="ec728-144">Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="ec728-145">其他命令</span><span class="sxs-lookup"><span data-stu-id="ec728-145">Additional Commands</span></span>

<span data-ttu-id="ec728-146">还有历史命令可与适用于 Linux 的 Windows 子系统交互。</span><span class="sxs-lookup"><span data-stu-id="ec728-146">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="ec728-147">它们的功能包含在`wsl.exe`中, 但仍可供使用。</span><span class="sxs-lookup"><span data-stu-id="ec728-147">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="ec728-148">此命令可让你配置 WSL 分布。</span><span class="sxs-lookup"><span data-stu-id="ec728-148">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="ec728-149">下面是其选项的列表。</span><span class="sxs-lookup"><span data-stu-id="ec728-149">Below is a list of its options.</span></span>

* <span data-ttu-id="ec728-150">/l,/list [选项]</span><span class="sxs-lookup"><span data-stu-id="ec728-150">/l, /list [Option]</span></span>
    * <span data-ttu-id="ec728-151">列出已注册的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-151">Lists registered distributions.</span></span>
        * <span data-ttu-id="ec728-152">/all-(可选) 列出所有分发, 包括当前正在安装或卸载的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-152">/all - Optionally list all distributions, including distributions that       are currently being installed or uninstalled.</span></span>

        * <span data-ttu-id="ec728-153">/running-仅列出当前正在运行的分发。</span><span class="sxs-lookup"><span data-stu-id="ec728-153">/running - List only distributions that are currently running.</span></span>

* <span data-ttu-id="ec728-154">/s、/setdefault<DistributionName></span><span class="sxs-lookup"><span data-stu-id="ec728-154">/s, /setdefault <DistributionName></span></span>
    * <span data-ttu-id="ec728-155">将分布设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="ec728-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="ec728-156">/t、/terminate<DistributionName></span><span class="sxs-lookup"><span data-stu-id="ec728-156">/t, /terminate <DistributionName></span></span>
    * <span data-ttu-id="ec728-157">终止分布。</span><span class="sxs-lookup"><span data-stu-id="ec728-157">Terminates the distribution.</span></span>

* <span data-ttu-id="ec728-158">/u,/unregister<DistributionName></span><span class="sxs-lookup"><span data-stu-id="ec728-158">/u, /unregister <DistributionName></span></span>
    * <span data-ttu-id="ec728-159">注销分布。</span><span class="sxs-lookup"><span data-stu-id="ec728-159">Unregisters the distribution.</span></span>

### `bash.exe`

<span data-ttu-id="ec728-160">此命令用于启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="ec728-160">This command is used to start a bash shell.</span></span> <span data-ttu-id="ec728-161">下面是可用于此命令的选项。</span><span class="sxs-lookup"><span data-stu-id="ec728-161">Below are the options you can use with this command.</span></span>

* <span data-ttu-id="ec728-162">未给定选项</span><span class="sxs-lookup"><span data-stu-id="ec728-162">No Option given</span></span>
    * <span data-ttu-id="ec728-163">在当前目录中启动 Bash shell。</span><span class="sxs-lookup"><span data-stu-id="ec728-163">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="ec728-164">如果未自动安装 Bash shell, 则运行`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="ec728-164">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* <span data-ttu-id="ec728-165">bash ~</span><span class="sxs-lookup"><span data-stu-id="ec728-165">bash ~</span></span>
    * <span data-ttu-id="ec728-166">在用户的主目录中启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="ec728-166">Launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="ec728-167">类似于运行`cd ~`。</span><span class="sxs-lookup"><span data-stu-id="ec728-167">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="ec728-168">bash-c "&lt;command&gt;"</span><span class="sxs-lookup"><span data-stu-id="ec728-168">bash -c "&lt;command&gt;"</span></span>
    * <span data-ttu-id="ec728-169">运行命令, 打印输出并退出到 Windows 命令提示符。</span><span class="sxs-lookup"><span data-stu-id="ec728-169">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="ec728-170">实例`bash -c "ls"`</span><span class="sxs-lookup"><span data-stu-id="ec728-170">Example:  `bash -c "ls"`</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="ec728-171">弃用的命令</span><span class="sxs-lookup"><span data-stu-id="ec728-171">Deprecated Commands</span></span>

<span data-ttu-id="ec728-172">`lxrun.exe`是用于安装和管理适用于 Linux 的 Windows 子系统的第一个命令。</span><span class="sxs-lookup"><span data-stu-id="ec728-172">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="ec728-173">它在 Windows 10 1803 和更高版本中已弃用。</span><span class="sxs-lookup"><span data-stu-id="ec728-173">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="ec728-174">命令`lxrun.exe`可用于直接与适用于 Linux 的[Windows 子系统 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)交互。</span><span class="sxs-lookup"><span data-stu-id="ec728-174">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="ec728-175">这些命令安装`\Windows\System32`在目录中, 可以在 Windows 命令提示符下或在 PowerShell 中运行。</span><span class="sxs-lookup"><span data-stu-id="ec728-175">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="ec728-176">Command</span><span class="sxs-lookup"><span data-stu-id="ec728-176">Command</span></span>                     | <span data-ttu-id="ec728-177">描述</span><span class="sxs-lookup"><span data-stu-id="ec728-177">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="ec728-178">Lxrun 命令用于管理 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="ec728-178">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="ec728-179">开始下载和安装过程。</span><span class="sxs-lookup"><span data-stu-id="ec728-179">Starts the download and install process.</span></span> <br/> <span data-ttu-id="ec728-180">可以添加 **/y**来绕过所有提示。</span><span class="sxs-lookup"><span data-stu-id="ec728-180">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="ec728-181">系统会自动接受确认提示, 并将 "默认用户" 设置为 "root"。</span><span class="sxs-lookup"><span data-stu-id="ec728-181">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="ec728-182">卸载并删除 Ubuntu 映像。</span><span class="sxs-lookup"><span data-stu-id="ec728-182">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="ec728-183">默认情况下, 这不会删除用户的 Ubuntu 主目录。</span><span class="sxs-lookup"><span data-stu-id="ec728-183">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="ec728-184">可以添加 **/y**来自动接受确认提示</span><span class="sxs-lookup"><span data-stu-id="ec728-184">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="ec728-185">**/full**卸载并删除用户的 Ubuntu 主目录</span><span class="sxs-lookup"><span data-stu-id="ec728-185">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="ec728-186">设置 Ubuntu 用户上的默认 Bash。</span><span class="sxs-lookup"><span data-stu-id="ec728-186">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="ec728-187">如果指定的用户不存在, 将提示输入密码。</span><span class="sxs-lookup"><span data-stu-id="ec728-187">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="ec728-188">有关详细信息, 请 https://aka.ms/wslusers 访问:。</span><span class="sxs-lookup"><span data-stu-id="ec728-188">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="ec728-189">**/y**绕过密码的 promping。</span><span class="sxs-lookup"><span data-stu-id="ec728-189">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="ec728-190">将创建不带密码的用户。</span><span class="sxs-lookup"><span data-stu-id="ec728-190">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="ec728-191">更新子系统的包索引</span><span class="sxs-lookup"><span data-stu-id="ec728-191">Updates the subsystem's package index</span></span>          |
