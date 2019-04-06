---
title: 初始化新的 WSL Linux 发行版
description: 后安装 WSL 的 Linux 发行版，请按照以下简单步骤完成初始化
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063605"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="3f581-104">初始化新安装的发行版</span><span class="sxs-lookup"><span data-stu-id="3f581-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="3f581-105">一旦下载并安装你的发行，您将需要完成初始化新的发行版：</span><span class="sxs-lookup"><span data-stu-id="3f581-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="3f581-106">启动发行版</span><span class="sxs-lookup"><span data-stu-id="3f581-106">Launch a distro</span></span>
<span data-ttu-id="3f581-107">若要完成初始化的新安装发行版，启动新实例。</span><span class="sxs-lookup"><span data-stu-id="3f581-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="3f581-108">通过单击 Windows 应用商店应用中的"启动"按钮或启动从开始菜单的发行版，可以执行此操作：</span><span class="sxs-lookup"><span data-stu-id="3f581-108">You can do this by clicking the "launch" button in the Windows Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="3f581-109">提示：你可能想要固定到开始菜单，和/或任务栏将使用频率最高发行版 ！</span><span class="sxs-lookup"><span data-stu-id="3f581-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![启动从开始菜单的发行版](media/start-menu.png)

> <span data-ttu-id="3f581-111">在 Windows 服务器上，可以启动可执行文件的发行版的启动器`<distro>.exe`发行版安装文件夹中。</span><span class="sxs-lookup"><span data-stu-id="3f581-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="3f581-112">第一次新安装的发行版运行时，的控制台窗口将打开，并将询问您等待一两分钟才能完成安装。</span><span class="sxs-lookup"><span data-stu-id="3f581-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="3f581-113">在安装此最终阶段，发行版的文件是取消压缩和存储在您 PC 上，供使用。</span><span class="sxs-lookup"><span data-stu-id="3f581-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="3f581-114">这可能需要一分钟或更多具体取决于你的电脑的存储设备的性能。</span><span class="sxs-lookup"><span data-stu-id="3f581-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="3f581-115">此初始安装阶段才需要清理的安装的发行版时所有将来的启动应采取少于一秒。</span><span class="sxs-lookup"><span data-stu-id="3f581-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="3f581-116">设置新的 Linux 用户帐户</span><span class="sxs-lookup"><span data-stu-id="3f581-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="3f581-117">安装完成后，系统会提示您创建新的用户帐户 （和其密码）。</span><span class="sxs-lookup"><span data-stu-id="3f581-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![解包 Windows 控制台中的 Ubuntu](media/UbuntuInstall.png)

<span data-ttu-id="3f581-119">此用户帐户是正常的非管理员用户，就可以登录的作为默认情况下启动发行版时。</span><span class="sxs-lookup"><span data-stu-id="3f581-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="3f581-120">可以选择任何用户名和密码想-你的 Windows 用户名没有任何关系。</span><span class="sxs-lookup"><span data-stu-id="3f581-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="3f581-121">打开新的发行版实例时，您不会被提示输入你的密码，但**如果进程使用提升`sudo`，将需要输入密码**，因此请确保你选择可以很容易记住的密码 ！</span><span class="sxs-lookup"><span data-stu-id="3f581-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="3f581-122">请参阅[用户支持](user-support.md)的详细信息页。</span><span class="sxs-lookup"><span data-stu-id="3f581-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="3f581-123">更新和升级你的发行包</span><span class="sxs-lookup"><span data-stu-id="3f581-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="3f581-124">大多数发行版所附带的最小空/包目录。</span><span class="sxs-lookup"><span data-stu-id="3f581-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="3f581-125">我们强烈建议定期更新您的包目录，并升级已安装的包使用发行版的首选的包管理器。</span><span class="sxs-lookup"><span data-stu-id="3f581-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="3f581-126">在 Debian/Ubuntu 上使用 apt:</span><span class="sxs-lookup"><span data-stu-id="3f581-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="3f581-127">Windows 不会不会自动更新或升级 Linux distro(s):这是 Linux 用户想控制自己的任务。</span><span class="sxs-lookup"><span data-stu-id="3f581-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="3f581-128">操作完成！</span><span class="sxs-lookup"><span data-stu-id="3f581-128">You're done!</span></span> <span data-ttu-id="3f581-129">喜欢在 WSL 上使用新的 Linux 发行版 ！</span><span class="sxs-lookup"><span data-stu-id="3f581-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="3f581-130">若要了解有关 WSL 的详细信息，请查看其他[WSL docs](https://aka.ms/wsldocs)，或[WSL 学习资源页面](https://aka.ms/learnwsl)。</span><span class="sxs-lookup"><span data-stu-id="3f581-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![喜欢使用 Linux 上 WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="3f581-132">疑难解答</span><span class="sxs-lookup"><span data-stu-id="3f581-132">Troubleshooting</span></span>

<span data-ttu-id="3f581-133">以下是相关的错误的建议修补程序。</span><span class="sxs-lookup"><span data-stu-id="3f581-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="3f581-134">请参阅[WSL 故障排除页](troubleshooting.md)其他常见的错误和其解决方案。</span><span class="sxs-lookup"><span data-stu-id="3f581-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="3f581-135">**安装失败，出现错误 0x8007007e**系统不支持从应用商店 Linux 时发生此错误。</span><span class="sxs-lookup"><span data-stu-id="3f581-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="3f581-136">请确保：</span><span class="sxs-lookup"><span data-stu-id="3f581-136">Make sure that:</span></span>
> * <span data-ttu-id="3f581-137">正在运行 Windows 生成 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="3f581-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="3f581-138">[检查你的生成](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="3f581-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="3f581-139">Linux 可选组件的 Windows 子系统，并重新启动计算机。</span><span class="sxs-lookup"><span data-stu-id="3f581-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="3f581-140">[请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="3f581-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
