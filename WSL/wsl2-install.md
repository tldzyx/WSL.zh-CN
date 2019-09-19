---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: bced0fd0bf948842b8c465f645aa5c368c2f4335
ms.sourcegitcommit: ebc6ae7e7546a6d33644e68788fa0215028859b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2019
ms.locfileid: "71070302"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="a7031-104">WSL 2 的安装说明</span><span class="sxs-lookup"><span data-stu-id="a7031-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="a7031-105">若要安装并开始使用 WSL 2，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="a7031-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="a7031-106">确保已安装 WSL （可以在[此处](./install-win10.md)找到相关说明），并且运行的是 Windows 10 内部版本18917或更高版本</span><span class="sxs-lookup"><span data-stu-id="a7031-106">Ensure that you have WSL installed (you can find instructions to do so [here](./install-win10.md)) and that you are running Windows 10 build 18917 or higher</span></span>
   - <span data-ttu-id="a7031-107">若要确保使用的是版本18917或更高版本，请加入[Windows 预览体验计划](https://insider.windows.com/en-us/)，并选择 "快速" 环。</span><span class="sxs-lookup"><span data-stu-id="a7031-107">To make sure you are using build 18917 or higher please join [the Windows Insider Program](https://insider.windows.com/en-us/) and select the 'Fast' ring.</span></span> 
   - <span data-ttu-id="a7031-108">可以通过打开命令提示符并运行`ver`命令来检查 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="a7031-108">You can check your Windows version by opening Command Prompt and running the `ver` command.</span></span>
- <span data-ttu-id="a7031-109">启用“虚拟机平台”可选组件</span><span class="sxs-lookup"><span data-stu-id="a7031-109">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="a7031-110">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="a7031-110">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="a7031-111">验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="a7031-111">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a><span data-ttu-id="a7031-112">启用 "虚拟机平台" 可选组件，并确保已启用 WSL</span><span class="sxs-lookup"><span data-stu-id="a7031-112">Enable the 'Virtual Machine Platform' optional component and make sure WSL is enabled</span></span>

<span data-ttu-id="a7031-113">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="a7031-113">Open PowerShell as an Administrator and run:</span></span>

```powershell
Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform
Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

<span data-ttu-id="a7031-114">这将确保安装了适用于 Linux 的虚拟机平台和 Windows 子系统可选组件。</span><span class="sxs-lookup"><span data-stu-id="a7031-114">This will make sure that both the Virtual Machine Platform and Windows Subsystem for Linux optional components are installed.</span></span> <span data-ttu-id="a7031-115">运行这些命令后，需要重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="a7031-115">After you've run these commands you'll need to restart your computer.</span></span> 

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="a7031-116">使用命令行设置要由 WSL 2 支持的发行版</span><span class="sxs-lookup"><span data-stu-id="a7031-116">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="a7031-117">在 PowerShell 中运行：</span><span class="sxs-lookup"><span data-stu-id="a7031-117">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="a7031-118">并且确保将 `<Distro>` 替换为你的发行版的实际名称。</span><span class="sxs-lookup"><span data-stu-id="a7031-118">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="a7031-119">（可使用以下命令找到这些内容：`wsl -l`）。</span><span class="sxs-lookup"><span data-stu-id="a7031-119">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="a7031-120">可以随时更改回 WSL 1，方法是运行与上面相同的命令，但将“2”替换为“1”。</span><span class="sxs-lookup"><span data-stu-id="a7031-120">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="a7031-121">此外，如果要使 WSL 2 成为你的默认体系结构，可以通过此命令执行该操作：</span><span class="sxs-lookup"><span data-stu-id="a7031-121">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="a7031-122">这会使你安装的任何新发行版均初始化为 WSL 2 发行版。</span><span class="sxs-lookup"><span data-stu-id="a7031-122">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="a7031-123">完成验证发行版使用的 WSL 版本</span><span class="sxs-lookup"><span data-stu-id="a7031-123">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="a7031-124">若要验证每个发行版使用的 WSL 版本，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="a7031-124">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="a7031-125">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="a7031-125">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="a7031-126">上面选择的发行版现在应在“version”列下显示“2”。</span><span class="sxs-lookup"><span data-stu-id="a7031-126">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="a7031-127">既然已经完成，便可以随时开始使用 WSL 2 发行版了！</span><span class="sxs-lookup"><span data-stu-id="a7031-127">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 

## <a name="troubleshooting"></a><span data-ttu-id="a7031-128">疑难解答：</span><span class="sxs-lookup"><span data-stu-id="a7031-128">Troubleshooting:</span></span> 

<span data-ttu-id="a7031-129">下面是安装 WSL 2 时的相关错误和建议的修补程序。</span><span class="sxs-lookup"><span data-stu-id="a7031-129">Below are related errors and suggested fixes when installing WSL 2.</span></span> <span data-ttu-id="a7031-130">请参阅 [WSL 故障排除页](troubleshooting.md)以了解其他常见的 WSL 错误及其解决方案。</span><span class="sxs-lookup"><span data-stu-id="a7031-130">Please refer to the [WSL troubleshooting page](troubleshooting.md) for other general WSL errors and their solutions.</span></span>

* <span data-ttu-id="a7031-131">**安装失败，出现错误 0x80070003 或错误 0x80370102**</span><span class="sxs-lookup"><span data-stu-id="a7031-131">**Installation failed with error 0x80070003 or error 0x80370102**</span></span>
    * <span data-ttu-id="a7031-132">请确保在计算机的 BIOS 内已启用虚拟化。</span><span class="sxs-lookup"><span data-stu-id="a7031-132">Please make sure that virtualization is enabled inside of your computer's BIOS.</span></span> <span data-ttu-id="a7031-133">有关如何执行此操作的说明因计算机而异，并且很可能在 CPU 相关选项下。</span><span class="sxs-lookup"><span data-stu-id="a7031-133">The instructions on how to do this will vary from computer to computer, and will most likely be under CPU related options.</span></span>
   
* <span data-ttu-id="a7031-134">**尝试升级时出错：`Invalid command line option: wsl --set-version Ubuntu 2`**</span><span class="sxs-lookup"><span data-stu-id="a7031-134">**Error when trying to upgrade: `Invalid command line option: wsl --set-version Ubuntu 2`**</span></span>
    * <span data-ttu-id="a7031-135">请确保已启用适用于 Linux 的 Windows 子系统，并且你使用的是 Windows 内部版本 18917 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a7031-135">Please make sure that you have the Windows Subsystem for Linux enabled, and that you're using Windows Build version 18917 or higher.</span></span> <span data-ttu-id="a7031-136">若要启用 WSL，请在 Powershell 提示符下以具有管理员权限的身份运行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。</span><span class="sxs-lookup"><span data-stu-id="a7031-136">To enable WSL run this command in a Powershell prompt with admin privileges: `Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`.</span></span> <span data-ttu-id="a7031-137">可在[此处](./install-win10.md)找到完整的 WSL 安装说明。</span><span class="sxs-lookup"><span data-stu-id="a7031-137">You can find the full WSL install instructions [here](./install-win10.md).</span></span>