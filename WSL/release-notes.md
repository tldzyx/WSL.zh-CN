---
title: 适用于 Linux 的 Windows 子系统的发行说明
description: 适用于 Linux 的 Windows 子系统的发行说明。  每周更新。
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: e2d9d5fc70c173e9b516ab7af01599b623b40b39
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2019
ms.locfileid: "67042422"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="46d6e-105">适用于 Linux 的 Windows 子系统的发行说明</span><span class="sxs-lookup"><span data-stu-id="46d6e-105">Release Notes for Windows Subsystem for Linux</span></span>


## <a name="build-18917"></a><span data-ttu-id="46d6e-106">生成18917</span><span class="sxs-lookup"><span data-stu-id="46d6e-106">Build 18917</span></span>
<span data-ttu-id="46d6e-107">有关生成18917的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-107">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-108">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-108">WSL</span></span>
* <span data-ttu-id="46d6e-109">WSL 2 现已可用!</span><span class="sxs-lookup"><span data-stu-id="46d6e-109">WSL 2 is now available!</span></span> <span data-ttu-id="46d6e-110">有关更多详细信息, 请参阅[博客](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-110">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="46d6e-111">解决通过符号链接启动 Windows 进程时无法正常工作的回归 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="46d6e-111">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="46d6e-112">将 wsl--list--verbose、wsl--list--quiet 和 wsl--import--import-</span><span class="sxs-lookup"><span data-stu-id="46d6e-112">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="46d6e-113">添加 wsl--shutdown 选项</span><span class="sxs-lookup"><span data-stu-id="46d6e-113">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="46d6e-114">计划 9:允许打开目录进行写入成功</span><span class="sxs-lookup"><span data-stu-id="46d6e-114">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="46d6e-115">生成18890</span><span class="sxs-lookup"><span data-stu-id="46d6e-115">Build 18890</span></span>
<span data-ttu-id="46d6e-116">有关生成18890的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-116">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-117">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-117">WSL</span></span>
* <span data-ttu-id="46d6e-118">非阻塞套接字泄露 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="46d6e-118">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="46d6e-119">到 terminal 的 EOF 输入会阻止后续读取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="46d6e-119">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="46d6e-120">更新 resolv.conf 标头以引用 wsl [在 GH 3928 中讨论]</span><span class="sxs-lookup"><span data-stu-id="46d6e-120">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="46d6e-121">Epoll 删除代码中的死锁 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="46d6e-121">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="46d6e-122">处理中的空格--import 和– export [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="46d6e-122">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="46d6e-123">扩展 mmap 的文件无法正常工作 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="46d6e-123">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="46d6e-124">解决 ARM64 \\wsl $ access 无法正常工作的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-124">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="46d6e-125">为 wsl 添加更好的默认图标</span><span class="sxs-lookup"><span data-stu-id="46d6e-125">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="46d6e-126">生成18342</span><span class="sxs-lookup"><span data-stu-id="46d6e-126">Build 18342</span></span>
<span data-ttu-id="46d6e-127">有关生成18342的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-127">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-128">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-128">WSL</span></span>
* <span data-ttu-id="46d6e-129">我们添加了一项功能, 使用户能够从 Windows 访问 WSL 发行版中的 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-129">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="46d6e-130">可以通过命令行访问这些文件, 并且 Windows 应用 (如文件资源管理器、VSCode 等) 可与这些文件进行交互。</span><span class="sxs-lookup"><span data-stu-id="46d6e-130">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="46d6e-131">通过\\\\ \\导航到\\wsl $ < distro_name > 访问文件, 或通过导航到 wsl $ 查看正在运行的分发的列表\\</span><span class="sxs-lookup"><span data-stu-id="46d6e-131">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="46d6e-132">添加额外的 CPU 信息标记并修复 Cpus_allowed [_list] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="46d6e-132">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="46d6e-133">支持非前导线程中的 exec [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="46d6e-133">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="46d6e-134">将配置更新失败视为非致命的 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="46d6e-134">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="46d6e-135">更新 binfmt 以正确处理偏移量 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="46d6e-135">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="46d6e-136">为计划9启用映射网络驱动器 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="46d6e-136">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="46d6e-137">支持 Windows > Linux 和 Linux-> 用于绑定装载的 Windows 路径转换</span><span class="sxs-lookup"><span data-stu-id="46d6e-137">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="46d6e-138">为以只读打开的文件中的映射创建只读部分</span><span class="sxs-lookup"><span data-stu-id="46d6e-138">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="46d6e-139">生成18334</span><span class="sxs-lookup"><span data-stu-id="46d6e-139">Build 18334</span></span>
<span data-ttu-id="46d6e-140">有关生成18334的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-140">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-141">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-141">WSL</span></span>
* <span data-ttu-id="46d6e-142">重新设计 Windows 时区映射到 Linux 时区的方式 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="46d6e-142">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="46d6e-143">修复内存泄漏并添加新的字符串转换函数 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="46d6e-143">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="46d6e-144">不带线程的 threadgroup 上的 SIGCONT 是一种无操作 [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="46d6e-144">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="46d6e-145">正确显示/proc/self/fd 中的套接字和 epoll 文件描述符</span><span class="sxs-lookup"><span data-stu-id="46d6e-145">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="46d6e-146">生成18305</span><span class="sxs-lookup"><span data-stu-id="46d6e-146">Build 18305</span></span>
<span data-ttu-id="46d6e-147">有关生成18305的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-147">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-148">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-148">WSL</span></span>
* <span data-ttu-id="46d6e-149">主线程退出时, pthreads 将失去对文件的访问权限 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="46d6e-149">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="46d6e-150">除非需要, 否则 TIOCSCTTY 应忽略 "force" 参数 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="46d6e-150">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="46d6e-151">wsl 命令行改进并添加了导入/导出功能。</span><span class="sxs-lookup"><span data-stu-id="46d6e-151">wsl.exe command line improvements and addition of import / export functionality.</span></span>
```
Usage: wsl.exe [Argument] [Options...] [CommandLine]

Arguments to run Linux binaries:

    If no command line is provided, wsl.exe launches the default shell.

    --exec, -e <CommandLine>
        Execute the specified command without using the default Linux shell.

    --
        Pass the remaining command line as is.

Options:
    --distribution, -d <DistributionName>
        Run the specified distribution.

    --user, -u <UserName>
        Run as the specified user.

Arguments to manage Windows Subsystem for Linux:

    --export <DistributionName> <FileName>
        Exports the distribution to a tar file.
        The filename can be - for standard output.

    --import <DistributionName> <InstallLocation> <FileName>
        Imports the specified tar file as a new distribution.
        The filename can be - for standard input.

    --list, -l [Options]
        Lists distributions.

        Options:
            --all
                List all distributions, including distributions that are currently
                being installed or uninstalled.

            --running
                List only distributions that are currently running.

    -setdefault, -s <DistributionName>
        Sets the distribution as the default.

    --terminate, -t <DistributionName>
        Terminates the distribution.

    --unregister <DistributionName>
        Unregisters the distribution.

    --upgrade <DistributionName>
        Upgrades the distribution to the WslFs file system format.

    --help
        Display usage information.
```

## <a name="build-18277"></a><span data-ttu-id="46d6e-152">生成18277</span><span class="sxs-lookup"><span data-stu-id="46d6e-152">Build 18277</span></span>
<span data-ttu-id="46d6e-153">有关生成18277的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-153">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-154">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-154">WSL</span></span>
* <span data-ttu-id="46d6e-155">修复了生成 18272 [GH 3645] 中引入的 "不支持此类接口" 错误</span><span class="sxs-lookup"><span data-stu-id="46d6e-155">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="46d6e-156">忽略卸载 syscall [GH 3605] 的 MNT_FORCE 标志</span><span class="sxs-lookup"><span data-stu-id="46d6e-156">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="46d6e-157">切换 WSL 互操作以使用官方 CreatePseudoConsole API</span><span class="sxs-lookup"><span data-stu-id="46d6e-157">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="46d6e-158">FUTEX_WAIT 重新启动时保持无超时值</span><span class="sxs-lookup"><span data-stu-id="46d6e-158">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="46d6e-159">生成18272</span><span class="sxs-lookup"><span data-stu-id="46d6e-159">Build 18272</span></span>
<span data-ttu-id="46d6e-160">有关生成18272的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-160">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-161">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-161">WSL</span></span>
* <span data-ttu-id="46d6e-162">**警告：** 在此版本中, 导致 WSL 不可操作的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-162">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="46d6e-163">尝试启动分发时, 将看到 "不支持此类接口" 错误。</span><span class="sxs-lookup"><span data-stu-id="46d6e-163">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="46d6e-164">此问题已修复, 将在下一周的预览体验期内提供。</span><span class="sxs-lookup"><span data-stu-id="46d6e-164">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="46d6e-165">如果已安装此版本, 则可以使用 "设置-> 更新 & 安全 > 恢复", 在 "设置-更新" 中回滚到以前的 Windows 版本。</span><span class="sxs-lookup"><span data-stu-id="46d6e-165">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="46d6e-166">生成18267</span><span class="sxs-lookup"><span data-stu-id="46d6e-166">Build 18267</span></span>
<span data-ttu-id="46d6e-167">有关生成18267的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-167">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-168">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-168">WSL</span></span>
* <span data-ttu-id="46d6e-169">修复了傀儡过程不会 reaped 并始终处于无限期的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-169">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="46d6e-170">如果错误消息超过最大长度, 则 WslRegisterDistribution 挂起 [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="46d6e-170">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="46d6e-171">允许 fsync 对 DrvFs 上的只读文件成功 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="46d6e-171">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="46d6e-172">在 [GH 3584] 中创建符号链接之前, 请确保/bin 和/sbin 目录存在</span><span class="sxs-lookup"><span data-stu-id="46d6e-172">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="46d6e-173">添加了 WSL 实例的实例终止超时机制。</span><span class="sxs-lookup"><span data-stu-id="46d6e-173">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="46d6e-174">超时值当前设置为15秒, 这意味着实例将在上一个 WSL 进程退出15秒后终止。</span><span class="sxs-lookup"><span data-stu-id="46d6e-174">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="46d6e-175">若要立即终止分发, 请使用:</span><span class="sxs-lookup"><span data-stu-id="46d6e-175">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="46d6e-176">版本 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="46d6e-176">Build 17763 (1809)</span></span>
<span data-ttu-id="46d6e-177">有关生成17763的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-177">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-178">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-178">WSL</span></span>
* <span data-ttu-id="46d6e-179">Setpriority syscall 权限检查太严格, 无法更改相同的线程优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="46d6e-179">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="46d6e-180">确保使用无偏差中断时间进行启动时间, 以避免返回 clock_gettime (CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="46d6e-180">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="46d6e-181">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="46d6e-181">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="46d6e-182">更好地处理 threadgroup 前导文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="46d6e-182">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="46d6e-183">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter 来避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="46d6e-183">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="46d6e-184">Ptrace attach 可能会导致来自系统调用的错误返回值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="46d6e-184">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="46d6e-185">解决几个 AF_UNIX 相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="46d6e-185">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="46d6e-186">修复了以下问题: 如果当前工作目录长度少于5个字符, 则可能导致 WSL 互操作失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="46d6e-186">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="46d6e-187">避免与不存在的端口发生环回连接时出现一秒钟延迟失败 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="46d6e-187">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="46d6e-188">添加/proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="46d6e-188">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="46d6e-189">更准确的 IPV6 作用域信息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-189">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="46d6e-190">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="46d6e-190">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="46d6e-191">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="46d6e-191">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="46d6e-192">通过 NTFS 符号启动的 Win32 可执行文件不遵守符号名称 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="46d6e-192">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="46d6e-193">改善了傀儡支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="46d6e-193">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="46d6e-194">添加 wsl 项以控制 Windows 互操作行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="46d6e-194">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="46d6e-195">修复 getsockname not always 返回 UNIX 套接字系列类型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="46d6e-195">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="46d6e-196">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="46d6e-196">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="46d6e-197">连接过程中的非阻止套接字应为写入尝试返回 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="46d6e-197">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="46d6e-198">支持已装入 Vhd 上的互操作 [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="46d6e-198">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="46d6e-199">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="46d6e-199">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="46d6e-200">对 TTY 键盘 ioctls KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-200">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="46d6e-201">即使在后台启动, 也应执行 Windows UI 应用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-201">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="46d6e-202">添加 wsl 或--user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="46d6e-202">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="46d6e-203">启用快速启动时修复 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="46d6e-203">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="46d6e-204">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="46d6e-204">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="46d6e-205">非阻止 Unix 套接字通过 EAGAIN 无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="46d6e-205">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="46d6e-206">case = off 是新的默认 drvfs 装载类型 [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="46d6e-206">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="46d6e-207">有关详细信息, 请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-207">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="46d6e-208">添加 wslconfig/terminate 以停止正在运行的分发。</span><span class="sxs-lookup"><span data-stu-id="46d6e-208">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="46d6e-209">解决了无法正确处理带有空格的路径的 WSL shell 上下文菜单项的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-209">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="46d6e-210">公开作为扩展属性的每目录大小写敏感度</span><span class="sxs-lookup"><span data-stu-id="46d6e-210">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="46d6e-211">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="46d6e-211">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="46d6e-212">解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-212">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="46d6e-213">DrvFs: 只有专用范围中对应于转义字符的 unescape 字符。</span><span class="sxs-lookup"><span data-stu-id="46d6e-213">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="46d6e-214">修复 ELF 分析器解释器长度验证 [GH 3154] 中的一个错误</span><span class="sxs-lookup"><span data-stu-id="46d6e-214">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="46d6e-215">WSL 包含过去时间的绝对计时器 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="46d6e-215">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="46d6e-216">确保新创建的重新分析点在父目录中列出为这样。</span><span class="sxs-lookup"><span data-stu-id="46d6e-216">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="46d6e-217">以原子方式创建 DrvFs 中的区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="46d6e-217">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="46d6e-218">修复了一个额外的问题, 即即使文件存在, 多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="46d6e-218">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="46d6e-219">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="46d6e-219">[GH 2712]</span></span>
* <span data-ttu-id="46d6e-220">修复了 UMCI 启用时的 WSL 启动失败。</span><span class="sxs-lookup"><span data-stu-id="46d6e-220">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="46d6e-221">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="46d6e-221">[GH 3020]</span></span>
* <span data-ttu-id="46d6e-222">添加浏览器上下文菜单以启动 WSL [GH 437, 603, 1836]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-222">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="46d6e-223">若要使用, 请在浏览器窗口中按住 shift 键并右键单击。</span><span class="sxs-lookup"><span data-stu-id="46d6e-223">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="46d6e-224">修复 Unix 套接字非阻止行为 [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="46d6e-224">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="46d6e-225">修复 GH 2026 中报告的挂起 NETLINK 命令。</span><span class="sxs-lookup"><span data-stu-id="46d6e-225">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="46d6e-226">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-226">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="46d6e-227">修复了截断不会导致 inotify 事件 [GH 2978] 的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-227">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="46d6e-228">添加--exec 选项, 用于 wsl, 以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-228">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="46d6e-229">添加--wsl 的分发选项, 以选择特定的发行版。</span><span class="sxs-lookup"><span data-stu-id="46d6e-229">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="46d6e-230">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-230">Limited support for dmesg.</span></span> <span data-ttu-id="46d6e-231">现在, 应用程序可以登录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="46d6e-231">Applications can now log to dmesg.</span></span> <span data-ttu-id="46d6e-232">WSL 驱动程序将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="46d6e-232">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="46d6e-233">将来, 可以通过扩展此功能从驱动程序携带其他信息/诊断。</span><span class="sxs-lookup"><span data-stu-id="46d6e-233">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="46d6e-234">注意: 当前支持通过`/dev/kmsg`设备接口进行 dmesg。</span><span class="sxs-lookup"><span data-stu-id="46d6e-234">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="46d6e-235">`syslog`目前尚不支持 syscall 接口。</span><span class="sxs-lookup"><span data-stu-id="46d6e-235">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="46d6e-236">而且, 某些`dmesg`命令行选项`-S`(如) `-C`不起作用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-236">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="46d6e-237">更改串行设备的默认 gid 和模式以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="46d6e-237">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="46d6e-238">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="46d6e-238">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="46d6e-239">注意:DrvFs 对扩展属性的名称有一些限制。</span><span class="sxs-lookup"><span data-stu-id="46d6e-239">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="46d6e-240">不允许使用某些字符 (如 "/"、":\*" 和 ""), 并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="46d6e-240">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="46d6e-241">生成 18252 (向前跳过)</span><span class="sxs-lookup"><span data-stu-id="46d6e-241">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="46d6e-242">有关生成18252的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-242">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-243">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-243">WSL</span></span>
* <span data-ttu-id="46d6e-244">将 init 和 bsdtar 二进制文件从 lxssmanager dll 移到单独的工具文件夹中</span><span class="sxs-lookup"><span data-stu-id="46d6e-244">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="46d6e-245">解决使用 CLONE_FILES 时关闭文件描述符的争用</span><span class="sxs-lookup"><span data-stu-id="46d6e-245">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="46d6e-246">转换 DrvFs 路径时处理/proc/pid/mountinfo 中的可选字段</span><span class="sxs-lookup"><span data-stu-id="46d6e-246">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="46d6e-247">允许 DrvFs mknod 成功而不支持 S_IFREG 的元数据</span><span class="sxs-lookup"><span data-stu-id="46d6e-247">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="46d6e-248">在 DrvFs 上创建的 readonly 文件应具有 readonly 属性集 [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="46d6e-248">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="46d6e-249">添加/sbin/mount.drvfs helper 以处理 DrvFs 挂载</span><span class="sxs-lookup"><span data-stu-id="46d6e-249">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="46d6e-250">在 DrvFs 中使用 POSIX rename。</span><span class="sxs-lookup"><span data-stu-id="46d6e-250">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="46d6e-251">允许无卷 GUID 的卷上的路径转换。</span><span class="sxs-lookup"><span data-stu-id="46d6e-251">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="46d6e-252">生成 17738 (快速)</span><span class="sxs-lookup"><span data-stu-id="46d6e-252">Build 17738 (Fast)</span></span>
<span data-ttu-id="46d6e-253">有关生成17738的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-253">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-254">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-254">WSL</span></span>
* <span data-ttu-id="46d6e-255">Setpriority syscall 权限检查太严格, 无法更改相同的线程优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="46d6e-255">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="46d6e-256">确保使用无偏差中断时间进行启动时间, 以避免返回 clock_gettime (CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="46d6e-256">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="46d6e-257">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="46d6e-257">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="46d6e-258">更好地处理 threadgroup 前导文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="46d6e-258">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="46d6e-259">生成 17728 (快速)</span><span class="sxs-lookup"><span data-stu-id="46d6e-259">Build 17728 (Fast)</span></span>
<span data-ttu-id="46d6e-260">有关生成17728的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-260">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-261">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-261">WSL</span></span>
* <span data-ttu-id="46d6e-262">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter 来避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="46d6e-262">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="46d6e-263">Ptrace attach 可能会导致来自系统调用的错误返回值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="46d6e-263">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="46d6e-264">解决与 AF_UNIX 相关的问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="46d6e-264">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="46d6e-265">修复了以下问题: 如果当前工作目录长度少于5个字符, 则可能导致 WSL 互操作失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="46d6e-265">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="46d6e-266">生成 18204 (向前跳过)</span><span class="sxs-lookup"><span data-stu-id="46d6e-266">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="46d6e-267">有关生成18204的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-267">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-268">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-268">WSL</span></span>
* <span data-ttu-id="46d6e-269">管道文件系统 inadvertenly 清除边缘-触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="46d6e-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="46d6e-270">通过 NTFS 符号启动的 Win32 可执行文件不遵守符号名称 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="46d6e-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="46d6e-271">生成 17723 (快速)</span><span class="sxs-lookup"><span data-stu-id="46d6e-271">Build 17723 (Fast)</span></span>
<span data-ttu-id="46d6e-272">有关生成17723的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-272">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-273">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-273">WSL</span></span>
* <span data-ttu-id="46d6e-274">避免与不存在的端口发生环回连接时出现一秒钟延迟失败 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="46d6e-274">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="46d6e-275">添加/proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="46d6e-275">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="46d6e-276">更准确的 IPV6 作用域信息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-276">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="46d6e-277">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="46d6e-277">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="46d6e-278">管道文件系统 inadvertenly 清除边缘-触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="46d6e-278">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="46d6e-279">通过 NTFS 符号启动的 Win32 可执行文件不遵守符号名称 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="46d6e-279">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="46d6e-280">生成17713</span><span class="sxs-lookup"><span data-stu-id="46d6e-280">Build 17713</span></span>
<span data-ttu-id="46d6e-281">有关生成17713的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-281">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-282">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-282">WSL</span></span>
* <span data-ttu-id="46d6e-283">改善了傀儡支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="46d6e-283">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="46d6e-284">添加 wsl 项以控制 Windows 互操作行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="46d6e-284">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="46d6e-285">修复 getsockname not always 返回 UNIX 套接字系列类型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="46d6e-285">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="46d6e-286">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="46d6e-286">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="46d6e-287">连接过程中的非阻止套接字应为写入尝试返回 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="46d6e-287">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="46d6e-288">支持已装入 Vhd 上的互操作 [GH 3246, 3291]</span><span class="sxs-lookup"><span data-stu-id="46d6e-288">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="46d6e-289">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="46d6e-289">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="46d6e-290">对 TTY 键盘 ioctls KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-290">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="46d6e-291">即使在后台启动, 也应执行 Windows UI 应用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-291">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="46d6e-292">生成17704</span><span class="sxs-lookup"><span data-stu-id="46d6e-292">Build 17704</span></span>
<span data-ttu-id="46d6e-293">有关生成17704的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-293">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-294">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-294">WSL</span></span>
* <span data-ttu-id="46d6e-295">添加 wsl 或--user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="46d6e-295">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="46d6e-296">启用快速启动时修复 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="46d6e-296">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="46d6e-297">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="46d6e-297">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="46d6e-298">非阻止 Unix 套接字通过 EAGAIN 无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="46d6e-298">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="46d6e-299">case = off 是新的默认 drvfs 装载类型 [GH 2937, 3212, 3328]</span><span class="sxs-lookup"><span data-stu-id="46d6e-299">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="46d6e-300">有关详细信息, 请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-300">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="46d6e-301">添加 wslconfig/terminate 以停止正在运行的分发。</span><span class="sxs-lookup"><span data-stu-id="46d6e-301">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="46d6e-302">版本 17692</span><span class="sxs-lookup"><span data-stu-id="46d6e-302">Build 17692</span></span>
<span data-ttu-id="46d6e-303">有关生成17692的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-303">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-304">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-304">WSL</span></span>
* <span data-ttu-id="46d6e-305">解决了无法正确处理带有空格的路径的 WSL shell 上下文菜单项的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-305">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="46d6e-306">公开作为扩展属性的每目录大小写敏感度</span><span class="sxs-lookup"><span data-stu-id="46d6e-306">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="46d6e-307">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="46d6e-307">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="46d6e-308">解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-308">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="46d6e-309">DrvFs: 只有专用范围中对应于转义字符的 unescape 字符。</span><span class="sxs-lookup"><span data-stu-id="46d6e-309">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="46d6e-310">版本 17686</span><span class="sxs-lookup"><span data-stu-id="46d6e-310">Build 17686</span></span>
<span data-ttu-id="46d6e-311">有关生成17686的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-311">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-312">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-312">WSL</span></span>
* <span data-ttu-id="46d6e-313">修复 ELF 分析器解释器长度验证 [GH 3154] 中的一个错误</span><span class="sxs-lookup"><span data-stu-id="46d6e-313">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="46d6e-314">WSL 包含过去时间的绝对计时器 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="46d6e-314">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="46d6e-315">确保新创建的重新分析点在父目录中列出为这样。</span><span class="sxs-lookup"><span data-stu-id="46d6e-315">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="46d6e-316">以原子方式创建 DrvFs 中的区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="46d6e-316">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="46d6e-317">生成17677</span><span class="sxs-lookup"><span data-stu-id="46d6e-317">Build 17677</span></span>
<span data-ttu-id="46d6e-318">有关生成17677的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-318">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-319">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-319">WSL</span></span>
* <span data-ttu-id="46d6e-320">修复了一个额外的问题, 即即使文件存在, 多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="46d6e-320">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="46d6e-321">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="46d6e-321">[GH 2712]</span></span>
* <span data-ttu-id="46d6e-322">修复了 UMCI 启用时的 WSL 启动失败。</span><span class="sxs-lookup"><span data-stu-id="46d6e-322">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="46d6e-323">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="46d6e-323">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="46d6e-324">生成17666</span><span class="sxs-lookup"><span data-stu-id="46d6e-324">Build 17666</span></span>
<span data-ttu-id="46d6e-325">有关生成17666的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-325">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-326">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-326">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="46d6e-327">警告：某些 AMD 芯片组上出现阻止 WSL 运行的问题 [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-327">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="46d6e-328">修补程序已准备就绪, 并将其转移到有问必答生成分支。</span><span class="sxs-lookup"><span data-stu-id="46d6e-328">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="46d6e-329">添加浏览器上下文菜单以启动 WSL [GH 437, 603, 1836]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-329">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="46d6e-330">在资源管理器窗口中使用按住 shift 键并右键单击。</span><span class="sxs-lookup"><span data-stu-id="46d6e-330">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="46d6e-331">修复 unix 套接字非阻止行为 [GH 2822, 3100]</span><span class="sxs-lookup"><span data-stu-id="46d6e-331">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="46d6e-332">修复 GH 2026 中报告的挂起 NETLINK 命令。</span><span class="sxs-lookup"><span data-stu-id="46d6e-332">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="46d6e-333">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-333">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="46d6e-334">修复了截断不会导致 inotify 事件 [GH 2978] 的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-334">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="46d6e-335">添加--exec 选项, 用于 wsl, 以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-335">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="46d6e-336">添加--wsl 的分发选项, 以选择特定的发行版。</span><span class="sxs-lookup"><span data-stu-id="46d6e-336">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="46d6e-337">生成 17655 (向前跳过)</span><span class="sxs-lookup"><span data-stu-id="46d6e-337">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="46d6e-338">有关生成17655的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-338">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-339">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-339">WSL</span></span>
* <span data-ttu-id="46d6e-340">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-340">Limited support for dmesg.</span></span> <span data-ttu-id="46d6e-341">现在, 应用程序可以登录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="46d6e-341">Applications can now log to dmesg.</span></span> <span data-ttu-id="46d6e-342">WSL 驱动程序将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="46d6e-342">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="46d6e-343">将来, 可以通过扩展此功能从驱动程序携带其他信息/诊断。</span><span class="sxs-lookup"><span data-stu-id="46d6e-343">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="46d6e-344">注意: 当前支持通过`/dev/kmsg`设备接口进行 dmesg。</span><span class="sxs-lookup"><span data-stu-id="46d6e-344">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="46d6e-345">`syslog`尚不支持 sycall 接口。</span><span class="sxs-lookup"><span data-stu-id="46d6e-345">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="46d6e-346">而且, 某些`dmesg`命令行选项`-S`(如) `-C`不起作用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-346">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="46d6e-347">修复了即使文件存在, 多线程操作可以返回 ENOENT 的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-347">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="46d6e-348">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="46d6e-348">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="46d6e-349">生成 17639 (向前跳过)</span><span class="sxs-lookup"><span data-stu-id="46d6e-349">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="46d6e-350">有关生成17639的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-350">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-351">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-351">WSL</span></span>
* <span data-ttu-id="46d6e-352">更改串行设备的默认 gid 和模式以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="46d6e-352">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="46d6e-353">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="46d6e-353">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="46d6e-354">注意:DrvFs 对扩展属性的名称有一些限制。</span><span class="sxs-lookup"><span data-stu-id="46d6e-354">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="46d6e-355">特别是, 不允许使用某些字符 (如 "/"、":\*" 和 ""), 并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="46d6e-355">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="46d6e-356">生成 17133 (快速)</span><span class="sxs-lookup"><span data-stu-id="46d6e-356">Build 17133 (Fast)</span></span>
<span data-ttu-id="46d6e-357">有关生成17133的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-357">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-358">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-358">WSL</span></span>
* <span data-ttu-id="46d6e-359">修复 WSL 中的挂起问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-359">Fix for hang in WSL.</span></span> <span data-ttu-id="46d6e-360">[GH 3039, 3034]</span><span class="sxs-lookup"><span data-stu-id="46d6e-360">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="46d6e-361">生成 17128 (快速)</span><span class="sxs-lookup"><span data-stu-id="46d6e-361">Build 17128 (Fast)</span></span>
<span data-ttu-id="46d6e-362">有关生成17128的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-362">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-363">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-363">WSL</span></span>
* <span data-ttu-id="46d6e-364">无</span><span class="sxs-lookup"><span data-stu-id="46d6e-364">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="46d6e-365">生成 17627 (向前跳过)</span><span class="sxs-lookup"><span data-stu-id="46d6e-365">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="46d6e-366">有关生成17627的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-366">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-367">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-367">WSL</span></span>
* <span data-ttu-id="46d6e-368">添加对 futex pi 感知操作的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-368">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="46d6e-369">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="46d6e-369">[GH 1006]</span></span>
    * <span data-ttu-id="46d6e-370">请注意, 目前不支持优先级, 因此存在一些限制, 但应解除标准使用的 WSL。</span><span class="sxs-lookup"><span data-stu-id="46d6e-370">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="46d6e-371">Windows 防火墙对 WSL 进程的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-371">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="46d6e-372">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="46d6e-372">[GH 1852]</span></span>
    * <span data-ttu-id="46d6e-373">例如, 若要允许 WSL python 进程侦听任何端口, 请使用提升的 Windows cmd:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="46d6e-373">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="46d6e-374">有关如何添加防火墙规则的其他详细信息, 请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="46d6e-374">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="46d6e-375">使用 wsl 时, 请尊重用户的默认外壳。</span><span class="sxs-lookup"><span data-stu-id="46d6e-375">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="46d6e-376">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="46d6e-376">[GH 2372]</span></span>
* <span data-ttu-id="46d6e-377">将所有网络接口报告为以太网。</span><span class="sxs-lookup"><span data-stu-id="46d6e-377">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="46d6e-378">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="46d6e-378">[GH 2996]</span></span>
* <span data-ttu-id="46d6e-379">更好地处理损坏的/etc/passwd 文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-379">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="46d6e-380">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="46d6e-380">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-381">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-381">Console</span></span>
* <span data-ttu-id="46d6e-382">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-382">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-383">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-383">LTP Results:</span></span>
<span data-ttu-id="46d6e-384">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-384">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="46d6e-385">生成 17618 (向前跳过)</span><span class="sxs-lookup"><span data-stu-id="46d6e-385">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="46d6e-386">有关生成17618的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-386">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-387">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-387">WSL</span></span>
* <span data-ttu-id="46d6e-388">介绍用于 NT 互操作的 pseudoconsole 功能 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-388">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="46d6e-389">旧安装机制 (lxrun) 已弃用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-389">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="46d6e-390">安装分发的支持机制是通过 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="46d6e-390">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-391">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-391">Console</span></span>
* <span data-ttu-id="46d6e-392">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-392">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-393">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-393">LTP Results:</span></span>
<span data-ttu-id="46d6e-394">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-394">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="46d6e-395">版本 17110</span><span class="sxs-lookup"><span data-stu-id="46d6e-395">Build 17110</span></span>
<span data-ttu-id="46d6e-396">有关生成17110的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-396">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-397">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-397">WSL</span></span>
* <span data-ttu-id="46d6e-398">允许从 Windows 终止/init [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-398">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="46d6e-399">默认情况下, DrvFs 在默认情况下使用每个目录的区分大小写 (相当于 "case = dir" 装载选项)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-399">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="46d6e-400">使用 "case = force" (旧行为) 需要设置注册表项。</span><span class="sxs-lookup"><span data-stu-id="46d6e-400">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="46d6e-401">如果需要使用, 请运行以下命令启用 "case = force": reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="46d6e-401">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="46d6e-402">如果在较早版本的 Windows 中使用 WSL 创建了现有目录 (需要区分大小写), 请使用 dism.exe 将它们标记为区分大小写: setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="46d6e-402">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="46d6e-403">NULL 终止从 uname syscall 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="46d6e-403">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-404">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-404">Console</span></span>
* <span data-ttu-id="46d6e-405">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-405">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-406">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-406">LTP Results:</span></span>
<span data-ttu-id="46d6e-407">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-407">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="46d6e-408">生成17107</span><span class="sxs-lookup"><span data-stu-id="46d6e-408">Build 17107</span></span>
<span data-ttu-id="46d6e-409">有关生成17107的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-409">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-410">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-410">WSL</span></span>
* <span data-ttu-id="46d6e-411">支持在 master pty 终结点上的 TCSETSF 和 TCSETSW [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-411">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="46d6e-412">启动并发互操作进程可能会导致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-412">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="46d6e-413">修复 PTRACE_ATTACH 以在/proc/pid/status. 中显示正确的跟踪状态</span><span class="sxs-lookup"><span data-stu-id="46d6e-413">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="46d6e-414">修复了在不清除 TID 地址的情况下, 通过 CLEARTID 和 SETTID 标志克隆的生存期较短的进程可能退出的争用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-414">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="46d6e-415">在从17093之前的版本迁移时, 在升级 Linux 文件系统目录时显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-415">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="46d6e-416">有关17093文件系统更改的更多详细信息, 请参阅[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)的发行说明。</span><span class="sxs-lookup"><span data-stu-id="46d6e-416">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-417">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-417">Console</span></span>
* <span data-ttu-id="46d6e-418">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-418">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-419">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-419">LTP Results:</span></span>
<span data-ttu-id="46d6e-420">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-420">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="46d6e-421">生成17101</span><span class="sxs-lookup"><span data-stu-id="46d6e-421">Build 17101</span></span>
<span data-ttu-id="46d6e-422">有关生成17101的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-422">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-423">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-423">WSL</span></span>
* <span data-ttu-id="46d6e-424">支持 signalfd。</span><span class="sxs-lookup"><span data-stu-id="46d6e-424">Support for signalfd.</span></span> <span data-ttu-id="46d6e-425">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="46d6e-425">[GH 129]</span></span>
* <span data-ttu-id="46d6e-426">支持包含非法 NTFS 字符的文件名, 方法是将它们编码为私有 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="46d6e-426">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="46d6e-427">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="46d6e-427">[GH 1514]</span></span>
* <span data-ttu-id="46d6e-428">当不支持写入时, 自动装入将回退为只读。</span><span class="sxs-lookup"><span data-stu-id="46d6e-428">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="46d6e-429">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="46d6e-429">[GH 2603]</span></span>
* <span data-ttu-id="46d6e-430">允许粘贴 Unicode 代理项对 (如表情符号)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-430">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="46d6e-431">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="46d6e-431">[GH 2765]</span></span>
* <span data-ttu-id="46d6e-432">/Proc 和/sys 中的伪文件应从 select、轮询、epoll、et al 返回读取和写入准备就绪。 [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="46d6e-432">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="46d6e-433">修复问题: 当注册表被篡改或损坏时, 可能导致服务进入无限循环。</span><span class="sxs-lookup"><span data-stu-id="46d6e-433">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="46d6e-434">修复 netlink 消息以使用 iproute2 的更新版本 (上游 4.14)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-434">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-435">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-435">Console</span></span>
* <span data-ttu-id="46d6e-436">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-436">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-437">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-437">LTP Results:</span></span>
<span data-ttu-id="46d6e-438">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-438">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="46d6e-439">生成17093</span><span class="sxs-lookup"><span data-stu-id="46d6e-439">Build 17093</span></span>
<span data-ttu-id="46d6e-440">有关生成17093的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-440">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="46d6e-441">重要提示：</span><span class="sxs-lookup"><span data-stu-id="46d6e-441">Important:</span></span>
<span data-ttu-id="46d6e-442">升级到此版本后首次启动 WSL 时, 需要执行一些操作来升级 Linux 文件系统目录。</span><span class="sxs-lookup"><span data-stu-id="46d6e-442">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="46d6e-443">这可能需要几分钟, 因此 WSL 的启动速度可能会很慢。</span><span class="sxs-lookup"><span data-stu-id="46d6e-443">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="46d6e-444">对于从应用商店中安装的每个分发, 此操作应只发生一次。</span><span class="sxs-lookup"><span data-stu-id="46d6e-444">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="46d6e-445">改进了 DrvFs 中的区分大小写支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-445">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="46d6e-446">DrvFs 现在支持每个目录的区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-446">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="46d6e-447">这是一种新的标志, 可对目录进行设置, 以指示应将这些目录中的所有操作视为区分大小写, 甚至允许 Windows 应用程序正确打开仅大小写不同的文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-447">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="46d6e-448">DrvFs 有新的装载选项, 这些选项控制每个目录的区分大小写</span><span class="sxs-lookup"><span data-stu-id="46d6e-448">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="46d6e-449">case = force: 所有目录都被视为区分大小写 (驱动器根除外)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-449">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="46d6e-450">用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-450">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="46d6e-451">这是旧的行为, 但将新目录标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-451">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="46d6e-452">case = dir: 只有具有每个目录大小写区分标志的目录才被视为区分大小写;其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-452">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="46d6e-453">用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-453">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="46d6e-454">case = off: 仅将具有每个目录大小写敏感度标志的目录视为区分大小写;其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-454">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="46d6e-455">用 WSL 创建的新目录标记为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-455">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="46d6e-456">注意: 以前版本中的 WSL 创建的目录未设置此标志, 因此, 如果使用 "case = dir" 选项, 则不会将其视为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-456">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="46d6e-457">即将推出一种在现有目录上设置此标志的方法。</span><span class="sxs-lookup"><span data-stu-id="46d6e-457">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="46d6e-458">装载这些选项的示例 (对于现有驱动器, 必须先卸载, 然后才能装载不同选项): sudo mount-t drvfs C:/mnt/c-o case = dir</span><span class="sxs-lookup"><span data-stu-id="46d6e-458">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="46d6e-459">目前, case = force 仍是默认选项。</span><span class="sxs-lookup"><span data-stu-id="46d6e-459">For now, case=force is still the default option.</span></span> <span data-ttu-id="46d6e-460">以后将更改为 case = dir。</span><span class="sxs-lookup"><span data-stu-id="46d6e-460">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="46d6e-461">你现在可以在安装 DrvFs 时使用 Windows 路径中的正斜杠, 例如: sudo mount-t DrvFs//server/share/mnt/share</span><span class="sxs-lookup"><span data-stu-id="46d6e-461">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="46d6e-462">WSL 现在会在实例启动期间处理/etc/fstab 文件 [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-462">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="46d6e-463">这是在自动装载 DrvFs 驱动器之前完成的;fstab 已装载的任何驱动器都不会自动重新装载, 使你可以更改特定驱动器的装入点。</span><span class="sxs-lookup"><span data-stu-id="46d6e-463">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="46d6e-464">使用 wsl 可以关闭此行为。</span><span class="sxs-lookup"><span data-stu-id="46d6e-464">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="46d6e-465">/Proc 中的 mount、mountinfo 和 mountstats 文件正确地转义特殊字符, 如反斜杠和空格 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="46d6e-465">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="46d6e-466">启用元数据后, 通过 DrvFs 创建的特殊文件 (如 WSL 符号链接或 fifos 和套接字) 现在可以从 Windows 复制和移动。</span><span class="sxs-lookup"><span data-stu-id="46d6e-466">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="46d6e-467">WSL 更易于配置 WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-467">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="46d6e-468">添加了一种方法, 用于在 WSL 中自动配置某些功能, 这些功能将在每次启动子系统时应用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-468">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="46d6e-469">这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="46d6e-469">This includes automount options and network configuration.</span></span> <span data-ttu-id="46d6e-470">在博客文章中了解更多相关信息: https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="46d6e-470">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="46d6e-471">AF_UNIX 允许在 WSL 和 Windows 本机进程上的 Linux 进程之间进行套接字连接</span><span class="sxs-lookup"><span data-stu-id="46d6e-471">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="46d6e-472">现在, WSL 和 Windows 应用程序可以通过 Unix 套接字彼此通信。</span><span class="sxs-lookup"><span data-stu-id="46d6e-472">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="46d6e-473">假设你想要在 Windows 中运行服务, 并使其可用于 Windows 和 WSL 应用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-473">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="46d6e-474">现在, 可以通过 Unix 套接字实现。</span><span class="sxs-lookup"><span data-stu-id="46d6e-474">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="46d6e-475">有关详细信息, 请阅读我们的博客文章 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="46d6e-475">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-476">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-476">WSL</span></span>
* <span data-ttu-id="46d6e-477">支持带有 MAP_NORESERVE 的 mmap () [GH 121, 2784]</span><span class="sxs-lookup"><span data-stu-id="46d6e-477">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="46d6e-478">支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="46d6e-478">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="46d6e-479">处理克隆中的非 SIGCHLD 终止信号 [GH 121, 2781]</span><span class="sxs-lookup"><span data-stu-id="46d6e-479">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="46d6e-480">存根/proc/sys/fs/inotify/max_user_instances 和/proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="46d6e-480">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="46d6e-481">加载包含非零偏移量的负载标头的 ELF 二进制文件时出错 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="46d6e-481">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="46d6e-482">加载图像时, 为零个尾随页字节。</span><span class="sxs-lookup"><span data-stu-id="46d6e-482">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="46d6e-483">减少 execve 以静默方式终止进程的情况</span><span class="sxs-lookup"><span data-stu-id="46d6e-483">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-484">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-484">Console</span></span>
* <span data-ttu-id="46d6e-485">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-485">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-486">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-486">LTP Results:</span></span>
<span data-ttu-id="46d6e-487">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-487">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="46d6e-488">版本 17083</span><span class="sxs-lookup"><span data-stu-id="46d6e-488">Build 17083</span></span>
<span data-ttu-id="46d6e-489">有关生成17083的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-489">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-490">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-490">WSL</span></span>
* <span data-ttu-id="46d6e-491">修复了与 epoll 相关的检测错误 [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="46d6e-491">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="46d6e-492">修复了关闭 ASLR 时挂起 [GH 1185, 2870]</span><span class="sxs-lookup"><span data-stu-id="46d6e-492">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="46d6e-493">确保 mmap 操作出现原子 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="46d6e-493">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-494">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-494">Console</span></span>
* <span data-ttu-id="46d6e-495">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-496">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-496">LTP Results:</span></span>
<span data-ttu-id="46d6e-497">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-497">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="46d6e-498">生成17074</span><span class="sxs-lookup"><span data-stu-id="46d6e-498">Build 17074</span></span>
<span data-ttu-id="46d6e-499">有关生成17074的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-499">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-500">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-500">WSL</span></span>
* <span data-ttu-id="46d6e-501">固定存储格式的 DrvFs 元数据 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="46d6e-501">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="46d6e-502">**重要说明：** 在此生成之前创建的 DrvFs 元数据将错误显示或根本不显示。</span><span class="sxs-lookup"><span data-stu-id="46d6e-502">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="46d6e-503">若要修复受影响的文件, 请使用 chmod 和 chown 重新应用元数据。</span><span class="sxs-lookup"><span data-stu-id="46d6e-503">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="46d6e-504">修复了多个信号和可重启 syscall 的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-504">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-505">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-505">Console</span></span>
* <span data-ttu-id="46d6e-506">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-506">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-507">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-507">LTP Results:</span></span>
<span data-ttu-id="46d6e-508">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-508">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="46d6e-509">生成17063</span><span class="sxs-lookup"><span data-stu-id="46d6e-509">Build 17063</span></span>
<span data-ttu-id="46d6e-510">有关生成17063的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-510">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="46d6e-511">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-511">WSL</span></span>
* <span data-ttu-id="46d6e-512">DrvFs 支持其他 Linux 元数据。</span><span class="sxs-lookup"><span data-stu-id="46d6e-512">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="46d6e-513">这允许使用 chmod/chown 设置文件的所有者和模式, 还可以创建特殊文件 (如 fifos、unix 套接字和设备文件)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-513">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="46d6e-514">默认情况下, 此功能处于禁用状态, 因为它仍在实验中。</span><span class="sxs-lookup"><span data-stu-id="46d6e-514">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="46d6e-515">**注意：** 修复了 DrvFs 使用的元数据格式的错误。</span><span class="sxs-lookup"><span data-stu-id="46d6e-515">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="46d6e-516">当元数据在此生成上适用于试验时, 将来的生成将无法正确读取此生成创建的元数据。</span><span class="sxs-lookup"><span data-stu-id="46d6e-516">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="46d6e-517">你可能需要手动更新已修改文件的所有者, 并且必须重新创建具有自定义设备 ID 的设备。</span><span class="sxs-lookup"><span data-stu-id="46d6e-517">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="46d6e-518">若要启用, 请使用 metadata 选项装载 DrvFs (若要在现有装载上启用它, 必须先卸载它):</span><span class="sxs-lookup"><span data-stu-id="46d6e-518">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="46d6e-519">Linux 权限作为附加的元数据添加到文件;它们不会影响 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="46d6e-519">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="46d6e-520">请记住, 使用 Windows 编辑器编辑文件可能会删除元数据。</span><span class="sxs-lookup"><span data-stu-id="46d6e-520">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="46d6e-521">在这种情况下, 该文件将恢复为默认权限。</span><span class="sxs-lookup"><span data-stu-id="46d6e-521">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="46d6e-522">向 DrvFs 添加了装载选项, 以控制没有元数据的文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-522">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="46d6e-523">uid: 用于所有文件所有者的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="46d6e-523">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="46d6e-524">gid: 用于所有文件的所有者的组 ID。</span><span class="sxs-lookup"><span data-stu-id="46d6e-524">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="46d6e-525">umask: 要排除所有文件和目录的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-525">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="46d6e-526">fmask: 为所有常规文件排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-526">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="46d6e-527">dmask: 为所有目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-527">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="46d6e-528">例如：</span><span class="sxs-lookup"><span data-stu-id="46d6e-528">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="46d6e-529">与 metadata 选项结合, 可指定没有元数据的文件的默认权限。</span><span class="sxs-lookup"><span data-stu-id="46d6e-529">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="46d6e-530">引入了一个新的环境`WSLENV`变量, 用于配置环境变量在 WSL 和 Win32 之间的流动方式。</span><span class="sxs-lookup"><span data-stu-id="46d6e-530">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="46d6e-531">例如：</span><span class="sxs-lookup"><span data-stu-id="46d6e-531">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="46d6e-532">`WSLENV`以冒号分隔的环境变量列表, 可以在从 WSL 启动 Win32 或 Win32 进程中的 WSL 进程时包含这些变量。</span><span class="sxs-lookup"><span data-stu-id="46d6e-532">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="46d6e-533">每个变量可以用斜杠 (后跟标志) 作为后缀, 以指定它的转换方式。</span><span class="sxs-lookup"><span data-stu-id="46d6e-533">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="46d6e-534">h-p值是应在 WSL 路径与 Win32 路径之间进行转换的路径。</span><span class="sxs-lookup"><span data-stu-id="46d6e-534">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="46d6e-535">l值是路径的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-535">l: The value is a list of paths.</span></span> <span data-ttu-id="46d6e-536">在 WSL 中, 它是用冒号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-536">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="46d6e-537">在 Win32 中, 它是一个以分号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-537">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="46d6e-538">形仅应在从 Win32 调用 WSL 时包含值</span><span class="sxs-lookup"><span data-stu-id="46d6e-538">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="46d6e-539">水平仅应在从 WSL 调用 Win32 时包括该值</span><span class="sxs-lookup"><span data-stu-id="46d6e-539">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="46d6e-540">可以在 .bashrc `WSLENV`中或在用户的自定义 Windows 环境中设置。</span><span class="sxs-lookup"><span data-stu-id="46d6e-540">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="46d6e-541">drvfs 装入正确保留 tar、cp-p (GH 1939) 的时间戳</span><span class="sxs-lookup"><span data-stu-id="46d6e-541">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="46d6e-542">drvfs 符号链接报告正确大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="46d6e-542">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="46d6e-543">读/写适用于非常大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="46d6e-543">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="46d6e-544">waitpid 适用于进程组 Id (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="46d6e-544">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="46d6e-545">显著提高了大型保留区域的 mmap 性能;提高 ghc 性能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="46d6e-545">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="46d6e-546">个性支持 READ_IMPLIES_EXEC;修复最大值和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="46d6e-546">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="46d6e-547">mprotect 支持 PROT_GROWSDOWN;修补 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="46d6e-547">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="46d6e-548">过载模式下的页错误修复;修补 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="46d6e-548">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="46d6e-549">克隆支持更多标志组合</span><span class="sxs-lookup"><span data-stu-id="46d6e-549">clone supports more flags combinations</span></span>
* <span data-ttu-id="46d6e-550">支持 epoll 文件的 select/epoll (以前为无操作)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-550">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="46d6e-551">通知 ptrace 未实现的 syscall。</span><span class="sxs-lookup"><span data-stu-id="46d6e-551">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="46d6e-552">生成 resolv.conf 名称服务器时忽略未启动的接口 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="46d6e-552">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="46d6e-553">枚举没有物理地址的网络接口。</span><span class="sxs-lookup"><span data-stu-id="46d6e-553">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="46d6e-554">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="46d6e-554">[GH 2685]</span></span>
* <span data-ttu-id="46d6e-555">其他 bug 修复和改进。</span><span class="sxs-lookup"><span data-stu-id="46d6e-555">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="46d6e-556">适用于 Windows 上的开发人员的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="46d6e-556">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="46d6e-557">Windows 命令行工具链包括 bsdtar (tar) 和曲线。</span><span class="sxs-lookup"><span data-stu-id="46d6e-557">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="46d6e-558">阅读[此博客](https://aka.ms/tarcurlwindows), 了解有关添加这两个新工具的详细信息, 并了解如何在 Windows 上形成开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="46d6e-558">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="46d6e-559">`AF_UNIX`适用于 Windows 有问必答 SDK (17061 +)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-559">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="46d6e-560">阅读[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), 了解有关如何`AF_UNIX`在 Windows 上使用开发人员以及如何使用它的详细信息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-560">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="46d6e-561">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-561">Console</span></span>
* <span data-ttu-id="46d6e-562">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-563">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-563">LTP Results:</span></span>
<span data-ttu-id="46d6e-564">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-564">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="46d6e-565">生成17046</span><span class="sxs-lookup"><span data-stu-id="46d6e-565">Build 17046</span></span>

<span data-ttu-id="46d6e-566">有关生成17046的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-566">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="46d6e-567">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-567">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-568">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-568">WSL</span></span>
- <span data-ttu-id="46d6e-569">允许在没有活动终端的情况下运行进程。</span><span class="sxs-lookup"><span data-stu-id="46d6e-569">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="46d6e-570">[GH 709, 1007, 1511, 2252, 2391, et al]</span><span class="sxs-lookup"><span data-stu-id="46d6e-570">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="46d6e-571">更好地支持 CLONE_VFORK 和 CLONE_VM。</span><span class="sxs-lookup"><span data-stu-id="46d6e-571">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="46d6e-572">[GH 1878, 2615]</span><span class="sxs-lookup"><span data-stu-id="46d6e-572">[GH 1878, 2615]</span></span>
- <span data-ttu-id="46d6e-573">跳过 WSL 网络操作的 TDI 筛选器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-573">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="46d6e-574">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="46d6e-574">[GH 1554]</span></span>
- <span data-ttu-id="46d6e-575">满足某些条件时, DrvFs 将创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="46d6e-575">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="46d6e-576">[GH 353, 1475, 2602]</span><span class="sxs-lookup"><span data-stu-id="46d6e-576">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="46d6e-577">链接目标必须是相对的, 不能跨任何装入点或符号链接, 并且必须存在。</span><span class="sxs-lookup"><span data-stu-id="46d6e-577">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="46d6e-578">用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (这通常需要你启动 wsl), 除非已打开开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="46d6e-578">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="46d6e-579">在所有其他情况下, DrvFs 仍创建 WSL 符号链接。</span><span class="sxs-lookup"><span data-stu-id="46d6e-579">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="46d6e-580">允许同时运行提升和非提升的 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="46d6e-580">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="46d6e-581">支持/proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="46d6e-581">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="46d6e-582">添加 wslpath 以执行 WSL < > Windows 路径转换。</span><span class="sxs-lookup"><span data-stu-id="46d6e-582">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="46d6e-583">[GH 522, 1243, 1834, 2327, et al]</span><span class="sxs-lookup"><span data-stu-id="46d6e-583">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="46d6e-584">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-584">Console</span></span>
- <span data-ttu-id="46d6e-585">无修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-585">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-586">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-586">LTP Results:</span></span>
<span data-ttu-id="46d6e-587">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-587">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="46d6e-588">生成17040</span><span class="sxs-lookup"><span data-stu-id="46d6e-588">Build 17040</span></span>

<span data-ttu-id="46d6e-589">有关生成17040的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-589">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-590">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-591">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-591">WSL</span></span>
- <span data-ttu-id="46d6e-592">自17035以来没有修复。</span><span class="sxs-lookup"><span data-stu-id="46d6e-592">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-593">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-593">Console</span></span>
- <span data-ttu-id="46d6e-594">自17035以来没有修复。</span><span class="sxs-lookup"><span data-stu-id="46d6e-594">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-595">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-595">LTP Results:</span></span>
<span data-ttu-id="46d6e-596">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-596">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="46d6e-597">生成17035</span><span class="sxs-lookup"><span data-stu-id="46d6e-597">Build 17035</span></span>

<span data-ttu-id="46d6e-598">有关生成17035的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-598">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-599">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-599">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-600">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-600">WSL</span></span>
- <span data-ttu-id="46d6e-601">访问 DrvFs 上的文件有时会因 EINVAL 而失败。</span><span class="sxs-lookup"><span data-stu-id="46d6e-601">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="46d6e-602">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="46d6e-602">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-603">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-603">Console</span></span>
- <span data-ttu-id="46d6e-604">在 VT 模式下插入/删除行时的一些颜色损失。</span><span class="sxs-lookup"><span data-stu-id="46d6e-604">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-605">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-605">LTP Results:</span></span>
<span data-ttu-id="46d6e-606">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-606">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="46d6e-607">生成17025</span><span class="sxs-lookup"><span data-stu-id="46d6e-607">Build 17025</span></span>

<span data-ttu-id="46d6e-608">有关生成17025的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-608">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-609">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-609">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-610">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-610">WSL</span></span>
- <span data-ttu-id="46d6e-611">启动新的前台进程组中的初始进程 [GH 1653, 2510]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-611">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="46d6e-612">SIGHUP 传递修复 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-612">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="46d6e-613">如果未提供, 则生成默认的虚拟桥名称 [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-613">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="46d6e-614">实现/proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-614">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="46d6e-615">更多互操作 stdout/stderr 管道修补程序。</span><span class="sxs-lookup"><span data-stu-id="46d6e-615">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="46d6e-616">存根 syncfs 系统调用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-616">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-617">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-617">Console</span></span>
- <span data-ttu-id="46d6e-618">修复第三方控制台的输入 VT 转换 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="46d6e-618">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-619">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-619">LTP Results:</span></span>
<span data-ttu-id="46d6e-620">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-620">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="46d6e-621">生成17017</span><span class="sxs-lookup"><span data-stu-id="46d6e-621">Build 17017</span></span>

<span data-ttu-id="46d6e-622">有关生成17017的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-622">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-623">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-623">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-624">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-624">WSL</span></span>
- <span data-ttu-id="46d6e-625">忽略空的 ELF 程序头 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-625">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="46d6e-626">允许 LxssManager 为非交互式用户 (ssh 和计划任务支持) 创建 WSL 实例 [GH 777, 1602]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-626">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="46d6e-627">支持 WSL-> Win32 > WSL ("开始") 方案 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-627">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="46d6e-628">对通过互操作调用的控制台应用终止的有限支持 [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-628">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="46d6e-629">支持 devpts [GH 1948] 的装载选项。</span><span class="sxs-lookup"><span data-stu-id="46d6e-629">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="46d6e-630">Ptrace 阻止子启动 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-630">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="46d6e-631">EPOLLET 缺少某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-631">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="46d6e-632">返回 PTRACE_GETSIGINFO 的更多数据。</span><span class="sxs-lookup"><span data-stu-id="46d6e-632">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="46d6e-633">带有 lseek 的 Getdents 提供了不正确的结果。</span><span class="sxs-lookup"><span data-stu-id="46d6e-633">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="46d6e-634">修复某些 Win32 互操作应用挂起, 并等待管道中没有更多数据的输入。</span><span class="sxs-lookup"><span data-stu-id="46d6e-634">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="46d6e-635">O_ASYNC 支持 tty/pty 文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-635">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="46d6e-636">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-636">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-637">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-637">Console</span></span>
- <span data-ttu-id="46d6e-638">此版本中没有与控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-638">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-639">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-639">LTP Results:</span></span>
<span data-ttu-id="46d6e-640">正在进行测试。</span><span class="sxs-lookup"><span data-stu-id="46d6e-640">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="46d6e-641">秋季创意者更新</span><span class="sxs-lookup"><span data-stu-id="46d6e-641">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="46d6e-642">生成16288</span><span class="sxs-lookup"><span data-stu-id="46d6e-642">Build 16288</span></span>

<span data-ttu-id="46d6e-643">有关生成16288的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-643">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-644">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-645">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-645">WSL</span></span>
- <span data-ttu-id="46d6e-646">正确初始化和报告套接字文件描述符的 uid、gid 和模式 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="46d6e-646">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="46d6e-647">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-647">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-648">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-648">Console</span></span>
- <span data-ttu-id="46d6e-649">此版本中没有与控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-649">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-650">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-650">LTP Results:</span></span>
<span data-ttu-id="46d6e-651">自16273以来无更改</span><span class="sxs-lookup"><span data-stu-id="46d6e-651">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="46d6e-652">生成16278</span><span class="sxs-lookup"><span data-stu-id="46d6e-652">Build 16278</span></span>

<span data-ttu-id="46d6e-653">有关生成162738的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-653">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-654">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-655">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-655">WSL</span></span>
- <span data-ttu-id="46d6e-656">当撕裂 LX MM 状态 [GH 2415] 时, 显式取消文件所支持节的映射视图</span><span class="sxs-lookup"><span data-stu-id="46d6e-656">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="46d6e-657">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-657">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-658">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-658">Console</span></span>
- <span data-ttu-id="46d6e-659">此版本中没有与控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-660">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-660">LTP Results:</span></span>
<span data-ttu-id="46d6e-661">自16273以来无更改</span><span class="sxs-lookup"><span data-stu-id="46d6e-661">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="46d6e-662">生成16275</span><span class="sxs-lookup"><span data-stu-id="46d6e-662">Build 16275</span></span>

<span data-ttu-id="46d6e-663">有关生成162735的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-663">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-664">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-665">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-665">WSL</span></span>
- <span data-ttu-id="46d6e-666">此版本中没有与 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-666">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-667">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-667">Console</span></span>
- <span data-ttu-id="46d6e-668">此版本中没有与控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-668">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-669">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-669">LTP Results:</span></span>
<span data-ttu-id="46d6e-670">自16273以来无更改</span><span class="sxs-lookup"><span data-stu-id="46d6e-670">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="46d6e-671">生成16273</span><span class="sxs-lookup"><span data-stu-id="46d6e-671">Build 16273</span></span>

<span data-ttu-id="46d6e-672">有关生成16273的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-672">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-673">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-674">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-674">WSL</span></span>
- <span data-ttu-id="46d6e-675">解决了 DrvFs 有时报告了目录的错误文件类型 [GH 2392] 的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-675">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="46d6e-676">允许创建 NETLINK_KOBJECT_UEVENT 套接字来取消阻止使用 UEVENT 的程序 [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="46d6e-676">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="46d6e-677">添加对非阻止连接的支持 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="46d6e-677">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="46d6e-678">实现 CLONE_FS 克隆系统调用标志 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="46d6e-678">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="46d6e-679">解决了在 NT 互操作中无法正确处理选项卡或引号的问题 [GH 1625, 2164]</span><span class="sxs-lookup"><span data-stu-id="46d6e-679">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="46d6e-680">尝试重新启动 WSL 实例时解决拒绝访问错误 [GH 651, 2095]</span><span class="sxs-lookup"><span data-stu-id="46d6e-680">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="46d6e-681">实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="46d6e-681">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="46d6e-682">修补各种 SysFs 文件的权限 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="46d6e-682">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="46d6e-683">在安装过程中修复 Haskell stack 挂起 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="46d6e-683">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="46d6e-684">实现 binfmt_misc "C"、"O" 和 "P" 标志 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="46d6e-684">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="46d6e-685">添加/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="46d6e-685">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="46d6e-686">添加对 ioprio_set 系统调用的部分支持 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="46d6e-686">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="46d6e-687">存根 SO_REUSEPORT & 为 netlink 套接字添加对 SO_PASSCRED 的支持 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="46d6e-687">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="46d6e-688">如果当前正在安装或卸载分发, 则从 RegisterDistribuiton 返回不同的错误代码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-688">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="46d6e-689">允许通过 wslconfig 取消注册部分安装的 WSL 分发</span><span class="sxs-lookup"><span data-stu-id="46d6e-689">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="46d6e-690">从 udp:: msg_peek 修复 python 套接字测试挂起</span><span class="sxs-lookup"><span data-stu-id="46d6e-690">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="46d6e-691">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-691">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-692">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-692">Console</span></span>
- <span data-ttu-id="46d6e-693">此版本中没有与控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-693">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-694">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-694">LTP Results:</span></span>
<span data-ttu-id="46d6e-695">总测试数:1904</span><span class="sxs-lookup"><span data-stu-id="46d6e-695">Total Tests: 1904</span></span><br/>
<span data-ttu-id="46d6e-696">跳过的测试总数:209</span><span class="sxs-lookup"><span data-stu-id="46d6e-696">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="46d6e-697">失败总数:229</span><span class="sxs-lookup"><span data-stu-id="46d6e-697">Total Failures: 229</span></span><br/>
[<span data-ttu-id="46d6e-698">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-698">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="46d6e-699">版本 16257</span><span class="sxs-lookup"><span data-stu-id="46d6e-699">Build 16257</span></span>

<span data-ttu-id="46d6e-700">有关生成16257的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-700">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-701">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-701">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-702">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-702">WSL</span></span>
- <span data-ttu-id="46d6e-703">实现 prlimit64 系统调用</span><span class="sxs-lookup"><span data-stu-id="46d6e-703">Implement prlimit64 system call</span></span>
- <span data-ttu-id="46d6e-704">添加对 ulimit 的支持-n (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="46d6e-704">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="46d6e-705">用于 TCP 套接字的存根 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="46d6e-705">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="46d6e-706">修复无效的 AT_EXECFN 辅助矢量行为 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="46d6e-706">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="46d6e-707">修复 console/tty 的复制/粘贴行为, 并添加更好的完整缓冲区处理 [GH 2204, 2131]</span><span class="sxs-lookup"><span data-stu-id="46d6e-707">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="46d6e-708">设置用户 ID 和组-ID 程序的辅助向量中的 AT_SECURE [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="46d6e-708">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="46d6e-709">伪类-终端主终结点未处理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="46d6e-709">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="46d6e-710">修复 lseek 在 LxFs 中倒带目录 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="46d6e-710">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="46d6e-711">使用繁重的/dev/ptmx 锁 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="46d6e-711">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="46d6e-712">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-712">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-713">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-713">Console</span></span>
- <span data-ttu-id="46d6e-714">在任何位置修复水平线条/下划线 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="46d6e-714">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="46d6e-715">解决处理顺序更改, 使 NPM 更难关闭 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="46d6e-715">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="46d6e-716">添加了新的配色方案: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="46d6e-716">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-717">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-717">LTP Results:</span></span>
<span data-ttu-id="46d6e-718">自16251以来无更改</span><span class="sxs-lookup"><span data-stu-id="46d6e-718">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-719">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-719">Syscall Support</span></span>
<span data-ttu-id="46d6e-720">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-720">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-721">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-721">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="46d6e-722">已知问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-722">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="46d6e-723">GitHub 问题 2392:WSL 无法识别的 Windows 文件夹 .。。</span><span class="sxs-lookup"><span data-stu-id="46d6e-723">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="46d6e-724">在版本16257中, WSL 在通过`/mnt/c/...`枚举 Windows 文件/文件夹时遇到问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-724">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="46d6e-725">此问题已修复, 应在第一周的第一8/14/2017 周的内部版本中发布。</span><span class="sxs-lookup"><span data-stu-id="46d6e-725">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="46d6e-726">生成16251</span><span class="sxs-lookup"><span data-stu-id="46d6e-726">Build 16251</span></span>

<span data-ttu-id="46d6e-727">有关生成16251的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-727">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-728">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-729">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-729">WSL</span></span>
- <span data-ttu-id="46d6e-730">从 WSL 可选组件中删除 beta 标记, 有关详细信息, 请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-730">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="46d6e-731">正确地为 exec [GH 962, 1415, 2072] 上的设置用户 ID 和组 ID 二进制文件初始化已保存的设置的 uid 和 gid</span><span class="sxs-lookup"><span data-stu-id="46d6e-731">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="46d6e-732">添加了对 ptrace PTRACE_O_TRACEEXIT 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="46d6e-732">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="46d6e-733">添加了对 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支持, NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="46d6e-733">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="46d6e-734">修复了在忽略信号时停止的 ptrace</span><span class="sxs-lookup"><span data-stu-id="46d6e-734">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="46d6e-735">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-735">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-736">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-736">Console</span></span>
- <span data-ttu-id="46d6e-737">此版本中没有与控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-738">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-738">LTP Results:</span></span>
<span data-ttu-id="46d6e-739">通过的测试数:768</span><span class="sxs-lookup"><span data-stu-id="46d6e-739">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="46d6e-740">失败的测试数:244</span><span class="sxs-lookup"><span data-stu-id="46d6e-740">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="46d6e-741">跳过的测试数:96</span><span class="sxs-lookup"><span data-stu-id="46d6e-741">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="46d6e-742">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-742">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="46d6e-743">生成16241</span><span class="sxs-lookup"><span data-stu-id="46d6e-743">Build 16241</span></span>

<span data-ttu-id="46d6e-744">有关生成16241的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-744">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-745">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-745">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="46d6e-746">WSL</span><span class="sxs-lookup"><span data-stu-id="46d6e-746">WSL</span></span>
- <span data-ttu-id="46d6e-747">此版本中没有与 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-747">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="46d6e-748">控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-748">Console</span></span>
- <span data-ttu-id="46d6e-749">修复了[以下](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)问题, 以便为每12月的交叉行输出错误的字符。</span><span class="sxs-lookup"><span data-stu-id="46d6e-749">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="46d6e-750">修复代码页 65001 (utf8) 中没有显示的输出文本</span><span class="sxs-lookup"><span data-stu-id="46d6e-750">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="46d6e-751">不要将对一种颜色的 RGB 值所做的更改传输到选定内容更改的调色板的其他部分。</span><span class="sxs-lookup"><span data-stu-id="46d6e-751">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="46d6e-752">这会使控制台属性表更易于使用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-752">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="46d6e-753">Ctrl + S 似乎无法正常工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-753">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="46d6e-754">ANSI 转义代码中完全不存在的粗体/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="46d6e-754">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="46d6e-755">控制台无法正确支持 Vim 颜色主题 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="46d6e-755">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="46d6e-756">无法粘贴特定字符 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="46d6e-756">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="46d6e-757">当内容在编辑/命令行上时, 重新调整大小会与奇怪交互, 同时调整 bash 窗口的大小 [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="46d6e-757">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="46d6e-758">按住 Ctrl 的同时屏幕会脏 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="46d6e-758">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="46d6e-759">在 HDPI 上显示 VT 时的控制台呈现 bug [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="46d6e-759">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="46d6e-760">Unicode 字符 U + 30FB 的 Japansese 字符看起来很奇怪 [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="46d6e-760">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="46d6e-761">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-761">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="46d6e-762">版本 16237</span><span class="sxs-lookup"><span data-stu-id="46d6e-762">Build 16237</span></span>

<span data-ttu-id="46d6e-763">有关生成16237的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-763">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-764">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-764">Fixed</span></span>
- <span data-ttu-id="46d6e-765">在 lxfs 中使用不带 Ea 的文件的默认属性 (root、root、0000)</span><span class="sxs-lookup"><span data-stu-id="46d6e-765">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="46d6e-766">添加了对使用扩展属性的分发的支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-766">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="46d6e-767">修复 getdents 和 getdents64 返回的项的填充</span><span class="sxs-lookup"><span data-stu-id="46d6e-767">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="46d6e-768">针对 shmctl SHM_STAT 系统调用修复权限检查 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="46d6e-768">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="46d6e-769">修复了 tty 的初始 epoll 状态 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="46d6e-769">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="46d6e-770">修复 DrvFs readdir 不返回所有条目 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="46d6e-770">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="46d6e-771">取消链接文件时修复 LxFs readdir [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="46d6e-771">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="46d6e-772">允许通过 procfs 重新打开未链接的 drvfs 文件</span><span class="sxs-lookup"><span data-stu-id="46d6e-772">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="46d6e-773">添加了用于禁用 WSL 功能的全局注册表项替代 (互操作性/驱动器安装)</span><span class="sxs-lookup"><span data-stu-id="46d6e-773">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="46d6e-774">修复 DrvFs (和 LxFs) 的 "stat" 中错误的块计数 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="46d6e-774">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="46d6e-775">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-775">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="46d6e-776">生成16232</span><span class="sxs-lookup"><span data-stu-id="46d6e-776">Build 16232</span></span>

<span data-ttu-id="46d6e-777">有关生成16232的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-777">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-778">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-778">Fixed</span></span>
- <span data-ttu-id="46d6e-779">此版本中没有与 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-779">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="46d6e-780">生成16226</span><span class="sxs-lookup"><span data-stu-id="46d6e-780">Build 16226</span></span>

<span data-ttu-id="46d6e-781">有关生成16226的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-781">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-782">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-782">Fixed</span></span>
- <span data-ttu-id="46d6e-783">xattr 相关 syscall 支持 (getxattr、setxattr、listxattr、removexattr)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-783">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="46d6e-784">capablity xattr 支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-784">security.capablity xattr support.</span></span>
- <span data-ttu-id="46d6e-785">提高了与某些文件系统和筛选器 (包括非 MS SMB 服务器) 的兼容性。</span><span class="sxs-lookup"><span data-stu-id="46d6e-785">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="46d6e-786">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="46d6e-786">[GH #1952]</span></span>
- <span data-ttu-id="46d6e-787">改进了对 OneDrive 占位符、GVFS 占位符和精简操作系统压缩文件的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-787">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="46d6e-788">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-788">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="46d6e-789">生成16215</span><span class="sxs-lookup"><span data-stu-id="46d6e-789">Build 16215</span></span>

<span data-ttu-id="46d6e-790">有关生成16215的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-790">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-791">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-791">Fixed</span></span>
- <span data-ttu-id="46d6e-792">WSL 不再需要开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="46d6e-792">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="46d6e-793">支持 drvfs 中的目录联接。</span><span class="sxs-lookup"><span data-stu-id="46d6e-793">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="46d6e-794">处理 WSL 分发 appx 包的卸载。</span><span class="sxs-lookup"><span data-stu-id="46d6e-794">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="46d6e-795">更新 procfs 以显示专用和共享映射。</span><span class="sxs-lookup"><span data-stu-id="46d6e-795">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="46d6e-796">添加 wslconfig 的功能以清理部分安装或卸载的分发。</span><span class="sxs-lookup"><span data-stu-id="46d6e-796">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="46d6e-797">添加了对 TCP 套接字 IP_MTU_DISCOVER 的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-797">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="46d6e-798">[GH 1639, 2115, 2205]</span><span class="sxs-lookup"><span data-stu-id="46d6e-798">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="46d6e-799">推断协议系列以便路由到 AF_INADDR。</span><span class="sxs-lookup"><span data-stu-id="46d6e-799">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="46d6e-800">串行设备改进 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="46d6e-800">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="46d6e-801">生成16199</span><span class="sxs-lookup"><span data-stu-id="46d6e-801">Build 16199</span></span>

<span data-ttu-id="46d6e-802">有关生成16199的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-802">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-803">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-803">Fixed</span></span>
- <span data-ttu-id="46d6e-804">这些版本中没有与 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="46d6e-804">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="46d6e-805">生成16193</span><span class="sxs-lookup"><span data-stu-id="46d6e-805">Build 16193</span></span>

<span data-ttu-id="46d6e-806">有关生成16193的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-806">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-807">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-807">Fixed</span></span>
- <span data-ttu-id="46d6e-808">发送 SIGCONT 和 threadgroup 终止之间的争用条件 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="46d6e-808">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="46d6e-809">将 tty 和 pty 设备更改为 report FILE_DEVICE_NAMED_PIPE, 而不是 FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="46d6e-809">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="46d6e-810">IP_OPTIONS 的 SSH 修补程序</span><span class="sxs-lookup"><span data-stu-id="46d6e-810">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="46d6e-811">已将 DrvFs 装载迁移到 init daemon [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="46d6e-811">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="46d6e-812">为以下 NT 符号链接添加了 DrvFs 中的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-812">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="46d6e-813">生成16184</span><span class="sxs-lookup"><span data-stu-id="46d6e-813">Build 16184</span></span>

<span data-ttu-id="46d6e-814">有关生成16184的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-814">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-815">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-815">Fixed</span></span>
- <span data-ttu-id="46d6e-816">删除 apt 包维护任务 (lxrun/update)</span><span class="sxs-lookup"><span data-stu-id="46d6e-816">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="46d6e-817">固定输出不显示在 node.js 中的 Windows 进程中 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="46d6e-817">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="46d6e-818">放宽 lxcore 中的对齐要求 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="46d6e-818">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="46d6e-819">修复了 AT_EMPTY_PATH 标志在系统调用收藏中的处理。</span><span class="sxs-lookup"><span data-stu-id="46d6e-819">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="46d6e-820">修复了删除 DrvFs 文件和打开句柄的问题时, 文件会显示未定义的行为 [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="46d6e-820">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="46d6e-821">/etc/hosts 现在将从 Windows hosts 文件 (%windir%\system32\drivers\etc\hosts) 继承条目 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="46d6e-821">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="46d6e-822">生成16179</span><span class="sxs-lookup"><span data-stu-id="46d6e-822">Build 16179</span></span>

<span data-ttu-id="46d6e-823">有关生成16179的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-823">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-824">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-824">Fixed</span></span>
- <span data-ttu-id="46d6e-825">本周不会更改 WSL。</span><span class="sxs-lookup"><span data-stu-id="46d6e-825">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="46d6e-826">生成16176</span><span class="sxs-lookup"><span data-stu-id="46d6e-826">Build 16176</span></span>

<span data-ttu-id="46d6e-827">有关生成16176的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-827">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-828">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-828">Fixed</span></span>

- [<span data-ttu-id="46d6e-829">启用的串行支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-829">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="46d6e-830">添加了 IP 套接字选项 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="46d6e-830">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="46d6e-831">实现的 pwritev 函数 (在将文件上传到 nginx/PHP-PHP-FPM) [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="46d6e-831">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="46d6e-832">添加的 IP 套接字选项 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="46d6e-832">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="46d6e-833">支持套接字选项 IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="46d6e-833">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="46d6e-834">添加了适用于 apps 节点、traceroute、挖掘、nslookup、主机的 IP (V6) _MTU 套接字选项</span><span class="sxs-lookup"><span data-stu-id="46d6e-834">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="46d6e-835">添加的 IP 套接字选项 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="46d6e-835">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="46d6e-836">文件系统改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-836">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="46d6e-837">允许装载 UNC 路径</span><span class="sxs-lookup"><span data-stu-id="46d6e-837">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="46d6e-838">在 drvfs 中启用 CDFS 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-838">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="46d6e-839">正确处理 drvfs 中网络文件系统的权限</span><span class="sxs-lookup"><span data-stu-id="46d6e-839">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="46d6e-840">向 drvfs 添加远程驱动器支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-840">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="46d6e-841">在 drvfs 中启用 FAT 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-841">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="46d6e-842">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-842">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-843">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="46d6e-843">LTP Results</span></span>
<span data-ttu-id="46d6e-844">自15042以来无更改</span><span class="sxs-lookup"><span data-stu-id="46d6e-844">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="46d6e-845">生成16170</span><span class="sxs-lookup"><span data-stu-id="46d6e-845">Build 16170</span></span>

<span data-ttu-id="46d6e-846">有关生成16170的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-846">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="46d6e-847">我们发布了新的[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), 讨论了测试 WSL 的努力。</span><span class="sxs-lookup"><span data-stu-id="46d6e-847">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="46d6e-848">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-848">Fixed</span></span>

- <span data-ttu-id="46d6e-849">Support socket 选项 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="46d6e-849">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="46d6e-850">添加对 PTRACE_OLDSETOPTIONS 的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-850">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="46d6e-851">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="46d6e-851">[GH 1692]</span></span>
- <span data-ttu-id="46d6e-852">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-852">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-853">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="46d6e-853">LTP Results</span></span>
<span data-ttu-id="46d6e-854">自15042以来无更改</span><span class="sxs-lookup"><span data-stu-id="46d6e-854">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="46d6e-855">生成15046到 Windows 10 创意者更新</span><span class="sxs-lookup"><span data-stu-id="46d6e-855">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="46d6e-856">没有更多的 WSL 修补程序或功能已计划包含在 Windows 10 的创意者更新中。</span><span class="sxs-lookup"><span data-stu-id="46d6e-856">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="46d6e-857">WSL 的发行说明将在接下来的几周内恢复, 添加目标为下一个主要 Windows 更新。</span><span class="sxs-lookup"><span data-stu-id="46d6e-857">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="46d6e-858">有关生成15046和未来的内部版本的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-858">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="46d6e-859">生成15042</span><span class="sxs-lookup"><span data-stu-id="46d6e-859">Build 15042</span></span>

<span data-ttu-id="46d6e-860">有关生成15042的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-860">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-861">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-861">Fixed</span></span>

- <span data-ttu-id="46d6e-862">解决在删除以 "..." 结尾的路径时出现死锁的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-862">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="46d6e-863">修复了 FIONBIO 在成功时不返回0的问题 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="46d6e-863">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="46d6e-864">修复了 inet 数据报套接字的长度为零的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-864">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="46d6e-865">由于 drvfs inode 查找中的争用条件, 修复可能的死锁 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="46d6e-865">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="46d6e-866">扩展了对 unix 套接字辅助数据的支持;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514, 613, 1326]</span><span class="sxs-lookup"><span data-stu-id="46d6e-866">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="46d6e-867">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-867">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-868">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-868">LTP Results:</span></span>
<span data-ttu-id="46d6e-869">通过的测试数:737</span><span class="sxs-lookup"><span data-stu-id="46d6e-869">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="46d6e-870">未通过的数目 (失败，已跳过，等等...):255</span><span class="sxs-lookup"><span data-stu-id="46d6e-870">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="46d6e-871">生成15031</span><span class="sxs-lookup"><span data-stu-id="46d6e-871">Build 15031</span></span>

<span data-ttu-id="46d6e-872">有关生成15031的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-872">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-873">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-873">Fixed</span></span>

- <span data-ttu-id="46d6e-874">修复了时间 (2) 偶尔错误行为的 bug。</span><span class="sxs-lookup"><span data-stu-id="46d6e-874">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="46d6e-875">已修复并发出 \* SIGPROCMASK syscall 可能会损坏信号掩码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-875">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="46d6e-876">现在, 在 WSL 进程创建通知中返回完整的命令行长度。</span><span class="sxs-lookup"><span data-stu-id="46d6e-876">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="46d6e-877">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="46d6e-877">[GH 1632]</span></span>
- <span data-ttu-id="46d6e-878">WSL 现在报告通过 ptrace 的线程退出, 以获得 GDB 挂起。</span><span class="sxs-lookup"><span data-stu-id="46d6e-878">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="46d6e-879">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="46d6e-879">[GH 1196]</span></span>
- <span data-ttu-id="46d6e-880">修复了严重 tmux IO 后 ptys 将挂起的 bug。</span><span class="sxs-lookup"><span data-stu-id="46d6e-880">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="46d6e-881">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="46d6e-881">[GH 1358]</span></span>
- <span data-ttu-id="46d6e-882">修复了许多系统调用中的超时验证 (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create)</span><span class="sxs-lookup"><span data-stu-id="46d6e-882">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="46d6e-883">添加了 eventfd EFD_SEMAPHORE 支持 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="46d6e-883">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="46d6e-884">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-884">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-885">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-885">LTP Results:</span></span>
<span data-ttu-id="46d6e-886">通过的测试数:737</span><span class="sxs-lookup"><span data-stu-id="46d6e-886">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="46d6e-887">未通过的数目 (失败，已跳过，等等...):255</span><span class="sxs-lookup"><span data-stu-id="46d6e-887">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46d6e-888">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-888">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="46d6e-889">生成15025</span><span class="sxs-lookup"><span data-stu-id="46d6e-889">Build 15025</span></span>

<span data-ttu-id="46d6e-890">有关生成15025的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-890">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-891">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-891">Fixed</span></span>

- <span data-ttu-id="46d6e-892">修复破坏 grep 2.27 [GH 1578] 的 bug</span><span class="sxs-lookup"><span data-stu-id="46d6e-892">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="46d6e-893">Eventfd2 syscall 的已实现 EFD_SEMAPHORE 标志 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="46d6e-893">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="46d6e-894">已实现的/proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="46d6e-894">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="46d6e-895">面向 unix 流套接字的信号驱动 IO 支持 [GH 393, 68]</span><span class="sxs-lookup"><span data-stu-id="46d6e-895">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="46d6e-896">支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="46d6e-896">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="46d6e-897">实现 recvmmsg () syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="46d6e-897">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="46d6e-898">修复了 epoll_wait () 未在等待的 bug [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="46d6e-898">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="46d6e-899">实现/proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="46d6e-899">Implement /proc/version_signature</span></span>
- <span data-ttu-id="46d6e-900">如果两个文件说明符引用同一管道, 则</span><span class="sxs-lookup"><span data-stu-id="46d6e-900">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="46d6e-901">为 SO_PEERCRED for Unix 套接字实现了正确行为</span><span class="sxs-lookup"><span data-stu-id="46d6e-901">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="46d6e-902">Fixed tkill syscall 无效的参数处理</span><span class="sxs-lookup"><span data-stu-id="46d6e-902">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="46d6e-903">更改以提高 drvfs 的 preformace</span><span class="sxs-lookup"><span data-stu-id="46d6e-903">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="46d6e-904">Ruby IO 阻止的次要修补程序</span><span class="sxs-lookup"><span data-stu-id="46d6e-904">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="46d6e-905">Fixed recvmsg () 为 inet 套接字的 MSG_DONTWAIT 标志返回 EINVAL [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="46d6e-905">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="46d6e-906">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-906">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-907">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-907">LTP Results:</span></span>
<span data-ttu-id="46d6e-908">通过的测试数:732</span><span class="sxs-lookup"><span data-stu-id="46d6e-908">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="46d6e-909">未通过的数目 (失败，已跳过，等等...):255</span><span class="sxs-lookup"><span data-stu-id="46d6e-909">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46d6e-910">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-910">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="46d6e-911">生成15019</span><span class="sxs-lookup"><span data-stu-id="46d6e-911">Build 15019</span></span>

<span data-ttu-id="46d6e-912">有关生成15019的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-912">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-913">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-913">Fixed</span></span>

- <span data-ttu-id="46d6e-914">修复了在 procfs 中错误报告了 CPU 使用率的 bug, 如 htop (GH 823、945、971)</span><span class="sxs-lookup"><span data-stu-id="46d6e-914">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="46d6e-915">在现有文件上对 O_TRUNC 调用 open () 时, inotify 现在会在 IN_OPEN 之前生成 IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="46d6e-915">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="46d6e-916">修复了 unix 套接字 getsockopt SO_ERROR 以启用 postgress [GH 61, 1354]</span><span class="sxs-lookup"><span data-stu-id="46d6e-916">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="46d6e-917">为中转语言实现/proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="46d6e-917">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="46d6e-918">Apt-获取包更新后台任务现在从视图中运行隐藏</span><span class="sxs-lookup"><span data-stu-id="46d6e-918">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="46d6e-919">清除 ipv6 localhost 的作用域 (弹簧框架 (Java) 故障)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-919">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="46d6e-920">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-920">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-921">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-921">LTP Results:</span></span>
<span data-ttu-id="46d6e-922">通过的测试数:714</span><span class="sxs-lookup"><span data-stu-id="46d6e-922">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="46d6e-923">未通过的数目 (失败，已跳过，等等...):249</span><span class="sxs-lookup"><span data-stu-id="46d6e-923">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="46d6e-924">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-924">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="46d6e-925">生成15014</span><span class="sxs-lookup"><span data-stu-id="46d6e-925">Build 15014</span></span>

<span data-ttu-id="46d6e-926">有关生成15014的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-926">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-927">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-927">Fixed</span></span>

- <span data-ttu-id="46d6e-928">Ctrl + C 现在按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-928">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="46d6e-929">htop 和 ps auxw 现在显示正确的资源利用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="46d6e-929">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="46d6e-930">将 NT 异常转换为信号的基本转换。</span><span class="sxs-lookup"><span data-stu-id="46d6e-930">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="46d6e-931">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="46d6e-931">(GH #513)</span></span>
- <span data-ttu-id="46d6e-932">当空间不足而不是 EINVAL (GH #1571) 时, fallocate 现在会失败 ENOSPC</span><span class="sxs-lookup"><span data-stu-id="46d6e-932">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="46d6e-933">添加的/proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="46d6e-933">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="46d6e-934">实现 semop 和 semtimedop 系统调用</span><span class="sxs-lookup"><span data-stu-id="46d6e-934">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="46d6e-935">修复了 IP_RECVTOS & IPV6_RECVTCLASS 套接字选项的 nslookup 错误 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="46d6e-935">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="46d6e-936">支持套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="46d6e-936">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="46d6e-937">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-937">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-938">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-938">LTP Results:</span></span>
<span data-ttu-id="46d6e-939">通过的测试数:709</span><span class="sxs-lookup"><span data-stu-id="46d6e-939">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="46d6e-940">未通过的数目 (失败，已跳过，等等...):255</span><span class="sxs-lookup"><span data-stu-id="46d6e-940">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46d6e-941">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-941">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="46d6e-942">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="46d6e-942">Syscall Summary</span></span>
<span data-ttu-id="46d6e-943">总 Syscall:384</span><span class="sxs-lookup"><span data-stu-id="46d6e-943">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="46d6e-944">已实现的总数:235</span><span class="sxs-lookup"><span data-stu-id="46d6e-944">Total Implemented: 235</span></span> </br>
<span data-ttu-id="46d6e-945">总用作存根:22</span><span class="sxs-lookup"><span data-stu-id="46d6e-945">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="46d6e-946">未实现总数:127</span><span class="sxs-lookup"><span data-stu-id="46d6e-946">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="46d6e-947">详细细目</span><span class="sxs-lookup"><span data-stu-id="46d6e-947">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="46d6e-948">生成15007</span><span class="sxs-lookup"><span data-stu-id="46d6e-948">Build 15007</span></span>

<span data-ttu-id="46d6e-949">有关生成15007的常规 Windows 信息, 请访问[Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-949">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="46d6e-950">已知问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-950">Known Issue</span></span>

- <span data-ttu-id="46d6e-951">有一个已知 bug, 控制台无法识别某些 Ctrl + <key>输入。</span><span class="sxs-lookup"><span data-stu-id="46d6e-951">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="46d6e-952">这包括将充当普通 "c" 按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="46d6e-952">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="46d6e-953">解决方法：将备用键映射到 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="46d6e-953">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="46d6e-954">例如, 若要将 Ctrl + K 映射到 Ctrl + C, `stty intr \^k`请执行:。</span><span class="sxs-lookup"><span data-stu-id="46d6e-954">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="46d6e-955">此映射按终端进行, 并且*每*次启动 bash 时都必须执行此映射。</span><span class="sxs-lookup"><span data-stu-id="46d6e-955">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="46d6e-956">用户可以在其`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="46d6e-956">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="46d6e-957">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-957">Fixed</span></span>

- <span data-ttu-id="46d6e-958">更正了运行 WSL 会消耗 100% 的 CPU 内核的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-958">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="46d6e-959">套接字选项 IP_PKTINFO、IPV6_RECVPKTINFO 现在支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-959">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="46d6e-960">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="46d6e-960">(GH #851, 987)</span></span>
- <span data-ttu-id="46d6e-961">在 lxcore (GH #1452, 1414, 1343, 468, 308) 中将网络接口物理地址截断为16字节</span><span class="sxs-lookup"><span data-stu-id="46d6e-961">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="46d6e-962">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-962">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-963">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-963">LTP Results:</span></span>
<span data-ttu-id="46d6e-964">通过的测试数:709</span><span class="sxs-lookup"><span data-stu-id="46d6e-964">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="46d6e-965">未通过的数目 (失败，已跳过，等等...):255</span><span class="sxs-lookup"><span data-stu-id="46d6e-965">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="46d6e-966">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-966">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="46d6e-967">生成15002</span><span class="sxs-lookup"><span data-stu-id="46d6e-967">Build 15002</span></span>

<span data-ttu-id="46d6e-968">有关生成15002的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-968">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="46d6e-969">已知问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-969">Known Issue</span></span>

<span data-ttu-id="46d6e-970">两个已知问题:</span><span class="sxs-lookup"><span data-stu-id="46d6e-970">Two known issues:</span></span>
- <span data-ttu-id="46d6e-971">有一个已知 bug, 控制台无法识别某些 Ctrl + <key>输入。</span><span class="sxs-lookup"><span data-stu-id="46d6e-971">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="46d6e-972">这包括将充当普通 "c" 按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="46d6e-972">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="46d6e-973">解决方法：将备用键映射到 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="46d6e-973">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="46d6e-974">例如, 若要将 Ctrl + K 映射到 Ctrl + C, `stty intr \^k`请执行:。</span><span class="sxs-lookup"><span data-stu-id="46d6e-974">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="46d6e-975">此映射按终端进行, 并且*每*次启动 bash 时都必须执行此映射。</span><span class="sxs-lookup"><span data-stu-id="46d6e-975">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="46d6e-976">用户可以在其`.bashrc`</span><span class="sxs-lookup"><span data-stu-id="46d6e-976">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="46d6e-977">当 WSL 运行时, 系统线程将消耗 100% 的 CPU 内核。</span><span class="sxs-lookup"><span data-stu-id="46d6e-977">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="46d6e-978">根本原因已解决并在内部修复。</span><span class="sxs-lookup"><span data-stu-id="46d6e-978">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="46d6e-979">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-979">Fixed</span></span>

- <span data-ttu-id="46d6e-980">现在必须在同一权限级别创建所有 bash 会话。</span><span class="sxs-lookup"><span data-stu-id="46d6e-980">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="46d6e-981">尝试在不同级别启动会话将被阻止。</span><span class="sxs-lookup"><span data-stu-id="46d6e-981">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="46d6e-982">这意味着管理员和非管理员控制台不能同时运行。</span><span class="sxs-lookup"><span data-stu-id="46d6e-982">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="46d6e-983">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="46d6e-983">(GH #626)</span></span>
<br/>
- <span data-ttu-id="46d6e-984">实现以下 NETLINK_ROUTE 消息 (需要 Windows 管理员)</span><span class="sxs-lookup"><span data-stu-id="46d6e-984">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="46d6e-985">RTM_NEWADDR (支持`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="46d6e-985">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="46d6e-986">RTM_NEWROUTE (支持`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="46d6e-986">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="46d6e-987">RTM_DELADDR (支持`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="46d6e-987">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="46d6e-988">RTM_DELROUTE (支持`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="46d6e-988">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="46d6e-989">要更新的包的计划任务检查将不再对按流量计费的连接运行 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="46d6e-989">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="46d6e-990">修复了管道停滞的错误, 即 bash-c "ls-alR/" |bash-c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="46d6e-990">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="46d6e-991">已实现 TCP_KEEPCNT 套接字选项 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="46d6e-991">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="46d6e-992">实现的 IP_MTU_DISCOVER INET 套接字选项 (GH #720、717、170、69)</span><span class="sxs-lookup"><span data-stu-id="46d6e-992">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="46d6e-993">删除了旧功能, 可通过 NT 路径查找从 init 运行 NT 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-993">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="46d6e-994">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="46d6e-994">(GH #1325)</span></span>
- <span data-ttu-id="46d6e-995">修复/dev/kmsg 模式以允许组/其他读访问 (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="46d6e-995">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="46d6e-996">实现的/proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="46d6e-996">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="46d6e-997">更正了进程开始时间显示为2432年的错误 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="46d6e-997">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="46d6e-998">切换到 xterm-256color (GH #1446) 的默认术语环境变量</span><span class="sxs-lookup"><span data-stu-id="46d6e-998">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="46d6e-999">修改了处理分叉期间计算处理提交的方式。</span><span class="sxs-lookup"><span data-stu-id="46d6e-999">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="46d6e-1000">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1000">(GH #1286)</span></span>
- <span data-ttu-id="46d6e-1001">实现的/proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1001">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="46d6e-1002">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1002">(GH #1286)</span></span>
- <span data-ttu-id="46d6e-1003">实现的/proc/net/route 文件 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1003">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="46d6e-1004">修复了快捷方式名称错误本地化的错误 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1004">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="46d6e-1005">已修复不正确验证程序标头的 elf 解析逻辑必须小于 (或等于) PATH_MAX。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1005">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="46d6e-1006">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1006">(GH #1048)</span></span>
- <span data-ttu-id="46d6e-1007">为 procfs、sysfs、cgroupfs 和 binfmtfs (GH #1378) 实现了 statfs 回调</span><span class="sxs-lookup"><span data-stu-id="46d6e-1007">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="46d6e-1008">修复了不会关闭的 AptPackageIndexUpdate 窗口 (GH #1184, 还会在 GH #1193 中讨论)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1008">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="46d6e-1009">添加了 ASLR 个性 ADDR_NO_RANDOMIZE 支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1009">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="46d6e-1010">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1010">(GH #1148, 1128)</span></span>
- <span data-ttu-id="46d6e-1011">改善了 PTRACE_GETSIGINFO、SIGSEGV, 适用于 AV 期间的适当 gdb 堆栈跟踪 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1011">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="46d6e-1012">Patchelf 二进制文件的 Elf 分析不再失败。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1012">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="46d6e-1013">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1013">(GH #471)</span></span>
- <span data-ttu-id="46d6e-1014">VPN DNS 传播到/etc/resolv.conf (GH #416, 1350)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1014">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="46d6e-1015">提高 TCP 关闭以实现更可靠的数据传输。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1015">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="46d6e-1016">(GH #610, 616, 1025, 1335)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1016">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="46d6e-1017">现在, 在打开太多文件时返回正确的错误代码 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1017">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="46d6e-1018">(GH #1126, 2090)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1018">(GH #1126, 2090)</span></span>
- <span data-ttu-id="46d6e-1019">Windows 审核日志现在会报告进程创建审核中的映像名称。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1019">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="46d6e-1020">从 bash 窗口中启动 bash 时, 现在正常失败</span><span class="sxs-lookup"><span data-stu-id="46d6e-1020">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="46d6e-1021">在互操作无法访问 LxFs 下的工作目录时添加了错误消息 (例如 .bashrc)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1021">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="46d6e-1022">修复了在 WSL 中截断 Windows 路径的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1022">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="46d6e-1023">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1023">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1024">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1024">LTP Results:</span></span>
<span data-ttu-id="46d6e-1025">通过的测试数:690</span><span class="sxs-lookup"><span data-stu-id="46d6e-1025">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="46d6e-1026">未通过的数目 (失败，已跳过，等等...):274</span><span class="sxs-lookup"><span data-stu-id="46d6e-1026">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="46d6e-1027">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1027">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1028">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1028">Syscall Support</span></span>
<span data-ttu-id="46d6e-1029">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1029">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1030">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1030">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="46d6e-1031">生成14986</span><span class="sxs-lookup"><span data-stu-id="46d6e-1031">Build 14986</span></span>

<span data-ttu-id="46d6e-1032">有关生成14986的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1032">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1033">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1033">Fixed</span></span>

- <span data-ttu-id="46d6e-1034">修复了与 Netlink 和 Pty IOCTLs 的错误检查</span><span class="sxs-lookup"><span data-stu-id="46d6e-1034">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="46d6e-1035">内核版本现在报告 4.4.0-43 与 Xenial 的一致性</span><span class="sxs-lookup"><span data-stu-id="46d6e-1035">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="46d6e-1036">当输入定向到 "nul:" (GH #1259) 时, Bash 立即启动</span><span class="sxs-lookup"><span data-stu-id="46d6e-1036">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="46d6e-1037">线程 Id 现在在 procfs 中报告正确 (GH #967)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1037">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="46d6e-1038">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |Inotify_add_watch () 中现支持 IN_ISDIR 标志 (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1038">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="46d6e-1039">实现 timer_create 和相关的系统调用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1039">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="46d6e-1040">这将启用 GHC 支持 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1040">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="46d6e-1041">修复了 ping 返回时间 0.000 ms 的问题 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1041">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="46d6e-1042">当打开太多文件时, 返回正确的错误代码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1042">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="46d6e-1043">修复了 WSL 中的问题: 如果接口的硬件地址为32字节 (如 Teredo 接口), 则网络接口数据的 Netlink 请求将会失败, 并出现 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1043">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="46d6e-1044">请注意, Linux "ip" 实用工具包含一个 bug, 如果 WSL 报告了32字节的硬件地址, 它会崩溃。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1044">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="46d6e-1045">这是 "ip" 中的错误, 而不是 WSL。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1045">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="46d6e-1046">"Ip" 实用工具将用于打印硬件地址的字符串缓冲区的长度硬编码, 而该缓冲区太小, 无法打印32字节的硬件地址。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1046">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="46d6e-1047">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1047">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1048">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1048">LTP Results:</span></span>
<span data-ttu-id="46d6e-1049">通过的测试数:669</span><span class="sxs-lookup"><span data-stu-id="46d6e-1049">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="46d6e-1050">未通过的数目 (失败，已跳过，等等...):258</span><span class="sxs-lookup"><span data-stu-id="46d6e-1050">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="46d6e-1051">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1051">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1052">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1052">Syscall Support</span></span>
<span data-ttu-id="46d6e-1053">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1053">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1054">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1054">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="46d6e-1055">生成14971</span><span class="sxs-lookup"><span data-stu-id="46d6e-1055">Build 14971</span></span>

<span data-ttu-id="46d6e-1056">有关生成14971的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1056">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1057">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1057">Fixed</span></span>

 - <span data-ttu-id="46d6e-1058">由于控件之外的情况, 对于适用于 Linux 的 Windows 子系统, 此版本中没有更新。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1058">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="46d6e-1059">定期计划的更新将在下一版本中继续进行。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1059">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1060">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1060">LTP Results:</span></span>
<span data-ttu-id="46d6e-1061">从14965无变化</span><span class="sxs-lookup"><span data-stu-id="46d6e-1061">Unchanged from 14965</span></span> </br>
<span data-ttu-id="46d6e-1062">通过的测试数:664</span><span class="sxs-lookup"><span data-stu-id="46d6e-1062">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="46d6e-1063">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1063">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1064">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1064">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="46d6e-1065">生成14965</span><span class="sxs-lookup"><span data-stu-id="46d6e-1065">Build 14965</span></span>

<span data-ttu-id="46d6e-1066">有关生成14965的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1066">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1067">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1067">Fixed</span></span>

- <span data-ttu-id="46d6e-1068">支持 Netlink socket NETLINK_ROUTE 协议的 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1068">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="46d6e-1069">为网络枚举启用 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="46d6e-1069">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="46d6e-1070">有关详细信息, 请参阅[WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1070">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="46d6e-1071">默认情况下,/sbin 现在位于用户的路径中</span><span class="sxs-lookup"><span data-stu-id="46d6e-1071">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="46d6e-1072">默认情况下, NT 用户路径现在追加到 WSL 路径 (即, 你现在可以键入 notepad.exe, 无需向 Linux 路径添加 System32)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1072">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="46d6e-1073">添加了对/proc/sys/kernel/cap_last_cap 的支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1073">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="46d6e-1074">当当前工作目录包含非 ansi 字符时, 现在可以从 WSL 启动 NT 二进制文件 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1074">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="46d6e-1075">允许在断开连接的 unix 流套接字上关闭。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1075">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="46d6e-1076">添加了对 PR_GET_PDEATHSIG 的支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1076">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="46d6e-1077">添加了对 CLONE_PARENT 的支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1077">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="46d6e-1078">修复了管道停滞的错误, 即 bash-c "ls-alR/" |bash-c "cat" (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1078">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="46d6e-1079">处理连接到当前终端的请求。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1079">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="46d6e-1080">将/proc/<pid>/oom_score_adj 标记为可写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1080">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="46d6e-1081">添加/sys/fs/cgroup 文件夹。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1081">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="46d6e-1082">sched_setaffinity 应返回关联位掩码的数目</span><span class="sxs-lookup"><span data-stu-id="46d6e-1082">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="46d6e-1083">修复不正确假定解释器路径的 ELF 验证逻辑长度必须小于64个字符。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1083">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="46d6e-1084">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1084">(GH #743)</span></span>
- <span data-ttu-id="46d6e-1085">打开文件描述符会使控制台窗口保持打开状态 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1085">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="46d6e-1086">Fixeed 错误, 其中重命名 () 失败, 目标名称上有尾随斜杠 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1086">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="46d6e-1087">实现/proc/net/dev 文件</span><span class="sxs-lookup"><span data-stu-id="46d6e-1087">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="46d6e-1088">已修复 0.000 ms ping, 因为计时器分辨率。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1088">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="46d6e-1089">实现的/proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1089">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="46d6e-1090">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1090">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1091">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1091">LTP Results:</span></span>
<span data-ttu-id="46d6e-1092">通过的测试数:664</span><span class="sxs-lookup"><span data-stu-id="46d6e-1092">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="46d6e-1093">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1093">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1094">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1094">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="46d6e-1095">生成14959</span><span class="sxs-lookup"><span data-stu-id="46d6e-1095">Build 14959</span></span>

<span data-ttu-id="46d6e-1096">有关生成14959的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1096">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1097">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1097">Fixed</span></span>

- <span data-ttu-id="46d6e-1098">改善了 Windows 的 Pico 过程通知。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1098">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="46d6e-1099">[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)上的其他信息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1099">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="46d6e-1100">提高了 Windows 互操作性的稳定性</span><span class="sxs-lookup"><span data-stu-id="46d6e-1100">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="46d6e-1101">修复了在启用企业数据保护 (EDP) 时启动 bash 时出现的错误0x80070057</span><span class="sxs-lookup"><span data-stu-id="46d6e-1101">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="46d6e-1102">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1102">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1103">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1103">LTP Results:</span></span>
<span data-ttu-id="46d6e-1104">通过的测试数:665</span><span class="sxs-lookup"><span data-stu-id="46d6e-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46d6e-1105">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1106">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="46d6e-1107">生成14955</span><span class="sxs-lookup"><span data-stu-id="46d6e-1107">Build 14955</span></span>

<span data-ttu-id="46d6e-1108">有关生成14955的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1108">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1109">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1109">Fixed</span></span>

 - <span data-ttu-id="46d6e-1110">由于控件之外的情况, 对于适用于 Linux 的 Windows 子系统, 此版本中没有更新。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1110">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="46d6e-1111">定期计划的更新将在下一版本中继续进行。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1111">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1112">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1112">LTP Results:</span></span>
<span data-ttu-id="46d6e-1113">通过的测试数:665</span><span class="sxs-lookup"><span data-stu-id="46d6e-1113">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46d6e-1114">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1114">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1115">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="46d6e-1116">生成14951</span><span class="sxs-lookup"><span data-stu-id="46d6e-1116">Build 14951</span></span>

<span data-ttu-id="46d6e-1117">有关生成14951的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1117">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="46d6e-1118">新功能:Windows/Ubuntu 互操作性</span><span class="sxs-lookup"><span data-stu-id="46d6e-1118">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="46d6e-1119">现在可以从 WSL 命令行直接调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1119">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="46d6e-1120">这使用户能够以一种不可能的方式与其 Windows 环境和系统交互。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1120">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="46d6e-1121">作为一个快速示例, 用户现在可以运行以下命令:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1121">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="46d6e-1122">有关详细信息, 请参阅:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1122">More information can be found at:</span></span>

- [<span data-ttu-id="46d6e-1123">互操作的 WSL 团队博客</span><span class="sxs-lookup"><span data-stu-id="46d6e-1123">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="46d6e-1124">MSDN 互操作文档</span><span class="sxs-lookup"><span data-stu-id="46d6e-1124">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1125">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1125">Fixed</span></span>

- <span data-ttu-id="46d6e-1126">现在为所有新的 WSL 实例安装了 Ubuntu 16.04 (Xenial)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1126">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="46d6e-1127">将不会自动升级具有现有 14.04 (t) 实例的用户。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1127">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="46d6e-1128">现在会显示安装过程中设置的区域设置</span><span class="sxs-lookup"><span data-stu-id="46d6e-1128">Locale set during install is now displayed</span></span>
- <span data-ttu-id="46d6e-1129">包含 bug 的终端改进, 其中将 WSL 进程重定向到文件并不总是有效</span><span class="sxs-lookup"><span data-stu-id="46d6e-1129">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="46d6e-1130">控制台生存期应该与 bash 生存期相关联</span><span class="sxs-lookup"><span data-stu-id="46d6e-1130">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="46d6e-1131">控制台窗口大小应使用可见大小, 而不是缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="46d6e-1131">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="46d6e-1132">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1132">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1133">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1133">LTP Results:</span></span>
<span data-ttu-id="46d6e-1134">通过的测试数:665</span><span class="sxs-lookup"><span data-stu-id="46d6e-1134">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46d6e-1135">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1135">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1136">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1136">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="46d6e-1137">生成14946</span><span class="sxs-lookup"><span data-stu-id="46d6e-1137">Build 14946</span></span>

<span data-ttu-id="46d6e-1138">有关生成14946的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1138">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1139">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1139">Fixed</span></span>

- <span data-ttu-id="46d6e-1140">修复了阻止为具有包含空格或引号的 NT 用户名的用户创建 WSL 用户帐户的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1140">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="46d6e-1141">更改 VolFs 和 DrvFs, 以在 stat 中为目录的链接计数返回0</span><span class="sxs-lookup"><span data-stu-id="46d6e-1141">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="46d6e-1142">支持 IPV6_MULTICAST_HOPS 套接字选项。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1142">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="46d6e-1143">仅限每 tty 使用单个控制台 i/o 循环。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1143">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="46d6e-1144">示例: 可以执行以下命令:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1144">Example: the following command is possible:</span></span>
  - <span data-ttu-id="46d6e-1145">bash-c "回显数据" |bash-c "ssh user@example.com " cat > foo .txt ""</span><span class="sxs-lookup"><span data-stu-id="46d6e-1145">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="46d6e-1146">用/proc/cpuinfo 中的制表符替换空格 (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1146">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="46d6e-1147">DrvFs 现在显示在 mountinfo 中, 其名称与已装入的 Windows 卷匹配</span><span class="sxs-lookup"><span data-stu-id="46d6e-1147">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="46d6e-1148">/home 和/root 现在显示在具有正确名称的 mountinfo 中</span><span class="sxs-lookup"><span data-stu-id="46d6e-1148">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="46d6e-1149">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1149">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1150">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1150">LTP Results:</span></span>
<span data-ttu-id="46d6e-1151">通过的测试数:665</span><span class="sxs-lookup"><span data-stu-id="46d6e-1151">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46d6e-1152">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1152">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1153">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1153">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="46d6e-1154">生成14942</span><span class="sxs-lookup"><span data-stu-id="46d6e-1154">Build 14942</span></span>

<span data-ttu-id="46d6e-1155">有关生成14942的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1155">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1156">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1156">Fixed</span></span>

- <span data-ttu-id="46d6e-1157">解决了多个错误检查, 包括正在阻止 SSH 的 "尝试执行 NOEXECUTE 内存" 网络崩溃</span><span class="sxs-lookup"><span data-stu-id="46d6e-1157">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="46d6e-1158">inotifiy 对 DrvFs 上的 Windows 应用程序生成的通知的支持现已在</span><span class="sxs-lookup"><span data-stu-id="46d6e-1158">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="46d6e-1159">实现 TCP_KEEPIDLE 和 TCP_KEEPINTVL for mongod.exe。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1159">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="46d6e-1160">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1160">(GH #695)</span></span>
- <span data-ttu-id="46d6e-1161">实现 pivot_root 系统调用</span><span class="sxs-lookup"><span data-stu-id="46d6e-1161">Implement the pivot_root system call</span></span>
- <span data-ttu-id="46d6e-1162">为 SO_DONTROUTE 实现套接字选项</span><span class="sxs-lookup"><span data-stu-id="46d6e-1162">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="46d6e-1163">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1163">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="46d6e-1164">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1164">LTP Results:</span></span>
<span data-ttu-id="46d6e-1165">通过的测试数:665</span><span class="sxs-lookup"><span data-stu-id="46d6e-1165">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="46d6e-1166">未通过的数目 (失败，已跳过，等等...):263</span><span class="sxs-lookup"><span data-stu-id="46d6e-1166">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="46d6e-1167">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1167">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1168">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1168">Syscall Support</span></span>
<span data-ttu-id="46d6e-1169">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1169">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1170">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1170">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="46d6e-1171">生成14936</span><span class="sxs-lookup"><span data-stu-id="46d6e-1171">Build 14936</span></span>

<span data-ttu-id="46d6e-1172">有关生成14936的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1172">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="46d6e-1173">注意:在即将发布的版本中, WSL 将安装 Ubuntu 版本 16.04 (Xenial), 而不是 Ubuntu 14.04 (t)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1173">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="46d6e-1174">此更改将应用于安装新实例的预览体验 (lxrun/install 或首次运行 bash)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1174">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="46d6e-1175">具有 t 的现有实例将不自动升级。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1175">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="46d6e-1176">用户可以使用 "t-升级" 命令将其 "" 映像升级到 Xenial。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1176">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="46d6e-1177">已知问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1177">Known Issue</span></span>
<span data-ttu-id="46d6e-1178">WSL 遇到一些套接字实现问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1178">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="46d6e-1179">错误检查会将自身视为崩溃, 并出现错误 "已尝试执行 NOEXECUTE 内存"。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1179">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="46d6e-1180">此问题的最常见表现形式是使用 ssh 时出现故障。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1180">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="46d6e-1181">根本原因是在内部版本中修复的, 将按最早的机会推送到内部版本。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1181">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="46d6e-1182">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1182">Fixed</span></span>

- <span data-ttu-id="46d6e-1183">实现了 chroot 系统调用</span><span class="sxs-lookup"><span data-stu-id="46d6e-1183">Implemented the chroot system call</span></span>
- <span data-ttu-id="46d6e-1184">Inotify 中的改进~~, 包括支持在 DrvFs 上的 Windows 应用程序中生成的通知~~</span><span class="sxs-lookup"><span data-stu-id="46d6e-1184">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="46d6e-1185">更正Inotify 对源自 Windows 应用程序的更改的支持目前不可用。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1185">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="46d6e-1186">将套接字绑定到 IPV6<port n> :: 现在支持 IPV6_V6ONLY (GH #68、#157、#393、#460、#674、#740、#982、#996)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1186">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="46d6e-1187">Waitid systemcall 实现的 WNOWAIT 行为 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1187">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="46d6e-1188">支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="46d6e-1188">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="46d6e-1189">长度为零的读取 () 应立即返回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1189">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="46d6e-1190">正确处理在 tar 文件中不包括 NULL 终止符的文件名和文件名前缀。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1190">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="46d6e-1191">epoll 对/dev/null 的支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1191">epoll support for /dev/null</span></span>
- <span data-ttu-id="46d6e-1192">修复/dev/alarm 时间源</span><span class="sxs-lookup"><span data-stu-id="46d6e-1192">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="46d6e-1193">Bash-c 现在可以重定向到文件</span><span class="sxs-lookup"><span data-stu-id="46d6e-1193">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="46d6e-1194">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1194">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1195">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1195">LTP Results:</span></span>
<span data-ttu-id="46d6e-1196">通过的测试数:664</span><span class="sxs-lookup"><span data-stu-id="46d6e-1196">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="46d6e-1197">未通过的数目 (失败，已跳过，等等...):264</span><span class="sxs-lookup"><span data-stu-id="46d6e-1197">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="46d6e-1198">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1198">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1199">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1199">Syscall Support</span></span>
<span data-ttu-id="46d6e-1200">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1200">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1201">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1201">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="46d6e-1202">生成14931</span><span class="sxs-lookup"><span data-stu-id="46d6e-1202">Build 14931</span></span>

<span data-ttu-id="46d6e-1203">有关生成14931的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1203">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1204">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1204">Fixed</span></span>

 - <span data-ttu-id="46d6e-1205">由于控件之外的情况, 对于适用于 Linux 的 Windows 子系统, 此版本中没有更新。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1205">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="46d6e-1206">定期计划的更新将在下一版本中继续进行。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1206">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="46d6e-1207">生成14926</span><span class="sxs-lookup"><span data-stu-id="46d6e-1207">Build 14926</span></span>

<span data-ttu-id="46d6e-1208">有关生成14926的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1208">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1209">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1209">Fixed</span></span>

- <span data-ttu-id="46d6e-1210">Ping 现在适用于没有管理员权限的控制台</span><span class="sxs-lookup"><span data-stu-id="46d6e-1210">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="46d6e-1211">现在还支持 Ping6, 无需管理员权限</span><span class="sxs-lookup"><span data-stu-id="46d6e-1211">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="46d6e-1212">Inotify 支持通过 WSL 修改的文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1212">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="46d6e-1213">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1213">(GH #216)</span></span>
  - <span data-ttu-id="46d6e-1214">支持的标志:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1214">Flags supported:</span></span>
    - <span data-ttu-id="46d6e-1215">inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="46d6e-1215">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="46d6e-1216">inotify_add_watch 事件:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="46d6e-1216">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="46d6e-1217">inotify_add_watch 属性:LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="46d6e-1217">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="46d6e-1218">读取输出:LX_IN_ISDIR, LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="46d6e-1218">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="46d6e-1219">已知问题:修改 Windows 应用程序中的文件不会生成任何事件</span><span class="sxs-lookup"><span data-stu-id="46d6e-1219">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="46d6e-1220">Unix 套接字现在支持 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="46d6e-1220">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="46d6e-1221">LTP 结果:</span><span class="sxs-lookup"><span data-stu-id="46d6e-1221">LTP Results:</span></span>
<span data-ttu-id="46d6e-1222">通过的测试数:651</span><span class="sxs-lookup"><span data-stu-id="46d6e-1222">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="46d6e-1223">未通过的数目 (失败，已跳过，等等...):258</span><span class="sxs-lookup"><span data-stu-id="46d6e-1223">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="46d6e-1224">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1224">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="46d6e-1225">生成14915</span><span class="sxs-lookup"><span data-stu-id="46d6e-1225">Build 14915</span></span>

<span data-ttu-id="46d6e-1226">有关生成14915的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1226">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1227">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1227">Fixed</span></span>
-  <span data-ttu-id="46d6e-1228">Socketpair for unix 数据报套接字 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1228">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="46d6e-1229">适用于 SO_REUSEADDR 的 Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1229">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="46d6e-1230">UNIX 套接字支持 SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1230">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="46d6e-1231">适用于 SOCK_SEQPACKET (GH #758, #546) 的 Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1231">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="46d6e-1232">添加对 unix 数据报套接字发送、接收和关闭的支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1232">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="46d6e-1233">由于非固定地址的 mmap 参数验证无效, 因此修复了检测错误。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1233">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="46d6e-1234">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1234">(GH #847)</span></span>
- <span data-ttu-id="46d6e-1235">支持暂停/继续停止状态</span><span class="sxs-lookup"><span data-stu-id="46d6e-1235">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="46d6e-1236">支持 TIOCPKT ioctl 阻止屏幕实用工具 (GH #774)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1236">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="46d6e-1237">已知问题:功能键不可操作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1237">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="46d6e-1238">更正了 TimerFd 中的争用, 这可能导致 LxpTimerFdWorkerRoutine (GH #814) 访问已释放的成员 "ReaderReady"</span><span class="sxs-lookup"><span data-stu-id="46d6e-1238">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="46d6e-1239">为 futex、投票和 clock_nanosleep 启用可重启的系统调用支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1239">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="46d6e-1240">添加了 bind 装载支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1240">Added bind mount support</span></span>
- <span data-ttu-id="46d6e-1241">用于装载命名空间支持的取消共享</span><span class="sxs-lookup"><span data-stu-id="46d6e-1241">unshare for mount namespace support</span></span>
    - <span data-ttu-id="46d6e-1242">已知问题:使用`unshare(CLONE_NEWNS)`当前工作目录创建新的装载命名空间时, 将继续指向旧命名空间</span><span class="sxs-lookup"><span data-stu-id="46d6e-1242">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="46d6e-1243">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-1243">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="46d6e-1244">生成14905</span><span class="sxs-lookup"><span data-stu-id="46d6e-1244">Build 14905</span></span>

<span data-ttu-id="46d6e-1245">有关生成14905的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1245">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1246">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1246">Fixed</span></span>
- <span data-ttu-id="46d6e-1247">现在支持可重启的系统调用 (GH #349, GH #520)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1247">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="46d6e-1248">符号链接结束/立即操作的目录 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1248">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="46d6e-1249">为/dev/random 实现了 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="46d6e-1249">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="46d6e-1250">实现了/proc/[pid]/mounts、/proc/[pid]/mountinfo 和/proc/[pid]/mountstats 文件</span><span class="sxs-lookup"><span data-stu-id="46d6e-1250">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="46d6e-1251">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1251">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="46d6e-1252">生成14901</span><span class="sxs-lookup"><span data-stu-id="46d6e-1252">Build 14901</span></span>
<span data-ttu-id="46d6e-1253">Windows 10 周年更新版本的第一批内幕构建。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1253">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="46d6e-1254">有关生成14901的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1254">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1255">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1255">Fixed</span></span>
- <span data-ttu-id="46d6e-1256">修复了尾随斜杠问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1256">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="46d6e-1257">像现在这样`$ mv a/c/ a/b/`的命令</span><span class="sxs-lookup"><span data-stu-id="46d6e-1257">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="46d6e-1258">如果 Ubuntu 区域设置应设置为 Windows 区域设置, 则立即安装</span><span class="sxs-lookup"><span data-stu-id="46d6e-1258">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="46d6e-1259">Procfs 支持 ns 文件夹</span><span class="sxs-lookup"><span data-stu-id="46d6e-1259">Procfs support for ns folder</span></span>
- <span data-ttu-id="46d6e-1260">添加了 tmpfs、procfs 和 sysfs 文件系统的装载和卸载</span><span class="sxs-lookup"><span data-stu-id="46d6e-1260">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="46d6e-1261">修复 mknod [at] 32 位 ABI 签名</span><span class="sxs-lookup"><span data-stu-id="46d6e-1261">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="46d6e-1262">Unix 套接字已移动到调度模型</span><span class="sxs-lookup"><span data-stu-id="46d6e-1262">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="46d6e-1263">INET 套接字接收使用 setsockopt 设置的缓冲区大小应遵守</span><span class="sxs-lookup"><span data-stu-id="46d6e-1263">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="46d6e-1264">实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志</span><span class="sxs-lookup"><span data-stu-id="46d6e-1264">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="46d6e-1265">Linux 进程 stdin/stdout 管道重定向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1265">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="46d6e-1266">允许在 CMD 中管道的 bash 命令。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1266">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="46d6e-1267">示例: > dir |bash-c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="46d6e-1267">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="46d6e-1268">Bash 现在可以安装在具有多个页面页面 (GH #538, #358) 的系统上</span><span class="sxs-lookup"><span data-stu-id="46d6e-1268">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="46d6e-1269">默认的 INET 套接字缓冲区大小应与默认 Ubuntu 安装程序的大小匹配</span><span class="sxs-lookup"><span data-stu-id="46d6e-1269">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="46d6e-1270">将 xattr syscall 与 listxattr 对齐</span><span class="sxs-lookup"><span data-stu-id="46d6e-1270">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="46d6e-1271">仅返回具有 SIOCGIFCONF 的有效 IPv4 地址的接口</span><span class="sxs-lookup"><span data-stu-id="46d6e-1271">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="46d6e-1272">修复 ptrace 注入的信号默认操作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1272">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="46d6e-1273">实现/proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="46d6e-1273">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="46d6e-1274">还原 sigreturn 中的上下文时使用计算机上下文寄存器值</span><span class="sxs-lookup"><span data-stu-id="46d6e-1274">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="46d6e-1275">这解决了某些用户的 java 和 javac 挂起的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1275">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="46d6e-1276">实现/proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="46d6e-1276">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1277">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1277">Syscall Support</span></span>
<span data-ttu-id="46d6e-1278">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1278">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1279">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1279">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="46d6e-1280">生成14388到 Windows 10 周年更新</span><span class="sxs-lookup"><span data-stu-id="46d6e-1280">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="46d6e-1281">有关生成14388的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1281">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1282">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1282">Fixed</span></span>
- <span data-ttu-id="46d6e-1283">修复了8/2 上 Windows 10 周年更新的准备工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1283">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="46d6e-1284">有关周年更新中的 WSL 的详细信息, 请参阅我们的[博客](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1284">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="46d6e-1285">生成14376</span><span class="sxs-lookup"><span data-stu-id="46d6e-1285">Build 14376</span></span>
<span data-ttu-id="46d6e-1286">有关生成14376的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1286">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1287">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1287">Fixed</span></span>
- <span data-ttu-id="46d6e-1288">删除了一些实例, 其中 apt 挂起 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1288">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="46d6e-1289">修复了未正确处理空装载的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1289">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="46d6e-1290">修复了 ramdisks 未正确装载的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1290">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="46d6e-1291">更改 unix 套接字接受以支持标志 (部分 GH #451)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1291">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="46d6e-1292">修复了与通用网络相关的蓝屏</span><span class="sxs-lookup"><span data-stu-id="46d6e-1292">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="46d6e-1293">修复了访问/proc/时的蓝屏 [pid]/task (GH #523)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1293">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="46d6e-1294">修复了某些 pty 方案的高 CPU 使用率 (GH #488, #504)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1294">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="46d6e-1295">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1295">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="46d6e-1296">生成14371</span><span class="sxs-lookup"><span data-stu-id="46d6e-1296">Build 14371</span></span>
<span data-ttu-id="46d6e-1297">有关生成14371的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1297">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1298">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1298">Fixed</span></span>
- <span data-ttu-id="46d6e-1299">使用 ptrace 更正计时争用与 SIGCHLD 和 wait ()</span><span class="sxs-lookup"><span data-stu-id="46d6e-1299">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="46d6e-1300">当路径具有尾随/(GH #432) 时更正了某些行为</span><span class="sxs-lookup"><span data-stu-id="46d6e-1300">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="46d6e-1301">修复了重命名/取消链接因打开子句柄而失败的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1301">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="46d6e-1302">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1302">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="46d6e-1303">生成14366</span><span class="sxs-lookup"><span data-stu-id="46d6e-1303">Build 14366</span></span>
<span data-ttu-id="46d6e-1304">有关生成14366的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1304">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1305">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1305">Fixed</span></span>
- <span data-ttu-id="46d6e-1306">通过符号链接在文件创建中修复</span><span class="sxs-lookup"><span data-stu-id="46d6e-1306">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="46d6e-1307">添加了适用于 Python 的 listxattr (GH 385)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1307">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="46d6e-1308">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1308">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1309">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1309">Syscall Support</span></span>
-   <span data-ttu-id="46d6e-1310">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1310">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1311">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1311">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="46d6e-1312">生成14361</span><span class="sxs-lookup"><span data-stu-id="46d6e-1312">Build 14361</span></span>
<span data-ttu-id="46d6e-1313">有关生成14361的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1313">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1314">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1314">Fixed</span></span>
- <span data-ttu-id="46d6e-1315">在 Windows 上的 Ubuntu 上运行 Bash 时, DrvFs 现在区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1315">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="46d6e-1316">用户可以为 .txt 和 CASE。/Mnt/c 驱动器上的 TXT</span><span class="sxs-lookup"><span data-stu-id="46d6e-1316">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="46d6e-1317">Windows 上的 Bash 中仅支持区分大小写。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1317">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="46d6e-1318">在 Bash NTFS 外, 会正确报告文件, 但可能会发生意外行为, 与 Windows 中的文件交互。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1318">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="46d6e-1319">每个卷的根目录 (即/mnt/c) 不区分大小写</span><span class="sxs-lookup"><span data-stu-id="46d6e-1319">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="46d6e-1320">可在[此处](https://support.microsoft.com/en-us/kb/100625)找到有关如何处理 Windows 中的这些文件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1320">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="46d6e-1321">大大增强了 pty/tty 支持。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1321">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="46d6e-1322">现在支持 TMUX 等应用程序 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1322">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="46d6e-1323">修复了不总是创建用户帐户的安装问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1323">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="46d6e-1324">优化的命令行 arg 结构, 允许非常长的参数列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1324">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="46d6e-1325">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1325">(GH #153)</span></span>
- <span data-ttu-id="46d6e-1326">现可从 DrvFs 删除和 chmod read_only 文件</span><span class="sxs-lookup"><span data-stu-id="46d6e-1326">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="46d6e-1327">修复了终端在断开连接时挂起的某些实例 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1327">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="46d6e-1328">chmod 和 chown 现在可在 tty 设备上工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1328">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="46d6e-1329">允许连接到0.0.0.0 和:: 作为 localhost (GH #388)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1329">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="46d6e-1330">Sendmsg/recvmsg 现在处理 > 1 (partial GH #376) 的 IO 矢量长度</span><span class="sxs-lookup"><span data-stu-id="46d6e-1330">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="46d6e-1331">用户现在可以选择退出自动生成的 hosts 文件 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1331">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="46d6e-1332">在安装期间自动将 Linux 区域设置与 NT 区域设置匹配 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1332">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="46d6e-1333">添加了/proc/sys/vm/swappiness 文件 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1333">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="46d6e-1334">跟踪来现已正确退出</span><span class="sxs-lookup"><span data-stu-id="46d6e-1334">strace now exits correctly</span></span>
- <span data-ttu-id="46d6e-1335">允许通过/proc/self/fd 重新打开管道 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1335">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="46d6e-1336">隐藏%LOCALAPPDATA%\lxss 中的目录 DrvFs (GH #270)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1336">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="46d6e-1337">更好地处理 bash ~。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1337">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="46d6e-1338">现在支持类似于 "bash ~-c ls" 的命令 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1338">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="46d6e-1339">插座现在会通知 epoll 读取在关闭期间可用 (GH #271)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1339">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="46d6e-1340">lxrun/uninstall 更好地删除文件和文件夹</span><span class="sxs-lookup"><span data-stu-id="46d6e-1340">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="46d6e-1341">更正的 ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1341">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="46d6e-1342">改善了对 x11 应用的支持, 如 xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1342">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="46d6e-1343">已更新初始线程堆栈大小以匹配默认 Ubuntu 设置, 并正确报告 get_rlimit syscall 的大小 (GH #172, #258)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1343">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="46d6e-1344">改善了 pico 进程映像名称 (例如, 审核) 的报告</span><span class="sxs-lookup"><span data-stu-id="46d6e-1344">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="46d6e-1345">为 df 命令实现了/proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="46d6e-1345">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="46d6e-1346">修复了子名称的符号链接错误代码。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1346">Fixed symlink error code for child name .</span></span> <span data-ttu-id="46d6e-1347">和。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1347">and ..</span></span>
- <span data-ttu-id="46d6e-1348">其他改进 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1348">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1349">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1349">Syscall Support</span></span>
<span data-ttu-id="46d6e-1350">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1350">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1351">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1351">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="46d6e-1352">生成14352</span><span class="sxs-lookup"><span data-stu-id="46d6e-1352">Build 14352</span></span>
<span data-ttu-id="46d6e-1353">有关生成14352的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1353">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1354">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1354">Fixed</span></span>
- <span data-ttu-id="46d6e-1355">修复了找不到正确下载/创建大型文件的问题。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1355">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="46d6e-1356">这应取消阻止 npm 和其他方案 (GH #3, GH #313)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1356">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="46d6e-1357">删除了套接字挂起的一些实例</span><span class="sxs-lookup"><span data-stu-id="46d6e-1357">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="46d6e-1358">更正了一些 ptrace 错误</span><span class="sxs-lookup"><span data-stu-id="46d6e-1358">Corrected some ptrace errors</span></span>
- <span data-ttu-id="46d6e-1359">修复了 WSL 的问题, 允许文件名超过255个字符</span><span class="sxs-lookup"><span data-stu-id="46d6e-1359">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="46d6e-1360">改进了对非英语字符的支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1360">Improved support for non-English characters</span></span>
- <span data-ttu-id="46d6e-1361">添加当前 Windows 时区数据并将其设置为默认值</span><span class="sxs-lookup"><span data-stu-id="46d6e-1361">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="46d6e-1362">每个装入点的唯一设备 id (jre fix – GH #49)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1362">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="46d6e-1363">更正包含 "." 的路径的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1363">Correct issue with paths containing “.”</span></span> <span data-ttu-id="46d6e-1364">和 "..."</span><span class="sxs-lookup"><span data-stu-id="46d6e-1364">and “..”</span></span>
- <span data-ttu-id="46d6e-1365">添加了 Fifo 支持 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1365">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="46d6e-1366">已更新 resolv.conf 格式, 以匹配本地 Ubuntu 格式</span><span class="sxs-lookup"><span data-stu-id="46d6e-1366">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="46d6e-1367">某些 procfs 清理</span><span class="sxs-lookup"><span data-stu-id="46d6e-1367">Some procfs cleanup</span></span>
- <span data-ttu-id="46d6e-1368">为管理员控制台启用了 ping (GH #18)</span><span class="sxs-lookup"><span data-stu-id="46d6e-1368">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1369">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1369">Syscall Support</span></span>
<span data-ttu-id="46d6e-1370">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1370">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1371">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1371">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="46d6e-1372">生成14342</span><span class="sxs-lookup"><span data-stu-id="46d6e-1372">Build 14342</span></span>
<span data-ttu-id="46d6e-1373">有关[Windows 博客](https://aka.ms/wip14342)上版本14342的常规 windows 信息。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1373">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="46d6e-1374">有关 VolFs 和 DriveFs 的信息, 请参阅[WSL 博客](https://blogs.msdn.microsoft.com/wsl)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1374">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="46d6e-1375">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1375">Fixed</span></span>
- <span data-ttu-id="46d6e-1376">修复了 Windows 用户在用户名中包含 Unicode 字符时的安装问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1376">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="46d6e-1377">默认情况下, 在首次运行时, 默认情况下提供常见问题中的 apt-get update udev 解决方法</span><span class="sxs-lookup"><span data-stu-id="46d6e-1377">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="46d6e-1378">已启用 DriveFs (/mnt/<drive>) 目录中的符号链接</span><span class="sxs-lookup"><span data-stu-id="46d6e-1378">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="46d6e-1379">符号链接在 DriveFs 和 VolFs 之间工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1379">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="46d6e-1380">解决了顶层路径分析问题: ls.//现在将按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1380">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="46d6e-1381">npm 安装在 DriveFs 上并且-g 选项现在正在工作</span><span class="sxs-lookup"><span data-stu-id="46d6e-1381">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="46d6e-1382">修复了阻止 PHP 服务器启动的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1382">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="46d6e-1383">更新了默认环境值, 例如 $PATH 以便更接近本地 Ubuntu</span><span class="sxs-lookup"><span data-stu-id="46d6e-1383">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="46d6e-1384">在 Windows 中添加了每周维护任务以更新 apt 包缓存</span><span class="sxs-lookup"><span data-stu-id="46d6e-1384">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="46d6e-1385">修复了 ELF 标头验证问题, WSL 现在支持所有 Melkor 选项</span><span class="sxs-lookup"><span data-stu-id="46d6e-1385">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="46d6e-1386">Zsh shell 正常运行</span><span class="sxs-lookup"><span data-stu-id="46d6e-1386">Zsh shell is functional</span></span>
- <span data-ttu-id="46d6e-1387">现在支持预编译的中转二进制文件</span><span class="sxs-lookup"><span data-stu-id="46d6e-1387">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="46d6e-1388">在 Bash 首次运行时提示现在已正确本地化</span><span class="sxs-lookup"><span data-stu-id="46d6e-1388">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="46d6e-1389">/proc/meminfo 现在返回正确的信息</span><span class="sxs-lookup"><span data-stu-id="46d6e-1389">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="46d6e-1390">VFS 现在支持套接字</span><span class="sxs-lookup"><span data-stu-id="46d6e-1390">Sockets now supported in VFS</span></span>
- <span data-ttu-id="46d6e-1391">/dev 现在装载为 tempfs</span><span class="sxs-lookup"><span data-stu-id="46d6e-1391">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="46d6e-1392">现在支持 Fifo</span><span class="sxs-lookup"><span data-stu-id="46d6e-1392">Fifo now supported</span></span>
- <span data-ttu-id="46d6e-1393">多核系统现在在/proc/cpuinfo 中显示正确</span><span class="sxs-lookup"><span data-stu-id="46d6e-1393">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="46d6e-1394">首次运行时下载的其他改进和错误消息</span><span class="sxs-lookup"><span data-stu-id="46d6e-1394">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="46d6e-1395">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1395">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="46d6e-1396">下面支持的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1396">Supported syscall list below.</span></span>
- <span data-ttu-id="46d6e-1397">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1397">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="46d6e-1398">已知问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1398">Known Issues</span></span>
- <span data-ttu-id="46d6e-1399">不解析 "..."</span><span class="sxs-lookup"><span data-stu-id="46d6e-1399">Not resolving ‘..’</span></span> <span data-ttu-id="46d6e-1400">在某些情况下, 在 DriveFs 上正确</span><span class="sxs-lookup"><span data-stu-id="46d6e-1400">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1401">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1401">Syscall Support</span></span>
<span data-ttu-id="46d6e-1402">下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1402">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1403">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1403">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FCHOWNAT`<br/>
`GETEUID`<br/>
`GETGID`<br/>
`GETRESUID`<br/>
`GETXATTR`<br/>
`PTRACE`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETXATTR`<br/>
<br/>

## <a name="build-14332"></a><span data-ttu-id="46d6e-1404">生成14332</span><span class="sxs-lookup"><span data-stu-id="46d6e-1404">Build 14332</span></span>

<span data-ttu-id="46d6e-1405">有关生成14332的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1405">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="46d6e-1406">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1406">Fixed</span></span>
- <span data-ttu-id="46d6e-1407">更好的 resolv.conf 生成, 包括优先级 DNS 条目</span><span class="sxs-lookup"><span data-stu-id="46d6e-1407">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="46d6e-1408">在/mnt 和非/mnt 驱动器之间移动文件和目录时出现的问题</span><span class="sxs-lookup"><span data-stu-id="46d6e-1408">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="46d6e-1409">现在可以通过符号链接创建 Tar 文件。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1409">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="46d6e-1410">创建实例时添加了默认的/run/lock 目录</span><span class="sxs-lookup"><span data-stu-id="46d6e-1410">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="46d6e-1411">更新/dev/null 以返回正确的 stat 信息</span><span class="sxs-lookup"><span data-stu-id="46d6e-1411">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="46d6e-1412">首次运行期间下载时出现的其他错误</span><span class="sxs-lookup"><span data-stu-id="46d6e-1412">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="46d6e-1413">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1413">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="46d6e-1414">下面支持的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1414">Supported syscall list below.</span></span>
- <span data-ttu-id="46d6e-1415">其他改进 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1415">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1416">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1416">Syscall Support</span></span>
<span data-ttu-id="46d6e-1417">下面是在 WSL 中具有一些实现的新 syscall。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1417">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="46d6e-1418">此列表中的 syscall 至少在一种方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1418">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="46d6e-1419">生成14328</span><span class="sxs-lookup"><span data-stu-id="46d6e-1419">Build 14328</span></span>

<span data-ttu-id="46d6e-1420">有关生成14332的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1420">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="46d6e-1421">新功能</span><span class="sxs-lookup"><span data-stu-id="46d6e-1421">New Features</span></span>
* <span data-ttu-id="46d6e-1422">现在支持 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1422">Now support Linux users.</span></span>  <span data-ttu-id="46d6e-1423">在 Windows 上的 Ubuntu 上安装 Bash 将提示创建 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1423">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="46d6e-1424">有关详细信息, 请访问 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="46d6e-1424">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="46d6e-1425">现在, 主机名设置为 Windows 计算机名称, 不能再@localhost</span><span class="sxs-lookup"><span data-stu-id="46d6e-1425">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="46d6e-1426">有关生成14328的详细信息, 请访问: https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="46d6e-1426">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="46d6e-1427">固定</span><span class="sxs-lookup"><span data-stu-id="46d6e-1427">Fixed</span></span>
* <span data-ttu-id="46d6e-1428">非/mnt/<drive>文件的符号改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1428">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="46d6e-1429">npm 安装现可正常运行</span><span class="sxs-lookup"><span data-stu-id="46d6e-1429">npm install now works</span></span>
    * <span data-ttu-id="46d6e-1430">现在使用[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)的说明可安装 jdk/jre。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1430">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="46d6e-1431">已知问题: 符号链接不适用于 Windows 安装。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1431">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="46d6e-1432">功能将在以后的版本中提供</span><span class="sxs-lookup"><span data-stu-id="46d6e-1432">Functionality will be available in a later build</span></span>
* <span data-ttu-id="46d6e-1433">顶部和 htop 现在显示</span><span class="sxs-lookup"><span data-stu-id="46d6e-1433">top and htop now display</span></span>
* <span data-ttu-id="46d6e-1434">某些安装失败的其他错误消息</span><span class="sxs-lookup"><span data-stu-id="46d6e-1434">Additional error messages for some install failures</span></span>
* <span data-ttu-id="46d6e-1435">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1435">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="46d6e-1436">下面支持的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1436">Supported syscall list below.</span></span>
* <span data-ttu-id="46d6e-1437">其他改进 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="46d6e-1437">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="46d6e-1438">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="46d6e-1438">Syscall Support</span></span>
<span data-ttu-id="46d6e-1439">下面是在 WSL 中具有一些实现的 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1439">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="46d6e-1440">此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。</span><span class="sxs-lookup"><span data-stu-id="46d6e-1440">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`ACCEPT`<br/>
`ACCEPT4`<br/>
`ACCESS`<br/>
`ALARM`<br/>
`ARCH_PRCTL`<br/>
`BIND`<br/>
`BRK`<br/>
`CAPGET`<br/>
`CAPSET`<br/>
`CHDIR`<br/>
`CHMOD`<br/>
`CHOWN`<br/>
`CLOCK_GETRES`<br/>
`CLOCK_GETTIME`<br/>
`CLOCK_NANOSLEEP`<br/>
`CLONE`<br/>
`CLOSE`<br/>
`CONNECT`<br/>
`CREAT`<br/>
`DUP`<br/>
`DUP2`<br/>
`DUP3`<br/>
`EPOLL_CREATE`<br/>
`EPOLL_CREATE1`<br/>
`EPOLL_CTL`<br/>
`EPOLL_WAIT`<br/>
`EVENTFD`<br/>
`EVENTFD2`<br/>
`EXECVE`<br/>
`EXIT`<br/>
`EXIT_GROUP`<br/>
`FACCESSAT`<br/>
`FADVISE64`<br/>
`FCHDIR`<br/>
`FCHMOD`<br/>
`FCHMODAT`<br/>
`FCHOWN`<br/>
`FCHOWNAT`<br/>
`FCNTL64`<br/>
`FDATASYNC`<br/>
`FLOCK`<br/>
`FORK`<br/>
`FSETXATTR`<br/>
`FSTAT64`<br/>
`FSTATAT64`<br/>
`FSTATFS64`<br/>
`FSYNC`<br/>
`FTRUNCATE`<br/>
`FTRUNCATE64`<br/>
`FUTEX`<br/>
`GETCPU`<br/>
`GETCWD`<br/>
`GETDENTS`<br/>
`GETDENTS64`<br/>
`GETEGID`<br/>
`GETEGID16`<br/>
`GETEUID`<br/>
`GETEUID16`<br/>
`GETGID`<br/>
`GETGID16`<br/>
`GETGROUPS`<br/>
`GETPEERNAME`<br/>
`GETPGID`<br/>
`GETPGRP`<br/>
`GETPID`<br/>
`GETPPID`<br/>
`GETPRIORITY`<br/>
`GETRESGID`<br/>
`GETRESGID16`<br/>
`GETRESUID`<br/>
`GETRESUID16`<br/>
`GETRLIMIT`<br/>
`GETRUSAGE`<br/>
`GETSID`<br/>
`GETSOCKNAME`<br/>
`GETSOCKOPT`<br/>
`GETTID`<br/>
`GETTIMEOFDAY`<br/>
`GETUID`<br/>
`GETUID16`<br/>
`GETXATTR`<br/>
`GET_ROBUST_LIST`<br/>
`GET_THREAD_AREA`<br/>
`INOTIFY_ADD_WATCH`<br/>
`INOTIFY_INIT`<br/>
`INOTIFY_RM_WATCH`<br/>
`IOCTL`<br/>
`IOPRIO_GET`<br/>
`IOPRIO_SET`<br/>
`KEYCTL`<br/>
`KILL`<br/>
`LCHOWN`<br/>
`LINK`<br/>
`LINKAT`<br/>
`LISTEN`<br/>
`LLSEEK`<br/>
`LSEEK`<br/>
`LSTAT64`<br/>
`MADVISE`<br/>
`MKDIR`<br/>
`MKDIRAT`<br/>
`MKNOD`<br/>
`MLOCK`<br/>
`MMAP`<br/>
`MMAP2`<br/>
`MOUNT`<br/>
`MPROTECT`<br/>
`MREMAP`<br/>
`MSYNC`<br/>
`MUNLOCK`<br/>
`MUNMAP`<br/>
`NANOSLEEP`<br/>
`NEWUNAME`<br/>
`OPEN`<br/>
`OPENAT`<br/>
`PAUSE`<br/>
`PERF_EVENT_OPEN`<br/>
`PERSONALITY`<br/>
`PIPE`<br/>
`PIPE2`<br/>
`POLL`<br/>
`PPOLL`<br/>
`PRCTL`<br/>
`PREAD64`<br/>
`PROCESS_VM_READV`<br/>
`PROCESS_VM_WRITEV`<br/>
`PSELECT6`<br/>
`PTRACE`<br/>
`PWRITE64`<br/>
`READ`<br/>
`READLINK`<br/>
`READV`<br/>
`REBOOT`<br/>
`RECV`<br/>
`RECVFROM`<br/>
`RECVMSG`<br/>
`RENAME`<br/>
`RMDIR`<br/>
`RT_SIGACTION`<br/>
`RT_SIGPENDING`<br/>
`RT_SIGPROCMASK`<br/>
`RT_SIGRETURN`<br/>
`RT_SIGSUSPEND`<br/>
`RT_SIGTIMEDWAIT`<br/>
`SCHED_GETAFFINITY`<br/>
`SCHED_GETPARAM`<br/>
`SCHED_GETSCHEDULER`<br/>
`SCHED_GET_PRIORITY_MAX`<br/>
`SCHED_GET_PRIORITY_MIN`<br/>
`SCHED_SETAFFINITY`<br/>
`SCHED_SETPARAM`<br/>
`SCHED_SETSCHEDULER`<br/>
`SCHED_YIELD`<br/>
`SELECT`<br/>
`SEND`<br/>
`SENDMMSG`<br/>
`SENDMSG`<br/>
`SENDTO`<br/>
`SETDOMAINNAME`<br/>
`SETGID`<br/>
`SETGROUPS`<br/>
`SETHOSTNAME`<br/>
`SETITIMER`<br/>
`SETPGID`<br/>
`SETPRIORITY`<br/>
`SETREGID`<br/>
`SETRESGID`<br/>
`SETRESUID`<br/>
`SETREUID`<br/>
`SETRLIMIT`<br/>
`SETSID`<br/>
`SETSOCKOPT`<br/>
`SETTIMEOFDAY`<br/>
`SETUID`<br/>
`SETXATTR`<br/>
`SET_ROBUST_LIST`<br/>
`SET_THREAD_AREA`<br/>
`SET_TID_ADDRESS`<br/>
`SHUTDOWN`<br/>
`SIGACTION`<br/>
`SIGALTSTACK`<br/>
`SIGPENDING`<br/>
`SIGPROCMASK`<br/>
`SIGRETURN`<br/>
`SIGSUSPEND`<br/>
`SOCKET`<br/>
`SOCKETCALL`<br/>
`SOCKETPAIR`<br/>
`SPLICE`<br/>
`STAT64`<br/>
`STATFS64`<br/>
`SYMLINK`<br/>
`SYMLINKAT`<br/>
`SYNC`<br/>
`SYSINFO`<br/>
`TEE`<br/>
`TGKILL`<br/>
`TIME`<br/>
`TIMERFD_CREATE`<br/>
`TIMERFD_GETTIME`<br/>
`TIMERFD_SETTIME`<br/>
`TIMES`<br/>
`TKILL`<br/>
`TRUNCATE`<br/>
`TRUNCATE64`<br/>
`UMASK`<br/>
`UMOUNT`<br/>
`UMOUNT2`<br/>
`UNLINK`<br/>
`UNLINKAT`<br/>
`UNSHARE`<br/>
`UTIME`<br/>
`UTIMENSAT`<br/>
`UTIMES`<br/>
`VFORK`<br/>
`WAIT4`<br/>
`WAITPID`<br/>
`WRITE`<br/>
`WRITEV`<br/>
