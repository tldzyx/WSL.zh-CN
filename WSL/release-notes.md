---
title: 适用于 Linux 的 Windows 子系统的发行说明
description: 适用于 Linux 的 Windows 子系统的发行说明。  每周更新。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu 的 windows 子系统
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: 2567e68ca0e9897a7b7bc7315760b81ff4923c1a
ms.sourcegitcommit: 8c74868b8d8ff0106e15e4bce5e8337642883ec1
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/01/2019
ms.locfileid: "64988265"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="bafce-105">适用于 Linux 的 Windows 子系统的发行说明</span><span class="sxs-lookup"><span data-stu-id="bafce-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18890"></a><span data-ttu-id="bafce-106">生成 18890</span><span class="sxs-lookup"><span data-stu-id="bafce-106">Build 18890</span></span>
<span data-ttu-id="bafce-107">有关常规 Windows 上生成 18890 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-107">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-108">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-108">WSL</span></span>
* <span data-ttu-id="bafce-109">非阻塞套接字泄漏 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="bafce-109">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="bafce-110">终端的 EOF 输入可以阻止后续读取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="bafce-110">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="bafce-111">更新 resolv.conf 标头来指代 wsl.conf [所述 GH 3928]</span><span class="sxs-lookup"><span data-stu-id="bafce-111">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="bafce-112">死锁中 epoll 删除代码 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="bafce-112">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="bafce-113">处理参数-导入和 – 导出 [GH 3932] 中的空格</span><span class="sxs-lookup"><span data-stu-id="bafce-113">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="bafce-114">扩展 mmap 处理的文件无法正常工作 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="bafce-114">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="bafce-115">修复问题的 ARM64 \\wsl$ 访问不能正常工作</span><span class="sxs-lookup"><span data-stu-id="bafce-115">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="bafce-116">添加 wsl.exe 更好的默认图标</span><span class="sxs-lookup"><span data-stu-id="bafce-116">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="bafce-117">生成 18342</span><span class="sxs-lookup"><span data-stu-id="bafce-117">Build 18342</span></span>
<span data-ttu-id="bafce-118">有关常规 Windows 上生成 18342 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-118">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-119">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-119">WSL</span></span>
* <span data-ttu-id="bafce-120">我们已添加了用户从 Windows 访问 WSL 发行版中的 Linux 文件的能力。</span><span class="sxs-lookup"><span data-stu-id="bafce-120">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="bafce-121">可以通过命令行中，以及 Windows 应用，如文件资源管理器，VSCode 访问这些文件，等可以使用这些文件进行交互。</span><span class="sxs-lookup"><span data-stu-id="bafce-121">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="bafce-122">通过导航到访问的文件\\ \\wsl$\\< distro_name >，或查看运行的分布的方法是导航到列表\\ \\wsl$</span><span class="sxs-lookup"><span data-stu-id="bafce-122">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="bafce-123">添加更多的 CPU 信息标记和修复 Cpus_allowed [列表 （_l)] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="bafce-123">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="bafce-124">支持从非领导线程 [GH 3800] exec</span><span class="sxs-lookup"><span data-stu-id="bafce-124">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="bafce-125">配置更新失败视为非致命性 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="bafce-125">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="bafce-126">更新 binfmt 能够正确处理偏移量 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="bafce-126">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="bafce-127">为计划 9 [GH 3854] 启用映射网络驱动器</span><span class="sxs-lookup"><span data-stu-id="bafce-127">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="bafce-128">支持 Windows-> Linux 和 Linux-> Windows 路径转换为绑定挂载</span><span class="sxs-lookup"><span data-stu-id="bafce-128">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="bafce-129">在打开的文件上创建映射的只读的部分，只读的</span><span class="sxs-lookup"><span data-stu-id="bafce-129">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="bafce-130">生成 18334</span><span class="sxs-lookup"><span data-stu-id="bafce-130">Build 18334</span></span>
<span data-ttu-id="bafce-131">有关常规 Windows 上生成 18334 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-131">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-132">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-132">WSL</span></span>
* <span data-ttu-id="bafce-133">重新设计 Windows 时区映射到 Linux 时区 [GH 3747] 的方式</span><span class="sxs-lookup"><span data-stu-id="bafce-133">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="bafce-134">修复内存泄漏，并添加新的字符串转换函数 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="bafce-134">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="bafce-135">在无线程 threadgroup SIGCONT 是一个无操作 [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="bafce-135">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="bafce-136">正确显示在 /proc/self/fd 套接字和 epoll 文件描述符</span><span class="sxs-lookup"><span data-stu-id="bafce-136">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="bafce-137">生成 18305</span><span class="sxs-lookup"><span data-stu-id="bafce-137">Build 18305</span></span>
<span data-ttu-id="bafce-138">有关常规 Windows 上生成 18305 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-138">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-139">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-139">WSL</span></span>
* <span data-ttu-id="bafce-140">pthreads 失去对文件访问权限，当主线程退出 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="bafce-140">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="bafce-141">TIOCSCTTY 应忽略"force"参数，除非必需，否则 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="bafce-141">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="bafce-142">wsl.exe 命令行改进和添加导入/导出功能。</span><span class="sxs-lookup"><span data-stu-id="bafce-142">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="bafce-143">生成 18277</span><span class="sxs-lookup"><span data-stu-id="bafce-143">Build 18277</span></span>
<span data-ttu-id="bafce-144">有关常规 Windows 上生成 18277 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-144">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-145">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-145">WSL</span></span>
* <span data-ttu-id="bafce-146">修复在生成 18272 [GH 3645] 中引入的"不支持此类接口"错误</span><span class="sxs-lookup"><span data-stu-id="bafce-146">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="bafce-147">忽略 umount syscall [GH 3605] MNT_FORCE 标志</span><span class="sxs-lookup"><span data-stu-id="bafce-147">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="bafce-148">若要使用官方 CreatePseudoConsole API 的交换机 WSL 互操作</span><span class="sxs-lookup"><span data-stu-id="bafce-148">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="bafce-149">FUTEX_WAIT 重新启动时维护任何超时值</span><span class="sxs-lookup"><span data-stu-id="bafce-149">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="bafce-150">生成 18272</span><span class="sxs-lookup"><span data-stu-id="bafce-150">Build 18272</span></span>
<span data-ttu-id="bafce-151">有关常规 Windows 上生成 18272 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-151">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-152">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-152">WSL</span></span>
* <span data-ttu-id="bafce-153">**警告：** 使 WSL 无法运行此生成时出现问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-153">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="bafce-154">尝试启动你的分发时您将看到"不支持此类接口"错误。</span><span class="sxs-lookup"><span data-stu-id="bafce-154">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="bafce-155">此问题已修复，并且将在下一步一周的快速深入了解生成。</span><span class="sxs-lookup"><span data-stu-id="bafce-155">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="bafce-156">如果已安装此您可以回滚到以前的 Windows 内部版本使用"转到返回到以前版本的 Windows 10"在设置生成-> 更新和安全-> 恢复。</span><span class="sxs-lookup"><span data-stu-id="bafce-156">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="bafce-157">生成 18267</span><span class="sxs-lookup"><span data-stu-id="bafce-157">Build 18267</span></span>
<span data-ttu-id="bafce-158">有关常规 Windows 上生成 18267 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-158">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-159">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-159">WSL</span></span>
* <span data-ttu-id="bafce-160">解决的问题，其中僵停进程可能会不 reaped 和无限期地保持。</span><span class="sxs-lookup"><span data-stu-id="bafce-160">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="bafce-161">如果错误消息超过最大长度 [GH 3592] WslRegisterDistribution 挂起</span><span class="sxs-lookup"><span data-stu-id="bafce-161">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="bafce-162">允许 fsync DrvFs [GH 3556] 上的只读文件成功</span><span class="sxs-lookup"><span data-stu-id="bafce-162">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="bafce-163">确保创建符号链接 [GH 3584] 内的之前存在 /bin 和 /sbin 目录</span><span class="sxs-lookup"><span data-stu-id="bafce-163">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="bafce-164">添加 WSL 实例的实例终止超时机制。</span><span class="sxs-lookup"><span data-stu-id="bafce-164">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="bafce-165">超时时间当前设置为 15 秒，这意味着该实例将终止 15 秒的最新的 WSL 进程退出后。</span><span class="sxs-lookup"><span data-stu-id="bafce-165">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="bafce-166">若要立即终止分发，请使用：</span><span class="sxs-lookup"><span data-stu-id="bafce-166">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="bafce-167">生成 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="bafce-167">Build 17763 (1809)</span></span>
<span data-ttu-id="bafce-168">有关常规 Windows 上生成 17763 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-168">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-169">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-169">WSL</span></span>
* <span data-ttu-id="bafce-170">Setpriority syscall 权限检查太严格的更改相同的线程优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="bafce-170">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="bafce-171">确保公平的中断时间使用启动时若要避免返回负数值的 clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="bafce-171">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="bafce-172">在 WSL binfmt 解释器 [GH 3424] 中的句柄符号链接</span><span class="sxs-lookup"><span data-stu-id="bafce-172">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="bafce-173">更好地处理 threadgroup 领导文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="bafce-173">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="bafce-174">切换 WSL 使用而不是 KeQueryPerformanceCounter KeQueryInterruptTimePrecise 以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="bafce-174">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="bafce-175">Ptrace 连接可能会返回的值不正确导致从系统调用 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="bafce-175">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="bafce-176">修复多个 AF_UNIX 相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="bafce-176">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="bafce-177">解决问题可能导致 WSL 互操作，如果当前工作目录为小于 5 个字符长 [GH 3379] 失败</span><span class="sxs-lookup"><span data-stu-id="bafce-177">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="bafce-178">避免一个失败的环回连接到不存在的端口 [GH 3286] 的第二个延迟</span><span class="sxs-lookup"><span data-stu-id="bafce-178">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="bafce-179">添加 /proc/sys/fs/file-max 存根 （stub） 文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="bafce-179">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="bafce-180">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-180">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="bafce-181">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="bafce-181">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="bafce-182">通过管道传递无意中清除边缘触发 epoll 事件 [GH 3276] 的文件系统</span><span class="sxs-lookup"><span data-stu-id="bafce-182">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="bafce-183">Win32 可执行文件启动通过 NTFS 符号链接不遵循符号链接名称 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="bafce-183">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="bafce-184">改进了僵停的支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="bafce-184">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="bafce-185">添加用于控制 Windows 互操作行为 [GH 1493] wsl.conf 条目</span><span class="sxs-lookup"><span data-stu-id="bafce-185">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="bafce-186">修复 getsockname 不总是返回 UNIX 套接字系列类型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="bafce-186">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="bafce-187">添加对 TIOCSTI [GH 1863] 的支持</span><span class="sxs-lookup"><span data-stu-id="bafce-187">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="bafce-188">非阻塞套接字连接的过程中应返回 EAGAIN 的写入尝试 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="bafce-188">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="bafce-189">在已装载的 Vhd [GH 3246，3291] 上支持互操作</span><span class="sxs-lookup"><span data-stu-id="bafce-189">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="bafce-190">修复权限检查在根文件夹 [GH 3304] 上的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-190">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="bafce-191">TTY 键盘 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-191">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="bafce-192">Windows UI 应用程序应执行，即使在后台启动。</span><span class="sxs-lookup"><span data-stu-id="bafce-192">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="bafce-193">添加 wsl-u 或--用户选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="bafce-193">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="bafce-194">启用快速启动时，解决 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="bafce-194">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="bafce-195">Unix 套接字需要保留已断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="bafce-195">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="bafce-196">非阻塞 Unix 套接字失败，而无限期地 EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="bafce-196">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="bafce-197">用例 = off 是新的默认 drvfs 装载类型 [GH 2937，3212，3328]</span><span class="sxs-lookup"><span data-stu-id="bafce-197">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="bafce-198">请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)有关详细信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-198">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="bafce-199">添加 wslconfig/终止停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="bafce-199">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="bafce-200">修复 WSL shell 上下文菜单项未正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-200">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="bafce-201">公开每个目录区分大小写为扩展属性</span><span class="sxs-lookup"><span data-stu-id="bafce-201">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="bafce-202">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="bafce-202">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="bafce-203">解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="bafce-203">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="bafce-204">DrvFs： 只能恢复原义私有范围相对应的字符为转义字符。</span><span class="sxs-lookup"><span data-stu-id="bafce-204">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="bafce-205">在 ELF 分析器解释器长度验证 [GH 3154] 修复关闭--一个错误</span><span class="sxs-lookup"><span data-stu-id="bafce-205">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="bafce-206">在过去的时间 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="bafce-206">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="bafce-207">确保新的父目录中这种情况下列出创建重新分析点。</span><span class="sxs-lookup"><span data-stu-id="bafce-207">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="bafce-208">以原子方式在 DrvFs 创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="bafce-208">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="bafce-209">修复了其他问题，多线程的操作可能返回 ENOENT，即使该文件存在。</span><span class="sxs-lookup"><span data-stu-id="bafce-209">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="bafce-210">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="bafce-210">[GH 2712]</span></span>
* <span data-ttu-id="bafce-211">固定的 WSL 启用 UMCI 后启动失败。</span><span class="sxs-lookup"><span data-stu-id="bafce-211">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="bafce-212">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="bafce-212">[GH 3020]</span></span>
* <span data-ttu-id="bafce-213">添加用于启动 WSL [GH 437，603、 1836年] 的资源管理器上下文菜单。</span><span class="sxs-lookup"><span data-stu-id="bafce-213">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="bafce-214">若要使用，请按住 shift 并在资源管理器窗口中右键单击。</span><span class="sxs-lookup"><span data-stu-id="bafce-214">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="bafce-215">修复 Unix 套接字非阻塞行为 [GH 2822，3100]</span><span class="sxs-lookup"><span data-stu-id="bafce-215">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="bafce-216">修复 GH 2026 中报告挂起 NETLINK 命令。</span><span class="sxs-lookup"><span data-stu-id="bafce-216">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="bafce-217">添加对装入传播标志 [GH 2911] 的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-217">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="bafce-218">截断不导致 inotify 事件 [GH 2978] 修复问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-218">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="bafce-219">添加了--exec wsl.exe 调用单一的二进制文件而无需 shell 的选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-219">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="bafce-220">添加了--wsl.exe 以选择特定的发行版的分发选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-220">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="bafce-221">对 dmesg 的有限的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-221">Limited support for dmesg.</span></span> <span data-ttu-id="bafce-222">现在，应用程序可以将记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="bafce-222">Applications can now log to dmesg.</span></span> <span data-ttu-id="bafce-223">WSL 驱动程序记录到 dmesg 有限的信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-223">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="bafce-224">在将来，这可以扩展来执行其他来自驱动程序的信息/诊断。</span><span class="sxs-lookup"><span data-stu-id="bafce-224">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="bafce-225">注意： 当前支持通过 dmesg`/dev/kmsg`设备接口。</span><span class="sxs-lookup"><span data-stu-id="bafce-225">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="bafce-226">`syslog` 尚不支持 syscall 接口。</span><span class="sxs-lookup"><span data-stu-id="bafce-226">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="bafce-227">和，因此，某些`dmesg`命令行选项，例如`-S`，`-C`不起作用。</span><span class="sxs-lookup"><span data-stu-id="bafce-227">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="bafce-228">更改默认 gid 和模式的串行设备以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="bafce-228">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="bafce-229">DrvFs 现在支持扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="bafce-229">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="bafce-230">注意：DrvFs 上的扩展属性名称具有一些限制。</span><span class="sxs-lookup"><span data-stu-id="bafce-230">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="bafce-231">某些字符 (如 /、: 和\*) 不允许，并且扩展属性名称不区分大小写上 DrvFs</span><span class="sxs-lookup"><span data-stu-id="bafce-231">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="bafce-232">生成 18252 （提前跳过）</span><span class="sxs-lookup"><span data-stu-id="bafce-232">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="bafce-233">有关常规 Windows 上生成 18252 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-233">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-234">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-234">WSL</span></span>
* <span data-ttu-id="bafce-235">移动 init 和 bsdtar 二进制文件，带 lxssmanager dll 和到单独的工具文件夹</span><span class="sxs-lookup"><span data-stu-id="bafce-235">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="bafce-236">修复周围使用 CLONE_FILES 时关闭文件描述符的争用</span><span class="sxs-lookup"><span data-stu-id="bafce-236">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="bafce-237">转换 DrvFs 路径时处理 /proc/pid/mountinfo 中的可选字段</span><span class="sxs-lookup"><span data-stu-id="bafce-237">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="bafce-238">允许 DrvFs mknod 也不会对 S_IFREG 的元数据支持</span><span class="sxs-lookup"><span data-stu-id="bafce-238">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="bafce-239">DrvFs 上创建 Readonly 文件应具有设置 [GH 3411] 的 readonly 属性</span><span class="sxs-lookup"><span data-stu-id="bafce-239">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="bafce-240">添加 /sbin/mount.drvfs 帮助器来处理 DrvFs 装载</span><span class="sxs-lookup"><span data-stu-id="bafce-240">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="bafce-241">使用中 DrvFs POSIX 重命名。</span><span class="sxs-lookup"><span data-stu-id="bafce-241">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="bafce-242">允许对卷不包括卷 GUID 路径翻译。</span><span class="sxs-lookup"><span data-stu-id="bafce-242">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="bafce-243">生成 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="bafce-243">Build 17738 (Fast)</span></span>
<span data-ttu-id="bafce-244">有关常规 Windows 上生成 17738 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-244">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-245">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-245">WSL</span></span>
* <span data-ttu-id="bafce-246">Setpriority syscall 权限检查太严格的更改相同的线程优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="bafce-246">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="bafce-247">确保公平的中断时间使用启动时若要避免返回负数值的 clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="bafce-247">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="bafce-248">在 WSL binfmt 解释器 [GH 3424] 中的句柄符号链接</span><span class="sxs-lookup"><span data-stu-id="bafce-248">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="bafce-249">更好地处理 threadgroup 领导文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="bafce-249">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="bafce-250">生成 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="bafce-250">Build 17728 (Fast)</span></span>
<span data-ttu-id="bafce-251">有关常规 Windows 上生成 17728 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-251">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-252">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-252">WSL</span></span>
* <span data-ttu-id="bafce-253">切换 WSL 使用而不是 KeQueryPerformanceCounter KeQueryInterruptTimePrecise 以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="bafce-253">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="bafce-254">Ptrace 连接可能会返回的值不正确导致从系统调用 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="bafce-254">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="bafce-255">修复 AF_UNIX 的大量相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="bafce-255">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="bafce-256">解决问题可能导致 WSL 互操作，如果当前工作目录为小于 5 个字符长 [GH 3379] 失败</span><span class="sxs-lookup"><span data-stu-id="bafce-256">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="bafce-257">生成 18204 （提前跳过）</span><span class="sxs-lookup"><span data-stu-id="bafce-257">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="bafce-258">有关常规 Windows 上生成 18204 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-258">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-259">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-259">WSL</span></span>
* <span data-ttu-id="bafce-260">通过管道将文件系统 inadvertenly 清除边缘触发 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="bafce-260">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="bafce-261">Win32 可执行文件启动通过 NTFS 符号链接不遵循符号链接名称 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="bafce-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="bafce-262">生成 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="bafce-262">Build 17723 (Fast)</span></span>
<span data-ttu-id="bafce-263">有关常规 Windows 上生成 17723 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-263">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-264">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-264">WSL</span></span>
* <span data-ttu-id="bafce-265">避免一个失败的环回连接到不存在的端口 [GH 3286] 的第二个延迟</span><span class="sxs-lookup"><span data-stu-id="bafce-265">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="bafce-266">添加 /proc/sys/fs/file-max 存根 （stub） 文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="bafce-266">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="bafce-267">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-267">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="bafce-268">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="bafce-268">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="bafce-269">通过管道将文件系统 inadvertenly 清除边缘触发 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="bafce-269">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="bafce-270">Win32 可执行文件启动通过 NTFS 符号链接不遵循符号链接名称 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="bafce-270">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="bafce-271">生成 17713</span><span class="sxs-lookup"><span data-stu-id="bafce-271">Build 17713</span></span>
<span data-ttu-id="bafce-272">有关常规 Windows 上生成 17713 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-272">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-273">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-273">WSL</span></span>
* <span data-ttu-id="bafce-274">改进了僵停的支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="bafce-274">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="bafce-275">添加用于控制 Windows 互操作行为 [GH 1493] wsl.conf 条目</span><span class="sxs-lookup"><span data-stu-id="bafce-275">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="bafce-276">修复 getsockname 不总是返回 UNIX 套接字系列类型 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="bafce-276">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="bafce-277">添加对 TIOCSTI [GH 1863] 的支持</span><span class="sxs-lookup"><span data-stu-id="bafce-277">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="bafce-278">非阻塞套接字连接的过程中应返回 EAGAIN 的写入尝试 [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="bafce-278">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="bafce-279">在已装载的 Vhd [GH 3246，3291] 上支持互操作</span><span class="sxs-lookup"><span data-stu-id="bafce-279">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="bafce-280">修复权限检查在根文件夹 [GH 3304] 上的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-280">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="bafce-281">TTY 键盘 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-281">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="bafce-282">Windows UI 应用程序应执行，即使在后台启动。</span><span class="sxs-lookup"><span data-stu-id="bafce-282">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="bafce-283">生成 17704</span><span class="sxs-lookup"><span data-stu-id="bafce-283">Build 17704</span></span>
<span data-ttu-id="bafce-284">有关常规 Windows 上生成 17704 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-284">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-285">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-285">WSL</span></span>
* <span data-ttu-id="bafce-286">添加 wsl-u 或--用户选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="bafce-286">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="bafce-287">启用快速启动时，解决 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="bafce-287">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="bafce-288">Unix 套接字需要保留已断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="bafce-288">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="bafce-289">非阻塞 Unix 套接字失败，而无限期地 EAGAIN [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="bafce-289">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="bafce-290">用例 = off 是新的默认 drvfs 装载类型 [GH 2937，3212，3328]</span><span class="sxs-lookup"><span data-stu-id="bafce-290">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="bafce-291">请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)有关详细信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-291">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="bafce-292">添加 wslconfig/终止停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="bafce-292">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="bafce-293">版本 17692</span><span class="sxs-lookup"><span data-stu-id="bafce-293">Build 17692</span></span>
<span data-ttu-id="bafce-294">有关常规 Windows 上生成 17692 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="bafce-294">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-295">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-295">WSL</span></span>
* <span data-ttu-id="bafce-296">修复 WSL shell 上下文菜单项未正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-296">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="bafce-297">公开每个目录区分大小写为扩展属性</span><span class="sxs-lookup"><span data-stu-id="bafce-297">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="bafce-298">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="bafce-298">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="bafce-299">解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="bafce-299">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="bafce-300">DrvFs： 只能恢复原义私有范围相对应的字符为转义字符。</span><span class="sxs-lookup"><span data-stu-id="bafce-300">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="bafce-301">版本 17686</span><span class="sxs-lookup"><span data-stu-id="bafce-301">Build 17686</span></span>
<span data-ttu-id="bafce-302">有关常规 Windows 上生成 17686 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="bafce-302">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-303">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-303">WSL</span></span>
* <span data-ttu-id="bafce-304">在 ELF 分析器解释器长度验证 [GH 3154] 修复关闭--一个错误</span><span class="sxs-lookup"><span data-stu-id="bafce-304">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="bafce-305">在过去的时间 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="bafce-305">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="bafce-306">确保新的父目录中这种情况下列出创建重新分析点。</span><span class="sxs-lookup"><span data-stu-id="bafce-306">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="bafce-307">以原子方式在 DrvFs 创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="bafce-307">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="bafce-308">生成 17677</span><span class="sxs-lookup"><span data-stu-id="bafce-308">Build 17677</span></span>
<span data-ttu-id="bafce-309">有关常规 Windows 上生成 17677 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-309">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-310">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-310">WSL</span></span>
* <span data-ttu-id="bafce-311">修复了其他问题，多线程的操作可能返回 ENOENT，即使该文件存在。</span><span class="sxs-lookup"><span data-stu-id="bafce-311">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="bafce-312">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="bafce-312">[GH 2712]</span></span>
* <span data-ttu-id="bafce-313">固定的 WSL 启用 UMCI 后启动失败。</span><span class="sxs-lookup"><span data-stu-id="bafce-313">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="bafce-314">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="bafce-314">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="bafce-315">生成 17666</span><span class="sxs-lookup"><span data-stu-id="bafce-315">Build 17666</span></span>
<span data-ttu-id="bafce-316">有关常规 Windows 上生成 17666 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-316">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-317">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-317">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="bafce-318">警告：出现了问题导致无法 WSL 一些 AMD 芯片集 [GH 3134] 上运行。</span><span class="sxs-lookup"><span data-stu-id="bafce-318">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="bafce-319">解决方法是准备就绪，并可使发送给预览体验内部版本分支。</span><span class="sxs-lookup"><span data-stu-id="bafce-319">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="bafce-320">添加用于启动 WSL [GH 437，603、 1836年] 的资源管理器上下文菜单。</span><span class="sxs-lookup"><span data-stu-id="bafce-320">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="bafce-321">若要使用按住 shift 键并右键单击资源管理器窗口中。</span><span class="sxs-lookup"><span data-stu-id="bafce-321">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="bafce-322">修复 unix 套接字非阻塞行为 [GH 2822，3100]</span><span class="sxs-lookup"><span data-stu-id="bafce-322">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="bafce-323">修复 GH 2026 中报告挂起 NETLINK 命令。</span><span class="sxs-lookup"><span data-stu-id="bafce-323">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="bafce-324">添加对装入传播标志 [GH 2911] 的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-324">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="bafce-325">截断不导致 inotify 事件 [GH 2978] 修复问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-325">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="bafce-326">添加了--exec wsl.exe 调用单一的二进制文件而无需 shell 的选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-326">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="bafce-327">添加了--wsl.exe 以选择特定的发行版的分发选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-327">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="bafce-328">生成 17655 （提前跳过）</span><span class="sxs-lookup"><span data-stu-id="bafce-328">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="bafce-329">有关常规 Windows 上生成 17655 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-329">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-330">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-330">WSL</span></span>
* <span data-ttu-id="bafce-331">对 dmesg 的有限的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-331">Limited support for dmesg.</span></span> <span data-ttu-id="bafce-332">现在，应用程序可以将记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="bafce-332">Applications can now log to dmesg.</span></span> <span data-ttu-id="bafce-333">WSL 驱动程序记录到 dmesg 有限的信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-333">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="bafce-334">在将来，这可以扩展来执行其他来自驱动程序的信息/诊断。</span><span class="sxs-lookup"><span data-stu-id="bafce-334">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="bafce-335">注意： 当前支持通过 dmesg`/dev/kmsg`设备接口。</span><span class="sxs-lookup"><span data-stu-id="bafce-335">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="bafce-336">`syslog` 尚不支持 sycall 接口。</span><span class="sxs-lookup"><span data-stu-id="bafce-336">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="bafce-337">和，因此，某些`dmesg`命令行选项，例如`-S`，`-C`不起作用。</span><span class="sxs-lookup"><span data-stu-id="bafce-337">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="bafce-338">修复了问题，多线程的操作可能返回 ENOENT，即使该文件存在。</span><span class="sxs-lookup"><span data-stu-id="bafce-338">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="bafce-339">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="bafce-339">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="bafce-340">生成 17639 （提前跳过）</span><span class="sxs-lookup"><span data-stu-id="bafce-340">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="bafce-341">有关常规 Windows 上生成 17639 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-341">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-342">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-342">WSL</span></span>
* <span data-ttu-id="bafce-343">更改默认 gid 和模式的串行设备以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="bafce-343">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="bafce-344">DrvFs 现在支持扩展的属性。</span><span class="sxs-lookup"><span data-stu-id="bafce-344">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="bafce-345">注意：DrvFs 上的扩展属性名称具有一些限制。</span><span class="sxs-lookup"><span data-stu-id="bafce-345">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="bafce-346">具体而言，某些字符 (如 /、: 和\*) 不允许，并且扩展属性名称不区分大小写上 DrvFs</span><span class="sxs-lookup"><span data-stu-id="bafce-346">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="bafce-347">生成 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="bafce-347">Build 17133 (Fast)</span></span>
<span data-ttu-id="bafce-348">有关常规 Windows 上生成 17133 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-348">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-349">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-349">WSL</span></span>
* <span data-ttu-id="bafce-350">在 WSL 中挂起的修复。</span><span class="sxs-lookup"><span data-stu-id="bafce-350">Fix for hang in WSL.</span></span> <span data-ttu-id="bafce-351">[GH 3039，3034]</span><span class="sxs-lookup"><span data-stu-id="bafce-351">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="bafce-352">生成 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="bafce-352">Build 17128 (Fast)</span></span>
<span data-ttu-id="bafce-353">有关常规 Windows 上生成 17128 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-353">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-354">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-354">WSL</span></span>
* <span data-ttu-id="bafce-355">无</span><span class="sxs-lookup"><span data-stu-id="bafce-355">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="bafce-356">生成 17627 （提前跳过）</span><span class="sxs-lookup"><span data-stu-id="bafce-356">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="bafce-357">有关常规 Windows 上生成 17627 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-357">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-358">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-358">WSL</span></span>
* <span data-ttu-id="bafce-359">添加对 futex pi 注意操作的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-359">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="bafce-360">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="bafce-360">[GH 1006]</span></span>
    * <span data-ttu-id="bafce-361">请注意，优先级目前不受支持的 WSL 功能以便存在一些限制，但应解除对标准使用情况。</span><span class="sxs-lookup"><span data-stu-id="bafce-361">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="bafce-362">WSL 进程的 Windows 防火墙支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-362">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="bafce-363">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="bafce-363">[GH 1852]</span></span>
    * <span data-ttu-id="bafce-364">例如，若要允许 WSL python 处理任何端口上侦听，请使用提升的 Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="bafce-364">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="bafce-365">有关如何添加防火墙规则的其他详细信息，请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="bafce-365">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="bafce-366">使用 wsl.exe 时遵从用户的默认外壳。</span><span class="sxs-lookup"><span data-stu-id="bafce-366">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="bafce-367">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="bafce-367">[GH 2372]</span></span>
* <span data-ttu-id="bafce-368">报告为以太网的所有网络接口。</span><span class="sxs-lookup"><span data-stu-id="bafce-368">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="bafce-369">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="bafce-369">[GH 2996]</span></span>
* <span data-ttu-id="bafce-370">更好地处理已损坏的 /etc/passwd 文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-370">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="bafce-371">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="bafce-371">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="bafce-372">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-372">Console</span></span>
* <span data-ttu-id="bafce-373">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-373">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-374">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-374">LTP Results:</span></span>
<span data-ttu-id="bafce-375">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-375">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="bafce-376">生成 17618 （提前跳过）</span><span class="sxs-lookup"><span data-stu-id="bafce-376">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="bafce-377">有关常规 Windows 上生成 17618 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-377">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-378">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-378">WSL</span></span>
* <span data-ttu-id="bafce-379">引入 pseudoconsole NT 互操作的功能 [GH 988，1366，1433年、 1542年、 2370年、 2406年]。</span><span class="sxs-lookup"><span data-stu-id="bafce-379">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="bafce-380">已弃用旧安装机制 (lxrun.exe)。</span><span class="sxs-lookup"><span data-stu-id="bafce-380">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="bafce-381">安装发行版的受支持的机制是通过 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="bafce-381">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="bafce-382">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-382">Console</span></span>
* <span data-ttu-id="bafce-383">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-383">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-384">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-384">LTP Results:</span></span>
<span data-ttu-id="bafce-385">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-385">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="bafce-386">版本 17110</span><span class="sxs-lookup"><span data-stu-id="bafce-386">Build 17110</span></span>
<span data-ttu-id="bafce-387">有关常规 Windows 上生成 17110 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-387">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-388">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-388">WSL</span></span>
* <span data-ttu-id="bafce-389">允许 /init 从 Windows [GH 2928] 终止。</span><span class="sxs-lookup"><span data-stu-id="bafce-389">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="bafce-390">DrvFs 现在默认情况下使用每个目录的区分大小写 (等效于"用例为 dir"装载选项)。</span><span class="sxs-lookup"><span data-stu-id="bafce-390">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="bafce-391">使用"用例 = 强制"（旧行为） 需要设置注册表项。</span><span class="sxs-lookup"><span data-stu-id="bafce-391">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="bafce-392">运行以下命令以启用"用例 = 强制"如果需要使用它： reg 添加 HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span><span class="sxs-lookup"><span data-stu-id="bafce-392">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="bafce-393">如果必须使用 WSL 较旧版本的 Windows 需要区分大小写的中创建的现有目录，请使用 fsutil.exe 以便将它们标记为区分大小写： fsutil.exe 文件 setcasesensitiveinfo<path>启用</span><span class="sxs-lookup"><span data-stu-id="bafce-393">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="bafce-394">Uname syscall 从返回的字符串以 NULL 结尾。</span><span class="sxs-lookup"><span data-stu-id="bafce-394">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="bafce-395">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-395">Console</span></span>
* <span data-ttu-id="bafce-396">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-396">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-397">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-397">LTP Results:</span></span>
<span data-ttu-id="bafce-398">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-398">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="bafce-399">生成 17107</span><span class="sxs-lookup"><span data-stu-id="bafce-399">Build 17107</span></span>
<span data-ttu-id="bafce-400">有关常规 Windows 上生成 17107 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-400">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-401">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-401">WSL</span></span>
* <span data-ttu-id="bafce-402">主 pty 终结点 [GH 2552] 上支持 TCSETSF 和 TCSETSW。</span><span class="sxs-lookup"><span data-stu-id="bafce-402">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="bafce-403">启动同时进行互操作的进程可能会导致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="bafce-403">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="bafce-404">修复 PTRACE_ATTACH /proc/pid/status 中显示正确的跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="bafce-404">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="bafce-405">修复争用生存期较短的进程，克隆 CLEARTID 和 SETTID 标志无法退出而不清除 TID 地址。</span><span class="sxs-lookup"><span data-stu-id="bafce-405">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="bafce-406">从预 17093 生成移动时升级 Linux 文件系统目录时，将显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="bafce-406">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="bafce-407">17093 文件系统更改的更多详细信息，请参阅发行说明[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)。</span><span class="sxs-lookup"><span data-stu-id="bafce-407">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="bafce-408">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-408">Console</span></span>
* <span data-ttu-id="bafce-409">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-409">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-410">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-410">LTP Results:</span></span>
<span data-ttu-id="bafce-411">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-411">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="bafce-412">生成 17101</span><span class="sxs-lookup"><span data-stu-id="bafce-412">Build 17101</span></span>
<span data-ttu-id="bafce-413">有关常规 Windows 上生成 17101 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-413">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-414">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-414">WSL</span></span>
* <span data-ttu-id="bafce-415">对 signalfd 的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-415">Support for signalfd.</span></span> <span data-ttu-id="bafce-416">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="bafce-416">[GH 129]</span></span>
* <span data-ttu-id="bafce-417">支持文件名称包含非法 NTFS 字符编码为专用的 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="bafce-417">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="bafce-418">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="bafce-418">[GH 1514]</span></span>
* <span data-ttu-id="bafce-419">不支持写时，自动装入将回退到只读的。</span><span class="sxs-lookup"><span data-stu-id="bafce-419">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="bafce-420">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="bafce-420">[GH 2603]</span></span>
* <span data-ttu-id="bafce-421">允许粘贴 Unicode 代理项对 （如表情符号字符为单位）。</span><span class="sxs-lookup"><span data-stu-id="bafce-421">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="bafce-422">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="bafce-422">[GH 2765]</span></span>
* <span data-ttu-id="bafce-423">/Proc 和 /sys 中的伪文件应返回读取和写入就绪 select、 轮询、 epoll，et 都 [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="bafce-423">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="bafce-424">修复可能导致服务注册表被篡改或损坏时进入无限循环的问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-424">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="bafce-425">修复 netlink 消息要替换的 iproute2 更新 (上游 4.14) 版本。</span><span class="sxs-lookup"><span data-stu-id="bafce-425">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="bafce-426">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-426">Console</span></span>
* <span data-ttu-id="bafce-427">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-427">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-428">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-428">LTP Results:</span></span>
<span data-ttu-id="bafce-429">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-429">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="bafce-430">生成 17093</span><span class="sxs-lookup"><span data-stu-id="bafce-430">Build 17093</span></span>
<span data-ttu-id="bafce-431">有关常规 Windows 上生成 17093 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-431">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="bafce-432">重要提示：</span><span class="sxs-lookup"><span data-stu-id="bafce-432">Important:</span></span>
<span data-ttu-id="bafce-433">时从 WSL 开始第一次后升级到此版本，它需要执行一些升级 Linux 文件系统目录的工作。</span><span class="sxs-lookup"><span data-stu-id="bafce-433">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="bafce-434">这可能需要几分钟时间，因此 WSL 可能看起来启动慢。</span><span class="sxs-lookup"><span data-stu-id="bafce-434">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="bafce-435">安装从应用商店的每个分布区后，仅应发生这种情况。</span><span class="sxs-lookup"><span data-stu-id="bafce-435">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="bafce-436">改进了在 DrvFs 区分大小写支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-436">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="bafce-437">DrvFs 现在支持每个目录的区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-437">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="bafce-438">这是新标志可设置目录以指示在这些目录中的所有操作应被都视为区分大小写，这样即使 Windows 应用程序就可正确打开仅大小写不同的文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-438">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="bafce-439">DrvFs 具有新的装入选项控制在每个目录的基础上区分大小写</span><span class="sxs-lookup"><span data-stu-id="bafce-439">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="bafce-440">用例 = 强制： 所有目录将被都视为区分大小写 （除外驱动器根目录中）。</span><span class="sxs-lookup"><span data-stu-id="bafce-440">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="bafce-441">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-441">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="bafce-442">这是除标记区分大小写的新目录的旧行为。</span><span class="sxs-lookup"><span data-stu-id="bafce-442">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="bafce-443">用例为 dir： 仅使用每个目录的区分大小写标志的目录将被视为区分大小写;其他目录是不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-443">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="bafce-444">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-444">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="bafce-445">用例 = 关闭： 仅使用每个目录的区分大小写标志的目录将被视为区分大小写;其他目录是不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-445">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="bafce-446">使用 WSL 创建的新目录将标记为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-446">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="bafce-447">注意： 在以前版本中创建 WSL 目录没有此标志设置，因此将不被视为区分大小写如果使用"用例为 dir"选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-447">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="bafce-448">在现有目录上设置此标志的方法即将推出。</span><span class="sxs-lookup"><span data-stu-id="bafce-448">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="bafce-449">装载与这些选项的示例 （对于现有的驱动器，您必须首先卸载之前可以使用不同选项装载）： sudo mount-t drvfs c: mnt/c o 用例为 dir</span><span class="sxs-lookup"><span data-stu-id="bafce-449">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="bafce-450">现在，本例 = 强制仍是默认选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-450">For now, case=force is still the default option.</span></span> <span data-ttu-id="bafce-451">这将更改为用例在将来为 dir。</span><span class="sxs-lookup"><span data-stu-id="bafce-451">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="bafce-452">你现在可以使用正斜杠 Windows 路径中时装载 DrvFs，例如： sudo 装载-t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="bafce-452">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="bafce-453">WSL 现将在实例启动 [GH 2636] 处理 /etc/fstab 文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-453">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="bafce-454">这是在自动装载 DrvFs 驱动器; 之前任何已由 fstab 已装载的驱动器，将不重新装入自动，从而允许您更改特定驱动器的装入点。</span><span class="sxs-lookup"><span data-stu-id="bafce-454">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="bafce-455">此行为可以关闭使用 wsl.conf。</span><span class="sxs-lookup"><span data-stu-id="bafce-455">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="bafce-456">/Proc 中的装入、 mountinfo 和 mountstats 文件会正确地转义特殊字符，如反斜杠和空格 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="bafce-456">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="bafce-457">特殊文件使用创建 DrvFs 如 WSL 符号链接，或 fifos 和套接字启用元数据后，现在可以复制和从 Windows 移动。</span><span class="sxs-lookup"><span data-stu-id="bafce-457">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="bafce-458">WSL 是更多可配置为 wsl.conf</span><span class="sxs-lookup"><span data-stu-id="bafce-458">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="bafce-459">我们添加了一个方法，以便自动在每次启动子系统将应用的 WSL 中配置的特定功能。</span><span class="sxs-lookup"><span data-stu-id="bafce-459">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="bafce-460">这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="bafce-460">This includes automount options and network configuration.</span></span> <span data-ttu-id="bafce-461">在我们的博客文章中了解其详细信息： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="bafce-461">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="bafce-462">AF_UNIX 允许 Linux 进程在 WSL 和 Windows 本机进程之间的套接字连接</span><span class="sxs-lookup"><span data-stu-id="bafce-462">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="bafce-463">通过 Unix 套接字，现在相互 WSL 和 Windows 应用程序可以通信。</span><span class="sxs-lookup"><span data-stu-id="bafce-463">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="bafce-464">想象你想要在 Windows 中运行服务并使其可供 Windows 和 WSL 应用。</span><span class="sxs-lookup"><span data-stu-id="bafce-464">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="bafce-465">现在，这是可能使用 Unix 套接字。</span><span class="sxs-lookup"><span data-stu-id="bafce-465">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="bafce-466">读取在我们的博客文章 https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="bafce-466">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-467">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-467">WSL</span></span>
* <span data-ttu-id="bafce-468">支持使用 MAP_NORESERVE [GH 121，2784年] mmap()</span><span class="sxs-lookup"><span data-stu-id="bafce-468">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="bafce-469">支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121，2781年]</span><span class="sxs-lookup"><span data-stu-id="bafce-469">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="bafce-470">在克隆 [GH 121，2781年] 中的句柄非 SIGCHLD 终止信号</span><span class="sxs-lookup"><span data-stu-id="bafce-470">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="bafce-471">存根 （stub) /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="bafce-471">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="bafce-472">加载包含非零值的偏移量 [GH 1884] 的负载标头的 ELF 二进制文件时出错</span><span class="sxs-lookup"><span data-stu-id="bafce-472">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="bafce-473">加载图像时尾随页字节清零。</span><span class="sxs-lookup"><span data-stu-id="bafce-473">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="bafce-474">减少 execve 以无提示方式终止进程的情况下</span><span class="sxs-lookup"><span data-stu-id="bafce-474">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="bafce-475">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-475">Console</span></span>
* <span data-ttu-id="bafce-476">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-476">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-477">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-477">LTP Results:</span></span>
<span data-ttu-id="bafce-478">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-478">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="bafce-479">版本 17083</span><span class="sxs-lookup"><span data-stu-id="bafce-479">Build 17083</span></span>
<span data-ttu-id="bafce-480">有关常规 Windows 上生成 17083 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-480">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-481">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-481">WSL</span></span>
* <span data-ttu-id="bafce-482">固定的 epoll [GH 2798，2801，2857年] 与相关的错误检查</span><span class="sxs-lookup"><span data-stu-id="bafce-482">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="bafce-483">固定的挂起时关闭 ASLR [GH 1185，2870年]</span><span class="sxs-lookup"><span data-stu-id="bafce-483">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="bafce-484">确保 mmap 操作出现原子 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="bafce-484">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="bafce-485">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-485">Console</span></span>
* <span data-ttu-id="bafce-486">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-486">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-487">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-487">LTP Results:</span></span>
<span data-ttu-id="bafce-488">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-488">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="bafce-489">生成 17074</span><span class="sxs-lookup"><span data-stu-id="bafce-489">Build 17074</span></span>
<span data-ttu-id="bafce-490">有关常规 Windows 上生成 17074 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-490">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-491">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-491">WSL</span></span>
* <span data-ttu-id="bafce-492">固定的存储格式的 DrvFs 元数据 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="bafce-492">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="bafce-493">**重要说明：** 此生成不正确或根本不会显示之前创建的 DrvFs 元数据。</span><span class="sxs-lookup"><span data-stu-id="bafce-493">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="bafce-494">若要修复受影响的文件，请使用 chmod 和 chown 重新应用元数据。</span><span class="sxs-lookup"><span data-stu-id="bafce-494">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="bafce-495">多个信号和可重新启动 syscall 已修复的问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-495">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="bafce-496">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-496">Console</span></span>
* <span data-ttu-id="bafce-497">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-497">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-498">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-498">LTP Results:</span></span>
<span data-ttu-id="bafce-499">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-499">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="bafce-500">生成 17063</span><span class="sxs-lookup"><span data-stu-id="bafce-500">Build 17063</span></span>
<span data-ttu-id="bafce-501">有关常规 Windows 上生成 17063 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-501">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="bafce-502">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-502">WSL</span></span>
* <span data-ttu-id="bafce-503">DrvFs 支持 Linux 的其他元数据。</span><span class="sxs-lookup"><span data-stu-id="bafce-503">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="bafce-504">这允许设置所有者和使用 chmod/chown 和特殊文件，如 fifos、 unix 套接字和设备文件创建的文件模式。</span><span class="sxs-lookup"><span data-stu-id="bafce-504">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="bafce-505">这是默认情况下禁用现在由于它是仍处于实验阶段。</span><span class="sxs-lookup"><span data-stu-id="bafce-505">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="bafce-506">**注意：** 我们修复了 bug 中使用 DrvFs 的元数据格式。</span><span class="sxs-lookup"><span data-stu-id="bafce-506">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="bafce-507">而元数据适用于此生成的试验，将来的内部版本将不正确地读取元数据创建此生成的。</span><span class="sxs-lookup"><span data-stu-id="bafce-507">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="bafce-508">可能需要手动更新已修改的文件的所有者和使用自定义设备 ID 的设备将需要重新创建。</span><span class="sxs-lookup"><span data-stu-id="bafce-508">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="bafce-509">若要启用，装入 DrvFs 使用元数据选项 （若要在现有安装上启用它，您必须首先卸载该映像）：</span><span class="sxs-lookup"><span data-stu-id="bafce-509">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="bafce-510">Linux 权限为附加元数据添加到该文件;它们不会影响 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="bafce-510">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="bafce-511">请记住，编辑文件使用 Windows 编辑器可能删除的元数据。</span><span class="sxs-lookup"><span data-stu-id="bafce-511">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="bafce-512">在这种情况下，该文件将恢复为其默认权限。</span><span class="sxs-lookup"><span data-stu-id="bafce-512">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="bafce-513">添加的装载到不包含元数据的控制文件 DrvFs 的选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-513">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="bafce-514">uid： 用于所有文件的所有者的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="bafce-514">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="bafce-515">gid： 用于所有文件的所有者的组 ID。</span><span class="sxs-lookup"><span data-stu-id="bafce-515">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="bafce-516">umask： 若要排除的所有文件和目录的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="bafce-516">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="bafce-517">fmask： 权限以排除所有常规的文件的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="bafce-517">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="bafce-518">dmask： 权限以排除所有目录的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="bafce-518">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="bafce-519">例如：</span><span class="sxs-lookup"><span data-stu-id="bafce-519">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="bafce-520">将与指定的文件不包含元数据的默认权限的元数据选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-520">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="bafce-521">引入了一个新的环境变量， `WSLENV`，可以配置环境变量如何在 WSL 和 Win32 之间流动。</span><span class="sxs-lookup"><span data-stu-id="bafce-521">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="bafce-522">例如：</span><span class="sxs-lookup"><span data-stu-id="bafce-522">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="bafce-523">`WSLENV` 是可以包含来自 Win32 的 WSL 进程或从 WSL 的 Win32 进程启动时的环境变量的分号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-523">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="bafce-524">标志以指定如何对其进行转换后跟反斜杠结尾，每个变量可以作为后缀。</span><span class="sxs-lookup"><span data-stu-id="bafce-524">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="bafce-525">p:值是应翻译 WSL 路径和 Win32 路径之间的路径。</span><span class="sxs-lookup"><span data-stu-id="bafce-525">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="bafce-526">L:值为一系列路径。</span><span class="sxs-lookup"><span data-stu-id="bafce-526">l: The value is a list of paths.</span></span> <span data-ttu-id="bafce-527">在 WSL，它是一个冒号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-527">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="bafce-528">在 Win32 中，它是以分号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-528">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="bafce-529">U:更改在调用来自 Win32 的 WSL 时只应包含值</span><span class="sxs-lookup"><span data-stu-id="bafce-529">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="bafce-530">w:更改在调用 Win32 从 WSL 时只应包含值</span><span class="sxs-lookup"><span data-stu-id="bafce-530">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="bafce-531">可以设置`WSLENV`.bashrc 或你的用户自定义 Windows 环境中。</span><span class="sxs-lookup"><span data-stu-id="bafce-531">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="bafce-532">drvfs 装载正确保留 tar 文件，从时间戳 cp-p (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="bafce-532">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="bafce-533">drvfs 符号链接报告正确的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="bafce-533">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="bafce-534">读/写适用于非常大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="bafce-534">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="bafce-535">waitpid 适用于进程组 Id (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="bafce-535">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="bafce-536">显著的性能改进的 mmap 大型保留区域;改进了 ghc 性能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="bafce-536">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="bafce-537">READ_IMPLIES_EXEC; 的个性支持修复了最大值和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="bafce-537">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="bafce-538">mprotect 支持 PROT_GROWSDOWN;修复了 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="bafce-538">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="bafce-539">中的页错误修复过载模式;修复了 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="bafce-539">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="bafce-540">克隆支持更多的标志组合</span><span class="sxs-lookup"><span data-stu-id="bafce-540">clone supports more flags combinations</span></span>
* <span data-ttu-id="bafce-541">支持 epoll 文件 （之前执行任何操作） 的选择/epoll。</span><span class="sxs-lookup"><span data-stu-id="bafce-541">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="bafce-542">通知未实现 syscall ptrace。</span><span class="sxs-lookup"><span data-stu-id="bafce-542">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="bafce-543">忽略接口时，将不会生成 resolv.conf 名称服务器 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="bafce-543">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="bafce-544">枚举与没有物理地址的网络接口。</span><span class="sxs-lookup"><span data-stu-id="bafce-544">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="bafce-545">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="bafce-545">[GH 2685]</span></span>
* <span data-ttu-id="bafce-546">其他 bug 修复和改进。</span><span class="sxs-lookup"><span data-stu-id="bafce-546">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="bafce-547">供开发人员在 Windows 上的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="bafce-547">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="bafce-548">Windows 命令行工具链包含 bsdtar (tar) 和 curl 配合使用。</span><span class="sxs-lookup"><span data-stu-id="bafce-548">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="bafce-549">读取[此博客](https://aka.ms/tarcurlwindows)若要了解有关新增的两个新工具的详细信息并查看它们如何调整 Windows 上的开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="bafce-549">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="bafce-550">`AF_UNIX` 现已推出 Windows Insider SDK （17061 +）。</span><span class="sxs-lookup"><span data-stu-id="bafce-550">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="bafce-551">读取[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)若要详细了解`AF_UNIX`和 Windows 上的开发人员可以使用它。</span><span class="sxs-lookup"><span data-stu-id="bafce-551">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="bafce-552">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-552">Console</span></span>
* <span data-ttu-id="bafce-553">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-553">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-554">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-554">LTP Results:</span></span>
<span data-ttu-id="bafce-555">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-555">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="bafce-556">生成 17046</span><span class="sxs-lookup"><span data-stu-id="bafce-556">Build 17046</span></span>

<span data-ttu-id="bafce-557">有关常规 Windows 上生成 17046 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="bafce-557">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="bafce-558">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-558">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-559">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-559">WSL</span></span>
- <span data-ttu-id="bafce-560">允许进程运行时没有活动的终端。</span><span class="sxs-lookup"><span data-stu-id="bafce-560">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="bafce-561">[GH 709，1007，1511年、 2252年、 2391，et al。]</span><span class="sxs-lookup"><span data-stu-id="bafce-561">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="bafce-562">CLONE_VFORK 和 CLONE_VM 的更好的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-562">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="bafce-563">[GH 1878，2615年]</span><span class="sxs-lookup"><span data-stu-id="bafce-563">[GH 1878, 2615]</span></span>
- <span data-ttu-id="bafce-564">跳过网络操作的 WSL TDI 筛选器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-564">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="bafce-565">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="bafce-565">[GH 1554]</span></span>
- <span data-ttu-id="bafce-566">当满足某些条件时，DrvFs 创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="bafce-566">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="bafce-567">[GH 353，1475，2602年]</span><span class="sxs-lookup"><span data-stu-id="bafce-567">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="bafce-568">链接目标必须是相对路径，不能跨越任何装入点或符号链接，并且必须存在。</span><span class="sxs-lookup"><span data-stu-id="bafce-568">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="bafce-569">用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE （这通常要求您启动 wsl.exe 提升），除非打开开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="bafce-569">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="bafce-570">在所有其他情况下，DrvFs 仍会 WSL 符号链接。</span><span class="sxs-lookup"><span data-stu-id="bafce-570">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="bafce-571">允许同时运行提升和非提升 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="bafce-571">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="bafce-572">Support /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="bafce-572">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="bafce-573">添加 wslpath 为 WSL <>-Windows 路径转换。</span><span class="sxs-lookup"><span data-stu-id="bafce-573">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="bafce-574">[GH 522，1243，1834年、 2327，et al。]</span><span class="sxs-lookup"><span data-stu-id="bafce-574">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="bafce-575">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-575">Console</span></span>
- <span data-ttu-id="bafce-576">任何修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-576">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-577">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-577">LTP Results:</span></span>
<span data-ttu-id="bafce-578">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-578">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="bafce-579">生成 17040</span><span class="sxs-lookup"><span data-stu-id="bafce-579">Build 17040</span></span>

<span data-ttu-id="bafce-580">有关常规 Windows 上生成 17040 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="bafce-580">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-581">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-581">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-582">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-582">WSL</span></span>
- <span data-ttu-id="bafce-583">无 17035 以来的修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-583">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-584">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-584">Console</span></span>
- <span data-ttu-id="bafce-585">无 17035 以来的修补程序。</span><span class="sxs-lookup"><span data-stu-id="bafce-585">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-586">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-586">LTP Results:</span></span>
<span data-ttu-id="bafce-587">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-587">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="bafce-588">生成 17035</span><span class="sxs-lookup"><span data-stu-id="bafce-588">Build 17035</span></span>

<span data-ttu-id="bafce-589">有关常规 Windows 上生成 17035 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="bafce-589">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-590">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-590">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-591">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-591">WSL</span></span>
- <span data-ttu-id="bafce-592">访问 DrvFs 上的文件无法与 EINVAL 偶尔也会失败。</span><span class="sxs-lookup"><span data-stu-id="bafce-592">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="bafce-593">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="bafce-593">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-594">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-594">Console</span></span>
- <span data-ttu-id="bafce-595">插入/删除 VT 模式中的行时，某些颜色丢失。</span><span class="sxs-lookup"><span data-stu-id="bafce-595">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-596">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-596">LTP Results:</span></span>
<span data-ttu-id="bafce-597">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-597">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="bafce-598">内部版本 17025</span><span class="sxs-lookup"><span data-stu-id="bafce-598">Build 17025</span></span>

<span data-ttu-id="bafce-599">有关常规 Windows 内部版本 17025 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="bafce-599">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-600">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-600">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-601">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-601">WSL</span></span>
- <span data-ttu-id="bafce-602">启动新的前台进程组 [GH 1653，2510年] 中的初始进程。</span><span class="sxs-lookup"><span data-stu-id="bafce-602">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="bafce-603">SIGHUP 交付修补程序 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="bafce-603">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="bafce-604">如果未提供 [GH 2497]，生成默认虚拟桥的名称。</span><span class="sxs-lookup"><span data-stu-id="bafce-604">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="bafce-605">实现 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="bafce-605">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="bafce-606">修复了多互操作的 stdout/stderr 管道。</span><span class="sxs-lookup"><span data-stu-id="bafce-606">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="bafce-607">存根 syncfs 系统调用。</span><span class="sxs-lookup"><span data-stu-id="bafce-607">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-608">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-608">Console</span></span>
- <span data-ttu-id="bafce-609">修复输入的 VT 转换为第三方控制台 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="bafce-609">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-610">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-610">LTP Results:</span></span>
<span data-ttu-id="bafce-611">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-611">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="bafce-612">生成 17017</span><span class="sxs-lookup"><span data-stu-id="bafce-612">Build 17017</span></span>

<span data-ttu-id="bafce-613">有关常规 Windows 上生成 17017 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="bafce-613">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-614">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-614">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-615">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-615">WSL</span></span>
- <span data-ttu-id="bafce-616">忽略空 ELF 程序标头 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="bafce-616">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="bafce-617">允许 LxssManager 创建非交互式用户的 WSL 实例 (ssh 和计划任务支持) [GH 777，1602年]。</span><span class="sxs-lookup"><span data-stu-id="bafce-617">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="bafce-618">支持 WSL-> Win32-> WSL （"开始"） 方案 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="bafce-618">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="bafce-619">终止通过互操作 [GH 1614] 调用的控制台应用程序的有限的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-619">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="bafce-620">Devpts [GH 1948] 的支持装载选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-620">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="bafce-621">阻止子启动 [GH 2333] 的 Ptrace。</span><span class="sxs-lookup"><span data-stu-id="bafce-621">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="bafce-622">EPOLLET 缺少某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="bafce-622">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="bafce-623">为 PTRACE_GETSIGINFO 返回更多的数据。</span><span class="sxs-lookup"><span data-stu-id="bafce-623">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="bafce-624">使用 lseek Getdents 提供不正确的结果。</span><span class="sxs-lookup"><span data-stu-id="bafce-624">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="bafce-625">修复在已没有更多数据的管道上等待输入一些 Win32 互操作应用挂起。</span><span class="sxs-lookup"><span data-stu-id="bafce-625">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="bafce-626">O_ASYNC 支持 tty/pty 文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-626">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="bafce-627">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-627">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-628">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-628">Console</span></span>
- <span data-ttu-id="bafce-629">没有控制台相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-629">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-630">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-630">LTP Results:</span></span>
<span data-ttu-id="bafce-631">测试正在进行中。</span><span class="sxs-lookup"><span data-stu-id="bafce-631">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="bafce-632">秋季创意者更新</span><span class="sxs-lookup"><span data-stu-id="bafce-632">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="bafce-633">生成 16288</span><span class="sxs-lookup"><span data-stu-id="bafce-633">Build 16288</span></span>

<span data-ttu-id="bafce-634">有关常规 Windows 上生成 16288 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-634">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-635">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-635">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-636">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-636">WSL</span></span>
- <span data-ttu-id="bafce-637">正确初始化并报告 uid 和 gid，模式套接字文件描述符 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="bafce-637">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="bafce-638">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-638">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-639">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-639">Console</span></span>
- <span data-ttu-id="bafce-640">没有控制台相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-640">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-641">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-641">LTP Results:</span></span>
<span data-ttu-id="bafce-642">16273 以来未更改</span><span class="sxs-lookup"><span data-stu-id="bafce-642">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="bafce-643">生成 16278</span><span class="sxs-lookup"><span data-stu-id="bafce-643">Build 16278</span></span>

<span data-ttu-id="bafce-644">有关常规 Windows 上生成 162738 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-644">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-645">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-645">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-646">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-646">WSL</span></span>
- <span data-ttu-id="bafce-647">显式取消的备份文件的部分映射的视图映射时关闭 LX MM 状态 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="bafce-647">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="bafce-648">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-648">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-649">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-649">Console</span></span>
- <span data-ttu-id="bafce-650">没有控制台相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-650">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-651">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-651">LTP Results:</span></span>
<span data-ttu-id="bafce-652">16273 以来未更改</span><span class="sxs-lookup"><span data-stu-id="bafce-652">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="bafce-653">生成 16275</span><span class="sxs-lookup"><span data-stu-id="bafce-653">Build 16275</span></span>

<span data-ttu-id="bafce-654">有关常规 Windows 上生成 162735 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-654">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-655">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-655">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-656">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-656">WSL</span></span>
- <span data-ttu-id="bafce-657">没有 WSL 相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-657">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-658">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-658">Console</span></span>
- <span data-ttu-id="bafce-659">没有控制台相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-659">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-660">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-660">LTP Results:</span></span>
<span data-ttu-id="bafce-661">16273 以来未更改</span><span class="sxs-lookup"><span data-stu-id="bafce-661">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="bafce-662">生成 16273</span><span class="sxs-lookup"><span data-stu-id="bafce-662">Build 16273</span></span>

<span data-ttu-id="bafce-663">有关常规 Windows 上生成 16273 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-663">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-664">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-664">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-665">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-665">WSL</span></span>
- <span data-ttu-id="bafce-666">修复了 DrvFs 有时报告目录 [GH 2392] 的错误的文件类型</span><span class="sxs-lookup"><span data-stu-id="bafce-666">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="bafce-667">允许的 NETLINK_KOBJECT_UEVENT 套接字，若要取消阻止程序创建该使用 uevent [GH 1121，2293，2242年、 2295年、 2235，648、 637]</span><span class="sxs-lookup"><span data-stu-id="bafce-667">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="bafce-668">添加对非阻止连接的支持 [GH 903，1391，1584年、 1585年、 1829年、 2290年、 2314年]</span><span class="sxs-lookup"><span data-stu-id="bafce-668">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="bafce-669">实现 CLONE_FS 克隆系统调用标志 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="bafce-669">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="bafce-670">修复不处理选项卡或 NT 互操作 [GH 1625，2164年] 中正确的引号等事宜</span><span class="sxs-lookup"><span data-stu-id="bafce-670">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="bafce-671">解决拒绝访问错误时尝试重新启动 WSL 实例 [GH 651，2095年]</span><span class="sxs-lookup"><span data-stu-id="bafce-671">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="bafce-672">实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="bafce-672">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="bafce-673">修复各种 SysFs 文件 [GH 2214] 的权限</span><span class="sxs-lookup"><span data-stu-id="bafce-673">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="bafce-674">在安装程序 [GH 2290] 期间修复 Haskell 堆栈挂起</span><span class="sxs-lookup"><span data-stu-id="bafce-674">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="bafce-675">实现 binfmt_misc 'C' O 和 P 标志 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="bafce-675">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="bafce-676">添加 /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="bafce-676">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="bafce-677">添加对 ioprio_set 系统调用 [GH 498] 的部分支持</span><span class="sxs-lookup"><span data-stu-id="bafce-677">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="bafce-678">存根 SO_REUSEPORT 和添加支持 SO_PASSCRED netlink 套接字 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="bafce-678">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="bafce-679">从 RegisterDistribuiton 返回不同的错误代码，如果当前正在分发安装或卸载。</span><span class="sxs-lookup"><span data-stu-id="bafce-679">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="bafce-680">允许通过 wslconfig.exe 部分安装 WSL 分发的注销</span><span class="sxs-lookup"><span data-stu-id="bafce-680">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="bafce-681">修复从 udp::msg_peek python 套接字测试挂起</span><span class="sxs-lookup"><span data-stu-id="bafce-681">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="bafce-682">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-682">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-683">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-683">Console</span></span>
- <span data-ttu-id="bafce-684">没有控制台相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-684">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-685">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-685">LTP Results:</span></span>
<span data-ttu-id="bafce-686">测试总数：1904</span><span class="sxs-lookup"><span data-stu-id="bafce-686">Total Tests: 1904</span></span><br/>
<span data-ttu-id="bafce-687">总跳过测试：209</span><span class="sxs-lookup"><span data-stu-id="bafce-687">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="bafce-688">故障总数：229</span><span class="sxs-lookup"><span data-stu-id="bafce-688">Total Failures: 229</span></span><br/>
[<span data-ttu-id="bafce-689">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-689">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="bafce-690">版本 16257</span><span class="sxs-lookup"><span data-stu-id="bafce-690">Build 16257</span></span>

<span data-ttu-id="bafce-691">有关常规 Windows 上生成 16257 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-691">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-692">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-693">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-693">WSL</span></span>
- <span data-ttu-id="bafce-694">实现 prlimit64 系统调用</span><span class="sxs-lookup"><span data-stu-id="bafce-694">Implement prlimit64 system call</span></span>
- <span data-ttu-id="bafce-695">添加对 ulimit-n (setrlimit RLIMIT_NOFILE) 的支持 [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="bafce-695">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="bafce-696">存根 MSG_MORE 针对 TCP 套接字 [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="bafce-696">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="bafce-697">修复无效 AT_EXECFN 辅助向量行为 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="bafce-697">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="bafce-698">修复控制台/tty 的复制/粘贴行为并添加更好地处理 [GH 2204，2131年] 已满缓冲区</span><span class="sxs-lookup"><span data-stu-id="bafce-698">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="bafce-699">有关设置用户 ID 和组-组 ID 程序 [GH 2031] 的辅助向量中设置 AT_SECURE</span><span class="sxs-lookup"><span data-stu-id="bafce-699">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="bafce-700">仿真终端主终结点不处理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="bafce-700">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="bafce-701">修复 lseek 执行的操作以 rewind LxFs [GH 2310] 中的目录</span><span class="sxs-lookup"><span data-stu-id="bafce-701">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="bafce-702">/dev/ptmx 锁定的时间之后的高使用率 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="bafce-702">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="bafce-703">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-703">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-704">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-704">Console</span></span>
- <span data-ttu-id="bafce-705">修复水平行/下划线无处不在 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="bafce-705">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="bafce-706">修复处理订单更改使 NPM 难关闭 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="bafce-706">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="bafce-707">添加我们新的配色方案： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="bafce-707">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-708">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-708">LTP Results:</span></span>
<span data-ttu-id="bafce-709">16251 以来未更改</span><span class="sxs-lookup"><span data-stu-id="bafce-709">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-710">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-710">Syscall Support</span></span>
<span data-ttu-id="bafce-711">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-711">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-712">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-712">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="bafce-713">已知问题</span><span class="sxs-lookup"><span data-stu-id="bafce-713">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="bafce-714">GitHub 问题 2392年:Windows 无法识别的 WSL 文件夹...</span><span class="sxs-lookup"><span data-stu-id="bafce-714">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="bafce-715">在生成 16257，WSL 有问题，枚举通过 Windows 文件/文件夹时`/mnt/c/...`。</span><span class="sxs-lookup"><span data-stu-id="bafce-715">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="bafce-716">此问题已修复，并且应在释放预览体验成员版本官员在 2017 年 8 月 14 日开始的一周内。</span><span class="sxs-lookup"><span data-stu-id="bafce-716">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="bafce-717">生成 16251</span><span class="sxs-lookup"><span data-stu-id="bafce-717">Build 16251</span></span>

<span data-ttu-id="bafce-718">有关常规 Windows 上生成 16251 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-718">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-719">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-719">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-720">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-720">WSL</span></span>
- <span data-ttu-id="bafce-721">删除 beta 标记从 WSL 可选组件，请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)有关详细信息。</span><span class="sxs-lookup"><span data-stu-id="bafce-721">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="bafce-722">保存设置 uid 和 gid exec [GH 962，1415、 2072年] 上的设置用户 ID 和组-组 ID 的二进制文件的正确初始化</span><span class="sxs-lookup"><span data-stu-id="bafce-722">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="bafce-723">添加了的对 ptrace PTRACE_O_TRACEEXIT [GH 555]</span><span class="sxs-lookup"><span data-stu-id="bafce-723">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="bafce-724">添加了对 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 与 NT_FPREGSET [GH 555]</span><span class="sxs-lookup"><span data-stu-id="bafce-724">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="bafce-725">已修复的 ptrace 上停止忽略信号</span><span class="sxs-lookup"><span data-stu-id="bafce-725">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="bafce-726">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-727">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-727">Console</span></span>
- <span data-ttu-id="bafce-728">没有控制台相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-729">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-729">LTP Results:</span></span>
<span data-ttu-id="bafce-730">通过的测试数：768</span><span class="sxs-lookup"><span data-stu-id="bafce-730">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="bafce-731">未通过的测试数：244</span><span class="sxs-lookup"><span data-stu-id="bafce-731">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="bafce-732">已跳过的测试数：96</span><span class="sxs-lookup"><span data-stu-id="bafce-732">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="bafce-733">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-733">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="bafce-734">生成 16241</span><span class="sxs-lookup"><span data-stu-id="bafce-734">Build 16241</span></span>

<span data-ttu-id="bafce-735">有关常规 Windows 上生成 16241 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-735">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-736">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-736">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="bafce-737">WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-737">WSL</span></span>
- <span data-ttu-id="bafce-738">没有 WSL 相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-738">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="bafce-739">控制台</span><span class="sxs-lookup"><span data-stu-id="bafce-739">Console</span></span>
- <span data-ttu-id="bafce-740">修复错误的字符输出跨越行 dec，最初报告[此处](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="bafce-740">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="bafce-741">修复了显示在代码页 65001 (utf8) 没有输出文本</span><span class="sxs-lookup"><span data-stu-id="bafce-741">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="bafce-742">不会传输到所选内容更改调色板的其他部分的一种颜色的 RGB 值所做的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-742">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="bafce-743">这将使控制台属性表更易于使用。</span><span class="sxs-lookup"><span data-stu-id="bafce-743">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="bafce-744">Ctrl + S 似乎不正常工作</span><span class="sxs-lookup"><span data-stu-id="bafce-744">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="bafce-745">未加粗 /-维度完全不存在从 ANSI 转义码 [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="bafce-745">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="bafce-746">控制台不会正确地支持 Vim 颜色主题 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="bafce-746">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="bafce-747">不能粘贴特定字符 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="bafce-747">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="bafce-748">重排调整大小与当内容在编辑/命令行 [GH ConEmu 1123] 时调整大小的 bash 窗口奇怪交互</span><span class="sxs-lookup"><span data-stu-id="bafce-748">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="bafce-749">Ctrl-L 离开屏幕已更新 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="bafce-749">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="bafce-750">控制台呈现 bug 上 HDPI [GH 又回到了 1907] 显示 VT 时</span><span class="sxs-lookup"><span data-stu-id="bafce-750">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="bafce-751">Japansese 字符看起来很奇怪的 Unicode 字符 U + 30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="bafce-751">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="bafce-752">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-752">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="bafce-753">版本 16237</span><span class="sxs-lookup"><span data-stu-id="bafce-753">Build 16237</span></span>

<span data-ttu-id="bafce-754">有关常规 Windows 上生成 16237 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-754">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-755">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-755">Fixed</span></span>
- <span data-ttu-id="bafce-756">中的文件而无需 EAs lxfs （根、 根，0000） 使用默认属性</span><span class="sxs-lookup"><span data-stu-id="bafce-756">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="bafce-757">添加了的对使用扩展的属性的分发</span><span class="sxs-lookup"><span data-stu-id="bafce-757">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="bafce-758">修复 getdents 和 getdents64 返回项的填充</span><span class="sxs-lookup"><span data-stu-id="bafce-758">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="bafce-759">修复 shmctl SHM_STAT 系统调用 [GH 2068] 的权限检查</span><span class="sxs-lookup"><span data-stu-id="bafce-759">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="bafce-760">Tty [GH 2231] 的固定不正确的初始 epoll 状态</span><span class="sxs-lookup"><span data-stu-id="bafce-760">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="bafce-761">修复 DrvFs readdir 未返回所有条目 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="bafce-761">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="bafce-762">修复 LxFs readdir 文件时已取消链接 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="bafce-762">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="bafce-763">允许通过 procfs 重新打开取消链接的 drvfs 文件</span><span class="sxs-lookup"><span data-stu-id="bafce-763">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="bafce-764">添加全局注册表禁用 WSL 功能密钥替代 (互操作 / 驱动器装载)</span><span class="sxs-lookup"><span data-stu-id="bafce-764">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="bafce-765">适用于 DrvFs （和 LxFs） 解决"状态"中的不正确的块计数 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="bafce-765">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="bafce-766">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-766">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="bafce-767">生成 16232</span><span class="sxs-lookup"><span data-stu-id="bafce-767">Build 16232</span></span>

<span data-ttu-id="bafce-768">有关常规 Windows 上生成 16232 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-768">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-769">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-769">Fixed</span></span>
- <span data-ttu-id="bafce-770">没有 WSL 相关的此版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-770">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="bafce-771">生成 16226</span><span class="sxs-lookup"><span data-stu-id="bafce-771">Build 16226</span></span>

<span data-ttu-id="bafce-772">有关常规 Windows 上生成 16226 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-772">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-773">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-773">Fixed</span></span>
- <span data-ttu-id="bafce-774">xattr 相关 syscall 支持 （getxattr、 setxattr、 listxattr、 removexattr）。</span><span class="sxs-lookup"><span data-stu-id="bafce-774">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="bafce-775">security.capablity xattr 支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-775">security.capablity xattr support.</span></span>
- <span data-ttu-id="bafce-776">改进与特定的文件系统和筛选器，包括非 MS SMB 服务器的兼容性。</span><span class="sxs-lookup"><span data-stu-id="bafce-776">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="bafce-777">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="bafce-777">[GH #1952]</span></span>
- <span data-ttu-id="bafce-778">改进了对 OneDrive 的占位符、 GVFS 占位符和 Compact OS 支持压缩文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-778">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="bafce-779">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-779">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="bafce-780">生成 16215</span><span class="sxs-lookup"><span data-stu-id="bafce-780">Build 16215</span></span>

<span data-ttu-id="bafce-781">有关常规 Windows 上生成 16215 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-781">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-782">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-782">Fixed</span></span>
- <span data-ttu-id="bafce-783">WSL 不再要求开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="bafce-783">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="bafce-784">支持 drvfs 目录接合点。</span><span class="sxs-lookup"><span data-stu-id="bafce-784">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="bafce-785">处理卸载的 WSL 分发 appx 包。</span><span class="sxs-lookup"><span data-stu-id="bafce-785">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="bafce-786">更新 procfs 显示专用和共享的映射。</span><span class="sxs-lookup"><span data-stu-id="bafce-786">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="bafce-787">添加 wslconfig.exe 清理的部分安装或卸载分发版的功能。</span><span class="sxs-lookup"><span data-stu-id="bafce-787">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="bafce-788">针对 TCP 套接字 IP_MTU_DISCOVER 添加的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-788">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="bafce-789">[GH 1639，2115，2205年]</span><span class="sxs-lookup"><span data-stu-id="bafce-789">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="bafce-790">推断 AF_INADDR 的路由的协议家族。</span><span class="sxs-lookup"><span data-stu-id="bafce-790">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="bafce-791">串行设备改进 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="bafce-791">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="bafce-792">生成 16199</span><span class="sxs-lookup"><span data-stu-id="bafce-792">Build 16199</span></span>

<span data-ttu-id="bafce-793">有关常规 Windows 上生成 16199 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-793">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-794">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-794">Fixed</span></span>
- <span data-ttu-id="bafce-795">没有 WSL 相关的这些版本中的更改。</span><span class="sxs-lookup"><span data-stu-id="bafce-795">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="bafce-796">生成 16193</span><span class="sxs-lookup"><span data-stu-id="bafce-796">Build 16193</span></span>

<span data-ttu-id="bafce-797">有关常规 Windows 上生成 16193 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-797">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-798">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-798">Fixed</span></span>
- <span data-ttu-id="bafce-799">发送 SIGCONT 和终止 [GH 1973] threadgroup 之间的争用条件</span><span class="sxs-lookup"><span data-stu-id="bafce-799">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="bafce-800">更改报表而不是 FILE_DEVICE_CONSOLE [GH 1840] FILE_DEVICE_NAMED_PIPE tty 和 pty 设备</span><span class="sxs-lookup"><span data-stu-id="bafce-800">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="bafce-801">SSH IP_OPTIONS 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-801">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="bafce-802">移动 DrvFs 装载到 init 守护程序 [GH 1862，1968，1767年、 1933年]</span><span class="sxs-lookup"><span data-stu-id="bafce-802">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="bafce-803">添加了的对在 DrvFs 遵循 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="bafce-803">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="bafce-804">生成 16184</span><span class="sxs-lookup"><span data-stu-id="bafce-804">Build 16184</span></span>

<span data-ttu-id="bafce-805">有关常规 Windows 上生成 16184 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-805">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-806">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-806">Fixed</span></span>
- <span data-ttu-id="bafce-807">已删除的 apt 包维护任务 （lxrun.exe/更新）</span><span class="sxs-lookup"><span data-stu-id="bafce-807">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="bafce-808">固定的输出中未显示从 node.js [GH 1840] 中的 Windows 进程</span><span class="sxs-lookup"><span data-stu-id="bafce-808">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="bafce-809">放宽 lxcore [GH 1794] 中的对齐需求</span><span class="sxs-lookup"><span data-stu-id="bafce-809">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="bafce-810">修复了处理的系统调用数中的 AT_EMPTY_PATH 标志。</span><span class="sxs-lookup"><span data-stu-id="bafce-810">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="bafce-811">修复了在其中删除带有开放句柄 DrvFs 文件将导致出现未定义的行为 [GH 544,966,1357,1535,1615] 的文件的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-811">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="bafce-812">/ 主机将从 Windows 主机文件 (%windir%\system32\drivers\etc\hosts) 现在继承项 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="bafce-812">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="bafce-813">生成 16179</span><span class="sxs-lookup"><span data-stu-id="bafce-813">Build 16179</span></span>

<span data-ttu-id="bafce-814">有关常规 Windows 上生成 16179 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-814">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-815">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-815">Fixed</span></span>
- <span data-ttu-id="bafce-816">没有 WSL 更改这一周。</span><span class="sxs-lookup"><span data-stu-id="bafce-816">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="bafce-817">生成 16176</span><span class="sxs-lookup"><span data-stu-id="bafce-817">Build 16176</span></span>

<span data-ttu-id="bafce-818">有关常规 Windows 上生成 16176 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-818">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-819">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-819">Fixed</span></span>

- [<span data-ttu-id="bafce-820">已启用串行支持</span><span class="sxs-lookup"><span data-stu-id="bafce-820">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="bafce-821">添加了的 IP 套接字选项 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="bafce-821">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="bafce-822">（同时将文件上传到 nginx/PHP-FPM） 实现 pwritev 函数 [GH 1506]</span><span class="sxs-lookup"><span data-stu-id="bafce-822">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="bafce-823">添加了 IP 套接字选项 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="bafce-823">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="bafce-824">支持的套接字选项 IP_MULTICAST_LOOP 和 IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="bafce-824">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="bafce-825">添加的应用程序节点、 traceroute、 dig、 nslookup、 主机的 IP (V6) _MTU 套接字选项</span><span class="sxs-lookup"><span data-stu-id="bafce-825">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="bafce-826">添加了的 IP 套接字选项 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="bafce-826">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="bafce-827">文件系统的改进</span><span class="sxs-lookup"><span data-stu-id="bafce-827">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="bafce-828">允许 UNC 路径的装载</span><span class="sxs-lookup"><span data-stu-id="bafce-828">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="bafce-829">启用在 drvfs CDFS 支持</span><span class="sxs-lookup"><span data-stu-id="bafce-829">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="bafce-830">正确处理 drvfs 中的网络文件系统权限</span><span class="sxs-lookup"><span data-stu-id="bafce-830">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="bafce-831">将对远程驱动器的支持添加到 drvfs</span><span class="sxs-lookup"><span data-stu-id="bafce-831">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="bafce-832">启用 FAT 支持 drvfs 中</span><span class="sxs-lookup"><span data-stu-id="bafce-832">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="bafce-833">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-833">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-834">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="bafce-834">LTP Results</span></span>
<span data-ttu-id="bafce-835">15042 之后的任何更改</span><span class="sxs-lookup"><span data-stu-id="bafce-835">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="bafce-836">生成 16170</span><span class="sxs-lookup"><span data-stu-id="bafce-836">Build 16170</span></span>

<span data-ttu-id="bafce-837">有关常规 Windows 上生成 16170 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-837">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="bafce-838">我们发布了新[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)讨论测试 WSL 我们努力。</span><span class="sxs-lookup"><span data-stu-id="bafce-838">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="bafce-839">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-839">Fixed</span></span>

- <span data-ttu-id="bafce-840">支持套接字选项 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="bafce-840">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="bafce-841">添加对 PTRACE_OLDSETOPTIONS 的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-841">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="bafce-842">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="bafce-842">[GH 1692]</span></span>
- <span data-ttu-id="bafce-843">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-843">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-844">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="bafce-844">LTP Results</span></span>
<span data-ttu-id="bafce-845">15042 之后的任何更改</span><span class="sxs-lookup"><span data-stu-id="bafce-845">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="bafce-846">生成 15046 到 Windows 10 创意者更新</span><span class="sxs-lookup"><span data-stu-id="bafce-846">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="bafce-847">没有更多 WSL 修复或计划到 Windows 10 创意者更新中包含的功能。</span><span class="sxs-lookup"><span data-stu-id="bafce-847">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="bafce-848">WSL 的发行说明将在未来几周定目标到下一步的主要 Windows Update 中添加的恢复。</span><span class="sxs-lookup"><span data-stu-id="bafce-848">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="bafce-849">为常规 Windows 的生成 15046 和将来的内部版本信息，请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-849">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="bafce-850">生成 15042</span><span class="sxs-lookup"><span data-stu-id="bafce-850">Build 15042</span></span>

<span data-ttu-id="bafce-851">有关常规 Windows 上生成 15042 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-851">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-852">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-852">Fixed</span></span>

- <span data-ttu-id="bafce-853">修复出现死锁时删除路径以"..."</span><span class="sxs-lookup"><span data-stu-id="bafce-853">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="bafce-854">修复了在其中 FIONBIO 未成功 [GH 1683] 返回 0</span><span class="sxs-lookup"><span data-stu-id="bafce-854">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="bafce-855">已修复的问题的 inet 数据报套接字的长度为零的读取</span><span class="sxs-lookup"><span data-stu-id="bafce-855">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="bafce-856">修复由于争用条件可能死锁中 drvfs inode 查找 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="bafce-856">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="bafce-857">扩展对 unix 套接字的辅助数据; 支持SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514，613、 1326年]</span><span class="sxs-lookup"><span data-stu-id="bafce-857">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="bafce-858">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-858">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-859">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-859">LTP Results:</span></span>
<span data-ttu-id="bafce-860">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="bafce-860">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="bafce-861">未通过的数目 (失败，已跳过，等等。...):255</span><span class="sxs-lookup"><span data-stu-id="bafce-861">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="bafce-862">生成 15031</span><span class="sxs-lookup"><span data-stu-id="bafce-862">Build 15031</span></span>

<span data-ttu-id="bafce-863">有关常规 Windows 上生成 15031 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-863">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-864">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-864">Fixed</span></span>

- <span data-ttu-id="bafce-865">修复了 bug time(2) 错误偶尔行为。</span><span class="sxs-lookup"><span data-stu-id="bafce-865">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="bafce-866">已修复并发出 where \* SIGPROCMASK syscall 可能会损坏信号掩码。</span><span class="sxs-lookup"><span data-stu-id="bafce-866">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="bafce-867">在 WSL 进程创建通知现在返回完整的命令行长度。</span><span class="sxs-lookup"><span data-stu-id="bafce-867">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="bafce-868">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="bafce-868">[GH 1632]</span></span>
- <span data-ttu-id="bafce-869">WSL 现在将报告线程退出时通过 GDB 挂起的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="bafce-869">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="bafce-870">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="bafce-870">[GH 1196]</span></span>
- <span data-ttu-id="bafce-871">修复了 bug，其中 ptys 会挂起后大量 tmux IO。</span><span class="sxs-lookup"><span data-stu-id="bafce-871">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="bafce-872">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="bafce-872">[GH 1358]</span></span>
- <span data-ttu-id="bafce-873">许多系统调用 （futex、 semtimedop、 ppoll、 sigtimedwait、 itimer、 timer_create） 中的固定的超时验证</span><span class="sxs-lookup"><span data-stu-id="bafce-873">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="bafce-874">添加了的 eventfd EFD_SEMAPHORE 支持 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="bafce-874">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="bafce-875">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-875">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-876">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-876">LTP Results:</span></span>
<span data-ttu-id="bafce-877">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="bafce-877">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="bafce-878">未通过的数目 (失败，已跳过，等等。...):255</span><span class="sxs-lookup"><span data-stu-id="bafce-878">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="bafce-879">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-879">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="bafce-880">生成 15025</span><span class="sxs-lookup"><span data-stu-id="bafce-880">Build 15025</span></span>

<span data-ttu-id="bafce-881">有关常规 Windows 上生成 15025 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-881">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-882">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-882">Fixed</span></span>

- <span data-ttu-id="bafce-883">Bug 修复该坏 grep 2.27 [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="bafce-883">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="bafce-884">实现的 EFD_SEMAPHORE 标志 eventfd2 syscall [GH 452]</span><span class="sxs-lookup"><span data-stu-id="bafce-884">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="bafce-885">实现 /proc/ [pid] / net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="bafce-885">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="bafce-886">信号驱动 IO 支持 unix 流套接字 [GH 393，68]</span><span class="sxs-lookup"><span data-stu-id="bafce-886">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="bafce-887">支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="bafce-887">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="bafce-888">实现 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="bafce-888">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="bafce-889">修复了 bug 其中 epoll_wait() 不等待 [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="bafce-889">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="bafce-890">实现 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="bafce-890">Implement /proc/version_signature</span></span>
- <span data-ttu-id="bafce-891">Tee syscall 现在返回失败，如果这两个文件描述符是指同一管道</span><span class="sxs-lookup"><span data-stu-id="bafce-891">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="bafce-892">实现正确的 Unix 套接字 SO_PEERCRED 行为</span><span class="sxs-lookup"><span data-stu-id="bafce-892">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="bafce-893">固定的 tkill syscall 无效参数处理</span><span class="sxs-lookup"><span data-stu-id="bafce-893">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="bafce-894">若要增加的 drvfs preformace 的更改</span><span class="sxs-lookup"><span data-stu-id="bafce-894">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="bafce-895">微调了 Ruby IO 阻塞</span><span class="sxs-lookup"><span data-stu-id="bafce-895">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="bafce-896">固定的 recvmsg() inet 套接字 [GH 1296] MSG_DONTWAIT 标志返回 EINVAL</span><span class="sxs-lookup"><span data-stu-id="bafce-896">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="bafce-897">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-897">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-898">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-898">LTP Results:</span></span>
<span data-ttu-id="bafce-899">通过的测试数：732</span><span class="sxs-lookup"><span data-stu-id="bafce-899">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="bafce-900">未通过的数目 (失败，已跳过，等等。...):255</span><span class="sxs-lookup"><span data-stu-id="bafce-900">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="bafce-901">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-901">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="bafce-902">生成 15019</span><span class="sxs-lookup"><span data-stu-id="bafce-902">Build 15019</span></span>

<span data-ttu-id="bafce-903">有关常规 Windows 上生成 15019 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-903">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-904">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-904">Fixed</span></span>

- <span data-ttu-id="bafce-905">修复了 bug 的不正确地报告中的 CPU 使用率 procfs htop (GH 823，945、 971) 等工具</span><span class="sxs-lookup"><span data-stu-id="bafce-905">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="bafce-906">在现有调用 open （） 方法与 O_TRUNC 时文件 inotify 现在会生成之前 IN_OPEN IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="bafce-906">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="bafce-907">Unix 套接字 getsockopt SO_ERROR 启用 postgress [GH 61，1354年] 的修补程序</span><span class="sxs-lookup"><span data-stu-id="bafce-907">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="bafce-908">实现针对 GO 语言 /proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="bafce-908">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="bafce-909">Pt-get 包更新后台任务现在在隐藏模式运行从视图</span><span class="sxs-lookup"><span data-stu-id="bafce-909">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="bafce-910">Ipv6 localhost （Spring-Framework(Java) 失败） 的清除范围。</span><span class="sxs-lookup"><span data-stu-id="bafce-910">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="bafce-911">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-911">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-912">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-912">LTP Results:</span></span>
<span data-ttu-id="bafce-913">通过的测试数：714</span><span class="sxs-lookup"><span data-stu-id="bafce-913">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="bafce-914">未通过的数目 (失败，已跳过，等等。...):249</span><span class="sxs-lookup"><span data-stu-id="bafce-914">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="bafce-915">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-915">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="bafce-916">生成 15014</span><span class="sxs-lookup"><span data-stu-id="bafce-916">Build 15014</span></span>

<span data-ttu-id="bafce-917">有关常规 Windows 上生成 15014 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="bafce-917">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-918">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-918">Fixed</span></span>

- <span data-ttu-id="bafce-919">Ctrl + C 现在可按预期方式</span><span class="sxs-lookup"><span data-stu-id="bafce-919">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="bafce-920">htop 和 ps auxw 现在显示正确的资源利用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="bafce-920">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="bafce-921">NT 异常信号的基本转换。</span><span class="sxs-lookup"><span data-stu-id="bafce-921">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="bafce-922">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="bafce-922">(GH #513)</span></span>
- <span data-ttu-id="bafce-923">fallocate 现在 ENOSPC 与运行时失败而不是 EINVAL (GH #1571) 空间不足</span><span class="sxs-lookup"><span data-stu-id="bafce-923">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="bafce-924">添加了的 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="bafce-924">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="bafce-925">实现的 semop 和 semtimedop 系统调用</span><span class="sxs-lookup"><span data-stu-id="bafce-925">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="bafce-926">固定的 nslookup 错误的 IP_RECVTOS & IPV6_RECVTCLASS 套接字选项 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="bafce-926">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="bafce-927">对套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT 的支持</span><span class="sxs-lookup"><span data-stu-id="bafce-927">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="bafce-928">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-928">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-929">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-929">LTP Results:</span></span>
<span data-ttu-id="bafce-930">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="bafce-930">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="bafce-931">未通过的数目 (失败，已跳过，等等。...):255</span><span class="sxs-lookup"><span data-stu-id="bafce-931">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="bafce-932">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-932">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="bafce-933">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="bafce-933">Syscall Summary</span></span>
<span data-ttu-id="bafce-934">总 Syscall:384</span><span class="sxs-lookup"><span data-stu-id="bafce-934">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="bafce-935">实现的总计：235</span><span class="sxs-lookup"><span data-stu-id="bafce-935">Total Implemented: 235</span></span> </br>
<span data-ttu-id="bafce-936">用作存根的总计：22</span><span class="sxs-lookup"><span data-stu-id="bafce-936">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="bafce-937">未实现的总计：127</span><span class="sxs-lookup"><span data-stu-id="bafce-937">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="bafce-938">详细的分解结构</span><span class="sxs-lookup"><span data-stu-id="bafce-938">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="bafce-939">生成 15007</span><span class="sxs-lookup"><span data-stu-id="bafce-939">Build 15007</span></span>

<span data-ttu-id="bafce-940">有关常规 Windows 上生成 15007 信息请访问[Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="bafce-940">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="bafce-941">已知的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-941">Known Issue</span></span>

- <span data-ttu-id="bafce-942">是一个已知的 bug，控制台不识别某些 Ctrl +<key>输入。</span><span class="sxs-lookup"><span data-stu-id="bafce-942">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="bafce-943">这包括将充当正常的 c 按键的 ctrl + c 命令。</span><span class="sxs-lookup"><span data-stu-id="bafce-943">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="bafce-944">解决方法：将备用键映射到 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="bafce-944">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="bafce-945">例如，若要映射到 Ctrl + C Ctrl + K 执行： `stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="bafce-945">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="bafce-946">此映射的每个终端，将需要进行*每个*启动时间 bash。</span><span class="sxs-lookup"><span data-stu-id="bafce-946">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="bafce-947">用户可以浏览选项，此操作在其 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="bafce-947">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="bafce-948">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-948">Fixed</span></span>

- <span data-ttu-id="bafce-949">更正了在其中运行 WSL 会占用 100%的 CPU 内核的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-949">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="bafce-950">套接字选项 IP_PKTINFO，IPV6_RECVPKTINFO 现在支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-950">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="bafce-951">(GH #851, 987)</span><span class="sxs-lookup"><span data-stu-id="bafce-951">(GH #851, 987)</span></span>
- <span data-ttu-id="bafce-952">截断到 lxcore 以 16 个字节的网络接口物理地址 (GH #1452，1414，1343，468，308)</span><span class="sxs-lookup"><span data-stu-id="bafce-952">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="bafce-953">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-954">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-954">LTP Results:</span></span>
<span data-ttu-id="bafce-955">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="bafce-955">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="bafce-956">未通过的数目 (失败，已跳过，等等。...):255</span><span class="sxs-lookup"><span data-stu-id="bafce-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="bafce-957">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="bafce-958">生成 15002</span><span class="sxs-lookup"><span data-stu-id="bafce-958">Build 15002</span></span>

<span data-ttu-id="bafce-959">有关常规 Windows 上生成 15002 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-959">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="bafce-960">已知的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-960">Known Issue</span></span>

<span data-ttu-id="bafce-961">两个已知的问题：</span><span class="sxs-lookup"><span data-stu-id="bafce-961">Two known issues:</span></span>
- <span data-ttu-id="bafce-962">是一个已知的 bug，控制台不识别某些 Ctrl +<key>输入。</span><span class="sxs-lookup"><span data-stu-id="bafce-962">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="bafce-963">这包括将充当正常的 c 按键的 ctrl + c 命令。</span><span class="sxs-lookup"><span data-stu-id="bafce-963">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="bafce-964">解决方法：将备用键映射到 Ctrl + C。</span><span class="sxs-lookup"><span data-stu-id="bafce-964">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="bafce-965">例如，若要映射到 Ctrl + C Ctrl + K 执行： `stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="bafce-965">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="bafce-966">此映射的每个终端，将需要进行*每个*启动时间 bash。</span><span class="sxs-lookup"><span data-stu-id="bafce-966">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="bafce-967">用户可以浏览选项，此操作在其 `.bashrc`</span><span class="sxs-lookup"><span data-stu-id="bafce-967">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="bafce-968">WSL 正在运行时系统线程将占用 100%的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="bafce-968">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="bafce-969">解决并在内部修复根本原因。</span><span class="sxs-lookup"><span data-stu-id="bafce-969">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="bafce-970">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-970">Fixed</span></span>

- <span data-ttu-id="bafce-971">现在必须在相同的权限级别创建所有的 bash 会话。</span><span class="sxs-lookup"><span data-stu-id="bafce-971">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="bafce-972">尝试在不同级别上启动会话将被阻止。</span><span class="sxs-lookup"><span data-stu-id="bafce-972">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="bafce-973">这意味着管理员和非管理员控制台不能在同一时间运行。</span><span class="sxs-lookup"><span data-stu-id="bafce-973">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="bafce-974">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="bafce-974">(GH #626)</span></span>
<br/>
- <span data-ttu-id="bafce-975">实现以下 NETLINK_ROUTE 消息 （需要 Windows 管理员）</span><span class="sxs-lookup"><span data-stu-id="bafce-975">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="bafce-976">RTM_NEWADDR (支持`ip addr add`)</span><span class="sxs-lookup"><span data-stu-id="bafce-976">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="bafce-977">RTM_NEWROUTE (支持`ip route add`)</span><span class="sxs-lookup"><span data-stu-id="bafce-977">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="bafce-978">RTM_DELADDR (支持`ip addr del`)</span><span class="sxs-lookup"><span data-stu-id="bafce-978">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="bafce-979">RTM_DELROUTE (支持`ip route del`)</span><span class="sxs-lookup"><span data-stu-id="bafce-979">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="bafce-980">检查要更新的包的计划的任务运行将不再按流量计费的连接 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="bafce-980">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="bafce-981">修复了错误卡在何处通过管道将获取即 bash-c"ls alR /"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="bafce-981">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="bafce-982">实现的 TCP_KEEPCNT 套接字选项 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="bafce-982">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="bafce-983">实现的 IP_MTU_DISCOVER INET 套接字选项 (GH #720、 717，170，69)</span><span class="sxs-lookup"><span data-stu-id="bafce-983">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="bafce-984">删除旧的功能，若要从使用 NT 路径查找 init 运行 NT 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-984">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="bafce-985">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="bafce-985">(GH #1325)</span></span>
- <span data-ttu-id="bafce-986">修复/kmsg 以允许组 / 其他读取访问权限 (0644) （GH # 1321） 哈希模式</span><span class="sxs-lookup"><span data-stu-id="bafce-986">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="bafce-987">实现的 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="bafce-987">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="bafce-988">更正了的错误的进程启动时间显示为 2432 年 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="bafce-988">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="bafce-989">切换的默认术语环境变量为 xterm 256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="bafce-989">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="bafce-990">修改后在进程分叉期间计算处理提交的方式。</span><span class="sxs-lookup"><span data-stu-id="bafce-990">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="bafce-991">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="bafce-991">(GH #1286)</span></span>
- <span data-ttu-id="bafce-992">实现的 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="bafce-992">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="bafce-993">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="bafce-993">(GH #1286)</span></span>
- <span data-ttu-id="bafce-994">实现的 /proc/net/route 文件 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="bafce-994">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="bafce-995">修复了快捷方式名称不正确的错误本地化 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="bafce-995">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="bafce-996">固定的 elf 分析错误地验证程序标头的逻辑必须是小于 （或等于） PATH_MAX。</span><span class="sxs-lookup"><span data-stu-id="bafce-996">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="bafce-997">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="bafce-997">(GH #1048)</span></span>
- <span data-ttu-id="bafce-998">实现的 statfs 回调 procfs，sysfs、 cgroupfs，和 binfmtfs (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="bafce-998">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="bafce-999">不会关闭 (GH #1184，GH # 1193年中也讨论了) 的固定的 AptPackageIndexUpdate windows</span><span class="sxs-lookup"><span data-stu-id="bafce-999">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="bafce-1000">添加了的 ASLR 个性 ADDR_NO_RANDOMIZE 支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-1000">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="bafce-1001">(GH #1148, 1128)</span><span class="sxs-lookup"><span data-stu-id="bafce-1001">(GH #1148, 1128)</span></span>
- <span data-ttu-id="bafce-1002">改进了的 PTRACE_GETSIGINFO，SIGSEGV 的适当 gdb AV (GH #875) 期间的堆栈跟踪</span><span class="sxs-lookup"><span data-stu-id="bafce-1002">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="bafce-1003">Elf 不再解析为 patchelf 二进制文件无法正常工作。</span><span class="sxs-lookup"><span data-stu-id="bafce-1003">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="bafce-1004">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="bafce-1004">(GH #471)</span></span>
- <span data-ttu-id="bafce-1005">VPN DNS 传播到 /etc/resolv.conf (GH #416，1350年)</span><span class="sxs-lookup"><span data-stu-id="bafce-1005">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="bafce-1006">对 TCP 的改进关闭的更可靠的数据传输。</span><span class="sxs-lookup"><span data-stu-id="bafce-1006">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="bafce-1007">(GH #610 616、 1025，1335年)</span><span class="sxs-lookup"><span data-stu-id="bafce-1007">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="bafce-1008">现在返回正确的错误代码的文件太多时打开 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1008">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="bafce-1009">(GH # 1126年 2090年)</span><span class="sxs-lookup"><span data-stu-id="bafce-1009">(GH #1126, 2090)</span></span>
- <span data-ttu-id="bafce-1010">Windows 审核过程中的映像名称日志现在报表创建审核。</span><span class="sxs-lookup"><span data-stu-id="bafce-1010">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="bafce-1011">正常失败时启动 bash 窗口中的从 bash.exe</span><span class="sxs-lookup"><span data-stu-id="bafce-1011">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="bafce-1012">互操作时，添加了的错误消息无法访问工作目录下 LxFs (即 notepad.exe.bashrc)</span><span class="sxs-lookup"><span data-stu-id="bafce-1012">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="bafce-1013">修复了问题，Windows 路径已被截断 WSL</span><span class="sxs-lookup"><span data-stu-id="bafce-1013">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="bafce-1014">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1015">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1015">LTP Results:</span></span>
<span data-ttu-id="bafce-1016">通过的测试数：690</span><span class="sxs-lookup"><span data-stu-id="bafce-1016">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="bafce-1017">未通过的数目 (失败，已跳过，等等。...):274</span><span class="sxs-lookup"><span data-stu-id="bafce-1017">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="bafce-1018">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1019">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1019">Syscall Support</span></span>
<span data-ttu-id="bafce-1020">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1020">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1021">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1021">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="bafce-1022">生成 14986</span><span class="sxs-lookup"><span data-stu-id="bafce-1022">Build 14986</span></span>

<span data-ttu-id="bafce-1023">有关常规 Windows 上生成 14986 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1023">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1024">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1024">Fixed</span></span>

- <span data-ttu-id="bafce-1025">使用 Netlink 和 Pty Ioctl 固定错误检查</span><span class="sxs-lookup"><span data-stu-id="bafce-1025">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="bafce-1026">内核版本现在将报告 4.4.0-43 与 Xenial 的一致性</span><span class="sxs-lookup"><span data-stu-id="bafce-1026">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="bafce-1027">Bash.exe 现在启动时输入定向到 nul: (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="bafce-1027">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="bafce-1028">线程 Id 现在可以正确报告中 procfs (GH #967)</span><span class="sxs-lookup"><span data-stu-id="bafce-1028">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="bafce-1029">IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |现在支持在 inotify_add_watch() (GH #1280) IN_ISDIR 标志</span><span class="sxs-lookup"><span data-stu-id="bafce-1029">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="bafce-1030">实现 timer_create 和相关的系统调用。</span><span class="sxs-lookup"><span data-stu-id="bafce-1030">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="bafce-1031">这使 GHC 支持 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="bafce-1031">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="bafce-1032">修复了 ping 返回的时间为 0.000ms (GH #1296) 的位置的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1032">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="bafce-1033">打开的文件太多时，请返回正确的错误代码。</span><span class="sxs-lookup"><span data-stu-id="bafce-1033">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="bafce-1034">其中的网络接口数据 Netlink 请求接口的硬件地址为 32 字节 （如 Teredo 接口） 将失败并 EINVAL WSL 中修复的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1034">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="bafce-1035">请注意，Linux"ip"实用程序包含一个 bug，它会崩溃如果 WSL 报告 32 字节硬件地址。</span><span class="sxs-lookup"><span data-stu-id="bafce-1035">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="bafce-1036">这是"ip"，不 WSL 中的 bug。</span><span class="sxs-lookup"><span data-stu-id="bafce-1036">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="bafce-1037">"Ip"实用程序硬编码的字符串缓冲区长度用于打印硬件地址，并且该缓冲区因过小，若要打印的 32 字节硬件地址。</span><span class="sxs-lookup"><span data-stu-id="bafce-1037">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="bafce-1038">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1038">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1039">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1039">LTP Results:</span></span>
<span data-ttu-id="bafce-1040">通过的测试数：669</span><span class="sxs-lookup"><span data-stu-id="bafce-1040">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="bafce-1041">未通过的数目 (失败，已跳过，等等。...):258</span><span class="sxs-lookup"><span data-stu-id="bafce-1041">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="bafce-1042">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1042">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1043">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1043">Syscall Support</span></span>
<span data-ttu-id="bafce-1044">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1044">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1045">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1045">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="bafce-1046">生成 14971</span><span class="sxs-lookup"><span data-stu-id="bafce-1046">Build 14971</span></span>

<span data-ttu-id="bafce-1047">有关常规 Windows 上生成 14971 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1047">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1048">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1048">Fixed</span></span>

 - <span data-ttu-id="bafce-1049">由于超出我们的控制范围的情况适用于 Linux 的 Windows 子系统本版本中没有的更新。</span><span class="sxs-lookup"><span data-stu-id="bafce-1049">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="bafce-1050">定期计划的更新将在下一版本上继续进行。</span><span class="sxs-lookup"><span data-stu-id="bafce-1050">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1051">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1051">LTP Results:</span></span>
<span data-ttu-id="bafce-1052">14965 相比并无变化</span><span class="sxs-lookup"><span data-stu-id="bafce-1052">Unchanged from 14965</span></span> </br>
<span data-ttu-id="bafce-1053">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="bafce-1053">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="bafce-1054">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1054">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1055">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1055">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="bafce-1056">生成 14965</span><span class="sxs-lookup"><span data-stu-id="bafce-1056">Build 14965</span></span>

<span data-ttu-id="bafce-1057">有关常规 Windows 上生成 14965 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1057">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1058">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1058">Fixed</span></span>

- <span data-ttu-id="bafce-1059">支持 Netlink 套接字 NETLINK_ROUTE 协议 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="bafce-1059">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="bafce-1060">启用网络枚举 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="bafce-1060">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="bafce-1061">详细信息可在我们[WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1061">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="bafce-1062">/sbin 现在在默认情况下的用户的 path</span><span class="sxs-lookup"><span data-stu-id="bafce-1062">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="bafce-1063">现在默认情况下 （即可以现在键入 notepad.exe 而无需添加到 Linux 路径 System32） 追加到 WSL 路径的 NT 用户路径</span><span class="sxs-lookup"><span data-stu-id="bafce-1063">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="bafce-1064">添加了的对 /proc/sys/kernel/cap_last_cap</span><span class="sxs-lookup"><span data-stu-id="bafce-1064">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="bafce-1065">现在 NT 二进制文件可以启动从 WSL 中，如果当前工作目录包含非 ansi 字符 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="bafce-1065">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="bafce-1066">允许断开连接的 unix 流套接字上的关闭。</span><span class="sxs-lookup"><span data-stu-id="bafce-1066">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="bafce-1067">添加了的对 PR_GET_PDEATHSIG。</span><span class="sxs-lookup"><span data-stu-id="bafce-1067">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="bafce-1068">添加了的对 CLONE_PARENT</span><span class="sxs-lookup"><span data-stu-id="bafce-1068">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="bafce-1069">修复了错误卡在何处通过管道将获取即 bash-c"ls alR /"|bash-c"cat"(GH #1214)</span><span class="sxs-lookup"><span data-stu-id="bafce-1069">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="bafce-1070">若要连接到当前终端的处理请求。</span><span class="sxs-lookup"><span data-stu-id="bafce-1070">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="bafce-1071">将标记 /proc/<pid>/oom_score_adj 为可写入。</span><span class="sxs-lookup"><span data-stu-id="bafce-1071">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="bafce-1072">添加 /sys/fs/cgroup 文件夹。</span><span class="sxs-lookup"><span data-stu-id="bafce-1072">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="bafce-1073">sched_setaffinity 应返回关联位掩码的数</span><span class="sxs-lookup"><span data-stu-id="bafce-1073">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="bafce-1074">修复错误地假设它解释器路径必须少于 64 个字符长 ELF 验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="bafce-1074">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="bafce-1075">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="bafce-1075">(GH #743)</span></span>
- <span data-ttu-id="bafce-1076">打开的文件描述符可以保留控制台窗口处于打开状态 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="bafce-1076">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="bafce-1077">Fixeed 错误其中 rename （） 失败，出现尾部反斜杠目标名称 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="bafce-1077">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="bafce-1078">实现 /proc/net/dev 文件</span><span class="sxs-lookup"><span data-stu-id="bafce-1078">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="bafce-1079">由于计时器分辨率，固定的 0.000ms 执行 ping 操作。</span><span class="sxs-lookup"><span data-stu-id="bafce-1079">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="bafce-1080">实现的 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="bafce-1080">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="bafce-1081">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1081">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1082">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1082">LTP Results:</span></span>
<span data-ttu-id="bafce-1083">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="bafce-1083">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="bafce-1084">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1084">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1085">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1085">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="bafce-1086">生成 14959</span><span class="sxs-lookup"><span data-stu-id="bafce-1086">Build 14959</span></span>

<span data-ttu-id="bafce-1087">有关常规 Windows 上生成 14959 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1087">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1088">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1088">Fixed</span></span>

- <span data-ttu-id="bafce-1089">改进了的 Windows 的 Pico 进程通知。</span><span class="sxs-lookup"><span data-stu-id="bafce-1089">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="bafce-1090">上找到其他信息[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1090">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="bafce-1091">使用 Windows 的互操作性的改进了的稳定性</span><span class="sxs-lookup"><span data-stu-id="bafce-1091">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="bafce-1092">修复了错误 0x80070057 时启动 bash.exe 时启用了企业数据保护 (EDP)</span><span class="sxs-lookup"><span data-stu-id="bafce-1092">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="bafce-1093">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1093">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1094">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1094">LTP Results:</span></span>
<span data-ttu-id="bafce-1095">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="bafce-1095">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="bafce-1096">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1096">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1097">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1097">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="bafce-1098">生成 14955</span><span class="sxs-lookup"><span data-stu-id="bafce-1098">Build 14955</span></span>

<span data-ttu-id="bafce-1099">有关常规 Windows 上生成 14955 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1099">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1100">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1100">Fixed</span></span>

 - <span data-ttu-id="bafce-1101">由于超出我们的控制范围的情况适用于 Linux 的 Windows 子系统本版本中没有的更新。</span><span class="sxs-lookup"><span data-stu-id="bafce-1101">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="bafce-1102">定期计划的更新将在下一版本上继续进行。</span><span class="sxs-lookup"><span data-stu-id="bafce-1102">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1103">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1103">LTP Results:</span></span>
<span data-ttu-id="bafce-1104">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="bafce-1104">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="bafce-1105">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1105">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1106">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1106">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="bafce-1107">生成 14951</span><span class="sxs-lookup"><span data-stu-id="bafce-1107">Build 14951</span></span>

<span data-ttu-id="bafce-1108">有关常规 Windows 上生成 14951 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1108">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="bafce-1109">新功能：Windows / Ubuntu 的互操作性</span><span class="sxs-lookup"><span data-stu-id="bafce-1109">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="bafce-1110">现在可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-1110">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="bafce-1111">这使用户能够使用其 Windows 环境和系统中已不可能的方式进行交互。</span><span class="sxs-lookup"><span data-stu-id="bafce-1111">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="bafce-1112">作为快速示例中，是现在用户可以运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="bafce-1112">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="bafce-1113">可以在找到详细信息：</span><span class="sxs-lookup"><span data-stu-id="bafce-1113">More information can be found at:</span></span>

- [<span data-ttu-id="bafce-1114">互操作的 WSL 团队博客</span><span class="sxs-lookup"><span data-stu-id="bafce-1114">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="bafce-1115">MSDN 互操作文档</span><span class="sxs-lookup"><span data-stu-id="bafce-1115">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1116">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1116">Fixed</span></span>

- <span data-ttu-id="bafce-1117">Ubuntu 16.04 (Xenial) 现已安装的所有新 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="bafce-1117">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="bafce-1118">具有现有 14.04 （值得信赖） 实例的用户将不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="bafce-1118">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="bafce-1119">现在显示在安装过程中设置的区域设置</span><span class="sxs-lookup"><span data-stu-id="bafce-1119">Locale set during install is now displayed</span></span>
- <span data-ttu-id="bafce-1120">终端的改进包括的 bug 其中不始终将 WSL 过程重定向到一个文件不起作用</span><span class="sxs-lookup"><span data-stu-id="bafce-1120">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="bafce-1121">控制台生存期应取决于 bash.exe 生存期</span><span class="sxs-lookup"><span data-stu-id="bafce-1121">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="bafce-1122">控制台窗口大小应使用可见的大小，不缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="bafce-1122">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="bafce-1123">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1123">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1124">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1124">LTP Results:</span></span>
<span data-ttu-id="bafce-1125">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="bafce-1125">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="bafce-1126">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1126">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1127">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1127">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="bafce-1128">生成 14946</span><span class="sxs-lookup"><span data-stu-id="bafce-1128">Build 14946</span></span>

<span data-ttu-id="bafce-1129">有关常规 Windows 上生成 14946 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1129">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1130">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1130">Fixed</span></span>

- <span data-ttu-id="bafce-1131">修复了阻止使用包含空格或引号的 NT 用户名创建 WSL 的用户的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="bafce-1131">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="bafce-1132">更改 VolFs 和 DrvFs 统计信息中返回 0 表示目录的链接计数</span><span class="sxs-lookup"><span data-stu-id="bafce-1132">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="bafce-1133">支持 IPV6_MULTICAST_HOPS 套接字选项。</span><span class="sxs-lookup"><span data-stu-id="bafce-1133">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="bafce-1134">限制到单个控制台 I/O 循环每 tty。</span><span class="sxs-lookup"><span data-stu-id="bafce-1134">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="bafce-1135">示例： 可能是以下命令：</span><span class="sxs-lookup"><span data-stu-id="bafce-1135">Example: the following command is possible:</span></span>
  - <span data-ttu-id="bafce-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="bafce-1136">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="bafce-1137">空格替换为 /proc/cpuinfo (GH #1115) 中的选项卡</span><span class="sxs-lookup"><span data-stu-id="bafce-1137">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="bafce-1138">DrvFs 现在将显示在名称匹配已安装的 Windows 卷 mountinfo</span><span class="sxs-lookup"><span data-stu-id="bafce-1138">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="bafce-1139">/home 和 /root 现在出现在正确的名称与 mountinfo</span><span class="sxs-lookup"><span data-stu-id="bafce-1139">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="bafce-1140">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1140">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1141">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1141">LTP Results:</span></span>
<span data-ttu-id="bafce-1142">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="bafce-1142">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="bafce-1143">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1143">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1144">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1144">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="bafce-1145">生成 14942</span><span class="sxs-lookup"><span data-stu-id="bafce-1145">Build 14942</span></span>

<span data-ttu-id="bafce-1146">有关常规 Windows 上生成 14942 信息请访问[Windows 博客](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1146">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1147">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1147">Fixed</span></span>

- <span data-ttu-id="bafce-1148">错误检查，包括"尝试执行的 NOEXECUTE 内存"网络已阻止 SSH 的故障数</span><span class="sxs-lookup"><span data-stu-id="bafce-1148">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="bafce-1149">在现 inotifiy 支持来自 DrvFs 上的 Windows 应用程序生成的通知</span><span class="sxs-lookup"><span data-stu-id="bafce-1149">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="bafce-1150">实施 mongod TCP_KEEPIDLE 和 TCP_KEEPINTVL。</span><span class="sxs-lookup"><span data-stu-id="bafce-1150">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="bafce-1151">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="bafce-1151">(GH #695)</span></span>
- <span data-ttu-id="bafce-1152">实现 pivot_root 系统调用</span><span class="sxs-lookup"><span data-stu-id="bafce-1152">Implement the pivot_root system call</span></span>
- <span data-ttu-id="bafce-1153">实现 SO_DONTROUTE 的套接字选项</span><span class="sxs-lookup"><span data-stu-id="bafce-1153">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="bafce-1154">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1154">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="bafce-1155">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1155">LTP Results:</span></span>
<span data-ttu-id="bafce-1156">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="bafce-1156">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="bafce-1157">未通过的数目 (失败，已跳过，等等。...):263</span><span class="sxs-lookup"><span data-stu-id="bafce-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="bafce-1158">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1159">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1159">Syscall Support</span></span>
<span data-ttu-id="bafce-1160">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1160">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1161">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1161">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="bafce-1162">生成 14936</span><span class="sxs-lookup"><span data-stu-id="bafce-1162">Build 14936</span></span>

<span data-ttu-id="bafce-1163">有关常规 Windows 上生成 14936 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1163">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="bafce-1164">注意：WSL 将在即将发布的版本中安装 Ubuntu 版本 16.04 (Xenial) 而不是 Ubuntu 14.04 （可信赖）。</span><span class="sxs-lookup"><span data-stu-id="bafce-1164">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="bafce-1165">此更改将应用于预览体验成员安装新实例 （lxrun.exe /install 或首次运行 bash.exe）。</span><span class="sxs-lookup"><span data-stu-id="bafce-1165">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="bafce-1166">可信赖的现有实例将不自动升级。</span><span class="sxs-lookup"><span data-stu-id="bafce-1166">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="bafce-1167">用户可以升级其值得信赖的映像为 Xenial 使用执行版本升级命令。</span><span class="sxs-lookup"><span data-stu-id="bafce-1167">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="bafce-1168">已知的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1168">Known Issue</span></span>
<span data-ttu-id="bafce-1169">WSL 遇到某些套接字实现的问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-1169">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="bafce-1170">检测的错误表现为崩溃并出现错误"尝试执行的 NOEXECUTE 内存"。</span><span class="sxs-lookup"><span data-stu-id="bafce-1170">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="bafce-1171">使用 ssh 配合使用时，此问题的最常见的表现是崩溃。</span><span class="sxs-lookup"><span data-stu-id="bafce-1171">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="bafce-1172">在内部版本中已修复并尽早将被推送到内部人员根本原因。</span><span class="sxs-lookup"><span data-stu-id="bafce-1172">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="bafce-1173">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1173">Fixed</span></span>

- <span data-ttu-id="bafce-1174">实现 chroot 系统调用</span><span class="sxs-lookup"><span data-stu-id="bafce-1174">Implemented the chroot system call</span></span>
- <span data-ttu-id="bafce-1175">改进 inotify~~包括对来自 DrvFs 上的 Windows 应用程序生成的通知的支持~~</span><span class="sxs-lookup"><span data-stu-id="bafce-1175">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="bafce-1176">更正：Inotify 更改源自 Windows 应用程序在此时间不可用的支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-1176">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="bafce-1177">套接字绑定到 IPV6::<port n>现在支持 IPV6_V6ONLY (GH #68、 #157、 #393、 #460，#674、 #740、 #982、 #996)</span><span class="sxs-lookup"><span data-stu-id="bafce-1177">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="bafce-1178">Waitid systemcall WNOWAIT 行为实现 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="bafce-1178">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="bafce-1179">支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="bafce-1179">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="bafce-1180">应立即返回长度为零的 read （） (GH #975)</span><span class="sxs-lookup"><span data-stu-id="bafce-1180">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="bafce-1181">正确处理文件名和文件名的前缀，.tar 文件中不包括 NULL 终止符。</span><span class="sxs-lookup"><span data-stu-id="bafce-1181">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="bafce-1182">epoll /dev/null 时支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1182">epoll support for /dev/null</span></span>
- <span data-ttu-id="bafce-1183">修复 /dev/alarm 时间源</span><span class="sxs-lookup"><span data-stu-id="bafce-1183">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="bafce-1184">Bash-c 现在可以将重定向到文件</span><span class="sxs-lookup"><span data-stu-id="bafce-1184">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="bafce-1185">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1185">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1186">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1186">LTP Results:</span></span>
<span data-ttu-id="bafce-1187">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="bafce-1187">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="bafce-1188">未通过的数目 (失败，已跳过，等等。...):264</span><span class="sxs-lookup"><span data-stu-id="bafce-1188">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="bafce-1189">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1189">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1190">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1190">Syscall Support</span></span>
<span data-ttu-id="bafce-1191">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1191">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1192">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1192">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="bafce-1193">生成 14931</span><span class="sxs-lookup"><span data-stu-id="bafce-1193">Build 14931</span></span>

<span data-ttu-id="bafce-1194">有关常规 Windows 上生成 14931 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1194">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1195">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1195">Fixed</span></span>

 - <span data-ttu-id="bafce-1196">由于超出我们的控制范围的情况适用于 Linux 的 Windows 子系统本版本中没有的更新。</span><span class="sxs-lookup"><span data-stu-id="bafce-1196">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="bafce-1197">定期计划的更新将继续进行下一版本中。</span><span class="sxs-lookup"><span data-stu-id="bafce-1197">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="bafce-1198">生成 14926</span><span class="sxs-lookup"><span data-stu-id="bafce-1198">Build 14926</span></span>

<span data-ttu-id="bafce-1199">有关常规 Windows 上生成 14926 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1199">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1200">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1200">Fixed</span></span>

- <span data-ttu-id="bafce-1201">成功进行 ping 操作现在具有管理员特权的控制台中的工作原理</span><span class="sxs-lookup"><span data-stu-id="bafce-1201">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="bafce-1202">Ping6 现在支持，也无需管理员权限</span><span class="sxs-lookup"><span data-stu-id="bafce-1202">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="bafce-1203">Inotify 支持通过 WSL 修改的文件。</span><span class="sxs-lookup"><span data-stu-id="bafce-1203">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="bafce-1204">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="bafce-1204">(GH #216)</span></span>
  - <span data-ttu-id="bafce-1205">支持的标志：</span><span class="sxs-lookup"><span data-stu-id="bafce-1205">Flags supported:</span></span>
    - <span data-ttu-id="bafce-1206">inotify_init1:LX_O_CLOEXEC LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="bafce-1206">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="bafce-1207">inotify_add_watch 事件：LX_IN_ACCESS、 LX_IN_MODIFY、 LX_IN_ATTRIB、 LX_IN_CLOSE_WRITE、 LX_IN_CLOSE_NOWRITE、 LX_IN_OPEN、 LX_IN_MOVED_FROM、 LX_IN_MOVED_TO、 LX_IN_CREATE、 LX_IN_DELETE、 LX_IN_DELETE_SELF、 LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="bafce-1207">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="bafce-1208">inotify_add_watch 属性：LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="bafce-1208">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="bafce-1209">读取输出：LX_IN_ISDIR LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="bafce-1209">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="bafce-1210">已知的问题：修改文件从 Windows 应用程序不会生成任何事件</span><span class="sxs-lookup"><span data-stu-id="bafce-1210">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="bafce-1211">Unix 套接字现在支持 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="bafce-1211">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="bafce-1212">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="bafce-1212">LTP Results:</span></span>
<span data-ttu-id="bafce-1213">通过的测试数：651</span><span class="sxs-lookup"><span data-stu-id="bafce-1213">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="bafce-1214">未通过的数目 (失败，已跳过，等等。...):258</span><span class="sxs-lookup"><span data-stu-id="bafce-1214">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="bafce-1215">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="bafce-1215">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="bafce-1216">生成 14915</span><span class="sxs-lookup"><span data-stu-id="bafce-1216">Build 14915</span></span>

<span data-ttu-id="bafce-1217">有关常规 Windows 上生成 14915 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1217">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1218">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1218">Fixed</span></span>
-  <span data-ttu-id="bafce-1219">Socketpair unix 数据报套接字 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="bafce-1219">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="bafce-1220">SO_REUSEADDR Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1220">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="bafce-1221">UNIX 套接字支持 SO_BROADCAST (GH #568)</span><span class="sxs-lookup"><span data-stu-id="bafce-1221">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="bafce-1222">Unix 套接字支持 SOCK_SEQPACKET (GH #758，#546)</span><span class="sxs-lookup"><span data-stu-id="bafce-1222">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="bafce-1223">添加对 unix 数据报套接字发送、 接收和关闭的支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1223">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="bafce-1224">解决由于非固定地址无效 mmap 参数验证错误检查。</span><span class="sxs-lookup"><span data-stu-id="bafce-1224">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="bafce-1225">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="bafce-1225">(GH #847)</span></span>
- <span data-ttu-id="bafce-1226">支持暂停 / 恢复终端状态的</span><span class="sxs-lookup"><span data-stu-id="bafce-1226">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="bafce-1227">对 TIOCPKT ioctl，若要取消阻止屏幕实用程序 (GH #774) 的支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1227">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="bafce-1228">已知的问题：功能键不可操作</span><span class="sxs-lookup"><span data-stu-id="bafce-1228">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="bafce-1229">更正可能导致已释放的成员 ReaderReady LxpTimerFdWorkerRoutine (GH #814) 访问的 TimerFd 的争用问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1229">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="bafce-1230">启用可重新启动系统调用支持 futex、 投票、 和 clock_nanosleep</span><span class="sxs-lookup"><span data-stu-id="bafce-1230">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="bafce-1231">添加了的绑定装入支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1231">Added bind mount support</span></span>
- <span data-ttu-id="bafce-1232">取消共享装入命名空间支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1232">unshare for mount namespace support</span></span>
    - <span data-ttu-id="bafce-1233">已知的问题：创建与新的装入命名空间时`unshare(CLONE_NEWNS)`当前工作目录将继续指向旧的命名空间</span><span class="sxs-lookup"><span data-stu-id="bafce-1233">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="bafce-1234">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="bafce-1234">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="bafce-1235">生成 14905</span><span class="sxs-lookup"><span data-stu-id="bafce-1235">Build 14905</span></span>

<span data-ttu-id="bafce-1236">有关常规 Windows 上生成 14905 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1236">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1237">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1237">Fixed</span></span>
- <span data-ttu-id="bafce-1238">可重新启动系统调用现支持 (GH #349，GH #520)</span><span class="sxs-lookup"><span data-stu-id="bafce-1238">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="bafce-1239">符号链接到目录结束在 / 现在操作 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="bafce-1239">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="bafce-1240">实现的 RNDGETENTCNT ioctl 用于 /dev/random</span><span class="sxs-lookup"><span data-stu-id="bafce-1240">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="bafce-1241">实现 /proc/ [pid] / 装载 /proc/ [pid] / mountinfo 和 /proc/ [pid] / mountstats 文件</span><span class="sxs-lookup"><span data-stu-id="bafce-1241">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="bafce-1242">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1242">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="bafce-1243">生成 14901</span><span class="sxs-lookup"><span data-stu-id="bafce-1243">Build 14901</span></span>
<span data-ttu-id="bafce-1244">第一个预览体验内部版本的 Windows 10 周年更新发布的文章。</span><span class="sxs-lookup"><span data-stu-id="bafce-1244">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="bafce-1245">有关常规 Windows 上生成 14901 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1245">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1246">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1246">Fixed</span></span>
- <span data-ttu-id="bafce-1247">修复了尾随斜杠问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1247">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="bafce-1248">命令，如`$ mv a/c/ a/b/`现在工作</span><span class="sxs-lookup"><span data-stu-id="bafce-1248">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="bafce-1249">如果 Ubuntu 区域设置应设置为 Windows 区域设置安装现在会提示</span><span class="sxs-lookup"><span data-stu-id="bafce-1249">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="bafce-1250">Procfs 支持 ns 文件夹</span><span class="sxs-lookup"><span data-stu-id="bafce-1250">Procfs support for ns folder</span></span>
- <span data-ttu-id="bafce-1251">添加装载和卸载 tmpfs，procfs 和 sysfs 文件系统</span><span class="sxs-lookup"><span data-stu-id="bafce-1251">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="bafce-1252">[32 位 ABI 签名在] 修复 mknod</span><span class="sxs-lookup"><span data-stu-id="bafce-1252">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="bafce-1253">Unix 套接字移动调度模型</span><span class="sxs-lookup"><span data-stu-id="bafce-1253">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="bafce-1254">应遵循设置使用 setsockopt INET 套接字接收缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="bafce-1254">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="bafce-1255">实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志</span><span class="sxs-lookup"><span data-stu-id="bafce-1255">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="bafce-1256">Linux 进程 stdin/stdout 管道重定向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="bafce-1256">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="bafce-1257">允许在命令中的 bash-c 命令的管道</span><span class="sxs-lookup"><span data-stu-id="bafce-1257">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="bafce-1258">示例： > dir |bash-c"grep foo"</span><span class="sxs-lookup"><span data-stu-id="bafce-1258">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="bafce-1259">现在可以具有多个页面文件 (GH #538，#358) 的系统上安装 bash</span><span class="sxs-lookup"><span data-stu-id="bafce-1259">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="bafce-1260">默认 INET 套接字缓冲区大小应与匹配的默认 Ubuntu 安装程序</span><span class="sxs-lookup"><span data-stu-id="bafce-1260">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="bafce-1261">对齐到 listxattr xattr syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1261">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="bafce-1262">只能从 SIOCGIFCONF 返回有效的 IPv4 地址的接口</span><span class="sxs-lookup"><span data-stu-id="bafce-1262">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="bafce-1263">修复信号时由 ptrace 注入的默认操作</span><span class="sxs-lookup"><span data-stu-id="bafce-1263">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="bafce-1264">implement /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="bafce-1264">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="bafce-1265">还原在 sigreturn 上下文时使用计算机上下文寄存器值</span><span class="sxs-lookup"><span data-stu-id="bafce-1265">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="bafce-1266">这样可以解决问题 java 和 javac 已挂起的位置为一些用户</span><span class="sxs-lookup"><span data-stu-id="bafce-1266">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="bafce-1267">实现 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="bafce-1267">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1268">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1268">Syscall Support</span></span>
<span data-ttu-id="bafce-1269">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1270">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="bafce-1271">生成 14388 到 Windows 10 周年更新</span><span class="sxs-lookup"><span data-stu-id="bafce-1271">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="bafce-1272">有关常规 Windows 上生成 14388 信息请访问[Windows 博客](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1272">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1273">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1273">Fixed</span></span>
- <span data-ttu-id="bafce-1274">修复了准备的 Windows 10 周年更新上 8/2</span><span class="sxs-lookup"><span data-stu-id="bafce-1274">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="bafce-1275">有关 WSL 周年更新中的详细信息可以位于我们[博客](https://blogs.msdn.microsoft.com/wsl/)</span><span class="sxs-lookup"><span data-stu-id="bafce-1275">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="bafce-1276">生成 14376</span><span class="sxs-lookup"><span data-stu-id="bafce-1276">Build 14376</span></span>
<span data-ttu-id="bafce-1277">有关常规 Windows 上生成 14376 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1277">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1278">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1278">Fixed</span></span>
- <span data-ttu-id="bafce-1279">删除某些情况下其中的 apt-get 挂起 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="bafce-1279">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="bafce-1280">修复了在其中空装载了无法正确处理</span><span class="sxs-lookup"><span data-stu-id="bafce-1280">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="bafce-1281">修复了在其中 ramdisks 未正确安装</span><span class="sxs-lookup"><span data-stu-id="bafce-1281">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="bafce-1282">更改 unix 套接字接受以支持标志 (部分 GH #451)</span><span class="sxs-lookup"><span data-stu-id="bafce-1282">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="bafce-1283">固定的常见网络相关 bluescreen</span><span class="sxs-lookup"><span data-stu-id="bafce-1283">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="bafce-1284">修复出现蓝屏时访问 /proc/ [pid] / 任务 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="bafce-1284">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="bafce-1285">对于某些 pty 方案 (GH #488，#504) 的固定高 CPU 使用率</span><span class="sxs-lookup"><span data-stu-id="bafce-1285">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="bafce-1286">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1286">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="bafce-1287">生成 14371</span><span class="sxs-lookup"><span data-stu-id="bafce-1287">Build 14371</span></span>
<span data-ttu-id="bafce-1288">有关常规 Windows 上生成 14371 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1288">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1289">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1289">Fixed</span></span>
- <span data-ttu-id="bafce-1290">使用的 ptrace 时更正 SIGCHLD 和 wait() 计时争用</span><span class="sxs-lookup"><span data-stu-id="bafce-1290">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="bafce-1291">更正一些行为，当路径中含有尾随 / (GH #432)</span><span class="sxs-lookup"><span data-stu-id="bafce-1291">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="bafce-1292">修复了重命名/取消关联由于打开句柄子级而失败的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1292">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="bafce-1293">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1293">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="bafce-1294">生成 14366</span><span class="sxs-lookup"><span data-stu-id="bafce-1294">Build 14366</span></span>
<span data-ttu-id="bafce-1295">有关常规 Windows 上生成 14366 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1295">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1296">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1296">Fixed</span></span>
- <span data-ttu-id="bafce-1297">修复中通过符号链接的文件创建</span><span class="sxs-lookup"><span data-stu-id="bafce-1297">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="bafce-1298">用于 Python (GH 385) 添加了的 listxattr</span><span class="sxs-lookup"><span data-stu-id="bafce-1298">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="bafce-1299">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1299">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1300">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1300">Syscall Support</span></span>
-   <span data-ttu-id="bafce-1301">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1301">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1302">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1302">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="bafce-1303">版本 14361</span><span class="sxs-lookup"><span data-stu-id="bafce-1303">Build 14361</span></span>
<span data-ttu-id="bafce-1304">有关常规 Windows 内部版本 14361 信息请访问[Windows 博客](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1304">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1305">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1305">Fixed</span></span>
- <span data-ttu-id="bafce-1306">在中的 Bash 在 Ubuntu 上运行在 Windows 上时，DrvFs 现区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-1306">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="bafce-1307">用户可能 case.txt 和用例。TXT 上其/mnt/c 驱动器</span><span class="sxs-lookup"><span data-stu-id="bafce-1307">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="bafce-1308">Bash on Ubuntu 上 Windows 仅支持区分大小写。</span><span class="sxs-lookup"><span data-stu-id="bafce-1308">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="bafce-1309">当 Bash NTFS 的外部将报表文件正确，但可能发生意外的行为与 Windows 中的文件进行交互。</span><span class="sxs-lookup"><span data-stu-id="bafce-1309">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="bafce-1310">每个卷 (即 /mnt/c) 的根目录不区分大小写</span><span class="sxs-lookup"><span data-stu-id="bafce-1310">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="bafce-1311">可在处理这些文件在 Windows 中的详细信息[此处](https://support.microsoft.com/en-us/kb/100625)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1311">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="bafce-1312">大大增强 pty / tty 支持。</span><span class="sxs-lookup"><span data-stu-id="bafce-1312">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="bafce-1313">应用程序，如 TMUX 现在支持 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="bafce-1313">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="bafce-1314">不是始终创建用户帐户的固定的安装问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1314">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="bafce-1315">优化允许相当长参数列表的命令行参数结构。</span><span class="sxs-lookup"><span data-stu-id="bafce-1315">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="bafce-1316">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="bafce-1316">(GH #153)</span></span>
- <span data-ttu-id="bafce-1317">现在可以删除和 chmod read_only 文件从 DrvFs</span><span class="sxs-lookup"><span data-stu-id="bafce-1317">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="bafce-1318">修复了某些情况下，在终端挂起断开连接 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="bafce-1318">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="bafce-1319">chmod 和 chown 现在在 tty 设备上工作</span><span class="sxs-lookup"><span data-stu-id="bafce-1319">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="bafce-1320">允许连接到 0.0.0.0 和:: 为本地主机 (GH #388)</span><span class="sxs-lookup"><span data-stu-id="bafce-1320">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="bafce-1321">Sendmsg/recvmsg 现在处理的 IO 向量长度 > 1 (部分 GH #376)</span><span class="sxs-lookup"><span data-stu-id="bafce-1321">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="bafce-1322">用户可以立即选择退出自动生成的主机文件 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="bafce-1322">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="bafce-1323">自动与 Linux 为 NT 区域设置的区域设置匹配 (GH #11) 安装过程</span><span class="sxs-lookup"><span data-stu-id="bafce-1323">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="bafce-1324">添加 /proc/sys/vm/swappiness 文件 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="bafce-1324">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="bafce-1325">跟踪来现在正常退出</span><span class="sxs-lookup"><span data-stu-id="bafce-1325">strace now exits correctly</span></span>
- <span data-ttu-id="bafce-1326">允许通过 /proc/self/fd (GH #222) 重新打开管道</span><span class="sxs-lookup"><span data-stu-id="bafce-1326">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="bafce-1327">隐藏 %LOCALAPPDATA%\lxss 从 DrvFs (GH #270) 下的目录</span><span class="sxs-lookup"><span data-stu-id="bafce-1327">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="bafce-1328">更好地处理 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="bafce-1328">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="bafce-1329">命令，如"bash ~-c ls"现在支持 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="bafce-1329">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="bafce-1330">套接字现在当 epoll 读取期间关闭 (GH #271) 可用</span><span class="sxs-lookup"><span data-stu-id="bafce-1330">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="bafce-1331">lxrun / 卸载更好地删除文件和文件夹</span><span class="sxs-lookup"><span data-stu-id="bafce-1331">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="bafce-1332">已更正的 ps-f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="bafce-1332">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="bafce-1333">改进了对 x11 支持应用程序，例如 xEmacs (GH #481)</span><span class="sxs-lookup"><span data-stu-id="bafce-1333">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="bafce-1334">已更新初始线程堆栈大小，使之与默认 Ubuntu 设置和向 get_rlimit syscall (GH #172，#258) 正确报告大小</span><span class="sxs-lookup"><span data-stu-id="bafce-1334">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="bafce-1335">改进了 pico 进程映像名称 （例如，用于审核） 的报告</span><span class="sxs-lookup"><span data-stu-id="bafce-1335">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="bafce-1336">实现的 /proc/mountinfo df 命令</span><span class="sxs-lookup"><span data-stu-id="bafce-1336">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="bafce-1337">修复子名称的符号链接错误代码。</span><span class="sxs-lookup"><span data-stu-id="bafce-1337">Fixed symlink error code for child name .</span></span> <span data-ttu-id="bafce-1338">和...</span><span class="sxs-lookup"><span data-stu-id="bafce-1338">and ..</span></span>
- <span data-ttu-id="bafce-1339">其他改进 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1339">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1340">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1340">Syscall Support</span></span>
<span data-ttu-id="bafce-1341">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1341">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1342">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1342">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="bafce-1343">生成 14352</span><span class="sxs-lookup"><span data-stu-id="bafce-1343">Build 14352</span></span>
<span data-ttu-id="bafce-1344">有关常规 Windows 上生成 14352 信息请访问[Windows 博客](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1344">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1345">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1345">Fixed</span></span>
- <span data-ttu-id="bafce-1346">其中较大的文件是未下载 / 正确创建的已修复的问题。</span><span class="sxs-lookup"><span data-stu-id="bafce-1346">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="bafce-1347">这应取消阻止 npm 和其他方案 （GH #3，GH #313）</span><span class="sxs-lookup"><span data-stu-id="bafce-1347">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="bafce-1348">删除某些情况下，套接字会挂起</span><span class="sxs-lookup"><span data-stu-id="bafce-1348">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="bafce-1349">更正了一些的 ptrace 错误</span><span class="sxs-lookup"><span data-stu-id="bafce-1349">Corrected some ptrace errors</span></span>
- <span data-ttu-id="bafce-1350">已修复的问题 WSL 允许文件名长度超过 255 个字符</span><span class="sxs-lookup"><span data-stu-id="bafce-1350">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="bafce-1351">改进了对非英语字符支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1351">Improved support for non-English characters</span></span>
- <span data-ttu-id="bafce-1352">添加当前 Windows 时区数据并将设置为默认值</span><span class="sxs-lookup"><span data-stu-id="bafce-1352">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="bafce-1353">唯一的设备 id 的每个装入点 （jre 修复 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="bafce-1353">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="bafce-1354">更正问题与包含的路径"。"</span><span class="sxs-lookup"><span data-stu-id="bafce-1354">Correct issue with paths containing “.”</span></span> <span data-ttu-id="bafce-1355">和"."</span><span class="sxs-lookup"><span data-stu-id="bafce-1355">and “..”</span></span>
- <span data-ttu-id="bafce-1356">添加了先进先出的支持 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="bafce-1356">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="bafce-1357">Resolv.conf，与本机 Ubuntu 格式匹配的更新的格式</span><span class="sxs-lookup"><span data-stu-id="bafce-1357">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="bafce-1358">一些 procfs 清理</span><span class="sxs-lookup"><span data-stu-id="bafce-1358">Some procfs cleanup</span></span>
- <span data-ttu-id="bafce-1359">管理员控制台 (GH #18) 的已启用的 ping</span><span class="sxs-lookup"><span data-stu-id="bafce-1359">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1360">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1360">Syscall Support</span></span>
<span data-ttu-id="bafce-1361">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1361">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1362">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1362">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="bafce-1363">生成 14342</span><span class="sxs-lookup"><span data-stu-id="bafce-1363">Build 14342</span></span>
<span data-ttu-id="bafce-1364">常规的 Windows 上的信息生成 14342 [Windows 博客](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1364">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="bafce-1365">VolFs 和 DriveFs 信息可能位于[WSL 博客](https://blogs.msdn.microsoft.com/wsl)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1365">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="bafce-1366">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1366">Fixed</span></span>
- <span data-ttu-id="bafce-1367">修复 Windows 用户的用户名具有 Unicode 字符时安装的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1367">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="bafce-1368">默认情况下，首次运行时现在提供常见问题解答中的 apt-get 更新 udev 解决方法</span><span class="sxs-lookup"><span data-stu-id="bafce-1368">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="bafce-1369">启用 DriveFs 中的符号链接 (/mnt/<drive>) 目录</span><span class="sxs-lookup"><span data-stu-id="bafce-1369">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="bafce-1370">符号链接现在 DriveFs 和 VolFs 之间工作</span><span class="sxs-lookup"><span data-stu-id="bafce-1370">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="bafce-1371">分析问题的寻址顶部级别路径： ls。 / / 现在按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="bafce-1371">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="bafce-1372">npm 安装上 DriveFs 和-g 选项目前正在处理</span><span class="sxs-lookup"><span data-stu-id="bafce-1372">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="bafce-1373">修复了阻止 PHP 服务器启动的问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1373">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="bafce-1374">更新的默认环境值，例如 $PATH 以更接近匹配本机 Ubuntu</span><span class="sxs-lookup"><span data-stu-id="bafce-1374">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="bafce-1375">在 Windows 更新 apt 包缓存中添加一个每周维护任务</span><span class="sxs-lookup"><span data-stu-id="bafce-1375">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="bafce-1376">ELF 标头验证修复的问题，WSL 现在支持所有 Melkor 选项</span><span class="sxs-lookup"><span data-stu-id="bafce-1376">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="bafce-1377">Zsh shell 是功能</span><span class="sxs-lookup"><span data-stu-id="bafce-1377">Zsh shell is functional</span></span>
- <span data-ttu-id="bafce-1378">现在支持预编译转到二进制文件</span><span class="sxs-lookup"><span data-stu-id="bafce-1378">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="bafce-1379">在首次运行 Bash.exe 上提示现已正确本地化</span><span class="sxs-lookup"><span data-stu-id="bafce-1379">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="bafce-1380">/proc/meminfo 现在返回正确的信息</span><span class="sxs-lookup"><span data-stu-id="bafce-1380">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="bafce-1381">套接字 VFS 中现在支持</span><span class="sxs-lookup"><span data-stu-id="bafce-1381">Sockets now supported in VFS</span></span>
- <span data-ttu-id="bafce-1382">/dev 现在已装载为 tempfs</span><span class="sxs-lookup"><span data-stu-id="bafce-1382">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="bafce-1383">现在支持先进先出</span><span class="sxs-lookup"><span data-stu-id="bafce-1383">Fifo now supported</span></span>
- <span data-ttu-id="bafce-1384">多核系统现在/proc/cpuinfo 中正确显示</span><span class="sxs-lookup"><span data-stu-id="bafce-1384">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="bafce-1385">其他改进和下载在首次运行期间的错误消息</span><span class="sxs-lookup"><span data-stu-id="bafce-1385">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="bafce-1386">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="bafce-1386">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="bafce-1387">支持的 syscall 下面的列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-1387">Supported syscall list below.</span></span>
- <span data-ttu-id="bafce-1388">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1388">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="bafce-1389">已知问题</span><span class="sxs-lookup"><span data-stu-id="bafce-1389">Known Issues</span></span>
- <span data-ttu-id="bafce-1390">未解决...</span><span class="sxs-lookup"><span data-stu-id="bafce-1390">Not resolving ‘..’</span></span> <span data-ttu-id="bafce-1391">在某些情况下 DriveFs 上正确</span><span class="sxs-lookup"><span data-stu-id="bafce-1391">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1392">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1392">Syscall Support</span></span>
<span data-ttu-id="bafce-1393">下面是一系列新的或增强 syscall WSL 中具有一些实现的。</span><span class="sxs-lookup"><span data-stu-id="bafce-1393">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="bafce-1394">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1394">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="bafce-1395">生成 14332</span><span class="sxs-lookup"><span data-stu-id="bafce-1395">Build 14332</span></span>

<span data-ttu-id="bafce-1396">有关常规 Windows 上生成 14332 信息请访问[Windows 博客](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1396">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="bafce-1397">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1397">Fixed</span></span>
- <span data-ttu-id="bafce-1398">更好地 resolv.conf 生成包括确定优先级 DNS 条目</span><span class="sxs-lookup"><span data-stu-id="bafce-1398">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="bafce-1399">移动文件和目录之间 /mnt 和非问题-/ mnt 驱动器</span><span class="sxs-lookup"><span data-stu-id="bafce-1399">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="bafce-1400">现在可以使用符号链接创建的 tar 文件</span><span class="sxs-lookup"><span data-stu-id="bafce-1400">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="bafce-1401">添加了的默认 /run/lock 目录上创建实例</span><span class="sxs-lookup"><span data-stu-id="bafce-1401">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="bafce-1402">更新 /dev/null 时要返回正确的状态信息</span><span class="sxs-lookup"><span data-stu-id="bafce-1402">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="bafce-1403">下载期间首次运行时的其他错误</span><span class="sxs-lookup"><span data-stu-id="bafce-1403">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="bafce-1404">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="bafce-1404">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="bafce-1405">支持的 syscall 下面的列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-1405">Supported syscall list below.</span></span>
- <span data-ttu-id="bafce-1406">其他改进 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1406">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1407">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1407">Syscall Support</span></span>
<span data-ttu-id="bafce-1408">下面是在 WSL 中具有一些实现新 syscall。</span><span class="sxs-lookup"><span data-stu-id="bafce-1408">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="bafce-1409">在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1409">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="bafce-1410">内部版本 14328</span><span class="sxs-lookup"><span data-stu-id="bafce-1410">Build 14328</span></span>

<span data-ttu-id="bafce-1411">有关常规 Windows 上生成 14332 信息请访问[Windows 博客](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1411">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="bafce-1412">新功能</span><span class="sxs-lookup"><span data-stu-id="bafce-1412">New Features</span></span>
* <span data-ttu-id="bafce-1413">现在支持 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="bafce-1413">Now support Linux users.</span></span>  <span data-ttu-id="bafce-1414">在 Windows 上的 Ubuntu 上安装 Bash 会提示创建的 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="bafce-1414">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="bafce-1415">有关详细信息，请访问 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="bafce-1415">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="bafce-1416">主机名现在设置为 Windows 计算机名称，没有更多 @localhost</span><span class="sxs-lookup"><span data-stu-id="bafce-1416">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="bafce-1417">有关详细信息内部版本 14328，请访问： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="bafce-1417">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="bafce-1418">固定</span><span class="sxs-lookup"><span data-stu-id="bafce-1418">Fixed</span></span>
* <span data-ttu-id="bafce-1419">非 /mnt/ 的符号链接改进<drive>文件</span><span class="sxs-lookup"><span data-stu-id="bafce-1419">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="bafce-1420">npm 安装现在的工作原理</span><span class="sxs-lookup"><span data-stu-id="bafce-1420">npm install now works</span></span>
    * <span data-ttu-id="bafce-1421">jdk / 现在可安装的 jre 使用找到的说明[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)。</span><span class="sxs-lookup"><span data-stu-id="bafce-1421">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="bafce-1422">已知问题： 对于 Windows 装载符号链接不起作用。</span><span class="sxs-lookup"><span data-stu-id="bafce-1422">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="bafce-1423">可在更高版本中的功能</span><span class="sxs-lookup"><span data-stu-id="bafce-1423">Functionality will be available in a later build</span></span>
* <span data-ttu-id="bafce-1424">top 和 htop 现在会显示</span><span class="sxs-lookup"><span data-stu-id="bafce-1424">top and htop now display</span></span>
* <span data-ttu-id="bafce-1425">对于某些其他错误消息安装失败</span><span class="sxs-lookup"><span data-stu-id="bafce-1425">Additional error messages for some install failures</span></span>
* <span data-ttu-id="bafce-1426">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="bafce-1426">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="bafce-1427">支持的 syscall 下面的列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-1427">Supported syscall list below.</span></span>
* <span data-ttu-id="bafce-1428">其他改进 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="bafce-1428">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="bafce-1429">支持 Syscall</span><span class="sxs-lookup"><span data-stu-id="bafce-1429">Syscall Support</span></span>
<span data-ttu-id="bafce-1430">下面是在 WSL 中有一些实现 syscall 的列表。</span><span class="sxs-lookup"><span data-stu-id="bafce-1430">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="bafce-1431">在此列表上的 Syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。</span><span class="sxs-lookup"><span data-stu-id="bafce-1431">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
