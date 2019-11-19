---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91994f3a075436c022acb9dadeea072142687b72
ms.sourcegitcommit: cf6d8e277ed3102f8f879b9f39ba0966d4ea6135
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2019
ms.locfileid: "74164342"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="756f1-104">WSL 2 的安装说明</span><span class="sxs-lookup"><span data-stu-id="756f1-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="756f1-105">若要安装并开始使用 WSL 2，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="756f1-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="756f1-106">WSL 2 仅适用于 Windows 10 版本18917或更高版本</span><span class="sxs-lookup"><span data-stu-id="756f1-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="756f1-107">确保已安装 WSL （可以在[此处](./install-win10.md)找到相关说明），并且运行的是 Windows 10**内部版本 18917**或更高版本</span><span class="sxs-lookup"><span data-stu-id="756f1-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="756f1-108">若要确保使用的是版本18917或更高版本，请加入[Windows 预览体验计划](https://insider.windows.com/en-us/)，并选择 "快速" 环。</span><span class="sxs-lookup"><span data-stu-id="756f1-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="756f1-109">可以通过打开命令提示符并运行 `ver` 命令来检查 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="756f1-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="756f1-110">启用“虚拟机平台”可选组件</span><span class="sxs-lookup"><span data-stu-id="756f1-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="756f1-111">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="756f1-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="756f1-112">验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="756f1-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="756f1-113">启用 "虚拟机平台" 可选组件，并确保已启用 WSL</span><span class="sxs-lookup"><span data-stu-id="756f1-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="756f1-114">若要启用 "虚拟机平台" 组件，请以管理员身份打开 PowerShell 并运行以下命令。</span><span class="sxs-lookup"><span data-stu-id="756f1-114">To enable the 'Virtual Machine Platform' component open PowerShell as an administrator and run the command below.</span></span> <span data-ttu-id="756f1-115">如果是第一次安装 WSL，则在系统提示重新启动时选择 "否"，因为在安装 "适用于 Linux 的 Windows 子系统" 可选组件后，你将需要重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="756f1-115">If you are installing WSL for the first time then select 'No' when prompted for a restart, as you will need to restart your machine anyway after installing the 'Windows Subsystem for Linux' optional component.</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
```

<span data-ttu-id="756f1-116">还需要确保已启用适用于 Linux 的 Windows 子系统可选组件。</span><span class="sxs-lookup"><span data-stu-id="756f1-116">You will also need to make sure that the Windows Subsystem for Linux optional component is enabled.</span></span> <span data-ttu-id="756f1-117">要执行此操作，可以在具有管理员权限的 PowerShell 窗口中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="756f1-117">You can do this by running the following command from a PowerShell window with administrator privileges:</span></span> 

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="756f1-118">请重新启动计算机以完成两个组件的安装。</span><span class="sxs-lookup"><span data-stu-id="756f1-118">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="756f1-119">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="756f1-119">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="756f1-120">如果尚未安装 Linux 发行版，请参阅在[Windows 10 文档上安装](./install-win10.md#install-your-linux-distribution-of-choice)页，获取有关安装一个的说明。</span><span class="sxs-lookup"><span data-stu-id="756f1-120">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="756f1-121">在 PowerShell 中运行：</span><span class="sxs-lookup"><span data-stu-id="756f1-121">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="756f1-122">并且确保将 `<Distro>` 替换为你的发行版的实际名称。</span><span class="sxs-lookup"><span data-stu-id="756f1-122">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="756f1-123">（可使用以下命令找到这些内容：`wsl -l`）。</span><span class="sxs-lookup"><span data-stu-id="756f1-123">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="756f1-124">可以随时更改回 WSL 1，方法是运行与上面相同的命令，但将“2”替换为“1”。</span><span class="sxs-lookup"><span data-stu-id="756f1-124">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="756f1-125">此外，如果要使 WSL 2 成为你的默认体系结构，可以通过此命令执行该操作：</span><span class="sxs-lookup"><span data-stu-id="756f1-125">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="756f1-126">这会使你安装的任何新发行版均初始化为 WSL 2 发行版。</span><span class="sxs-lookup"><span data-stu-id="756f1-126">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="756f1-127">完成验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="756f1-127">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="756f1-128">若要验证每个发行版使用的 WSL 版本，请使用以下命令（仅适用于 Windows 版本18917或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="756f1-128">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="756f1-129">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="756f1-129">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="756f1-130">上面选择的发行版现在应在“version”列下显示“2”。</span><span class="sxs-lookup"><span data-stu-id="756f1-130">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="756f1-131">既然已经完成，便可以随时开始使用 WSL 2 发行版了！</span><span class="sxs-lookup"><span data-stu-id="756f1-131">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="756f1-132">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="756f1-132">Troubleshooting:</span></span> 

<span data-ttu-id="756f1-133">下面是安装 WSL 2 时的相关错误和建议的修补程序。</span><span class="sxs-lookup"><span data-stu-id="756f1-133">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="756f1-134">请参阅 [WSL 故障排除页](troubleshooting.md)以了解其他常见的 WSL 错误及其解决方案。</span><span class="sxs-lookup"><span data-stu-id="756f1-134">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="756f1-135">**安装失败，出现错误 0x80070003 或错误 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="756f1-135">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="756f1-136">请确保在计算机的 BIOS 内已启用虚拟化。</span><span class="sxs-lookup"><span data-stu-id="756f1-136">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="756f1-137">有关如何执行此操作的说明因计算机而异，并且很可能在 CPU 相关选项下。</span><span class="sxs-lookup"><span data-stu-id="756f1-137">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="756f1-138">**尝试升级时出错：`Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="756f1-138">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="756f1-139">请确保已启用适用于 Linux 的 Windows 子系统，并且你使用的是 Windows 内部版本 18917 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="756f1-139">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="756f1-140">若要启用 WSL，请在 Powershell 提示符下以具有管理员权限的身份运行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="756f1-140">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="756f1-141">可在[此处](./install-win10.md)找到完整的 WSL 安装说明。</span><span class="sxs-lookup"><span data-stu-id="756f1-141">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="756f1-142">**由于虚拟磁盘系统限制，无法完成请求的操作。虚拟硬盘文件必须是解压缩和未加密的，并且不能是稀疏的。**</span><span class="sxs-lookup"><span data-stu-id="756f1-142">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="756f1-143">请查看[WSL Github 线程 #4103](https://github.com/microsoft/WSL/issues/4103)正在跟踪此问题的更新信息。</span><span class="sxs-lookup"><span data-stu-id="756f1-143">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>