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
ms.openlocfilehash: dbc041c98081563d4f77b9fc186698fad8299c0d
ms.sourcegitcommit: 4beb93f80749ab4c8c6f0e6920ab7f809567e243
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/17/2019
ms.locfileid: "72549578"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="f6e86-105">适用于 Linux 的 Windows 子系统发行说明</span><span class="sxs-lookup"><span data-stu-id="f6e86-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-19002"></a><span data-ttu-id="f6e86-106">版本 19002</span><span class="sxs-lookup"><span data-stu-id="f6e86-106">Build 19002</span></span>
<span data-ttu-id="f6e86-107">有关版本 19002 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-107">For general Windows information on build 19002 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/17/announcing-windows-10-insider-preview-build-19002/).</span></span>

* <span data-ttu-id="f6e86-108">[WSL] 解决了有关处理某些 Unicode 字符的问题： https://github.com/microsoft/terminal/issues/2770</span><span class="sxs-lookup"><span data-stu-id="f6e86-108">[WSL] Fix issue with handling of some Unicode characters: https://github.com/microsoft/terminal/issues/2770</span></span>
* <span data-ttu-id="f6e86-109">[WSL] 解决了在版本到版本升级后立即启动时可能会注销发行版的罕见情况。</span><span class="sxs-lookup"><span data-stu-id="f6e86-109">[WSL] Fix rare cases where distros could be unregistered if launched immediately after a build-to-build upgrade.</span></span>
* <span data-ttu-id="f6e86-110">[WSL] 解决了 wsl.exe --shutdown 的以下小问题：无法取消实例空闲计时器。</span><span class="sxs-lookup"><span data-stu-id="f6e86-110">[WSL] Fix minor issue with wsl.exe --shutdown where instance idle timers were not cancelled.</span></span>

## <a name="build-18995"></a><span data-ttu-id="f6e86-111">内部版本 18995</span><span class="sxs-lookup"><span data-stu-id="f6e86-111">Build 18995</span></span>
<span data-ttu-id="f6e86-112">有关内部版本 18995 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-112">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="f6e86-113">[WSL2] 修复了 DrvFs 装载在某项操作被中断（例如 ctrl-c）后失效的问题 [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="f6e86-113">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="f6e86-114">[WSL2] 修复了处理极大型 hvsocket 消息的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="f6e86-114">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="f6e86-115">[WSL2] 修复了当 stdin 为文件时互操作出现的问题 [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="f6e86-115">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="f6e86-116">[WSL2] 修复了当遇到意外网络状态时服务崩溃的问题 [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="f6e86-116">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="f6e86-117">[WSL2] 在当前进程没有环境变量的情况下从互操作服务器查询发行版名称</span><span class="sxs-lookup"><span data-stu-id="f6e86-117">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="f6e86-118">[WSL2] 修复了当 stdin 为文件时互操作出现的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-118">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="f6e86-119">[WSL2] 将 Linux 内核版本更新到 4.19.72</span><span class="sxs-lookup"><span data-stu-id="f6e86-119">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="f6e86-120">[WSL2] 添加了通过 .wslconfig 指定其他内核命令行参数的功能</span><span class="sxs-lookup"><span data-stu-id="f6e86-120">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments

```

## <a name="build-18990"></a><span data-ttu-id="f6e86-121">版本 18990</span><span class="sxs-lookup"><span data-stu-id="f6e86-121">Build 18990</span></span>
<span data-ttu-id="f6e86-122">有关版本 18990 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-122">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="f6e86-123">提高 \\\\wsl$ 中目录列表的性能</span><span class="sxs-lookup"><span data-stu-id="f6e86-123">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="f6e86-124">[WSL2] 注入额外的启动熵 [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="f6e86-124">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="f6e86-125">[WSL2] 修复使用 su/sudo 时的 Windows 互操作 [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="f6e86-125">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>

## <a name="build-18980"></a><span data-ttu-id="f6e86-126">内部版本 18980</span><span class="sxs-lookup"><span data-stu-id="f6e86-126">Build 18980</span></span>
<span data-ttu-id="f6e86-127">有关内部版本 18980 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-127">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="f6e86-128">修复拒绝 FILE_READ_DATA 的读取符号链接。</span><span class="sxs-lookup"><span data-stu-id="f6e86-128">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="f6e86-129">这包括 Windows 为了实现后向兼容而创建的所有符号链接（例如“C:\Document and Settings”），以及用户配置文件目录中的一些符号链接。</span><span class="sxs-lookup"><span data-stu-id="f6e86-129">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="f6e86-130">使意外的文件系统状态变得不严重 [GH 4334、4305]</span><span class="sxs-lookup"><span data-stu-id="f6e86-130">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="f6e86-131">[WSL2] 添加当 CPU/固件支持虚拟化时对 arm64 的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-131">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="f6e86-132">[WSL2] 允许无特权用户查看内核日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-132">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="f6e86-133">[WSL2] 修复关闭 stdout/stderr 套接字后的输出中继 [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="f6e86-133">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="f6e86-134">[WSL2] 支持电池和交流适配器直通</span><span class="sxs-lookup"><span data-stu-id="f6e86-134">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="f6e86-135">[WSL2] 将 Linux 内核更新到 4.19.67</span><span class="sxs-lookup"><span data-stu-id="f6e86-135">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="f6e86-136">添加在 /etc/wsl.conf 中设置默认用户名的功能：</span><span class="sxs-lookup"><span data-stu-id="f6e86-136">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="f6e86-137">内部版本 18975</span><span class="sxs-lookup"><span data-stu-id="f6e86-137">Build 18975</span></span>
<span data-ttu-id="f6e86-138">有关内部版本 18975 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-138">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="f6e86-139">[WSL2] 修复大量 localhost 可靠性问题 [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="f6e86-139">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="f6e86-140">内部版本 18970</span><span class="sxs-lookup"><span data-stu-id="f6e86-140">Build 18970</span></span>
<span data-ttu-id="f6e86-141">有关内部版本 18970 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-141">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="f6e86-142">[WSL2] 当系统从睡眠状态恢复时，使时间与主机时间同步 [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="f6e86-142">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="f6e86-143">[WSL2] 在可能的情况下，在 Windows 卷上创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="f6e86-143">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="f6e86-144">[WSL2] 在 UTS、IPC、PID 和 Mount 命名空间中创建分发版。</span><span class="sxs-lookup"><span data-stu-id="f6e86-144">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="f6e86-145">[WSL2] 修复当服务器直接绑定到 localhost 时的 localhost 端口中继 [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="f6e86-145">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="f6e86-146">[WSL2] 修复重定向输出时的 interop [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="f6e86-146">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="f6e86-147">[WSL2] 支持转换绝对 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="f6e86-147">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="f6e86-148">[WSL2] 将内核更新到 4.19.59</span><span class="sxs-lookup"><span data-stu-id="f6e86-148">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="f6e86-149">[WSL2] 正确设置 eth0 的子网掩码。</span><span class="sxs-lookup"><span data-stu-id="f6e86-149">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="f6e86-150">[WSL2] 发出退出事件信号时更改逻辑，以中断控制台工作线程循环。</span><span class="sxs-lookup"><span data-stu-id="f6e86-150">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="f6e86-151">[WSL2] 分发版未运行时弹出分发版 VHD。</span><span class="sxs-lookup"><span data-stu-id="f6e86-151">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="f6e86-152">[WSL2] 修复配置分析库以正确处理空值。</span><span class="sxs-lookup"><span data-stu-id="f6e86-152">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="f6e86-153">[WSL2] 通过创建跨分发版装入点来支持 Docker Desktop。</span><span class="sxs-lookup"><span data-stu-id="f6e86-153">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="f6e86-154">分发版可以通过将以下行添加到 /etc/wsl.conf 文件来启用此行为：</span><span class="sxs-lookup"><span data-stu-id="f6e86-154">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="f6e86-155">内部版本 18945</span><span class="sxs-lookup"><span data-stu-id="f6e86-155">Build 18945</span></span>
<span data-ttu-id="f6e86-156">有关内部版本 18945 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-156">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-157">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-157">WSL</span></span>
* <span data-ttu-id="f6e86-158">[WSL2] 允许侦听可使用 localhost:port 通过主机访问的 WSL2 中的 TCP 套接字</span><span class="sxs-lookup"><span data-stu-id="f6e86-158">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="f6e86-159">[WSL2] 修复安装/转换失败和其他诊断，以跟踪将来的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="f6e86-159">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="f6e86-160">[WSL2] 改善 WSL2 网络问题的诊断</span><span class="sxs-lookup"><span data-stu-id="f6e86-160">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="f6e86-161">[WSL2] 将内核版本更新到 4.19.55</span><span class="sxs-lookup"><span data-stu-id="f6e86-161">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="f6e86-162">[WSL2] 使用 Docker 所需的配置选项更新了内核 [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="f6e86-162">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="f6e86-163">[WSL2] 增加分配给轻型实用程序 VM 的 CPU 数目，使其与主机相同（以前，内核配置中的 CONFIG_NR_CPUS 将数目限制为 8 个）[GH 4137]</span><span class="sxs-lookup"><span data-stu-id="f6e86-163">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="f6e86-164">[WSL2] 为 WSL2 轻型 VM 创建交换文件</span><span class="sxs-lookup"><span data-stu-id="f6e86-164">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="f6e86-165">[WSL2] 允许通过 \\\\wsl$\\distro（例如 sshfs）显示用户装入点 [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="f6e86-165">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="f6e86-166">[WSL2] 改善 9p 文件系统的性能</span><span class="sxs-lookup"><span data-stu-id="f6e86-166">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="f6e86-167">[WSL2] 确保 VHD ACL 不会无限增长 [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="f6e86-167">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="f6e86-168">[WSL2] 更新内核配置以支持 squashfs 和 xt_conntrack [GH 4107、4123]</span><span class="sxs-lookup"><span data-stu-id="f6e86-168">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="f6e86-169">[WSL2] 修复 interop.enabled /etc/wsl.conf 选项 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="f6e86-169">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="f6e86-170">[WSL2] 如果文件系统不支持 EA，则返回 ENOTSUP</span><span class="sxs-lookup"><span data-stu-id="f6e86-170">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="f6e86-171">[WSL2] 修复 \\\\wsl$ 时 CopyFile 挂起的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-171">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="f6e86-172">将默认 umask 切换为 0022，并将 filesystem.umask 设置添加到 /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="f6e86-172">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="f6e86-173">修复 wslpath 以正确解析符号链接，这是19h1 中的回归 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="f6e86-173">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="f6e86-174">引入 %UserProfile%\\.wslconfig 文件用于调整 WSL2 设置</span><span class="sxs-lookup"><span data-stu-id="f6e86-174">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="f6e86-175">内部版本 18917</span><span class="sxs-lookup"><span data-stu-id="f6e86-175">Build 18917</span></span>
<span data-ttu-id="f6e86-176">有关内部版本 18917 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-176">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-177">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-177">WSL</span></span>
* <span data-ttu-id="f6e86-178">WSL 2 现已推出！</span><span class="sxs-lookup"><span data-stu-id="f6e86-178">WSL 2 is now available!</span></span> <span data-ttu-id="f6e86-179">有关更多详细信息，请参阅[博客](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-179">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="f6e86-180">修复一个回归问题：无法通过符号链接启动 Windows 进程 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="f6e86-180">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="f6e86-181">将 wsl.exe --list --verbose、wsl.exe --list --quiet 和 wsl.exe --import --version 选项添加到 wsl.exe</span><span class="sxs-lookup"><span data-stu-id="f6e86-181">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="f6e86-182">添加 wsl.exe --shutdown 选项</span><span class="sxs-lookup"><span data-stu-id="f6e86-182">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="f6e86-183">Plan 9：允许打开目录以使写入成功</span><span class="sxs-lookup"><span data-stu-id="f6e86-183">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="f6e86-184">内部版本 18890</span><span class="sxs-lookup"><span data-stu-id="f6e86-184">Build 18890</span></span>
<span data-ttu-id="f6e86-185">有关内部版本 18890 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-185">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-186">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-186">WSL</span></span>
* <span data-ttu-id="f6e86-187">非阻塞套接字泄露 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="f6e86-187">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="f6e86-188">在终端中输入 EOF 可能会阻塞后续读取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="f6e86-188">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="f6e86-189">更新 resolv.conf 标头以引用 wsl.conf [在 GH 3928 中介绍]</span><span class="sxs-lookup"><span data-stu-id="f6e86-189">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="f6e86-190">epoll delete 代码中的死锁 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="f6e86-190">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="f6e86-191">处理 --import 和 –export 的参数中的空格 [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="f6e86-191">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="f6e86-192">无法正常扩展 mmap 的文件 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="f6e86-192">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="f6e86-193">修复了 ARM64 \\\\wsl$ 访问不正常的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-193">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="f6e86-194">为 wsl.exe 添加更好的默认图标</span><span class="sxs-lookup"><span data-stu-id="f6e86-194">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="f6e86-195">内部版本 18342</span><span class="sxs-lookup"><span data-stu-id="f6e86-195">Build 18342</span></span>
<span data-ttu-id="f6e86-196">有关内部版本 18342 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-196">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-197">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-197">WSL</span></span>
* <span data-ttu-id="f6e86-198">我们添加了相应的功能，使用户能够从 Windows 访问 WSL 分发版中的 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-198">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="f6e86-199">可以通过命令行访问这些文件，此外，文件资源管理器、VSCode 等 Windows 应用可与这些文件交互。</span><span class="sxs-lookup"><span data-stu-id="f6e86-199">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="f6e86-200">通过导航到 \\\\wsl$\\<分发版名称> 访问文件，或通过导航到 \\\\wsl$ 来查看正在运行的分发版列表</span><span class="sxs-lookup"><span data-stu-id="f6e86-200">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="f6e86-201">添加额外的 CPU 信息标记，并修复 Cpus_allowed[_list] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="f6e86-201">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="f6e86-202">支持从非领先线程执行 [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="f6e86-202">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="f6e86-203">将配置更新失败视为非严重错误 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="f6e86-203">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="f6e86-204">更新 binfmt 以正确处理偏移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="f6e86-204">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="f6e86-205">为 Plan 9 启用映射网络驱动器 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="f6e86-205">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="f6e86-206">支持对绑定载入点执行“Windows -> Linux”和“Linux -> Windows”路径转换</span><span class="sxs-lookup"><span data-stu-id="f6e86-206">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="f6e86-207">为以只读方式打开的文件中的映射创建只读节</span><span class="sxs-lookup"><span data-stu-id="f6e86-207">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="f6e86-208">内部版本 18334</span><span class="sxs-lookup"><span data-stu-id="f6e86-208">Build 18334</span></span>
<span data-ttu-id="f6e86-209">有关内部版本 18334 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-209">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-210">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-210">WSL</span></span>
* <span data-ttu-id="f6e86-211">重新设计 Windows 时区映射到 Linux 时区的方式 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="f6e86-211">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="f6e86-212">修复内存泄漏，并添加新的字符串转换函数 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="f6e86-212">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="f6e86-213">不包含任何线程的线程组上的 SIGCONT 是一个 no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="f6e86-213">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="f6e86-214">在 /proc/self/fd 中正确显示套接字和 epoll 文件描述符</span><span class="sxs-lookup"><span data-stu-id="f6e86-214">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="f6e86-215">内部版本 18305</span><span class="sxs-lookup"><span data-stu-id="f6e86-215">Build 18305</span></span>
<span data-ttu-id="f6e86-216">有关内部版本 18305 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-216">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-217">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-217">WSL</span></span>
* <span data-ttu-id="f6e86-218">当主线程退出时，pthreads 失去对文件的访问权限 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="f6e86-218">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="f6e86-219">除非有必要，否则 TIOCSCTTY 应忽略“force”参数 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="f6e86-219">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="f6e86-220">改善 wsl.exe 命令行，并添加导入/导出功能。</span><span class="sxs-lookup"><span data-stu-id="f6e86-220">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="f6e86-221">内部版本 18277</span><span class="sxs-lookup"><span data-stu-id="f6e86-221">Build 18277</span></span>
<span data-ttu-id="f6e86-222">有关内部版本 18277 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-222">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-223">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-223">WSL</span></span>
* <span data-ttu-id="f6e86-224">修复内部版本 18272 中引入的“不支持此类接口”错误 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="f6e86-224">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="f6e86-225">忽略 umount syscall 的 MNT_FORCE 标志 [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="f6e86-225">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="f6e86-226">切换 WSL interop 以使用官方的 CreatePseudoConsole API</span><span class="sxs-lookup"><span data-stu-id="f6e86-226">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="f6e86-227">FUTEX_WAIT 重启时不保留超时值</span><span class="sxs-lookup"><span data-stu-id="f6e86-227">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="f6e86-228">内部版本 18272</span><span class="sxs-lookup"><span data-stu-id="f6e86-228">Build 18272</span></span>
<span data-ttu-id="f6e86-229">有关内部版本 18272 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-229">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-230">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-230">WSL</span></span>
* <span data-ttu-id="f6e86-231">**警告：** 此版本中存在一个导致 WSL 不可操作的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-231">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="f6e86-232">尝试启动分发版时，会看到“不支持此类接口”错误。</span><span class="sxs-lookup"><span data-stu-id="f6e86-232">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="f6e86-233">该问题已修复，下周发布的 Insider Fast 内部版本将会应用修复程序。</span><span class="sxs-lookup"><span data-stu-id="f6e86-233">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="f6e86-234">如果已安装此内部版本，可以使用“设置”->“更新和安全”>“恢复”中的“回退到 Windows 10 的上一个版本”回滚到上一 Windows 内部版本。</span><span class="sxs-lookup"><span data-stu-id="f6e86-234">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="f6e86-235">内部版本 18267</span><span class="sxs-lookup"><span data-stu-id="f6e86-235">Build 18267</span></span>
<span data-ttu-id="f6e86-236">有关内部版本 18267 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-236">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-237">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-237">WSL</span></span>
* <span data-ttu-id="f6e86-238">修复 zombie 进程不会回收，而是无限期保留的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-238">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="f6e86-239">如果错误消息超过最大长度，WslRegisterDistribution 将会挂起 [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="f6e86-239">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="f6e86-240">允许 fsync 针对 DrvFs 上的只读文件成功运行 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="f6e86-240">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="f6e86-241">在内部创建符号链接之前，确保 /bin 和 /sbin 目录存在 [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="f6e86-241">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="f6e86-242">为 WSL 实例添加了实例终止超时机制。</span><span class="sxs-lookup"><span data-stu-id="f6e86-242">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="f6e86-243">超时目前设置为 15 秒，这意味着，实例将在上一个 WSL 进程退出 15 秒后终止。</span><span class="sxs-lookup"><span data-stu-id="f6e86-243">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="f6e86-244">若要立即终止分发版，请使用：</span><span class="sxs-lookup"><span data-stu-id="f6e86-244">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="f6e86-245">内部版本 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="f6e86-245">Build 17763 (1809)</span></span>
<span data-ttu-id="f6e86-246">有关内部版本 17763 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-246">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-247">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-247">WSL</span></span>
* <span data-ttu-id="f6e86-248">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="f6e86-248">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="f6e86-249">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="f6e86-249">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="f6e86-250">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="f6e86-250">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="f6e86-251">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="f6e86-251">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="f6e86-252">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="f6e86-252">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="f6e86-253">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="f6e86-253">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="f6e86-254">修复多个 AF_UNIX 相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="f6e86-254">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="f6e86-255">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="f6e86-255">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="f6e86-256">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="f6e86-256">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="f6e86-257">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="f6e86-257">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="f6e86-258">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-258">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="f6e86-259">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="f6e86-259">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="f6e86-260">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="f6e86-260">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="f6e86-261">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="f6e86-261">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="f6e86-262">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="f6e86-262">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="f6e86-263">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="f6e86-263">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="f6e86-264">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="f6e86-264">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="f6e86-265">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="f6e86-265">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="f6e86-266">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="f6e86-266">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="f6e86-267">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="f6e86-267">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="f6e86-268">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="f6e86-268">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="f6e86-269">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-269">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="f6e86-270">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="f6e86-270">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="f6e86-271">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="f6e86-271">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="f6e86-272">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="f6e86-272">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="f6e86-273">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="f6e86-273">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="f6e86-274">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="f6e86-274">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="f6e86-275">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="f6e86-275">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="f6e86-276">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-276">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="f6e86-277">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="f6e86-277">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="f6e86-278">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-278">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="f6e86-279">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="f6e86-279">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="f6e86-280">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="f6e86-280">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="f6e86-281">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-281">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="f6e86-282">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="f6e86-282">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="f6e86-283">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="f6e86-283">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="f6e86-284">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="f6e86-284">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="f6e86-285">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="f6e86-285">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="f6e86-286">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="f6e86-286">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="f6e86-287">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="f6e86-287">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="f6e86-288">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="f6e86-288">[GH 2712]</span></span>
* <span data-ttu-id="f6e86-289">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-289">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="f6e86-290">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="f6e86-290">[GH 3020]</span></span>
* <span data-ttu-id="f6e86-291">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-291">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="f6e86-292">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="f6e86-292">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="f6e86-293">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="f6e86-293">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="f6e86-294">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-294">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="f6e86-295">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-295">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="f6e86-296">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-296">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="f6e86-297">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-297">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="f6e86-298">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="f6e86-298">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="f6e86-299">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-299">Limited support for dmesg.</span></span> <span data-ttu-id="f6e86-300">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="f6e86-300">Applications can now log to dmesg.</span></span> <span data-ttu-id="f6e86-301">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="f6e86-301">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="f6e86-302">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-302">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="f6e86-303">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="f6e86-303">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="f6e86-304">尚不支持 `syslog` syscall 接口。</span><span class="sxs-lookup"><span data-stu-id="f6e86-304">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="f6e86-305">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-305">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="f6e86-306">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="f6e86-306">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="f6e86-307">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="f6e86-307">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="f6e86-308">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="f6e86-308">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="f6e86-309">不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="f6e86-309">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="f6e86-310">内部版本 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="f6e86-310">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="f6e86-311">有关内部版本 18252 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-311">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-312">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-312">WSL</span></span>
* <span data-ttu-id="f6e86-313">将 init 和 bsdtar 二进制文件移出 lxssmanager dll，移入单独的 tools 文件夹</span><span class="sxs-lookup"><span data-stu-id="f6e86-313">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="f6e86-314">修复在使用 CLONE_FILES 的情况下，关闭文件描述符时出现的争用</span><span class="sxs-lookup"><span data-stu-id="f6e86-314">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="f6e86-315">处理转换 DrvFs 路径时 /proc/pid/mountinfo 中的可选字段</span><span class="sxs-lookup"><span data-stu-id="f6e86-315">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="f6e86-316">允许 DrvFs mknod 成功，但不为 S_IFREG 提供元数据支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-316">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="f6e86-317">应为 DrvFs 上创建的只读文件设置只读属性 [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="f6e86-317">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="f6e86-318">添加 /sbin/mount.drvfs 帮助器用于处理 DrvFs 装载</span><span class="sxs-lookup"><span data-stu-id="f6e86-318">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="f6e86-319">在 DrvFs 中使用 POSIX rename。</span><span class="sxs-lookup"><span data-stu-id="f6e86-319">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="f6e86-320">允许在无卷 GUID 的卷上执行路径转换。</span><span class="sxs-lookup"><span data-stu-id="f6e86-320">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="f6e86-321">内部版本 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="f6e86-321">Build 17738 (Fast)</span></span>
<span data-ttu-id="f6e86-322">有关内部版本 17738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-322">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-323">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-323">WSL</span></span>
* <span data-ttu-id="f6e86-324">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="f6e86-324">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="f6e86-325">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="f6e86-325">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="f6e86-326">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="f6e86-326">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="f6e86-327">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="f6e86-327">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="f6e86-328">内部版本 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="f6e86-328">Build 17728 (Fast)</span></span>
<span data-ttu-id="f6e86-329">有关内部版本 17728 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-329">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-330">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-330">WSL</span></span>
* <span data-ttu-id="f6e86-331">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="f6e86-331">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="f6e86-332">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="f6e86-332">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="f6e86-333">修复一些 AF_UNIX 相关的问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="f6e86-333">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="f6e86-334">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="f6e86-334">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="f6e86-335">内部版本 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="f6e86-335">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="f6e86-336">有关内部版本 18204 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-336">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-337">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-337">WSL</span></span>
* <span data-ttu-id="f6e86-338">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="f6e86-338">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="f6e86-339">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="f6e86-339">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="f6e86-340">内部版本 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="f6e86-340">Build 17723 (Fast)</span></span>
<span data-ttu-id="f6e86-341">有关内部版本 17723 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-341">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-342">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-342">WSL</span></span>
* <span data-ttu-id="f6e86-343">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="f6e86-343">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="f6e86-344">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="f6e86-344">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="f6e86-345">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-345">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="f6e86-346">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="f6e86-346">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="f6e86-347">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="f6e86-347">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="f6e86-348">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="f6e86-348">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="f6e86-349">内部版本 17713</span><span class="sxs-lookup"><span data-stu-id="f6e86-349">Build 17713</span></span>
<span data-ttu-id="f6e86-350">有关内部版本 17713 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-350">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-351">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-351">WSL</span></span>
* <span data-ttu-id="f6e86-352">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="f6e86-352">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="f6e86-353">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="f6e86-353">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="f6e86-354">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="f6e86-354">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="f6e86-355">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="f6e86-355">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="f6e86-356">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="f6e86-356">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="f6e86-357">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="f6e86-357">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="f6e86-358">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="f6e86-358">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="f6e86-359">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-359">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="f6e86-360">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="f6e86-360">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="f6e86-361">内部版本 17704</span><span class="sxs-lookup"><span data-stu-id="f6e86-361">Build 17704</span></span>
<span data-ttu-id="f6e86-362">有关内部版本 17704 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-362">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-363">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-363">WSL</span></span>
* <span data-ttu-id="f6e86-364">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="f6e86-364">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="f6e86-365">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="f6e86-365">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="f6e86-366">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="f6e86-366">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="f6e86-367">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="f6e86-367">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="f6e86-368">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="f6e86-368">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="f6e86-369">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-369">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="f6e86-370">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="f6e86-370">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="f6e86-371">版本 17692</span><span class="sxs-lookup"><span data-stu-id="f6e86-371">Build 17692</span></span>
<span data-ttu-id="f6e86-372">有关内部版本 17692 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-372">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-373">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-373">WSL</span></span>
* <span data-ttu-id="f6e86-374">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-374">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="f6e86-375">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="f6e86-375">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="f6e86-376">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="f6e86-376">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="f6e86-377">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-377">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="f6e86-378">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="f6e86-378">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="f6e86-379">版本 17686</span><span class="sxs-lookup"><span data-stu-id="f6e86-379">Build 17686</span></span>
<span data-ttu-id="f6e86-380">有关内部版本 17686 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-380">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-381">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-381">WSL</span></span>
* <span data-ttu-id="f6e86-382">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="f6e86-382">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="f6e86-383">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="f6e86-383">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="f6e86-384">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="f6e86-384">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="f6e86-385">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="f6e86-385">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="f6e86-386">内部版本 17677</span><span class="sxs-lookup"><span data-stu-id="f6e86-386">Build 17677</span></span>
<span data-ttu-id="f6e86-387">有关内部版本 17677 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-387">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-388">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-388">WSL</span></span>
* <span data-ttu-id="f6e86-389">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="f6e86-389">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="f6e86-390">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="f6e86-390">[GH 2712]</span></span>
* <span data-ttu-id="f6e86-391">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-391">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="f6e86-392">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="f6e86-392">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="f6e86-393">内部版本 17666</span><span class="sxs-lookup"><span data-stu-id="f6e86-393">Build 17666</span></span>
<span data-ttu-id="f6e86-394">有关内部版本 17666 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-394">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-395">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-395">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="f6e86-396">警告：某个问题会阻止 WSL 在某些 AMD 芯片组上运行 [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-396">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="f6e86-397">修复程序已准备就绪，即将在 Insider Build 分支中发布。</span><span class="sxs-lookup"><span data-stu-id="f6e86-397">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="f6e86-398">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-398">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="f6e86-399">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="f6e86-399">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="f6e86-400">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="f6e86-400">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="f6e86-401">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-401">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="f6e86-402">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-402">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="f6e86-403">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-403">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="f6e86-404">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-404">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="f6e86-405">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="f6e86-405">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="f6e86-406">内部版本 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="f6e86-406">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="f6e86-407">有关内部版本 17655 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-407">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-408">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-408">WSL</span></span>
* <span data-ttu-id="f6e86-409">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-409">Limited support for dmesg.</span></span> <span data-ttu-id="f6e86-410">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="f6e86-410">Applications can now log to dmesg.</span></span> <span data-ttu-id="f6e86-411">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="f6e86-411">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="f6e86-412">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-412">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="f6e86-413">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="f6e86-413">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="f6e86-414">尚不支持 `syslog` sycall 接口。</span><span class="sxs-lookup"><span data-stu-id="f6e86-414">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="f6e86-415">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-415">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="f6e86-416">修复了即使文件存在，多线程操作也可能返回 ENOENT 的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-416">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="f6e86-417">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="f6e86-417">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="f6e86-418">内部版本 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="f6e86-418">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="f6e86-419">有关内部版本 17639 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-419">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-420">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-420">WSL</span></span>
* <span data-ttu-id="f6e86-421">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="f6e86-421">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="f6e86-422">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="f6e86-422">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="f6e86-423">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="f6e86-423">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="f6e86-424">具体而言，不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="f6e86-424">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="f6e86-425">内部版本 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="f6e86-425">Build 17133 (Fast)</span></span>
<span data-ttu-id="f6e86-426">有关内部版本 17133 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-426">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-427">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-427">WSL</span></span>
* <span data-ttu-id="f6e86-428">修复 WSL 中的挂起问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-428">Fix for hang in WSL.</span></span> <span data-ttu-id="f6e86-429">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="f6e86-429">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="f6e86-430">内部版本 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="f6e86-430">Build 17128 (Fast)</span></span>
<span data-ttu-id="f6e86-431">有关内部版本 17128 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-431">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-432">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-432">WSL</span></span>
* <span data-ttu-id="f6e86-433">无</span><span class="sxs-lookup"><span data-stu-id="f6e86-433">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="f6e86-434">内部版本 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="f6e86-434">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="f6e86-435">有关内部版本 17627 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-435">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-436">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-436">WSL</span></span>
* <span data-ttu-id="f6e86-437">添加对 futex pi 感知操作的支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-437">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="f6e86-438">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="f6e86-438">[GH 1006]</span></span>
    * <span data-ttu-id="f6e86-439">请注意，WSL 功能目前不支持优先级，因此存在一些限制，但标准用法应该不会受到阻止。</span><span class="sxs-lookup"><span data-stu-id="f6e86-439">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="f6e86-440">对 WSL 进程的 Windows 防火墙支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-440">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="f6e86-441">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="f6e86-441">[GH 1852]</span></span>
    * <span data-ttu-id="f6e86-442">例如，若要允许 WSL python 进程侦听任何端口，请使用提升的 Windows cmd：```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="f6e86-442">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="f6e86-443">有关如何添加防火墙规则的更多详细信息，请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="f6e86-443">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="f6e86-444">使用 wsl.exe 时遵循用户的默认 shell。</span><span class="sxs-lookup"><span data-stu-id="f6e86-444">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="f6e86-445">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="f6e86-445">[GH 2372]</span></span>
* <span data-ttu-id="f6e86-446">将所有网络接口报告为以太网。</span><span class="sxs-lookup"><span data-stu-id="f6e86-446">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="f6e86-447">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="f6e86-447">[GH 2996]</span></span>
* <span data-ttu-id="f6e86-448">更好地处理损坏的 /etc/passwd 文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-448">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="f6e86-449">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="f6e86-449">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-450">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-450">Console</span></span>
* <span data-ttu-id="f6e86-451">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-451">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-452">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-452">LTP Results:</span></span>
<span data-ttu-id="f6e86-453">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-453">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="f6e86-454">内部版本 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="f6e86-454">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="f6e86-455">有关内部版本 17618 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-455">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-456">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-456">WSL</span></span>
* <span data-ttu-id="f6e86-457">引入用于 NT interop 的伪控制台功能 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-457">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="f6e86-458">传统的安装机制 (lxrun.exe) 已弃用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-458">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="f6e86-459">支持用于安装分发版的机制是 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="f6e86-459">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-460">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-460">Console</span></span>
* <span data-ttu-id="f6e86-461">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-461">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-462">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-462">LTP Results:</span></span>
<span data-ttu-id="f6e86-463">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-463">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="f6e86-464">版本 17110</span><span class="sxs-lookup"><span data-stu-id="f6e86-464">Build 17110</span></span>
<span data-ttu-id="f6e86-465">有关内部版本 17110 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-465">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-466">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-466">WSL</span></span>
* <span data-ttu-id="f6e86-467">允许从 Windows 终止 /init [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-467">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="f6e86-468">现在，DrvFs 默认使用按目录区分大小写（相当于使用“case=dir”装载选项）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-468">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="f6e86-469">使用“case=dir”（旧行为）需要设置注册表项。</span><span class="sxs-lookup"><span data-stu-id="f6e86-469">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="f6e86-470">如果需要使用“case=dir”，请运行以下命令来启用它：reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="f6e86-470">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="f6e86-471">如果在旧版 Windows 中使用 WSL 创建的现有目录需要区分大小写，请使用 fsutil.exe 将其标记为区分大小写：fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="f6e86-471">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="f6e86-472">NULL 终止从 uname syscall 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="f6e86-472">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-473">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-473">Console</span></span>
* <span data-ttu-id="f6e86-474">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-474">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-475">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-475">LTP Results:</span></span>
<span data-ttu-id="f6e86-476">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-476">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="f6e86-477">内部版本 17107</span><span class="sxs-lookup"><span data-stu-id="f6e86-477">Build 17107</span></span>
<span data-ttu-id="f6e86-478">有关内部版本 17107 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-478">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-479">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-479">WSL</span></span>
* <span data-ttu-id="f6e86-480">支持主 pty 终结点上的 TCSETSF 和 TCSETSW [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-480">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="f6e86-481">启动同步 interop 进程可能会导致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-481">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="f6e86-482">修复 PTRACE_ATTACH 以在 /proc/pid/status 中显示正确的跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="f6e86-482">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="f6e86-483">修复以下争用问题：在不清除 TID 地址的情况下，通过 CLEARTID 和 SETTID 标志克隆的生存期较短的进程可能会退出。</span><span class="sxs-lookup"><span data-stu-id="f6e86-483">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="f6e86-484">在从 17093 以前的内部版本迁移期间，升级 Linux 文件系统目录时会显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-484">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="f6e86-485">有关 17093 文件系统更改的更多详细信息，请参阅 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) 的发行说明。</span><span class="sxs-lookup"><span data-stu-id="f6e86-485">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-486">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-486">Console</span></span>
* <span data-ttu-id="f6e86-487">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-487">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-488">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-488">LTP Results:</span></span>
<span data-ttu-id="f6e86-489">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-489">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="f6e86-490">内部版本 17101</span><span class="sxs-lookup"><span data-stu-id="f6e86-490">Build 17101</span></span>
<span data-ttu-id="f6e86-491">有关内部版本 17101 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-491">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-492">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-492">WSL</span></span>
* <span data-ttu-id="f6e86-493">signalfd 支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-493">Support for signalfd.</span></span> <span data-ttu-id="f6e86-494">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="f6e86-494">[GH 129]</span></span>
* <span data-ttu-id="f6e86-495">支持包含非法 NTFS 字符的文件名，现在会将这些字符编码为专用 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="f6e86-495">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="f6e86-496">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="f6e86-496">[GH 1514]</span></span>
* <span data-ttu-id="f6e86-497">不支持写入时，自动装载将回退到只读。</span><span class="sxs-lookup"><span data-stu-id="f6e86-497">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="f6e86-498">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="f6e86-498">[GH 2603]</span></span>
* <span data-ttu-id="f6e86-499">允许粘贴 Unicode 代理项对（类似于表情符号）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-499">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="f6e86-500">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="f6e86-500">[GH 2765]</span></span>
* <span data-ttu-id="f6e86-501">/proc 和/sys 中的伪文件应从 select、poll、epoll 等命令返回 read 和 write ready [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="f6e86-501">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="f6e86-502">修复当注册表被篡改或损坏时，可能导致服务进入无限循环的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-502">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="f6e86-503">修复 netlink 消息，以便能够使用更新版本（上游 4.14）的 iproute2。</span><span class="sxs-lookup"><span data-stu-id="f6e86-503">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-504">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-504">Console</span></span>
* <span data-ttu-id="f6e86-505">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-505">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-506">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-506">LTP Results:</span></span>
<span data-ttu-id="f6e86-507">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-507">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="f6e86-508">内部版本 17093</span><span class="sxs-lookup"><span data-stu-id="f6e86-508">Build 17093</span></span>
<span data-ttu-id="f6e86-509">有关内部版本 17093 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-509">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="f6e86-510">重要提示：</span><span class="sxs-lookup"><span data-stu-id="f6e86-510">Important:</span></span>
<span data-ttu-id="f6e86-511">升级到此内部版本后，首次启动 WSL 时，需要执行一些操作来升级 Linux 文件系统目录。</span><span class="sxs-lookup"><span data-stu-id="f6e86-511">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="f6e86-512">这可能需要几分钟时间，因此 WSL 的启动速度看上去可能很慢。</span><span class="sxs-lookup"><span data-stu-id="f6e86-512">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="f6e86-513">对于从 Store 安装的每个分发版，只需执行此操作一次。</span><span class="sxs-lookup"><span data-stu-id="f6e86-513">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="f6e86-514">改善了 DrvFs 中的区分大小写支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-514">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="f6e86-515">DrvFs 现在支持按目录区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-515">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="f6e86-516">这是一个可对目录设置的新标志，用于指示应将这些目录中的所有操作视为区分大小写，使得 Windows 应用程序能够正确打开按大小写区分的文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-516">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="f6e86-517">DrvFs 提供新的装载选项用于按目录控制区分大小写状态</span><span class="sxs-lookup"><span data-stu-id="f6e86-517">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="f6e86-518">case=force：将所有目录视为区分大小写（驱动器根目录除外）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-518">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="f6e86-519">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-519">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="f6e86-520">这也是一种传统行为，不过，它会将新目录标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-520">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="f6e86-521">case=dir：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-521">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="f6e86-522">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-522">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="f6e86-523">case=off：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-523">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="f6e86-524">使用 WSL 创建的新目录将标记为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-524">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="f6e86-525">注意：不会对旧版本中的 WSL 创建的目录设置此标志，因此，如果使用“case=dir”选项，则不会将这些目录视为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-525">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="f6e86-526">即将推出一种对现有目录设置此标志的方法。</span><span class="sxs-lookup"><span data-stu-id="f6e86-526">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="f6e86-527">使用这些选项进行装载的示例（对于现有的驱动器，必须先卸载，然后才能使用不同选项装载）：sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="f6e86-527">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="f6e86-528">目前，case=force 仍是默认选项。</span><span class="sxs-lookup"><span data-stu-id="f6e86-528">For now, case=force is still the default option.</span></span> <span data-ttu-id="f6e86-529">以后将更改为 case=dir。</span><span class="sxs-lookup"><span data-stu-id="f6e86-529">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="f6e86-530">现在，在装载 DrvFs 时，可以在 Windows 路径中使用正斜杠，例如：sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="f6e86-530">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="f6e86-531">WSL 现在会在实例启动期间处理 /etc/fstab 文件 [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-531">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="f6e86-532">这种处理是在自动装载 DrvFs 驱动器之前完成的；fstab 已装载的任何驱动器不会自动重新装载，使你可以更改特定驱动器的装入点。</span><span class="sxs-lookup"><span data-stu-id="f6e86-532">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="f6e86-533">可以使用 wsl.conf 禁用此行为。</span><span class="sxs-lookup"><span data-stu-id="f6e86-533">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="f6e86-534">/proc 中的 mount、mountinfo 和 mountstats 文件会正确转义反斜杠和空格等特殊字符 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="f6e86-534">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="f6e86-535">在启用元数据的情况下使用 DrvFs 创建的特殊文件（例如 WSL 符号链接，或 fifos 和 sockets）现在可以从 Windows 复制和移动。</span><span class="sxs-lookup"><span data-stu-id="f6e86-535">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="f6e86-536">可以使用 wsl.conf 更方便地配置 WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-536">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="f6e86-537">我们添加了一个方法，用于自动配置 WSL 中每次启动子系统时要应用的某些功能。</span><span class="sxs-lookup"><span data-stu-id="f6e86-537">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="f6e86-538">这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="f6e86-538">This includes automount options and network configuration.</span></span> <span data-ttu-id="f6e86-539">有关详细信息，请参阅博客文章： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="f6e86-539">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="f6e86-540">AF_UNIX 允许在 WSL 上的 Linux 进程与 Windows 本机进程之间建立套接字连接</span><span class="sxs-lookup"><span data-stu-id="f6e86-540">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="f6e86-541">现在，WSL 和 Windows 应用程序可以通过 Unix 套接字相互通信。</span><span class="sxs-lookup"><span data-stu-id="f6e86-541">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="f6e86-542">假设你要在 Windows 中运行某个服务，并使其可在 Windows 和 WSL 应用中使用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-542">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="f6e86-543">现在可以通过 Unix 套接字实现此目的。</span><span class="sxs-lookup"><span data-stu-id="f6e86-543">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="f6e86-544">有关详细信息，请参阅博客文章： https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="f6e86-544">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-545">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-545">WSL</span></span>
* <span data-ttu-id="f6e86-546">支持使用 MAP_NORESERVE 的 mmap() [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="f6e86-546">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="f6e86-547">支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="f6e86-547">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="f6e86-548">处理克隆中的非 SIGCHLD 终止信号 [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="f6e86-548">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="f6e86-549">存根 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="f6e86-549">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="f6e86-550">加载包含偏移量非零的负载标头的 ELF 二进制文件时出错 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="f6e86-550">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="f6e86-551">加载映像时将尾随页字节归零。</span><span class="sxs-lookup"><span data-stu-id="f6e86-551">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="f6e86-552">减少 execve 以静默方式终止进程的情况</span><span class="sxs-lookup"><span data-stu-id="f6e86-552">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-553">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-553">Console</span></span>
* <span data-ttu-id="f6e86-554">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-554">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-555">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-555">LTP Results:</span></span>
<span data-ttu-id="f6e86-556">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-556">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="f6e86-557">版本 17083</span><span class="sxs-lookup"><span data-stu-id="f6e86-557">Build 17083</span></span>
<span data-ttu-id="f6e86-558">有关内部版本 17083 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-558">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-559">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-559">WSL</span></span>
* <span data-ttu-id="f6e86-560">修复了与 epoll 相关的 bug 检查 [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="f6e86-560">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="f6e86-561">修复了关闭 ASLR 时挂起的问题 [GH 1185、2870]</span><span class="sxs-lookup"><span data-stu-id="f6e86-561">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="f6e86-562">确保 mmap 操作显示原子性 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="f6e86-562">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-563">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-563">Console</span></span>
* <span data-ttu-id="f6e86-564">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-564">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-565">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-565">LTP Results:</span></span>
<span data-ttu-id="f6e86-566">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-566">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="f6e86-567">内部版本 17074</span><span class="sxs-lookup"><span data-stu-id="f6e86-567">Build 17074</span></span>
<span data-ttu-id="f6e86-568">有关内部版本 17074 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-568">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-569">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-569">WSL</span></span>
* <span data-ttu-id="f6e86-570">固定了 DrvFs 元数据的存储格式 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="f6e86-570">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="f6e86-571">**重要说明：** 在此内部版本之前创建的 DrvFs 元数据将不正确地显示或根本不显示。</span><span class="sxs-lookup"><span data-stu-id="f6e86-571">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="f6e86-572">若要修复受影响的文件，请使用 chmod 和 chown 重新应用元数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-572">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="f6e86-573">修复了多个信号和可重启 syscall 的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-573">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-574">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-574">Console</span></span>
* <span data-ttu-id="f6e86-575">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-575">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-576">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-576">LTP Results:</span></span>
<span data-ttu-id="f6e86-577">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-577">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="f6e86-578">内部版本 17063</span><span class="sxs-lookup"><span data-stu-id="f6e86-578">Build 17063</span></span>
<span data-ttu-id="f6e86-579">有关内部版本 17063 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-579">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="f6e86-580">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-580">WSL</span></span>
* <span data-ttu-id="f6e86-581">DrvFs 支持其他 Linux 元数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-581">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="f6e86-582">这样，就可以使用 chmod/chown 设置文件的所有者和模式，并可以创建特殊文件，例如 fifos、Unix 套接字和设备文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-582">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="f6e86-583">默认情况下，此功能暂时处于禁用状态，因为它仍是试验性的。</span><span class="sxs-lookup"><span data-stu-id="f6e86-583">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="f6e86-584">**注意：** 修复了 DrvFs 使用的元数据格式的 bug。</span><span class="sxs-lookup"><span data-stu-id="f6e86-584">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="f6e86-585">尽管试验性的元数据可在此内部版本中正常工作，但将来的内部版本无法正确读取此内部版本创建的元数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-585">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="f6e86-586">你可能需要手动更新已修改的文件的所有者，并且必须重新创建使用自定义设备 ID 的设备。</span><span class="sxs-lookup"><span data-stu-id="f6e86-586">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="f6e86-587">若要启用元数据，请使用 metadata 选项装载 DrvFs（若要在现有装入点上启用，必须先将其卸载）：</span><span class="sxs-lookup"><span data-stu-id="f6e86-587">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="f6e86-588">Linux 权限将作为附加元数据添加到文件；它们不会影响 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="f6e86-588">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="f6e86-589">请记住，使用 Windows 编辑器编辑文件可能会删除元数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-589">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="f6e86-590">在这种情况下，文件将还原为默认权限。</span><span class="sxs-lookup"><span data-stu-id="f6e86-590">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="f6e86-591">已将 mount 选项添加到 DrvFs，用于控制不包含元数据的文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-591">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="f6e86-592">uid：所有文件的所有者使用的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="f6e86-592">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="f6e86-593">gid：所有文件的所有者使用的组 ID。</span><span class="sxs-lookup"><span data-stu-id="f6e86-593">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="f6e86-594">umask：要对所有文件和目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="f6e86-594">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="f6e86-595">fmask：要对所有常规文件排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="f6e86-595">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="f6e86-596">dmask：要对所有目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="f6e86-596">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="f6e86-597">例如：</span><span class="sxs-lookup"><span data-stu-id="f6e86-597">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="f6e86-598">与 metadata 选项相结合可以指定不包含元数据的文件的默认权限。</span><span class="sxs-lookup"><span data-stu-id="f6e86-598">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="f6e86-599">引入了新的环境变量 `WSLENV`，用于配置环境变量在 WSL 与 Win32 之间的流动方式。</span><span class="sxs-lookup"><span data-stu-id="f6e86-599">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="f6e86-600">例如：</span><span class="sxs-lookup"><span data-stu-id="f6e86-600">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="f6e86-601">`WSLENV` 是在从 Win32 启动 WSL 进程或者从 WSL 启动 Win32 进程时可以包含的环境变量的冒号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-601">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="f6e86-602">每个变量可以使用斜杠后接一个用于指定其转换方式的标志作为后缀。</span><span class="sxs-lookup"><span data-stu-id="f6e86-602">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="f6e86-603">p：值是应在 WSL 路径与 Win32 路径之间进行转换的路径。</span><span class="sxs-lookup"><span data-stu-id="f6e86-603">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="f6e86-604">l：值是路径列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-604">l: The value is a list of paths.</span></span> <span data-ttu-id="f6e86-605">在 WSL 中，它是冒号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-605">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="f6e86-606">在 Win32 中，它是分号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-606">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="f6e86-607">u：仅当从 Win32 调用 WSL 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="f6e86-607">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="f6e86-608">w：仅当从 WSL 调用 Win32 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="f6e86-608">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="f6e86-609">可以在 .bashrc 中或者在用户的自定义 Windows 环境中设置 `WSLENV`。</span><span class="sxs-lookup"><span data-stu-id="f6e86-609">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="f6e86-610">drvfs 装入点会正确保留 tar、cp -p 中的时间戳 (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="f6e86-610">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="f6e86-611">drvfs 符号链接会报告正确的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="f6e86-611">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="f6e86-612">read/write 适用于极大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="f6e86-612">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="f6e86-613">waitpid 适用于进程组 ID (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="f6e86-613">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="f6e86-614">极大改善了大型保留区域的 mmap 性能；改善了 ghc 性能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="f6e86-614">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="f6e86-615">READ_IMPLIES_EXEC 的个性化支持；修复 maxima 和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="f6e86-615">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="f6e86-616">mprotect 支持 PROT_GROWSDOWN；修复 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="f6e86-616">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="f6e86-617">overcommit 模式的页面错误修复；修复 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="f6e86-617">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="f6e86-618">clone 支持更多标志组合</span><span class="sxs-lookup"><span data-stu-id="f6e86-618">clone supports more flags combinations</span></span>
* <span data-ttu-id="f6e86-619">支持 epoll 文件的 select/epoll（以前为 no-op）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-619">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="f6e86-620">通知未实现的 syscall 的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="f6e86-620">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="f6e86-621">忽略生成 resolv.conf 名称服务器时不启动的接口 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="f6e86-621">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="f6e86-622">枚举没有物理地址的网络接口。</span><span class="sxs-lookup"><span data-stu-id="f6e86-622">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="f6e86-623">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="f6e86-623">[GH 2685]</span></span>
* <span data-ttu-id="f6e86-624">其他 bug 修复和改进。</span><span class="sxs-lookup"><span data-stu-id="f6e86-624">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="f6e86-625">适用于 Windows 上的开发人员的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="f6e86-625">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="f6e86-626">Windows 命令行工具链包括 bsdtar (tar) 和 curl。</span><span class="sxs-lookup"><span data-stu-id="f6e86-626">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="f6e86-627">请阅读[此博客](https://aka.ms/tarcurlwindows)来详细了解如何添加这两个新工具，以及它们如何打造 Windows 上的开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="f6e86-627">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="f6e86-628">`AF_UNIX` 适用于 Windows 预览体验成员 SDK (17061+)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-628">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="f6e86-629">请阅读[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)来详细了解 `AF_UNIX`，以及 Windows 上的开发人员如何使用它。</span><span class="sxs-lookup"><span data-stu-id="f6e86-629">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="f6e86-630">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-630">Console</span></span>
* <span data-ttu-id="f6e86-631">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-631">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-632">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-632">LTP Results:</span></span>
<span data-ttu-id="f6e86-633">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-633">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="f6e86-634">内部版本 17046</span><span class="sxs-lookup"><span data-stu-id="f6e86-634">Build 17046</span></span>

<span data-ttu-id="f6e86-635">有关内部版本 17046 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-635">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="f6e86-636">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-636">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-637">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-637">WSL</span></span>
- <span data-ttu-id="f6e86-638">允许进程在没有活动终端的情况下运行。</span><span class="sxs-lookup"><span data-stu-id="f6e86-638">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="f6e86-639">[GH 709、1007、1511、2252、2391 等]</span><span class="sxs-lookup"><span data-stu-id="f6e86-639">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="f6e86-640">更好地支持 CLONE_VFORK 和 CLONE_VM。</span><span class="sxs-lookup"><span data-stu-id="f6e86-640">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="f6e86-641">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="f6e86-641">[GH 1878, 2615]</span></span>
- <span data-ttu-id="f6e86-642">跳过 WSL 网络操作的 TDI 筛选器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="f6e86-642">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="f6e86-643">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="f6e86-643">[GH 1554]</span></span>
- <span data-ttu-id="f6e86-644">在满足特定的条件时，DrvFs 将创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="f6e86-644">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="f6e86-645">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="f6e86-645">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="f6e86-646">链接目标必须是相对性的，不能跨任何装入点或符号链接，并且必须存在。</span><span class="sxs-lookup"><span data-stu-id="f6e86-646">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="f6e86-647">除非已启用开发人员模式，否则用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE（这通常需要以提升的权限启动 wsl.exe）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-647">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="f6e86-648">在所有其他情况下，DrvFs 仍会创建 WSL 符号链接。</span><span class="sxs-lookup"><span data-stu-id="f6e86-648">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="f6e86-649">允许同时运行提升和未提升的 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="f6e86-649">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="f6e86-650">支持 /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="f6e86-650">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="f6e86-651">添加 wslpath 用于执行 WSL<->Windows 路径转换。</span><span class="sxs-lookup"><span data-stu-id="f6e86-651">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="f6e86-652">[GH 522、1243、1834、2327 等]</span><span class="sxs-lookup"><span data-stu-id="f6e86-652">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="f6e86-653">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-653">Console</span></span>
- <span data-ttu-id="f6e86-654">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-654">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-655">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-655">LTP Results:</span></span>
<span data-ttu-id="f6e86-656">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-656">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="f6e86-657">内部版本 17040</span><span class="sxs-lookup"><span data-stu-id="f6e86-657">Build 17040</span></span>

<span data-ttu-id="f6e86-658">有关内部版本 17040 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-658">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-659">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-659">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-660">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-660">WSL</span></span>
- <span data-ttu-id="f6e86-661">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-661">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-662">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-662">Console</span></span>
- <span data-ttu-id="f6e86-663">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-663">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-664">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-664">LTP Results:</span></span>
<span data-ttu-id="f6e86-665">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-665">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="f6e86-666">内部版本 17035</span><span class="sxs-lookup"><span data-stu-id="f6e86-666">Build 17035</span></span>

<span data-ttu-id="f6e86-667">有关内部版本 17035 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-667">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-668">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-668">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-669">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-669">WSL</span></span>
- <span data-ttu-id="f6e86-670">访问 DrvFs 上的文件偶尔会失败并出现 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="f6e86-670">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="f6e86-671">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="f6e86-671">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-672">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-672">Console</span></span>
- <span data-ttu-id="f6e86-673">在 VT 模式下插入/删除行时丢失一些颜色。</span><span class="sxs-lookup"><span data-stu-id="f6e86-673">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-674">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-674">LTP Results:</span></span>
<span data-ttu-id="f6e86-675">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-675">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="f6e86-676">内部版本 17025</span><span class="sxs-lookup"><span data-stu-id="f6e86-676">Build 17025</span></span>

<span data-ttu-id="f6e86-677">有关内部版本 17025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-677">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-678">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-678">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-679">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-679">WSL</span></span>
- <span data-ttu-id="f6e86-680">在新的前台进程组中启动初始进程 [GH 1653、2510]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-680">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="f6e86-681">SIGHUP 传递修复 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-681">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="f6e86-682">如果未提供虚拟网桥名称，将生成默认名称 [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-682">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="f6e86-683">实现 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-683">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="f6e86-684">更多 interop stdout/stderr 管道修复措施。</span><span class="sxs-lookup"><span data-stu-id="f6e86-684">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="f6e86-685">存根 syncfs 系统调用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-685">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-686">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-686">Console</span></span>
- <span data-ttu-id="f6e86-687">修复第三方控制台的输入 VT 转换 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="f6e86-687">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-688">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-688">LTP Results:</span></span>
<span data-ttu-id="f6e86-689">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-689">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="f6e86-690">内部版本 17017</span><span class="sxs-lookup"><span data-stu-id="f6e86-690">Build 17017</span></span>

<span data-ttu-id="f6e86-691">有关内部版本 17017 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-691">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-692">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-692">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-693">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-693">WSL</span></span>
- <span data-ttu-id="f6e86-694">忽略空的 ELF 程序标头 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-694">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="f6e86-695">允许 LxssManager 为非交互式用户创建 WSL 实例（ssh 和计划任务支持）[GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-695">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="f6e86-696">支持 WSL->Win32->WSL（“起始”）方案 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-696">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="f6e86-697">有限支持终止通过 interop 调用的控制台应用 [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-697">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="f6e86-698">支持 devpts 的装载选项 [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-698">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="f6e86-699">Ptrace 阻止子级启动 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-699">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="f6e86-700">EPOLLET 缺少某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-700">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="f6e86-701">返回 PTRACE_GETSIGINFO 的更多数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-701">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="f6e86-702">结合 lseek 运行 Getdents 会提供错误的结果。</span><span class="sxs-lookup"><span data-stu-id="f6e86-702">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="f6e86-703">修复某些 Win32 interop 应用挂起，并等待在没有更多数据的管道中提供输入的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-703">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="f6e86-704">tty/pty 文件的 O_ASYNC 支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-704">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="f6e86-705">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-705">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-706">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-706">Console</span></span>
- <span data-ttu-id="f6e86-707">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-707">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-708">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-708">LTP Results:</span></span>
<span data-ttu-id="f6e86-709">正在测试。</span><span class="sxs-lookup"><span data-stu-id="f6e86-709">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="f6e86-710">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="f6e86-710">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="f6e86-711">内部版本 16288</span><span class="sxs-lookup"><span data-stu-id="f6e86-711">Build 16288</span></span>

<span data-ttu-id="f6e86-712">有关内部版本 16288 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-712">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-713">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-713">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-714">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-714">WSL</span></span>
- <span data-ttu-id="f6e86-715">正确初始化和报告套接字文件描述符的 uid、gid 和模式 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="f6e86-715">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="f6e86-716">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-716">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-717">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-717">Console</span></span>
- <span data-ttu-id="f6e86-718">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-718">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-719">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-719">LTP Results:</span></span>
<span data-ttu-id="f6e86-720">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-720">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="f6e86-721">内部版本 16278</span><span class="sxs-lookup"><span data-stu-id="f6e86-721">Build 16278</span></span>

<span data-ttu-id="f6e86-722">有关内部版本 162738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-722">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-723">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-723">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-724">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-724">WSL</span></span>
- <span data-ttu-id="f6e86-725">分解 LX MM 状态时显式取消映射文件后备节的映射视图 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="f6e86-725">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="f6e86-726">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-726">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-727">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-727">Console</span></span>
- <span data-ttu-id="f6e86-728">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-728">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-729">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-729">LTP Results:</span></span>
<span data-ttu-id="f6e86-730">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-730">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="f6e86-731">内部版本 16275</span><span class="sxs-lookup"><span data-stu-id="f6e86-731">Build 16275</span></span>

<span data-ttu-id="f6e86-732">有关内部版本 162735 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-732">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-733">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-733">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-734">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-734">WSL</span></span>
- <span data-ttu-id="f6e86-735">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-735">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-736">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-736">Console</span></span>
- <span data-ttu-id="f6e86-737">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-737">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-738">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-738">LTP Results:</span></span>
<span data-ttu-id="f6e86-739">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-739">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="f6e86-740">内部版本 16273</span><span class="sxs-lookup"><span data-stu-id="f6e86-740">Build 16273</span></span>

<span data-ttu-id="f6e86-741">有关内部版本 16273 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-741">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-742">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-742">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-743">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-743">WSL</span></span>
- <span data-ttu-id="f6e86-744">修复了 DrvFs 有时报告目录的错误文件类型的问题 [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="f6e86-744">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="f6e86-745">允许创建 NETLINK_KOBJECT_UEVENT 套接字来取消阻止使用 UEVENT 的程序 [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="f6e86-745">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="f6e86-746">添加对非阻塞连接的支持 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="f6e86-746">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="f6e86-747">实现 CLONE_FS 克隆系统调用标志 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="f6e86-747">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="f6e86-748">修复有关在 NT interop 中不会正确处理制表符或引号的问题 [GH 1625、2164]</span><span class="sxs-lookup"><span data-stu-id="f6e86-748">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="f6e86-749">解决尝试重新启动 WSL 实例时发生的拒绝访问错误 [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="f6e86-749">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="f6e86-750">实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="f6e86-750">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="f6e86-751">修复各种 SysFs 文件的权限 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="f6e86-751">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="f6e86-752">修复设置过程中 Haskell 堆栈挂起的问题 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="f6e86-752">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="f6e86-753">实现 binfmt_misc“C”、“O”和“P”标志 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="f6e86-753">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="f6e86-754">添加 /proc/sys/kernel /shmmax /shmmni 和 /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="f6e86-754">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="f6e86-755">添加对 ioprio_set 系统调用的部分支持 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="f6e86-755">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="f6e86-756">存根 SO_REUSEPORT 和添加 netlink 套接字的 SO_PASSCRED 支持 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="f6e86-756">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="f6e86-757">如果当前正在安装或卸载分发版，将从 RegisterDistribuiton 返回不同的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f6e86-757">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="f6e86-758">允许通过 wslconfig.exe 取消注册部分安装的 WSL 分发版</span><span class="sxs-lookup"><span data-stu-id="f6e86-758">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="f6e86-759">修复 udp::msg_peek 的 python 套接字测试挂起问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-759">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="f6e86-760">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-760">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-761">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-761">Console</span></span>
- <span data-ttu-id="f6e86-762">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-762">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-763">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-763">LTP Results:</span></span>
<span data-ttu-id="f6e86-764">测试总数：1904</span><span class="sxs-lookup"><span data-stu-id="f6e86-764">Total Tests: 1904</span></span><br/>
<span data-ttu-id="f6e86-765">跳过的测试总数：209</span><span class="sxs-lookup"><span data-stu-id="f6e86-765">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="f6e86-766">失败总数：229</span><span class="sxs-lookup"><span data-stu-id="f6e86-766">Total Failures: 229</span></span><br/>
[<span data-ttu-id="f6e86-767">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-767">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="f6e86-768">版本 16257</span><span class="sxs-lookup"><span data-stu-id="f6e86-768">Build 16257</span></span>

<span data-ttu-id="f6e86-769">有关内部版本 16257 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-769">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-770">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-770">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-771">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-771">WSL</span></span>
- <span data-ttu-id="f6e86-772">实现 prlimit64 系统调用</span><span class="sxs-lookup"><span data-stu-id="f6e86-772">Implement prlimit64 system call</span></span>
- <span data-ttu-id="f6e86-773">添加对 ulimit -n 的支持 (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="f6e86-773">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="f6e86-774">TCP 套接字的存根 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="f6e86-774">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="f6e86-775">修复无效的 AT_EXECFN 辅助矢量行为 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="f6e86-775">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="f6e86-776">修复 console/tty 的 copy/paste 行为，并添加更适当的完整缓冲区处理 [GH 2204、2131]</span><span class="sxs-lookup"><span data-stu-id="f6e86-776">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="f6e86-777">在 set-user-ID 和 set-group-ID 程序的辅助矢量中设置 AT_SECURE [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="f6e86-777">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="f6e86-778">伪终端主终结点不处理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="f6e86-778">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="f6e86-779">修复 lseek 在 LxFs 中的回退目录行为 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="f6e86-779">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="f6e86-780">重度使用后 /dev/ptmx 锁定 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="f6e86-780">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="f6e86-781">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-781">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-782">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-782">Console</span></span>
- <span data-ttu-id="f6e86-783">修复横线/下划线四处可见的问题 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="f6e86-783">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="f6e86-784">修复进程顺序更改，使 NPM 更难以关闭的问题 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="f6e86-784">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="f6e86-785">添加了新的色彩方案： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="f6e86-785">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-786">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-786">LTP Results:</span></span>
<span data-ttu-id="f6e86-787">自 16251 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-787">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-788">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-788">Syscall Support</span></span>
<span data-ttu-id="f6e86-789">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-789">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-790">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-790">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="f6e86-791">已知问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-791">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="f6e86-792">GitHub 问题 2392：WSL 无法识别 Windows 文件夹 ...</span><span class="sxs-lookup"><span data-stu-id="f6e86-792">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="f6e86-793">在内部版本 16257 中，WSL 在通过 `/mnt/c/...` 枚举 Windows 文件/文件夹时会出现问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-793">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="f6e86-794">此问题已修复，修复程序将在 2017 年 8 月 14 日开始的周内，在预览体验成员内部版本中发布。</span><span class="sxs-lookup"><span data-stu-id="f6e86-794">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="f6e86-795">内部版本 16251</span><span class="sxs-lookup"><span data-stu-id="f6e86-795">Build 16251</span></span>

<span data-ttu-id="f6e86-796">有关内部版本 16251 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-796">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-797">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-797">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-798">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-798">WSL</span></span>
- <span data-ttu-id="f6e86-799">从 WSL 可选组件中删除 beta 标记，有关详细信息，请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-799">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="f6e86-800">在执行时正确初始化 set-user-ID 和 set-group-ID 二进制文件的 saved-set uid 和 gid [GH 962、1415、2072]</span><span class="sxs-lookup"><span data-stu-id="f6e86-800">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="f6e86-801">添加了对 ptrace PTRACE_O_TRACEEXIT 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="f6e86-801">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="f6e86-802">添加了对包含 NT_FPREGSET 的 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="f6e86-802">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="f6e86-803">修复了 ptrace 在忽略信号时停止的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-803">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="f6e86-804">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-804">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-805">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-805">Console</span></span>
- <span data-ttu-id="f6e86-806">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-806">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-807">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-807">LTP Results:</span></span>
<span data-ttu-id="f6e86-808">通过的测试数：768</span><span class="sxs-lookup"><span data-stu-id="f6e86-808">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="f6e86-809">失败的测试数：244</span><span class="sxs-lookup"><span data-stu-id="f6e86-809">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="f6e86-810">跳过的测试数：96</span><span class="sxs-lookup"><span data-stu-id="f6e86-810">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="f6e86-811">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-811">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="f6e86-812">内部版本 16241</span><span class="sxs-lookup"><span data-stu-id="f6e86-812">Build 16241</span></span>

<span data-ttu-id="f6e86-813">有关内部版本 16241 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-813">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-814">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-814">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="f6e86-815">WSL</span><span class="sxs-lookup"><span data-stu-id="f6e86-815">WSL</span></span>
- <span data-ttu-id="f6e86-816">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-816">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="f6e86-817">控制台</span><span class="sxs-lookup"><span data-stu-id="f6e86-817">Console</span></span>
- <span data-ttu-id="f6e86-818">修复输出跨行 DEC 的错误字符的问题，最初报告位于[此处](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="f6e86-818">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="f6e86-819">修复代码页 65001 (utf8) 中不显示输出文本的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-819">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="f6e86-820">更改选择内容时，不会将对某种颜色的 RGB 值所做的更改传输到调色板的其他部分。</span><span class="sxs-lookup"><span data-stu-id="f6e86-820">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="f6e86-821">这在一定程度上使得控制台属性表变得更易于使用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-821">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="f6e86-822">Ctrl+S 似乎不起作用</span><span class="sxs-lookup"><span data-stu-id="f6e86-822">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="f6e86-823">ANSI 转义代码中根本没有 Un-Bold/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="f6e86-823">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="f6e86-824">控制台不正常支持 Vim 色彩主题 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="f6e86-824">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="f6e86-825">无法粘贴特定的字符 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="f6e86-825">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="f6e86-826">当编辑/命令行上有内容时，重复流的调整大小操作以奇怪的方式与 bash 窗口调整大小操作交互 [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="f6e86-826">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="f6e86-827">按 Ctrl-L 不会清屏 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="f6e86-827">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="f6e86-828">在 HDPI 上显示 VT 时的控制台呈现 bug [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="f6e86-828">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="f6e86-829">日文字符出现乱码和 Unicode 字符 U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="f6e86-829">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="f6e86-830">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-830">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="f6e86-831">版本 16237</span><span class="sxs-lookup"><span data-stu-id="f6e86-831">Build 16237</span></span>

<span data-ttu-id="f6e86-832">有关内部版本 16237 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-832">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-833">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-833">Fixed</span></span>
- <span data-ttu-id="f6e86-834">对 lxfs 中不包含 EA 的文件使用默认属性 (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="f6e86-834">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="f6e86-835">添加了对使用扩展属性的分发版的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-835">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="f6e86-836">修复 getdents 和 getdents64 返回的项的填充</span><span class="sxs-lookup"><span data-stu-id="f6e86-836">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="f6e86-837">修复针对 shmctl SHM_STAT 系统调用的权限检查 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="f6e86-837">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="f6e86-838">修复了 tty 的错误初始 epoll 状态 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="f6e86-838">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="f6e86-839">修复 DrvFs readdir 不返回所有项的问题 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="f6e86-839">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="f6e86-840">修复取消链接文件时的 LxFs readdir [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="f6e86-840">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="f6e86-841">允许通过 procfs 重新打开未链接的 drvfs 文件</span><span class="sxs-lookup"><span data-stu-id="f6e86-841">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="f6e86-842">添加了用于禁用 WSL 功能的全局注册表项重写（interop/驱动器装载）</span><span class="sxs-lookup"><span data-stu-id="f6e86-842">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="f6e86-843">修复 DrvFs（和 LxFs）的“统计信息”中的错误块计数 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="f6e86-843">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="f6e86-844">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-844">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="f6e86-845">内部版本 16232</span><span class="sxs-lookup"><span data-stu-id="f6e86-845">Build 16232</span></span>

<span data-ttu-id="f6e86-846">有关内部版本 16232 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-846">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-847">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-847">Fixed</span></span>
- <span data-ttu-id="f6e86-848">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-848">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="f6e86-849">内部版本 16226</span><span class="sxs-lookup"><span data-stu-id="f6e86-849">Build 16226</span></span>

<span data-ttu-id="f6e86-850">有关内部版本 16226 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-850">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-851">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-851">Fixed</span></span>
- <span data-ttu-id="f6e86-852">xattr 相关的 syscall 支持（getxattr、setxattr、listxattr、removexattr）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-852">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="f6e86-853">security.capablity xattr 支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-853">security.capablity xattr support.</span></span>
- <span data-ttu-id="f6e86-854">改善了与某些文件系统和筛选器（包括非 MS SMB 服务器）的兼容性。</span><span class="sxs-lookup"><span data-stu-id="f6e86-854">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="f6e86-855">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="f6e86-855">[GH #1952]</span></span>
- <span data-ttu-id="f6e86-856">改善了对 OneDrive 占位符、GVFS 占位符和精简 OS 压缩文件的支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-856">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="f6e86-857">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-857">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="f6e86-858">内部版本 16215</span><span class="sxs-lookup"><span data-stu-id="f6e86-858">Build 16215</span></span>

<span data-ttu-id="f6e86-859">有关内部版本 16215 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-859">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-860">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-860">Fixed</span></span>
- <span data-ttu-id="f6e86-861">WSL 不再需要开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="f6e86-861">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="f6e86-862">支持 drvfs 中的目录接合。</span><span class="sxs-lookup"><span data-stu-id="f6e86-862">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="f6e86-863">处理 WSL appx 分发包的卸载。</span><span class="sxs-lookup"><span data-stu-id="f6e86-863">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="f6e86-864">更新 procfs 以显示专用映射和共享映射。</span><span class="sxs-lookup"><span data-stu-id="f6e86-864">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="f6e86-865">为 wslconfig.exe 添加清理部分安装或已卸载的分发版的功能。</span><span class="sxs-lookup"><span data-stu-id="f6e86-865">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="f6e86-866">添加了对 TCP 套接字的 IP_MTU_DISCOVER 的支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-866">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="f6e86-867">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="f6e86-867">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="f6e86-868">推断 AF_INADDR 路由的协议系列。</span><span class="sxs-lookup"><span data-stu-id="f6e86-868">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="f6e86-869">串行设备改进 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="f6e86-869">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="f6e86-870">内部版本 16199</span><span class="sxs-lookup"><span data-stu-id="f6e86-870">Build 16199</span></span>

<span data-ttu-id="f6e86-871">有关内部版本 16199 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-871">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-872">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-872">Fixed</span></span>
- <span data-ttu-id="f6e86-873">这些版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-873">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="f6e86-874">内部版本 16193</span><span class="sxs-lookup"><span data-stu-id="f6e86-874">Build 16193</span></span>

<span data-ttu-id="f6e86-875">有关内部版本 16193 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-875">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-876">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-876">Fixed</span></span>
- <span data-ttu-id="f6e86-877">发送 SIGCONT 与终止线程组之间的争用状态 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="f6e86-877">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="f6e86-878">更改 tty 和 pty 设备以报告 FILE_DEVICE_NAMED_PIPE 而不是 FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="f6e86-878">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="f6e86-879">IP_OPTIONS 的 SSH 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-879">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="f6e86-880">已将 DrvFs 装载移到初始化守护程序 [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="f6e86-880">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="f6e86-881">在 DrvFs 中添加了遵循 NT 符号链接的支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-881">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="f6e86-882">内部版本 16184</span><span class="sxs-lookup"><span data-stu-id="f6e86-882">Build 16184</span></span>

<span data-ttu-id="f6e86-883">有关内部版本 16184 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-883">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-884">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-884">Fixed</span></span>
- <span data-ttu-id="f6e86-885">删除了 apt 包维护任务 (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="f6e86-885">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="f6e86-886">修复了 node.js 中的 Windows 进程不显示输出的问题 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="f6e86-886">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="f6e86-887">放宽 lxcore 中的对齐要求 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="f6e86-887">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="f6e86-888">修复了许多系统调用中处理 AT_EMPTY_PATH 标志的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-888">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="f6e86-889">修复了删除存在已打开句柄的 DrvFs 文件时，导致文件出现未定义的行为的问题 [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="f6e86-889">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="f6e86-890">/etc/hosts 现在会从 Windows hosts 文件 (%windir%\system32\drivers\etc\hosts) 继承项 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="f6e86-890">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="f6e86-891">内部版本 16179</span><span class="sxs-lookup"><span data-stu-id="f6e86-891">Build 16179</span></span>

<span data-ttu-id="f6e86-892">有关内部版本 16179 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-892">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-893">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-893">Fixed</span></span>
- <span data-ttu-id="f6e86-894">本周没有 WSL 更改。</span><span class="sxs-lookup"><span data-stu-id="f6e86-894">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="f6e86-895">内部版本 16176</span><span class="sxs-lookup"><span data-stu-id="f6e86-895">Build 16176</span></span>

<span data-ttu-id="f6e86-896">有关内部版本 16176 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-896">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-897">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-897">Fixed</span></span>

- [<span data-ttu-id="f6e86-898">已启用串行支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-898">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="f6e86-899">添加了 IP 套接字选项 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="f6e86-899">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="f6e86-900">实现了 pwritev 函数（将文件上传到 nginx/PHP-FPM 时）[GH 1506]</span><span class="sxs-lookup"><span data-stu-id="f6e86-900">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="f6e86-901">添加了 IP 套接字选项 IP_MULTICAST_IF 和 IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="f6e86-901">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="f6e86-902">支持套接字选项 IP_MULTICAST_LOOP 和 IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="f6e86-902">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="f6e86-903">为应用节点、traceroute、dig、nslookup、主机添加了 IP(V6)_MTU 套接字选项</span><span class="sxs-lookup"><span data-stu-id="f6e86-903">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="f6e86-904">添加了 IP 套接字选项 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="f6e86-904">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="f6e86-905">文件系统改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-905">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="f6e86-906">允许装载 UNC 路径</span><span class="sxs-lookup"><span data-stu-id="f6e86-906">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="f6e86-907">在 drvfs 中启用 CDFS 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-907">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="f6e86-908">正确处理 drvfs 中网络文件系统的权限</span><span class="sxs-lookup"><span data-stu-id="f6e86-908">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="f6e86-909">在 drvfs 中添加远程驱动器的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-909">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="f6e86-910">在 drvfs 中启用 FAT 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-910">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="f6e86-911">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-911">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-912">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="f6e86-912">LTP Results</span></span>
<span data-ttu-id="f6e86-913">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-913">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="f6e86-914">内部版本 16170</span><span class="sxs-lookup"><span data-stu-id="f6e86-914">Build 16170</span></span>

<span data-ttu-id="f6e86-915">有关内部版本 16170 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-915">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="f6e86-916">我们发布的新[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)中介绍了我们在测试 WSL 方面所做的努力。</span><span class="sxs-lookup"><span data-stu-id="f6e86-916">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="f6e86-917">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-917">Fixed</span></span>

- <span data-ttu-id="f6e86-918">支持套接字选项 IP_ADD_MEMBERSHIP 和 IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="f6e86-918">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="f6e86-919">添加对 PTRACE_OLDSETOPTIONS 的支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-919">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="f6e86-920">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="f6e86-920">[GH 1692]</span></span>
- <span data-ttu-id="f6e86-921">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-921">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-922">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="f6e86-922">LTP Results</span></span>
<span data-ttu-id="f6e86-923">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-923">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="f6e86-924">内部版本 15046 到 Windows 10 创意者更新</span><span class="sxs-lookup"><span data-stu-id="f6e86-924">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="f6e86-925">我们未计划在 Windows 10 创意者更新中包含其他 WSL 修复或功能。</span><span class="sxs-lookup"><span data-stu-id="f6e86-925">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="f6e86-926">WSL 的发行说明将在未来几周恢复发布，其中补充了面向下一个 Windows 更新主要版本的信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-926">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="f6e86-927">有关内部版本 15046 和将来的预览体验版的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-927">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="f6e86-928">内部版本 15042</span><span class="sxs-lookup"><span data-stu-id="f6e86-928">Build 15042</span></span>

<span data-ttu-id="f6e86-929">有关内部版本 15042 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-929">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-930">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-930">Fixed</span></span>

- <span data-ttu-id="f6e86-931">修复删除以“...”结尾的路径时出现死锁的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-931">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="f6e86-932">修复了 FIONBIO 在成功时不返回 0 的问题 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="f6e86-932">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="f6e86-933">修复了 inet 数据报套接字的零长度读取问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-933">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="f6e86-934">修复 drvfs inode 查找中的争用状况可能导致死锁的问题 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="f6e86-934">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="f6e86-935">扩展了对 unix 套接字辅助数据的支持；SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="f6e86-935">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="f6e86-936">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-936">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-937">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-937">LTP Results:</span></span>
<span data-ttu-id="f6e86-938">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="f6e86-938">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="f6e86-939">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="f6e86-939">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="f6e86-940">内部版本 15031</span><span class="sxs-lookup"><span data-stu-id="f6e86-940">Build 15031</span></span>

<span data-ttu-id="f6e86-941">有关内部版本 15031 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-941">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-942">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-942">Fixed</span></span>

- <span data-ttu-id="f6e86-943">修复了 time(2) 偶尔行为异常的 bug。</span><span class="sxs-lookup"><span data-stu-id="f6e86-943">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="f6e86-944">修复了 \*SIGPROCMASK syscall 可能损坏信号掩码的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-944">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="f6e86-945">现在会在 WSL 进程创建通知中返回完整的命令行长度。</span><span class="sxs-lookup"><span data-stu-id="f6e86-945">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="f6e86-946">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="f6e86-946">[GH 1632]</span></span>
- <span data-ttu-id="f6e86-947">WSL 现在会针对 GDB 挂起通过 ptrace 报告线程退出。</span><span class="sxs-lookup"><span data-stu-id="f6e86-947">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="f6e86-948">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="f6e86-948">[GH 1196]</span></span>
- <span data-ttu-id="f6e86-949">修复了在收到繁重 tmux IO 后 ptys 挂起的 bug。</span><span class="sxs-lookup"><span data-stu-id="f6e86-949">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="f6e86-950">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="f6e86-950">[GH 1358]</span></span>
- <span data-ttu-id="f6e86-951">修复了许多系统调用中的超时验证（futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create）</span><span class="sxs-lookup"><span data-stu-id="f6e86-951">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="f6e86-952">添加了 eventfd EFD_SEMAPHORE 支持 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="f6e86-952">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="f6e86-953">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-953">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-954">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-954">LTP Results:</span></span>
<span data-ttu-id="f6e86-955">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="f6e86-955">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="f6e86-956">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="f6e86-956">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="f6e86-957">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-957">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="f6e86-958">内部版本 15025</span><span class="sxs-lookup"><span data-stu-id="f6e86-958">Build 15025</span></span>

<span data-ttu-id="f6e86-959">有关内部版本 15025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-959">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-960">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-960">Fixed</span></span>

- <span data-ttu-id="f6e86-961">修复破坏 grep 2.27 的 bug [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="f6e86-961">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="f6e86-962">为 eventfd2 syscall 实现了 EFD_SEMAPHORE 标志 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="f6e86-962">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="f6e86-963">实现了 /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="f6e86-963">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="f6e86-964">针对 unix 流套接字的信号驱动 IO 支持 [GH 393、68]</span><span class="sxs-lookup"><span data-stu-id="f6e86-964">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="f6e86-965">支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="f6e86-965">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="f6e86-966">实现 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="f6e86-966">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="f6e86-967">修复了 epoll_wait() 不等待的 bug [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="f6e86-967">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="f6e86-968">实现 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="f6e86-968">Implement /proc/version_signature</span></span>
- <span data-ttu-id="f6e86-969">现在，如果两个文件描述符引用同一管道，则 syscall 会返回失败</span><span class="sxs-lookup"><span data-stu-id="f6e86-969">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="f6e86-970">为 Unix 套接字的 SO_PEERCRED 实现了正确的行为</span><span class="sxs-lookup"><span data-stu-id="f6e86-970">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="f6e86-971">修复了 tkill syscall 处理无效参数的方法</span><span class="sxs-lookup"><span data-stu-id="f6e86-971">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="f6e86-972">做出更改以提高 drvfs 的性能</span><span class="sxs-lookup"><span data-stu-id="f6e86-972">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="f6e86-973">针对 Ruby IO 阻塞的次要修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-973">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="f6e86-974">修复了 recvmsg() 对 inet 套接字的 MSG_DONTWAIT 标志返回 EINVAL 的问题 [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="f6e86-974">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="f6e86-975">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-975">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-976">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-976">LTP Results:</span></span>
<span data-ttu-id="f6e86-977">通过的测试数：732</span><span class="sxs-lookup"><span data-stu-id="f6e86-977">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="f6e86-978">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="f6e86-978">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="f6e86-979">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-979">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="f6e86-980">内部版本 15019</span><span class="sxs-lookup"><span data-stu-id="f6e86-980">Build 15019</span></span>

<span data-ttu-id="f6e86-981">有关内部版本 15019 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-981">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-982">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-982">Fixed</span></span>

- <span data-ttu-id="f6e86-983">修复了 htop 等工具在 procfs 中错误报告 CPU 使用率的 bug（GH 823、945、971）</span><span class="sxs-lookup"><span data-stu-id="f6e86-983">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="f6e86-984">对现有的文件结合 O_TRUNC 调用 open() 时，inotify 现在会在 IN_OPEN 的前面生成 IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="f6e86-984">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="f6e86-985">修复 unix 套接字 getsockopt SO_ERROR 以启用 postgress [GH 61、1354]</span><span class="sxs-lookup"><span data-stu-id="f6e86-985">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="f6e86-986">为 GO 语言实现 /proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="f6e86-986">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="f6e86-987">Apt-get package update 后台任务现在会在视图中以隐藏方式运行</span><span class="sxs-lookup"><span data-stu-id="f6e86-987">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="f6e86-988">清除 ipv6 localhost 的范围（Spring-Framework(Java) 失败）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-988">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="f6e86-989">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-989">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-990">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-990">LTP Results:</span></span>
<span data-ttu-id="f6e86-991">通过的测试数：714</span><span class="sxs-lookup"><span data-stu-id="f6e86-991">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="f6e86-992">未通过的测试数（失败、已跳过等）：249</span><span class="sxs-lookup"><span data-stu-id="f6e86-992">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="f6e86-993">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-993">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="f6e86-994">内部版本 15014</span><span class="sxs-lookup"><span data-stu-id="f6e86-994">Build 15014</span></span>

<span data-ttu-id="f6e86-995">有关内部版本 15014 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-995">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-996">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-996">Fixed</span></span>

- <span data-ttu-id="f6e86-997">Ctrl+C 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="f6e86-997">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="f6e86-998">htop 和 ps auxw 现在会显示正确的资源利用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="f6e86-998">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="f6e86-999">NT 异常到信号的基本转换。</span><span class="sxs-lookup"><span data-stu-id="f6e86-999">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="f6e86-1000">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1000">(GH #513)</span></span>
- <span data-ttu-id="f6e86-1001">当空间耗尽时，fallocate 现在会失败并返回 ENOSPC，而不是返回 EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1001">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="f6e86-1002">添加了 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1002">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="f6e86-1003">实现了 semop 和 semtimedop 系统调用</span><span class="sxs-lookup"><span data-stu-id="f6e86-1003">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="f6e86-1004">修复了 IP_RECVTOS 和 IPV6_RECVTCLASS 套接字选项的 nslookup 错误 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1004">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="f6e86-1005">支持套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="f6e86-1005">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="f6e86-1006">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1006">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1007">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1007">LTP Results:</span></span>
<span data-ttu-id="f6e86-1008">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="f6e86-1008">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="f6e86-1009">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="f6e86-1009">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="f6e86-1010">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1010">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="f6e86-1011">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="f6e86-1011">Syscall Summary</span></span>
<span data-ttu-id="f6e86-1012">Syscall 总数：384</span><span class="sxs-lookup"><span data-stu-id="f6e86-1012">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="f6e86-1013">已实现总数：235</span><span class="sxs-lookup"><span data-stu-id="f6e86-1013">Total Implemented: 235</span></span> </br>
<span data-ttu-id="f6e86-1014">已存根总数：22</span><span class="sxs-lookup"><span data-stu-id="f6e86-1014">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="f6e86-1015">未实现总数：127</span><span class="sxs-lookup"><span data-stu-id="f6e86-1015">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="f6e86-1016">详细分解</span><span class="sxs-lookup"><span data-stu-id="f6e86-1016">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="f6e86-1017">内部版本 15007</span><span class="sxs-lookup"><span data-stu-id="f6e86-1017">Build 15007</span></span>

<span data-ttu-id="f6e86-1018">有关内部版本 15007 的一般 Windows 信息，请访问 [Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1018">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="f6e86-1019">已知问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1019">Known Issue</span></span>

- <span data-ttu-id="f6e86-1020">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1020">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="f6e86-1021">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1021">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="f6e86-1022">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1022">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="f6e86-1023">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1023">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="f6e86-1024">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="f6e86-1024">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="f6e86-1025">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="f6e86-1025">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="f6e86-1026">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1026">Fixed</span></span>

- <span data-ttu-id="f6e86-1027">更正了运行 WSL 会消耗 100% 的 CPU 核心的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1027">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="f6e86-1028">现在支持套接字选项 IP_PKTINFO、IPV6_RECVPKTINFO。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1028">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="f6e86-1029">（GH #851、987）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1029">(GH #851, 987)</span></span>
- <span data-ttu-id="f6e86-1030">在 lxcore 中将网络接口物理地址截断为 16 个字节（GH #1452、1414、1343、468、308）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1030">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="f6e86-1031">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1031">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1032">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1032">LTP Results:</span></span>
<span data-ttu-id="f6e86-1033">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="f6e86-1033">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="f6e86-1034">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="f6e86-1034">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="f6e86-1035">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1035">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="f6e86-1036">内部版本 15002</span><span class="sxs-lookup"><span data-stu-id="f6e86-1036">Build 15002</span></span>

<span data-ttu-id="f6e86-1037">有关内部版本 15002 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1037">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="f6e86-1038">已知问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1038">Known Issue</span></span>

<span data-ttu-id="f6e86-1039">两个已知问题：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1039">Two known issues:</span></span>
- <span data-ttu-id="f6e86-1040">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1040">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="f6e86-1041">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1041">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="f6e86-1042">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1042">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="f6e86-1043">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1043">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="f6e86-1044">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="f6e86-1044">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="f6e86-1045">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="f6e86-1045">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="f6e86-1046">当 WSL 运行时，系统线程将消耗 100% 的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1046">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="f6e86-1047">根本原因已解决并已在内部修复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1047">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="f6e86-1048">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1048">Fixed</span></span>

- <span data-ttu-id="f6e86-1049">现在，必须在同一权限级别创建所有 bash 会话。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1049">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="f6e86-1050">尝试在不同级别启动会话将遭到阻止。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1050">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="f6e86-1051">这意味着，管理员和非管理员控制台不能同时运行。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1051">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="f6e86-1052">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1052">(GH #626)</span></span>
<br/>
- <span data-ttu-id="f6e86-1053">实现了以下 NETLINK_ROUTE 消息（需要 Windows 管理员）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1053">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="f6e86-1054">RTM_NEWADDR（支持 `ip addr add`）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1054">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="f6e86-1055">RTM_NEWROUTE（支持 `ip route add`）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1055">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="f6e86-1056">RTM_DELADDR（支持 `ip addr del`）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1056">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="f6e86-1057">RTM_DELROUTE（支持 `ip route del`）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1057">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="f6e86-1058">用于检查要更新的包的计划任务将不再在按流量计费的连接上运行 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1058">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="f6e86-1059">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1059">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="f6e86-1060">实现了 TCP_KEEPCNT 套接字选项 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1060">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="f6e86-1061">实现了 IP_MTU_DISCOVER INET 套接字选项（GH #720、717、170、69）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1061">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="f6e86-1062">删除了旧功能，以通过 NT 路径查找从 init 运行 NT 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1062">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="f6e86-1063">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1063">(GH #1325)</span></span>
- <span data-ttu-id="f6e86-1064">修复 /dev/kmsg 的模式，以允许进行组访问/其他读取访问 (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1064">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="f6e86-1065">实现了 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1065">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="f6e86-1066">更正了进程开始时间显示为 2432 年的错误 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1066">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="f6e86-1067">已将默认 TERM 环境变量切换为 xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1067">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="f6e86-1068">修改了进程分叉期间进程提交的计算方式。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1068">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="f6e86-1069">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1069">(GH #1286)</span></span>
- <span data-ttu-id="f6e86-1070">实现了 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1070">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="f6e86-1071">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1071">(GH #1286)</span></span>
- <span data-ttu-id="f6e86-1072">实现了 /proc/net/route 文件 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1072">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="f6e86-1073">修复了不正确本地化快捷方式名称的错误 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1073">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="f6e86-1074">修复了错误地验证程序标头必须小于（或等于）PATH_MAX 的 elf 分析逻辑。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1074">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="f6e86-1075">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1075">(GH #1048)</span></span>
- <span data-ttu-id="f6e86-1076">为 procfs、sysfs、cgroupfs 和 binfmtfs 实现了 statfs 回调 (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1076">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="f6e86-1077">修复了 AptPackageIndexUpdate 窗口不会关闭的问题（GH #1184，GH #1193 中也有描述）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1077">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="f6e86-1078">添加了 ASLR 个性化 ADDR_NO_RANDOMIZE 支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1078">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="f6e86-1079">（GH #1148、1128）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1079">(GH #1148, 1128)</span></span>
- <span data-ttu-id="f6e86-1080">改善了 PTRACE_GETSIGINFO、SIGSEGV，在 AV 期间会提供正确的 gdb 堆栈跟踪 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1080">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="f6e86-1081">针对 patchelf 二进制文件的 Elf 分析不再失败。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1081">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="f6e86-1082">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1082">(GH #471)</span></span>
- <span data-ttu-id="f6e86-1083">VPN DNS 已传播到 /etc/resolv.conf（GH #416、1350）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1083">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="f6e86-1084">TCP 关闭改进，可以更可靠地传输数据。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1084">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="f6e86-1085">（GH #610、616、1025、1335）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1085">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="f6e86-1086">现在，在打开过多的文件时可返回正确的错误代码 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1086">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="f6e86-1087">（GH #1126、2090）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1087">(GH #1126, 2090)</span></span>
- <span data-ttu-id="f6e86-1088">Windows 审核日志现在会在进程创建审核中报告映像名称。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1088">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="f6e86-1089">现在，在从 bash 窗口内部启动 bash 时会正常失败</span><span class="sxs-lookup"><span data-stu-id="f6e86-1089">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="f6e86-1090">添加了在 interop 无法访问 LxFs 下的工作目录（即 notepad.exe .bashrc）时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="f6e86-1090">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="f6e86-1091">修复了 Windows 路径在 WSL 中截断的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1091">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="f6e86-1092">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1092">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1093">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1093">LTP Results:</span></span>
<span data-ttu-id="f6e86-1094">通过的测试数：690</span><span class="sxs-lookup"><span data-stu-id="f6e86-1094">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="f6e86-1095">未通过的测试数（失败、已跳过等）：274</span><span class="sxs-lookup"><span data-stu-id="f6e86-1095">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="f6e86-1096">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1096">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1097">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1097">Syscall Support</span></span>
<span data-ttu-id="f6e86-1098">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1098">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1099">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1099">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="f6e86-1100">内部版本 14986</span><span class="sxs-lookup"><span data-stu-id="f6e86-1100">Build 14986</span></span>

<span data-ttu-id="f6e86-1101">有关内部版本 14986 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1101">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1102">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1102">Fixed</span></span>

- <span data-ttu-id="f6e86-1103">修复了 Netlink 和 Pty IOCTL 的 bug 检查</span><span class="sxs-lookup"><span data-stu-id="f6e86-1103">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="f6e86-1104">内核版本现在会报告 4.4.0-43，以便与 Xenial 保持一致</span><span class="sxs-lookup"><span data-stu-id="f6e86-1104">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="f6e86-1105">现在，当输入定向到 'nul:' 时会启动 Bash.exe (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1105">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="f6e86-1106">现在，procfs 中会正确报告线程 ID (GH #967)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1106">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="f6e86-1107">现在，inotify_add_watch() 中支持 IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 标志 (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1107">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="f6e86-1108">实现 timer_create 和相关的系统调用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1108">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="f6e86-1109">这会启用 GHC 支持 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1109">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="f6e86-1110">修复了 ping 返回时间 0.000ms 的问题 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1110">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="f6e86-1111">打开过多的文件时返回正确的错误代码。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1111">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="f6e86-1112">修复了 WSL 中的问题：如果网络接口的硬件地址为 32 字节（例如 Teredo 接口），则针对该网络接口数据的 Netlink 请求将会失败并返回 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1112">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="f6e86-1113">请注意，Linux“ip”实用工具包含一个 bug：如果 WSL 报告 32 字节硬件地址，该实用工具将会崩溃。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1113">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="f6e86-1114">这是“ip”（而不是 WSL）中的一个 bug。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1114">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="f6e86-1115">“ip”实用工具会将用于输出硬件地址的字符串缓冲区的长度硬编码，而该缓冲区太小，无法输出 32 字节硬件地址。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1115">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="f6e86-1116">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1116">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1117">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1117">LTP Results:</span></span>
<span data-ttu-id="f6e86-1118">通过的测试数：669</span><span class="sxs-lookup"><span data-stu-id="f6e86-1118">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="f6e86-1119">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="f6e86-1119">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="f6e86-1120">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1120">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1121">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1121">Syscall Support</span></span>
<span data-ttu-id="f6e86-1122">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1122">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1123">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1123">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="f6e86-1124">内部版本 14971</span><span class="sxs-lookup"><span data-stu-id="f6e86-1124">Build 14971</span></span>

<span data-ttu-id="f6e86-1125">有关内部版本 14971 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1125">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1126">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1126">Fixed</span></span>

 - <span data-ttu-id="f6e86-1127">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1127">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="f6e86-1128">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1128">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1129">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1129">LTP Results:</span></span>
<span data-ttu-id="f6e86-1130">自 14965 以来无更改</span><span class="sxs-lookup"><span data-stu-id="f6e86-1130">Unchanged from 14965</span></span> </br>
<span data-ttu-id="f6e86-1131">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="f6e86-1131">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="f6e86-1132">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1132">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1133">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1133">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="f6e86-1134">内部版本 14965</span><span class="sxs-lookup"><span data-stu-id="f6e86-1134">Build 14965</span></span>

<span data-ttu-id="f6e86-1135">有关内部版本 14965 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1135">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1136">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1136">Fixed</span></span>

- <span data-ttu-id="f6e86-1137">支持 Netlink 套接字 NETLINK_ROUTE 协议的 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1137">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="f6e86-1138">为网络枚举启用 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="f6e86-1138">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="f6e86-1139">在 [WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)中可以找到详细信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1139">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="f6e86-1140">/sbin 现在默认位于用户的路径中</span><span class="sxs-lookup"><span data-stu-id="f6e86-1140">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="f6e86-1141">NT 用户路径现在默认会追加到 WSL 路径（即，现在可以键入 notepad.exe，无需将 System32 添加到 Linux 路径）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1141">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="f6e86-1142">添加了对 /proc/sys/kernel/cap_last_cap 的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1142">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="f6e86-1143">现在，如果当前工作目录包含非 ANSI 字符，则可以从 WSL 启动 NT 二进制文件 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1143">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="f6e86-1144">允许在断开连接的 unix 流套接字上关闭。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1144">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="f6e86-1145">添加了对 PR_GET_PDEATHSIG 的支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1145">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="f6e86-1146">添加了对 CLONE_PARENT 的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1146">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="f6e86-1147">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1147">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="f6e86-1148">处理连接到当前终端的请求。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1148">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="f6e86-1149">将 /proc/<pid>/oom_score_adj 标记为可写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1149">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="f6e86-1150">添加 /sys/fs/cgroup 文件夹。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1150">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="f6e86-1151">sched_setaffinity 应返回关联位掩码的数目</span><span class="sxs-lookup"><span data-stu-id="f6e86-1151">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="f6e86-1152">修复错误地假设解释器路径长度必须小于 64 个字符的 ELF 验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1152">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="f6e86-1153">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1153">(GH #743)</span></span>
- <span data-ttu-id="f6e86-1154">打开文件描述符会使控制台窗口保持打开状态 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1154">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="f6e86-1155">修复了当目标名称包含尾随斜杠时 rename() 失败的错误 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1155">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="f6e86-1156">实现 /proc/net/dev 文件</span><span class="sxs-lookup"><span data-stu-id="f6e86-1156">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="f6e86-1157">修复了计时器精度导致的 0.000ms ping 错误。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1157">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="f6e86-1158">实现了 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1158">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="f6e86-1159">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1159">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1160">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1160">LTP Results:</span></span>
<span data-ttu-id="f6e86-1161">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="f6e86-1161">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="f6e86-1162">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1162">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1163">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1163">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="f6e86-1164">内部版本 14959</span><span class="sxs-lookup"><span data-stu-id="f6e86-1164">Build 14959</span></span>

<span data-ttu-id="f6e86-1165">有关内部版本 14959 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1165">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1166">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1166">Fixed</span></span>

- <span data-ttu-id="f6e86-1167">改善了 Windows 的 Pico 进程通知。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1167">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="f6e86-1168">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)中可以找到更多信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1168">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="f6e86-1169">改善了 Windows 互操作的稳定性</span><span class="sxs-lookup"><span data-stu-id="f6e86-1169">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="f6e86-1170">修复了在启用企业数据保护 (EDP) 后启动 bash.exe 时出现的错误 0x80070057</span><span class="sxs-lookup"><span data-stu-id="f6e86-1170">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="f6e86-1171">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1171">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1172">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1172">LTP Results:</span></span>
<span data-ttu-id="f6e86-1173">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="f6e86-1173">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="f6e86-1174">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1174">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1175">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1175">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="f6e86-1176">内部版本 14955</span><span class="sxs-lookup"><span data-stu-id="f6e86-1176">Build 14955</span></span>

<span data-ttu-id="f6e86-1177">有关内部版本 14955 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1177">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1178">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1178">Fixed</span></span>

 - <span data-ttu-id="f6e86-1179">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1179">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="f6e86-1180">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1180">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1181">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1181">LTP Results:</span></span>
<span data-ttu-id="f6e86-1182">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="f6e86-1182">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="f6e86-1183">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1183">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1184">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1184">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="f6e86-1185">内部版本 14951</span><span class="sxs-lookup"><span data-stu-id="f6e86-1185">Build 14951</span></span>

<span data-ttu-id="f6e86-1186">有关内部版本 14951 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1186">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="f6e86-1187">新功能：Windows/Ubuntu 互操作性</span><span class="sxs-lookup"><span data-stu-id="f6e86-1187">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="f6e86-1188">现在可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1188">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="f6e86-1189">这样，用户便可以通过前所未有的方式来与其 Windows 环境和系统交互。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1189">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="f6e86-1190">举个简单的例子，用户现在可以运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1190">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="f6e86-1191">可在以下资源中找到详细信息：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1191">More information can be found at:</span></span>

- [<span data-ttu-id="f6e86-1192">WSL 团队的互操作博客</span><span class="sxs-lookup"><span data-stu-id="f6e86-1192">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="f6e86-1193">MSDN 互操作文档</span><span class="sxs-lookup"><span data-stu-id="f6e86-1193">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1194">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1194">Fixed</span></span>

- <span data-ttu-id="f6e86-1195">现在将为所有新的 WSL 实例安装 Ubuntu 16.04 (Xenial)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1195">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="f6e86-1196">使用现有 14.04 (Trusty) 实例的用户不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1196">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="f6e86-1197">现在会显示安装过程中指定的区域设置</span><span class="sxs-lookup"><span data-stu-id="f6e86-1197">Locale set during install is now displayed</span></span>
- <span data-ttu-id="f6e86-1198">终端改进，包括修复了不是总能将 WSL 进程重定向到文件的 bug</span><span class="sxs-lookup"><span data-stu-id="f6e86-1198">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="f6e86-1199">控制台生存期应与 bash.exe 生存期密切关联</span><span class="sxs-lookup"><span data-stu-id="f6e86-1199">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="f6e86-1200">控制台窗口大小应使用可视大小，而不是缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="f6e86-1200">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="f6e86-1201">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1201">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1202">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1202">LTP Results:</span></span>
<span data-ttu-id="f6e86-1203">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="f6e86-1203">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="f6e86-1204">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1204">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1205">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1205">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="f6e86-1206">内部版本 14946</span><span class="sxs-lookup"><span data-stu-id="f6e86-1206">Build 14946</span></span>

<span data-ttu-id="f6e86-1207">有关内部版本 14946 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1207">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1208">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1208">Fixed</span></span>

- <span data-ttu-id="f6e86-1209">修复了阻止使用包含空格或引号的 NT 用户名为用户创建 WSL 用户帐户的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1209">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="f6e86-1210">更改 VolFs 和 DrvFs，以在统计信息中返回 0 作为目录的链接计数</span><span class="sxs-lookup"><span data-stu-id="f6e86-1210">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="f6e86-1211">支持 IPV6_MULTICAST_HOPS 套接字选项。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1211">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="f6e86-1212">限制为每个 tty 只有一个控制台 I/O 循环。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1212">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="f6e86-1213">例如，可运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1213">Example: the following command is possible:</span></span>
  - <span data-ttu-id="f6e86-1214">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="f6e86-1214">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="f6e86-1215">在 /proc/cpuinfo 中将空格替换为制表符 (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1215">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="f6e86-1216">DrvFs 现在会显示在 mountinfo 中，其中包含一个与已装载的 Windows 卷匹配的名称</span><span class="sxs-lookup"><span data-stu-id="f6e86-1216">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="f6e86-1217">/home 和 /root 现在会显示在 mountinfo 中，并显示正确的名称</span><span class="sxs-lookup"><span data-stu-id="f6e86-1217">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="f6e86-1218">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1218">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1219">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1219">LTP Results:</span></span>
<span data-ttu-id="f6e86-1220">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="f6e86-1220">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="f6e86-1221">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1221">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1222">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1222">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="f6e86-1223">内部版本 14942</span><span class="sxs-lookup"><span data-stu-id="f6e86-1223">Build 14942</span></span>

<span data-ttu-id="f6e86-1224">有关内部版本 14942 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1224">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1225">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1225">Fixed</span></span>

- <span data-ttu-id="f6e86-1226">解决了一些 bug 检查，包括阻止 SSH 的“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”网络崩溃</span><span class="sxs-lookup"><span data-stu-id="f6e86-1226">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="f6e86-1227">inotifiy 现在支持从 DrvFs 上的 Windows 应用程序生成通知</span><span class="sxs-lookup"><span data-stu-id="f6e86-1227">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="f6e86-1228">实现 mongod 的 TCP_KEEPIDLE 和 TCP_KEEPINTVL。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1228">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="f6e86-1229">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1229">(GH #695)</span></span>
- <span data-ttu-id="f6e86-1230">实现 pivot_root 系统调用</span><span class="sxs-lookup"><span data-stu-id="f6e86-1230">Implement the pivot_root system call</span></span>
- <span data-ttu-id="f6e86-1231">实现 SO_DONTROUTE 的套接字选项</span><span class="sxs-lookup"><span data-stu-id="f6e86-1231">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="f6e86-1232">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1232">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="f6e86-1233">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1233">LTP Results:</span></span>
<span data-ttu-id="f6e86-1234">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="f6e86-1234">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="f6e86-1235">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="f6e86-1235">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="f6e86-1236">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1236">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1237">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1237">Syscall Support</span></span>
<span data-ttu-id="f6e86-1238">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1238">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1239">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1239">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="f6e86-1240">内部版本 14936</span><span class="sxs-lookup"><span data-stu-id="f6e86-1240">Build 14936</span></span>

<span data-ttu-id="f6e86-1241">有关内部版本 14936 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1241">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="f6e86-1242">注意：在即将发布的版本中，WSL 将会安装 Ubuntu 版本16.04 (Xenial) 而不是 Ubuntu 14.04 (Trusty)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1242">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="f6e86-1243">此更改将应用到安装新实例的预览体验版（lxrun /install 或首次运行 bash.exe）。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1243">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="f6e86-1244">包含 Trusty 的现有实例不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1244">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="f6e86-1245">用户可以使用 do-release-upgrade 命令将其 Trusty 映像升级到 Xenial。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1245">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="f6e86-1246">已知问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1246">Known Issue</span></span>
<span data-ttu-id="f6e86-1247">WSL 遇到了某些套接字实现的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1247">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="f6e86-1248">bug 检查将自身显示为崩溃，并出现错误“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1248">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="f6e86-1249">此问题的最常见表现形式是使用 ssh 时发生崩溃。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1249">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="f6e86-1250">根本原因已在内部版本中修复，将会尽快推送到预览体验版。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1250">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="f6e86-1251">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1251">Fixed</span></span>

- <span data-ttu-id="f6e86-1252">实现了 chroot 系统调用</span><span class="sxs-lookup"><span data-stu-id="f6e86-1252">Implemented the chroot system call</span></span>
- <span data-ttu-id="f6e86-1253">inotifiy 的改进，~~包括支持从 DrvFs 上的 Windows 应用程序生成通知~~</span><span class="sxs-lookup"><span data-stu-id="f6e86-1253">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="f6e86-1254">更正：对源自 Windows 应用程序的更改的 Inotify 支持目前不可用。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1254">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="f6e86-1255">与 IPV6::<port n> 的套接字绑定现在支持 IPV6_V6ONLY（GH #68、#157、#393、#460、#674、#740、#982、#996）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1255">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="f6e86-1256">实现了 waitid 系统调用的 WNOWAIT 行为 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1256">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="f6e86-1257">支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="f6e86-1257">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="f6e86-1258">零长度 read() 应立即返回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1258">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="f6e86-1259">在 .tar 文件中正确处理不包含 NULL 终止符的文件名和文件名前缀。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1259">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="f6e86-1260">对 /dev/null 的 epoll 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1260">epoll support for /dev/null</span></span>
- <span data-ttu-id="f6e86-1261">修复 /dev/alarm 时间源</span><span class="sxs-lookup"><span data-stu-id="f6e86-1261">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="f6e86-1262">Bash -c 现在可以重定向到文件</span><span class="sxs-lookup"><span data-stu-id="f6e86-1262">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="f6e86-1263">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1263">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1264">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1264">LTP Results:</span></span>
<span data-ttu-id="f6e86-1265">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="f6e86-1265">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="f6e86-1266">未通过的测试数（失败、已跳过等）：264</span><span class="sxs-lookup"><span data-stu-id="f6e86-1266">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="f6e86-1267">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1267">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1268">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1268">Syscall Support</span></span>
<span data-ttu-id="f6e86-1269">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1269">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1270">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1270">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="f6e86-1271">内部版本 14931</span><span class="sxs-lookup"><span data-stu-id="f6e86-1271">Build 14931</span></span>

<span data-ttu-id="f6e86-1272">有关内部版本 14931 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1272">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1273">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1273">Fixed</span></span>

 - <span data-ttu-id="f6e86-1274">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1274">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="f6e86-1275">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1275">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="f6e86-1276">内部版本 14926</span><span class="sxs-lookup"><span data-stu-id="f6e86-1276">Build 14926</span></span>

<span data-ttu-id="f6e86-1277">有关内部版本 14926 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1277">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1278">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1278">Fixed</span></span>

- <span data-ttu-id="f6e86-1279">Ping 现在可以在没有管理员特权的控制台中正常运行</span><span class="sxs-lookup"><span data-stu-id="f6e86-1279">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="f6e86-1280">现在支持 Ping6，也无需管理员特权</span><span class="sxs-lookup"><span data-stu-id="f6e86-1280">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="f6e86-1281">对通过 WSL 修改的文件的 Inotify 支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1281">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="f6e86-1282">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1282">(GH #216)</span></span>
  - <span data-ttu-id="f6e86-1283">支持的标志：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1283">Flags supported:</span></span>
    - <span data-ttu-id="f6e86-1284">inotify_init1：LX_O_CLOEXEC、LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="f6e86-1284">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="f6e86-1285">inotify_add_watch 事件：LX_IN_ACCESS、LX_IN_MODIFY、LX_IN_ATTRIB、LX_IN_CLOSE_WRITE、LX_IN_CLOSE_NOWRITE、LX_IN_OPEN、LX_IN_MOVED_FROM、LX_IN_MOVED_TO、LX_IN_CREATE、LX_IN_DELETE、LX_IN_DELETE_SELF、LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="f6e86-1285">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="f6e86-1286">inotify_add_watch 属性：LX_IN_DONT_FOLLOW、LX_IN_EXCL_UNLINK、LX_IN_MASK_ADD、LX_IN_ONESHOT、LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="f6e86-1286">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="f6e86-1287">读取输出：LX_IN_ISDIR、LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="f6e86-1287">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="f6e86-1288">已知问题：修改 Windows 应用程序中的文件不会生成任何事件</span><span class="sxs-lookup"><span data-stu-id="f6e86-1288">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="f6e86-1289">Unix 套接字现在支持 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="f6e86-1289">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="f6e86-1290">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="f6e86-1290">LTP Results:</span></span>
<span data-ttu-id="f6e86-1291">通过的测试数：651</span><span class="sxs-lookup"><span data-stu-id="f6e86-1291">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="f6e86-1292">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="f6e86-1292">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="f6e86-1293">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1293">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="f6e86-1294">内部版本 14915</span><span class="sxs-lookup"><span data-stu-id="f6e86-1294">Build 14915</span></span>

<span data-ttu-id="f6e86-1295">有关内部版本 14915 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1295">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1296">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1296">Fixed</span></span>
-  <span data-ttu-id="f6e86-1297">Unix 数据报套接字的套接字对 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1297">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="f6e86-1298">对 SO_REUSEADDR 的 Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1298">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="f6e86-1299">对 SO_BROADCAST 的 UNIX 套接字支持 (GH #568)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1299">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="f6e86-1300">对 SOCK_SEQPACKET 的 Unix 套接字支持（GH #758、#546）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1300">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="f6e86-1301">添加对 Unix 数据报套接字 send、recv 和 shutdown 的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1301">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="f6e86-1302">修复对非固定地址的无效 mmap 参数验证导致的 bug 检查。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1302">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="f6e86-1303">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1303">(GH #847)</span></span>
- <span data-ttu-id="f6e86-1304">支持暂停/恢复终端状态</span><span class="sxs-lookup"><span data-stu-id="f6e86-1304">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="f6e86-1305">支持使用 TIOCPKT ioctl 阻止 Screen 实用工具 (GH #774)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1305">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="f6e86-1306">已知问题：功能键不起作用</span><span class="sxs-lookup"><span data-stu-id="f6e86-1306">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="f6e86-1307">更正了 TimerFd 中的一种争用状态，该状态可能导致 LxpTimerFdWorkerRoutine 访问已释放的成员“ReaderReady” (GH #814)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1307">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="f6e86-1308">为 futex、poll 和 clock_nanosleep 启用可重启系统调用支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1308">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="f6e86-1309">添加了绑定装载支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1309">Added bind mount support</span></span>
- <span data-ttu-id="f6e86-1310">装载命名空间支持的取消共享</span><span class="sxs-lookup"><span data-stu-id="f6e86-1310">unshare for mount namespace support</span></span>
    - <span data-ttu-id="f6e86-1311">已知问题：使用 `unshare(CLONE_NEWNS)` 创建新的装载命名空间时，当前工作目录将继续指向旧命名空间</span><span class="sxs-lookup"><span data-stu-id="f6e86-1311">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="f6e86-1312">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="f6e86-1312">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="f6e86-1313">内部版本 14905</span><span class="sxs-lookup"><span data-stu-id="f6e86-1313">Build 14905</span></span>

<span data-ttu-id="f6e86-1314">有关内部版本 14905 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1314">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1315">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1315">Fixed</span></span>
- <span data-ttu-id="f6e86-1316">现在支持可重启系统调用（GH #349、GH #520）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1316">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="f6e86-1317">现在可正常使用指向以 / 结尾的目录的符号链接 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1317">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="f6e86-1318">为 /dev/random 实现了 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="f6e86-1318">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="f6e86-1319">实现了 /proc/[pid]/mounts、/proc/[pid]/mountinfo 和 /proc/[pid]/mountstats 文件</span><span class="sxs-lookup"><span data-stu-id="f6e86-1319">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="f6e86-1320">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1320">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="f6e86-1321">内部版本 14901</span><span class="sxs-lookup"><span data-stu-id="f6e86-1321">Build 14901</span></span>
<span data-ttu-id="f6e86-1322">Windows 10 周年更新版的第一个预览体验内部版本。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1322">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="f6e86-1323">有关内部版本 14901 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1323">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1324">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1324">Fixed</span></span>
- <span data-ttu-id="f6e86-1325">修复了尾随斜杠问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1325">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="f6e86-1326">`$ mv a/c/ a/b/` 等命令现在可正常运行</span><span class="sxs-lookup"><span data-stu-id="f6e86-1326">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="f6e86-1327">安装程序现在会提示是否应将 Ubuntu 区域设置指定为 Windows 区域设置</span><span class="sxs-lookup"><span data-stu-id="f6e86-1327">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="f6e86-1328">对 ns 文件夹的 Procfs 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1328">Procfs support for ns folder</span></span>
- <span data-ttu-id="f6e86-1329">添加了 tmpfs、procfs 和 sysfs 文件系统的装入点和卸载点</span><span class="sxs-lookup"><span data-stu-id="f6e86-1329">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="f6e86-1330">修复 mknod [at] 32 位 ABI 签名</span><span class="sxs-lookup"><span data-stu-id="f6e86-1330">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="f6e86-1331">Unix 套接字已移到调度模型</span><span class="sxs-lookup"><span data-stu-id="f6e86-1331">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="f6e86-1332">应遵循使用 setsockopt 设置的 INET 套接字接收缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="f6e86-1332">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="f6e86-1333">实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志</span><span class="sxs-lookup"><span data-stu-id="f6e86-1333">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="f6e86-1334">Linux 进程 stdin/stdout 管道重定向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1334">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="f6e86-1335">允许在 CMD 中使用竖线分隔 bash -c 命令。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1335">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="f6e86-1336">示例：>dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="f6e86-1336">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="f6e86-1337">Bash 现在可以安装在包含多个页面文件的系统上（GH #538、#358）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1337">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="f6e86-1338">默认的 INET 套接字缓冲区大小应与默认 Ubuntu 安装的大小相匹配</span><span class="sxs-lookup"><span data-stu-id="f6e86-1338">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="f6e86-1339">将 xattr syscall 与 listxattr 对齐</span><span class="sxs-lookup"><span data-stu-id="f6e86-1339">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="f6e86-1340">仅返回使用 SIOCGIFCONF 中有效 IPv4 地址的接口</span><span class="sxs-lookup"><span data-stu-id="f6e86-1340">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="f6e86-1341">修复 ptrace 注入时的信号默认操作</span><span class="sxs-lookup"><span data-stu-id="f6e86-1341">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="f6e86-1342">实现 /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="f6e86-1342">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="f6e86-1343">在 sigreturn 中还原上下文时使用计算机上下文寄存器值</span><span class="sxs-lookup"><span data-stu-id="f6e86-1343">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="f6e86-1344">这解决了某些用户遇到的 java 和 javac 挂起问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1344">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="f6e86-1345">实现 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="f6e86-1345">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1346">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1346">Syscall Support</span></span>
<span data-ttu-id="f6e86-1347">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1347">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1348">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1348">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="f6e86-1349">Windows 10 周年更新的内部版本 14388</span><span class="sxs-lookup"><span data-stu-id="f6e86-1349">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="f6e86-1350">有关内部版本 14388 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1350">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1351">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1351">Fixed</span></span>
- <span data-ttu-id="f6e86-1352">修复在 8/2 准备 Windows 10 周年更新时出现的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1352">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="f6e86-1353">可在我们的[博客](https://blogs.msdn.microsoft.com/wsl/)中找到有关周年更新中的 WSL 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1353">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="f6e86-1354">内部版本 14376</span><span class="sxs-lookup"><span data-stu-id="f6e86-1354">Build 14376</span></span>
<span data-ttu-id="f6e86-1355">有关内部版本 14376 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1355">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1356">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1356">Fixed</span></span>
- <span data-ttu-id="f6e86-1357">删除了一些存在 apt-get 挂起问题的实例 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1357">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="f6e86-1358">修复了不正确处理空装入点的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1358">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="f6e86-1359">修复了不正确装载 ramdisk 的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1359">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="f6e86-1360">更改 unix 套接字接受行为以支持标志（在 GH #451 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1360">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="f6e86-1361">修复了与网络相关的常见蓝屏问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1361">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="f6e86-1362">修复了访问 /proc/[pid]/task 时出现蓝屏的问题 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1362">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="f6e86-1363">修复了在某些 pty 方案中 CPU 利用率偏高的问题（GH #488、#504）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1363">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="f6e86-1364">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1364">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="f6e86-1365">内部版本 14371</span><span class="sxs-lookup"><span data-stu-id="f6e86-1365">Build 14371</span></span>
<span data-ttu-id="f6e86-1366">有关内部版本 14371 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1366">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1367">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1367">Fixed</span></span>
- <span data-ttu-id="f6e86-1368">更正了使用 ptrace 时 SIGCHLD 和 wait() 出现计时争用的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1368">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="f6e86-1369">更正了当路径包含尾随 / 时出现的某种行为 (GH #432)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1369">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="f6e86-1370">修复了由于打开子级句柄导致重命名/取消链接失败的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1370">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="f6e86-1371">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1371">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="f6e86-1372">内部版本 14366</span><span class="sxs-lookup"><span data-stu-id="f6e86-1372">Build 14366</span></span>
<span data-ttu-id="f6e86-1373">有关内部版本 14366 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1373">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1374">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1374">Fixed</span></span>
- <span data-ttu-id="f6e86-1375">修复通过符号链接创建文件的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1375">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="f6e86-1376">添加了 Python 的 listxattr (GH 385)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1376">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="f6e86-1377">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1377">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1378">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1378">Syscall Support</span></span>
-   <span data-ttu-id="f6e86-1379">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1379">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1380">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1380">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="f6e86-1381">内部版本 14361</span><span class="sxs-lookup"><span data-stu-id="f6e86-1381">Build 14361</span></span>
<span data-ttu-id="f6e86-1382">有关内部版本 14361 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1382">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1383">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1383">Fixed</span></span>
- <span data-ttu-id="f6e86-1384">现在，在 Windows 上的 Ubuntu Bash 中运行时，DrvFs 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1384">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="f6e86-1385">用户可在其 /mnt/c 驱动器中保存 case.txt 和 CASE.TXT</span><span class="sxs-lookup"><span data-stu-id="f6e86-1385">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="f6e86-1386">只有 Windows 上的 Ubuntu Bash 支持区分大小写。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1386">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="f6e86-1387">在 Bash 外部，NTFS 会正确报告文件，但在与 Windows 中的文件交互时，可能会出现意外的行为。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1387">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="f6e86-1388">每个卷的根目录（即 /mnt/c）不区分大小写</span><span class="sxs-lookup"><span data-stu-id="f6e86-1388">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="f6e86-1389">可在[此处](https://support.microsoft.com/en-us/kb/100625)找到有关处理 Windows 中的这些文件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1389">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="f6e86-1390">大幅增强了 pty/tty 支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1390">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="f6e86-1391">现在支持 TMUX 等应用程序 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1391">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="f6e86-1392">修复了不总会创建用户帐户的安装问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1392">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="f6e86-1393">优化了命令行参数结构，允许极长的参数列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1393">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="f6e86-1394">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1394">(GH #153)</span></span>
- <span data-ttu-id="f6e86-1395">现在可对 DrvFs 中的只读文件执行删除和 chmod</span><span class="sxs-lookup"><span data-stu-id="f6e86-1395">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="f6e86-1396">修复了一些在断开连接时终端会挂起的实例 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1396">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="f6e86-1397">现在可在 tty 设备上正常运行 chmod 和 chown</span><span class="sxs-lookup"><span data-stu-id="f6e86-1397">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="f6e86-1398">允许连接到作为 localhost 的 0.0.0.0 和 :: (GH #388)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1398">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="f6e86-1399">Sendmsg/recvmsg 现在可处理大于 1 的 IO 矢量长度（在 GH #376 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1399">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="f6e86-1400">用户现在可以选择禁用自动生成的 hosts 文件 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1400">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="f6e86-1401">在安装期间自动将 Linux 区域设置与 NT 区域设置进行匹配 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1401">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="f6e86-1402">添加了 /proc/sys/vm/swappiness 文件 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1402">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="f6e86-1403">strace 现在会正常退出</span><span class="sxs-lookup"><span data-stu-id="f6e86-1403">strace now exits correctly</span></span>
- <span data-ttu-id="f6e86-1404">允许通过 /proc/self/fd 重新打开管道 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1404">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="f6e86-1405">在 DrvFs 中隐藏 %LOCALAPPDATA%\lxss 下的目录 (GH #270)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1405">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="f6e86-1406">更好地处理 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1406">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="f6e86-1407">现在支持类似于“bash ~ -c ls”的命令 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1407">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="f6e86-1408">现在，在关闭期间，套接字会通知 epoll read 可用 (GH #271)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1408">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="f6e86-1409">lxrun /uninstall 可以更好地删除文件和文件夹</span><span class="sxs-lookup"><span data-stu-id="f6e86-1409">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="f6e86-1410">更正了 ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1410">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="f6e86-1411">改善了对 xEmacs 等 x11 应用的支持 (GH #481)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1411">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="f6e86-1412">更新了初始线程堆栈大小，以匹配默认的 Ubuntu 设置，并正确地向 get_rlimit syscall 报告大小（GH #172、#258）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1412">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="f6e86-1413">改善了 pico 进程映像名称的报告（例如，用于审核）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1413">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="f6e86-1414">实现了 df 命令的 /proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="f6e86-1414">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="f6e86-1415">修复了子名称 .</span><span class="sxs-lookup"><span data-stu-id="f6e86-1415">Fixed symlink error code for child name .</span></span> <span data-ttu-id="f6e86-1416">和 .. 的符号链接错误代码</span><span class="sxs-lookup"><span data-stu-id="f6e86-1416">and ..</span></span>
- <span data-ttu-id="f6e86-1417">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1417">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1418">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1418">Syscall Support</span></span>
<span data-ttu-id="f6e86-1419">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1419">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1420">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1420">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="f6e86-1421">内部版本 14352</span><span class="sxs-lookup"><span data-stu-id="f6e86-1421">Build 14352</span></span>
<span data-ttu-id="f6e86-1422">有关内部版本 14352 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1422">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1423">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1423">Fixed</span></span>
- <span data-ttu-id="f6e86-1424">修复了不正常下载/创建大型文件的问题。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1424">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="f6e86-1425">这应该可以解除 npm 和其他方案的阻碍（GH #3、GH #313）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1425">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="f6e86-1426">删除了一些存在套接字挂起情况的实例</span><span class="sxs-lookup"><span data-stu-id="f6e86-1426">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="f6e86-1427">更正了一些 ptrace 错误</span><span class="sxs-lookup"><span data-stu-id="f6e86-1427">Corrected some ptrace errors</span></span>
- <span data-ttu-id="f6e86-1428">修复了 WSL 中的问题，允许超过 255 个字符的文件名</span><span class="sxs-lookup"><span data-stu-id="f6e86-1428">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="f6e86-1429">改善了对非英语字符的支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1429">Improved support for non-English characters</span></span>
- <span data-ttu-id="f6e86-1430">添加当前 Windows 时区数据并将其设为默认值</span><span class="sxs-lookup"><span data-stu-id="f6e86-1430">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="f6e86-1431">每个装入点的唯一设备 ID （JRE 修复 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="f6e86-1431">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="f6e86-1432">更正路径中包含“.”</span><span class="sxs-lookup"><span data-stu-id="f6e86-1432">Correct issue with paths containing “.”</span></span> <span data-ttu-id="f6e86-1433">和“..”的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1433">and “..”</span></span>
- <span data-ttu-id="f6e86-1434">添加了 Fifo 支持 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1434">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="f6e86-1435">更新了 resolv.conf 的格式，以匹配本机 Ubuntu 格式</span><span class="sxs-lookup"><span data-stu-id="f6e86-1435">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="f6e86-1436">一些 procfs 清理</span><span class="sxs-lookup"><span data-stu-id="f6e86-1436">Some procfs cleanup</span></span>
- <span data-ttu-id="f6e86-1437">为管理员控制台启用了 ping (GH #18)</span><span class="sxs-lookup"><span data-stu-id="f6e86-1437">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1438">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1438">Syscall Support</span></span>
<span data-ttu-id="f6e86-1439">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1439">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1440">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1440">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="f6e86-1441">内部版本 14342</span><span class="sxs-lookup"><span data-stu-id="f6e86-1441">Build 14342</span></span>
<span data-ttu-id="f6e86-1442">有关内部版本 14342 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1442">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="f6e86-1443">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl)中可以找到有关 VolFs 和 DriveFs 的信息。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1443">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="f6e86-1444">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1444">Fixed</span></span>
- <span data-ttu-id="f6e86-1445">修复了 Windows 用户在用户名中包含 Unicode 字符时出现的安装问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1445">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="f6e86-1446">现在，在首次运行时，默认会提供“常见问题解答”中的 apt-get update udev 解决方法</span><span class="sxs-lookup"><span data-stu-id="f6e86-1446">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="f6e86-1447">在 DriveFs (/mnt/<drive>) 目录中启用了符号链接</span><span class="sxs-lookup"><span data-stu-id="f6e86-1447">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="f6e86-1448">现在可以在 DriveFs 和 VolFs 之间使用符号链接</span><span class="sxs-lookup"><span data-stu-id="f6e86-1448">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="f6e86-1449">解决了顶级路径分析问题：ls .// 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="f6e86-1449">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="f6e86-1450">DriveFs 上的 npm install 和 -g 选项现在可正常工作</span><span class="sxs-lookup"><span data-stu-id="f6e86-1450">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="f6e86-1451">修复了阻止 PHP 服务器启动的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1451">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="f6e86-1452">更新了默认环境值（例如 $PATH），以便与本机 Ubuntu 更匹配</span><span class="sxs-lookup"><span data-stu-id="f6e86-1452">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="f6e86-1453">在 Windows 中添加了每周维护任务以更新 apt 包缓存</span><span class="sxs-lookup"><span data-stu-id="f6e86-1453">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="f6e86-1454">修复了 ELF 标头验证的问题，WSL 现在支持所有 Melkor 选项</span><span class="sxs-lookup"><span data-stu-id="f6e86-1454">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="f6e86-1455">Zsh shell 可正常运行</span><span class="sxs-lookup"><span data-stu-id="f6e86-1455">Zsh shell is functional</span></span>
- <span data-ttu-id="f6e86-1456">现在支持预编译的 Go 二进制文件</span><span class="sxs-lookup"><span data-stu-id="f6e86-1456">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="f6e86-1457">现已正确本地化首次运行 Bash 时出现的提示</span><span class="sxs-lookup"><span data-stu-id="f6e86-1457">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="f6e86-1458">/proc/meminfo 现在会返回正确的信息</span><span class="sxs-lookup"><span data-stu-id="f6e86-1458">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="f6e86-1459">VFS 现在支持套接字</span><span class="sxs-lookup"><span data-stu-id="f6e86-1459">Sockets now supported in VFS</span></span>
- <span data-ttu-id="f6e86-1460">/dev 现在装载为 tempfs</span><span class="sxs-lookup"><span data-stu-id="f6e86-1460">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="f6e86-1461">现在支持 Fifo</span><span class="sxs-lookup"><span data-stu-id="f6e86-1461">Fifo now supported</span></span>
- <span data-ttu-id="f6e86-1462">多核系统现在会在 /proc/cpuinfo 中正确显示</span><span class="sxs-lookup"><span data-stu-id="f6e86-1462">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="f6e86-1463">其他改进以及首次运行期间下载内容时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="f6e86-1463">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="f6e86-1464">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1464">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="f6e86-1465">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1465">Supported syscall list below.</span></span>
- <span data-ttu-id="f6e86-1466">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1466">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="f6e86-1467">已知问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1467">Known Issues</span></span>
- <span data-ttu-id="f6e86-1468">在某些情况下，</span><span class="sxs-lookup"><span data-stu-id="f6e86-1468">Not resolving ‘..’</span></span> <span data-ttu-id="f6e86-1469">不会正确解析 DriveFs 上的“..”</span><span class="sxs-lookup"><span data-stu-id="f6e86-1469">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1470">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1470">Syscall Support</span></span>
<span data-ttu-id="f6e86-1471">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1471">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1472">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1472">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="f6e86-1473">内部版本 14332</span><span class="sxs-lookup"><span data-stu-id="f6e86-1473">Build 14332</span></span>

<span data-ttu-id="f6e86-1474">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1474">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="f6e86-1475">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1475">Fixed</span></span>
- <span data-ttu-id="f6e86-1476">更好地生成 resolv.conf，包括指定 DNS 项的优先级</span><span class="sxs-lookup"><span data-stu-id="f6e86-1476">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="f6e86-1477">在 /mnt 与非 /mnt 驱动器之间移动文件和目录时出现的问题</span><span class="sxs-lookup"><span data-stu-id="f6e86-1477">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="f6e86-1478">现在可以使用符号链接创建 Tar 文件。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1478">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="f6e86-1479">创建实例时会添加默认的 /run/lock 目录</span><span class="sxs-lookup"><span data-stu-id="f6e86-1479">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="f6e86-1480">更新 /dev/null 以返回正确的统计信息</span><span class="sxs-lookup"><span data-stu-id="f6e86-1480">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="f6e86-1481">首次运行期间下载内容时出现的其他错误</span><span class="sxs-lookup"><span data-stu-id="f6e86-1481">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="f6e86-1482">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1482">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="f6e86-1483">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1483">Supported syscall list below.</span></span>
- <span data-ttu-id="f6e86-1484">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1484">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1485">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1485">Syscall Support</span></span>
<span data-ttu-id="f6e86-1486">下面是在 WSL 中具有某种实现的新 syscall。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1486">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="f6e86-1487">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1487">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="f6e86-1488">内部版本 14328</span><span class="sxs-lookup"><span data-stu-id="f6e86-1488">Build 14328</span></span>

<span data-ttu-id="f6e86-1489">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1489">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="f6e86-1490">新功能</span><span class="sxs-lookup"><span data-stu-id="f6e86-1490">New Features</span></span>
* <span data-ttu-id="f6e86-1491">现在支持 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1491">Now support Linux users.</span></span>  <span data-ttu-id="f6e86-1492">安装 Windows 上的 Ubuntu Bash 时会提示创建 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1492">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="f6e86-1493">有关详细信息，请访问 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="f6e86-1493">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="f6e86-1494">现在，主机名将设置为 Windows 计算机名，而不再是 @localhost</span><span class="sxs-lookup"><span data-stu-id="f6e86-1494">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="f6e86-1495">有关内部版本 14328 的详细信息，请访问： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="f6e86-1495">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="f6e86-1496">固定</span><span class="sxs-lookup"><span data-stu-id="f6e86-1496">Fixed</span></span>
* <span data-ttu-id="f6e86-1497">非 /mnt/<drive> 文件的符号链接改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1497">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="f6e86-1498">现在可正常运行 npm install</span><span class="sxs-lookup"><span data-stu-id="f6e86-1498">npm install now works</span></span>
    * <span data-ttu-id="f6e86-1499">现在可以根据[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)的说明安装 jdk/jre。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1499">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="f6e86-1500">已知问题：符号链接不适用于 Windows 装载。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1500">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="f6e86-1501">此功能将在以后的内部版本中可用</span><span class="sxs-lookup"><span data-stu-id="f6e86-1501">Functionality will be available in a later build</span></span>
* <span data-ttu-id="f6e86-1502">现在会显示 top 和 htop</span><span class="sxs-lookup"><span data-stu-id="f6e86-1502">top and htop now display</span></span>
* <span data-ttu-id="f6e86-1503">有关某些安装失败的其他错误消息</span><span class="sxs-lookup"><span data-stu-id="f6e86-1503">Additional error messages for some install failures</span></span>
* <span data-ttu-id="f6e86-1504">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1504">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="f6e86-1505">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1505">Supported syscall list below.</span></span>
* <span data-ttu-id="f6e86-1506">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="f6e86-1506">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="f6e86-1507">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="f6e86-1507">Syscall Support</span></span>
<span data-ttu-id="f6e86-1508">下面是在 WSL 中具有某种实现的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1508">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="f6e86-1509">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="f6e86-1509">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
