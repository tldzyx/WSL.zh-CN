---
title: 初始化新的 WSL Linux 发行版
description: 安装适用于 WSL 的 Linux 发行版后, 请按照以下简单步骤完成初始化
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 30cb1de0a01fd46bc434061cd36794f4ece77e4b
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499299"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="a9c68-104">初始化新安装的发行版</span><span class="sxs-lookup"><span data-stu-id="a9c68-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="a9c68-105">下载并安装发行版后, 需要完成新发行版的初始化:</span><span class="sxs-lookup"><span data-stu-id="a9c68-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="a9c68-106">启动发行版</span><span class="sxs-lookup"><span data-stu-id="a9c68-106">Launch a distro</span></span>
<span data-ttu-id="a9c68-107">若要完成新安装的发行版的初始化, 请启动新的实例。</span><span class="sxs-lookup"><span data-stu-id="a9c68-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="a9c68-108">要执行此操作, 可以单击 Microsoft Store 应用中的 "启动" 按钮, 或从 "开始" 菜单启动发行版:</span><span class="sxs-lookup"><span data-stu-id="a9c68-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="a9c68-109">提示：你可能需要将最常使用的发行版固定到 "开始" 菜单, 并/或任务栏上!</span><span class="sxs-lookup"><span data-stu-id="a9c68-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![从 "开始" 菜单启动发行版](media/start-menu.png)

> <span data-ttu-id="a9c68-111">在 Windows Server 上, 可以从发行版安装文件夹启动发行版`<distro>.exe`的启动器可执行文件。</span><span class="sxs-lookup"><span data-stu-id="a9c68-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="a9c68-112">首次运行新安装的发行版时, 将打开一个控制台窗口, 系统会要求你等待一分钟或两分钟来完成安装。</span><span class="sxs-lookup"><span data-stu-id="a9c68-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="a9c68-113">在安装的最后阶段, 发行版的文件将被取消压缩并存储在你的电脑上, 随时可以使用。</span><span class="sxs-lookup"><span data-stu-id="a9c68-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="a9c68-114">这可能需要一分钟或更长时间, 具体取决于 PC 的存储设备的性能。</span><span class="sxs-lookup"><span data-stu-id="a9c68-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="a9c68-115">仅当发行版干净安装时, 才需要执行此初始安装阶段-所有将来启动的时间应不到一秒钟。</span><span class="sxs-lookup"><span data-stu-id="a9c68-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="a9c68-116">设置新的 Linux 用户帐户</span><span class="sxs-lookup"><span data-stu-id="a9c68-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="a9c68-117">安装完成后, 系统会提示创建新的用户帐户 (及其密码)。</span><span class="sxs-lookup"><span data-stu-id="a9c68-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows 控制台中的 Ubuntu 解包](media/UbuntuInstall.png)

<span data-ttu-id="a9c68-119">此用户帐户适用于默认情况下, 在启动发行版时将以默认方式登录的非管理员用户。</span><span class="sxs-lookup"><span data-stu-id="a9c68-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="a9c68-120">你可以选择所需的任何用户名和密码, 而无需使用 Windows 用户名。</span><span class="sxs-lookup"><span data-stu-id="a9c68-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="a9c68-121">当你打开新的发行版实例时, 系统不会提示你输入密码, 但**如果`sudo`使用来提升进程, 则需要输入密码**, 因此请确保选择可轻松记住的密码!</span><span class="sxs-lookup"><span data-stu-id="a9c68-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="a9c68-122">有关详细信息, 请参阅[用户支持](user-support.md)页。</span><span class="sxs-lookup"><span data-stu-id="a9c68-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="a9c68-123">更新 & 升级发行版的包</span><span class="sxs-lookup"><span data-stu-id="a9c68-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="a9c68-124">大多数发行版附带了一个空/最小包目录。</span><span class="sxs-lookup"><span data-stu-id="a9c68-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="a9c68-125">我们强烈建议定期更新包目录, 并使用发行版的首选包管理器升级已安装的包。</span><span class="sxs-lookup"><span data-stu-id="a9c68-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="a9c68-126">在 Debian/Ubuntu 上, 使用 apt:</span><span class="sxs-lookup"><span data-stu-id="a9c68-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="a9c68-127">Windows 不会自动更新或升级 Linux 发行版:这是 Linux 用户喜欢自行控制的任务。</span><span class="sxs-lookup"><span data-stu-id="a9c68-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="a9c68-128">操作完成！</span><span class="sxs-lookup"><span data-stu-id="a9c68-128">You're done!</span></span> <span data-ttu-id="a9c68-129">在 WSL 上使用新的 Linux 发行版!</span><span class="sxs-lookup"><span data-stu-id="a9c68-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="a9c68-130">若要了解有关 WSL 的详细信息, 请查看其他[WSL 文档](https://aka.ms/wsldocs)或[WSL 学习资源页](https://aka.ms/learnwsl)。</span><span class="sxs-lookup"><span data-stu-id="a9c68-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![在 WSL 上使用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="a9c68-132">疑难解答</span><span class="sxs-lookup"><span data-stu-id="a9c68-132">Troubleshooting</span></span>

<span data-ttu-id="a9c68-133">下面是相关错误和建议的修补程序。</span><span class="sxs-lookup"><span data-stu-id="a9c68-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="a9c68-134">有关其他常见错误及其解决方案, 请参阅[WSL 故障排除页](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="a9c68-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="a9c68-135">**安装失败, 出现错误 0x8007007e**当你的系统不支持应用商店中的 Linux 时, 会发生此错误。</span><span class="sxs-lookup"><span data-stu-id="a9c68-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="a9c68-136">请确保：</span><span class="sxs-lookup"><span data-stu-id="a9c68-136">Make sure that:</span></span>
> * <span data-ttu-id="a9c68-137">你正在运行 Windows 版本16215或更高版本。</span><span class="sxs-lookup"><span data-stu-id="a9c68-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="a9c68-138">[检查生成](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="a9c68-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="a9c68-139">已启用适用于 Linux 的 Windows 子系统可选组件, 并已重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="a9c68-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="a9c68-140">[请确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="a9c68-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
