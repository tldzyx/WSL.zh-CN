---
title: 初始化新的 WSL Linux 分发版
description: 安装适用于 WSL 的 Linux 分发版后，请执行以下简单步骤来完成初始化
keywords: BashOnWindows, bash, wsl, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: c33d349a6d39c325b079ccbf7ed6350bed796e33
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "71269591"
---
# <a name="initializing-a-newly-installed-distro"></a><span data-ttu-id="d7346-104">初始化新安装的分发版</span><span class="sxs-lookup"><span data-stu-id="d7346-104">Initializing a newly installed distro</span></span>
<span data-ttu-id="d7346-105">下载并安装分发版后，需要对新的分发版完成初始化：</span><span class="sxs-lookup"><span data-stu-id="d7346-105">Once your distro has been downloaded and installed, you'll need to complete initialization of the new distro:</span></span>

## <a name="launch-a-distro"></a><span data-ttu-id="d7346-106">启动分发版</span><span class="sxs-lookup"><span data-stu-id="d7346-106">Launch a distro</span></span>
<span data-ttu-id="d7346-107">若要完成新安装的分发版的初始化，请启动新实例。</span><span class="sxs-lookup"><span data-stu-id="d7346-107">To complete the initialization of your newly installed distro, launch a new instance.</span></span> <span data-ttu-id="d7346-108">为此，可以单击 Microsoft Store 应用中的“启动”按钮，或者从“开始”菜单启动分发版：</span><span class="sxs-lookup"><span data-stu-id="d7346-108">You can do this by clicking the "launch" button in the Microsoft Store app, or launching the distro from the Start menu:</span></span>

> <span data-ttu-id="d7346-109">提示：可将最常用的分发版固定到“开始”菜单和/或任务栏！</span><span class="sxs-lookup"><span data-stu-id="d7346-109">Tip: You might want to pin your most frequently used distros to your Start menu, and/or to your taskbar!</span></span>

![从“开始”菜单启动分发版](media/start-menu.png)

> <span data-ttu-id="d7346-111">在 Windows Server 上，可以从分发版的安装文件夹启动分发版的启动程序可执行文件 `<distro>.exe`。</span><span class="sxs-lookup"><span data-stu-id="d7346-111">On Windows Server, you can launch your distro's launcher executable `<distro>.exe` from the distro installation folder.</span></span>

<span data-ttu-id="d7346-112">首次运行新安装的分发版时，会打开一个控制台窗口，其中指出需要等待一两分钟时间来完成安装。</span><span class="sxs-lookup"><span data-stu-id="d7346-112">The first time a newly installed distro runs, a Console window will open, and you'll be asked to wait for a minute or two for the installation to complete.</span></span>

> <span data-ttu-id="d7346-113">在这最后一个安装阶段，分发版的文件将会解压缩，并存储在电脑上供你使用。</span><span class="sxs-lookup"><span data-stu-id="d7346-113">During this final stage of installation, the distro's files are de-compressed and stored on your PC, ready for use.</span></span> <span data-ttu-id="d7346-114">这可能需要一分钟或更长时间，具体取决于电脑存储设备的性能。</span><span class="sxs-lookup"><span data-stu-id="d7346-114">This may take around a minute or more depending on the performance of your PC's storage devices.</span></span> <span data-ttu-id="d7346-115">仅当分发版是干净安装的版本时，才需要执行此初始安装阶段 - 将来在不到一秒内即可启动分发版。</span><span class="sxs-lookup"><span data-stu-id="d7346-115">This initial installation phase is only required when a distro is clean-installed - all future launches should take less than a second.</span></span>

## <a name="setting-up-a-new-linux-user-account"></a><span data-ttu-id="d7346-116">设置新的 Linux 用户帐户</span><span class="sxs-lookup"><span data-stu-id="d7346-116">Setting up a new Linux user account</span></span>

<span data-ttu-id="d7346-117">安装完成后，系统会提示创建新的用户帐户（及其密码）。</span><span class="sxs-lookup"><span data-stu-id="d7346-117">Once installation is complete, you will be prompted to create a new user account (and its password).</span></span> 

![Windows 控制台中的 Ubuntu 解包](media/UbuntuInstall.png)

<span data-ttu-id="d7346-119">此用户帐户用于启动分发版时默认登录的非管理员用户。</span><span class="sxs-lookup"><span data-stu-id="d7346-119">This user account is for the normal non-admin user that you'll be logged-in as by default when launching a distro.</span></span>

> <span data-ttu-id="d7346-120">可根据需要选择任何用户名和密码 - 它们与 Windows 用户名无关。</span><span class="sxs-lookup"><span data-stu-id="d7346-120">You can choose any username and password you wish - they have no bearing on your Windows username.</span></span> 

<span data-ttu-id="d7346-121">打开新的分发版实例时，系统不会提示你输入密码，但**如果使用 `sudo` 提升了进程的权限，则需要输入密码**，因此请确保选择一个容易记住的密码！</span><span class="sxs-lookup"><span data-stu-id="d7346-121">When you open a new distro instance, you won't be prompted for your password, but **if you elevate a process using `sudo`, you will need to enter your password**, so make sure you choose a password you can easily remember!</span></span> <span data-ttu-id="d7346-122">有关详细信息，请参阅[用户支持](user-support.md)页。</span><span class="sxs-lookup"><span data-stu-id="d7346-122">See the [User Support](user-support.md) page for more info.</span></span>

## <a name="update--upgrade-your-distros-packages"></a><span data-ttu-id="d7346-123">更新和升级分发版的包</span><span class="sxs-lookup"><span data-stu-id="d7346-123">Update & upgrade your distro's packages</span></span>

<span data-ttu-id="d7346-124">大多数分发版随附了一个空的/精简的包目录。</span><span class="sxs-lookup"><span data-stu-id="d7346-124">Most distros ship with an empty/minimal package catalog.</span></span> <span data-ttu-id="d7346-125">我们强烈建议定期更新包目录，并使用分发版的首选包管理器升级已安装的包。</span><span class="sxs-lookup"><span data-stu-id="d7346-125">We strongly recommend regularly updating your package catalog, and upgrading your installed packages using your distro's preferred package manager.</span></span> <span data-ttu-id="d7346-126">在 Debian/Ubuntu 上使用 apt：</span><span class="sxs-lookup"><span data-stu-id="d7346-126">On Debian/Ubuntu, you use apt:</span></span>

```bash
sudo apt update && sudo apt upgrade
```

> <span data-ttu-id="d7346-127">Windows 不会自动更新或升级 Linux 分发版：Linux 用户往往倾向于自行控制此任务。</span><span class="sxs-lookup"><span data-stu-id="d7346-127">Windows does not automatically update or upgrade your Linux distro(s): This is a task that the Linux users prefer to control themselves.</span></span>

<span data-ttu-id="d7346-128">大功告成！</span><span class="sxs-lookup"><span data-stu-id="d7346-128">You're done!</span></span> <span data-ttu-id="d7346-129">现在，可以在 WSL 上享用新的 Linux 分发版！</span><span class="sxs-lookup"><span data-stu-id="d7346-129">Enjoy using your new Linux distro on WSL!</span></span> <span data-ttu-id="d7346-130">若要详细了解 WSL，请查看其他 [WSL 文档](https://aka.ms/wsldocs)或 [WSL 学习资源页](https://aka.ms/learnwsl)。</span><span class="sxs-lookup"><span data-stu-id="d7346-130">To learn more about WSL, review the other [WSL docs](https://aka.ms/wsldocs), or the [WSL learning resources page](https://aka.ms/learnwsl).</span></span>

![在 WSL 上享用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a><span data-ttu-id="d7346-132">疑难解答</span><span class="sxs-lookup"><span data-stu-id="d7346-132">Troubleshooting</span></span>

<span data-ttu-id="d7346-133">下面是相关的错误和建议的修复措施。</span><span class="sxs-lookup"><span data-stu-id="d7346-133">Below are related errors and suggested fixes.</span></span> <span data-ttu-id="d7346-134">有关其他常见错误及其解决方法，请参阅 [WSL 故障排除页](troubleshooting.md)。</span><span class="sxs-lookup"><span data-stu-id="d7346-134">Refer to the [WSL troubleshooting page](troubleshooting.md) for other common errors and their solutions.</span></span>

> <span data-ttu-id="d7346-135">**安装失败并出现错误 0x8007007e** 如果系统不支持从 Store 安装的 Linux，则会出现此错误。</span><span class="sxs-lookup"><span data-stu-id="d7346-135">**Installation failed with error 0x8007007e** This error occurs when your system doesn't support Linux from the store.</span></span>  <span data-ttu-id="d7346-136">请确保：</span><span class="sxs-lookup"><span data-stu-id="d7346-136">Make sure that:</span></span>
> * <span data-ttu-id="d7346-137">运行 Windows 内部版本 16215 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="d7346-137">You're running Windows build 16215 or later.</span></span> <span data-ttu-id="d7346-138">[检查内部版本](troubleshooting.md#check-your-build-number)。</span><span class="sxs-lookup"><span data-stu-id="d7346-138">[Check your build](troubleshooting.md#check-your-build-number).</span></span>
> * <span data-ttu-id="d7346-139">已启用“适用于 Linux 的 Windows 子系统”可选组件，并已重启计算机。</span><span class="sxs-lookup"><span data-stu-id="d7346-139">The Windows Subsystem for Linux optional component is enabled and the computer has restarted.</span></span>  <span data-ttu-id="d7346-140">[确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。</span><span class="sxs-lookup"><span data-stu-id="d7346-140">[Make sure WSL is enabled](troubleshooting.md#confirm-wsl-is-enabled).</span></span>
