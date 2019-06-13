---
title: 安装或删除在 Windows 10 周年更新或创意者更新
description: 旧版、 beta 发行版在 Windows 10 周年更新或创意者更新的安装和卸载说明
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10，旧版、 beta 版的 windows 子系统安装、 删除、 卸载，请卸载，删除，不推荐使用
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: fbb5bdc401a013b0853774cff6ad2dc84a36e412
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040840"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="d0794-104">若要安装或卸载适用于 Windows 10 周年更新和创意者更新上的 Linux 的 Windows 子系统的指南</span><span class="sxs-lookup"><span data-stu-id="d0794-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="d0794-105">如果要运行 Windows 10 创意者更新或更高版本，请[按照 Windows 10 安装说明进行操作](install-win10.md)。</span><span class="sxs-lookup"><span data-stu-id="d0794-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="d0794-106"><strong><em><span style="color: #f28014">以下说明适用于运行 Windows 10 周年更新或 Windows 10 创意者更新的用户</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="d0794-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="d0794-107">在 Windows 10 Fall Creators Update （版本 1709年） 之前, WSL 作为 beta 版功能发布和安装单个 Ubuntu 实例"的 Bash 在 Ubuntu 上 Windows"（或 Bash.exe） 首次运行时。</span><span class="sxs-lookup"><span data-stu-id="d0794-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="d0794-108">尽管在早期的 Windows 10 版本上，可以使用 WSL，"旧发行版"此测试版现已被淘汰。</span><span class="sxs-lookup"><span data-stu-id="d0794-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="d0794-109">我们强烈建议你运行 Windows 10 个可用的最新版本。</span><span class="sxs-lookup"><span data-stu-id="d0794-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="d0794-110">每个新的 Windows 10 版本包括在 WSL 独立的允许更 Linux 工具和应用，以便在 WSL 上正确运行数百个修复和改进。</span><span class="sxs-lookup"><span data-stu-id="d0794-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="d0794-111">如果您不能升级为 Fall Creators Update 或更高版本，请执行以下步骤来启用和使用 WSL:</span><span class="sxs-lookup"><span data-stu-id="d0794-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="d0794-112">打开开发人员模式为 Windows 10 周年更新或创意者更新上运行 WSL，必须启用开发人员模式：</span><span class="sxs-lookup"><span data-stu-id="d0794-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="d0794-113">打开**设置** -> **更新和安全** -> **面向开发人员**</span><span class="sxs-lookup"><span data-stu-id="d0794-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="d0794-114">选择开发人员模式下的单选按钮</span><span class="sxs-lookup"><span data-stu-id="d0794-114">Select the Developer Mode radio button</span></span>  
    ![启用开发人员模式](media/updateAndSecurity.png)

    > <span data-ttu-id="d0794-116">若要启用开发人员模式的要求是[在 Windows 10 Fall Creators Update 中删除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span><span class="sxs-lookup"><span data-stu-id="d0794-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="d0794-117">打开命令提示符。</span><span class="sxs-lookup"><span data-stu-id="d0794-117">Open a command prompt.</span></span>  <span data-ttu-id="d0794-118">类型`bash`并按 enter</span><span class="sxs-lookup"><span data-stu-id="d0794-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="d0794-119">首次 Bash 在 Ubuntu 运行 Windows，系统会提示接受 Canonical 的许可证。</span><span class="sxs-lookup"><span data-stu-id="d0794-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="d0794-120">接受后，WSL 将下载并安装到您计算机上的 Ubuntu 实例和"Bash 在 Ubuntu 上 Windows"快捷方式将添加到开始菜单。</span><span class="sxs-lookup"><span data-stu-id="d0794-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![提示安装 Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="d0794-122">首次 Bash 在 Ubuntu 运行 Windows，系统会提示创建 UNIX 用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="d0794-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="d0794-123">请按照[发行版的新实例指令](initialize-distro.md)可完成安装</span><span class="sxs-lookup"><span data-stu-id="d0794-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="d0794-124">通过以下任一方法启动新的 Ubuntu 外壳程序：</span><span class="sxs-lookup"><span data-stu-id="d0794-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="d0794-125">运行`bash`从命令提示符</span><span class="sxs-lookup"><span data-stu-id="d0794-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="d0794-126">单击开始菜单"Bash 在 Ubuntu 上 Windows"快捷方式</span><span class="sxs-lookup"><span data-stu-id="d0794-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="d0794-127">卸载/删除旧的发行版</span><span class="sxs-lookup"><span data-stu-id="d0794-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="d0794-128">如果您从在其安装 WSL 早期 Windows 10 版本升级到 Windows 10 Fall Creators Update，则你现有的发行版将保持不变。</span><span class="sxs-lookup"><span data-stu-id="d0794-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="d0794-129">但是，我们强烈建议您安装的新应用商店提供发行版，ASAP，并将任何必要的文件、 数据等从旧发行版迁移到新发行版。</span><span class="sxs-lookup"><span data-stu-id="d0794-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="d0794-130">若要从计算机中删除旧的发行版，从命令行或 PowerShell 实例运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="d0794-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="d0794-131">手动删除旧的发行版</span><span class="sxs-lookup"><span data-stu-id="d0794-131">Manually deleting the legacy distro</span></span>
<span data-ttu-id="d0794-132">如果您愿意，可以手动删除旧实例。</span><span class="sxs-lookup"><span data-stu-id="d0794-132">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="d0794-133">如果遇到问题卸载旧的发行版使用这可能是所需`lxrun.exe`，或在运行 Windows 10 Spring 2018 Update （或更高版本） 的不会随附于`lxrun.exe`。</span><span class="sxs-lookup"><span data-stu-id="d0794-133">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="d0794-134">若要强制删除旧的 WSL 发行版，删除`%localappdata%\lxss\`文件夹 (和所有它的子内容) 使用 Windows 的文件资源管理器或命令行：</span><span class="sxs-lookup"><span data-stu-id="d0794-134">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="d0794-135">使用 PowerShell</span><span class="sxs-lookup"><span data-stu-id="d0794-135">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="d0794-136">使用 Cmd:</span><span class="sxs-lookup"><span data-stu-id="d0794-136">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
