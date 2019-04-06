---
title: Linux 用户帐户和权限
description: 用户帐户和权限管理与适用于 Linux 的 Windows 子系统的参考资料。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 用户帐户的 windows 子系统
author: scooley
ms.author: scooley
ms.date: 09/11/2017
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.openlocfilehash: 5820d701d5c0e22f14bf76e3dc6fe70bacb5213a
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063595"
---
# <a name="user-accounts-and-permissions-for-windows-subsystem-for-linux"></a><span data-ttu-id="b5cb1-104">用户帐户和适用于 Linux 的 Windows 子系统权限</span><span class="sxs-lookup"><span data-stu-id="b5cb1-104">User Accounts and Permissions for Windows Subsystem for Linux</span></span>

<span data-ttu-id="b5cb1-105">创建 Linux 用户是设置新的 Linux 分发上 WSL 的第一步。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-105">Creating your Linux user is the first step in setting up a new Linux distribution on WSL.</span></span>  <span data-ttu-id="b5cb1-106">您创建的第一个用户帐户可通过几个特殊属性自动配置：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-106">The first user account you create is automatically configured with a few special attributes:</span></span>

1. <span data-ttu-id="b5cb1-107">它是默认用户--它登录自动启动。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-107">It is your default user -- it signs-in automatically on launch.</span></span>
1. <span data-ttu-id="b5cb1-108">Linux 管理员 （sudo 组的成员） 默认情况下它。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-108">It is Linux administrator (a member of the sudo group) by default.</span></span>

<span data-ttu-id="b5cb1-109">在适用于 Linux 的 Windows 子系统上运行每个 Linux 分发版都有自己的 Linux 用户帐户和密码。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="b5cb1-110">必须将配置添加分发、 重新安装，或重置任何时间的 Linux 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-110">You will have to configure a Linux user account any time you add a distribution, reinstall, or reset.</span></span>  <span data-ttu-id="b5cb1-111">Linux 用户帐户不只是每个分布区独立，它们也是独立于您的 Windows 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-111">Linux user accounts are not only independent per distribution, they are also independent from your Windows user account.</span></span>

## <a name="resetting-your-linux-password"></a><span data-ttu-id="b5cb1-112">重置 Linux 密码</span><span class="sxs-lookup"><span data-stu-id="b5cb1-112">Resetting your Linux password</span></span>

<span data-ttu-id="b5cb1-113">如果您为 Linux 用户帐户具有访问权限并且知道当前的密码，将其更改使用 Linux 密码重置该分发-最可能的工具`passwd`。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-113">If you have access to your Linux user account and know your current password, change it using Linux password reset tools of that distribution -- most likely `passwd`.</span></span>

<span data-ttu-id="b5cb1-114">如果这是未一个选项，具体取决于分发，你可以通过重置默认用户重置密码。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-114">If that's not an option, depending on the distribution, you may be able to reset your password by resetting the default user.</span></span>

<span data-ttu-id="b5cb1-115">WSL 提供了默认用户标记以标识哪些用户帐户自动登录时启动 WSL。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-115">WSL offers a default user tag to identify which user account automatically logs in when you start a WSL.</span></span>  <span data-ttu-id="b5cb1-116">由于许多分发包括命令，以对根和根用户的默认用户设置与设置密码，更改为根的默认用户是一个方便的工具，密码重置之类的内容。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-116">Since many distributions include commands to set the default user to root and also a root user with no password set, changing the default user to root is a handy tool for things like password reset.</span></span>

### <a name="for-creators-update-and-earlier"></a><span data-ttu-id="b5cb1-117">针对创意者更新及更早版本</span><span class="sxs-lookup"><span data-stu-id="b5cb1-117">For Creators Update and earlier</span></span>
<span data-ttu-id="b5cb1-118">如果您在运行 Windows 10 创意者更新或更早版本，可以通过运行以下命令更改默认 Bash 用户：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-118">If you're running Windows 10 Creators update or earlier, you can change the default Bash user by running the following commands:</span></span>

1. <span data-ttu-id="b5cb1-119">更改到的默认用户`root`:</span><span class="sxs-lookup"><span data-stu-id="b5cb1-119">Change the default user to `root`:</span></span>

    ```console
    C:\> lxrun /setdefaultuser root
    ```

1. <span data-ttu-id="b5cb1-120">运行`bash.exe`现在以用户身份登录到`root`:</span><span class="sxs-lookup"><span data-stu-id="b5cb1-120">Run `bash.exe` to now login as `root`:</span></span>

    ```console
    C:\> bash.exe
    ```

1. <span data-ttu-id="b5cb1-121">重置密码使用的分布时密码命令，然后关闭 Linux 控制台：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-121">Reset your password using the distribution's password command, and close the Linux Console:</span></span>

    ```BASH
    $ passwd username
    $ exit
    ```

1. <span data-ttu-id="b5cb1-122">从 Windows 命令行重置回正常的 Linux 用户帐户的默认用户：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-122">From Windows CMD, reset your default user back to your normal Linux user account:</span></span>

    ```console
    C:\> lxrun.exe /setdefaultuser username
    ```

### <a name="for-fall-creators-update-and-later"></a><span data-ttu-id="b5cb1-123">Fall Creators Update 及更高版本</span><span class="sxs-lookup"><span data-stu-id="b5cb1-123">For Fall Creators Update and later</span></span>
<span data-ttu-id="b5cb1-124">若要查看哪些命令适用于特定的分发，请运行`[distro.exe] /?`。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-124">To see what commands are available for a particular distribution, run `[distro.exe] /?`.</span></span>
    
<span data-ttu-id="b5cb1-125">例如，使用 Ubuntu 安装：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-125">For example, with Ubuntu installed:</span></span>

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

<span data-ttu-id="b5cb1-126">通过逐步介绍了如何使用 Ubuntu 单步：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-126">Step by step instructions using Ubuntu:</span></span>

1. <span data-ttu-id="b5cb1-127">打开 CMD</span><span class="sxs-lookup"><span data-stu-id="b5cb1-127">Open CMD</span></span>
1. <span data-ttu-id="b5cb1-128">默认 Linux 用户设置为`root`:</span><span class="sxs-lookup"><span data-stu-id="b5cb1-128">Set the default Linux user to `root`:</span></span>

    ```console
    C:\> ubuntu config --default-user root
    ```    

1. <span data-ttu-id="b5cb1-129">启动你的 Linux 分发 (`ubuntu`)。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-129">Launch your Linux distribution (`ubuntu`).</span></span>  <span data-ttu-id="b5cb1-130">自动将以用户身份登录`root`:</span><span class="sxs-lookup"><span data-stu-id="b5cb1-130">You will automatically login as `root`:</span></span>

1. <span data-ttu-id="b5cb1-131">重置应用密码使用`passwd`命令：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-131">Reset your password using the `passwd` command:</span></span>

    ```BASH
    $ passwd username
    ```

1. <span data-ttu-id="b5cb1-132">从 Windows 命令行重置回正常的 Linux 用户帐户的默认用户。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-132">From Windows CMD, reset your default user back to your normal Linux user account.</span></span>

    ```console
    C:\> ubuntu config --default-user username
    ```

## <a name="permissions"></a><span data-ttu-id="b5cb1-133">权限</span><span class="sxs-lookup"><span data-stu-id="b5cb1-133">Permissions</span></span>

<span data-ttu-id="b5cb1-134">有两个在 WSL 中的权限时，需要注意的重要概念：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-134">There are two important concepts to keep in mind when it comes to permissions in WSL:</span></span>

1. <span data-ttu-id="b5cb1-135">Windows 权限模型控制 Windows 资源的进程的权限</span><span class="sxs-lookup"><span data-stu-id="b5cb1-135">The Windows permission model governs a process' rights to Windows resources</span></span>
2. <span data-ttu-id="b5cb1-136">Linux 权限模型控制 Linux 资源的进程的权限</span><span class="sxs-lookup"><span data-stu-id="b5cb1-136">The Linux permission model controls a process' rights to Linux resources</span></span>

<span data-ttu-id="b5cb1-137">在 WSL 中运行 Linux，Linux 会将它启动的进程相同的 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-137">When running Linux on WSL, Linux will have the same Windows permissions as the process that launches it.</span></span> <span data-ttu-id="b5cb1-138">Linux 可以启动两个权限级别之一：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-138">Linux can be launched in one of two permission levels:</span></span>

* <span data-ttu-id="b5cb1-139">正常 （非提升）：使用的登录的用户权限运行的 Linux</span><span class="sxs-lookup"><span data-stu-id="b5cb1-139">Normal (non-elevated): Linux runs with the permissions of the logged-in user</span></span>
* <span data-ttu-id="b5cb1-140">提升/管理员：使用提升/管理的 Windows 权限运行的 Linux</span><span class="sxs-lookup"><span data-stu-id="b5cb1-140">Elevated/admin: Linux runs with elevated/admin Windows permissions</span></span>

> <span data-ttu-id="b5cb1-141">因为，提升的进程可以更改/损坏系统范围的设置和数据，和可以访问/修改受保护的文件和文件夹，**避免**启动提升的进程，除非绝对必要的-无论是 Windows 或Linux 应用程序/tools/shell ！</span><span class="sxs-lookup"><span data-stu-id="b5cb1-141">Because that elevated processes can change/damage system-wide settings and data, and can access/modify protected files and folders, **AVOID** launching elevated processes unless you absolutely have to - whether they're Windows or Linux applications/tools/shells!</span></span>

<span data-ttu-id="b5cb1-142">更高版本的 Windows 权限是独立的 Linux 实例中的权限：Linux"Root 权限"只影响在 Linux 环境和文件系统; 中的用户的权限它们将不会影响对授予的 Windows 特权。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-142">The above Windows permissions are independent of the permissions within a Linux instance: Linux "Root privileges" only impact the user’s rights within the Linux environment & filesystem; they have no impact on the Windows privileges granted.</span></span> <span data-ttu-id="b5cb1-143">因此，以根身份运行 Linux 进程 (例如通过`sudo`) 仅处理在 Linux 环境中的管理员权限的授予。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-143">Thus, running a Linux process as root (e.g. via `sudo`) only grants that process admin rights within the Linux environment.</span></span>

**<span data-ttu-id="b5cb1-144">例如：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-144">Example:</span></span>**    
<span data-ttu-id="b5cb1-145">具有 Windows 管理员权限的 Bash 会话可以访问`cd /mnt/c/Users/Administrator`没有管理员权限会看到"权限被拒绝"错误而 Bash 会话。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-145">A Bash session with Windows admin privileges may access `cd /mnt/c/Users/Administrator` while a Bash session without admin privileges would see a "Permission Denied" error.</span></span>

<span data-ttu-id="b5cb1-146">在 Linux 中，键入`sudo cd /mnt/c/Users/Administrator`将授予对管理员的目录访问权限，因为 Windows 内的权限管理的 Windows。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-146">In Linux, typing `sudo cd /mnt/c/Users/Administrator` will not grant access to the Administrator’s directory since permissions within Windows are managed by Windows.</span></span>

<span data-ttu-id="b5cb1-147">Linux 权限模型很重要时在用户具有基于当前的 Linux 用户的权限在 Linux 环境中。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-147">The Linux permission model is important when inside the Linux environment where the user has permissions based on the current Linux user.</span></span>

**<span data-ttu-id="b5cb1-148">例如：</span><span class="sxs-lookup"><span data-stu-id="b5cb1-148">Example:</span></span>**  
<span data-ttu-id="b5cb1-149">Sudo 组中的用户可能会运行`sudo apt update`。</span><span class="sxs-lookup"><span data-stu-id="b5cb1-149">A user in the sudo group may run `sudo apt update`.</span></span>
