---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 65c0440a95637708881c00558cba6c7985f89ec0
ms.sourcegitcommit: 522af20edfba4d4a9e429327389967a83e6d1156
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/06/2019
ms.locfileid: "74881379"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="2c6f9-104">WSL 2 的安装说明</span><span class="sxs-lookup"><span data-stu-id="2c6f9-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="2c6f9-105">若要安装并开始使用 WSL 2，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="2c6f9-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="2c6f9-106">WSL 2 仅适用于 Windows 10 版本18917或更高版本</span><span class="sxs-lookup"><span data-stu-id="2c6f9-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="2c6f9-107">确保已安装 WSL （可以在[此处](./install-win10.md)找到相关说明），并且运行的是 Windows 10**内部版本 18917**或更高版本</span><span class="sxs-lookup"><span data-stu-id="2c6f9-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="2c6f9-108">若要确保使用的是版本18917或更高版本，请加入[Windows 预览体验计划](https://insider.windows.com/en-us/)，并选择 "快速" 环或 "慢速" 环。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring or the 'Slow' ring.</span></span> 
   - <span data-ttu-id="2c6f9-109">可以通过打开命令提示符并运行 `ver` 命令来检查 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="2c6f9-110">启用“虚拟机平台”可选组件</span><span class="sxs-lookup"><span data-stu-id="2c6f9-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="2c6f9-111">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="2c6f9-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="2c6f9-112">验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="2c6f9-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="2c6f9-113">启用 "虚拟机平台" 可选组件，并确保已启用 WSL</span><span class="sxs-lookup"><span data-stu-id="2c6f9-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="2c6f9-114">你将需要确保你已安装适用于 Linux 的 Windows 子系统和已安装的虚拟机平台可选组件。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="2c6f9-115">可以通过在 PowerShell 中运行以下命令来执行此操作：</span><span class="sxs-lookup"><span data-stu-id="2c6f9-115">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="2c6f9-116">请重新启动计算机以完成两个组件的安装。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-116">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="2c6f9-117">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="2c6f9-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="2c6f9-118">如果尚未安装 Linux 发行版，请参阅在[Windows 10 文档上安装](./install-win10.md#install-your-linux-distribution-of-choice)页，获取有关安装一个的说明。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="2c6f9-119">若要设置发行版，请运行：</span><span class="sxs-lookup"><span data-stu-id="2c6f9-119">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="2c6f9-120">并且确保将 `<Distro>` 替换为你的发行版的实际名称。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-120">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="2c6f9-121">（可使用以下命令找到这些内容：`wsl -l`）。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-121">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="2c6f9-122">可以随时更改回 WSL 1，方法是运行与上面相同的命令，但将“2”替换为“1”。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-122">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="2c6f9-123">此外，如果要使 WSL 2 成为你的默认体系结构，可以通过此命令执行该操作：</span><span class="sxs-lookup"><span data-stu-id="2c6f9-123">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="2c6f9-124">这会使你安装的任何新发行版均初始化为 WSL 2 发行版。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-124">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="2c6f9-125">完成验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="2c6f9-125">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="2c6f9-126">若要验证每个发行版使用的 WSL 版本，请使用以下命令（仅适用于 Windows 版本18917或更高版本）：</span><span class="sxs-lookup"><span data-stu-id="2c6f9-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="2c6f9-127">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="2c6f9-127">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="2c6f9-128">上面选择的发行版现在应在“version”列下显示“2”。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-128">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="2c6f9-129">既然已经完成，便可以随时开始使用 WSL 2 发行版了！</span><span class="sxs-lookup"><span data-stu-id="2c6f9-129">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="2c6f9-130">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="2c6f9-130">Troubleshooting:</span></span> 

<span data-ttu-id="2c6f9-131">下面是安装 WSL 2 时的相关错误和建议的修补程序。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-131">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="2c6f9-132">请参阅 [WSL 故障排除页](troubleshooting.md)以了解其他常见的 WSL 错误及其解决方案。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-132">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="2c6f9-133">**安装失败，出现错误 0x80070003 或错误 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="2c6f9-133">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="2c6f9-134">请确保在计算机的 BIOS 内已启用虚拟化。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-134">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="2c6f9-135">有关如何执行此操作的说明因计算机而异，并且很可能在 CPU 相关选项下。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-135">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="2c6f9-136">**尝试升级时出错：`Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="2c6f9-136">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="2c6f9-137">请确保已启用适用于 Linux 的 Windows 子系统，并且你使用的是 Windows 内部版本 18917 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-137">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="2c6f9-138">若要启用 WSL，请在 Powershell 提示符下以具有管理员权限的身份运行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-138">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="2c6f9-139">可在[此处](./install-win10.md)找到完整的 WSL 安装说明。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-139">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="2c6f9-140">**由于虚拟磁盘系统限制，无法完成请求的操作。虚拟硬盘文件必须是解压缩和未加密的，并且不能是稀疏的。**</span><span class="sxs-lookup"><span data-stu-id="2c6f9-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="2c6f9-141">请查看[WSL Github 线程 #4103](https://github.com/microsoft/WSL/issues/4103)正在跟踪此问题的更新信息。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="2c6f9-142">**术语 "wsl" 未被识别为 cmdlet、函数、脚本文件或可运行程序的名称。**</span><span class="sxs-lookup"><span data-stu-id="2c6f9-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="2c6f9-143">确保[已安装适用于 Linux 的 Windows 子系统可选组件](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="2c6f9-144">此外，如果使用 Arm64 设备，并从 PowerShell 运行此命令，将收到此错误。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="2c6f9-145">改为从[PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6)或命令提示符运行 `wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="2c6f9-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
