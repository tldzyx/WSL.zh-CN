---
title: 适用于 Linux 的 Windows 子系统命令参考
description: 用于管理适用于 Linux 的 Windows 子系统的命令列表
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d74a6926fd797f2e1ede0fd5d8d080d0f1ce3f6b
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269845"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="e8360-104">适用于 Linux 的 Windows 子系统的命令参考</span><span class="sxs-lookup"><span data-stu-id="e8360-104">Command Reference for Windows Subsystem for Linux</span></span>

<span data-ttu-id="e8360-105">与适用于 Linux 的 Windows 子系统交互的最佳方式是使用 `wsl.exe` 命令。</span><span class="sxs-lookup"><span data-stu-id="e8360-105">The best way to interact with the Windows Subsystem for Linux is to use the `wsl.exe` command.</span></span> 


## `wsl.exe`

<span data-ttu-id="e8360-106">以下列表包含自 Windows 版本 1903 开始，在使用 `wsl.exe` 时可用的所有选项。</span><span class="sxs-lookup"><span data-stu-id="e8360-106">Below is a list containing all options when using `wsl.exe` as of Windows Version 1903.</span></span>

<span data-ttu-id="e8360-107">使用：`wsl [Argument] [Options...] [CommandLine]`</span><span class="sxs-lookup"><span data-stu-id="e8360-107">Using: `wsl [Argument] [Options...] [CommandLine]`</span></span>

### <a name="arguments-for-running-linux-binaries"></a><span data-ttu-id="e8360-108">用于运行 Linux 二进制文件的参数</span><span class="sxs-lookup"><span data-stu-id="e8360-108">Arguments for running Linux binaries</span></span>

* <span data-ttu-id="e8360-109">**不带参数**</span><span class="sxs-lookup"><span data-stu-id="e8360-109">**Without arguments**</span></span>

  <span data-ttu-id="e8360-110">如果未提供命令行，wsl.exe 将启动默认 shell。</span><span class="sxs-lookup"><span data-stu-id="e8360-110">If no command line is provided, wsl.exe launches the default shell.</span></span>

* <span data-ttu-id="e8360-111">**--exec、-e \<命令行>**</span><span class="sxs-lookup"><span data-stu-id="e8360-111">**--exec, -e \<CommandLine>**</span></span>
  
  <span data-ttu-id="e8360-112">执行指定的命令，但不使用默认的 Linux shell。</span><span class="sxs-lookup"><span data-stu-id="e8360-112">Execute the specified command without using the default Linux shell.</span></span>

* **--**
  
  <span data-ttu-id="e8360-113">按原样传递剩余的命令行。</span><span class="sxs-lookup"><span data-stu-id="e8360-113">Pass the remaining command line as is.</span></span>

<span data-ttu-id="e8360-114">上述命令也接受以下选项：</span><span class="sxs-lookup"><span data-stu-id="e8360-114">The above commands also accept the following options:</span></span>

* <span data-ttu-id="e8360-115">**--distribution、-d \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-115">**--distribution, -d \<Distro>**</span></span>

  <span data-ttu-id="e8360-116">运行指定的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-116">Run the specified distribution.</span></span>

* <span data-ttu-id="e8360-117">**--user、-u \<用户名>**</span><span class="sxs-lookup"><span data-stu-id="e8360-117">**--user, -u \<UserName>**</span></span>

  <span data-ttu-id="e8360-118">以指定用户的身份运行。</span><span class="sxs-lookup"><span data-stu-id="e8360-118">Run as the specified user.</span></span>

### <a name="arguments-for-managing-windows-subsystem-for-linux"></a><span data-ttu-id="e8360-119">用于管理适用于 Linux 的 Windows 子系统的参数</span><span class="sxs-lookup"><span data-stu-id="e8360-119">Arguments for managing Windows Subsystem for Linux</span></span>

* <span data-ttu-id="e8360-120">**--export \<分发版> \<文件名>**</span><span class="sxs-lookup"><span data-stu-id="e8360-120">**--export \<Distro> \<FileName>**</span></span>
  
  <span data-ttu-id="e8360-121">将分发版导出到 tar 文件。</span><span class="sxs-lookup"><span data-stu-id="e8360-121">Exports the distribution to a tar file.</span></span> <span data-ttu-id="e8360-122">在标准输出中，文件名可以是 -。</span><span class="sxs-lookup"><span data-stu-id="e8360-122">The filename can be - for standard output.</span></span>

* <span data-ttu-id="e8360-123">**--import \<分发版> \<安装位置> \<文件名>**</span><span class="sxs-lookup"><span data-stu-id="e8360-123">**--import \<Distro> \<InstallLocation> \<FileName>**</span></span>
  
  <span data-ttu-id="e8360-124">导入指定的 tar 文件作为新的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-124">Imports the specified tar file as a new distribution.</span></span> <span data-ttu-id="e8360-125">在标准输入中，文件名可以是 -。</span><span class="sxs-lookup"><span data-stu-id="e8360-125">The filename can be - for standard input.</span></span>

* <span data-ttu-id="e8360-126">**--list、-l [选项]**</span><span class="sxs-lookup"><span data-stu-id="e8360-126">**--list, -l [Options]**</span></span>
  
  <span data-ttu-id="e8360-127">列出分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-127">Lists distributions.</span></span>

  <span data-ttu-id="e8360-128">选项：</span><span class="sxs-lookup"><span data-stu-id="e8360-128">Options:</span></span>
  * <span data-ttu-id="e8360-129">**--all**</span><span class="sxs-lookup"><span data-stu-id="e8360-129">**--all**</span></span>
      
    <span data-ttu-id="e8360-130">列出所有分发版，包括当前正在安装或卸载的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-130">List all distributions, including distributions that are currently being installed or uninstalled.</span></span>

  * <span data-ttu-id="e8360-131">**--running**</span><span class="sxs-lookup"><span data-stu-id="e8360-131">**--running**</span></span>
      
    <span data-ttu-id="e8360-132">仅列出当前正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-132">List only distributions that are currently running.</span></span>

* <span data-ttu-id="e8360-133">**--set-default、-s \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-133">**--set-default, -s \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-134">将分发版设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="e8360-134">Sets the distribution as the default.</span></span>

* <span data-ttu-id="e8360-135">**--terminate, -t \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-135">**--terminate, -t \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-136">终止指定的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-136">Terminates the specified distribution.</span></span>

* <span data-ttu-id="e8360-137">**--unregister \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-137">**--unregister \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-138">取消注册分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-138">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="e8360-139">**--help** 显示用法信息。</span><span class="sxs-lookup"><span data-stu-id="e8360-139">**--help** Display usage information.</span></span>

## <a name="additional-commands"></a><span data-ttu-id="e8360-140">其他命令</span><span class="sxs-lookup"><span data-stu-id="e8360-140">Additional Commands</span></span>

<span data-ttu-id="e8360-141">还可以使用一些传统命令来与适用于 Linux 的 Windows 子系统交互。</span><span class="sxs-lookup"><span data-stu-id="e8360-141">There are also historic commands to interact with the Windows Subsystem for Linux.</span></span> <span data-ttu-id="e8360-142">这些命令的功能已包含在 `wsl.exe` 中，但仍可供使用。</span><span class="sxs-lookup"><span data-stu-id="e8360-142">Their functionality is encompassed within `wsl.exe`, but they are still available for use.</span></span> 

### `wslconfig.exe`

<span data-ttu-id="e8360-143">此命令可用于配置 WSL 分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-143">This command lets you configure your WSL distribution.</span></span> <span data-ttu-id="e8360-144">下面是其选项列表。</span><span class="sxs-lookup"><span data-stu-id="e8360-144">Below is a list of its options.</span></span>

<span data-ttu-id="e8360-145">使用：`wslconfig [Argument] [Options...]`</span><span class="sxs-lookup"><span data-stu-id="e8360-145">Using: `wslconfig [Argument] [Options...]`</span></span>

#### <a name="arguments"></a><span data-ttu-id="e8360-146">参数</span><span class="sxs-lookup"><span data-stu-id="e8360-146">Arguments</span></span>
* <span data-ttu-id="e8360-147">**/l、/list [选项]**</span><span class="sxs-lookup"><span data-stu-id="e8360-147">**/l, /list [Options]**</span></span>
  
  <span data-ttu-id="e8360-148">列出已注册的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-148">Lists registered distributions.</span></span>
  
  <span data-ttu-id="e8360-149">选项：</span><span class="sxs-lookup"><span data-stu-id="e8360-149">Options:</span></span>
    * <span data-ttu-id="e8360-150">**/all**</span><span class="sxs-lookup"><span data-stu-id="e8360-150">**/all**</span></span>
    
      <span data-ttu-id="e8360-151">（可选）列出所有分发版，包括当前正在安装或卸载的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-151">Optionally list all distributions, including distributions that are currently being installed or uninstalled.</span></span>

    * <span data-ttu-id="e8360-152">**/running**</span><span class="sxs-lookup"><span data-stu-id="e8360-152">**/running**</span></span>
      
      <span data-ttu-id="e8360-153">仅列出当前正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-153">List only distributions that are currently running.</span></span>

* <span data-ttu-id="e8360-154">**/s、/setdefault \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-154">**/s, /setdefault \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-155">将分发版设置为默认值。</span><span class="sxs-lookup"><span data-stu-id="e8360-155">Sets the distribution as the default.</span></span>

* <span data-ttu-id="e8360-156">**/t、/terminate \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-156">**/t, /terminate \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-157">终止分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-157">Terminates the distribution.</span></span>

* <span data-ttu-id="e8360-158">**/u、/unregister \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-158">**/u, /unregister \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-159">取消注册分发版。</span><span class="sxs-lookup"><span data-stu-id="e8360-159">Unregisters the distribution.</span></span>
   
* <span data-ttu-id="e8360-160">**/upgrade \<分发版>**</span><span class="sxs-lookup"><span data-stu-id="e8360-160">**/upgrade \<Distro>**</span></span>
  
  <span data-ttu-id="e8360-161">将分发版升级为 WslFs 文件系统格式。</span><span class="sxs-lookup"><span data-stu-id="e8360-161">Upgrades the distribution to the WslFs file system format.</span></span>

### `bash.exe`

<span data-ttu-id="e8360-162">此命令用于启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="e8360-162">This command is used to start a bash shell.</span></span> <span data-ttu-id="e8360-163">下面是可在此命令中使用的选项。</span><span class="sxs-lookup"><span data-stu-id="e8360-163">Below are the options you can use with this command.</span></span>

<span data-ttu-id="e8360-164">使用：`bash [Options...]`</span><span class="sxs-lookup"><span data-stu-id="e8360-164">Using: `bash [Options...]`</span></span>

* <span data-ttu-id="e8360-165">**未指定选项**</span><span class="sxs-lookup"><span data-stu-id="e8360-165">**No Option given**</span></span>
  
  <span data-ttu-id="e8360-166">在当前目录中启动 Bash shell。</span><span class="sxs-lookup"><span data-stu-id="e8360-166">Launches the Bash shell in the current directory.</span></span> <span data-ttu-id="e8360-167">如果未自动安装 Bash shell，请运行 `lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="e8360-167">If the Bash shell is not installed automatically runs `lxrun /install`</span></span>

* **~**
  
  <span data-ttu-id="e8360-168">`bash ~` 在用户的主目录中启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="e8360-168">`bash ~` launches the bash shell into the user's home directory.</span></span>  <span data-ttu-id="e8360-169">类似于运行 `cd ~`。</span><span class="sxs-lookup"><span data-stu-id="e8360-169">Similar to running `cd ~`.</span></span>

* <span data-ttu-id="e8360-170">**-c "\<命令>"**</span><span class="sxs-lookup"><span data-stu-id="e8360-170">**-c "\<command>"**</span></span>
  
  <span data-ttu-id="e8360-171">运行命令，列显输出，并返回到 Windows 命令提示符。</span><span class="sxs-lookup"><span data-stu-id="e8360-171">Runs the command, prints the output and exits back to the Windows command prompt.</span></span>
    
  <span data-ttu-id="e8360-172">示例：`bash -c "ls"`。</span><span class="sxs-lookup"><span data-stu-id="e8360-172">Example:  `bash -c "ls"`.</span></span>

## <a name="deprecated-commands"></a><span data-ttu-id="e8360-173">已弃用的命令</span><span class="sxs-lookup"><span data-stu-id="e8360-173">Deprecated Commands</span></span>

<span data-ttu-id="e8360-174">`lxrun.exe` 是用于安装和管理适用于 Linux 的 Windows 子系统的第一个命令。</span><span class="sxs-lookup"><span data-stu-id="e8360-174">The `lxrun.exe` was the first command used to install and manage the Windows Subsystem for Linux.</span></span> <span data-ttu-id="e8360-175">从 Windows 10 1803 和更高版本开始，此命令已弃用。</span><span class="sxs-lookup"><span data-stu-id="e8360-175">It is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="e8360-176">可以使用命令 `lxrun.exe` 来直接与[适用于 Linux 的 Windows 子系统 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) 交互。</span><span class="sxs-lookup"><span data-stu-id="e8360-176">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="e8360-177">这些命令已安装到 `\Windows\System32` 目录中，可以在 Windows 命令提示符或 PowerShell 中运行。</span><span class="sxs-lookup"><span data-stu-id="e8360-177">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

| <span data-ttu-id="e8360-178">命令</span><span class="sxs-lookup"><span data-stu-id="e8360-178">Command</span></span>                     | <span data-ttu-id="e8360-179">描述</span><span class="sxs-lookup"><span data-stu-id="e8360-179">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="e8360-180">lxrun 命令用于管理 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="e8360-180">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="e8360-181">启动下载和安装过程。</span><span class="sxs-lookup"><span data-stu-id="e8360-181">Starts the download and install process.</span></span> <br/> <span data-ttu-id="e8360-182">可以添加 **/y** 来绕过所有提示。</span><span class="sxs-lookup"><span data-stu-id="e8360-182">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="e8360-183">系统会自动接受确认提示，默认用户将设置为 root。</span><span class="sxs-lookup"><span data-stu-id="e8360-183">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="e8360-184">卸载并删除 Ubuntu 映像。</span><span class="sxs-lookup"><span data-stu-id="e8360-184">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="e8360-185">默认情况下，这不会删除用户的 Ubuntu 主目录。</span><span class="sxs-lookup"><span data-stu-id="e8360-185">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="e8360-186">可以添加 **/y** 来自动接受确认提示</span><span class="sxs-lookup"><span data-stu-id="e8360-186">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="e8360-187">**/full** 卸载并删除用户的 Ubuntu 主目录</span><span class="sxs-lookup"><span data-stu-id="e8360-187">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="e8360-188">设置默认的 Bash on Ubuntu 用户。</span><span class="sxs-lookup"><span data-stu-id="e8360-188">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="e8360-189">如果指定的用户不存在，该命令会提示输入密码。</span><span class="sxs-lookup"><span data-stu-id="e8360-189">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="e8360-190">有关详细信息，请访问： https://aka.ms/wslusers 。</span><span class="sxs-lookup"><span data-stu-id="e8360-190">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="e8360-191">**/y** 绕过密码提示。</span><span class="sxs-lookup"><span data-stu-id="e8360-191">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="e8360-192">将创建不带密码的用户。</span><span class="sxs-lookup"><span data-stu-id="e8360-192">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="e8360-193">更新子系统的包索引</span><span class="sxs-lookup"><span data-stu-id="e8360-193">Updates the subsystem's package index</span></span>          |
