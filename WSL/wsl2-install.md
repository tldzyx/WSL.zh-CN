---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a53e6a986813809d0c355b80b3fe3028adb21375
ms.sourcegitcommit: 73f4cc6ac9482ea9727f3cda0ec5c3572e164256
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/21/2019
ms.locfileid: "74309050"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="ff54e-104">WSL 2 的安装说明</span><span class="sxs-lookup"><span data-stu-id="ff54e-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="ff54e-105">若要安装并开始使用 WSL 2，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="ff54e-105">To install and start using WSL 2 complete the following steps:</span></span>

> <span data-ttu-id="ff54e-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span><span class="sxs-lookup"><span data-stu-id="ff54e-106">WSL 2 is only available in Windows 10 builds 18917 or higher</span></span>

- <span data-ttu-id="ff54e-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span><span class="sxs-lookup"><span data-stu-id="ff54e-107">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 **build 18917** or higher</span></span>
   - <span data-ttu-id="ff54e-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span><span class="sxs-lookup"><span data-stu-id="ff54e-108">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="ff54e-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span><span class="sxs-lookup"><span data-stu-id="ff54e-109">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="ff54e-110">启用“虚拟机平台”可选组件</span><span class="sxs-lookup"><span data-stu-id="ff54e-110">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="ff54e-111">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="ff54e-111">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="ff54e-112">验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="ff54e-112">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="ff54e-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span><span class="sxs-lookup"><span data-stu-id="ff54e-113">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="ff54e-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span><span class="sxs-lookup"><span data-stu-id="ff54e-114">You will need to make sure that you have both the Windows Subsystem for Linux and the Virtual Machine Platform optional components installed.</span></span> <span data-ttu-id="ff54e-115">You can do that by running the following command in PowerShell:</span><span class="sxs-lookup"><span data-stu-id="ff54e-115">You can do that by running the following command in PowerShell:</span></span> 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

<span data-ttu-id="ff54e-116">Please restart your machine to finish installing both components.</span><span class="sxs-lookup"><span data-stu-id="ff54e-116">Please restart your machine to finish installing both components.</span></span>


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="ff54e-117">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="ff54e-117">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="ff54e-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span><span class="sxs-lookup"><span data-stu-id="ff54e-118">If you do not have a Linux distro installed, please refer to the [Install on Windows 10](./install-win10.md#install-your-linux-distribution-of-choice) docs page for instructions on installing one.</span></span> 

<span data-ttu-id="ff54e-119">To set a distro please run:</span><span class="sxs-lookup"><span data-stu-id="ff54e-119">To set a distro please run:</span></span> 

```
wsl --set-version <Distro> 2
```

<span data-ttu-id="ff54e-120">并且确保将 `<Distro>` 替换为你的发行版的实际名称。</span><span class="sxs-lookup"><span data-stu-id="ff54e-120">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="ff54e-121">（可使用以下命令找到这些内容：`wsl -l`）。</span><span class="sxs-lookup"><span data-stu-id="ff54e-121">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="ff54e-122">可以随时更改回 WSL 1，方法是运行与上面相同的命令，但将“2”替换为“1”。</span><span class="sxs-lookup"><span data-stu-id="ff54e-122">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="ff54e-123">此外，如果要使 WSL 2 成为你的默认体系结构，可以通过此命令执行该操作：</span><span class="sxs-lookup"><span data-stu-id="ff54e-123">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

```
wsl --set-default-version 2
```

<span data-ttu-id="ff54e-124">这会使你安装的任何新发行版均初始化为 WSL 2 发行版。</span><span class="sxs-lookup"><span data-stu-id="ff54e-124">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="ff54e-125">完成验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="ff54e-125">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="ff54e-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span><span class="sxs-lookup"><span data-stu-id="ff54e-126">To verify what versions of WSL each distro is using use the following command (only available in Windows Build 18917 or higher):</span></span>

<span data-ttu-id="ff54e-127">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="ff54e-127">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="ff54e-128">上面选择的发行版现在应在“version”列下显示“2”。</span><span class="sxs-lookup"><span data-stu-id="ff54e-128">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="ff54e-129">既然已经完成，便可以随时开始使用 WSL 2 发行版了！</span><span class="sxs-lookup"><span data-stu-id="ff54e-129">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="ff54e-130">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="ff54e-130">Troubleshooting:</span></span> 

<span data-ttu-id="ff54e-131">下面是安装 WSL 2 时的相关错误和建议的修补程序。</span><span class="sxs-lookup"><span data-stu-id="ff54e-131">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="ff54e-132">请参阅 [WSL 故障排除页](troubleshooting.md)以了解其他常见的 WSL 错误及其解决方案。</span><span class="sxs-lookup"><span data-stu-id="ff54e-132">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="ff54e-133">**安装失败，出现错误 0x80070003 或错误 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="ff54e-133">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="ff54e-134">请确保在计算机的 BIOS 内已启用虚拟化。</span><span class="sxs-lookup"><span data-stu-id="ff54e-134">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="ff54e-135">有关如何执行此操作的说明因计算机而异，并且很可能在 CPU 相关选项下。</span><span class="sxs-lookup"><span data-stu-id="ff54e-135">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="ff54e-136">**尝试升级时出错：`Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="ff54e-136">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="ff54e-137">请确保已启用适用于 Linux 的 Windows 子系统，并且你使用的是 Windows 内部版本 18917 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="ff54e-137">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="ff54e-138">若要启用 WSL，请在 Powershell 提示符下以具有管理员权限的身份运行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="ff54e-138">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="ff54e-139">可在[此处](./install-win10.md)找到完整的 WSL 安装说明。</span><span class="sxs-lookup"><span data-stu-id="ff54e-139">You can find the full WSL install instructions [here](./install-win10.md).</span></span>

* <span data-ttu-id="ff54e-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span><span class="sxs-lookup"><span data-stu-id="ff54e-140">**The requested operation could not be completed due to a virtual disk system limitation. Virtual hard disk files must be uncompressed and unencrypted and must not be sparse.**</span></span>
    * <span data-ttu-id="ff54e-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span><span class="sxs-lookup"><span data-stu-id="ff54e-141">Please check [WSL Github thread #4103](https://github.com/microsoft/WSL/issues/4103) where this issue is being tracked for updated information.</span></span>

* <span data-ttu-id="ff54e-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span><span class="sxs-lookup"><span data-stu-id="ff54e-142">**The term 'wsl' is not recognized as the name of a cmdlet, function, script file, or operable program.**</span></span> 
    * <span data-ttu-id="ff54e-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span><span class="sxs-lookup"><span data-stu-id="ff54e-143">Ensure that the [Windows Subsystem for Linux Optional Component is installed](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled).</span></span><br> <span data-ttu-id="ff54e-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span><span class="sxs-lookup"><span data-stu-id="ff54e-144">Additionally, if you are using an Arm64 device and running this command from PowerShell, you will receive this error.</span></span> <span data-ttu-id="ff54e-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span><span class="sxs-lookup"><span data-stu-id="ff54e-145">Instead run `wsl.exe` from [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6), or Command Prompt.</span></span> 
