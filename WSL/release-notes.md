---
title: 适用于 Linux 的 Windows 子系统发行说明
description: 适用于 Linux 的 Windows 子系统的发行说明。  每周更新。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 63c0e14dab73faf7f835e9ae1eb23eb490b13c44
ms.sourcegitcommit: 48ca05ce1ac8bf35408af3bc2a2b92a43adba0af
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/30/2019
ms.locfileid: "73166657"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="58d22-105">适用于 Linux 的 Windows 子系统发行说明</span><span class="sxs-lookup"><span data-stu-id="58d22-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19013"></a><span data-ttu-id="58d22-106">内部版本 19013</span><span class="sxs-lookup"><span data-stu-id="58d22-106">Build 19013</span></span>
<span data-ttu-id="58d22-107">有关内部版本 19013 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-107">For general Windows information on build 19013 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/29/announcing-windows-10-insider-preview-build-19013/).</span></span>

* <span data-ttu-id="58d22-108">[WSL2] 提高 WSL 实用工具 VM 的内存性能。</span><span class="sxs-lookup"><span data-stu-id="58d22-108">[WSL2] Improve memory performance of WSL utility VM.</span></span> <span data-ttu-id="58d22-109">不再处于使用状态的内存将释放回主机。</span><span class="sxs-lookup"><span data-stu-id="58d22-109">Memory that is no longer in use will be freed back to the host.</span></span>
* <span data-ttu-id="58d22-110">[WSL2] 将内核版本更新到 4.19.79。</span><span class="sxs-lookup"><span data-stu-id="58d22-110">[WSL2] Update kernel version to 4.19.79.</span></span> <span data-ttu-id="58d22-111">（添加 CONFIG_HIGH_RES_TIMERS、CONFIG_TASK_XACCT、CONFIG_TASK_IO_ACCOUNTING、CONFIG_SCHED_HRTICK 和 CONFIG_BRIDGE_VLAN_FILTERING）。</span><span class="sxs-lookup"><span data-stu-id="58d22-111">(add CONFIG_HIGH_RES_TIMERS, CONFIG_TASK_XACCT, CONFIG_TASK_IO_ACCOUNTING, CONFIG_SCHED_HRTICK, and CONFIG_BRIDGE_VLAN_FILTERING).</span></span>
* <span data-ttu-id="58d22-112">[WSL2] 修复了输入中继，以处理 stdin 为未关闭管道句柄的情况 [GH 4424]</span><span class="sxs-lookup"><span data-stu-id="58d22-112">[WSL2] Fix input relay to handle cases where stdin is a pipe handle that is not closed [GH 4424]</span></span>
* <span data-ttu-id="58d22-113">检查 \\\\wsl$ 是否不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-113">Make the check for \\\\wsl$ case-insensitive.</span></span>
```
[wsl2]
pageReporting = <bool>    # Enable or disable the free memory page reporting feature (default true).
idleThreshold = <integer> # Set the idle threshold for memory compaction, 0 disables the feature (default 1).
```

## <a name="build-19002"></a><span data-ttu-id="58d22-114">版本 19002</span><span class="sxs-lookup"><span data-stu-id="58d22-114">Build 19002</span></span>
<span data-ttu-id="58d22-115">有关版本 19002 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-115">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="58d22-116">[WSL] 解决了有关处理某些 Unicode 字符的问题： https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="58d22-116">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="58d22-117">[WSL] 解决了在版本到版本升级后立即启动时可能会注销发行版的罕见情况。</span><span class="sxs-lookup"><span data-stu-id="58d22-117">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="58d22-118">[WSL] 解决了 wsl.exe --shutdown 的以下小问题：无法取消实例空闲计时器。</span><span class="sxs-lookup"><span data-stu-id="58d22-118">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="58d22-119">内部版本 18995</span><span class="sxs-lookup"><span data-stu-id="58d22-119">Build 18995</span></span>
<span data-ttu-id="58d22-120">有关内部版本 18995 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-120">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="58d22-121">[WSL2] 修复了 DrvFs 装载在某项操作被中断（例如 ctrl-c）后失效的问题 [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="58d22-121">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="58d22-122">[WSL2] 修复了处理极大型 hvsocket 消息的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="58d22-122">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="58d22-123">[WSL2] 修复了当 stdin 为文件时互操作出现的问题 [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="58d22-123">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="58d22-124">[WSL2] 修复了当遇到意外网络状态时服务崩溃的问题 [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="58d22-124">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="58d22-125">[WSL2] 在当前进程没有环境变量的情况下从互操作服务器查询发行版名称</span><span class="sxs-lookup"><span data-stu-id="58d22-125">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="58d22-126">[WSL2] 修复了当 stdin 为文件时互操作出现的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-126">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="58d22-127">[WSL2] 将 Linux 内核版本更新到 4.19.72</span><span class="sxs-lookup"><span data-stu-id="58d22-127">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="58d22-128">[WSL2] 添加了通过 .wslconfig 指定其他内核命令行参数的功能</span><span class="sxs-lookup"><span data-stu-id="58d22-128">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments
```

## <a name="build-18990"></a><span data-ttu-id="58d22-129">版本 18990</span><span class="sxs-lookup"><span data-stu-id="58d22-129">Build 18990</span></span>
<span data-ttu-id="58d22-130">有关版本 18990 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-130">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="58d22-131">提高 \\\\wsl$ 中目录列表的性能</span><span class="sxs-lookup"><span data-stu-id="58d22-131">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="58d22-132">[WSL2] 注入额外的启动熵 [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="58d22-132">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="58d22-133">[WSL2] 修复使用 su/sudo 时的 Windows 互操作 [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="58d22-133">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="58d22-134">内部版本 18980</span><span class="sxs-lookup"><span data-stu-id="58d22-134">Build 18980</span></span>
<span data-ttu-id="58d22-135">有关内部版本 18980 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-135">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="58d22-136">修复拒绝 FILE_READ_DATA 的读取符号链接。</span><span class="sxs-lookup"><span data-stu-id="58d22-136">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="58d22-137">这包括 Windows 为了实现后向兼容而创建的所有符号链接（例如“C:\Document and Settings”），以及用户配置文件目录中的一些符号链接。</span><span class="sxs-lookup"><span data-stu-id="58d22-137">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="58d22-138">使意外的文件系统状态变得不严重 [GH 4334、4305]</span><span class="sxs-lookup"><span data-stu-id="58d22-138">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="58d22-139">[WSL2] 添加当 CPU/固件支持虚拟化时对 arm64 的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-139">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="58d22-140">[WSL2] 允许无特权用户查看内核日志</span><span class="sxs-lookup"><span data-stu-id="58d22-140">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="58d22-141">[WSL2] 修复关闭 stdout/stderr 套接字后的输出中继 [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="58d22-141">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="58d22-142">[WSL2] 支持电池和交流适配器直通</span><span class="sxs-lookup"><span data-stu-id="58d22-142">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="58d22-143">[WSL2] 将 Linux 内核更新到 4.19.67</span><span class="sxs-lookup"><span data-stu-id="58d22-143">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="58d22-144">添加在 /etc/wsl.conf 中设置默认用户名的功能：</span><span class="sxs-lookup"><span data-stu-id="58d22-144">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="58d22-145">内部版本 18975</span><span class="sxs-lookup"><span data-stu-id="58d22-145">Build 18975</span></span>
<span data-ttu-id="58d22-146">有关内部版本 18975 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-146">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="58d22-147">[WSL2] 修复大量 localhost 可靠性问题 [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="58d22-147">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="58d22-148">内部版本 18970</span><span class="sxs-lookup"><span data-stu-id="58d22-148">Build 18970</span></span>
<span data-ttu-id="58d22-149">有关内部版本 18970 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-149">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="58d22-150">[WSL2] 当系统从睡眠状态恢复时，使时间与主机时间同步 [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="58d22-150">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="58d22-151">[WSL2] 在可能的情况下，在 Windows 卷上创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="58d22-151">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="58d22-152">[WSL2] 在 UTS、IPC、PID 和 Mount 命名空间中创建分发版。</span><span class="sxs-lookup"><span data-stu-id="58d22-152">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="58d22-153">[WSL2] 修复当服务器直接绑定到 localhost 时的 localhost 端口中继 [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="58d22-153">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="58d22-154">[WSL2] 修复重定向输出时的 interop [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="58d22-154">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="58d22-155">[WSL2] 支持转换绝对 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="58d22-155">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="58d22-156">[WSL2] 将内核更新到 4.19.59</span><span class="sxs-lookup"><span data-stu-id="58d22-156">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="58d22-157">[WSL2] 正确设置 eth0 的子网掩码。</span><span class="sxs-lookup"><span data-stu-id="58d22-157">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="58d22-158">[WSL2] 发出退出事件信号时更改逻辑，以中断控制台工作线程循环。</span><span class="sxs-lookup"><span data-stu-id="58d22-158">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="58d22-159">[WSL2] 分发版未运行时弹出分发版 VHD。</span><span class="sxs-lookup"><span data-stu-id="58d22-159">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="58d22-160">[WSL2] 修复配置分析库以正确处理空值。</span><span class="sxs-lookup"><span data-stu-id="58d22-160">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="58d22-161">[WSL2] 通过创建跨分发版装入点来支持 Docker Desktop。</span><span class="sxs-lookup"><span data-stu-id="58d22-161">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="58d22-162">分发版可以通过将以下行添加到 /etc/wsl.conf 文件来启用此行为：</span><span class="sxs-lookup"><span data-stu-id="58d22-162">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="58d22-163">内部版本 18945</span><span class="sxs-lookup"><span data-stu-id="58d22-163">Build 18945</span></span>
<span data-ttu-id="58d22-164">有关内部版本 18945 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-164">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-165">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-165">WSL</span></span>
* <span data-ttu-id="58d22-166">[WSL2] 允许侦听可使用 localhost:port 通过主机访问的 WSL2 中的 TCP 套接字</span><span class="sxs-lookup"><span data-stu-id="58d22-166">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="58d22-167">[WSL2] 修复安装/转换失败和其他诊断，以跟踪将来的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="58d22-167">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="58d22-168">[WSL2] 改善 WSL2 网络问题的诊断</span><span class="sxs-lookup"><span data-stu-id="58d22-168">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="58d22-169">[WSL2] 将内核版本更新到 4.19.55</span><span class="sxs-lookup"><span data-stu-id="58d22-169">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="58d22-170">[WSL2] 使用 Docker 所需的配置选项更新了内核 [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="58d22-170">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="58d22-171">[WSL2] 增加分配给轻型实用程序 VM 的 CPU 数目，使其与主机相同（以前，内核配置中的 CONFIG_NR_CPUS 将数目限制为 8 个）[GH 4137]</span><span class="sxs-lookup"><span data-stu-id="58d22-171">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="58d22-172">[WSL2] 为 WSL2 轻型 VM 创建交换文件</span><span class="sxs-lookup"><span data-stu-id="58d22-172">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="58d22-173">[WSL2] 允许通过 \\\\wsl$\\distro（例如 sshfs）显示用户装入点 [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="58d22-173">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="58d22-174">[WSL2] 改善 9p 文件系统的性能</span><span class="sxs-lookup"><span data-stu-id="58d22-174">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="58d22-175">[WSL2] 确保 VHD ACL 不会无限增长 [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="58d22-175">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="58d22-176">[WSL2] 更新内核配置以支持 squashfs 和 xt_conntrack [GH 4107、4123]</span><span class="sxs-lookup"><span data-stu-id="58d22-176">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="58d22-177">[WSL2] 修复 interop.enabled /etc/wsl.conf 选项 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="58d22-177">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="58d22-178">[WSL2] 如果文件系统不支持 EA，则返回 ENOTSUP</span><span class="sxs-lookup"><span data-stu-id="58d22-178">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="58d22-179">[WSL2] 修复 \\\\wsl$ 时 CopyFile 挂起的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-179">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="58d22-180">将默认 umask 切换为 0022，并将 filesystem.umask 设置添加到 /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="58d22-180">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="58d22-181">修复 wslpath 以正确解析符号链接，这是19h1 中的回归 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="58d22-181">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="58d22-182">引入 %UserProfile%\\.wslconfig 文件用于调整 WSL2 设置</span><span class="sxs-lookup"><span data-stu-id="58d22-182">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
```
[wsl2]
kernel=<path>              # An absolute Windows path to a custom Linux kernel.
memory=<size>              # How much memory to assign to the WSL2 VM.
processors=<number>        # How many processors to assign to the WSL2 VM.
swap=<size>                # How much swap space to add to the WSL2 VM. 0 for no swap file.
swapFile=<path>            # An absolute Windows path to the swap vhd.
localhostForwarding=<bool> # Boolean specifying if ports bound to wildcard or localhost in the WSL2 VM should be connectable from the host via localhost:port (default true).

# <path> entries must be absolute Windows paths with escaped backslashes, for example C:\\Users\\Ben\\kernel
# <size> entries must be size followed by unit, for example 8GB or 512MB
```

## <a name="build-18917"></a><span data-ttu-id="58d22-183">内部版本 18917</span><span class="sxs-lookup"><span data-stu-id="58d22-183">Build 18917</span></span>
<span data-ttu-id="58d22-184">有关内部版本 18917 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-184">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-185">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-185">WSL</span></span>
* <span data-ttu-id="58d22-186">WSL 2 现已推出！</span><span class="sxs-lookup"><span data-stu-id="58d22-186">WSL 2 is now available!</span></span> <span data-ttu-id="58d22-187">有关更多详细信息，请参阅[博客](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-187">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="58d22-188">修复一个回归问题：无法通过符号链接启动 Windows 进程 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="58d22-188">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="58d22-189">将 wsl.exe --list --verbose、wsl.exe --list --quiet 和 wsl.exe --import --version 选项添加到 wsl.exe</span><span class="sxs-lookup"><span data-stu-id="58d22-189">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="58d22-190">添加 wsl.exe --shutdown 选项</span><span class="sxs-lookup"><span data-stu-id="58d22-190">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="58d22-191">Plan 9：允许打开目录以使写入成功</span><span class="sxs-lookup"><span data-stu-id="58d22-191">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="58d22-192">内部版本 18890</span><span class="sxs-lookup"><span data-stu-id="58d22-192">Build 18890</span></span>
<span data-ttu-id="58d22-193">有关内部版本 18890 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-193">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-194">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-194">WSL</span></span>
* <span data-ttu-id="58d22-195">非阻塞套接字泄露 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="58d22-195">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="58d22-196">在终端中输入 EOF 可能会阻塞后续读取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="58d22-196">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="58d22-197">更新 resolv.conf 标头以引用 wsl.conf [在 GH 3928 中介绍]</span><span class="sxs-lookup"><span data-stu-id="58d22-197">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="58d22-198">epoll delete 代码中的死锁 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="58d22-198">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="58d22-199">处理 --import 和 –export 的参数中的空格 [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="58d22-199">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="58d22-200">无法正常扩展 mmap 的文件 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="58d22-200">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="58d22-201">修复了 ARM64 \\\\wsl$ 访问不正常的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-201">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="58d22-202">为 wsl.exe 添加更好的默认图标</span><span class="sxs-lookup"><span data-stu-id="58d22-202">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="58d22-203">内部版本 18342</span><span class="sxs-lookup"><span data-stu-id="58d22-203">Build 18342</span></span>
<span data-ttu-id="58d22-204">有关内部版本 18342 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-204">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-205">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-205">WSL</span></span>
* <span data-ttu-id="58d22-206">我们添加了相应的功能，使用户能够从 Windows 访问 WSL 分发版中的 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-206">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="58d22-207">可以通过命令行访问这些文件，此外，文件资源管理器、VSCode 等 Windows 应用可与这些文件交互。</span><span class="sxs-lookup"><span data-stu-id="58d22-207">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="58d22-208">通过导航到 \\\\wsl$\\<分发版名称> 访问文件，或通过导航到 \\\\wsl$ 来查看正在运行的分发版列表</span><span class="sxs-lookup"><span data-stu-id="58d22-208">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="58d22-209">添加额外的 CPU 信息标记，并修复 Cpus_allowed[_list] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="58d22-209">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="58d22-210">支持从非领先线程执行 [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="58d22-210">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="58d22-211">将配置更新失败视为非严重错误 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="58d22-211">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="58d22-212">更新 binfmt 以正确处理偏移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="58d22-212">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="58d22-213">为 Plan 9 启用映射网络驱动器 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="58d22-213">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="58d22-214">支持对绑定载入点执行“Windows -> Linux”和“Linux -> Windows”路径转换</span><span class="sxs-lookup"><span data-stu-id="58d22-214">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="58d22-215">为以只读方式打开的文件中的映射创建只读节</span><span class="sxs-lookup"><span data-stu-id="58d22-215">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="58d22-216">内部版本 18334</span><span class="sxs-lookup"><span data-stu-id="58d22-216">Build 18334</span></span>
<span data-ttu-id="58d22-217">有关内部版本 18334 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-217">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-218">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-218">WSL</span></span>
* <span data-ttu-id="58d22-219">重新设计 Windows 时区映射到 Linux 时区的方式 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="58d22-219">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="58d22-220">修复内存泄漏，并添加新的字符串转换函数 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="58d22-220">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="58d22-221">不包含任何线程的线程组上的 SIGCONT 是一个 no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="58d22-221">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="58d22-222">在 /proc/self/fd 中正确显示套接字和 epoll 文件描述符</span><span class="sxs-lookup"><span data-stu-id="58d22-222">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="58d22-223">内部版本 18305</span><span class="sxs-lookup"><span data-stu-id="58d22-223">Build 18305</span></span>
<span data-ttu-id="58d22-224">有关内部版本 18305 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-224">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-225">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-225">WSL</span></span>
* <span data-ttu-id="58d22-226">当主线程退出时，pthreads 失去对文件的访问权限 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="58d22-226">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="58d22-227">除非有必要，否则 TIOCSCTTY 应忽略“force”参数 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="58d22-227">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="58d22-228">改善 wsl.exe 命令行，并添加导入/导出功能。</span><span class="sxs-lookup"><span data-stu-id="58d22-228">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="58d22-229">内部版本 18277</span><span class="sxs-lookup"><span data-stu-id="58d22-229">Build 18277</span></span>
<span data-ttu-id="58d22-230">有关内部版本 18277 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-230">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-231">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-231">WSL</span></span>
* <span data-ttu-id="58d22-232">修复内部版本 18272 中引入的“不支持此类接口”错误 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="58d22-232">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="58d22-233">忽略 umount syscall 的 MNT_FORCE 标志 [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="58d22-233">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="58d22-234">切换 WSL interop 以使用官方的 CreatePseudoConsole API</span><span class="sxs-lookup"><span data-stu-id="58d22-234">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="58d22-235">FUTEX_WAIT 重启时不保留超时值</span><span class="sxs-lookup"><span data-stu-id="58d22-235">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="58d22-236">内部版本 18272</span><span class="sxs-lookup"><span data-stu-id="58d22-236">Build 18272</span></span>
<span data-ttu-id="58d22-237">有关内部版本 18272 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-237">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-238">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-238">WSL</span></span>
* <span data-ttu-id="58d22-239">**警告：** 此版本中存在一个导致 WSL 不可操作的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-239">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="58d22-240">尝试启动分发版时，会看到“不支持此类接口”错误。</span><span class="sxs-lookup"><span data-stu-id="58d22-240">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="58d22-241">该问题已修复，下周发布的 Insider Fast 内部版本将会应用修复程序。</span><span class="sxs-lookup"><span data-stu-id="58d22-241">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="58d22-242">如果已安装此内部版本，可以使用“设置”->“更新和安全”>“恢复”中的“回退到 Windows 10 的上一个版本”回滚到上一 Windows 内部版本。</span><span class="sxs-lookup"><span data-stu-id="58d22-242">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="58d22-243">内部版本 18267</span><span class="sxs-lookup"><span data-stu-id="58d22-243">Build 18267</span></span>
<span data-ttu-id="58d22-244">有关内部版本 18267 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-244">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-245">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-245">WSL</span></span>
* <span data-ttu-id="58d22-246">修复 zombie 进程不会回收，而是无限期保留的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-246">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="58d22-247">如果错误消息超过最大长度，WslRegisterDistribution 将会挂起 [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="58d22-247">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="58d22-248">允许 fsync 针对 DrvFs 上的只读文件成功运行 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="58d22-248">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="58d22-249">在内部创建符号链接之前，确保 /bin 和 /sbin 目录存在 [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="58d22-249">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="58d22-250">为 WSL 实例添加了实例终止超时机制。</span><span class="sxs-lookup"><span data-stu-id="58d22-250">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="58d22-251">超时目前设置为 15 秒，这意味着，实例将在上一个 WSL 进程退出 15 秒后终止。</span><span class="sxs-lookup"><span data-stu-id="58d22-251">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="58d22-252">若要立即终止分发版，请使用：</span><span class="sxs-lookup"><span data-stu-id="58d22-252">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="58d22-253">内部版本 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="58d22-253">Build 17763 (1809)</span></span>
<span data-ttu-id="58d22-254">有关内部版本 17763 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-254">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-255">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-255">WSL</span></span>
* <span data-ttu-id="58d22-256">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="58d22-256">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="58d22-257">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="58d22-257">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="58d22-258">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="58d22-258">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="58d22-259">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="58d22-259">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="58d22-260">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="58d22-260">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="58d22-261">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="58d22-261">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="58d22-262">修复多个 AF_UNIX 相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="58d22-262">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="58d22-263">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="58d22-263">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="58d22-264">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="58d22-264">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="58d22-265">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="58d22-265">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="58d22-266">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-266">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="58d22-267">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="58d22-267">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="58d22-268">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="58d22-268">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="58d22-269">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="58d22-269">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="58d22-270">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="58d22-270">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="58d22-271">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="58d22-271">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="58d22-272">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="58d22-272">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="58d22-273">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="58d22-273">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="58d22-274">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="58d22-274">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="58d22-275">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="58d22-275">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="58d22-276">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="58d22-276">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="58d22-277">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-277">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="58d22-278">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="58d22-278">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="58d22-279">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="58d22-279">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="58d22-280">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="58d22-280">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="58d22-281">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="58d22-281">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="58d22-282">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="58d22-282">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="58d22-283">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="58d22-283">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="58d22-284">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-284">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="58d22-285">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="58d22-285">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="58d22-286">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-286">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="58d22-287">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="58d22-287">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="58d22-288">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="58d22-288">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="58d22-289">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="58d22-289">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="58d22-290">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="58d22-290">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="58d22-291">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="58d22-291">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="58d22-292">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="58d22-292">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="58d22-293">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="58d22-293">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="58d22-294">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="58d22-294">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="58d22-295">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="58d22-295">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="58d22-296">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="58d22-296">[GH 2712]</span></span>
* <span data-ttu-id="58d22-297">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-297">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="58d22-298">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="58d22-298">[GH 3020]</span></span>
* <span data-ttu-id="58d22-299">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="58d22-299">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="58d22-300">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="58d22-300">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="58d22-301">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="58d22-301">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="58d22-302">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-302">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="58d22-303">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="58d22-303">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="58d22-304">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="58d22-304">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="58d22-305">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-305">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="58d22-306">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="58d22-306">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="58d22-307">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-307">Limited support for dmesg.</span></span> <span data-ttu-id="58d22-308">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="58d22-308">Applications can now log to dmesg.</span></span> <span data-ttu-id="58d22-309">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="58d22-309">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="58d22-310">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-310">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="58d22-311">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="58d22-311">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="58d22-312">尚不支持 `syslog` syscall 接口。</span><span class="sxs-lookup"><span data-stu-id="58d22-312">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="58d22-313">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="58d22-313">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="58d22-314">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="58d22-314">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="58d22-315">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="58d22-315">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="58d22-316">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="58d22-316">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="58d22-317">不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="58d22-317">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="58d22-318">内部版本 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="58d22-318">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="58d22-319">有关内部版本 18252 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-319">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-320">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-320">WSL</span></span>
* <span data-ttu-id="58d22-321">将 init 和 bsdtar 二进制文件移出 lxssmanager dll，移入单独的 tools 文件夹</span><span class="sxs-lookup"><span data-stu-id="58d22-321">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="58d22-322">修复在使用 CLONE_FILES 的情况下，关闭文件描述符时出现的争用</span><span class="sxs-lookup"><span data-stu-id="58d22-322">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="58d22-323">处理转换 DrvFs 路径时 /proc/pid/mountinfo 中的可选字段</span><span class="sxs-lookup"><span data-stu-id="58d22-323">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="58d22-324">允许 DrvFs mknod 成功，但不为 S_IFREG 提供元数据支持</span><span class="sxs-lookup"><span data-stu-id="58d22-324">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="58d22-325">应为 DrvFs 上创建的只读文件设置只读属性 [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="58d22-325">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="58d22-326">添加 /sbin/mount.drvfs 帮助器用于处理 DrvFs 装载</span><span class="sxs-lookup"><span data-stu-id="58d22-326">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="58d22-327">在 DrvFs 中使用 POSIX rename。</span><span class="sxs-lookup"><span data-stu-id="58d22-327">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="58d22-328">允许在无卷 GUID 的卷上执行路径转换。</span><span class="sxs-lookup"><span data-stu-id="58d22-328">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="58d22-329">内部版本 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="58d22-329">Build 17738 (Fast)</span></span>
<span data-ttu-id="58d22-330">有关内部版本 17738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-330">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-331">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-331">WSL</span></span>
* <span data-ttu-id="58d22-332">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="58d22-332">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="58d22-333">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="58d22-333">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="58d22-334">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="58d22-334">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="58d22-335">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="58d22-335">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="58d22-336">内部版本 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="58d22-336">Build 17728 (Fast)</span></span>
<span data-ttu-id="58d22-337">有关内部版本 17728 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-337">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-338">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-338">WSL</span></span>
* <span data-ttu-id="58d22-339">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="58d22-339">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="58d22-340">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="58d22-340">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="58d22-341">修复一些 AF_UNIX 相关的问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="58d22-341">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="58d22-342">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="58d22-342">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="58d22-343">内部版本 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="58d22-343">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="58d22-344">有关内部版本 18204 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-344">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-345">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-345">WSL</span></span>
* <span data-ttu-id="58d22-346">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="58d22-346">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="58d22-347">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="58d22-347">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="58d22-348">内部版本 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="58d22-348">Build 17723 (Fast)</span></span>
<span data-ttu-id="58d22-349">有关内部版本 17723 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-349">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-350">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-350">WSL</span></span>
* <span data-ttu-id="58d22-351">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="58d22-351">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="58d22-352">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="58d22-352">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="58d22-353">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-353">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="58d22-354">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="58d22-354">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="58d22-355">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="58d22-355">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="58d22-356">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="58d22-356">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="58d22-357">内部版本 17713</span><span class="sxs-lookup"><span data-stu-id="58d22-357">Build 17713</span></span>
<span data-ttu-id="58d22-358">有关内部版本 17713 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-358">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-359">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-359">WSL</span></span>
* <span data-ttu-id="58d22-360">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="58d22-360">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="58d22-361">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="58d22-361">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="58d22-362">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="58d22-362">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="58d22-363">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="58d22-363">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="58d22-364">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="58d22-364">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="58d22-365">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="58d22-365">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="58d22-366">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="58d22-366">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="58d22-367">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-367">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="58d22-368">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="58d22-368">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="58d22-369">内部版本 17704</span><span class="sxs-lookup"><span data-stu-id="58d22-369">Build 17704</span></span>
<span data-ttu-id="58d22-370">有关内部版本 17704 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-370">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-371">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-371">WSL</span></span>
* <span data-ttu-id="58d22-372">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="58d22-372">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="58d22-373">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="58d22-373">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="58d22-374">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="58d22-374">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="58d22-375">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="58d22-375">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="58d22-376">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="58d22-376">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="58d22-377">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-377">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="58d22-378">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="58d22-378">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="58d22-379">版本 17692</span><span class="sxs-lookup"><span data-stu-id="58d22-379">Build 17692</span></span>
<span data-ttu-id="58d22-380">有关内部版本 17692 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="58d22-380">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-381">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-381">WSL</span></span>
* <span data-ttu-id="58d22-382">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-382">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="58d22-383">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="58d22-383">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="58d22-384">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="58d22-384">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="58d22-385">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="58d22-385">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="58d22-386">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="58d22-386">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="58d22-387">版本 17686</span><span class="sxs-lookup"><span data-stu-id="58d22-387">Build 17686</span></span>
<span data-ttu-id="58d22-388">有关内部版本 17686 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="58d22-388">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-389">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-389">WSL</span></span>
* <span data-ttu-id="58d22-390">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="58d22-390">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="58d22-391">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="58d22-391">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="58d22-392">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="58d22-392">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="58d22-393">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="58d22-393">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="58d22-394">内部版本 17677</span><span class="sxs-lookup"><span data-stu-id="58d22-394">Build 17677</span></span>
<span data-ttu-id="58d22-395">有关内部版本 17677 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-395">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-396">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-396">WSL</span></span>
* <span data-ttu-id="58d22-397">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="58d22-397">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="58d22-398">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="58d22-398">[GH 2712]</span></span>
* <span data-ttu-id="58d22-399">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-399">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="58d22-400">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="58d22-400">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="58d22-401">内部版本 17666</span><span class="sxs-lookup"><span data-stu-id="58d22-401">Build 17666</span></span>
<span data-ttu-id="58d22-402">有关内部版本 17666 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-402">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-403">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-403">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="58d22-404">警告：某个问题会阻止 WSL 在某些 AMD 芯片组上运行 [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="58d22-404">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="58d22-405">修复程序已准备就绪，即将在 Insider Build 分支中发布。</span><span class="sxs-lookup"><span data-stu-id="58d22-405">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="58d22-406">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="58d22-406">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="58d22-407">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="58d22-407">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="58d22-408">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="58d22-408">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="58d22-409">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-409">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="58d22-410">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="58d22-410">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="58d22-411">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="58d22-411">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="58d22-412">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-412">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="58d22-413">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="58d22-413">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="58d22-414">内部版本 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="58d22-414">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="58d22-415">有关内部版本 17655 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-415">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-416">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-416">WSL</span></span>
* <span data-ttu-id="58d22-417">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-417">Limited support for dmesg.</span></span> <span data-ttu-id="58d22-418">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="58d22-418">Applications can now log to dmesg.</span></span> <span data-ttu-id="58d22-419">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="58d22-419">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="58d22-420">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-420">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="58d22-421">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="58d22-421">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="58d22-422">尚不支持 `syslog` sycall 接口。</span><span class="sxs-lookup"><span data-stu-id="58d22-422">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="58d22-423">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="58d22-423">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="58d22-424">修复了即使文件存在，多线程操作也可能返回 ENOENT 的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-424">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="58d22-425">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="58d22-425">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="58d22-426">内部版本 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="58d22-426">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="58d22-427">有关内部版本 17639 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-427">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-428">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-428">WSL</span></span>
* <span data-ttu-id="58d22-429">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="58d22-429">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="58d22-430">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="58d22-430">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="58d22-431">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="58d22-431">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="58d22-432">具体而言，不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="58d22-432">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="58d22-433">内部版本 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="58d22-433">Build 17133 (Fast)</span></span>
<span data-ttu-id="58d22-434">有关内部版本 17133 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-434">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-435">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-435">WSL</span></span>
* <span data-ttu-id="58d22-436">修复 WSL 中的挂起问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-436">Fix for hang in WSL.</span></span> <span data-ttu-id="58d22-437">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="58d22-437">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="58d22-438">内部版本 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="58d22-438">Build 17128 (Fast)</span></span>
<span data-ttu-id="58d22-439">有关内部版本 17128 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-439">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-440">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-440">WSL</span></span>
* <span data-ttu-id="58d22-441">无</span><span class="sxs-lookup"><span data-stu-id="58d22-441">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="58d22-442">内部版本 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="58d22-442">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="58d22-443">有关内部版本 17627 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-443">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-444">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-444">WSL</span></span>
* <span data-ttu-id="58d22-445">添加对 futex pi 感知操作的支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-445">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="58d22-446">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="58d22-446">[GH 1006]</span></span>
    * <span data-ttu-id="58d22-447">请注意，WSL 功能目前不支持优先级，因此存在一些限制，但标准用法应该不会受到阻止。</span><span class="sxs-lookup"><span data-stu-id="58d22-447">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="58d22-448">对 WSL 进程的 Windows 防火墙支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-448">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="58d22-449">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="58d22-449">[GH 1852]</span></span>
    * <span data-ttu-id="58d22-450">例如，若要允许 WSL python 进程侦听任何端口，请使用提升的 Windows cmd：```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="58d22-450">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="58d22-451">有关如何添加防火墙规则的更多详细信息，请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="58d22-451">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="58d22-452">使用 wsl.exe 时遵循用户的默认 shell。</span><span class="sxs-lookup"><span data-stu-id="58d22-452">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="58d22-453">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="58d22-453">[GH 2372]</span></span>
* <span data-ttu-id="58d22-454">将所有网络接口报告为以太网。</span><span class="sxs-lookup"><span data-stu-id="58d22-454">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="58d22-455">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="58d22-455">[GH 2996]</span></span>
* <span data-ttu-id="58d22-456">更好地处理损坏的 /etc/passwd 文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-456">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="58d22-457">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="58d22-457">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="58d22-458">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-458">Console</span></span>
* <span data-ttu-id="58d22-459">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-459">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-460">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-460">LTP Results:</span></span>
<span data-ttu-id="58d22-461">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-461">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="58d22-462">内部版本 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="58d22-462">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="58d22-463">有关内部版本 17618 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-463">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-464">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-464">WSL</span></span>
* <span data-ttu-id="58d22-465">引入用于 NT interop 的伪控制台功能 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="58d22-465">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="58d22-466">传统的安装机制 (lxrun.exe) 已弃用。</span><span class="sxs-lookup"><span data-stu-id="58d22-466">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="58d22-467">支持用于安装分发版的机制是 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="58d22-467">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="58d22-468">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-468">Console</span></span>
* <span data-ttu-id="58d22-469">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-469">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-470">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-470">LTP Results:</span></span>
<span data-ttu-id="58d22-471">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-471">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="58d22-472">版本 17110</span><span class="sxs-lookup"><span data-stu-id="58d22-472">Build 17110</span></span>
<span data-ttu-id="58d22-473">有关内部版本 17110 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-473">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-474">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-474">WSL</span></span>
* <span data-ttu-id="58d22-475">允许从 Windows 终止 /init [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="58d22-475">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="58d22-476">现在，DrvFs 默认使用按目录区分大小写（相当于使用“case=dir”装载选项）。</span><span class="sxs-lookup"><span data-stu-id="58d22-476">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="58d22-477">使用“case=dir”（旧行为）需要设置注册表项。</span><span class="sxs-lookup"><span data-stu-id="58d22-477">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="58d22-478">如果需要使用“case=dir”，请运行以下命令来启用它：reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="58d22-478">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="58d22-479">如果在旧版 Windows 中使用 WSL 创建的现有目录需要区分大小写，请使用 fsutil.exe 将其标记为区分大小写：fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="58d22-479">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="58d22-480">NULL 终止从 uname syscall 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="58d22-480">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="58d22-481">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-481">Console</span></span>
* <span data-ttu-id="58d22-482">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-482">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-483">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-483">LTP Results:</span></span>
<span data-ttu-id="58d22-484">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-484">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="58d22-485">内部版本 17107</span><span class="sxs-lookup"><span data-stu-id="58d22-485">Build 17107</span></span>
<span data-ttu-id="58d22-486">有关内部版本 17107 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-486">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-487">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-487">WSL</span></span>
* <span data-ttu-id="58d22-488">支持主 pty 终结点上的 TCSETSF 和 TCSETSW [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="58d22-488">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="58d22-489">启动同步 interop 进程可能会导致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="58d22-489">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="58d22-490">修复 PTRACE_ATTACH 以在 /proc/pid/status 中显示正确的跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="58d22-490">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="58d22-491">修复以下争用问题：在不清除 TID 地址的情况下，通过 CLEARTID 和 SETTID 标志克隆的生存期较短的进程可能会退出。</span><span class="sxs-lookup"><span data-stu-id="58d22-491">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="58d22-492">在从 17093 以前的内部版本迁移期间，升级 Linux 文件系统目录时会显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="58d22-492">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="58d22-493">有关 17093 文件系统更改的更多详细信息，请参阅 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) 的发行说明。</span><span class="sxs-lookup"><span data-stu-id="58d22-493">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="58d22-494">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-494">Console</span></span>
* <span data-ttu-id="58d22-495">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-495">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-496">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-496">LTP Results:</span></span>
<span data-ttu-id="58d22-497">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-497">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="58d22-498">内部版本 17101</span><span class="sxs-lookup"><span data-stu-id="58d22-498">Build 17101</span></span>
<span data-ttu-id="58d22-499">有关内部版本 17101 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-499">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-500">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-500">WSL</span></span>
* <span data-ttu-id="58d22-501">signalfd 支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-501">Support for signalfd.</span></span> <span data-ttu-id="58d22-502">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="58d22-502">[GH 129]</span></span>
* <span data-ttu-id="58d22-503">支持包含非法 NTFS 字符的文件名，现在会将这些字符编码为专用 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="58d22-503">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="58d22-504">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="58d22-504">[GH 1514]</span></span>
* <span data-ttu-id="58d22-505">不支持写入时，自动装载将回退到只读。</span><span class="sxs-lookup"><span data-stu-id="58d22-505">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="58d22-506">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="58d22-506">[GH 2603]</span></span>
* <span data-ttu-id="58d22-507">允许粘贴 Unicode 代理项对（类似于表情符号）。</span><span class="sxs-lookup"><span data-stu-id="58d22-507">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="58d22-508">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="58d22-508">[GH 2765]</span></span>
* <span data-ttu-id="58d22-509">/proc 和/sys 中的伪文件应从 select、poll、epoll 等命令返回 read 和 write ready [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="58d22-509">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="58d22-510">修复当注册表被篡改或损坏时，可能导致服务进入无限循环的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-510">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="58d22-511">修复 netlink 消息，以便能够使用更新版本（上游 4.14）的 iproute2。</span><span class="sxs-lookup"><span data-stu-id="58d22-511">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="58d22-512">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-512">Console</span></span>
* <span data-ttu-id="58d22-513">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-513">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-514">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-514">LTP Results:</span></span>
<span data-ttu-id="58d22-515">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-515">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="58d22-516">内部版本 17093</span><span class="sxs-lookup"><span data-stu-id="58d22-516">Build 17093</span></span>
<span data-ttu-id="58d22-517">有关内部版本 17093 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-517">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="58d22-518">重要提示：</span><span class="sxs-lookup"><span data-stu-id="58d22-518">Important:</span></span>
<span data-ttu-id="58d22-519">升级到此内部版本后，首次启动 WSL 时，需要执行一些操作来升级 Linux 文件系统目录。</span><span class="sxs-lookup"><span data-stu-id="58d22-519">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="58d22-520">这可能需要几分钟时间，因此 WSL 的启动速度看上去可能很慢。</span><span class="sxs-lookup"><span data-stu-id="58d22-520">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="58d22-521">对于从 Store 安装的每个分发版，只需执行此操作一次。</span><span class="sxs-lookup"><span data-stu-id="58d22-521">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="58d22-522">改善了 DrvFs 中的区分大小写支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-522">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="58d22-523">DrvFs 现在支持按目录区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-523">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="58d22-524">这是一个可对目录设置的新标志，用于指示应将这些目录中的所有操作视为区分大小写，使得 Windows 应用程序能够正确打开按大小写区分的文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-524">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="58d22-525">DrvFs 提供新的装载选项用于按目录控制区分大小写状态</span><span class="sxs-lookup"><span data-stu-id="58d22-525">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="58d22-526">case=force：将所有目录视为区分大小写（驱动器根目录除外）。</span><span class="sxs-lookup"><span data-stu-id="58d22-526">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="58d22-527">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-527">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="58d22-528">这也是一种传统行为，不过，它会将新目录标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-528">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="58d22-529">case=dir：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-529">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="58d22-530">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-530">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="58d22-531">case=off：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-531">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="58d22-532">使用 WSL 创建的新目录将标记为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-532">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="58d22-533">注意：不会对旧版本中的 WSL 创建的目录设置此标志，因此，如果使用“case=dir”选项，则不会将这些目录视为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-533">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="58d22-534">即将推出一种对现有目录设置此标志的方法。</span><span class="sxs-lookup"><span data-stu-id="58d22-534">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="58d22-535">使用这些选项进行装载的示例（对于现有的驱动器，必须先卸载，然后才能使用不同选项装载）：sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="58d22-535">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="58d22-536">目前，case=force 仍是默认选项。</span><span class="sxs-lookup"><span data-stu-id="58d22-536">For now, case=force is still the default option.</span></span> <span data-ttu-id="58d22-537">以后将更改为 case=dir。</span><span class="sxs-lookup"><span data-stu-id="58d22-537">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="58d22-538">现在，在装载 DrvFs 时，可以在 Windows 路径中使用正斜杠，例如：sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="58d22-538">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="58d22-539">WSL 现在会在实例启动期间处理 /etc/fstab 文件 [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="58d22-539">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="58d22-540">这种处理是在自动装载 DrvFs 驱动器之前完成的；fstab 已装载的任何驱动器不会自动重新装载，使你可以更改特定驱动器的装入点。</span><span class="sxs-lookup"><span data-stu-id="58d22-540">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="58d22-541">可以使用 wsl.conf 禁用此行为。</span><span class="sxs-lookup"><span data-stu-id="58d22-541">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="58d22-542">/proc 中的 mount、mountinfo 和 mountstats 文件会正确转义反斜杠和空格等特殊字符 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="58d22-542">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="58d22-543">在启用元数据的情况下使用 DrvFs 创建的特殊文件（例如 WSL 符号链接，或 fifos 和 sockets）现在可以从 Windows 复制和移动。</span><span class="sxs-lookup"><span data-stu-id="58d22-543">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="58d22-544">可以使用 wsl.conf 更方便地配置 WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-544">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="58d22-545">我们添加了一个方法，用于自动配置 WSL 中每次启动子系统时要应用的某些功能。</span><span class="sxs-lookup"><span data-stu-id="58d22-545">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="58d22-546">这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="58d22-546">This includes automount options and network configuration.</span></span> <span data-ttu-id="58d22-547">有关详细信息，请参阅博客文章： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="58d22-547">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="58d22-548">AF_UNIX 允许在 WSL 上的 Linux 进程与 Windows 本机进程之间建立套接字连接</span><span class="sxs-lookup"><span data-stu-id="58d22-548">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="58d22-549">现在，WSL 和 Windows 应用程序可以通过 Unix 套接字相互通信。</span><span class="sxs-lookup"><span data-stu-id="58d22-549">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="58d22-550">假设你要在 Windows 中运行某个服务，并使其可在 Windows 和 WSL 应用中使用。</span><span class="sxs-lookup"><span data-stu-id="58d22-550">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="58d22-551">现在可以通过 Unix 套接字实现此目的。</span><span class="sxs-lookup"><span data-stu-id="58d22-551">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="58d22-552">有关详细信息，请参阅博客文章： https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="58d22-552">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-553">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-553">WSL</span></span>
* <span data-ttu-id="58d22-554">支持使用 MAP_NORESERVE 的 mmap() [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="58d22-554">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="58d22-555">支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="58d22-555">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="58d22-556">处理克隆中的非 SIGCHLD 终止信号 [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="58d22-556">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="58d22-557">存根 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="58d22-557">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="58d22-558">加载包含偏移量非零的负载标头的 ELF 二进制文件时出错 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="58d22-558">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="58d22-559">加载映像时将尾随页字节归零。</span><span class="sxs-lookup"><span data-stu-id="58d22-559">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="58d22-560">减少 execve 以静默方式终止进程的情况</span><span class="sxs-lookup"><span data-stu-id="58d22-560">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="58d22-561">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-561">Console</span></span>
* <span data-ttu-id="58d22-562">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-562">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-563">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-563">LTP Results:</span></span>
<span data-ttu-id="58d22-564">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-564">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="58d22-565">版本 17083</span><span class="sxs-lookup"><span data-stu-id="58d22-565">Build 17083</span></span>
<span data-ttu-id="58d22-566">有关内部版本 17083 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-566">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-567">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-567">WSL</span></span>
* <span data-ttu-id="58d22-568">修复了与 epoll 相关的 bug 检查 [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="58d22-568">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="58d22-569">修复了关闭 ASLR 时挂起的问题 [GH 1185、2870]</span><span class="sxs-lookup"><span data-stu-id="58d22-569">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="58d22-570">确保 mmap 操作显示原子性 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="58d22-570">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="58d22-571">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-571">Console</span></span>
* <span data-ttu-id="58d22-572">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-572">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-573">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-573">LTP Results:</span></span>
<span data-ttu-id="58d22-574">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-574">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="58d22-575">内部版本 17074</span><span class="sxs-lookup"><span data-stu-id="58d22-575">Build 17074</span></span>
<span data-ttu-id="58d22-576">有关内部版本 17074 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-576">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-577">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-577">WSL</span></span>
* <span data-ttu-id="58d22-578">固定了 DrvFs 元数据的存储格式 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="58d22-578">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="58d22-579">**重要说明：** 在此内部版本之前创建的 DrvFs 元数据将不正确地显示或根本不显示。</span><span class="sxs-lookup"><span data-stu-id="58d22-579">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="58d22-580">若要修复受影响的文件，请使用 chmod 和 chown 重新应用元数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-580">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="58d22-581">修复了多个信号和可重启 syscall 的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-581">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="58d22-582">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-582">Console</span></span>
* <span data-ttu-id="58d22-583">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-583">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-584">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-584">LTP Results:</span></span>
<span data-ttu-id="58d22-585">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-585">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="58d22-586">内部版本 17063</span><span class="sxs-lookup"><span data-stu-id="58d22-586">Build 17063</span></span>
<span data-ttu-id="58d22-587">有关内部版本 17063 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-587">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="58d22-588">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-588">WSL</span></span>
* <span data-ttu-id="58d22-589">DrvFs 支持其他 Linux 元数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-589">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="58d22-590">这样，就可以使用 chmod/chown 设置文件的所有者和模式，并可以创建特殊文件，例如 fifos、Unix 套接字和设备文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-590">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="58d22-591">默认情况下，此功能暂时处于禁用状态，因为它仍是试验性的。</span><span class="sxs-lookup"><span data-stu-id="58d22-591">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="58d22-592">**注意：** 修复了 DrvFs 使用的元数据格式的 bug。</span><span class="sxs-lookup"><span data-stu-id="58d22-592">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="58d22-593">尽管试验性的元数据可在此内部版本中正常工作，但将来的内部版本无法正确读取此内部版本创建的元数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-593">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="58d22-594">你可能需要手动更新已修改的文件的所有者，并且必须重新创建使用自定义设备 ID 的设备。</span><span class="sxs-lookup"><span data-stu-id="58d22-594">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="58d22-595">若要启用元数据，请使用 metadata 选项装载 DrvFs（若要在现有装入点上启用，必须先将其卸载）：</span><span class="sxs-lookup"><span data-stu-id="58d22-595">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="58d22-596">Linux 权限将作为附加元数据添加到文件；它们不会影响 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="58d22-596">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="58d22-597">请记住，使用 Windows 编辑器编辑文件可能会删除元数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-597">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="58d22-598">在这种情况下，文件将还原为默认权限。</span><span class="sxs-lookup"><span data-stu-id="58d22-598">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="58d22-599">已将 mount 选项添加到 DrvFs，用于控制不包含元数据的文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-599">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="58d22-600">uid：所有文件的所有者使用的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="58d22-600">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="58d22-601">gid：所有文件的所有者使用的组 ID。</span><span class="sxs-lookup"><span data-stu-id="58d22-601">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="58d22-602">umask：要对所有文件和目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="58d22-602">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="58d22-603">fmask：要对所有常规文件排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="58d22-603">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="58d22-604">dmask：要对所有目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="58d22-604">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="58d22-605">例如：</span><span class="sxs-lookup"><span data-stu-id="58d22-605">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="58d22-606">与 metadata 选项相结合可以指定不包含元数据的文件的默认权限。</span><span class="sxs-lookup"><span data-stu-id="58d22-606">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="58d22-607">引入了新的环境变量 `WSLENV`，用于配置环境变量在 WSL 与 Win32 之间的流动方式。</span><span class="sxs-lookup"><span data-stu-id="58d22-607">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="58d22-608">例如：</span><span class="sxs-lookup"><span data-stu-id="58d22-608">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="58d22-609">`WSLENV` 是在从 Win32 启动 WSL 进程或者从 WSL 启动 Win32 进程时可以包含的环境变量的冒号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-609">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="58d22-610">每个变量可以使用斜杠后接一个用于指定其转换方式的标志作为后缀。</span><span class="sxs-lookup"><span data-stu-id="58d22-610">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="58d22-611">p：值是应在 WSL 路径与 Win32 路径之间进行转换的路径。</span><span class="sxs-lookup"><span data-stu-id="58d22-611">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="58d22-612">l：值是路径列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-612">l: The value is a list of paths.</span></span> <span data-ttu-id="58d22-613">在 WSL 中，它是冒号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-613">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="58d22-614">在 Win32 中，它是分号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-614">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="58d22-615">u：仅当从 Win32 调用 WSL 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="58d22-615">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="58d22-616">w：仅当从 WSL 调用 Win32 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="58d22-616">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="58d22-617">可以在 .bashrc 中或者在用户的自定义 Windows 环境中设置 `WSLENV`。</span><span class="sxs-lookup"><span data-stu-id="58d22-617">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="58d22-618">drvfs 装入点会正确保留 tar、cp -p 中的时间戳 (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="58d22-618">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="58d22-619">drvfs 符号链接会报告正确的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="58d22-619">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="58d22-620">read/write 适用于极大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="58d22-620">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="58d22-621">waitpid 适用于进程组 ID (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="58d22-621">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="58d22-622">极大改善了大型保留区域的 mmap 性能；改善了 ghc 性能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="58d22-622">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="58d22-623">READ_IMPLIES_EXEC 的个性化支持；修复 maxima 和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="58d22-623">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="58d22-624">mprotect 支持 PROT_GROWSDOWN；修复 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="58d22-624">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="58d22-625">overcommit 模式的页面错误修复；修复 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="58d22-625">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="58d22-626">clone 支持更多标志组合</span><span class="sxs-lookup"><span data-stu-id="58d22-626">clone supports more flags combinations</span></span>
* <span data-ttu-id="58d22-627">支持 epoll 文件的 select/epoll（以前为 no-op）。</span><span class="sxs-lookup"><span data-stu-id="58d22-627">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="58d22-628">通知未实现的 syscall 的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="58d22-628">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="58d22-629">忽略生成 resolv.conf 名称服务器时不启动的接口 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="58d22-629">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="58d22-630">枚举没有物理地址的网络接口。</span><span class="sxs-lookup"><span data-stu-id="58d22-630">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="58d22-631">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="58d22-631">[GH 2685]</span></span>
* <span data-ttu-id="58d22-632">其他 bug 修复和改进。</span><span class="sxs-lookup"><span data-stu-id="58d22-632">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="58d22-633">适用于 Windows 上的开发人员的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="58d22-633">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="58d22-634">Windows 命令行工具链包括 bsdtar (tar) 和 curl。</span><span class="sxs-lookup"><span data-stu-id="58d22-634">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="58d22-635">请阅读[此博客](https://aka.ms/tarcurlwindows)来详细了解如何添加这两个新工具，以及它们如何打造 Windows 上的开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="58d22-635">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="58d22-636">`AF_UNIX` 适用于 Windows 预览体验成员 SDK (17061+)。</span><span class="sxs-lookup"><span data-stu-id="58d22-636">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="58d22-637">请阅读[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)来详细了解 `AF_UNIX`，以及 Windows 上的开发人员如何使用它。</span><span class="sxs-lookup"><span data-stu-id="58d22-637">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="58d22-638">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-638">Console</span></span>
* <span data-ttu-id="58d22-639">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-639">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-640">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-640">LTP Results:</span></span>
<span data-ttu-id="58d22-641">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-641">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="58d22-642">内部版本 17046</span><span class="sxs-lookup"><span data-stu-id="58d22-642">Build 17046</span></span>

<span data-ttu-id="58d22-643">有关内部版本 17046 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="58d22-643">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="58d22-644">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-645">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-645">WSL</span></span>
- <span data-ttu-id="58d22-646">允许进程在没有活动终端的情况下运行。</span><span class="sxs-lookup"><span data-stu-id="58d22-646">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="58d22-647">[GH 709、1007、1511、2252、2391 等]</span><span class="sxs-lookup"><span data-stu-id="58d22-647">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="58d22-648">更好地支持 CLONE_VFORK 和 CLONE_VM。</span><span class="sxs-lookup"><span data-stu-id="58d22-648">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="58d22-649">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="58d22-649">[GH 1878, 2615]</span></span>
- <span data-ttu-id="58d22-650">跳过 WSL 网络操作的 TDI 筛选器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="58d22-650">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="58d22-651">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="58d22-651">[GH 1554]</span></span>
- <span data-ttu-id="58d22-652">在满足特定的条件时，DrvFs 将创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="58d22-652">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="58d22-653">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="58d22-653">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="58d22-654">链接目标必须是相对性的，不能跨任何装入点或符号链接，并且必须存在。</span><span class="sxs-lookup"><span data-stu-id="58d22-654">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="58d22-655">除非已启用开发人员模式，否则用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE（这通常需要以提升的权限启动 wsl.exe）。</span><span class="sxs-lookup"><span data-stu-id="58d22-655">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="58d22-656">在所有其他情况下，DrvFs 仍会创建 WSL 符号链接。</span><span class="sxs-lookup"><span data-stu-id="58d22-656">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="58d22-657">允许同时运行提升和未提升的 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="58d22-657">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="58d22-658">支持 /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="58d22-658">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="58d22-659">添加 wslpath 用于执行 WSL<->Windows 路径转换。</span><span class="sxs-lookup"><span data-stu-id="58d22-659">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="58d22-660">[GH 522、1243、1834、2327 等]</span><span class="sxs-lookup"><span data-stu-id="58d22-660">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="58d22-661">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-661">Console</span></span>
- <span data-ttu-id="58d22-662">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-662">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-663">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-663">LTP Results:</span></span>
<span data-ttu-id="58d22-664">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-664">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="58d22-665">内部版本 17040</span><span class="sxs-lookup"><span data-stu-id="58d22-665">Build 17040</span></span>

<span data-ttu-id="58d22-666">有关内部版本 17040 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="58d22-666">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-667">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-667">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-668">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-668">WSL</span></span>
- <span data-ttu-id="58d22-669">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-669">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-670">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-670">Console</span></span>
- <span data-ttu-id="58d22-671">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-671">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-672">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-672">LTP Results:</span></span>
<span data-ttu-id="58d22-673">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-673">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="58d22-674">内部版本 17035</span><span class="sxs-lookup"><span data-stu-id="58d22-674">Build 17035</span></span>

<span data-ttu-id="58d22-675">有关内部版本 17035 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="58d22-675">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-676">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-676">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-677">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-677">WSL</span></span>
- <span data-ttu-id="58d22-678">访问 DrvFs 上的文件偶尔会失败并出现 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="58d22-678">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="58d22-679">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="58d22-679">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-680">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-680">Console</span></span>
- <span data-ttu-id="58d22-681">在 VT 模式下插入/删除行时丢失一些颜色。</span><span class="sxs-lookup"><span data-stu-id="58d22-681">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-682">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-682">LTP Results:</span></span>
<span data-ttu-id="58d22-683">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-683">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="58d22-684">内部版本 17025</span><span class="sxs-lookup"><span data-stu-id="58d22-684">Build 17025</span></span>

<span data-ttu-id="58d22-685">有关内部版本 17025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="58d22-685">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-686">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-686">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-687">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-687">WSL</span></span>
- <span data-ttu-id="58d22-688">在新的前台进程组中启动初始进程 [GH 1653、2510]。</span><span class="sxs-lookup"><span data-stu-id="58d22-688">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="58d22-689">SIGHUP 传递修复 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="58d22-689">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="58d22-690">如果未提供虚拟网桥名称，将生成默认名称 [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="58d22-690">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="58d22-691">实现 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="58d22-691">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="58d22-692">更多 interop stdout/stderr 管道修复措施。</span><span class="sxs-lookup"><span data-stu-id="58d22-692">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="58d22-693">存根 syncfs 系统调用。</span><span class="sxs-lookup"><span data-stu-id="58d22-693">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-694">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-694">Console</span></span>
- <span data-ttu-id="58d22-695">修复第三方控制台的输入 VT 转换 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="58d22-695">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-696">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-696">LTP Results:</span></span>
<span data-ttu-id="58d22-697">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-697">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="58d22-698">内部版本 17017</span><span class="sxs-lookup"><span data-stu-id="58d22-698">Build 17017</span></span>

<span data-ttu-id="58d22-699">有关内部版本 17017 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="58d22-699">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-700">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-700">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-701">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-701">WSL</span></span>
- <span data-ttu-id="58d22-702">忽略空的 ELF 程序标头 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="58d22-702">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="58d22-703">允许 LxssManager 为非交互式用户创建 WSL 实例（ssh 和计划任务支持）[GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="58d22-703">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="58d22-704">支持 WSL->Win32->WSL（“起始”）方案 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="58d22-704">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="58d22-705">有限支持终止通过 interop 调用的控制台应用 [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="58d22-705">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="58d22-706">支持 devpts 的装载选项 [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="58d22-706">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="58d22-707">Ptrace 阻止子级启动 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="58d22-707">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="58d22-708">EPOLLET 缺少某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="58d22-708">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="58d22-709">返回 PTRACE_GETSIGINFO 的更多数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-709">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="58d22-710">结合 lseek 运行 Getdents 会提供错误的结果。</span><span class="sxs-lookup"><span data-stu-id="58d22-710">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="58d22-711">修复某些 Win32 interop 应用挂起，并等待在没有更多数据的管道中提供输入的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-711">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="58d22-712">tty/pty 文件的 O_ASYNC 支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-712">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="58d22-713">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-713">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-714">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-714">Console</span></span>
- <span data-ttu-id="58d22-715">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-715">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-716">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-716">LTP Results:</span></span>
<span data-ttu-id="58d22-717">正在测试。</span><span class="sxs-lookup"><span data-stu-id="58d22-717">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="58d22-718">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="58d22-718">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="58d22-719">内部版本 16288</span><span class="sxs-lookup"><span data-stu-id="58d22-719">Build 16288</span></span>

<span data-ttu-id="58d22-720">有关内部版本 16288 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-720">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-721">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-721">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-722">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-722">WSL</span></span>
- <span data-ttu-id="58d22-723">正确初始化和报告套接字文件描述符的 uid、gid 和模式 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="58d22-723">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="58d22-724">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-724">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-725">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-725">Console</span></span>
- <span data-ttu-id="58d22-726">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-726">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-727">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-727">LTP Results:</span></span>
<span data-ttu-id="58d22-728">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-728">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="58d22-729">内部版本 16278</span><span class="sxs-lookup"><span data-stu-id="58d22-729">Build 16278</span></span>

<span data-ttu-id="58d22-730">有关内部版本 162738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-730">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-731">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-731">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-732">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-732">WSL</span></span>
- <span data-ttu-id="58d22-733">分解 LX MM 状态时显式取消映射文件后备节的映射视图 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="58d22-733">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="58d22-734">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-734">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-735">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-735">Console</span></span>
- <span data-ttu-id="58d22-736">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-736">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-737">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-737">LTP Results:</span></span>
<span data-ttu-id="58d22-738">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-738">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="58d22-739">内部版本 16275</span><span class="sxs-lookup"><span data-stu-id="58d22-739">Build 16275</span></span>

<span data-ttu-id="58d22-740">有关内部版本 162735 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-740">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-741">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-741">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-742">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-742">WSL</span></span>
- <span data-ttu-id="58d22-743">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-743">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-744">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-744">Console</span></span>
- <span data-ttu-id="58d22-745">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-745">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-746">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-746">LTP Results:</span></span>
<span data-ttu-id="58d22-747">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-747">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="58d22-748">内部版本 16273</span><span class="sxs-lookup"><span data-stu-id="58d22-748">Build 16273</span></span>

<span data-ttu-id="58d22-749">有关内部版本 16273 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-749">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-750">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-750">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-751">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-751">WSL</span></span>
- <span data-ttu-id="58d22-752">修复了 DrvFs 有时报告目录的错误文件类型的问题 [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="58d22-752">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="58d22-753">允许创建 NETLINK_KOBJECT_UEVENT 套接字来取消阻止使用 UEVENT 的程序 [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="58d22-753">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="58d22-754">添加对非阻塞连接的支持 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="58d22-754">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="58d22-755">实现 CLONE_FS 克隆系统调用标志 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="58d22-755">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="58d22-756">修复有关在 NT interop 中不会正确处理制表符或引号的问题 [GH 1625、2164]</span><span class="sxs-lookup"><span data-stu-id="58d22-756">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="58d22-757">解决尝试重新启动 WSL 实例时发生的拒绝访问错误 [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="58d22-757">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="58d22-758">实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="58d22-758">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="58d22-759">修复各种 SysFs 文件的权限 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="58d22-759">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="58d22-760">修复设置过程中 Haskell 堆栈挂起的问题 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="58d22-760">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="58d22-761">实现 binfmt_misc“C”、“O”和“P”标志 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="58d22-761">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="58d22-762">添加 /proc/sys/kernel /shmmax /shmmni 和 /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="58d22-762">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="58d22-763">添加对 ioprio_set 系统调用的部分支持 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="58d22-763">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="58d22-764">存根 SO_REUSEPORT 和添加 netlink 套接字的 SO_PASSCRED 支持 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="58d22-764">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="58d22-765">如果当前正在安装或卸载分发版，将从 RegisterDistribuiton 返回不同的错误代码。</span><span class="sxs-lookup"><span data-stu-id="58d22-765">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="58d22-766">允许通过 wslconfig.exe 取消注册部分安装的 WSL 分发版</span><span class="sxs-lookup"><span data-stu-id="58d22-766">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="58d22-767">修复 udp::msg_peek 的 python 套接字测试挂起问题</span><span class="sxs-lookup"><span data-stu-id="58d22-767">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="58d22-768">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-768">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-769">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-769">Console</span></span>
- <span data-ttu-id="58d22-770">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-770">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-771">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-771">LTP Results:</span></span>
<span data-ttu-id="58d22-772">测试总数：1904</span><span class="sxs-lookup"><span data-stu-id="58d22-772">Total Tests: 1904</span></span><br/>
<span data-ttu-id="58d22-773">跳过的测试总数：209</span><span class="sxs-lookup"><span data-stu-id="58d22-773">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="58d22-774">失败总数：229</span><span class="sxs-lookup"><span data-stu-id="58d22-774">Total Failures: 229</span></span><br/>
[<span data-ttu-id="58d22-775">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-775">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="58d22-776">版本 16257</span><span class="sxs-lookup"><span data-stu-id="58d22-776">Build 16257</span></span>

<span data-ttu-id="58d22-777">有关内部版本 16257 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-777">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-778">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-778">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-779">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-779">WSL</span></span>
- <span data-ttu-id="58d22-780">实现 prlimit64 系统调用</span><span class="sxs-lookup"><span data-stu-id="58d22-780">Implement prlimit64 system call</span></span>
- <span data-ttu-id="58d22-781">添加对 ulimit -n 的支持 (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="58d22-781">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="58d22-782">TCP 套接字的存根 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="58d22-782">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="58d22-783">修复无效的 AT_EXECFN 辅助矢量行为 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="58d22-783">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="58d22-784">修复 console/tty 的 copy/paste 行为，并添加更适当的完整缓冲区处理 [GH 2204、2131]</span><span class="sxs-lookup"><span data-stu-id="58d22-784">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="58d22-785">在 set-user-ID 和 set-group-ID 程序的辅助矢量中设置 AT_SECURE [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="58d22-785">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="58d22-786">伪终端主终结点不处理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="58d22-786">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="58d22-787">修复 lseek 在 LxFs 中的回退目录行为 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="58d22-787">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="58d22-788">重度使用后 /dev/ptmx 锁定 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="58d22-788">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="58d22-789">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-789">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-790">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-790">Console</span></span>
- <span data-ttu-id="58d22-791">修复横线/下划线四处可见的问题 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="58d22-791">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="58d22-792">修复进程顺序更改，使 NPM 更难以关闭的问题 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="58d22-792">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="58d22-793">添加了新的色彩方案： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="58d22-793">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-794">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-794">LTP Results:</span></span>
<span data-ttu-id="58d22-795">自 16251 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-795">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-796">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-796">Syscall Support</span></span>
<span data-ttu-id="58d22-797">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-797">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-798">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-798">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="58d22-799">已知问题</span><span class="sxs-lookup"><span data-stu-id="58d22-799">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="58d22-800">GitHub 问题 2392：WSL 无法识别 Windows 文件夹 ...</span><span class="sxs-lookup"><span data-stu-id="58d22-800">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="58d22-801">在内部版本 16257 中，WSL 在通过 `/mnt/c/...` 枚举 Windows 文件/文件夹时会出现问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-801">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="58d22-802">此问题已修复，修复程序将在 2017 年 8 月 14 日开始的周内，在预览体验成员内部版本中发布。</span><span class="sxs-lookup"><span data-stu-id="58d22-802">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="58d22-803">内部版本 16251</span><span class="sxs-lookup"><span data-stu-id="58d22-803">Build 16251</span></span>

<span data-ttu-id="58d22-804">有关内部版本 16251 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-804">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-805">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-805">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-806">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-806">WSL</span></span>
- <span data-ttu-id="58d22-807">从 WSL 可选组件中删除 beta 标记，有关详细信息，请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-807">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="58d22-808">在执行时正确初始化 set-user-ID 和 set-group-ID 二进制文件的 saved-set uid 和 gid [GH 962、1415、2072]</span><span class="sxs-lookup"><span data-stu-id="58d22-808">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="58d22-809">添加了对 ptrace PTRACE_O_TRACEEXIT 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="58d22-809">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="58d22-810">添加了对包含 NT_FPREGSET 的 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="58d22-810">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="58d22-811">修复了 ptrace 在忽略信号时停止的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-811">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="58d22-812">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-812">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-813">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-813">Console</span></span>
- <span data-ttu-id="58d22-814">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-814">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-815">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-815">LTP Results:</span></span>
<span data-ttu-id="58d22-816">通过的测试数：768</span><span class="sxs-lookup"><span data-stu-id="58d22-816">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="58d22-817">失败的测试数：244</span><span class="sxs-lookup"><span data-stu-id="58d22-817">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="58d22-818">跳过的测试数：96</span><span class="sxs-lookup"><span data-stu-id="58d22-818">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="58d22-819">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-819">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="58d22-820">内部版本 16241</span><span class="sxs-lookup"><span data-stu-id="58d22-820">Build 16241</span></span>

<span data-ttu-id="58d22-821">有关内部版本 16241 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-821">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-822">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-822">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="58d22-823">WSL</span><span class="sxs-lookup"><span data-stu-id="58d22-823">WSL</span></span>
- <span data-ttu-id="58d22-824">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-824">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="58d22-825">控制台</span><span class="sxs-lookup"><span data-stu-id="58d22-825">Console</span></span>
- <span data-ttu-id="58d22-826">修复输出跨行 DEC 的错误字符的问题，最初报告位于[此处](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="58d22-826">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="58d22-827">修复代码页 65001 (utf8) 中不显示输出文本的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-827">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="58d22-828">更改选择内容时，不会将对某种颜色的 RGB 值所做的更改传输到调色板的其他部分。</span><span class="sxs-lookup"><span data-stu-id="58d22-828">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="58d22-829">这在一定程度上使得控制台属性表变得更易于使用。</span><span class="sxs-lookup"><span data-stu-id="58d22-829">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="58d22-830">Ctrl+S 似乎不起作用</span><span class="sxs-lookup"><span data-stu-id="58d22-830">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="58d22-831">ANSI 转义代码中根本没有 Un-Bold/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="58d22-831">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="58d22-832">控制台不正常支持 Vim 色彩主题 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="58d22-832">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="58d22-833">无法粘贴特定的字符 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="58d22-833">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="58d22-834">当编辑/命令行上有内容时，重复流的调整大小操作以奇怪的方式与 bash 窗口调整大小操作交互 [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="58d22-834">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="58d22-835">按 Ctrl-L 不会清屏 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="58d22-835">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="58d22-836">在 HDPI 上显示 VT 时的控制台呈现 bug [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="58d22-836">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="58d22-837">日文字符出现乱码和 Unicode 字符 U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="58d22-837">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="58d22-838">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-838">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="58d22-839">版本 16237</span><span class="sxs-lookup"><span data-stu-id="58d22-839">Build 16237</span></span>

<span data-ttu-id="58d22-840">有关内部版本 16237 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-840">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-841">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-841">Fixed</span></span>
- <span data-ttu-id="58d22-842">对 lxfs 中不包含 EA 的文件使用默认属性 (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="58d22-842">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="58d22-843">添加了对使用扩展属性的分发版的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-843">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="58d22-844">修复 getdents 和 getdents64 返回的项的填充</span><span class="sxs-lookup"><span data-stu-id="58d22-844">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="58d22-845">修复针对 shmctl SHM_STAT 系统调用的权限检查 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="58d22-845">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="58d22-846">修复了 tty 的错误初始 epoll 状态 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="58d22-846">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="58d22-847">修复 DrvFs readdir 不返回所有项的问题 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="58d22-847">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="58d22-848">修复取消链接文件时的 LxFs readdir [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="58d22-848">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="58d22-849">允许通过 procfs 重新打开未链接的 drvfs 文件</span><span class="sxs-lookup"><span data-stu-id="58d22-849">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="58d22-850">添加了用于禁用 WSL 功能的全局注册表项重写（interop/驱动器装载）</span><span class="sxs-lookup"><span data-stu-id="58d22-850">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="58d22-851">修复 DrvFs（和 LxFs）的“统计信息”中的错误块计数 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="58d22-851">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="58d22-852">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-852">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="58d22-853">内部版本 16232</span><span class="sxs-lookup"><span data-stu-id="58d22-853">Build 16232</span></span>

<span data-ttu-id="58d22-854">有关内部版本 16232 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-854">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-855">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-855">Fixed</span></span>
- <span data-ttu-id="58d22-856">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-856">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="58d22-857">内部版本 16226</span><span class="sxs-lookup"><span data-stu-id="58d22-857">Build 16226</span></span>

<span data-ttu-id="58d22-858">有关内部版本 16226 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-858">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-859">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-859">Fixed</span></span>
- <span data-ttu-id="58d22-860">xattr 相关的 syscall 支持（getxattr、setxattr、listxattr、removexattr）。</span><span class="sxs-lookup"><span data-stu-id="58d22-860">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="58d22-861">security.capablity xattr 支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-861">security.capablity xattr support.</span></span>
- <span data-ttu-id="58d22-862">改善了与某些文件系统和筛选器（包括非 MS SMB 服务器）的兼容性。</span><span class="sxs-lookup"><span data-stu-id="58d22-862">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="58d22-863">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="58d22-863">[GH #1952]</span></span>
- <span data-ttu-id="58d22-864">改善了对 OneDrive 占位符、GVFS 占位符和精简 OS 压缩文件的支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-864">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="58d22-865">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-865">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="58d22-866">内部版本 16215</span><span class="sxs-lookup"><span data-stu-id="58d22-866">Build 16215</span></span>

<span data-ttu-id="58d22-867">有关内部版本 16215 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-867">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-868">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-868">Fixed</span></span>
- <span data-ttu-id="58d22-869">WSL 不再需要开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="58d22-869">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="58d22-870">支持 drvfs 中的目录接合。</span><span class="sxs-lookup"><span data-stu-id="58d22-870">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="58d22-871">处理 WSL appx 分发包的卸载。</span><span class="sxs-lookup"><span data-stu-id="58d22-871">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="58d22-872">更新 procfs 以显示专用映射和共享映射。</span><span class="sxs-lookup"><span data-stu-id="58d22-872">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="58d22-873">为 wslconfig.exe 添加清理部分安装或已卸载的分发版的功能。</span><span class="sxs-lookup"><span data-stu-id="58d22-873">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="58d22-874">添加了对 TCP 套接字的 IP_MTU_DISCOVER 的支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-874">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="58d22-875">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="58d22-875">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="58d22-876">推断 AF_INADDR 路由的协议系列。</span><span class="sxs-lookup"><span data-stu-id="58d22-876">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="58d22-877">串行设备改进 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="58d22-877">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="58d22-878">内部版本 16199</span><span class="sxs-lookup"><span data-stu-id="58d22-878">Build 16199</span></span>

<span data-ttu-id="58d22-879">有关内部版本 16199 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-879">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-880">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-880">Fixed</span></span>
- <span data-ttu-id="58d22-881">这些版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-881">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="58d22-882">内部版本 16193</span><span class="sxs-lookup"><span data-stu-id="58d22-882">Build 16193</span></span>

<span data-ttu-id="58d22-883">有关内部版本 16193 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-883">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-884">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-884">Fixed</span></span>
- <span data-ttu-id="58d22-885">发送 SIGCONT 与终止线程组之间的争用状态 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="58d22-885">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="58d22-886">更改 tty 和 pty 设备以报告 FILE_DEVICE_NAMED_PIPE 而不是 FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="58d22-886">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="58d22-887">IP_OPTIONS 的 SSH 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-887">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="58d22-888">已将 DrvFs 装载移到初始化守护程序 [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="58d22-888">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="58d22-889">在 DrvFs 中添加了遵循 NT 符号链接的支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-889">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="58d22-890">内部版本 16184</span><span class="sxs-lookup"><span data-stu-id="58d22-890">Build 16184</span></span>

<span data-ttu-id="58d22-891">有关内部版本 16184 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-891">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-892">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-892">Fixed</span></span>
- <span data-ttu-id="58d22-893">删除了 apt 包维护任务 (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="58d22-893">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="58d22-894">修复了 node.js 中的 Windows 进程不显示输出的问题 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="58d22-894">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="58d22-895">放宽 lxcore 中的对齐要求 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="58d22-895">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="58d22-896">修复了许多系统调用中处理 AT_EMPTY_PATH 标志的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-896">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="58d22-897">修复了删除存在已打开句柄的 DrvFs 文件时，导致文件出现未定义的行为的问题 [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="58d22-897">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="58d22-898">/etc/hosts 现在会从 Windows hosts 文件 (%windir%\system32\drivers\etc\hosts) 继承项 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="58d22-898">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="58d22-899">内部版本 16179</span><span class="sxs-lookup"><span data-stu-id="58d22-899">Build 16179</span></span>

<span data-ttu-id="58d22-900">有关内部版本 16179 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-900">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-901">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-901">Fixed</span></span>
- <span data-ttu-id="58d22-902">本周没有 WSL 更改。</span><span class="sxs-lookup"><span data-stu-id="58d22-902">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="58d22-903">内部版本 16176</span><span class="sxs-lookup"><span data-stu-id="58d22-903">Build 16176</span></span>

<span data-ttu-id="58d22-904">有关内部版本 16176 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-904">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-905">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-905">Fixed</span></span>

- [<span data-ttu-id="58d22-906">已启用串行支持</span><span class="sxs-lookup"><span data-stu-id="58d22-906">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="58d22-907">添加了 IP 套接字选项 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="58d22-907">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="58d22-908">实现了 pwritev 函数（将文件上传到 nginx/PHP-FPM 时）[GH 1506]</span><span class="sxs-lookup"><span data-stu-id="58d22-908">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="58d22-909">添加了 IP 套接字选项 IP_MULTICAST_IF 和 IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="58d22-909">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="58d22-910">支持套接字选项 IP_MULTICAST_LOOP 和 IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="58d22-910">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="58d22-911">为应用节点、traceroute、dig、nslookup、主机添加了 IP(V6)_MTU 套接字选项</span><span class="sxs-lookup"><span data-stu-id="58d22-911">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="58d22-912">添加了 IP 套接字选项 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="58d22-912">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="58d22-913">文件系统改进</span><span class="sxs-lookup"><span data-stu-id="58d22-913">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="58d22-914">允许装载 UNC 路径</span><span class="sxs-lookup"><span data-stu-id="58d22-914">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="58d22-915">在 drvfs 中启用 CDFS 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-915">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="58d22-916">正确处理 drvfs 中网络文件系统的权限</span><span class="sxs-lookup"><span data-stu-id="58d22-916">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="58d22-917">在 drvfs 中添加远程驱动器的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-917">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="58d22-918">在 drvfs 中启用 FAT 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-918">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="58d22-919">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-919">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-920">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="58d22-920">LTP Results</span></span>
<span data-ttu-id="58d22-921">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-921">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="58d22-922">内部版本 16170</span><span class="sxs-lookup"><span data-stu-id="58d22-922">Build 16170</span></span>

<span data-ttu-id="58d22-923">有关内部版本 16170 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-923">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="58d22-924">我们发布的新[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)中介绍了我们在测试 WSL 方面所做的努力。</span><span class="sxs-lookup"><span data-stu-id="58d22-924">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="58d22-925">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-925">Fixed</span></span>

- <span data-ttu-id="58d22-926">支持套接字选项 IP_ADD_MEMBERSHIP 和 IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="58d22-926">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="58d22-927">添加对 PTRACE_OLDSETOPTIONS 的支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-927">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="58d22-928">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="58d22-928">[GH 1692]</span></span>
- <span data-ttu-id="58d22-929">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-929">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-930">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="58d22-930">LTP Results</span></span>
<span data-ttu-id="58d22-931">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-931">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="58d22-932">内部版本 15046 到 Windows 10 创意者更新</span><span class="sxs-lookup"><span data-stu-id="58d22-932">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="58d22-933">我们未计划在 Windows 10 创意者更新中包含其他 WSL 修复或功能。</span><span class="sxs-lookup"><span data-stu-id="58d22-933">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="58d22-934">WSL 的发行说明将在未来几周恢复发布，其中补充了面向下一个 Windows 更新主要版本的信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-934">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="58d22-935">有关内部版本 15046 和将来的预览体验版的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-935">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="58d22-936">内部版本 15042</span><span class="sxs-lookup"><span data-stu-id="58d22-936">Build 15042</span></span>

<span data-ttu-id="58d22-937">有关内部版本 15042 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-937">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-938">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-938">Fixed</span></span>

- <span data-ttu-id="58d22-939">修复删除以“...”结尾的路径时出现死锁的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-939">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="58d22-940">修复了 FIONBIO 在成功时不返回 0 的问题 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="58d22-940">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="58d22-941">修复了 inet 数据报套接字的零长度读取问题</span><span class="sxs-lookup"><span data-stu-id="58d22-941">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="58d22-942">修复 drvfs inode 查找中的争用状况可能导致死锁的问题 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="58d22-942">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="58d22-943">扩展了对 unix 套接字辅助数据的支持；SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="58d22-943">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="58d22-944">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-944">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-945">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-945">LTP Results:</span></span>
<span data-ttu-id="58d22-946">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="58d22-946">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="58d22-947">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="58d22-947">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="58d22-948">内部版本 15031</span><span class="sxs-lookup"><span data-stu-id="58d22-948">Build 15031</span></span>

<span data-ttu-id="58d22-949">有关内部版本 15031 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-949">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-950">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-950">Fixed</span></span>

- <span data-ttu-id="58d22-951">修复了 time(2) 偶尔行为异常的 bug。</span><span class="sxs-lookup"><span data-stu-id="58d22-951">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="58d22-952">修复了 \*SIGPROCMASK syscall 可能损坏信号掩码的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-952">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="58d22-953">现在会在 WSL 进程创建通知中返回完整的命令行长度。</span><span class="sxs-lookup"><span data-stu-id="58d22-953">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="58d22-954">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="58d22-954">[GH 1632]</span></span>
- <span data-ttu-id="58d22-955">WSL 现在会针对 GDB 挂起通过 ptrace 报告线程退出。</span><span class="sxs-lookup"><span data-stu-id="58d22-955">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="58d22-956">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="58d22-956">[GH 1196]</span></span>
- <span data-ttu-id="58d22-957">修复了在收到繁重 tmux IO 后 ptys 挂起的 bug。</span><span class="sxs-lookup"><span data-stu-id="58d22-957">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="58d22-958">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="58d22-958">[GH 1358]</span></span>
- <span data-ttu-id="58d22-959">修复了许多系统调用中的超时验证（futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create）</span><span class="sxs-lookup"><span data-stu-id="58d22-959">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="58d22-960">添加了 eventfd EFD_SEMAPHORE 支持 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="58d22-960">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="58d22-961">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-961">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-962">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-962">LTP Results:</span></span>
<span data-ttu-id="58d22-963">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="58d22-963">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="58d22-964">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="58d22-964">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="58d22-965">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-965">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="58d22-966">内部版本 15025</span><span class="sxs-lookup"><span data-stu-id="58d22-966">Build 15025</span></span>

<span data-ttu-id="58d22-967">有关内部版本 15025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-967">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-968">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-968">Fixed</span></span>

- <span data-ttu-id="58d22-969">修复破坏 grep 2.27 的 bug [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="58d22-969">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="58d22-970">为 eventfd2 syscall 实现了 EFD_SEMAPHORE 标志 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="58d22-970">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="58d22-971">实现了 /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="58d22-971">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="58d22-972">针对 unix 流套接字的信号驱动 IO 支持 [GH 393、68]</span><span class="sxs-lookup"><span data-stu-id="58d22-972">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="58d22-973">支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="58d22-973">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="58d22-974">实现 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="58d22-974">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="58d22-975">修复了 epoll_wait() 不等待的 bug [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="58d22-975">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="58d22-976">实现 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="58d22-976">Implement /proc/version_signature</span></span>
- <span data-ttu-id="58d22-977">现在，如果两个文件描述符引用同一管道，则 syscall 会返回失败</span><span class="sxs-lookup"><span data-stu-id="58d22-977">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="58d22-978">为 Unix 套接字的 SO_PEERCRED 实现了正确的行为</span><span class="sxs-lookup"><span data-stu-id="58d22-978">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="58d22-979">修复了 tkill syscall 处理无效参数的方法</span><span class="sxs-lookup"><span data-stu-id="58d22-979">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="58d22-980">做出更改以提高 drvfs 的性能</span><span class="sxs-lookup"><span data-stu-id="58d22-980">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="58d22-981">针对 Ruby IO 阻塞的次要修复</span><span class="sxs-lookup"><span data-stu-id="58d22-981">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="58d22-982">修复了 recvmsg() 对 inet 套接字的 MSG_DONTWAIT 标志返回 EINVAL 的问题 [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="58d22-982">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="58d22-983">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-983">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-984">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-984">LTP Results:</span></span>
<span data-ttu-id="58d22-985">通过的测试数：732</span><span class="sxs-lookup"><span data-stu-id="58d22-985">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="58d22-986">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="58d22-986">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="58d22-987">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-987">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="58d22-988">内部版本 15019</span><span class="sxs-lookup"><span data-stu-id="58d22-988">Build 15019</span></span>

<span data-ttu-id="58d22-989">有关内部版本 15019 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-989">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-990">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-990">Fixed</span></span>

- <span data-ttu-id="58d22-991">修复了 htop 等工具在 procfs 中错误报告 CPU 使用率的 bug（GH 823、945、971）</span><span class="sxs-lookup"><span data-stu-id="58d22-991">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="58d22-992">对现有的文件结合 O_TRUNC 调用 open() 时，inotify 现在会在 IN_OPEN 的前面生成 IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="58d22-992">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="58d22-993">修复 unix 套接字 getsockopt SO_ERROR 以启用 postgress [GH 61、1354]</span><span class="sxs-lookup"><span data-stu-id="58d22-993">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="58d22-994">为 GO 语言实现 /proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="58d22-994">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="58d22-995">Apt-get package update 后台任务现在会在视图中以隐藏方式运行</span><span class="sxs-lookup"><span data-stu-id="58d22-995">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="58d22-996">清除 ipv6 localhost 的范围（Spring-Framework(Java) 失败）。</span><span class="sxs-lookup"><span data-stu-id="58d22-996">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="58d22-997">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-997">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-998">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-998">LTP Results:</span></span>
<span data-ttu-id="58d22-999">通过的测试数：714</span><span class="sxs-lookup"><span data-stu-id="58d22-999">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="58d22-1000">未通过的测试数（失败、已跳过等）：249</span><span class="sxs-lookup"><span data-stu-id="58d22-1000">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="58d22-1001">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1001">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="58d22-1002">内部版本 15014</span><span class="sxs-lookup"><span data-stu-id="58d22-1002">Build 15014</span></span>

<span data-ttu-id="58d22-1003">有关内部版本 15014 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1003">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1004">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1004">Fixed</span></span>

- <span data-ttu-id="58d22-1005">Ctrl+C 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="58d22-1005">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="58d22-1006">htop 和 ps auxw 现在会显示正确的资源利用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="58d22-1006">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="58d22-1007">NT 异常到信号的基本转换。</span><span class="sxs-lookup"><span data-stu-id="58d22-1007">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="58d22-1008">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="58d22-1008">(GH #513)</span></span>
- <span data-ttu-id="58d22-1009">当空间耗尽时，fallocate 现在会失败并返回 ENOSPC，而不是返回 EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="58d22-1009">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="58d22-1010">添加了 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="58d22-1010">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="58d22-1011">实现了 semop 和 semtimedop 系统调用</span><span class="sxs-lookup"><span data-stu-id="58d22-1011">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="58d22-1012">修复了 IP_RECVTOS 和 IPV6_RECVTCLASS 套接字选项的 nslookup 错误 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="58d22-1012">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="58d22-1013">支持套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="58d22-1013">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="58d22-1014">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1014">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1015">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1015">LTP Results:</span></span>
<span data-ttu-id="58d22-1016">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="58d22-1016">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="58d22-1017">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="58d22-1017">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="58d22-1018">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1018">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="58d22-1019">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="58d22-1019">Syscall Summary</span></span>
<span data-ttu-id="58d22-1020">Syscall 总数：384</span><span class="sxs-lookup"><span data-stu-id="58d22-1020">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="58d22-1021">已实现总数：235</span><span class="sxs-lookup"><span data-stu-id="58d22-1021">Total Implemented: 235</span></span> </br>
<span data-ttu-id="58d22-1022">已存根总数：22</span><span class="sxs-lookup"><span data-stu-id="58d22-1022">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="58d22-1023">未实现总数：127</span><span class="sxs-lookup"><span data-stu-id="58d22-1023">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="58d22-1024">详细分解</span><span class="sxs-lookup"><span data-stu-id="58d22-1024">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="58d22-1025">内部版本 15007</span><span class="sxs-lookup"><span data-stu-id="58d22-1025">Build 15007</span></span>

<span data-ttu-id="58d22-1026">有关内部版本 15007 的一般 Windows 信息，请访问 [Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1026">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="58d22-1027">已知问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1027">Known Issue</span></span>

- <span data-ttu-id="58d22-1028">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="58d22-1028">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="58d22-1029">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="58d22-1029">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="58d22-1030">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="58d22-1030">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="58d22-1031">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="58d22-1031">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="58d22-1032">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="58d22-1032">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="58d22-1033">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="58d22-1033">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="58d22-1034">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1034">Fixed</span></span>

- <span data-ttu-id="58d22-1035">更正了运行 WSL 会消耗 100% 的 CPU 核心的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1035">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="58d22-1036">现在支持套接字选项 IP_PKTINFO、IPV6_RECVPKTINFO。</span><span class="sxs-lookup"><span data-stu-id="58d22-1036">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="58d22-1037">（GH #851、987）</span><span class="sxs-lookup"><span data-stu-id="58d22-1037">(GH #851, 987)</span></span>
- <span data-ttu-id="58d22-1038">在 lxcore 中将网络接口物理地址截断为 16 个字节（GH #1452、1414、1343、468、308）</span><span class="sxs-lookup"><span data-stu-id="58d22-1038">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="58d22-1039">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1039">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1040">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1040">LTP Results:</span></span>
<span data-ttu-id="58d22-1041">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="58d22-1041">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="58d22-1042">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="58d22-1042">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="58d22-1043">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1043">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="58d22-1044">内部版本 15002</span><span class="sxs-lookup"><span data-stu-id="58d22-1044">Build 15002</span></span>

<span data-ttu-id="58d22-1045">有关内部版本 15002 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1045">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="58d22-1046">已知问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1046">Known Issue</span></span>

<span data-ttu-id="58d22-1047">两个已知问题：</span><span class="sxs-lookup"><span data-stu-id="58d22-1047">Two known issues:</span></span>
- <span data-ttu-id="58d22-1048">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="58d22-1048">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="58d22-1049">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="58d22-1049">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="58d22-1050">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="58d22-1050">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="58d22-1051">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="58d22-1051">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="58d22-1052">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="58d22-1052">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="58d22-1053">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="58d22-1053">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="58d22-1054">当 WSL 运行时，系统线程将消耗 100% 的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="58d22-1054">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="58d22-1055">根本原因已解决并已在内部修复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1055">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="58d22-1056">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1056">Fixed</span></span>

- <span data-ttu-id="58d22-1057">现在，必须在同一权限级别创建所有 bash 会话。</span><span class="sxs-lookup"><span data-stu-id="58d22-1057">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="58d22-1058">尝试在不同级别启动会话将遭到阻止。</span><span class="sxs-lookup"><span data-stu-id="58d22-1058">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="58d22-1059">这意味着，管理员和非管理员控制台不能同时运行。</span><span class="sxs-lookup"><span data-stu-id="58d22-1059">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="58d22-1060">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="58d22-1060">(GH #626)</span></span>
<br/>
- <span data-ttu-id="58d22-1061">实现了以下 NETLINK_ROUTE 消息（需要 Windows 管理员）</span><span class="sxs-lookup"><span data-stu-id="58d22-1061">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="58d22-1062">RTM_NEWADDR（支持 `ip addr add`）</span><span class="sxs-lookup"><span data-stu-id="58d22-1062">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="58d22-1063">RTM_NEWROUTE（支持 `ip route add`）</span><span class="sxs-lookup"><span data-stu-id="58d22-1063">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="58d22-1064">RTM_DELADDR（支持 `ip addr del`）</span><span class="sxs-lookup"><span data-stu-id="58d22-1064">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="58d22-1065">RTM_DELROUTE（支持 `ip route del`）</span><span class="sxs-lookup"><span data-stu-id="58d22-1065">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="58d22-1066">用于检查要更新的包的计划任务将不再在按流量计费的连接上运行 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="58d22-1066">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="58d22-1067">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="58d22-1067">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="58d22-1068">实现了 TCP_KEEPCNT 套接字选项 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="58d22-1068">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="58d22-1069">实现了 IP_MTU_DISCOVER INET 套接字选项（GH #720、717、170、69）</span><span class="sxs-lookup"><span data-stu-id="58d22-1069">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="58d22-1070">删除了旧功能，以通过 NT 路径查找从 init 运行 NT 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-1070">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="58d22-1071">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="58d22-1071">(GH #1325)</span></span>
- <span data-ttu-id="58d22-1072">修复 /dev/kmsg 的模式，以允许进行组访问/其他读取访问 (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="58d22-1072">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="58d22-1073">实现了 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="58d22-1073">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="58d22-1074">更正了进程开始时间显示为 2432 年的错误 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="58d22-1074">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="58d22-1075">已将默认 TERM 环境变量切换为 xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="58d22-1075">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="58d22-1076">修改了进程分叉期间进程提交的计算方式。</span><span class="sxs-lookup"><span data-stu-id="58d22-1076">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="58d22-1077">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="58d22-1077">(GH #1286)</span></span>
- <span data-ttu-id="58d22-1078">实现了 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="58d22-1078">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="58d22-1079">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="58d22-1079">(GH #1286)</span></span>
- <span data-ttu-id="58d22-1080">实现了 /proc/net/route 文件 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="58d22-1080">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="58d22-1081">修复了不正确本地化快捷方式名称的错误 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="58d22-1081">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="58d22-1082">修复了错误地验证程序标头必须小于（或等于）PATH_MAX 的 elf 分析逻辑。</span><span class="sxs-lookup"><span data-stu-id="58d22-1082">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="58d22-1083">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="58d22-1083">(GH #1048)</span></span>
- <span data-ttu-id="58d22-1084">为 procfs、sysfs、cgroupfs 和 binfmtfs 实现了 statfs 回调 (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="58d22-1084">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="58d22-1085">修复了 AptPackageIndexUpdate 窗口不会关闭的问题（GH #1184，GH #1193 中也有描述）</span><span class="sxs-lookup"><span data-stu-id="58d22-1085">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="58d22-1086">添加了 ASLR 个性化 ADDR_NO_RANDOMIZE 支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1086">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="58d22-1087">（GH #1148、1128）</span><span class="sxs-lookup"><span data-stu-id="58d22-1087">(GH #1148, 1128)</span></span>
- <span data-ttu-id="58d22-1088">改善了 PTRACE_GETSIGINFO、SIGSEGV，在 AV 期间会提供正确的 gdb 堆栈跟踪 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="58d22-1088">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="58d22-1089">针对 patchelf 二进制文件的 Elf 分析不再失败。</span><span class="sxs-lookup"><span data-stu-id="58d22-1089">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="58d22-1090">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="58d22-1090">(GH #471)</span></span>
- <span data-ttu-id="58d22-1091">VPN DNS 已传播到 /etc/resolv.conf（GH #416、1350）</span><span class="sxs-lookup"><span data-stu-id="58d22-1091">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="58d22-1092">TCP 关闭改进，可以更可靠地传输数据。</span><span class="sxs-lookup"><span data-stu-id="58d22-1092">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="58d22-1093">（GH #610、616、1025、1335）</span><span class="sxs-lookup"><span data-stu-id="58d22-1093">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="58d22-1094">现在，在打开过多的文件时可返回正确的错误代码 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1094">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="58d22-1095">（GH #1126、2090）</span><span class="sxs-lookup"><span data-stu-id="58d22-1095">(GH #1126, 2090)</span></span>
- <span data-ttu-id="58d22-1096">Windows 审核日志现在会在进程创建审核中报告映像名称。</span><span class="sxs-lookup"><span data-stu-id="58d22-1096">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="58d22-1097">现在，在从 bash 窗口内部启动 bash 时会正常失败</span><span class="sxs-lookup"><span data-stu-id="58d22-1097">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="58d22-1098">添加了在 interop 无法访问 LxFs 下的工作目录（即 notepad.exe .bashrc）时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="58d22-1098">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="58d22-1099">修复了 Windows 路径在 WSL 中截断的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1099">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="58d22-1100">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1100">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1101">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1101">LTP Results:</span></span>
<span data-ttu-id="58d22-1102">通过的测试数：690</span><span class="sxs-lookup"><span data-stu-id="58d22-1102">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="58d22-1103">未通过的测试数（失败、已跳过等）：274</span><span class="sxs-lookup"><span data-stu-id="58d22-1103">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="58d22-1104">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1104">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1105">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1105">Syscall Support</span></span>
<span data-ttu-id="58d22-1106">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1106">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1107">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1107">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="58d22-1108">内部版本 14986</span><span class="sxs-lookup"><span data-stu-id="58d22-1108">Build 14986</span></span>

<span data-ttu-id="58d22-1109">有关内部版本 14986 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1109">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1110">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1110">Fixed</span></span>

- <span data-ttu-id="58d22-1111">修复了 Netlink 和 Pty IOCTL 的 bug 检查</span><span class="sxs-lookup"><span data-stu-id="58d22-1111">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="58d22-1112">内核版本现在会报告 4.4.0-43，以便与 Xenial 保持一致</span><span class="sxs-lookup"><span data-stu-id="58d22-1112">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="58d22-1113">现在，当输入定向到 'nul:' 时会启动 Bash.exe (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="58d22-1113">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="58d22-1114">现在，procfs 中会正确报告线程 ID (GH #967)</span><span class="sxs-lookup"><span data-stu-id="58d22-1114">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="58d22-1115">现在，inotify_add_watch() 中支持 IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 标志 (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="58d22-1115">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="58d22-1116">实现 timer_create 和相关的系统调用。</span><span class="sxs-lookup"><span data-stu-id="58d22-1116">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="58d22-1117">这会启用 GHC 支持 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="58d22-1117">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="58d22-1118">修复了 ping 返回时间 0.000ms 的问题 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="58d22-1118">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="58d22-1119">打开过多的文件时返回正确的错误代码。</span><span class="sxs-lookup"><span data-stu-id="58d22-1119">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="58d22-1120">修复了 WSL 中的问题：如果网络接口的硬件地址为 32 字节（例如 Teredo 接口），则针对该网络接口数据的 Netlink 请求将会失败并返回 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="58d22-1120">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="58d22-1121">请注意，Linux“ip”实用工具包含一个 bug：如果 WSL 报告 32 字节硬件地址，该实用工具将会崩溃。</span><span class="sxs-lookup"><span data-stu-id="58d22-1121">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="58d22-1122">这是“ip”（而不是 WSL）中的一个 bug。</span><span class="sxs-lookup"><span data-stu-id="58d22-1122">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="58d22-1123">“ip”实用工具会将用于输出硬件地址的字符串缓冲区的长度硬编码，而该缓冲区太小，无法输出 32 字节硬件地址。</span><span class="sxs-lookup"><span data-stu-id="58d22-1123">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="58d22-1124">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1124">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1125">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1125">LTP Results:</span></span>
<span data-ttu-id="58d22-1126">通过的测试数：669</span><span class="sxs-lookup"><span data-stu-id="58d22-1126">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="58d22-1127">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="58d22-1127">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="58d22-1128">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1128">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1129">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1129">Syscall Support</span></span>
<span data-ttu-id="58d22-1130">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1130">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1131">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1131">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="58d22-1132">内部版本 14971</span><span class="sxs-lookup"><span data-stu-id="58d22-1132">Build 14971</span></span>

<span data-ttu-id="58d22-1133">有关内部版本 14971 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1133">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1134">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1134">Fixed</span></span>

 - <span data-ttu-id="58d22-1135">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="58d22-1135">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="58d22-1136">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1136">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1137">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1137">LTP Results:</span></span>
<span data-ttu-id="58d22-1138">自 14965 以来无更改</span><span class="sxs-lookup"><span data-stu-id="58d22-1138">Unchanged from 14965</span></span> </br>
<span data-ttu-id="58d22-1139">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="58d22-1139">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="58d22-1140">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1140">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1141">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1141">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="58d22-1142">内部版本 14965</span><span class="sxs-lookup"><span data-stu-id="58d22-1142">Build 14965</span></span>

<span data-ttu-id="58d22-1143">有关内部版本 14965 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1143">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1144">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1144">Fixed</span></span>

- <span data-ttu-id="58d22-1145">支持 Netlink 套接字 NETLINK_ROUTE 协议的 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="58d22-1145">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="58d22-1146">为网络枚举启用 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="58d22-1146">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="58d22-1147">在 [WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)中可以找到详细信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-1147">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="58d22-1148">/sbin 现在默认位于用户的路径中</span><span class="sxs-lookup"><span data-stu-id="58d22-1148">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="58d22-1149">NT 用户路径现在默认会追加到 WSL 路径（即，现在可以键入 notepad.exe，无需将 System32 添加到 Linux 路径）</span><span class="sxs-lookup"><span data-stu-id="58d22-1149">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="58d22-1150">添加了对 /proc/sys/kernel/cap_last_cap 的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1150">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="58d22-1151">现在，如果当前工作目录包含非 ANSI 字符，则可以从 WSL 启动 NT 二进制文件 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="58d22-1151">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="58d22-1152">允许在断开连接的 unix 流套接字上关闭。</span><span class="sxs-lookup"><span data-stu-id="58d22-1152">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="58d22-1153">添加了对 PR_GET_PDEATHSIG 的支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1153">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="58d22-1154">添加了对 CLONE_PARENT 的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1154">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="58d22-1155">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="58d22-1155">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="58d22-1156">处理连接到当前终端的请求。</span><span class="sxs-lookup"><span data-stu-id="58d22-1156">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="58d22-1157">将 /proc/<pid>/oom_score_adj 标记为可写。</span><span class="sxs-lookup"><span data-stu-id="58d22-1157">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="58d22-1158">添加 /sys/fs/cgroup 文件夹。</span><span class="sxs-lookup"><span data-stu-id="58d22-1158">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="58d22-1159">sched_setaffinity 应返回关联位掩码的数目</span><span class="sxs-lookup"><span data-stu-id="58d22-1159">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="58d22-1160">修复错误地假设解释器路径长度必须小于 64 个字符的 ELF 验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="58d22-1160">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="58d22-1161">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="58d22-1161">(GH #743)</span></span>
- <span data-ttu-id="58d22-1162">打开文件描述符会使控制台窗口保持打开状态 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="58d22-1162">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="58d22-1163">修复了当目标名称包含尾随斜杠时 rename() 失败的错误 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="58d22-1163">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="58d22-1164">实现 /proc/net/dev 文件</span><span class="sxs-lookup"><span data-stu-id="58d22-1164">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="58d22-1165">修复了计时器精度导致的 0.000ms ping 错误。</span><span class="sxs-lookup"><span data-stu-id="58d22-1165">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="58d22-1166">实现了 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="58d22-1166">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="58d22-1167">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1167">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1168">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1168">LTP Results:</span></span>
<span data-ttu-id="58d22-1169">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="58d22-1169">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="58d22-1170">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1170">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1171">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1171">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="58d22-1172">内部版本 14959</span><span class="sxs-lookup"><span data-stu-id="58d22-1172">Build 14959</span></span>

<span data-ttu-id="58d22-1173">有关内部版本 14959 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1173">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1174">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1174">Fixed</span></span>

- <span data-ttu-id="58d22-1175">改善了 Windows 的 Pico 进程通知。</span><span class="sxs-lookup"><span data-stu-id="58d22-1175">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="58d22-1176">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)中可以找到更多信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-1176">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="58d22-1177">改善了 Windows 互操作的稳定性</span><span class="sxs-lookup"><span data-stu-id="58d22-1177">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="58d22-1178">修复了在启用企业数据保护 (EDP) 后启动 bash.exe 时出现的错误 0x80070057</span><span class="sxs-lookup"><span data-stu-id="58d22-1178">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="58d22-1179">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1179">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1180">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1180">LTP Results:</span></span>
<span data-ttu-id="58d22-1181">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="58d22-1181">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="58d22-1182">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1182">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1183">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1183">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="58d22-1184">内部版本 14955</span><span class="sxs-lookup"><span data-stu-id="58d22-1184">Build 14955</span></span>

<span data-ttu-id="58d22-1185">有关内部版本 14955 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1185">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1186">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1186">Fixed</span></span>

 - <span data-ttu-id="58d22-1187">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="58d22-1187">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="58d22-1188">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1188">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1189">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1189">LTP Results:</span></span>
<span data-ttu-id="58d22-1190">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="58d22-1190">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="58d22-1191">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1191">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1192">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1192">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="58d22-1193">内部版本 14951</span><span class="sxs-lookup"><span data-stu-id="58d22-1193">Build 14951</span></span>

<span data-ttu-id="58d22-1194">有关内部版本 14951 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1194">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="58d22-1195">新功能：Windows/Ubuntu 互操作性</span><span class="sxs-lookup"><span data-stu-id="58d22-1195">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="58d22-1196">现在可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-1196">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="58d22-1197">这样，用户便可以通过前所未有的方式来与其 Windows 环境和系统交互。</span><span class="sxs-lookup"><span data-stu-id="58d22-1197">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="58d22-1198">举个简单的例子，用户现在可以运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="58d22-1198">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="58d22-1199">可在以下资源中找到详细信息：</span><span class="sxs-lookup"><span data-stu-id="58d22-1199">More information can be found at:</span></span>

- [<span data-ttu-id="58d22-1200">WSL 团队的互操作博客</span><span class="sxs-lookup"><span data-stu-id="58d22-1200">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="58d22-1201">MSDN 互操作文档</span><span class="sxs-lookup"><span data-stu-id="58d22-1201">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1202">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1202">Fixed</span></span>

- <span data-ttu-id="58d22-1203">现在将为所有新的 WSL 实例安装 Ubuntu 16.04 (Xenial)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1203">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="58d22-1204">使用现有 14.04 (Trusty) 实例的用户不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="58d22-1204">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="58d22-1205">现在会显示安装过程中指定的区域设置</span><span class="sxs-lookup"><span data-stu-id="58d22-1205">Locale set during install is now displayed</span></span>
- <span data-ttu-id="58d22-1206">终端改进，包括修复了不是总能将 WSL 进程重定向到文件的 bug</span><span class="sxs-lookup"><span data-stu-id="58d22-1206">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="58d22-1207">控制台生存期应与 bash.exe 生存期密切关联</span><span class="sxs-lookup"><span data-stu-id="58d22-1207">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="58d22-1208">控制台窗口大小应使用可视大小，而不是缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="58d22-1208">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="58d22-1209">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1209">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1210">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1210">LTP Results:</span></span>
<span data-ttu-id="58d22-1211">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="58d22-1211">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="58d22-1212">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1212">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1213">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1213">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="58d22-1214">内部版本 14946</span><span class="sxs-lookup"><span data-stu-id="58d22-1214">Build 14946</span></span>

<span data-ttu-id="58d22-1215">有关内部版本 14946 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1215">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1216">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1216">Fixed</span></span>

- <span data-ttu-id="58d22-1217">修复了阻止使用包含空格或引号的 NT 用户名为用户创建 WSL 用户帐户的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-1217">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="58d22-1218">更改 VolFs 和 DrvFs，以在统计信息中返回 0 作为目录的链接计数</span><span class="sxs-lookup"><span data-stu-id="58d22-1218">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="58d22-1219">支持 IPV6_MULTICAST_HOPS 套接字选项。</span><span class="sxs-lookup"><span data-stu-id="58d22-1219">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="58d22-1220">限制为每个 tty 只有一个控制台 I/O 循环。</span><span class="sxs-lookup"><span data-stu-id="58d22-1220">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="58d22-1221">例如，可运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="58d22-1221">Example: the following command is possible:</span></span>
  - <span data-ttu-id="58d22-1222">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="58d22-1222">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="58d22-1223">在 /proc/cpuinfo 中将空格替换为制表符 (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="58d22-1223">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="58d22-1224">DrvFs 现在会显示在 mountinfo 中，其中包含一个与已装载的 Windows 卷匹配的名称</span><span class="sxs-lookup"><span data-stu-id="58d22-1224">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="58d22-1225">/home 和 /root 现在会显示在 mountinfo 中，并显示正确的名称</span><span class="sxs-lookup"><span data-stu-id="58d22-1225">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="58d22-1226">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1226">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1227">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1227">LTP Results:</span></span>
<span data-ttu-id="58d22-1228">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="58d22-1228">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="58d22-1229">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1229">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1230">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1230">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="58d22-1231">内部版本 14942</span><span class="sxs-lookup"><span data-stu-id="58d22-1231">Build 14942</span></span>

<span data-ttu-id="58d22-1232">有关内部版本 14942 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1232">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1233">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1233">Fixed</span></span>

- <span data-ttu-id="58d22-1234">解决了一些 bug 检查，包括阻止 SSH 的“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”网络崩溃</span><span class="sxs-lookup"><span data-stu-id="58d22-1234">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="58d22-1235">inotifiy 现在支持从 DrvFs 上的 Windows 应用程序生成通知</span><span class="sxs-lookup"><span data-stu-id="58d22-1235">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="58d22-1236">实现 mongod 的 TCP_KEEPIDLE 和 TCP_KEEPINTVL。</span><span class="sxs-lookup"><span data-stu-id="58d22-1236">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="58d22-1237">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="58d22-1237">(GH #695)</span></span>
- <span data-ttu-id="58d22-1238">实现 pivot_root 系统调用</span><span class="sxs-lookup"><span data-stu-id="58d22-1238">Implement the pivot_root system call</span></span>
- <span data-ttu-id="58d22-1239">实现 SO_DONTROUTE 的套接字选项</span><span class="sxs-lookup"><span data-stu-id="58d22-1239">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="58d22-1240">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1240">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="58d22-1241">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1241">LTP Results:</span></span>
<span data-ttu-id="58d22-1242">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="58d22-1242">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="58d22-1243">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="58d22-1243">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="58d22-1244">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1244">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1245">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1245">Syscall Support</span></span>
<span data-ttu-id="58d22-1246">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1246">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1247">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1247">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="58d22-1248">内部版本 14936</span><span class="sxs-lookup"><span data-stu-id="58d22-1248">Build 14936</span></span>

<span data-ttu-id="58d22-1249">有关内部版本 14936 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1249">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="58d22-1250">注意：在即将发布的版本中，WSL 将会安装 Ubuntu 版本16.04 (Xenial) 而不是 Ubuntu 14.04 (Trusty)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1250">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="58d22-1251">此更改将应用到安装新实例的预览体验版（lxrun /install 或首次运行 bash.exe）。</span><span class="sxs-lookup"><span data-stu-id="58d22-1251">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="58d22-1252">包含 Trusty 的现有实例不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="58d22-1252">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="58d22-1253">用户可以使用 do-release-upgrade 命令将其 Trusty 映像升级到 Xenial。</span><span class="sxs-lookup"><span data-stu-id="58d22-1253">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="58d22-1254">已知问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1254">Known Issue</span></span>
<span data-ttu-id="58d22-1255">WSL 遇到了某些套接字实现的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-1255">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="58d22-1256">bug 检查将自身显示为崩溃，并出现错误“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”。</span><span class="sxs-lookup"><span data-stu-id="58d22-1256">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="58d22-1257">此问题的最常见表现形式是使用 ssh 时发生崩溃。</span><span class="sxs-lookup"><span data-stu-id="58d22-1257">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="58d22-1258">根本原因已在内部版本中修复，将会尽快推送到预览体验版。</span><span class="sxs-lookup"><span data-stu-id="58d22-1258">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="58d22-1259">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1259">Fixed</span></span>

- <span data-ttu-id="58d22-1260">实现了 chroot 系统调用</span><span class="sxs-lookup"><span data-stu-id="58d22-1260">Implemented the chroot system call</span></span>
- <span data-ttu-id="58d22-1261">inotifiy 的改进，~~包括支持从 DrvFs 上的 Windows 应用程序生成通知~~</span><span class="sxs-lookup"><span data-stu-id="58d22-1261">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="58d22-1262">更正：对源自 Windows 应用程序的更改的 Inotify 支持目前不可用。</span><span class="sxs-lookup"><span data-stu-id="58d22-1262">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="58d22-1263">与 IPV6::<port n> 的套接字绑定现在支持 IPV6_V6ONLY（GH #68、#157、#393、#460、#674、#740、#982、#996）</span><span class="sxs-lookup"><span data-stu-id="58d22-1263">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="58d22-1264">实现了 waitid 系统调用的 WNOWAIT 行为 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="58d22-1264">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="58d22-1265">支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="58d22-1265">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="58d22-1266">零长度 read() 应立即返回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="58d22-1266">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="58d22-1267">在 .tar 文件中正确处理不包含 NULL 终止符的文件名和文件名前缀。</span><span class="sxs-lookup"><span data-stu-id="58d22-1267">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="58d22-1268">对 /dev/null 的 epoll 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1268">epoll support for /dev/null</span></span>
- <span data-ttu-id="58d22-1269">修复 /dev/alarm 时间源</span><span class="sxs-lookup"><span data-stu-id="58d22-1269">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="58d22-1270">Bash -c 现在可以重定向到文件</span><span class="sxs-lookup"><span data-stu-id="58d22-1270">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="58d22-1271">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1271">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1272">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1272">LTP Results:</span></span>
<span data-ttu-id="58d22-1273">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="58d22-1273">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="58d22-1274">未通过的测试数（失败、已跳过等）：264</span><span class="sxs-lookup"><span data-stu-id="58d22-1274">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="58d22-1275">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1275">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1276">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1276">Syscall Support</span></span>
<span data-ttu-id="58d22-1277">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1277">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1278">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1278">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="58d22-1279">内部版本 14931</span><span class="sxs-lookup"><span data-stu-id="58d22-1279">Build 14931</span></span>

<span data-ttu-id="58d22-1280">有关内部版本 14931 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1280">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1281">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1281">Fixed</span></span>

 - <span data-ttu-id="58d22-1282">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="58d22-1282">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="58d22-1283">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1283">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="58d22-1284">内部版本 14926</span><span class="sxs-lookup"><span data-stu-id="58d22-1284">Build 14926</span></span>

<span data-ttu-id="58d22-1285">有关内部版本 14926 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1285">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1286">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1286">Fixed</span></span>

- <span data-ttu-id="58d22-1287">Ping 现在可以在没有管理员特权的控制台中正常运行</span><span class="sxs-lookup"><span data-stu-id="58d22-1287">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="58d22-1288">现在支持 Ping6，也无需管理员特权</span><span class="sxs-lookup"><span data-stu-id="58d22-1288">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="58d22-1289">对通过 WSL 修改的文件的 Inotify 支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1289">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="58d22-1290">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="58d22-1290">(GH #216)</span></span>
  - <span data-ttu-id="58d22-1291">支持的标志：</span><span class="sxs-lookup"><span data-stu-id="58d22-1291">Flags supported:</span></span>
    - <span data-ttu-id="58d22-1292">inotify_init1：LX_O_CLOEXEC、LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="58d22-1292">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="58d22-1293">inotify_add_watch 事件：LX_IN_ACCESS、LX_IN_MODIFY、LX_IN_ATTRIB、LX_IN_CLOSE_WRITE、LX_IN_CLOSE_NOWRITE、LX_IN_OPEN、LX_IN_MOVED_FROM、LX_IN_MOVED_TO、LX_IN_CREATE、LX_IN_DELETE、LX_IN_DELETE_SELF、LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="58d22-1293">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="58d22-1294">inotify_add_watch 属性：LX_IN_DONT_FOLLOW、LX_IN_EXCL_UNLINK、LX_IN_MASK_ADD、LX_IN_ONESHOT、LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="58d22-1294">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="58d22-1295">读取输出：LX_IN_ISDIR、LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="58d22-1295">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="58d22-1296">已知问题：修改 Windows 应用程序中的文件不会生成任何事件</span><span class="sxs-lookup"><span data-stu-id="58d22-1296">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="58d22-1297">Unix 套接字现在支持 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="58d22-1297">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="58d22-1298">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="58d22-1298">LTP Results:</span></span>
<span data-ttu-id="58d22-1299">通过的测试数：651</span><span class="sxs-lookup"><span data-stu-id="58d22-1299">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="58d22-1300">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="58d22-1300">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="58d22-1301">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="58d22-1301">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="58d22-1302">内部版本 14915</span><span class="sxs-lookup"><span data-stu-id="58d22-1302">Build 14915</span></span>

<span data-ttu-id="58d22-1303">有关内部版本 14915 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1303">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1304">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1304">Fixed</span></span>
-  <span data-ttu-id="58d22-1305">Unix 数据报套接字的套接字对 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="58d22-1305">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="58d22-1306">对 SO_REUSEADDR 的 Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1306">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="58d22-1307">对 SO_BROADCAST 的 UNIX 套接字支持 (GH #568)</span><span class="sxs-lookup"><span data-stu-id="58d22-1307">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="58d22-1308">对 SOCK_SEQPACKET 的 Unix 套接字支持（GH #758、#546）</span><span class="sxs-lookup"><span data-stu-id="58d22-1308">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="58d22-1309">添加对 Unix 数据报套接字 send、recv 和 shutdown 的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1309">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="58d22-1310">修复对非固定地址的无效 mmap 参数验证导致的 bug 检查。</span><span class="sxs-lookup"><span data-stu-id="58d22-1310">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="58d22-1311">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="58d22-1311">(GH #847)</span></span>
- <span data-ttu-id="58d22-1312">支持暂停/恢复终端状态</span><span class="sxs-lookup"><span data-stu-id="58d22-1312">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="58d22-1313">支持使用 TIOCPKT ioctl 阻止 Screen 实用工具 (GH #774)</span><span class="sxs-lookup"><span data-stu-id="58d22-1313">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="58d22-1314">已知问题：功能键不起作用</span><span class="sxs-lookup"><span data-stu-id="58d22-1314">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="58d22-1315">更正了 TimerFd 中的一种争用状态，该状态可能导致 LxpTimerFdWorkerRoutine 访问已释放的成员“ReaderReady” (GH #814)</span><span class="sxs-lookup"><span data-stu-id="58d22-1315">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="58d22-1316">为 futex、poll 和 clock_nanosleep 启用可重启系统调用支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1316">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="58d22-1317">添加了绑定装载支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1317">Added bind mount support</span></span>
- <span data-ttu-id="58d22-1318">装载命名空间支持的取消共享</span><span class="sxs-lookup"><span data-stu-id="58d22-1318">unshare for mount namespace support</span></span>
    - <span data-ttu-id="58d22-1319">已知问题：使用 `unshare(CLONE_NEWNS)` 创建新的装载命名空间时，当前工作目录将继续指向旧命名空间</span><span class="sxs-lookup"><span data-stu-id="58d22-1319">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="58d22-1320">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="58d22-1320">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="58d22-1321">内部版本 14905</span><span class="sxs-lookup"><span data-stu-id="58d22-1321">Build 14905</span></span>

<span data-ttu-id="58d22-1322">有关内部版本 14905 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1322">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1323">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1323">Fixed</span></span>
- <span data-ttu-id="58d22-1324">现在支持可重启系统调用（GH #349、GH #520）</span><span class="sxs-lookup"><span data-stu-id="58d22-1324">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="58d22-1325">现在可正常使用指向以 / 结尾的目录的符号链接 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="58d22-1325">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="58d22-1326">为 /dev/random 实现了 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="58d22-1326">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="58d22-1327">实现了 /proc/[pid]/mounts、/proc/[pid]/mountinfo 和 /proc/[pid]/mountstats 文件</span><span class="sxs-lookup"><span data-stu-id="58d22-1327">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="58d22-1328">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1328">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="58d22-1329">内部版本 14901</span><span class="sxs-lookup"><span data-stu-id="58d22-1329">Build 14901</span></span>
<span data-ttu-id="58d22-1330">Windows 10 周年更新版的第一个预览体验内部版本。</span><span class="sxs-lookup"><span data-stu-id="58d22-1330">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="58d22-1331">有关内部版本 14901 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1331">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1332">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1332">Fixed</span></span>
- <span data-ttu-id="58d22-1333">修复了尾随斜杠问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1333">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="58d22-1334">`$ mv a/c/ a/b/` 等命令现在可正常运行</span><span class="sxs-lookup"><span data-stu-id="58d22-1334">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="58d22-1335">安装程序现在会提示是否应将 Ubuntu 区域设置指定为 Windows 区域设置</span><span class="sxs-lookup"><span data-stu-id="58d22-1335">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="58d22-1336">对 ns 文件夹的 Procfs 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1336">Procfs support for ns folder</span></span>
- <span data-ttu-id="58d22-1337">添加了 tmpfs、procfs 和 sysfs 文件系统的装入点和卸载点</span><span class="sxs-lookup"><span data-stu-id="58d22-1337">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="58d22-1338">修复 mknod [at] 32 位 ABI 签名</span><span class="sxs-lookup"><span data-stu-id="58d22-1338">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="58d22-1339">Unix 套接字已移到调度模型</span><span class="sxs-lookup"><span data-stu-id="58d22-1339">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="58d22-1340">应遵循使用 setsockopt 设置的 INET 套接字接收缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="58d22-1340">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="58d22-1341">实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志</span><span class="sxs-lookup"><span data-stu-id="58d22-1341">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="58d22-1342">Linux 进程 stdin/stdout 管道重定向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="58d22-1342">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="58d22-1343">允许在 CMD 中使用竖线分隔 bash -c 命令。</span><span class="sxs-lookup"><span data-stu-id="58d22-1343">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="58d22-1344">示例：>dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="58d22-1344">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="58d22-1345">Bash 现在可以安装在包含多个页面文件的系统上（GH #538、#358）</span><span class="sxs-lookup"><span data-stu-id="58d22-1345">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="58d22-1346">默认的 INET 套接字缓冲区大小应与默认 Ubuntu 安装的大小相匹配</span><span class="sxs-lookup"><span data-stu-id="58d22-1346">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="58d22-1347">将 xattr syscall 与 listxattr 对齐</span><span class="sxs-lookup"><span data-stu-id="58d22-1347">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="58d22-1348">仅返回使用 SIOCGIFCONF 中有效 IPv4 地址的接口</span><span class="sxs-lookup"><span data-stu-id="58d22-1348">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="58d22-1349">修复 ptrace 注入时的信号默认操作</span><span class="sxs-lookup"><span data-stu-id="58d22-1349">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="58d22-1350">实现 /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="58d22-1350">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="58d22-1351">在 sigreturn 中还原上下文时使用计算机上下文寄存器值</span><span class="sxs-lookup"><span data-stu-id="58d22-1351">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="58d22-1352">这解决了某些用户遇到的 java 和 javac 挂起问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1352">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="58d22-1353">实现 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="58d22-1353">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1354">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1354">Syscall Support</span></span>
<span data-ttu-id="58d22-1355">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1355">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1356">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1356">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="58d22-1357">Windows 10 周年更新的内部版本 14388</span><span class="sxs-lookup"><span data-stu-id="58d22-1357">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="58d22-1358">有关内部版本 14388 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1358">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1359">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1359">Fixed</span></span>
- <span data-ttu-id="58d22-1360">修复在 8/2 准备 Windows 10 周年更新时出现的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1360">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="58d22-1361">可在我们的[博客](https://blogs.msdn.microsoft.com/wsl/)中找到有关周年更新中的 WSL 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-1361">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="58d22-1362">内部版本 14376</span><span class="sxs-lookup"><span data-stu-id="58d22-1362">Build 14376</span></span>
<span data-ttu-id="58d22-1363">有关内部版本 14376 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1363">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1364">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1364">Fixed</span></span>
- <span data-ttu-id="58d22-1365">删除了一些存在 apt-get 挂起问题的实例 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="58d22-1365">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="58d22-1366">修复了不正确处理空装入点的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1366">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="58d22-1367">修复了不正确装载 ramdisk 的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1367">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="58d22-1368">更改 unix 套接字接受行为以支持标志（在 GH #451 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="58d22-1368">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="58d22-1369">修复了与网络相关的常见蓝屏问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1369">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="58d22-1370">修复了访问 /proc/[pid]/task 时出现蓝屏的问题 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="58d22-1370">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="58d22-1371">修复了在某些 pty 方案中 CPU 利用率偏高的问题（GH #488、#504）</span><span class="sxs-lookup"><span data-stu-id="58d22-1371">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="58d22-1372">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1372">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="58d22-1373">内部版本 14371</span><span class="sxs-lookup"><span data-stu-id="58d22-1373">Build 14371</span></span>
<span data-ttu-id="58d22-1374">有关内部版本 14371 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1374">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1375">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1375">Fixed</span></span>
- <span data-ttu-id="58d22-1376">更正了使用 ptrace 时 SIGCHLD 和 wait() 出现计时争用的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1376">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="58d22-1377">更正了当路径包含尾随 / 时出现的某种行为 (GH #432)</span><span class="sxs-lookup"><span data-stu-id="58d22-1377">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="58d22-1378">修复了由于打开子级句柄导致重命名/取消链接失败的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1378">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="58d22-1379">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1379">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="58d22-1380">内部版本 14366</span><span class="sxs-lookup"><span data-stu-id="58d22-1380">Build 14366</span></span>
<span data-ttu-id="58d22-1381">有关内部版本 14366 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1381">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1382">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1382">Fixed</span></span>
- <span data-ttu-id="58d22-1383">修复通过符号链接创建文件的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1383">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="58d22-1384">添加了 Python 的 listxattr (GH 385)</span><span class="sxs-lookup"><span data-stu-id="58d22-1384">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="58d22-1385">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1385">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1386">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1386">Syscall Support</span></span>
-   <span data-ttu-id="58d22-1387">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1387">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1388">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1388">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="58d22-1389">内部版本 14361</span><span class="sxs-lookup"><span data-stu-id="58d22-1389">Build 14361</span></span>
<span data-ttu-id="58d22-1390">有关内部版本 14361 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1390">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1391">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1391">Fixed</span></span>
- <span data-ttu-id="58d22-1392">现在，在 Windows 上的 Ubuntu Bash 中运行时，DrvFs 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-1392">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="58d22-1393">用户可在其 /mnt/c 驱动器中保存 case.txt 和 CASE.TXT</span><span class="sxs-lookup"><span data-stu-id="58d22-1393">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="58d22-1394">只有 Windows 上的 Ubuntu Bash 支持区分大小写。</span><span class="sxs-lookup"><span data-stu-id="58d22-1394">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="58d22-1395">在 Bash 外部，NTFS 会正确报告文件，但在与 Windows 中的文件交互时，可能会出现意外的行为。</span><span class="sxs-lookup"><span data-stu-id="58d22-1395">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="58d22-1396">每个卷的根目录（即 /mnt/c）不区分大小写</span><span class="sxs-lookup"><span data-stu-id="58d22-1396">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="58d22-1397">可在[此处](https://support.microsoft.com/en-us/kb/100625)找到有关处理 Windows 中的这些文件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-1397">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="58d22-1398">大幅增强了 pty/tty 支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1398">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="58d22-1399">现在支持 TMUX 等应用程序 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="58d22-1399">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="58d22-1400">修复了不总会创建用户帐户的安装问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1400">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="58d22-1401">优化了命令行参数结构，允许极长的参数列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1401">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="58d22-1402">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="58d22-1402">(GH #153)</span></span>
- <span data-ttu-id="58d22-1403">现在可对 DrvFs 中的只读文件执行删除和 chmod</span><span class="sxs-lookup"><span data-stu-id="58d22-1403">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="58d22-1404">修复了一些在断开连接时终端会挂起的实例 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="58d22-1404">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="58d22-1405">现在可在 tty 设备上正常运行 chmod 和 chown</span><span class="sxs-lookup"><span data-stu-id="58d22-1405">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="58d22-1406">允许连接到作为 localhost 的 0.0.0.0 和 :: (GH #388)</span><span class="sxs-lookup"><span data-stu-id="58d22-1406">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="58d22-1407">Sendmsg/recvmsg 现在可处理大于 1 的 IO 矢量长度（在 GH #376 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="58d22-1407">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="58d22-1408">用户现在可以选择禁用自动生成的 hosts 文件 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="58d22-1408">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="58d22-1409">在安装期间自动将 Linux 区域设置与 NT 区域设置进行匹配 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="58d22-1409">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="58d22-1410">添加了 /proc/sys/vm/swappiness 文件 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="58d22-1410">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="58d22-1411">strace 现在会正常退出</span><span class="sxs-lookup"><span data-stu-id="58d22-1411">strace now exits correctly</span></span>
- <span data-ttu-id="58d22-1412">允许通过 /proc/self/fd 重新打开管道 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="58d22-1412">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="58d22-1413">在 DrvFs 中隐藏 %LOCALAPPDATA%\lxss 下的目录 (GH #270)</span><span class="sxs-lookup"><span data-stu-id="58d22-1413">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="58d22-1414">更好地处理 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="58d22-1414">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="58d22-1415">现在支持类似于“bash ~ -c ls”的命令 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="58d22-1415">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="58d22-1416">现在，在关闭期间，套接字会通知 epoll read 可用 (GH #271)</span><span class="sxs-lookup"><span data-stu-id="58d22-1416">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="58d22-1417">lxrun /uninstall 可以更好地删除文件和文件夹</span><span class="sxs-lookup"><span data-stu-id="58d22-1417">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="58d22-1418">更正了 ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="58d22-1418">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="58d22-1419">改善了对 xEmacs 等 x11 应用的支持 (GH #481)</span><span class="sxs-lookup"><span data-stu-id="58d22-1419">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="58d22-1420">更新了初始线程堆栈大小，以匹配默认的 Ubuntu 设置，并正确地向 get_rlimit syscall 报告大小（GH #172、#258）</span><span class="sxs-lookup"><span data-stu-id="58d22-1420">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="58d22-1421">改善了 pico 进程映像名称的报告（例如，用于审核）</span><span class="sxs-lookup"><span data-stu-id="58d22-1421">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="58d22-1422">实现了 df 命令的 /proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="58d22-1422">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="58d22-1423">修复了子名称 .</span><span class="sxs-lookup"><span data-stu-id="58d22-1423">Fixed symlink error code for child name .</span></span> <span data-ttu-id="58d22-1424">和 .. 的符号链接错误代码</span><span class="sxs-lookup"><span data-stu-id="58d22-1424">and ..</span></span>
- <span data-ttu-id="58d22-1425">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1425">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1426">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1426">Syscall Support</span></span>
<span data-ttu-id="58d22-1427">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1427">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1428">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1428">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="58d22-1429">内部版本 14352</span><span class="sxs-lookup"><span data-stu-id="58d22-1429">Build 14352</span></span>
<span data-ttu-id="58d22-1430">有关内部版本 14352 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1430">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1431">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1431">Fixed</span></span>
- <span data-ttu-id="58d22-1432">修复了不正常下载/创建大型文件的问题。</span><span class="sxs-lookup"><span data-stu-id="58d22-1432">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="58d22-1433">这应该可以解除 npm 和其他方案的阻碍（GH #3、GH #313）</span><span class="sxs-lookup"><span data-stu-id="58d22-1433">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="58d22-1434">删除了一些存在套接字挂起情况的实例</span><span class="sxs-lookup"><span data-stu-id="58d22-1434">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="58d22-1435">更正了一些 ptrace 错误</span><span class="sxs-lookup"><span data-stu-id="58d22-1435">Corrected some ptrace errors</span></span>
- <span data-ttu-id="58d22-1436">修复了 WSL 中的问题，允许超过 255 个字符的文件名</span><span class="sxs-lookup"><span data-stu-id="58d22-1436">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="58d22-1437">改善了对非英语字符的支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1437">Improved support for non-English characters</span></span>
- <span data-ttu-id="58d22-1438">添加当前 Windows 时区数据并将其设为默认值</span><span class="sxs-lookup"><span data-stu-id="58d22-1438">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="58d22-1439">每个装入点的唯一设备 ID （JRE 修复 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="58d22-1439">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="58d22-1440">更正路径中包含“.”</span><span class="sxs-lookup"><span data-stu-id="58d22-1440">Correct issue with paths containing “.”</span></span> <span data-ttu-id="58d22-1441">和“..”的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1441">and “..”</span></span>
- <span data-ttu-id="58d22-1442">添加了 Fifo 支持 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="58d22-1442">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="58d22-1443">更新了 resolv.conf 的格式，以匹配本机 Ubuntu 格式</span><span class="sxs-lookup"><span data-stu-id="58d22-1443">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="58d22-1444">一些 procfs 清理</span><span class="sxs-lookup"><span data-stu-id="58d22-1444">Some procfs cleanup</span></span>
- <span data-ttu-id="58d22-1445">为管理员控制台启用了 ping (GH #18)</span><span class="sxs-lookup"><span data-stu-id="58d22-1445">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1446">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1446">Syscall Support</span></span>
<span data-ttu-id="58d22-1447">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1447">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1448">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1448">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="58d22-1449">内部版本 14342</span><span class="sxs-lookup"><span data-stu-id="58d22-1449">Build 14342</span></span>
<span data-ttu-id="58d22-1450">有关内部版本 14342 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1450">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="58d22-1451">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl)中可以找到有关 VolFs 和 DriveFs 的信息。</span><span class="sxs-lookup"><span data-stu-id="58d22-1451">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="58d22-1452">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1452">Fixed</span></span>
- <span data-ttu-id="58d22-1453">修复了 Windows 用户在用户名中包含 Unicode 字符时出现的安装问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1453">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="58d22-1454">现在，在首次运行时，默认会提供“常见问题解答”中的 apt-get update udev 解决方法</span><span class="sxs-lookup"><span data-stu-id="58d22-1454">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="58d22-1455">在 DriveFs (/mnt/<drive>) 目录中启用了符号链接</span><span class="sxs-lookup"><span data-stu-id="58d22-1455">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="58d22-1456">现在可以在 DriveFs 和 VolFs 之间使用符号链接</span><span class="sxs-lookup"><span data-stu-id="58d22-1456">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="58d22-1457">解决了顶级路径分析问题：ls .// 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="58d22-1457">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="58d22-1458">DriveFs 上的 npm install 和 -g 选项现在可正常工作</span><span class="sxs-lookup"><span data-stu-id="58d22-1458">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="58d22-1459">修复了阻止 PHP 服务器启动的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1459">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="58d22-1460">更新了默认环境值（例如 $PATH），以便与本机 Ubuntu 更匹配</span><span class="sxs-lookup"><span data-stu-id="58d22-1460">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="58d22-1461">在 Windows 中添加了每周维护任务以更新 apt 包缓存</span><span class="sxs-lookup"><span data-stu-id="58d22-1461">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="58d22-1462">修复了 ELF 标头验证的问题，WSL 现在支持所有 Melkor 选项</span><span class="sxs-lookup"><span data-stu-id="58d22-1462">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="58d22-1463">Zsh shell 可正常运行</span><span class="sxs-lookup"><span data-stu-id="58d22-1463">Zsh shell is functional</span></span>
- <span data-ttu-id="58d22-1464">现在支持预编译的 Go 二进制文件</span><span class="sxs-lookup"><span data-stu-id="58d22-1464">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="58d22-1465">现已正确本地化首次运行 Bash 时出现的提示</span><span class="sxs-lookup"><span data-stu-id="58d22-1465">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="58d22-1466">/proc/meminfo 现在会返回正确的信息</span><span class="sxs-lookup"><span data-stu-id="58d22-1466">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="58d22-1467">VFS 现在支持套接字</span><span class="sxs-lookup"><span data-stu-id="58d22-1467">Sockets now supported in VFS</span></span>
- <span data-ttu-id="58d22-1468">/dev 现在装载为 tempfs</span><span class="sxs-lookup"><span data-stu-id="58d22-1468">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="58d22-1469">现在支持 Fifo</span><span class="sxs-lookup"><span data-stu-id="58d22-1469">Fifo now supported</span></span>
- <span data-ttu-id="58d22-1470">多核系统现在会在 /proc/cpuinfo 中正确显示</span><span class="sxs-lookup"><span data-stu-id="58d22-1470">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="58d22-1471">其他改进以及首次运行期间下载内容时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="58d22-1471">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="58d22-1472">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1472">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="58d22-1473">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="58d22-1473">Supported syscall list below.</span></span>
- <span data-ttu-id="58d22-1474">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1474">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="58d22-1475">已知问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1475">Known Issues</span></span>
- <span data-ttu-id="58d22-1476">在某些情况下，</span><span class="sxs-lookup"><span data-stu-id="58d22-1476">Not resolving ‘..’</span></span> <span data-ttu-id="58d22-1477">不会正确解析 DriveFs 上的“..”</span><span class="sxs-lookup"><span data-stu-id="58d22-1477">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1478">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1478">Syscall Support</span></span>
<span data-ttu-id="58d22-1479">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1479">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="58d22-1480">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1480">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="58d22-1481">内部版本 14332</span><span class="sxs-lookup"><span data-stu-id="58d22-1481">Build 14332</span></span>

<span data-ttu-id="58d22-1482">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1482">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="58d22-1483">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1483">Fixed</span></span>
- <span data-ttu-id="58d22-1484">更好地生成 resolv.conf，包括指定 DNS 项的优先级</span><span class="sxs-lookup"><span data-stu-id="58d22-1484">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="58d22-1485">在 /mnt 与非 /mnt 驱动器之间移动文件和目录时出现的问题</span><span class="sxs-lookup"><span data-stu-id="58d22-1485">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="58d22-1486">现在可以使用符号链接创建 Tar 文件。</span><span class="sxs-lookup"><span data-stu-id="58d22-1486">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="58d22-1487">创建实例时会添加默认的 /run/lock 目录</span><span class="sxs-lookup"><span data-stu-id="58d22-1487">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="58d22-1488">更新 /dev/null 以返回正确的统计信息</span><span class="sxs-lookup"><span data-stu-id="58d22-1488">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="58d22-1489">首次运行期间下载内容时出现的其他错误</span><span class="sxs-lookup"><span data-stu-id="58d22-1489">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="58d22-1490">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1490">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="58d22-1491">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="58d22-1491">Supported syscall list below.</span></span>
- <span data-ttu-id="58d22-1492">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1492">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1493">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1493">Syscall Support</span></span>
<span data-ttu-id="58d22-1494">下面是在 WSL 中具有某种实现的新 syscall。</span><span class="sxs-lookup"><span data-stu-id="58d22-1494">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="58d22-1495">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1495">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="58d22-1496">内部版本 14328</span><span class="sxs-lookup"><span data-stu-id="58d22-1496">Build 14328</span></span>

<span data-ttu-id="58d22-1497">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="58d22-1497">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="58d22-1498">新功能</span><span class="sxs-lookup"><span data-stu-id="58d22-1498">New Features</span></span>
* <span data-ttu-id="58d22-1499">现在支持 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="58d22-1499">Now support Linux users.</span></span>  <span data-ttu-id="58d22-1500">安装 Windows 上的 Ubuntu Bash 时会提示创建 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="58d22-1500">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="58d22-1501">有关详细信息，请访问 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="58d22-1501">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="58d22-1502">现在，主机名将设置为 Windows 计算机名，而不再是 @localhost</span><span class="sxs-lookup"><span data-stu-id="58d22-1502">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="58d22-1503">有关内部版本 14328 的详细信息，请访问： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="58d22-1503">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="58d22-1504">固定</span><span class="sxs-lookup"><span data-stu-id="58d22-1504">Fixed</span></span>
* <span data-ttu-id="58d22-1505">非 /mnt/<drive> 文件的符号链接改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1505">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="58d22-1506">现在可正常运行 npm install</span><span class="sxs-lookup"><span data-stu-id="58d22-1506">npm install now works</span></span>
    * <span data-ttu-id="58d22-1507">现在可以根据[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)的说明安装 jdk/jre。</span><span class="sxs-lookup"><span data-stu-id="58d22-1507">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="58d22-1508">已知问题：符号链接不适用于 Windows 装载。</span><span class="sxs-lookup"><span data-stu-id="58d22-1508">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="58d22-1509">此功能将在以后的内部版本中可用</span><span class="sxs-lookup"><span data-stu-id="58d22-1509">Functionality will be available in a later build</span></span>
* <span data-ttu-id="58d22-1510">现在会显示 top 和 htop</span><span class="sxs-lookup"><span data-stu-id="58d22-1510">top and htop now display</span></span>
* <span data-ttu-id="58d22-1511">有关某些安装失败的其他错误消息</span><span class="sxs-lookup"><span data-stu-id="58d22-1511">Additional error messages for some install failures</span></span>
* <span data-ttu-id="58d22-1512">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="58d22-1512">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="58d22-1513">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="58d22-1513">Supported syscall list below.</span></span>
* <span data-ttu-id="58d22-1514">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="58d22-1514">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="58d22-1515">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="58d22-1515">Syscall Support</span></span>
<span data-ttu-id="58d22-1516">下面是在 WSL 中具有某种实现的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="58d22-1516">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="58d22-1517">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="58d22-1517">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
