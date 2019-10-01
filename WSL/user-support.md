---
title: Linux 用户帐户和权限
description: 适用于 Linux 的 Windows 子系统的用户帐户和权限管理参考。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, 用户帐户
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: d8434283e459ae25637fac0c0b1877ca07d9a255
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269715"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="fd60f-104">适用于 Linux 的 Windows 子系统的用户帐户和权限</span><span class="sxs-lookup"><span data-stu-id="fd60f-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="fd60f-105">创建 Linux 用户是在 WSL 上设置新 Linux 分发版的第一步。</span><span class="sxs-lookup"><span data-stu-id="fd60f-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="fd60f-106">系统将为创建的第一个用户帐户自动配置几个特殊属性：</span><span class="sxs-lookup"><span data-stu-id="fd60f-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="fd60f-107">它是你的默认用户 - 启动时它会自动登录。</span><span class="sxs-lookup"><span data-stu-id="fd60f-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="fd60f-108">默认情况下，它是 Linux 管理员（sudo 组的成员）。</span><span class="sxs-lookup"><span data-stu-id="fd60f-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="fd60f-109">在适用于 Linux 的 Windows 子系统上运行的每个 Linux 分发版都有其自身的 Linux 用户帐户和密码。</span><span class="sxs-lookup"><span data-stu-id="fd60f-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="fd60f-110">每当添加分发版、重新安装或重置时，都必须配置一个 Linux 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="fd60f-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="fd60f-111">Linux 用户帐户不仅是每个分发版中的独立帐户，而且也独立于 Windows 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="fd60f-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="fd60f-112">重置 Linux 密码</span><span class="sxs-lookup"><span data-stu-id="fd60f-112">Resetting your Linux password</span></span>

<span data-ttu-id="fd60f-113">如果你有权访问 Linux 用户帐户并知道自己的当前密码，请使用该分发版的 Linux 密码重置工具（很有可能是 `passwd`）更改此密码。</span><span class="sxs-lookup"><span data-stu-id="fd60f-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="fd60f-114">如果无法做到这一点，也许可以根据所用的分发版，通过重置默认用户来重置密码。</span><span class="sxs-lookup"><span data-stu-id="fd60f-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="fd60f-115">WSL 提供一个默认用户标记用于确定在启动 WSL 时要自动登录哪个用户帐户。</span><span class="sxs-lookup"><span data-stu-id="fd60f-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="fd60f-116">由于许多分发包都包含了用于将默认用户设置为 root 以及未设置密码的 root 用户的命令，因此，将默认用户更改为 root 是密码重置等操作的便捷方式。</span><span class="sxs-lookup"><span data-stu-id="fd60f-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="fd60f-117">对于创意者更新和更低版本</span><span class="sxs-lookup"><span data-stu-id="fd60f-117">For Creators Update and earlier</span></span>
<span data-ttu-id="fd60f-118">如果运行的是 Windows 10 创意者更新或更低版本，可以运行以下命令来更改默认 Bash 用户：</span><span class="sxs-lookup"><span data-stu-id="fd60f-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="fd60f-119">将默认用户更改为 `root`：</span><span class="sxs-lookup"><span data-stu-id="fd60f-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="fd60f-120">运行 `bash.exe`，立即以 `root` 身份登录：</span><span class="sxs-lookup"><span data-stu-id="fd60f-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="fd60f-121">使用分发版的 password 命令重置密码，并关闭 Linux 控制台：</span><span class="sxs-lookup"><span data-stu-id="fd60f-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="fd60f-122">在 Windows CMD 中，将默认用户重置回到普通的 Linux 用户帐户：</span><span class="sxs-lookup"><span data-stu-id="fd60f-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="fd60f-123">对于 Fall Creators Update 和更高版本</span><span class="sxs-lookup"><span data-stu-id="fd60f-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="fd60f-124">若要查看哪些命令适用于特定的分发版，请运行 `[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="fd60f-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="fd60f-125">例如，在安装了 Ubuntu 的情况下：</span><span class="sxs-lookup"><span data-stu-id="fd60f-125">For example, with Ubuntu installed:</span></span>

```console
C:\> ubuntu.exe /?

Launches or configures a linux distribution.

Usage:
    <no args>
      - Launches the distro's default behavior. By default, this launches your default shell.

    run <command line>
      - Run the given command line in that distro, using the default configuration.
      - Everything after `run ` is passed to the linux LaunchProcess cal

    config [setting [value]]
      - Configure certain settings for this distro.
      - Settings are any of the following (by default)
        - `--default-user <username>`: Set the default user for this distro to <username>

    clean
      - Uninstalls the distro. The appx remains on your machine. This can be
        useful for "factory resetting" your instance. This removes the linux
        filesystem from the disk, but not the app from your PC, so you don't
        need to redownload the entire tar.gz again.

    help
      - Print this usage message.
```

<span data-ttu-id="fd60f-126">有关使用 Ubuntu 的分步说明：</span><span class="sxs-lookup"><span data-stu-id="fd60f-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="fd60f-127">打开 CMD</span><span class="sxs-lookup"><span data-stu-id="fd60f-127">Open CMD</span></span>
1. <span data-ttu-id="fd60f-128">将默认 Linux 用户设置为 `root`：</span><span class="sxs-lookup"><span data-stu-id="fd60f-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="fd60f-129">启动 Linux 分发版 (`ubuntu`)。</span><span class="sxs-lookup"><span data-stu-id="fd60f-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="fd60f-130">你将自动以 `root` 身份登录：</span><span class="sxs-lookup"><span data-stu-id="fd60f-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="fd60f-131">使用 `passwd` 命令重置密码：</span><span class="sxs-lookup"><span data-stu-id="fd60f-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="fd60f-132">在 Windows CMD 中，将默认用户重置回到普通的 Linux 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="fd60f-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="fd60f-133">权限</span><span class="sxs-lookup"><span data-stu-id="fd60f-133">Permissions</span></span>

<span data-ttu-id="fd60f-134">在 WSL 中的权限方面，请注意两个重要概念：</span><span class="sxs-lookup"><span data-stu-id="fd60f-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="fd60f-135">Windows 权限模型控制进程对 Windows 资源的权限</span><span class="sxs-lookup"><span data-stu-id="fd60f-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="fd60f-136">Linux 权限模型控制进程对 Linux 资源的权限</span><span class="sxs-lookup"><span data-stu-id="fd60f-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="fd60f-137">在 WSL 上运行 Linux 时，Linux 拥有的 Windows 权限与启动 Linux 的进程的权限相同。</span><span class="sxs-lookup"><span data-stu-id="fd60f-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="fd60f-138">可使用以下两个权限级别之一启动 Linux：</span><span class="sxs-lookup"><span data-stu-id="fd60f-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="fd60f-139">正常（未提升）：Linux 将以登录用户的权限运行</span><span class="sxs-lookup"><span data-stu-id="fd60f-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="fd60f-140">提升/管理员：Linux 以提升的/管理员 Windows 权限运行</span><span class="sxs-lookup"><span data-stu-id="fd60f-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="fd60f-141">由于权限提升的进程可以访问/修改（因而可能会损坏）系统范围的设置和系统范围/受保护的数据，因此，除非绝对必要，否则请**避免**启动权限提升的进程 - 不管它们是 Windows 还是 Linux 应用程序/工具/shell！</span><span class="sxs-lookup"><span data-stu-id="fd60f-141">Because elevated processes can access/modify (and therefore damage) system-wide settings and system-wide/protected data, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="fd60f-142">上述 Windows 权限独立于 Linux 实例中的权限：Linux“Root 特权”只影响用户在 Linux 环境和文件系统中的权限；它们不影响授予的 Windows 特权。</span><span class="sxs-lookup"><span data-stu-id="fd60f-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="fd60f-143">因此，以 root 身份运行 Linux 进程（例如，通过 `sudo`）只在 Linux 环境中为该进程授予管理员权限。</span><span class="sxs-lookup"><span data-stu-id="fd60f-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

<span data-ttu-id="fd60f-144">示例  ：  </span><span class="sxs-lookup"><span data-stu-id="fd60f-144">**Example:**  </span></span>  
<span data-ttu-id="fd60f-145">拥有 Windows 管理员特权的 Bash 会话可以访问 `cd /mnt/c/Users/Administrator`，而没有管理员特权的 Bash 会话将出现“权限被拒绝”错误。</span><span class="sxs-lookup"><span data-stu-id="fd60f-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="fd60f-146">在 Linux 中，键入 `sudo cd /mnt/c/Users/Administrator` 不会授予对管理员目录的访问权限，因为 Windows 中的权限由 Windows 管理。</span><span class="sxs-lookup"><span data-stu-id="fd60f-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="fd60f-147">在用户的权限取决于当前 Linux 用户的 Linux 环境中，Linux 权限模型非常重要。</span><span class="sxs-lookup"><span data-stu-id="fd60f-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

<span data-ttu-id="fd60f-148">**示例：**</span><span class="sxs-lookup"><span data-stu-id="fd60f-148">**Example:**</span></span>  
<span data-ttu-id="fd60f-149">sudo 组中的用户可以运行 `sudo apt update`。</span><span class="sxs-lookup"><span data-stu-id="fd60f-149">A user in the sudo group may run `sudo apt update`.</span></span>
