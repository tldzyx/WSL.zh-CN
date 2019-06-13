---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows，bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038077"
---
# <a name="installation-instructions-for-wsl-2"></a><span data-ttu-id="46e8d-104">WSL 2 的安装说明</span><span class="sxs-lookup"><span data-stu-id="46e8d-104">Installation Instructions for WSL 2</span></span>

<span data-ttu-id="46e8d-105">若要安装和开始使用 WSL 2，请完成以下步骤：</span><span class="sxs-lookup"><span data-stu-id="46e8d-105">To install and start using WSL 2 complete the following steps:</span></span>

- <span data-ttu-id="46e8d-106">启用虚拟机平台可选组件</span><span class="sxs-lookup"><span data-stu-id="46e8d-106">Enable the 'Virtual Machine Platform' optional component</span></span>
- <span data-ttu-id="46e8d-107">设置要由 WSL 2： 使用命令行支持的发行版</span><span class="sxs-lookup"><span data-stu-id="46e8d-107">Set a distro to be backed by WSL 2 using the command line</span></span>
- <span data-ttu-id="46e8d-108">验证正在使用的版本的 WSL 在发行版</span><span class="sxs-lookup"><span data-stu-id="46e8d-108">Verify what versions of WSL your distros are using</span></span>

## <a name="enable-the-virtual-machine-platform-optional-component"></a><span data-ttu-id="46e8d-109">启用虚拟机平台可选组件</span><span class="sxs-lookup"><span data-stu-id="46e8d-109">Enable the 'Virtual Machine Platform' optional component</span></span>

<span data-ttu-id="46e8d-110">以管理员身份打开 PowerShell 并运行：</span><span class="sxs-lookup"><span data-stu-id="46e8d-110">Open PowerShell as an Administrator and run:</span></span>

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

<span data-ttu-id="46e8d-111">这些更改才会启用后，需要重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="46e8d-111">After these changes are enabled you will need to restart your computer.</span></span>

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a><span data-ttu-id="46e8d-112">设置要由 WSL 2： 使用命令行支持的发行版</span><span class="sxs-lookup"><span data-stu-id="46e8d-112">Set a distro to be backed by WSL 2 using the command line</span></span>

<span data-ttu-id="46e8d-113">在 PowerShell 中运行：</span><span class="sxs-lookup"><span data-stu-id="46e8d-113">In PowerShell run:</span></span>

`wsl --set-version <Distro> 2`

<span data-ttu-id="46e8d-114">请务必替换和`<Distro>`发行版的实际名称。</span><span class="sxs-lookup"><span data-stu-id="46e8d-114">and make sure to replace `<Distro>` with the actual name of your distro.</span></span> <span data-ttu-id="46e8d-115">(您可以找到这些命令： `wsl -l`)。</span><span class="sxs-lookup"><span data-stu-id="46e8d-115">(You can find these with the command: `wsl -l`).</span></span> <span data-ttu-id="46e8d-116">您可以改回为 WSL 1 随时通过按上述方式运行同一命令，但替换为"2"与"1"。</span><span class="sxs-lookup"><span data-stu-id="46e8d-116">You can change back to WSL 1 at anytime by running the same command as above but replacing the '2' with a '1'.</span></span>

<span data-ttu-id="46e8d-117">此外，如果你想要 WSL 2 默认体系结构就可以做到使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="46e8d-117">Additionally, if you want to make WSL 2 your default architecture you can do so with this command:</span></span>

`wsl --set-default-version 2`

<span data-ttu-id="46e8d-118">这将使任何新安装的发行版将初始化为 WSL 2 发行版。</span><span class="sxs-lookup"><span data-stu-id="46e8d-118">This will make any new distro that you install be initialized as a WSL 2 distro.</span></span>

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a><span data-ttu-id="46e8d-119">完成并验证 WSL 发行版的版本使用</span><span class="sxs-lookup"><span data-stu-id="46e8d-119">Finish with verifying what versions of WSL your distro are using</span></span>

<span data-ttu-id="46e8d-120">若要验证哪些版本的 WSL 使用每个发行版，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="46e8d-120">To verify what versions of WSL each distro is using use the following command:</span></span>

<span data-ttu-id="46e8d-121">`wsl --list --verbose` 或 `wsl -l -v`</span><span class="sxs-lookup"><span data-stu-id="46e8d-121">`wsl --list --verbose` or `wsl -l -v`</span></span>

<span data-ttu-id="46e8d-122">选择上面的发行版此时应显示"2"的版本列下。</span><span class="sxs-lookup"><span data-stu-id="46e8d-122">The distro that you've chosen above should now display a '2' under the 'version' column.</span></span> <span data-ttu-id="46e8d-123">现在，完成后随时开始使用 WSL 2 发行版 ！</span><span class="sxs-lookup"><span data-stu-id="46e8d-123">Now that you're finished feel free to start using your WSL 2 distro!</span></span> 