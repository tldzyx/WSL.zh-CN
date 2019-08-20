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
ms.openlocfilehash: 018b02b43e859476f7ee38f54df8efa0ca0e652b
ms.sourcegitcommit: 62c49d435a91f2e390c3c495f3e09e62b5ada13c
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2019
ms.locfileid: "69578838"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="3f551-104">适用于 Linux 的 Windows 子系统的命令参考</span><span class="sxs-lookup"><span data-stu-id="3f551-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="3f551-105">与适用于 Linux 的 Windows 子系统交互的最佳方式是使用`wsl.exe`命令。</span><span class="sxs-lookup"><span data-stu-id="3f551-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="3f551-106">下面是在使用 Windows 版本1903时使用`wsl.exe`的所有选项的列表。</span><span class="sxs-lookup"><span data-stu-id="3f551-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="3f551-107">利用`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="3f551-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="3f551-108">用于运行 Linux 二进制文件的参数</span><span class="sxs-lookup"><span data-stu-id="3f551-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="3f551-109">**不带参数**</span><span class="sxs-lookup"><span data-stu-id="3f551-109">**Without arguments**</span></span>

  <span data-ttu-id="3f551-110">如果未提供命令行, wsl 将启动默认 shell。</span><span class="sxs-lookup"><span data-stu-id="3f551-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="3f551-111">**--exec,-e \<命令行 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="3f551-112">执行指定的命令, 而不使用默认的 Linux shell。</span><span class="sxs-lookup"><span data-stu-id="3f551-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="3f551-113">按原样传递剩余的命令行。</span><span class="sxs-lookup"><span data-stu-id="3f551-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="3f551-114">上述命令也接受以下选项:</span><span class="sxs-lookup"><span data-stu-id="3f551-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="3f551-115">**--分发,-d \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="3f551-116">运行指定的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-116">Run the specified distribution.</span></span>

* <span data-ttu-id="3f551-117">**--user,-u \<UserName >**</span><span class="sxs-lookup"><span data-stu-id="3f551-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="3f551-118">以指定用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="3f551-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="3f551-119">用于管理适用于 Linux 的 Windows 子系统的参数</span><span class="sxs-lookup"><span data-stu-id="3f551-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="3f551-120">**--export \<发行版 > \<FileName >**</span><span class="sxs-lookup"><span data-stu-id="3f551-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="3f551-121">将分发导出到 tar 文件。</span><span class="sxs-lookup"><span data-stu-id="3f551-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="3f551-122">文件名可以是-标准输出。</span><span class="sxs-lookup"><span data-stu-id="3f551-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="3f551-123">**--import \<发行版 > \<InstallLocation > \<FileName >**</span><span class="sxs-lookup"><span data-stu-id="3f551-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="3f551-124">导入指定的 tar 文件作为新的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="3f551-125">文件名可以是-标准输入。</span><span class="sxs-lookup"><span data-stu-id="3f551-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="3f551-126">**--list,-l [Options]**</span><span class="sxs-lookup"><span data-stu-id="3f551-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="3f551-127">列出分布。</span><span class="sxs-lookup"><span data-stu-id="3f551-127">Lists distributions.</span></span>

  <span data-ttu-id="3f551-128">选项：</span><span class="sxs-lookup"><span data-stu-id="3f551-128">Options:</span></span>
  * <span data-ttu-id="3f551-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="3f551-129">**--all**</span></span>
      
    <span data-ttu-id="3f551-130">列出所有分发, 包括当前正在安装或卸载的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="3f551-131">**--正在运行**</span><span class="sxs-lookup"><span data-stu-id="3f551-131">**--running**</span></span>
      
    <span data-ttu-id="3f551-132">仅列出当前正在运行的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="3f551-133">**--set-default、-s \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-134">将分布设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="3f551-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="3f551-135">**--terminate,-t \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-136">终止指定的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="3f551-137">**--取消\<注册发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-138">注销分布。</span><span class="sxs-lookup"><span data-stu-id="3f551-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="3f551-139">**--帮助**显示用法信息。</span><span class="sxs-lookup"><span data-stu-id="3f551-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="3f551-140">其他命令</span><span class="sxs-lookup"><span data-stu-id="3f551-140">Additional Commands</span></span>

<span data-ttu-id="3f551-141">还有历史命令可与适用于 Linux 的 Windows 子系统交互。</span><span class="sxs-lookup"><span data-stu-id="3f551-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="3f551-142">它们的功能包含在`wsl.exe`中, 但仍可供使用。</span><span class="sxs-lookup"><span data-stu-id="3f551-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="3f551-143">此命令可让你配置 WSL 分布。</span><span class="sxs-lookup"><span data-stu-id="3f551-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="3f551-144">下面是其选项的列表。</span><span class="sxs-lookup"><span data-stu-id="3f551-144">Below is a list of its options.</span></span>

<span data-ttu-id="3f551-145">利用`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="3f551-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="3f551-146">参数</span><span class="sxs-lookup"><span data-stu-id="3f551-146">Arguments</span></span>
* <span data-ttu-id="3f551-147">**/l,/list [选项]**</span><span class="sxs-lookup"><span data-stu-id="3f551-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="3f551-148">列出已注册的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="3f551-149">选项：</span><span class="sxs-lookup"><span data-stu-id="3f551-149">Options:</span></span>
    * <span data-ttu-id="3f551-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="3f551-150">**/all**</span></span>
    
      <span data-ttu-id="3f551-151">根据需要列出所有分发, 包括当前正在安装或卸载的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="3f551-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="3f551-152">**/running**</span></span>
      
      <span data-ttu-id="3f551-153">仅列出当前正在运行的分发。</span><span class="sxs-lookup"><span data-stu-id="3f551-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="3f551-154">**/s、/setdefault \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-155">将分布设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="3f551-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="3f551-156">**/t、/terminate \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-157">终止分布。</span><span class="sxs-lookup"><span data-stu-id="3f551-157">Terminates the distribution.</span></span>

* <span data-ttu-id="3f551-158">**/u,/unregister \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-159">注销分布。</span><span class="sxs-lookup"><span data-stu-id="3f551-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="3f551-160">**/upgrade \<发行版 >**</span><span class="sxs-lookup"><span data-stu-id="3f551-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="3f551-161">将分发升级到 WslFs 文件系统格式。</span><span class="sxs-lookup"><span data-stu-id="3f551-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="3f551-162">此命令用于启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="3f551-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="3f551-163">下面是可用于此命令的选项。</span><span class="sxs-lookup"><span data-stu-id="3f551-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="3f551-164">利用`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="3f551-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="3f551-165">**未给定选项**</span><span class="sxs-lookup"><span data-stu-id="3f551-165">**No Option given**</span></span>
  
  <span data-ttu-id="3f551-166">在当前目录中启动 Bash shell。</span><span class="sxs-lookup"><span data-stu-id="3f551-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="3f551-167">如果未自动安装 Bash shell, 则运行`lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="3f551-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="3f551-168">`bash ~`在用户的主目录中启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="3f551-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="3f551-169">类似于运行`cd ~`。</span><span class="sxs-lookup"><span data-stu-id="3f551-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="3f551-170">**-c "\<command >"**</span><span class="sxs-lookup"><span data-stu-id="3f551-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="3f551-171">运行命令, 打印输出并退出到 Windows 命令提示符。</span><span class="sxs-lookup"><span data-stu-id="3f551-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="3f551-172">示例: `bash -c "ls"`。</span><span class="sxs-lookup"><span data-stu-id="3f551-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="3f551-173">弃用的命令</span><span class="sxs-lookup"><span data-stu-id="3f551-173">Deprecated Commands</span></span>

<span data-ttu-id="3f551-174">`lxrun.exe`是用于安装和管理适用于 Linux 的 Windows 子系统的第一个命令。</span><span class="sxs-lookup"><span data-stu-id="3f551-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="3f551-175">它在 Windows 10 1803 和更高版本中已弃用。</span><span class="sxs-lookup"><span data-stu-id="3f551-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="3f551-176">命令`lxrun.exe`可用于直接与适用于 Linux 的[Windows 子系统 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)交互。</span><span class="sxs-lookup"><span data-stu-id="3f551-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="3f551-177">这些命令安装`\Windows\System32`在目录中, 可以在 Windows 命令提示符下或在 PowerShell 中运行。</span><span class="sxs-lookup"><span data-stu-id="3f551-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="3f551-178">Command</span><span class="sxs-lookup"><span data-stu-id="3f551-178">Command</span></span>                     | <span data-ttu-id="3f551-179">描述</span><span class="sxs-lookup"><span data-stu-id="3f551-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="3f551-180">Lxrun 命令用于管理 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="3f551-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="3f551-181">开始下载和安装过程。</span><span class="sxs-lookup"><span data-stu-id="3f551-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="3f551-182">可以添加 **/y**来绕过所有提示。</span><span class="sxs-lookup"><span data-stu-id="3f551-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="3f551-183">系统会自动接受确认提示, 并将 "默认用户" 设置为 "root"。</span><span class="sxs-lookup"><span data-stu-id="3f551-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="3f551-184">卸载并删除 Ubuntu 映像。</span><span class="sxs-lookup"><span data-stu-id="3f551-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="3f551-185">默认情况下, 这不会删除用户的 Ubuntu 主目录。</span><span class="sxs-lookup"><span data-stu-id="3f551-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="3f551-186">可以添加 **/y**来自动接受确认提示</span><span class="sxs-lookup"><span data-stu-id="3f551-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="3f551-187">**/full**卸载并删除用户的 Ubuntu 主目录</span><span class="sxs-lookup"><span data-stu-id="3f551-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="3f551-188">设置 Ubuntu 用户上的默认 Bash。</span><span class="sxs-lookup"><span data-stu-id="3f551-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="3f551-189">如果指定的用户不存在, 将提示输入密码。</span><span class="sxs-lookup"><span data-stu-id="3f551-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="3f551-190">有关详细信息, 请 https://aka.ms/wslusers 访问:。</span><span class="sxs-lookup"><span data-stu-id="3f551-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="3f551-191">**/y**绕过密码的 promping。</span><span class="sxs-lookup"><span data-stu-id="3f551-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="3f551-192">将创建不带密码的用户。</span><span class="sxs-lookup"><span data-stu-id="3f551-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="3f551-193">更新子系统的包索引</span><span class="sxs-lookup"><span data-stu-id="3f551-193">Updates the subsystem's package index</span></span>          |
