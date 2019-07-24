---
title: 在 Windows 10 周年更新或创意者更新上安装或删除
description: 适用于 Windows 10 周年更新或创意者更新的旧版、beta 发行版的安装和卸载说明
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, debian, suse, windows 10, 旧版, beta, 安装, 删除, 卸载, 卸载, 删除, 已弃用
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0d8fdabd61fadbfc58549a220ead23585a3d3656
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499261"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a><span data-ttu-id="b238d-104">在 Windows 10 周年更新和创意者更新上安装或卸载适用于 Linux 的 Windows 子系统的指南</span><span class="sxs-lookup"><span data-stu-id="b238d-104">Guide to install or uninstall Windows Subsystem for Linux on Windows 10 Anniversary Update and Creators Update</span></span> 

<span data-ttu-id="b238d-105">如果运行的是 Windows 10 创意者更新或更高版本, 请[遵循 windows 10 安装说明](install-win10.md)。</span><span class="sxs-lookup"><span data-stu-id="b238d-105">If you're running Windows 10 Creators Update or later, please [follow the Windows 10 installation instructions](install-win10.md).</span></span>

<span data-ttu-id="b238d-106"><strong><em><span style="color: #f28014">以下说明适用于运行 Windows 10 周年更新或 Windows 10 创意者更新的用户</span></em></strong></span><span class="sxs-lookup"><span data-stu-id="b238d-106"><strong><em><span style="color: #f28014">The following instructions are for users running Windows 10 Anniversary Update or Windows 10 Creators Update</span></em></strong></span></span>

<span data-ttu-id="b238d-107">在 Windows 10 秋季创意者更新 (版本 1709) 之前, WSL 已作为 beta 功能发布, 并在第一次运行 "在 Windows 上的 Bash on Ubuntu 时安装了一个 Ubuntu 实例"。</span><span class="sxs-lookup"><span data-stu-id="b238d-107">Prior to Windows 10 Fall Creators Update (version 1709), WSL was released as a beta feature and installed a single Ubuntu instance when "Bash on Ubuntu on Windows" (or Bash.exe) was first run.</span></span>

> <span data-ttu-id="b238d-108">尽管可以在早期版本的 Windows 10 版本上使用 WSL, 但此 beta "旧发行版" 现在被视为已过时。</span><span class="sxs-lookup"><span data-stu-id="b238d-108">While you CAN use WSL on earlier Windows 10 releases, this beta "legacy distro" is now considered obsolete.</span></span> <span data-ttu-id="b238d-109">强烈建议运行最新版本的 Windows 10。</span><span class="sxs-lookup"><span data-stu-id="b238d-109">We strongly encourage you to run the most recent version of Windows 10 available.</span></span> <span data-ttu-id="b238d-110">每个新的 Windows 10 版本都单独包括 WSL 中的数百个修补程序和改进功能, 使更多的 Linux 工具和应用能够在 WSL 上正常运行。</span><span class="sxs-lookup"><span data-stu-id="b238d-110">Each new Windows 10 release includes many hundreds of fixes and improvements in WSL alone, allowing ever more Linux tools and apps to run correctly on WSL.</span></span>

<span data-ttu-id="b238d-111">如果无法升级到秋季创意者更新或更高版本, 请按照以下步骤启用和使用 WSL:</span><span class="sxs-lookup"><span data-stu-id="b238d-111">If you cannot upgrade to Fall Creators Update or later, follow the steps below to enable and use WSL:</span></span>

1. <span data-ttu-id="b238d-112">开启开发人员模式若要在 Windows 10 周年更新或创意者更新上运行 WSL, 必须启用开发人员模式:</span><span class="sxs-lookup"><span data-stu-id="b238d-112">Turn on Developer Mode  To run WSL on Windows 10 Anniversary Update or Creators Update, you must enable Developer Mode:</span></span>

    <span data-ttu-id="b238d-113">**为开发人员**打开**设置** -> **更新和安全性** -> </span><span class="sxs-lookup"><span data-stu-id="b238d-113">Open **Settings** -> **Update and Security** -> **For developers**</span></span>

    <span data-ttu-id="b238d-114">选择 "开发人员模式" 单选按钮</span><span class="sxs-lookup"><span data-stu-id="b238d-114">Select the Developer Mode radio button</span></span>  
    ![启用开发人员模式](media/updateAndSecurity.png)

    > <span data-ttu-id="b238d-116">[Windows 10 秋季创意者更新中已删除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)启用开发人员模式的要求</span><span class="sxs-lookup"><span data-stu-id="b238d-116">The requirement to enable Developer Mode was [removed in Windows 10 Fall Creators Update](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)</span></span>

1. <span data-ttu-id="b238d-117">打开命令提示符。</span><span class="sxs-lookup"><span data-stu-id="b238d-117">Open a command prompt.</span></span>  <span data-ttu-id="b238d-118">键入`bash`并按 enter</span><span class="sxs-lookup"><span data-stu-id="b238d-118">Type `bash` and hit enter</span></span>

    <span data-ttu-id="b238d-119">首次在 Windows 上的 Ubuntu 上运行 Bash 时, 系统将提示你接受规范的许可证。</span><span class="sxs-lookup"><span data-stu-id="b238d-119">The first time you run Bash on Ubuntu on Windows, you'll be prompted to accept Canonical's license.</span></span> <span data-ttu-id="b238d-120">接受后, WSL 会将 Ubuntu 实例下载并安装到计算机上, 并将在 "开始" 菜单中添加 "Bash on Ubuntu on Windows" 快捷方式。</span><span class="sxs-lookup"><span data-stu-id="b238d-120">Once accepted, WSL will download and install the Ubuntu instance onto your machine, and a "Bash on Ubuntu on Windows" shortcut will be added to your start menu.</span></span>

    ![提示安装 Ubuntu](media/bashShellInstall.png)

    <span data-ttu-id="b238d-122">首次在 Windows 上的 Ubuntu 上运行 Bash 时, 系统将提示你创建 UNIX 用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="b238d-122">The first time you run Bash on Ubuntu on Windows, you will be prompted to create a UNIX username and password.</span></span> <span data-ttu-id="b238d-123">按照[新的发行版实例说明](initialize-distro.md)完成安装</span><span class="sxs-lookup"><span data-stu-id="b238d-123">Follow the [new distro instance instructions](initialize-distro.md) to complete your installation</span></span>

1. <span data-ttu-id="b238d-124">通过以下方法之一启动新的 Ubuntu shell:</span><span class="sxs-lookup"><span data-stu-id="b238d-124">Launch a new Ubuntu shell by either:</span></span>
    * <span data-ttu-id="b238d-125">在`bash`命令提示符下运行</span><span class="sxs-lookup"><span data-stu-id="b238d-125">Running `bash` from a command-prompt</span></span>
    * <span data-ttu-id="b238d-126">单击 "开始" 菜单 "在 Windows 上打开 Ubuntu on Ubuntu" 快捷方式</span><span class="sxs-lookup"><span data-stu-id="b238d-126">Clicking the start menu "Bash on Ubuntu on Windows" shortcut</span></span>

    
## <a name="uninstallingremoving-the-legacy-distro"></a><span data-ttu-id="b238d-127">卸载/删除旧发行版</span><span class="sxs-lookup"><span data-stu-id="b238d-127">Uninstalling/Removing the legacy distro</span></span>
<span data-ttu-id="b238d-128">如果从安装了 WSL 的早期 Windows 10 版本升级到 Windows 10 秋季创意者更新, 则现有发行版将保持不变。</span><span class="sxs-lookup"><span data-stu-id="b238d-128">If you upgrade to Windows 10 Fall Creators Update from an earlier Windows 10 release upon which you installed WSL, your existing distro will remain intact.</span></span> <span data-ttu-id="b238d-129">但是, 我们强烈建议你尽快安装新的存储提供的发行版, 并将所有必要的文件、数据等从旧发行版迁移到新的发行版。</span><span class="sxs-lookup"><span data-stu-id="b238d-129">However, we STRONGLY encourage you to install a new Store-delivered distro ASAP, and migrate any necessary files, data, etc. from your legacy distro to your new distro.</span></span>

<span data-ttu-id="b238d-130">若要从计算机中删除旧的发行版, 请从命令行或 PowerShell 实例运行以下命令:</span><span class="sxs-lookup"><span data-stu-id="b238d-130">To remove the legacy distro from your machine, run the following from a Command Line or PowerShell instance:</span></span>

```console
wsl --unregister Legacy
```

<span data-ttu-id="b238d-131">如果使用的不是 Windows 版本1903或更高版本, 则可能需要`wslconfig /u Legacy`改`lxrun /uninstall /full`为运行或。</span><span class="sxs-lookup"><span data-stu-id="b238d-131">If you are not using Windows Version 1903 or higher, you may need to run `wslconfig /u Legacy` or `lxrun /uninstall /full` instead.</span></span> 

### <a name="manually-deleting-the-legacy-distro"></a><span data-ttu-id="b238d-132">手动删除旧发行版</span><span class="sxs-lookup"><span data-stu-id="b238d-132">Manually deleting the legacy distro</span></span>
<span data-ttu-id="b238d-133">如果需要, 可以手动删除旧实例。</span><span class="sxs-lookup"><span data-stu-id="b238d-133">If you wish, you can manually delete your legacy instance.</span></span> <span data-ttu-id="b238d-134">如果你在使用`lxrun.exe`卸载旧的发行版时遇到问题, 或者运行不`lxrun.exe`附带的 Windows 10 春季2018更新 (或更高版本), 则可能需要执行此操作。</span><span class="sxs-lookup"><span data-stu-id="b238d-134">This may be required if you encounter issues uninstalling the legacy distro using `lxrun.exe`, or are running Windows 10 Spring 2018 Update (or later) which do not ship with `lxrun.exe`.</span></span>

<span data-ttu-id="b238d-135">若要强制删除旧的 WSL 发行版, 请`%localappdata%\lxss\`使用 Windows 文件资源管理器或命令行删除该文件夹及其所有子内容:</span><span class="sxs-lookup"><span data-stu-id="b238d-135">To forcefully delete your legacy WSL distro, delete the `%localappdata%\lxss\` folder (and all it's sub-contents) using Windows' File Explorer, or the command-line:</span></span>

<span data-ttu-id="b238d-136">使用 PowerShell</span><span class="sxs-lookup"><span data-stu-id="b238d-136">Using PowerShell</span></span>
```powershell
rm -Recurse $env:localappdata/lxss/
```

<span data-ttu-id="b238d-137">使用 Cmd:</span><span class="sxs-lookup"><span data-stu-id="b238d-137">Using Cmd:</span></span>
```console
DEL /S %localappdata%\lxss\
```
