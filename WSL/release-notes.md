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
ms.openlocfilehash: b92c20bad50d0c58da05bb0c8f26a69d4c0b2970
ms.sourcegitcommit: 050f6095e92469b903db8ddf9356df5b22b21804
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/03/2019
ms.locfileid: "71910303"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="cb04f-105">适用于 Linux 的 Windows 子系统发行说明</span><span class="sxs-lookup"><span data-stu-id="cb04f-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18995"></a><span data-ttu-id="cb04f-106">内部版本 18995</span><span class="sxs-lookup"><span data-stu-id="cb04f-106">Build 18995</span></span>
<span data-ttu-id="cb04f-107">有关内部版本 18995 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-107">For general Windows information on build 18995 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/10/03/announcing-windows-10-insider-preview-build-18995/).</span></span>

* <span data-ttu-id="cb04f-108">[WSL2] 修复了 DrvFs 装载在某项操作被中断（例如 ctrl-c）后失效的问题 [GH 4377]</span><span class="sxs-lookup"><span data-stu-id="cb04f-108">[WSL2] Fix an issue where DrvFs mounts stopped working after an operation was interrupted (e.g. ctrl-c) [GH 4377]</span></span>
* <span data-ttu-id="cb04f-109">[WSL2] 修复了处理极大型 hvsocket 消息的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="cb04f-109">[WSL2] Fix handling of very large hvsocket messages [GH 4105]</span></span>
* <span data-ttu-id="cb04f-110">[WSL2] 修复了当 stdin 为文件时互操作出现的问题 [GH 4475]</span><span class="sxs-lookup"><span data-stu-id="cb04f-110">[WSL2] Fix issue with interop when stdin is a file [GH 4475]</span></span>
* <span data-ttu-id="cb04f-111">[WSL2] 修复了当遇到意外网络状态时服务崩溃的问题 [GH 4474]</span><span class="sxs-lookup"><span data-stu-id="cb04f-111">[WSL2] Fix service crash when unexpected network state is encountered [GH 4474]</span></span>
* <span data-ttu-id="cb04f-112">[WSL2] 在当前进程没有环境变量的情况下从互操作服务器查询发行版名称</span><span class="sxs-lookup"><span data-stu-id="cb04f-112">[WSL2] Query the distro name from the interop server if the current process does not have the environment variable</span></span>
* <span data-ttu-id="cb04f-113">[WSL2] 修复了当 stdin 为文件时互操作出现的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-113">[WSL2] Fix issue with interop whe stdin is a file</span></span>
* <span data-ttu-id="cb04f-114">[WSL2] 将 Linux 内核版本更新到 4.19.72</span><span class="sxs-lookup"><span data-stu-id="cb04f-114">[WSL2] Update Linux kernel version to 4.19.72</span></span>
* <span data-ttu-id="cb04f-115">[WSL2] 添加了通过 .wslconfig 指定其他内核命令行参数的功能</span><span class="sxs-lookup"><span data-stu-id="cb04f-115">[WSL2] Add ability to specify additional kernel command line parameters via .wslconfig</span></span>
```
[wsl2]
kernelCommandLine = <string> # Additional kernel command line arguments

```

## <a name="build-18990"></a><span data-ttu-id="cb04f-116">版本 18990</span><span class="sxs-lookup"><span data-stu-id="cb04f-116">Build 18990</span></span>
<span data-ttu-id="cb04f-117">有关版本 18990 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-117">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="cb04f-118">提高 \\\\wsl$ 中目录列表的性能</span><span class="sxs-lookup"><span data-stu-id="cb04f-118">Improve the performance for directory listings in \\\\wsl$</span></span>
* <span data-ttu-id="cb04f-119">[WSL2] 注入额外的启动熵 [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="cb04f-119">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="cb04f-120">[WSL2] 修复使用 su/sudo 时的 Windows 互操作 [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="cb04f-120">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>


## <a name="build-18980"></a><span data-ttu-id="cb04f-121">内部版本 18980</span><span class="sxs-lookup"><span data-stu-id="cb04f-121">Build 18980</span></span>
<span data-ttu-id="cb04f-122">有关内部版本 18980 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-122">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="cb04f-123">修复拒绝 FILE_READ_DATA 的读取符号链接。</span><span class="sxs-lookup"><span data-stu-id="cb04f-123">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="cb04f-124">这包括 Windows 为了实现后向兼容而创建的所有符号链接（例如“C:\Document and Settings”），以及用户配置文件目录中的一些符号链接。</span><span class="sxs-lookup"><span data-stu-id="cb04f-124">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="cb04f-125">使意外的文件系统状态变得不严重 [GH 4334、4305]</span><span class="sxs-lookup"><span data-stu-id="cb04f-125">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="cb04f-126">[WSL2] 添加当 CPU/固件支持虚拟化时对 arm64 的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-126">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="cb04f-127">[WSL2] 允许无特权用户查看内核日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-127">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="cb04f-128">[WSL2] 修复关闭 stdout/stderr 套接字后的输出中继 [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="cb04f-128">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="cb04f-129">[WSL2] 支持电池和交流适配器直通</span><span class="sxs-lookup"><span data-stu-id="cb04f-129">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="cb04f-130">[WSL2] 将 Linux 内核更新到 4.19.67</span><span class="sxs-lookup"><span data-stu-id="cb04f-130">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="cb04f-131">添加在 /etc/wsl.conf 中设置默认用户名的功能：</span><span class="sxs-lookup"><span data-stu-id="cb04f-131">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=<string>
```

## <a name="build-18975"></a><span data-ttu-id="cb04f-132">内部版本 18975</span><span class="sxs-lookup"><span data-stu-id="cb04f-132">Build 18975</span></span>
<span data-ttu-id="cb04f-133">有关内部版本 18975 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-133">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="cb04f-134">[WSL2] 修复大量 localhost 可靠性问题 [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="cb04f-134">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="cb04f-135">内部版本 18970</span><span class="sxs-lookup"><span data-stu-id="cb04f-135">Build 18970</span></span>
<span data-ttu-id="cb04f-136">有关内部版本 18970 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-136">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="cb04f-137">[WSL2] 当系统从睡眠状态恢复时，使时间与主机时间同步 [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="cb04f-137">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="cb04f-138">[WSL2] 在可能的情况下，在 Windows 卷上创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="cb04f-138">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="cb04f-139">[WSL2] 在 UTS、IPC、PID 和 Mount 命名空间中创建分发版。</span><span class="sxs-lookup"><span data-stu-id="cb04f-139">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="cb04f-140">[WSL2] 修复当服务器直接绑定到 localhost 时的 localhost 端口中继 [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="cb04f-140">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="cb04f-141">[WSL2] 修复重定向输出时的 interop [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="cb04f-141">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="cb04f-142">[WSL2] 支持转换绝对 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="cb04f-142">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="cb04f-143">[WSL2] 将内核更新到 4.19.59</span><span class="sxs-lookup"><span data-stu-id="cb04f-143">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="cb04f-144">[WSL2] 正确设置 eth0 的子网掩码。</span><span class="sxs-lookup"><span data-stu-id="cb04f-144">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="cb04f-145">[WSL2] 发出退出事件信号时更改逻辑，以中断控制台工作线程循环。</span><span class="sxs-lookup"><span data-stu-id="cb04f-145">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="cb04f-146">[WSL2] 分发版未运行时弹出分发版 VHD。</span><span class="sxs-lookup"><span data-stu-id="cb04f-146">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="cb04f-147">[WSL2] 修复配置分析库以正确处理空值。</span><span class="sxs-lookup"><span data-stu-id="cb04f-147">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="cb04f-148">[WSL2] 通过创建跨分发版装入点来支持 Docker Desktop。</span><span class="sxs-lookup"><span data-stu-id="cb04f-148">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="cb04f-149">分发版可以通过将以下行添加到 /etc/wsl.conf 文件来启用此行为：</span><span class="sxs-lookup"><span data-stu-id="cb04f-149">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="cb04f-150">内部版本 18945</span><span class="sxs-lookup"><span data-stu-id="cb04f-150">Build 18945</span></span>
<span data-ttu-id="cb04f-151">有关内部版本 18945 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-151">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-152">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-152">WSL</span></span>
* <span data-ttu-id="cb04f-153">[WSL2] 允许侦听可使用 localhost:port 通过主机访问的 WSL2 中的 TCP 套接字</span><span class="sxs-lookup"><span data-stu-id="cb04f-153">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="cb04f-154">[WSL2] 修复安装/转换失败和其他诊断，以跟踪将来的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="cb04f-154">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="cb04f-155">[WSL2] 改善 WSL2 网络问题的诊断</span><span class="sxs-lookup"><span data-stu-id="cb04f-155">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="cb04f-156">[WSL2] 将内核版本更新到 4.19.55</span><span class="sxs-lookup"><span data-stu-id="cb04f-156">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="cb04f-157">[WSL2] 使用 Docker 所需的配置选项更新了内核 [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="cb04f-157">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="cb04f-158">[WSL2] 增加分配给轻型实用程序 VM 的 CPU 数目，使其与主机相同（以前，内核配置中的 CONFIG_NR_CPUS 将数目限制为 8 个）[GH 4137]</span><span class="sxs-lookup"><span data-stu-id="cb04f-158">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="cb04f-159">[WSL2] 为 WSL2 轻型 VM 创建交换文件</span><span class="sxs-lookup"><span data-stu-id="cb04f-159">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="cb04f-160">[WSL2] 允许通过 \\\\wsl$\\distro（例如 sshfs）显示用户装入点 [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="cb04f-160">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="cb04f-161">[WSL2] 改善 9p 文件系统的性能</span><span class="sxs-lookup"><span data-stu-id="cb04f-161">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="cb04f-162">[WSL2] 确保 VHD ACL 不会无限增长 [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="cb04f-162">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="cb04f-163">[WSL2] 更新内核配置以支持 squashfs 和 xt_conntrack [GH 4107、4123]</span><span class="sxs-lookup"><span data-stu-id="cb04f-163">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="cb04f-164">[WSL2] 修复 interop.enabled /etc/wsl.conf 选项 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="cb04f-164">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="cb04f-165">[WSL2] 如果文件系统不支持 EA，则返回 ENOTSUP</span><span class="sxs-lookup"><span data-stu-id="cb04f-165">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="cb04f-166">[WSL2] 修复 \\\\wsl$ 时 CopyFile 挂起的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-166">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="cb04f-167">将默认 umask 切换为 0022，并将 filesystem.umask 设置添加到 /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="cb04f-167">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="cb04f-168">修复 wslpath 以正确解析符号链接，这是19h1 中的回归 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="cb04f-168">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="cb04f-169">引入 %UserProfile%\\.wslconfig 文件用于调整 WSL2 设置</span><span class="sxs-lookup"><span data-stu-id="cb04f-169">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="cb04f-170">内部版本 18917</span><span class="sxs-lookup"><span data-stu-id="cb04f-170">Build 18917</span></span>
<span data-ttu-id="cb04f-171">有关内部版本 18917 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-171">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-172">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-172">WSL</span></span>
* <span data-ttu-id="cb04f-173">WSL 2 现已推出！</span><span class="sxs-lookup"><span data-stu-id="cb04f-173">WSL 2 is now available!</span></span> <span data-ttu-id="cb04f-174">有关更多详细信息，请参阅[博客](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-174">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="cb04f-175">修复一个回归问题：无法通过符号链接启动 Windows 进程 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="cb04f-175">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="cb04f-176">将 wsl.exe --list --verbose、wsl.exe --list --quiet 和 wsl.exe --import --version 选项添加到 wsl.exe</span><span class="sxs-lookup"><span data-stu-id="cb04f-176">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="cb04f-177">添加 wsl.exe --shutdown 选项</span><span class="sxs-lookup"><span data-stu-id="cb04f-177">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="cb04f-178">Plan 9：允许打开目录以使写入成功</span><span class="sxs-lookup"><span data-stu-id="cb04f-178">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="cb04f-179">内部版本 18890</span><span class="sxs-lookup"><span data-stu-id="cb04f-179">Build 18890</span></span>
<span data-ttu-id="cb04f-180">有关内部版本 18890 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-180">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-181">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-181">WSL</span></span>
* <span data-ttu-id="cb04f-182">非阻塞套接字泄露 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="cb04f-182">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="cb04f-183">在终端中输入 EOF 可能会阻塞后续读取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="cb04f-183">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="cb04f-184">更新 resolv.conf 标头以引用 wsl.conf [在 GH 3928 中介绍]</span><span class="sxs-lookup"><span data-stu-id="cb04f-184">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="cb04f-185">epoll delete 代码中的死锁 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="cb04f-185">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="cb04f-186">处理 --import 和 –export 的参数中的空格 [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="cb04f-186">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="cb04f-187">无法正常扩展 mmap 的文件 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="cb04f-187">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="cb04f-188">修复了 ARM64 \\\\wsl$ 访问不正常的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-188">Fix issue with ARM64 \\\\wsl$ access not working properly</span></span>
* <span data-ttu-id="cb04f-189">为 wsl.exe 添加更好的默认图标</span><span class="sxs-lookup"><span data-stu-id="cb04f-189">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="cb04f-190">内部版本 18342</span><span class="sxs-lookup"><span data-stu-id="cb04f-190">Build 18342</span></span>
<span data-ttu-id="cb04f-191">有关内部版本 18342 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-191">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-192">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-192">WSL</span></span>
* <span data-ttu-id="cb04f-193">我们添加了相应的功能，使用户能够从 Windows 访问 WSL 分发版中的 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-193">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="cb04f-194">可以通过命令行访问这些文件，此外，文件资源管理器、VSCode 等 Windows 应用可与这些文件交互。</span><span class="sxs-lookup"><span data-stu-id="cb04f-194">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="cb04f-195">通过导航到 \\\\wsl$\\<分发版名称> 访问文件，或通过导航到 \\\\wsl$ 来查看正在运行的分发版列表</span><span class="sxs-lookup"><span data-stu-id="cb04f-195">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="cb04f-196">添加额外的 CPU 信息标记，并修复 Cpus_allowed[_list] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="cb04f-196">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="cb04f-197">支持从非领先线程执行 [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="cb04f-197">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="cb04f-198">将配置更新失败视为非严重错误 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="cb04f-198">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="cb04f-199">更新 binfmt 以正确处理偏移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="cb04f-199">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="cb04f-200">为 Plan 9 启用映射网络驱动器 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="cb04f-200">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="cb04f-201">支持对绑定载入点执行“Windows -> Linux”和“Linux -> Windows”路径转换</span><span class="sxs-lookup"><span data-stu-id="cb04f-201">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="cb04f-202">为以只读方式打开的文件中的映射创建只读节</span><span class="sxs-lookup"><span data-stu-id="cb04f-202">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="cb04f-203">内部版本 18334</span><span class="sxs-lookup"><span data-stu-id="cb04f-203">Build 18334</span></span>
<span data-ttu-id="cb04f-204">有关内部版本 18334 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-204">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-205">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-205">WSL</span></span>
* <span data-ttu-id="cb04f-206">重新设计 Windows 时区映射到 Linux 时区的方式 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="cb04f-206">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="cb04f-207">修复内存泄漏，并添加新的字符串转换函数 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="cb04f-207">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="cb04f-208">不包含任何线程的线程组上的 SIGCONT 是一个 no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="cb04f-208">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="cb04f-209">在 /proc/self/fd 中正确显示套接字和 epoll 文件描述符</span><span class="sxs-lookup"><span data-stu-id="cb04f-209">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="cb04f-210">内部版本 18305</span><span class="sxs-lookup"><span data-stu-id="cb04f-210">Build 18305</span></span>
<span data-ttu-id="cb04f-211">有关内部版本 18305 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-211">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-212">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-212">WSL</span></span>
* <span data-ttu-id="cb04f-213">当主线程退出时，pthreads 失去对文件的访问权限 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="cb04f-213">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="cb04f-214">除非有必要，否则 TIOCSCTTY 应忽略“force”参数 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="cb04f-214">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="cb04f-215">改善 wsl.exe 命令行，并添加导入/导出功能。</span><span class="sxs-lookup"><span data-stu-id="cb04f-215">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="cb04f-216">内部版本 18277</span><span class="sxs-lookup"><span data-stu-id="cb04f-216">Build 18277</span></span>
<span data-ttu-id="cb04f-217">有关内部版本 18277 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-217">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-218">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-218">WSL</span></span>
* <span data-ttu-id="cb04f-219">修复内部版本 18272 中引入的“不支持此类接口”错误 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="cb04f-219">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="cb04f-220">忽略 umount syscall 的 MNT_FORCE 标志 [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="cb04f-220">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="cb04f-221">切换 WSL interop 以使用官方的 CreatePseudoConsole API</span><span class="sxs-lookup"><span data-stu-id="cb04f-221">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="cb04f-222">FUTEX_WAIT 重启时不保留超时值</span><span class="sxs-lookup"><span data-stu-id="cb04f-222">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="cb04f-223">内部版本 18272</span><span class="sxs-lookup"><span data-stu-id="cb04f-223">Build 18272</span></span>
<span data-ttu-id="cb04f-224">有关内部版本 18272 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-224">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-225">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-225">WSL</span></span>
* <span data-ttu-id="cb04f-226">**警告：** 此版本中存在一个导致 WSL 不可操作的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-226">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="cb04f-227">尝试启动分发版时，会看到“不支持此类接口”错误。</span><span class="sxs-lookup"><span data-stu-id="cb04f-227">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="cb04f-228">该问题已修复，下周发布的 Insider Fast 内部版本将会应用修复程序。</span><span class="sxs-lookup"><span data-stu-id="cb04f-228">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="cb04f-229">如果已安装此内部版本，可以使用“设置”->“更新和安全”>“恢复”中的“回退到 Windows 10 的上一个版本”回滚到上一 Windows 内部版本。</span><span class="sxs-lookup"><span data-stu-id="cb04f-229">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="cb04f-230">内部版本 18267</span><span class="sxs-lookup"><span data-stu-id="cb04f-230">Build 18267</span></span>
<span data-ttu-id="cb04f-231">有关内部版本 18267 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-231">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-232">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-232">WSL</span></span>
* <span data-ttu-id="cb04f-233">修复 zombie 进程不会回收，而是无限期保留的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-233">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="cb04f-234">如果错误消息超过最大长度，WslRegisterDistribution 将会挂起 [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="cb04f-234">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="cb04f-235">允许 fsync 针对 DrvFs 上的只读文件成功运行 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="cb04f-235">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="cb04f-236">在内部创建符号链接之前，确保 /bin 和 /sbin 目录存在 [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="cb04f-236">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="cb04f-237">为 WSL 实例添加了实例终止超时机制。</span><span class="sxs-lookup"><span data-stu-id="cb04f-237">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="cb04f-238">超时目前设置为 15 秒，这意味着，实例将在上一个 WSL 进程退出 15 秒后终止。</span><span class="sxs-lookup"><span data-stu-id="cb04f-238">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="cb04f-239">若要立即终止分发版，请使用：</span><span class="sxs-lookup"><span data-stu-id="cb04f-239">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="cb04f-240">内部版本 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="cb04f-240">Build 17763 (1809)</span></span>
<span data-ttu-id="cb04f-241">有关内部版本 17763 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-241">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-242">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-242">WSL</span></span>
* <span data-ttu-id="cb04f-243">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="cb04f-243">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="cb04f-244">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="cb04f-244">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="cb04f-245">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="cb04f-245">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="cb04f-246">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="cb04f-246">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="cb04f-247">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="cb04f-247">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="cb04f-248">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="cb04f-248">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="cb04f-249">修复多个 AF_UNIX 相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="cb04f-249">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="cb04f-250">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="cb04f-250">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="cb04f-251">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="cb04f-251">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="cb04f-252">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="cb04f-252">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="cb04f-253">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-253">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="cb04f-254">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="cb04f-254">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="cb04f-255">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="cb04f-255">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="cb04f-256">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="cb04f-256">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="cb04f-257">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="cb04f-257">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="cb04f-258">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="cb04f-258">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="cb04f-259">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="cb04f-259">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="cb04f-260">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="cb04f-260">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="cb04f-261">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="cb04f-261">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="cb04f-262">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="cb04f-262">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="cb04f-263">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="cb04f-263">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="cb04f-264">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-264">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="cb04f-265">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="cb04f-265">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="cb04f-266">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="cb04f-266">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="cb04f-267">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="cb04f-267">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="cb04f-268">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="cb04f-268">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="cb04f-269">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="cb04f-269">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="cb04f-270">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="cb04f-270">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="cb04f-271">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-271">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="cb04f-272">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="cb04f-272">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="cb04f-273">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-273">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="cb04f-274">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="cb04f-274">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="cb04f-275">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="cb04f-275">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="cb04f-276">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-276">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="cb04f-277">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="cb04f-277">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="cb04f-278">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="cb04f-278">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="cb04f-279">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="cb04f-279">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="cb04f-280">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="cb04f-280">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="cb04f-281">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="cb04f-281">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="cb04f-282">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="cb04f-282">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="cb04f-283">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="cb04f-283">[GH 2712]</span></span>
* <span data-ttu-id="cb04f-284">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-284">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="cb04f-285">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="cb04f-285">[GH 3020]</span></span>
* <span data-ttu-id="cb04f-286">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-286">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="cb04f-287">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="cb04f-287">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="cb04f-288">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="cb04f-288">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="cb04f-289">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-289">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="cb04f-290">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-290">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="cb04f-291">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-291">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="cb04f-292">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-292">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="cb04f-293">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="cb04f-293">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="cb04f-294">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-294">Limited support for dmesg.</span></span> <span data-ttu-id="cb04f-295">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="cb04f-295">Applications can now log to dmesg.</span></span> <span data-ttu-id="cb04f-296">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="cb04f-296">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="cb04f-297">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-297">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="cb04f-298">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="cb04f-298">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="cb04f-299">尚不支持 `syslog` syscall 接口。</span><span class="sxs-lookup"><span data-stu-id="cb04f-299">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="cb04f-300">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-300">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="cb04f-301">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="cb04f-301">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="cb04f-302">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="cb04f-302">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="cb04f-303">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="cb04f-303">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="cb04f-304">不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="cb04f-304">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="cb04f-305">内部版本 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="cb04f-305">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="cb04f-306">有关内部版本 18252 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-306">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-307">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-307">WSL</span></span>
* <span data-ttu-id="cb04f-308">将 init 和 bsdtar 二进制文件移出 lxssmanager dll，移入单独的 tools 文件夹</span><span class="sxs-lookup"><span data-stu-id="cb04f-308">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="cb04f-309">修复在使用 CLONE_FILES 的情况下，关闭文件描述符时出现的争用</span><span class="sxs-lookup"><span data-stu-id="cb04f-309">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="cb04f-310">处理转换 DrvFs 路径时 /proc/pid/mountinfo 中的可选字段</span><span class="sxs-lookup"><span data-stu-id="cb04f-310">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="cb04f-311">允许 DrvFs mknod 成功，但不为 S_IFREG 提供元数据支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-311">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="cb04f-312">应为 DrvFs 上创建的只读文件设置只读属性 [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="cb04f-312">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="cb04f-313">添加 /sbin/mount.drvfs 帮助器用于处理 DrvFs 装载</span><span class="sxs-lookup"><span data-stu-id="cb04f-313">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="cb04f-314">在 DrvFs 中使用 POSIX rename。</span><span class="sxs-lookup"><span data-stu-id="cb04f-314">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="cb04f-315">允许在无卷 GUID 的卷上执行路径转换。</span><span class="sxs-lookup"><span data-stu-id="cb04f-315">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="cb04f-316">内部版本 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="cb04f-316">Build 17738 (Fast)</span></span>
<span data-ttu-id="cb04f-317">有关内部版本 17738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-317">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-318">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-318">WSL</span></span>
* <span data-ttu-id="cb04f-319">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="cb04f-319">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="cb04f-320">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="cb04f-320">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="cb04f-321">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="cb04f-321">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="cb04f-322">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="cb04f-322">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="cb04f-323">内部版本 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="cb04f-323">Build 17728 (Fast)</span></span>
<span data-ttu-id="cb04f-324">有关内部版本 17728 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-324">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-325">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-325">WSL</span></span>
* <span data-ttu-id="cb04f-326">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="cb04f-326">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="cb04f-327">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="cb04f-327">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="cb04f-328">修复一些 AF_UNIX 相关的问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="cb04f-328">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="cb04f-329">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="cb04f-329">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="cb04f-330">内部版本 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="cb04f-330">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="cb04f-331">有关内部版本 18204 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-331">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-332">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-332">WSL</span></span>
* <span data-ttu-id="cb04f-333">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="cb04f-333">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="cb04f-334">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="cb04f-334">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="cb04f-335">内部版本 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="cb04f-335">Build 17723 (Fast)</span></span>
<span data-ttu-id="cb04f-336">有关内部版本 17723 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-336">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-337">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-337">WSL</span></span>
* <span data-ttu-id="cb04f-338">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="cb04f-338">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="cb04f-339">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="cb04f-339">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="cb04f-340">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-340">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="cb04f-341">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="cb04f-341">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="cb04f-342">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="cb04f-342">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="cb04f-343">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="cb04f-343">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="cb04f-344">内部版本 17713</span><span class="sxs-lookup"><span data-stu-id="cb04f-344">Build 17713</span></span>
<span data-ttu-id="cb04f-345">有关内部版本 17713 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-345">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-346">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-346">WSL</span></span>
* <span data-ttu-id="cb04f-347">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="cb04f-347">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="cb04f-348">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="cb04f-348">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="cb04f-349">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="cb04f-349">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="cb04f-350">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="cb04f-350">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="cb04f-351">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="cb04f-351">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="cb04f-352">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="cb04f-352">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="cb04f-353">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="cb04f-353">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="cb04f-354">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-354">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="cb04f-355">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="cb04f-355">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="cb04f-356">内部版本 17704</span><span class="sxs-lookup"><span data-stu-id="cb04f-356">Build 17704</span></span>
<span data-ttu-id="cb04f-357">有关内部版本 17704 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-357">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-358">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-358">WSL</span></span>
* <span data-ttu-id="cb04f-359">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="cb04f-359">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="cb04f-360">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="cb04f-360">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="cb04f-361">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="cb04f-361">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="cb04f-362">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="cb04f-362">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="cb04f-363">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="cb04f-363">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="cb04f-364">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-364">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="cb04f-365">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="cb04f-365">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="cb04f-366">版本 17692</span><span class="sxs-lookup"><span data-stu-id="cb04f-366">Build 17692</span></span>
<span data-ttu-id="cb04f-367">有关内部版本 17692 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-367">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-368">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-368">WSL</span></span>
* <span data-ttu-id="cb04f-369">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-369">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="cb04f-370">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="cb04f-370">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="cb04f-371">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="cb04f-371">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="cb04f-372">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-372">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="cb04f-373">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="cb04f-373">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="cb04f-374">版本 17686</span><span class="sxs-lookup"><span data-stu-id="cb04f-374">Build 17686</span></span>
<span data-ttu-id="cb04f-375">有关内部版本 17686 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-375">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-376">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-376">WSL</span></span>
* <span data-ttu-id="cb04f-377">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="cb04f-377">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="cb04f-378">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="cb04f-378">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="cb04f-379">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="cb04f-379">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="cb04f-380">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="cb04f-380">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="cb04f-381">内部版本 17677</span><span class="sxs-lookup"><span data-stu-id="cb04f-381">Build 17677</span></span>
<span data-ttu-id="cb04f-382">有关内部版本 17677 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-382">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-383">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-383">WSL</span></span>
* <span data-ttu-id="cb04f-384">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="cb04f-384">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="cb04f-385">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="cb04f-385">[GH 2712]</span></span>
* <span data-ttu-id="cb04f-386">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-386">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="cb04f-387">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="cb04f-387">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="cb04f-388">内部版本 17666</span><span class="sxs-lookup"><span data-stu-id="cb04f-388">Build 17666</span></span>
<span data-ttu-id="cb04f-389">有关内部版本 17666 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-389">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-390">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-390">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="cb04f-391">警告：某个问题会阻止 WSL 在某些 AMD 芯片组上运行 [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-391">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="cb04f-392">修复程序已准备就绪，即将在 Insider Build 分支中发布。</span><span class="sxs-lookup"><span data-stu-id="cb04f-392">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="cb04f-393">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-393">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="cb04f-394">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="cb04f-394">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="cb04f-395">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="cb04f-395">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="cb04f-396">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-396">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="cb04f-397">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-397">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="cb04f-398">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-398">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="cb04f-399">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-399">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="cb04f-400">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="cb04f-400">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="cb04f-401">内部版本 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="cb04f-401">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="cb04f-402">有关内部版本 17655 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-402">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-403">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-403">WSL</span></span>
* <span data-ttu-id="cb04f-404">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-404">Limited support for dmesg.</span></span> <span data-ttu-id="cb04f-405">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="cb04f-405">Applications can now log to dmesg.</span></span> <span data-ttu-id="cb04f-406">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="cb04f-406">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="cb04f-407">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-407">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="cb04f-408">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="cb04f-408">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="cb04f-409">尚不支持 `syslog` sycall 接口。</span><span class="sxs-lookup"><span data-stu-id="cb04f-409">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="cb04f-410">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-410">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="cb04f-411">修复了即使文件存在，多线程操作也可能返回 ENOENT 的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-411">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="cb04f-412">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="cb04f-412">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="cb04f-413">内部版本 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="cb04f-413">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="cb04f-414">有关内部版本 17639 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-414">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-415">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-415">WSL</span></span>
* <span data-ttu-id="cb04f-416">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="cb04f-416">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="cb04f-417">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="cb04f-417">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="cb04f-418">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="cb04f-418">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="cb04f-419">具体而言，不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="cb04f-419">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="cb04f-420">内部版本 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="cb04f-420">Build 17133 (Fast)</span></span>
<span data-ttu-id="cb04f-421">有关内部版本 17133 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-421">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-422">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-422">WSL</span></span>
* <span data-ttu-id="cb04f-423">修复 WSL 中的挂起问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-423">Fix for hang in WSL.</span></span> <span data-ttu-id="cb04f-424">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="cb04f-424">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="cb04f-425">内部版本 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="cb04f-425">Build 17128 (Fast)</span></span>
<span data-ttu-id="cb04f-426">有关内部版本 17128 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-426">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-427">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-427">WSL</span></span>
* <span data-ttu-id="cb04f-428">无</span><span class="sxs-lookup"><span data-stu-id="cb04f-428">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="cb04f-429">内部版本 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="cb04f-429">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="cb04f-430">有关内部版本 17627 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-430">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-431">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-431">WSL</span></span>
* <span data-ttu-id="cb04f-432">添加对 futex pi 感知操作的支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-432">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="cb04f-433">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="cb04f-433">[GH 1006]</span></span>
    * <span data-ttu-id="cb04f-434">请注意，WSL 功能目前不支持优先级，因此存在一些限制，但标准用法应该不会受到阻止。</span><span class="sxs-lookup"><span data-stu-id="cb04f-434">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="cb04f-435">对 WSL 进程的 Windows 防火墙支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-435">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="cb04f-436">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="cb04f-436">[GH 1852]</span></span>
    * <span data-ttu-id="cb04f-437">例如，若要允许 WSL python 进程侦听任何端口，请使用提升的 Windows cmd：```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="cb04f-437">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="cb04f-438">有关如何添加防火墙规则的更多详细信息，请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="cb04f-438">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="cb04f-439">使用 wsl.exe 时遵循用户的默认 shell。</span><span class="sxs-lookup"><span data-stu-id="cb04f-439">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="cb04f-440">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="cb04f-440">[GH 2372]</span></span>
* <span data-ttu-id="cb04f-441">将所有网络接口报告为以太网。</span><span class="sxs-lookup"><span data-stu-id="cb04f-441">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="cb04f-442">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="cb04f-442">[GH 2996]</span></span>
* <span data-ttu-id="cb04f-443">更好地处理损坏的 /etc/passwd 文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-443">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="cb04f-444">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="cb04f-444">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-445">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-445">Console</span></span>
* <span data-ttu-id="cb04f-446">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-446">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-447">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-447">LTP Results:</span></span>
<span data-ttu-id="cb04f-448">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-448">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="cb04f-449">内部版本 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="cb04f-449">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="cb04f-450">有关内部版本 17618 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-450">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-451">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-451">WSL</span></span>
* <span data-ttu-id="cb04f-452">引入用于 NT interop 的伪控制台功能 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-452">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="cb04f-453">传统的安装机制 (lxrun.exe) 已弃用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-453">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="cb04f-454">支持用于安装分发版的机制是 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="cb04f-454">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-455">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-455">Console</span></span>
* <span data-ttu-id="cb04f-456">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-456">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-457">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-457">LTP Results:</span></span>
<span data-ttu-id="cb04f-458">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-458">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="cb04f-459">版本 17110</span><span class="sxs-lookup"><span data-stu-id="cb04f-459">Build 17110</span></span>
<span data-ttu-id="cb04f-460">有关内部版本 17110 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-460">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-461">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-461">WSL</span></span>
* <span data-ttu-id="cb04f-462">允许从 Windows 终止 /init [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-462">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="cb04f-463">现在，DrvFs 默认使用按目录区分大小写（相当于使用“case=dir”装载选项）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-463">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="cb04f-464">使用“case=dir”（旧行为）需要设置注册表项。</span><span class="sxs-lookup"><span data-stu-id="cb04f-464">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="cb04f-465">如果需要使用“case=dir”，请运行以下命令来启用它：reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="cb04f-465">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="cb04f-466">如果在旧版 Windows 中使用 WSL 创建的现有目录需要区分大小写，请使用 fsutil.exe 将其标记为区分大小写：fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="cb04f-466">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="cb04f-467">NULL 终止从 uname syscall 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="cb04f-467">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-468">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-468">Console</span></span>
* <span data-ttu-id="cb04f-469">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-469">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-470">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-470">LTP Results:</span></span>
<span data-ttu-id="cb04f-471">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-471">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="cb04f-472">内部版本 17107</span><span class="sxs-lookup"><span data-stu-id="cb04f-472">Build 17107</span></span>
<span data-ttu-id="cb04f-473">有关内部版本 17107 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-473">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-474">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-474">WSL</span></span>
* <span data-ttu-id="cb04f-475">支持主 pty 终结点上的 TCSETSF 和 TCSETSW [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-475">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="cb04f-476">启动同步 interop 进程可能会导致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-476">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="cb04f-477">修复 PTRACE_ATTACH 以在 /proc/pid/status 中显示正确的跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="cb04f-477">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="cb04f-478">修复以下争用问题：在不清除 TID 地址的情况下，通过 CLEARTID 和 SETTID 标志克隆的生存期较短的进程可能会退出。</span><span class="sxs-lookup"><span data-stu-id="cb04f-478">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="cb04f-479">在从 17093 以前的内部版本迁移期间，升级 Linux 文件系统目录时会显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-479">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="cb04f-480">有关 17093 文件系统更改的更多详细信息，请参阅 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) 的发行说明。</span><span class="sxs-lookup"><span data-stu-id="cb04f-480">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-481">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-481">Console</span></span>
* <span data-ttu-id="cb04f-482">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-482">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-483">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-483">LTP Results:</span></span>
<span data-ttu-id="cb04f-484">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-484">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="cb04f-485">内部版本 17101</span><span class="sxs-lookup"><span data-stu-id="cb04f-485">Build 17101</span></span>
<span data-ttu-id="cb04f-486">有关内部版本 17101 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-486">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-487">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-487">WSL</span></span>
* <span data-ttu-id="cb04f-488">signalfd 支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-488">Support for signalfd.</span></span> <span data-ttu-id="cb04f-489">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="cb04f-489">[GH 129]</span></span>
* <span data-ttu-id="cb04f-490">支持包含非法 NTFS 字符的文件名，现在会将这些字符编码为专用 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="cb04f-490">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="cb04f-491">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="cb04f-491">[GH 1514]</span></span>
* <span data-ttu-id="cb04f-492">不支持写入时，自动装载将回退到只读。</span><span class="sxs-lookup"><span data-stu-id="cb04f-492">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="cb04f-493">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="cb04f-493">[GH 2603]</span></span>
* <span data-ttu-id="cb04f-494">允许粘贴 Unicode 代理项对（类似于表情符号）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-494">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="cb04f-495">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="cb04f-495">[GH 2765]</span></span>
* <span data-ttu-id="cb04f-496">/proc 和/sys 中的伪文件应从 select、poll、epoll 等命令返回 read 和 write ready [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="cb04f-496">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="cb04f-497">修复当注册表被篡改或损坏时，可能导致服务进入无限循环的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-497">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="cb04f-498">修复 netlink 消息，以便能够使用更新版本（上游 4.14）的 iproute2。</span><span class="sxs-lookup"><span data-stu-id="cb04f-498">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-499">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-499">Console</span></span>
* <span data-ttu-id="cb04f-500">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-500">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-501">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-501">LTP Results:</span></span>
<span data-ttu-id="cb04f-502">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-502">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="cb04f-503">内部版本 17093</span><span class="sxs-lookup"><span data-stu-id="cb04f-503">Build 17093</span></span>
<span data-ttu-id="cb04f-504">有关内部版本 17093 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-504">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="cb04f-505">重要提示：</span><span class="sxs-lookup"><span data-stu-id="cb04f-505">Important:</span></span>
<span data-ttu-id="cb04f-506">升级到此内部版本后，首次启动 WSL 时，需要执行一些操作来升级 Linux 文件系统目录。</span><span class="sxs-lookup"><span data-stu-id="cb04f-506">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="cb04f-507">这可能需要几分钟时间，因此 WSL 的启动速度看上去可能很慢。</span><span class="sxs-lookup"><span data-stu-id="cb04f-507">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="cb04f-508">对于从 Store 安装的每个分发版，只需执行此操作一次。</span><span class="sxs-lookup"><span data-stu-id="cb04f-508">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="cb04f-509">改善了 DrvFs 中的区分大小写支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-509">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="cb04f-510">DrvFs 现在支持按目录区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-510">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="cb04f-511">这是一个可对目录设置的新标志，用于指示应将这些目录中的所有操作视为区分大小写，使得 Windows 应用程序能够正确打开按大小写区分的文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-511">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="cb04f-512">DrvFs 提供新的装载选项用于按目录控制区分大小写状态</span><span class="sxs-lookup"><span data-stu-id="cb04f-512">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="cb04f-513">case=force：将所有目录视为区分大小写（驱动器根目录除外）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-513">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="cb04f-514">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-514">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="cb04f-515">这也是一种传统行为，不过，它会将新目录标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-515">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="cb04f-516">case=dir：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-516">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="cb04f-517">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-517">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="cb04f-518">case=off：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-518">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="cb04f-519">使用 WSL 创建的新目录将标记为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-519">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="cb04f-520">注意：不会对旧版本中的 WSL 创建的目录设置此标志，因此，如果使用“case=dir”选项，则不会将这些目录视为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-520">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="cb04f-521">即将推出一种对现有目录设置此标志的方法。</span><span class="sxs-lookup"><span data-stu-id="cb04f-521">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="cb04f-522">使用这些选项进行装载的示例（对于现有的驱动器，必须先卸载，然后才能使用不同选项装载）：sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="cb04f-522">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="cb04f-523">目前，case=force 仍是默认选项。</span><span class="sxs-lookup"><span data-stu-id="cb04f-523">For now, case=force is still the default option.</span></span> <span data-ttu-id="cb04f-524">以后将更改为 case=dir。</span><span class="sxs-lookup"><span data-stu-id="cb04f-524">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="cb04f-525">现在，在装载 DrvFs 时，可以在 Windows 路径中使用正斜杠，例如：sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="cb04f-525">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="cb04f-526">WSL 现在会在实例启动期间处理 /etc/fstab 文件 [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-526">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="cb04f-527">这种处理是在自动装载 DrvFs 驱动器之前完成的；fstab 已装载的任何驱动器不会自动重新装载，使你可以更改特定驱动器的装入点。</span><span class="sxs-lookup"><span data-stu-id="cb04f-527">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="cb04f-528">可以使用 wsl.conf 禁用此行为。</span><span class="sxs-lookup"><span data-stu-id="cb04f-528">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="cb04f-529">/proc 中的 mount、mountinfo 和 mountstats 文件会正确转义反斜杠和空格等特殊字符 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="cb04f-529">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="cb04f-530">在启用元数据的情况下使用 DrvFs 创建的特殊文件（例如 WSL 符号链接，或 fifos 和 sockets）现在可以从 Windows 复制和移动。</span><span class="sxs-lookup"><span data-stu-id="cb04f-530">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="cb04f-531">可以使用 wsl.conf 更方便地配置 WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-531">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="cb04f-532">我们添加了一个方法，用于自动配置 WSL 中每次启动子系统时要应用的某些功能。</span><span class="sxs-lookup"><span data-stu-id="cb04f-532">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="cb04f-533">这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="cb04f-533">This includes automount options and network configuration.</span></span> <span data-ttu-id="cb04f-534">有关详细信息，请参阅博客文章： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="cb04f-534">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="cb04f-535">AF_UNIX 允许在 WSL 上的 Linux 进程与 Windows 本机进程之间建立套接字连接</span><span class="sxs-lookup"><span data-stu-id="cb04f-535">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="cb04f-536">现在，WSL 和 Windows 应用程序可以通过 Unix 套接字相互通信。</span><span class="sxs-lookup"><span data-stu-id="cb04f-536">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="cb04f-537">假设你要在 Windows 中运行某个服务，并使其可在 Windows 和 WSL 应用中使用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-537">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="cb04f-538">现在可以通过 Unix 套接字实现此目的。</span><span class="sxs-lookup"><span data-stu-id="cb04f-538">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="cb04f-539">有关详细信息，请参阅博客文章： https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="cb04f-539">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-540">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-540">WSL</span></span>
* <span data-ttu-id="cb04f-541">支持使用 MAP_NORESERVE 的 mmap() [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="cb04f-541">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="cb04f-542">支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="cb04f-542">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="cb04f-543">处理克隆中的非 SIGCHLD 终止信号 [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="cb04f-543">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="cb04f-544">存根 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="cb04f-544">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="cb04f-545">加载包含偏移量非零的负载标头的 ELF 二进制文件时出错 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="cb04f-545">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="cb04f-546">加载映像时将尾随页字节归零。</span><span class="sxs-lookup"><span data-stu-id="cb04f-546">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="cb04f-547">减少 execve 以静默方式终止进程的情况</span><span class="sxs-lookup"><span data-stu-id="cb04f-547">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-548">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-548">Console</span></span>
* <span data-ttu-id="cb04f-549">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-549">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-550">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-550">LTP Results:</span></span>
<span data-ttu-id="cb04f-551">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-551">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="cb04f-552">版本 17083</span><span class="sxs-lookup"><span data-stu-id="cb04f-552">Build 17083</span></span>
<span data-ttu-id="cb04f-553">有关内部版本 17083 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-553">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-554">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-554">WSL</span></span>
* <span data-ttu-id="cb04f-555">修复了与 epoll 相关的 bug 检查 [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="cb04f-555">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="cb04f-556">修复了关闭 ASLR 时挂起的问题 [GH 1185、2870]</span><span class="sxs-lookup"><span data-stu-id="cb04f-556">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="cb04f-557">确保 mmap 操作显示原子性 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="cb04f-557">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-558">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-558">Console</span></span>
* <span data-ttu-id="cb04f-559">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-559">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-560">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-560">LTP Results:</span></span>
<span data-ttu-id="cb04f-561">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-561">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="cb04f-562">内部版本 17074</span><span class="sxs-lookup"><span data-stu-id="cb04f-562">Build 17074</span></span>
<span data-ttu-id="cb04f-563">有关内部版本 17074 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-563">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-564">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-564">WSL</span></span>
* <span data-ttu-id="cb04f-565">固定了 DrvFs 元数据的存储格式 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="cb04f-565">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="cb04f-566">**重要说明：** 在此内部版本之前创建的 DrvFs 元数据将不正确地显示或根本不显示。</span><span class="sxs-lookup"><span data-stu-id="cb04f-566">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="cb04f-567">若要修复受影响的文件，请使用 chmod 和 chown 重新应用元数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-567">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="cb04f-568">修复了多个信号和可重启 syscall 的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-568">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-569">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-569">Console</span></span>
* <span data-ttu-id="cb04f-570">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-570">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-571">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-571">LTP Results:</span></span>
<span data-ttu-id="cb04f-572">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-572">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="cb04f-573">内部版本 17063</span><span class="sxs-lookup"><span data-stu-id="cb04f-573">Build 17063</span></span>
<span data-ttu-id="cb04f-574">有关内部版本 17063 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-574">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="cb04f-575">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-575">WSL</span></span>
* <span data-ttu-id="cb04f-576">DrvFs 支持其他 Linux 元数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-576">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="cb04f-577">这样，就可以使用 chmod/chown 设置文件的所有者和模式，并可以创建特殊文件，例如 fifos、Unix 套接字和设备文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-577">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="cb04f-578">默认情况下，此功能暂时处于禁用状态，因为它仍是试验性的。</span><span class="sxs-lookup"><span data-stu-id="cb04f-578">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="cb04f-579">**注意：** 修复了 DrvFs 使用的元数据格式的 bug。</span><span class="sxs-lookup"><span data-stu-id="cb04f-579">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="cb04f-580">尽管试验性的元数据可在此内部版本中正常工作，但将来的内部版本无法正确读取此内部版本创建的元数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-580">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="cb04f-581">你可能需要手动更新已修改的文件的所有者，并且必须重新创建使用自定义设备 ID 的设备。</span><span class="sxs-lookup"><span data-stu-id="cb04f-581">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="cb04f-582">若要启用元数据，请使用 metadata 选项装载 DrvFs（若要在现有装入点上启用，必须先将其卸载）：</span><span class="sxs-lookup"><span data-stu-id="cb04f-582">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="cb04f-583">Linux 权限将作为附加元数据添加到文件；它们不会影响 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="cb04f-583">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="cb04f-584">请记住，使用 Windows 编辑器编辑文件可能会删除元数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-584">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="cb04f-585">在这种情况下，文件将还原为默认权限。</span><span class="sxs-lookup"><span data-stu-id="cb04f-585">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="cb04f-586">已将 mount 选项添加到 DrvFs，用于控制不包含元数据的文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-586">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="cb04f-587">uid：所有文件的所有者使用的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="cb04f-587">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="cb04f-588">gid：所有文件的所有者使用的组 ID。</span><span class="sxs-lookup"><span data-stu-id="cb04f-588">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="cb04f-589">umask：要对所有文件和目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="cb04f-589">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="cb04f-590">fmask：要对所有常规文件排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="cb04f-590">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="cb04f-591">dmask：要对所有目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="cb04f-591">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="cb04f-592">例如：</span><span class="sxs-lookup"><span data-stu-id="cb04f-592">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="cb04f-593">与 metadata 选项相结合可以指定不包含元数据的文件的默认权限。</span><span class="sxs-lookup"><span data-stu-id="cb04f-593">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="cb04f-594">引入了新的环境变量 `WSLENV`，用于配置环境变量在 WSL 与 Win32 之间的流动方式。</span><span class="sxs-lookup"><span data-stu-id="cb04f-594">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="cb04f-595">例如：</span><span class="sxs-lookup"><span data-stu-id="cb04f-595">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="cb04f-596">`WSLENV` 是在从 Win32 启动 WSL 进程或者从 WSL 启动 Win32 进程时可以包含的环境变量的冒号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-596">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="cb04f-597">每个变量可以使用斜杠后接一个用于指定其转换方式的标志作为后缀。</span><span class="sxs-lookup"><span data-stu-id="cb04f-597">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="cb04f-598">p：值是应在 WSL 路径与 Win32 路径之间进行转换的路径。</span><span class="sxs-lookup"><span data-stu-id="cb04f-598">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="cb04f-599">l：值是路径列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-599">l: The value is a list of paths.</span></span> <span data-ttu-id="cb04f-600">在 WSL 中，它是冒号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-600">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="cb04f-601">在 Win32 中，它是分号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-601">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="cb04f-602">u：仅当从 Win32 调用 WSL 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="cb04f-602">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="cb04f-603">w：仅当从 WSL 调用 Win32 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="cb04f-603">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="cb04f-604">可以在 .bashrc 中或者在用户的自定义 Windows 环境中设置 `WSLENV`。</span><span class="sxs-lookup"><span data-stu-id="cb04f-604">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="cb04f-605">drvfs 装入点会正确保留 tar、cp -p 中的时间戳 (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="cb04f-605">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="cb04f-606">drvfs 符号链接会报告正确的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="cb04f-606">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="cb04f-607">read/write 适用于极大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="cb04f-607">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="cb04f-608">waitpid 适用于进程组 ID (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="cb04f-608">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="cb04f-609">极大改善了大型保留区域的 mmap 性能；改善了 ghc 性能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="cb04f-609">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="cb04f-610">READ_IMPLIES_EXEC 的个性化支持；修复 maxima 和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="cb04f-610">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="cb04f-611">mprotect 支持 PROT_GROWSDOWN；修复 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="cb04f-611">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="cb04f-612">overcommit 模式的页面错误修复；修复 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="cb04f-612">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="cb04f-613">clone 支持更多标志组合</span><span class="sxs-lookup"><span data-stu-id="cb04f-613">clone supports more flags combinations</span></span>
* <span data-ttu-id="cb04f-614">支持 epoll 文件的 select/epoll（以前为 no-op）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-614">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="cb04f-615">通知未实现的 syscall 的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="cb04f-615">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="cb04f-616">忽略生成 resolv.conf 名称服务器时不启动的接口 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="cb04f-616">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="cb04f-617">枚举没有物理地址的网络接口。</span><span class="sxs-lookup"><span data-stu-id="cb04f-617">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="cb04f-618">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="cb04f-618">[GH 2685]</span></span>
* <span data-ttu-id="cb04f-619">其他 bug 修复和改进。</span><span class="sxs-lookup"><span data-stu-id="cb04f-619">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="cb04f-620">适用于 Windows 上的开发人员的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="cb04f-620">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="cb04f-621">Windows 命令行工具链包括 bsdtar (tar) 和 curl。</span><span class="sxs-lookup"><span data-stu-id="cb04f-621">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="cb04f-622">请阅读[此博客](https://aka.ms/tarcurlwindows)来详细了解如何添加这两个新工具，以及它们如何打造 Windows 上的开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="cb04f-622">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="cb04f-623">`AF_UNIX` 适用于 Windows 预览体验成员 SDK (17061+)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-623">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="cb04f-624">请阅读[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)来详细了解 `AF_UNIX`，以及 Windows 上的开发人员如何使用它。</span><span class="sxs-lookup"><span data-stu-id="cb04f-624">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="cb04f-625">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-625">Console</span></span>
* <span data-ttu-id="cb04f-626">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-626">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-627">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-627">LTP Results:</span></span>
<span data-ttu-id="cb04f-628">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-628">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="cb04f-629">内部版本 17046</span><span class="sxs-lookup"><span data-stu-id="cb04f-629">Build 17046</span></span>

<span data-ttu-id="cb04f-630">有关内部版本 17046 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-630">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="cb04f-631">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-631">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-632">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-632">WSL</span></span>
- <span data-ttu-id="cb04f-633">允许进程在没有活动终端的情况下运行。</span><span class="sxs-lookup"><span data-stu-id="cb04f-633">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="cb04f-634">[GH 709、1007、1511、2252、2391 等]</span><span class="sxs-lookup"><span data-stu-id="cb04f-634">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="cb04f-635">更好地支持 CLONE_VFORK 和 CLONE_VM。</span><span class="sxs-lookup"><span data-stu-id="cb04f-635">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="cb04f-636">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="cb04f-636">[GH 1878, 2615]</span></span>
- <span data-ttu-id="cb04f-637">跳过 WSL 网络操作的 TDI 筛选器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="cb04f-637">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="cb04f-638">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="cb04f-638">[GH 1554]</span></span>
- <span data-ttu-id="cb04f-639">在满足特定的条件时，DrvFs 将创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="cb04f-639">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="cb04f-640">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="cb04f-640">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="cb04f-641">链接目标必须是相对性的，不能跨任何装入点或符号链接，并且必须存在。</span><span class="sxs-lookup"><span data-stu-id="cb04f-641">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="cb04f-642">除非已启用开发人员模式，否则用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE（这通常需要以提升的权限启动 wsl.exe）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-642">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="cb04f-643">在所有其他情况下，DrvFs 仍会创建 WSL 符号链接。</span><span class="sxs-lookup"><span data-stu-id="cb04f-643">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="cb04f-644">允许同时运行提升和未提升的 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="cb04f-644">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="cb04f-645">支持 /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="cb04f-645">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="cb04f-646">添加 wslpath 用于执行 WSL<->Windows 路径转换。</span><span class="sxs-lookup"><span data-stu-id="cb04f-646">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="cb04f-647">[GH 522、1243、1834、2327 等]</span><span class="sxs-lookup"><span data-stu-id="cb04f-647">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="cb04f-648">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-648">Console</span></span>
- <span data-ttu-id="cb04f-649">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-649">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-650">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-650">LTP Results:</span></span>
<span data-ttu-id="cb04f-651">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-651">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="cb04f-652">内部版本 17040</span><span class="sxs-lookup"><span data-stu-id="cb04f-652">Build 17040</span></span>

<span data-ttu-id="cb04f-653">有关内部版本 17040 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-653">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-654">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-654">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-655">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-655">WSL</span></span>
- <span data-ttu-id="cb04f-656">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-656">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-657">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-657">Console</span></span>
- <span data-ttu-id="cb04f-658">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-658">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-659">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-659">LTP Results:</span></span>
<span data-ttu-id="cb04f-660">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-660">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="cb04f-661">内部版本 17035</span><span class="sxs-lookup"><span data-stu-id="cb04f-661">Build 17035</span></span>

<span data-ttu-id="cb04f-662">有关内部版本 17035 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-662">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-663">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-663">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-664">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-664">WSL</span></span>
- <span data-ttu-id="cb04f-665">访问 DrvFs 上的文件偶尔会失败并出现 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="cb04f-665">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="cb04f-666">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="cb04f-666">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-667">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-667">Console</span></span>
- <span data-ttu-id="cb04f-668">在 VT 模式下插入/删除行时丢失一些颜色。</span><span class="sxs-lookup"><span data-stu-id="cb04f-668">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-669">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-669">LTP Results:</span></span>
<span data-ttu-id="cb04f-670">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-670">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="cb04f-671">内部版本 17025</span><span class="sxs-lookup"><span data-stu-id="cb04f-671">Build 17025</span></span>

<span data-ttu-id="cb04f-672">有关内部版本 17025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-672">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-673">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-673">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-674">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-674">WSL</span></span>
- <span data-ttu-id="cb04f-675">在新的前台进程组中启动初始进程 [GH 1653、2510]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-675">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="cb04f-676">SIGHUP 传递修复 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-676">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="cb04f-677">如果未提供虚拟网桥名称，将生成默认名称 [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-677">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="cb04f-678">实现 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-678">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="cb04f-679">更多 interop stdout/stderr 管道修复措施。</span><span class="sxs-lookup"><span data-stu-id="cb04f-679">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="cb04f-680">存根 syncfs 系统调用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-680">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-681">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-681">Console</span></span>
- <span data-ttu-id="cb04f-682">修复第三方控制台的输入 VT 转换 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="cb04f-682">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-683">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-683">LTP Results:</span></span>
<span data-ttu-id="cb04f-684">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-684">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="cb04f-685">内部版本 17017</span><span class="sxs-lookup"><span data-stu-id="cb04f-685">Build 17017</span></span>

<span data-ttu-id="cb04f-686">有关内部版本 17017 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-686">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-687">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-687">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-688">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-688">WSL</span></span>
- <span data-ttu-id="cb04f-689">忽略空的 ELF 程序标头 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-689">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="cb04f-690">允许 LxssManager 为非交互式用户创建 WSL 实例（ssh 和计划任务支持）[GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-690">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="cb04f-691">支持 WSL->Win32->WSL（“起始”）方案 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-691">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="cb04f-692">有限支持终止通过 interop 调用的控制台应用 [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-692">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="cb04f-693">支持 devpts 的装载选项 [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-693">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="cb04f-694">Ptrace 阻止子级启动 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-694">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="cb04f-695">EPOLLET 缺少某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-695">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="cb04f-696">返回 PTRACE_GETSIGINFO 的更多数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-696">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="cb04f-697">结合 lseek 运行 Getdents 会提供错误的结果。</span><span class="sxs-lookup"><span data-stu-id="cb04f-697">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="cb04f-698">修复某些 Win32 interop 应用挂起，并等待在没有更多数据的管道中提供输入的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-698">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="cb04f-699">tty/pty 文件的 O_ASYNC 支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-699">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="cb04f-700">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-700">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-701">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-701">Console</span></span>
- <span data-ttu-id="cb04f-702">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-702">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-703">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-703">LTP Results:</span></span>
<span data-ttu-id="cb04f-704">正在测试。</span><span class="sxs-lookup"><span data-stu-id="cb04f-704">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="cb04f-705">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="cb04f-705">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="cb04f-706">内部版本 16288</span><span class="sxs-lookup"><span data-stu-id="cb04f-706">Build 16288</span></span>

<span data-ttu-id="cb04f-707">有关内部版本 16288 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-707">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-708">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-709">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-709">WSL</span></span>
- <span data-ttu-id="cb04f-710">正确初始化和报告套接字文件描述符的 uid、gid 和模式 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="cb04f-710">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="cb04f-711">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-712">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-712">Console</span></span>
- <span data-ttu-id="cb04f-713">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-714">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-714">LTP Results:</span></span>
<span data-ttu-id="cb04f-715">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-715">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="cb04f-716">内部版本 16278</span><span class="sxs-lookup"><span data-stu-id="cb04f-716">Build 16278</span></span>

<span data-ttu-id="cb04f-717">有关内部版本 162738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-717">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-718">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-718">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-719">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-719">WSL</span></span>
- <span data-ttu-id="cb04f-720">分解 LX MM 状态时显式取消映射文件后备节的映射视图 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="cb04f-720">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="cb04f-721">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-721">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-722">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-722">Console</span></span>
- <span data-ttu-id="cb04f-723">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-723">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-724">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-724">LTP Results:</span></span>
<span data-ttu-id="cb04f-725">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-725">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="cb04f-726">内部版本 16275</span><span class="sxs-lookup"><span data-stu-id="cb04f-726">Build 16275</span></span>

<span data-ttu-id="cb04f-727">有关内部版本 162735 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-727">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-728">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-728">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-729">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-729">WSL</span></span>
- <span data-ttu-id="cb04f-730">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-730">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-731">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-731">Console</span></span>
- <span data-ttu-id="cb04f-732">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-732">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-733">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-733">LTP Results:</span></span>
<span data-ttu-id="cb04f-734">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-734">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="cb04f-735">内部版本 16273</span><span class="sxs-lookup"><span data-stu-id="cb04f-735">Build 16273</span></span>

<span data-ttu-id="cb04f-736">有关内部版本 16273 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-736">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-737">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-737">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-738">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-738">WSL</span></span>
- <span data-ttu-id="cb04f-739">修复了 DrvFs 有时报告目录的错误文件类型的问题 [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="cb04f-739">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="cb04f-740">允许创建 NETLINK_KOBJECT_UEVENT 套接字来取消阻止使用 UEVENT 的程序 [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="cb04f-740">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="cb04f-741">添加对非阻塞连接的支持 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="cb04f-741">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="cb04f-742">实现 CLONE_FS 克隆系统调用标志 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="cb04f-742">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="cb04f-743">修复有关在 NT interop 中不会正确处理制表符或引号的问题 [GH 1625、2164]</span><span class="sxs-lookup"><span data-stu-id="cb04f-743">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="cb04f-744">解决尝试重新启动 WSL 实例时发生的拒绝访问错误 [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="cb04f-744">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="cb04f-745">实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="cb04f-745">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="cb04f-746">修复各种 SysFs 文件的权限 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="cb04f-746">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="cb04f-747">修复设置过程中 Haskell 堆栈挂起的问题 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="cb04f-747">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="cb04f-748">实现 binfmt_misc“C”、“O”和“P”标志 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="cb04f-748">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="cb04f-749">添加 /proc/sys/kernel /shmmax /shmmni 和 /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="cb04f-749">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="cb04f-750">添加对 ioprio_set 系统调用的部分支持 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="cb04f-750">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="cb04f-751">存根 SO_REUSEPORT 和添加 netlink 套接字的 SO_PASSCRED 支持 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="cb04f-751">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="cb04f-752">如果当前正在安装或卸载分发版，将从 RegisterDistribuiton 返回不同的错误代码。</span><span class="sxs-lookup"><span data-stu-id="cb04f-752">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="cb04f-753">允许通过 wslconfig.exe 取消注册部分安装的 WSL 分发版</span><span class="sxs-lookup"><span data-stu-id="cb04f-753">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="cb04f-754">修复 udp::msg_peek 的 python 套接字测试挂起问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-754">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="cb04f-755">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-755">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-756">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-756">Console</span></span>
- <span data-ttu-id="cb04f-757">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-757">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-758">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-758">LTP Results:</span></span>
<span data-ttu-id="cb04f-759">测试总数：1904</span><span class="sxs-lookup"><span data-stu-id="cb04f-759">Total Tests: 1904</span></span><br/>
<span data-ttu-id="cb04f-760">跳过的测试总数：209</span><span class="sxs-lookup"><span data-stu-id="cb04f-760">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="cb04f-761">失败总数：229</span><span class="sxs-lookup"><span data-stu-id="cb04f-761">Total Failures: 229</span></span><br/>
[<span data-ttu-id="cb04f-762">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-762">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="cb04f-763">版本 16257</span><span class="sxs-lookup"><span data-stu-id="cb04f-763">Build 16257</span></span>

<span data-ttu-id="cb04f-764">有关内部版本 16257 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-764">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-765">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-765">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-766">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-766">WSL</span></span>
- <span data-ttu-id="cb04f-767">实现 prlimit64 系统调用</span><span class="sxs-lookup"><span data-stu-id="cb04f-767">Implement prlimit64 system call</span></span>
- <span data-ttu-id="cb04f-768">添加对 ulimit -n 的支持 (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="cb04f-768">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="cb04f-769">TCP 套接字的存根 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="cb04f-769">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="cb04f-770">修复无效的 AT_EXECFN 辅助矢量行为 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="cb04f-770">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="cb04f-771">修复 console/tty 的 copy/paste 行为，并添加更适当的完整缓冲区处理 [GH 2204、2131]</span><span class="sxs-lookup"><span data-stu-id="cb04f-771">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="cb04f-772">在 set-user-ID 和 set-group-ID 程序的辅助矢量中设置 AT_SECURE [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="cb04f-772">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="cb04f-773">伪终端主终结点不处理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="cb04f-773">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="cb04f-774">修复 lseek 在 LxFs 中的回退目录行为 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="cb04f-774">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="cb04f-775">重度使用后 /dev/ptmx 锁定 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="cb04f-775">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="cb04f-776">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-776">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-777">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-777">Console</span></span>
- <span data-ttu-id="cb04f-778">修复横线/下划线四处可见的问题 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="cb04f-778">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="cb04f-779">修复进程顺序更改，使 NPM 更难以关闭的问题 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="cb04f-779">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="cb04f-780">添加了新的色彩方案： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="cb04f-780">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-781">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-781">LTP Results:</span></span>
<span data-ttu-id="cb04f-782">自 16251 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-782">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-783">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-783">Syscall Support</span></span>
<span data-ttu-id="cb04f-784">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-784">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-785">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-785">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="cb04f-786">已知问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-786">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="cb04f-787">GitHub 问题 2392：WSL 无法识别 Windows 文件夹 ...</span><span class="sxs-lookup"><span data-stu-id="cb04f-787">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="cb04f-788">在内部版本 16257 中，WSL 在通过 `/mnt/c/...` 枚举 Windows 文件/文件夹时会出现问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-788">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="cb04f-789">此问题已修复，修复程序将在 2017 年 8 月 14 日开始的周内，在预览体验成员内部版本中发布。</span><span class="sxs-lookup"><span data-stu-id="cb04f-789">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="cb04f-790">内部版本 16251</span><span class="sxs-lookup"><span data-stu-id="cb04f-790">Build 16251</span></span>

<span data-ttu-id="cb04f-791">有关内部版本 16251 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-791">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-792">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-792">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-793">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-793">WSL</span></span>
- <span data-ttu-id="cb04f-794">从 WSL 可选组件中删除 beta 标记，有关详细信息，请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-794">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="cb04f-795">在执行时正确初始化 set-user-ID 和 set-group-ID 二进制文件的 saved-set uid 和 gid [GH 962、1415、2072]</span><span class="sxs-lookup"><span data-stu-id="cb04f-795">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="cb04f-796">添加了对 ptrace PTRACE_O_TRACEEXIT 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="cb04f-796">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="cb04f-797">添加了对包含 NT_FPREGSET 的 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="cb04f-797">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="cb04f-798">修复了 ptrace 在忽略信号时停止的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-798">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="cb04f-799">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-799">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-800">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-800">Console</span></span>
- <span data-ttu-id="cb04f-801">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-801">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-802">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-802">LTP Results:</span></span>
<span data-ttu-id="cb04f-803">通过的测试数：768</span><span class="sxs-lookup"><span data-stu-id="cb04f-803">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="cb04f-804">失败的测试数：244</span><span class="sxs-lookup"><span data-stu-id="cb04f-804">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="cb04f-805">跳过的测试数：96</span><span class="sxs-lookup"><span data-stu-id="cb04f-805">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="cb04f-806">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-806">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="cb04f-807">内部版本 16241</span><span class="sxs-lookup"><span data-stu-id="cb04f-807">Build 16241</span></span>

<span data-ttu-id="cb04f-808">有关内部版本 16241 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-808">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-809">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-809">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="cb04f-810">WSL</span><span class="sxs-lookup"><span data-stu-id="cb04f-810">WSL</span></span>
- <span data-ttu-id="cb04f-811">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-811">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="cb04f-812">控制台</span><span class="sxs-lookup"><span data-stu-id="cb04f-812">Console</span></span>
- <span data-ttu-id="cb04f-813">修复输出跨行 DEC 的错误字符的问题，最初报告位于[此处](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="cb04f-813">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="cb04f-814">修复代码页 65001 (utf8) 中不显示输出文本的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-814">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="cb04f-815">更改选择内容时，不会将对某种颜色的 RGB 值所做的更改传输到调色板的其他部分。</span><span class="sxs-lookup"><span data-stu-id="cb04f-815">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="cb04f-816">这在一定程度上使得控制台属性表变得更易于使用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-816">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="cb04f-817">Ctrl+S 似乎不起作用</span><span class="sxs-lookup"><span data-stu-id="cb04f-817">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="cb04f-818">ANSI 转义代码中根本没有 Un-Bold/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="cb04f-818">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="cb04f-819">控制台不正常支持 Vim 色彩主题 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="cb04f-819">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="cb04f-820">无法粘贴特定的字符 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="cb04f-820">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="cb04f-821">当编辑/命令行上有内容时，重复流的调整大小操作以奇怪的方式与 bash 窗口调整大小操作交互 [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="cb04f-821">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="cb04f-822">按 Ctrl-L 不会清屏 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="cb04f-822">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="cb04f-823">在 HDPI 上显示 VT 时的控制台呈现 bug [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="cb04f-823">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="cb04f-824">日文字符出现乱码和 Unicode 字符 U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="cb04f-824">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="cb04f-825">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-825">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="cb04f-826">版本 16237</span><span class="sxs-lookup"><span data-stu-id="cb04f-826">Build 16237</span></span>

<span data-ttu-id="cb04f-827">有关内部版本 16237 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-827">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-828">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-828">Fixed</span></span>
- <span data-ttu-id="cb04f-829">对 lxfs 中不包含 EA 的文件使用默认属性 (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="cb04f-829">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="cb04f-830">添加了对使用扩展属性的分发版的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-830">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="cb04f-831">修复 getdents 和 getdents64 返回的项的填充</span><span class="sxs-lookup"><span data-stu-id="cb04f-831">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="cb04f-832">修复针对 shmctl SHM_STAT 系统调用的权限检查 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="cb04f-832">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="cb04f-833">修复了 tty 的错误初始 epoll 状态 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="cb04f-833">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="cb04f-834">修复 DrvFs readdir 不返回所有项的问题 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="cb04f-834">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="cb04f-835">修复取消链接文件时的 LxFs readdir [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="cb04f-835">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="cb04f-836">允许通过 procfs 重新打开未链接的 drvfs 文件</span><span class="sxs-lookup"><span data-stu-id="cb04f-836">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="cb04f-837">添加了用于禁用 WSL 功能的全局注册表项重写（interop/驱动器装载）</span><span class="sxs-lookup"><span data-stu-id="cb04f-837">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="cb04f-838">修复 DrvFs（和 LxFs）的“统计信息”中的错误块计数 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="cb04f-838">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="cb04f-839">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-839">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="cb04f-840">内部版本 16232</span><span class="sxs-lookup"><span data-stu-id="cb04f-840">Build 16232</span></span>

<span data-ttu-id="cb04f-841">有关内部版本 16232 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-841">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-842">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-842">Fixed</span></span>
- <span data-ttu-id="cb04f-843">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-843">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="cb04f-844">内部版本 16226</span><span class="sxs-lookup"><span data-stu-id="cb04f-844">Build 16226</span></span>

<span data-ttu-id="cb04f-845">有关内部版本 16226 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-845">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-846">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-846">Fixed</span></span>
- <span data-ttu-id="cb04f-847">xattr 相关的 syscall 支持（getxattr、setxattr、listxattr、removexattr）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-847">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="cb04f-848">security.capablity xattr 支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-848">security.capablity xattr support.</span></span>
- <span data-ttu-id="cb04f-849">改善了与某些文件系统和筛选器（包括非 MS SMB 服务器）的兼容性。</span><span class="sxs-lookup"><span data-stu-id="cb04f-849">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="cb04f-850">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="cb04f-850">[GH #1952]</span></span>
- <span data-ttu-id="cb04f-851">改善了对 OneDrive 占位符、GVFS 占位符和精简 OS 压缩文件的支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-851">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="cb04f-852">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-852">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="cb04f-853">内部版本 16215</span><span class="sxs-lookup"><span data-stu-id="cb04f-853">Build 16215</span></span>

<span data-ttu-id="cb04f-854">有关内部版本 16215 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-854">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-855">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-855">Fixed</span></span>
- <span data-ttu-id="cb04f-856">WSL 不再需要开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="cb04f-856">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="cb04f-857">支持 drvfs 中的目录接合。</span><span class="sxs-lookup"><span data-stu-id="cb04f-857">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="cb04f-858">处理 WSL appx 分发包的卸载。</span><span class="sxs-lookup"><span data-stu-id="cb04f-858">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="cb04f-859">更新 procfs 以显示专用映射和共享映射。</span><span class="sxs-lookup"><span data-stu-id="cb04f-859">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="cb04f-860">为 wslconfig.exe 添加清理部分安装或已卸载的分发版的功能。</span><span class="sxs-lookup"><span data-stu-id="cb04f-860">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="cb04f-861">添加了对 TCP 套接字的 IP_MTU_DISCOVER 的支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-861">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="cb04f-862">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="cb04f-862">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="cb04f-863">推断 AF_INADDR 路由的协议系列。</span><span class="sxs-lookup"><span data-stu-id="cb04f-863">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="cb04f-864">串行设备改进 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="cb04f-864">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="cb04f-865">内部版本 16199</span><span class="sxs-lookup"><span data-stu-id="cb04f-865">Build 16199</span></span>

<span data-ttu-id="cb04f-866">有关内部版本 16199 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-866">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-867">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-867">Fixed</span></span>
- <span data-ttu-id="cb04f-868">这些版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-868">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="cb04f-869">内部版本 16193</span><span class="sxs-lookup"><span data-stu-id="cb04f-869">Build 16193</span></span>

<span data-ttu-id="cb04f-870">有关内部版本 16193 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-870">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-871">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-871">Fixed</span></span>
- <span data-ttu-id="cb04f-872">发送 SIGCONT 与终止线程组之间的争用状态 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="cb04f-872">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="cb04f-873">更改 tty 和 pty 设备以报告 FILE_DEVICE_NAMED_PIPE 而不是 FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="cb04f-873">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="cb04f-874">IP_OPTIONS 的 SSH 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-874">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="cb04f-875">已将 DrvFs 装载移到初始化守护程序 [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="cb04f-875">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="cb04f-876">在 DrvFs 中添加了遵循 NT 符号链接的支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-876">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="cb04f-877">内部版本 16184</span><span class="sxs-lookup"><span data-stu-id="cb04f-877">Build 16184</span></span>

<span data-ttu-id="cb04f-878">有关内部版本 16184 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-878">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-879">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-879">Fixed</span></span>
- <span data-ttu-id="cb04f-880">删除了 apt 包维护任务 (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="cb04f-880">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="cb04f-881">修复了 node.js 中的 Windows 进程不显示输出的问题 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="cb04f-881">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="cb04f-882">放宽 lxcore 中的对齐要求 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="cb04f-882">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="cb04f-883">修复了许多系统调用中处理 AT_EMPTY_PATH 标志的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-883">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="cb04f-884">修复了删除存在已打开句柄的 DrvFs 文件时，导致文件出现未定义的行为的问题 [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="cb04f-884">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="cb04f-885">/etc/hosts 现在会从 Windows hosts 文件 (%windir%\system32\drivers\etc\hosts) 继承项 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="cb04f-885">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="cb04f-886">内部版本 16179</span><span class="sxs-lookup"><span data-stu-id="cb04f-886">Build 16179</span></span>

<span data-ttu-id="cb04f-887">有关内部版本 16179 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-887">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-888">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-888">Fixed</span></span>
- <span data-ttu-id="cb04f-889">本周没有 WSL 更改。</span><span class="sxs-lookup"><span data-stu-id="cb04f-889">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="cb04f-890">内部版本 16176</span><span class="sxs-lookup"><span data-stu-id="cb04f-890">Build 16176</span></span>

<span data-ttu-id="cb04f-891">有关内部版本 16176 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-891">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-892">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-892">Fixed</span></span>

- [<span data-ttu-id="cb04f-893">已启用串行支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-893">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="cb04f-894">添加了 IP 套接字选项 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="cb04f-894">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="cb04f-895">实现了 pwritev 函数（将文件上传到 nginx/PHP-FPM 时）[GH 1506]</span><span class="sxs-lookup"><span data-stu-id="cb04f-895">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="cb04f-896">添加了 IP 套接字选项 IP_MULTICAST_IF 和 IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="cb04f-896">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="cb04f-897">支持套接字选项 IP_MULTICAST_LOOP 和 IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="cb04f-897">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="cb04f-898">为应用节点、traceroute、dig、nslookup、主机添加了 IP(V6)_MTU 套接字选项</span><span class="sxs-lookup"><span data-stu-id="cb04f-898">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="cb04f-899">添加了 IP 套接字选项 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="cb04f-899">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="cb04f-900">文件系统改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-900">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="cb04f-901">允许装载 UNC 路径</span><span class="sxs-lookup"><span data-stu-id="cb04f-901">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="cb04f-902">在 drvfs 中启用 CDFS 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-902">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="cb04f-903">正确处理 drvfs 中网络文件系统的权限</span><span class="sxs-lookup"><span data-stu-id="cb04f-903">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="cb04f-904">在 drvfs 中添加远程驱动器的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-904">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="cb04f-905">在 drvfs 中启用 FAT 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-905">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="cb04f-906">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-906">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-907">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="cb04f-907">LTP Results</span></span>
<span data-ttu-id="cb04f-908">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-908">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="cb04f-909">内部版本 16170</span><span class="sxs-lookup"><span data-stu-id="cb04f-909">Build 16170</span></span>

<span data-ttu-id="cb04f-910">有关内部版本 16170 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-910">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="cb04f-911">我们发布的新[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)中介绍了我们在测试 WSL 方面所做的努力。</span><span class="sxs-lookup"><span data-stu-id="cb04f-911">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="cb04f-912">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-912">Fixed</span></span>

- <span data-ttu-id="cb04f-913">支持套接字选项 IP_ADD_MEMBERSHIP 和 IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="cb04f-913">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="cb04f-914">添加对 PTRACE_OLDSETOPTIONS 的支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-914">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="cb04f-915">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="cb04f-915">[GH 1692]</span></span>
- <span data-ttu-id="cb04f-916">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-916">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-917">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="cb04f-917">LTP Results</span></span>
<span data-ttu-id="cb04f-918">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-918">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="cb04f-919">内部版本 15046 到 Windows 10 创意者更新</span><span class="sxs-lookup"><span data-stu-id="cb04f-919">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="cb04f-920">我们未计划在 Windows 10 创意者更新中包含其他 WSL 修复或功能。</span><span class="sxs-lookup"><span data-stu-id="cb04f-920">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="cb04f-921">WSL 的发行说明将在未来几周恢复发布，其中补充了面向下一个 Windows 更新主要版本的信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-921">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="cb04f-922">有关内部版本 15046 和将来的预览体验版的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-922">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="cb04f-923">内部版本 15042</span><span class="sxs-lookup"><span data-stu-id="cb04f-923">Build 15042</span></span>

<span data-ttu-id="cb04f-924">有关内部版本 15042 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-924">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-925">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-925">Fixed</span></span>

- <span data-ttu-id="cb04f-926">修复删除以“...”结尾的路径时出现死锁的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-926">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="cb04f-927">修复了 FIONBIO 在成功时不返回 0 的问题 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="cb04f-927">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="cb04f-928">修复了 inet 数据报套接字的零长度读取问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-928">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="cb04f-929">修复 drvfs inode 查找中的争用状况可能导致死锁的问题 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="cb04f-929">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="cb04f-930">扩展了对 unix 套接字辅助数据的支持；SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="cb04f-930">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="cb04f-931">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-931">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-932">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-932">LTP Results:</span></span>
<span data-ttu-id="cb04f-933">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="cb04f-933">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="cb04f-934">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="cb04f-934">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="cb04f-935">内部版本 15031</span><span class="sxs-lookup"><span data-stu-id="cb04f-935">Build 15031</span></span>

<span data-ttu-id="cb04f-936">有关内部版本 15031 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-936">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-937">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-937">Fixed</span></span>

- <span data-ttu-id="cb04f-938">修复了 time(2) 偶尔行为异常的 bug。</span><span class="sxs-lookup"><span data-stu-id="cb04f-938">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="cb04f-939">修复了 \*SIGPROCMASK syscall 可能损坏信号掩码的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-939">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="cb04f-940">现在会在 WSL 进程创建通知中返回完整的命令行长度。</span><span class="sxs-lookup"><span data-stu-id="cb04f-940">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="cb04f-941">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="cb04f-941">[GH 1632]</span></span>
- <span data-ttu-id="cb04f-942">WSL 现在会针对 GDB 挂起通过 ptrace 报告线程退出。</span><span class="sxs-lookup"><span data-stu-id="cb04f-942">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="cb04f-943">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="cb04f-943">[GH 1196]</span></span>
- <span data-ttu-id="cb04f-944">修复了在收到繁重 tmux IO 后 ptys 挂起的 bug。</span><span class="sxs-lookup"><span data-stu-id="cb04f-944">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="cb04f-945">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="cb04f-945">[GH 1358]</span></span>
- <span data-ttu-id="cb04f-946">修复了许多系统调用中的超时验证（futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create）</span><span class="sxs-lookup"><span data-stu-id="cb04f-946">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="cb04f-947">添加了 eventfd EFD_SEMAPHORE 支持 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="cb04f-947">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="cb04f-948">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-948">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-949">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-949">LTP Results:</span></span>
<span data-ttu-id="cb04f-950">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="cb04f-950">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="cb04f-951">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="cb04f-951">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cb04f-952">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-952">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="cb04f-953">内部版本 15025</span><span class="sxs-lookup"><span data-stu-id="cb04f-953">Build 15025</span></span>

<span data-ttu-id="cb04f-954">有关内部版本 15025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-954">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-955">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-955">Fixed</span></span>

- <span data-ttu-id="cb04f-956">修复破坏 grep 2.27 的 bug [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="cb04f-956">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="cb04f-957">为 eventfd2 syscall 实现了 EFD_SEMAPHORE 标志 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="cb04f-957">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="cb04f-958">实现了 /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="cb04f-958">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="cb04f-959">针对 unix 流套接字的信号驱动 IO 支持 [GH 393、68]</span><span class="sxs-lookup"><span data-stu-id="cb04f-959">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="cb04f-960">支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="cb04f-960">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="cb04f-961">实现 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="cb04f-961">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="cb04f-962">修复了 epoll_wait() 不等待的 bug [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="cb04f-962">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="cb04f-963">实现 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="cb04f-963">Implement /proc/version_signature</span></span>
- <span data-ttu-id="cb04f-964">现在，如果两个文件描述符引用同一管道，则 syscall 会返回失败</span><span class="sxs-lookup"><span data-stu-id="cb04f-964">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="cb04f-965">为 Unix 套接字的 SO_PEERCRED 实现了正确的行为</span><span class="sxs-lookup"><span data-stu-id="cb04f-965">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="cb04f-966">修复了 tkill syscall 处理无效参数的方法</span><span class="sxs-lookup"><span data-stu-id="cb04f-966">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="cb04f-967">做出更改以提高 drvfs 的性能</span><span class="sxs-lookup"><span data-stu-id="cb04f-967">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="cb04f-968">针对 Ruby IO 阻塞的次要修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-968">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="cb04f-969">修复了 recvmsg() 对 inet 套接字的 MSG_DONTWAIT 标志返回 EINVAL 的问题 [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="cb04f-969">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="cb04f-970">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-970">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-971">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-971">LTP Results:</span></span>
<span data-ttu-id="cb04f-972">通过的测试数：732</span><span class="sxs-lookup"><span data-stu-id="cb04f-972">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="cb04f-973">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="cb04f-973">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cb04f-974">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-974">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="cb04f-975">内部版本 15019</span><span class="sxs-lookup"><span data-stu-id="cb04f-975">Build 15019</span></span>

<span data-ttu-id="cb04f-976">有关内部版本 15019 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-976">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-977">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-977">Fixed</span></span>

- <span data-ttu-id="cb04f-978">修复了 htop 等工具在 procfs 中错误报告 CPU 使用率的 bug（GH 823、945、971）</span><span class="sxs-lookup"><span data-stu-id="cb04f-978">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="cb04f-979">对现有的文件结合 O_TRUNC 调用 open() 时，inotify 现在会在 IN_OPEN 的前面生成 IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="cb04f-979">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="cb04f-980">修复 unix 套接字 getsockopt SO_ERROR 以启用 postgress [GH 61、1354]</span><span class="sxs-lookup"><span data-stu-id="cb04f-980">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="cb04f-981">为 GO 语言实现 /proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="cb04f-981">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="cb04f-982">Apt-get package update 后台任务现在会在视图中以隐藏方式运行</span><span class="sxs-lookup"><span data-stu-id="cb04f-982">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="cb04f-983">清除 ipv6 localhost 的范围（Spring-Framework(Java) 失败）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-983">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="cb04f-984">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-984">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-985">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-985">LTP Results:</span></span>
<span data-ttu-id="cb04f-986">通过的测试数：714</span><span class="sxs-lookup"><span data-stu-id="cb04f-986">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="cb04f-987">未通过的测试数（失败、已跳过等）：249</span><span class="sxs-lookup"><span data-stu-id="cb04f-987">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="cb04f-988">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-988">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="cb04f-989">内部版本 15014</span><span class="sxs-lookup"><span data-stu-id="cb04f-989">Build 15014</span></span>

<span data-ttu-id="cb04f-990">有关内部版本 15014 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-990">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-991">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-991">Fixed</span></span>

- <span data-ttu-id="cb04f-992">Ctrl+C 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="cb04f-992">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="cb04f-993">htop 和 ps auxw 现在会显示正确的资源利用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="cb04f-993">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="cb04f-994">NT 异常到信号的基本转换。</span><span class="sxs-lookup"><span data-stu-id="cb04f-994">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="cb04f-995">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="cb04f-995">(GH #513)</span></span>
- <span data-ttu-id="cb04f-996">当空间耗尽时，fallocate 现在会失败并返回 ENOSPC，而不是返回 EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="cb04f-996">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="cb04f-997">添加了 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="cb04f-997">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="cb04f-998">实现了 semop 和 semtimedop 系统调用</span><span class="sxs-lookup"><span data-stu-id="cb04f-998">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="cb04f-999">修复了 IP_RECVTOS 和 IPV6_RECVTCLASS 套接字选项的 nslookup 错误 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="cb04f-999">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="cb04f-1000">支持套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="cb04f-1000">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="cb04f-1001">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1001">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1002">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1002">LTP Results:</span></span>
<span data-ttu-id="cb04f-1003">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="cb04f-1003">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="cb04f-1004">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="cb04f-1004">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cb04f-1005">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1005">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="cb04f-1006">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="cb04f-1006">Syscall Summary</span></span>
<span data-ttu-id="cb04f-1007">Syscall 总数：384</span><span class="sxs-lookup"><span data-stu-id="cb04f-1007">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="cb04f-1008">已实现总数：235</span><span class="sxs-lookup"><span data-stu-id="cb04f-1008">Total Implemented: 235</span></span> </br>
<span data-ttu-id="cb04f-1009">已存根总数：22</span><span class="sxs-lookup"><span data-stu-id="cb04f-1009">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="cb04f-1010">未实现总数：127</span><span class="sxs-lookup"><span data-stu-id="cb04f-1010">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="cb04f-1011">详细分解</span><span class="sxs-lookup"><span data-stu-id="cb04f-1011">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="cb04f-1012">内部版本 15007</span><span class="sxs-lookup"><span data-stu-id="cb04f-1012">Build 15007</span></span>

<span data-ttu-id="cb04f-1013">有关内部版本 15007 的一般 Windows 信息，请访问 [Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1013">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="cb04f-1014">已知问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1014">Known Issue</span></span>

- <span data-ttu-id="cb04f-1015">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1015">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="cb04f-1016">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1016">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="cb04f-1017">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1017">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="cb04f-1018">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1018">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="cb04f-1019">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="cb04f-1019">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="cb04f-1020">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="cb04f-1020">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="cb04f-1021">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1021">Fixed</span></span>

- <span data-ttu-id="cb04f-1022">更正了运行 WSL 会消耗 100% 的 CPU 核心的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1022">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="cb04f-1023">现在支持套接字选项 IP_PKTINFO、IPV6_RECVPKTINFO。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1023">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="cb04f-1024">（GH #851、987）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1024">(GH #851, 987)</span></span>
- <span data-ttu-id="cb04f-1025">在 lxcore 中将网络接口物理地址截断为 16 个字节（GH #1452、1414、1343、468、308）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1025">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="cb04f-1026">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1026">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1027">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1027">LTP Results:</span></span>
<span data-ttu-id="cb04f-1028">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="cb04f-1028">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="cb04f-1029">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="cb04f-1029">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="cb04f-1030">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1030">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="cb04f-1031">内部版本 15002</span><span class="sxs-lookup"><span data-stu-id="cb04f-1031">Build 15002</span></span>

<span data-ttu-id="cb04f-1032">有关内部版本 15002 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1032">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="cb04f-1033">已知问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1033">Known Issue</span></span>

<span data-ttu-id="cb04f-1034">两个已知问题：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1034">Two known issues:</span></span>
- <span data-ttu-id="cb04f-1035">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1035">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="cb04f-1036">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1036">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="cb04f-1037">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1037">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="cb04f-1038">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1038">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="cb04f-1039">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="cb04f-1039">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="cb04f-1040">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="cb04f-1040">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="cb04f-1041">当 WSL 运行时，系统线程将消耗 100% 的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1041">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="cb04f-1042">根本原因已解决并已在内部修复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1042">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="cb04f-1043">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1043">Fixed</span></span>

- <span data-ttu-id="cb04f-1044">现在，必须在同一权限级别创建所有 bash 会话。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1044">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="cb04f-1045">尝试在不同级别启动会话将遭到阻止。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1045">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="cb04f-1046">这意味着，管理员和非管理员控制台不能同时运行。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1046">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="cb04f-1047">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1047">(GH #626)</span></span>
<br/>
- <span data-ttu-id="cb04f-1048">实现了以下 NETLINK_ROUTE 消息（需要 Windows 管理员）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1048">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="cb04f-1049">RTM_NEWADDR（支持 `ip addr add`）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1049">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="cb04f-1050">RTM_NEWROUTE（支持 `ip route add`）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1050">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="cb04f-1051">RTM_DELADDR（支持 `ip addr del`）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1051">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="cb04f-1052">RTM_DELROUTE（支持 `ip route del`）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1052">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="cb04f-1053">用于检查要更新的包的计划任务将不再在按流量计费的连接上运行 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1053">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="cb04f-1054">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1054">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="cb04f-1055">实现了 TCP_KEEPCNT 套接字选项 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1055">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="cb04f-1056">实现了 IP_MTU_DISCOVER INET 套接字选项（GH #720、717、170、69）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1056">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="cb04f-1057">删除了旧功能，以通过 NT 路径查找从 init 运行 NT 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1057">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="cb04f-1058">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1058">(GH #1325)</span></span>
- <span data-ttu-id="cb04f-1059">修复 /dev/kmsg 的模式，以允许进行组访问/其他读取访问 (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1059">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="cb04f-1060">实现了 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1060">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="cb04f-1061">更正了进程开始时间显示为 2432 年的错误 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1061">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="cb04f-1062">已将默认 TERM 环境变量切换为 xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1062">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="cb04f-1063">修改了进程分叉期间进程提交的计算方式。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1063">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="cb04f-1064">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1064">(GH #1286)</span></span>
- <span data-ttu-id="cb04f-1065">实现了 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1065">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="cb04f-1066">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1066">(GH #1286)</span></span>
- <span data-ttu-id="cb04f-1067">实现了 /proc/net/route 文件 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1067">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="cb04f-1068">修复了不正确本地化快捷方式名称的错误 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1068">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="cb04f-1069">修复了错误地验证程序标头必须小于（或等于）PATH_MAX 的 elf 分析逻辑。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1069">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="cb04f-1070">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1070">(GH #1048)</span></span>
- <span data-ttu-id="cb04f-1071">为 procfs、sysfs、cgroupfs 和 binfmtfs 实现了 statfs 回调 (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1071">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="cb04f-1072">修复了 AptPackageIndexUpdate 窗口不会关闭的问题（GH #1184，GH #1193 中也有描述）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1072">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="cb04f-1073">添加了 ASLR 个性化 ADDR_NO_RANDOMIZE 支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1073">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="cb04f-1074">（GH #1148、1128）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1074">(GH #1148, 1128)</span></span>
- <span data-ttu-id="cb04f-1075">改善了 PTRACE_GETSIGINFO、SIGSEGV，在 AV 期间会提供正确的 gdb 堆栈跟踪 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1075">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="cb04f-1076">针对 patchelf 二进制文件的 Elf 分析不再失败。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1076">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="cb04f-1077">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1077">(GH #471)</span></span>
- <span data-ttu-id="cb04f-1078">VPN DNS 已传播到 /etc/resolv.conf（GH #416、1350）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1078">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="cb04f-1079">TCP 关闭改进，可以更可靠地传输数据。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1079">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="cb04f-1080">（GH #610、616、1025、1335）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1080">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="cb04f-1081">现在，在打开过多的文件时可返回正确的错误代码 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1081">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="cb04f-1082">（GH #1126、2090）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1082">(GH #1126, 2090)</span></span>
- <span data-ttu-id="cb04f-1083">Windows 审核日志现在会在进程创建审核中报告映像名称。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1083">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="cb04f-1084">现在，在从 bash 窗口内部启动 bash 时会正常失败</span><span class="sxs-lookup"><span data-stu-id="cb04f-1084">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="cb04f-1085">添加了在 interop 无法访问 LxFs 下的工作目录（即 notepad.exe .bashrc）时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="cb04f-1085">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="cb04f-1086">修复了 Windows 路径在 WSL 中截断的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1086">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="cb04f-1087">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1087">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1088">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1088">LTP Results:</span></span>
<span data-ttu-id="cb04f-1089">通过的测试数：690</span><span class="sxs-lookup"><span data-stu-id="cb04f-1089">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="cb04f-1090">未通过的测试数（失败、已跳过等）：274</span><span class="sxs-lookup"><span data-stu-id="cb04f-1090">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="cb04f-1091">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1091">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1092">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1092">Syscall Support</span></span>
<span data-ttu-id="cb04f-1093">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1093">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1094">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1094">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="cb04f-1095">内部版本 14986</span><span class="sxs-lookup"><span data-stu-id="cb04f-1095">Build 14986</span></span>

<span data-ttu-id="cb04f-1096">有关内部版本 14986 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1096">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1097">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1097">Fixed</span></span>

- <span data-ttu-id="cb04f-1098">修复了 Netlink 和 Pty IOCTL 的 bug 检查</span><span class="sxs-lookup"><span data-stu-id="cb04f-1098">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="cb04f-1099">内核版本现在会报告 4.4.0-43，以便与 Xenial 保持一致</span><span class="sxs-lookup"><span data-stu-id="cb04f-1099">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="cb04f-1100">现在，当输入定向到 'nul:' 时会启动 Bash.exe (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1100">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="cb04f-1101">现在，procfs 中会正确报告线程 ID (GH #967)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1101">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="cb04f-1102">现在，inotify_add_watch() 中支持 IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 标志 (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1102">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="cb04f-1103">实现 timer_create 和相关的系统调用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1103">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="cb04f-1104">这会启用 GHC 支持 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1104">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="cb04f-1105">修复了 ping 返回时间 0.000ms 的问题 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1105">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="cb04f-1106">打开过多的文件时返回正确的错误代码。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1106">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="cb04f-1107">修复了 WSL 中的问题：如果网络接口的硬件地址为 32 字节（例如 Teredo 接口），则针对该网络接口数据的 Netlink 请求将会失败并返回 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1107">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="cb04f-1108">请注意，Linux“ip”实用工具包含一个 bug：如果 WSL 报告 32 字节硬件地址，该实用工具将会崩溃。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1108">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="cb04f-1109">这是“ip”（而不是 WSL）中的一个 bug。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1109">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="cb04f-1110">“ip”实用工具会将用于输出硬件地址的字符串缓冲区的长度硬编码，而该缓冲区太小，无法输出 32 字节硬件地址。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1110">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="cb04f-1111">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1111">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1112">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1112">LTP Results:</span></span>
<span data-ttu-id="cb04f-1113">通过的测试数：669</span><span class="sxs-lookup"><span data-stu-id="cb04f-1113">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="cb04f-1114">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="cb04f-1114">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="cb04f-1115">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1115">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1116">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1116">Syscall Support</span></span>
<span data-ttu-id="cb04f-1117">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1117">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1118">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1118">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="cb04f-1119">内部版本 14971</span><span class="sxs-lookup"><span data-stu-id="cb04f-1119">Build 14971</span></span>

<span data-ttu-id="cb04f-1120">有关内部版本 14971 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1120">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1121">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1121">Fixed</span></span>

 - <span data-ttu-id="cb04f-1122">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1122">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="cb04f-1123">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1123">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1124">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1124">LTP Results:</span></span>
<span data-ttu-id="cb04f-1125">自 14965 以来无更改</span><span class="sxs-lookup"><span data-stu-id="cb04f-1125">Unchanged from 14965</span></span> </br>
<span data-ttu-id="cb04f-1126">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="cb04f-1126">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="cb04f-1127">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1127">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1128">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1128">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="cb04f-1129">内部版本 14965</span><span class="sxs-lookup"><span data-stu-id="cb04f-1129">Build 14965</span></span>

<span data-ttu-id="cb04f-1130">有关内部版本 14965 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1130">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1131">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1131">Fixed</span></span>

- <span data-ttu-id="cb04f-1132">支持 Netlink 套接字 NETLINK_ROUTE 协议的 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1132">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="cb04f-1133">为网络枚举启用 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="cb04f-1133">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="cb04f-1134">在 [WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)中可以找到详细信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1134">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="cb04f-1135">/sbin 现在默认位于用户的路径中</span><span class="sxs-lookup"><span data-stu-id="cb04f-1135">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="cb04f-1136">NT 用户路径现在默认会追加到 WSL 路径（即，现在可以键入 notepad.exe，无需将 System32 添加到 Linux 路径）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1136">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="cb04f-1137">添加了对 /proc/sys/kernel/cap_last_cap 的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1137">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="cb04f-1138">现在，如果当前工作目录包含非 ANSI 字符，则可以从 WSL 启动 NT 二进制文件 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1138">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="cb04f-1139">允许在断开连接的 unix 流套接字上关闭。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1139">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="cb04f-1140">添加了对 PR_GET_PDEATHSIG 的支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1140">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="cb04f-1141">添加了对 CLONE_PARENT 的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1141">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="cb04f-1142">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1142">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="cb04f-1143">处理连接到当前终端的请求。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1143">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="cb04f-1144">将 /proc/<pid>/oom_score_adj 标记为可写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1144">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="cb04f-1145">添加 /sys/fs/cgroup 文件夹。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1145">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="cb04f-1146">sched_setaffinity 应返回关联位掩码的数目</span><span class="sxs-lookup"><span data-stu-id="cb04f-1146">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="cb04f-1147">修复错误地假设解释器路径长度必须小于 64 个字符的 ELF 验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1147">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="cb04f-1148">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1148">(GH #743)</span></span>
- <span data-ttu-id="cb04f-1149">打开文件描述符会使控制台窗口保持打开状态 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1149">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="cb04f-1150">修复了当目标名称包含尾随斜杠时 rename() 失败的错误 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1150">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="cb04f-1151">实现 /proc/net/dev 文件</span><span class="sxs-lookup"><span data-stu-id="cb04f-1151">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="cb04f-1152">修复了计时器精度导致的 0.000ms ping 错误。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1152">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="cb04f-1153">实现了 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1153">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="cb04f-1154">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1154">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1155">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1155">LTP Results:</span></span>
<span data-ttu-id="cb04f-1156">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="cb04f-1156">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="cb04f-1157">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1157">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1158">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1158">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="cb04f-1159">内部版本 14959</span><span class="sxs-lookup"><span data-stu-id="cb04f-1159">Build 14959</span></span>

<span data-ttu-id="cb04f-1160">有关内部版本 14959 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1160">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1161">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1161">Fixed</span></span>

- <span data-ttu-id="cb04f-1162">改善了 Windows 的 Pico 进程通知。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1162">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="cb04f-1163">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)中可以找到更多信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1163">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="cb04f-1164">改善了 Windows 互操作的稳定性</span><span class="sxs-lookup"><span data-stu-id="cb04f-1164">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="cb04f-1165">修复了在启用企业数据保护 (EDP) 后启动 bash.exe 时出现的错误 0x80070057</span><span class="sxs-lookup"><span data-stu-id="cb04f-1165">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="cb04f-1166">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1166">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1167">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1167">LTP Results:</span></span>
<span data-ttu-id="cb04f-1168">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="cb04f-1168">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cb04f-1169">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1169">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1170">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1170">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="cb04f-1171">内部版本 14955</span><span class="sxs-lookup"><span data-stu-id="cb04f-1171">Build 14955</span></span>

<span data-ttu-id="cb04f-1172">有关内部版本 14955 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1172">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1173">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1173">Fixed</span></span>

 - <span data-ttu-id="cb04f-1174">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1174">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="cb04f-1175">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1175">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1176">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1176">LTP Results:</span></span>
<span data-ttu-id="cb04f-1177">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="cb04f-1177">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cb04f-1178">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1178">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1179">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1179">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="cb04f-1180">内部版本 14951</span><span class="sxs-lookup"><span data-stu-id="cb04f-1180">Build 14951</span></span>

<span data-ttu-id="cb04f-1181">有关内部版本 14951 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1181">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="cb04f-1182">新功能：Windows/Ubuntu 互操作性</span><span class="sxs-lookup"><span data-stu-id="cb04f-1182">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="cb04f-1183">现在可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1183">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="cb04f-1184">这样，用户便可以通过前所未有的方式来与其 Windows 环境和系统交互。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1184">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="cb04f-1185">举个简单的例子，用户现在可以运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1185">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="cb04f-1186">可在以下资源中找到详细信息：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1186">More information can be found at:</span></span>

- [<span data-ttu-id="cb04f-1187">WSL 团队的互操作博客</span><span class="sxs-lookup"><span data-stu-id="cb04f-1187">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="cb04f-1188">MSDN 互操作文档</span><span class="sxs-lookup"><span data-stu-id="cb04f-1188">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1189">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1189">Fixed</span></span>

- <span data-ttu-id="cb04f-1190">现在将为所有新的 WSL 实例安装 Ubuntu 16.04 (Xenial)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1190">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="cb04f-1191">使用现有 14.04 (Trusty) 实例的用户不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1191">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="cb04f-1192">现在会显示安装过程中指定的区域设置</span><span class="sxs-lookup"><span data-stu-id="cb04f-1192">Locale set during install is now displayed</span></span>
- <span data-ttu-id="cb04f-1193">终端改进，包括修复了不是总能将 WSL 进程重定向到文件的 bug</span><span class="sxs-lookup"><span data-stu-id="cb04f-1193">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="cb04f-1194">控制台生存期应与 bash.exe 生存期密切关联</span><span class="sxs-lookup"><span data-stu-id="cb04f-1194">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="cb04f-1195">控制台窗口大小应使用可视大小，而不是缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="cb04f-1195">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="cb04f-1196">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1196">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1197">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1197">LTP Results:</span></span>
<span data-ttu-id="cb04f-1198">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="cb04f-1198">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cb04f-1199">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1199">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1200">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1200">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="cb04f-1201">内部版本 14946</span><span class="sxs-lookup"><span data-stu-id="cb04f-1201">Build 14946</span></span>

<span data-ttu-id="cb04f-1202">有关内部版本 14946 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1202">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1203">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1203">Fixed</span></span>

- <span data-ttu-id="cb04f-1204">修复了阻止使用包含空格或引号的 NT 用户名为用户创建 WSL 用户帐户的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1204">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="cb04f-1205">更改 VolFs 和 DrvFs，以在统计信息中返回 0 作为目录的链接计数</span><span class="sxs-lookup"><span data-stu-id="cb04f-1205">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="cb04f-1206">支持 IPV6_MULTICAST_HOPS 套接字选项。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1206">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="cb04f-1207">限制为每个 tty 只有一个控制台 I/O 循环。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1207">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="cb04f-1208">例如，可运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1208">Example: the following command is possible:</span></span>
  - <span data-ttu-id="cb04f-1209">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="cb04f-1209">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="cb04f-1210">在 /proc/cpuinfo 中将空格替换为制表符 (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1210">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="cb04f-1211">DrvFs 现在会显示在 mountinfo 中，其中包含一个与已装载的 Windows 卷匹配的名称</span><span class="sxs-lookup"><span data-stu-id="cb04f-1211">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="cb04f-1212">/home 和 /root 现在会显示在 mountinfo 中，并显示正确的名称</span><span class="sxs-lookup"><span data-stu-id="cb04f-1212">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="cb04f-1213">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1213">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1214">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1214">LTP Results:</span></span>
<span data-ttu-id="cb04f-1215">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="cb04f-1215">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cb04f-1216">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1216">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1217">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1217">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="cb04f-1218">内部版本 14942</span><span class="sxs-lookup"><span data-stu-id="cb04f-1218">Build 14942</span></span>

<span data-ttu-id="cb04f-1219">有关内部版本 14942 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1219">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1220">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1220">Fixed</span></span>

- <span data-ttu-id="cb04f-1221">解决了一些 bug 检查，包括阻止 SSH 的“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”网络崩溃</span><span class="sxs-lookup"><span data-stu-id="cb04f-1221">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="cb04f-1222">inotifiy 现在支持从 DrvFs 上的 Windows 应用程序生成通知</span><span class="sxs-lookup"><span data-stu-id="cb04f-1222">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="cb04f-1223">实现 mongod 的 TCP_KEEPIDLE 和 TCP_KEEPINTVL。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1223">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="cb04f-1224">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1224">(GH #695)</span></span>
- <span data-ttu-id="cb04f-1225">实现 pivot_root 系统调用</span><span class="sxs-lookup"><span data-stu-id="cb04f-1225">Implement the pivot_root system call</span></span>
- <span data-ttu-id="cb04f-1226">实现 SO_DONTROUTE 的套接字选项</span><span class="sxs-lookup"><span data-stu-id="cb04f-1226">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="cb04f-1227">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1227">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="cb04f-1228">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1228">LTP Results:</span></span>
<span data-ttu-id="cb04f-1229">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="cb04f-1229">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="cb04f-1230">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="cb04f-1230">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="cb04f-1231">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1231">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1232">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1232">Syscall Support</span></span>
<span data-ttu-id="cb04f-1233">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1233">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1234">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1234">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="cb04f-1235">内部版本 14936</span><span class="sxs-lookup"><span data-stu-id="cb04f-1235">Build 14936</span></span>

<span data-ttu-id="cb04f-1236">有关内部版本 14936 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1236">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="cb04f-1237">注意：在即将发布的版本中，WSL 将会安装 Ubuntu 版本16.04 (Xenial) 而不是 Ubuntu 14.04 (Trusty)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1237">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="cb04f-1238">此更改将应用到安装新实例的预览体验版（lxrun /install 或首次运行 bash.exe）。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1238">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="cb04f-1239">包含 Trusty 的现有实例不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1239">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="cb04f-1240">用户可以使用 do-release-upgrade 命令将其 Trusty 映像升级到 Xenial。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1240">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="cb04f-1241">已知问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1241">Known Issue</span></span>
<span data-ttu-id="cb04f-1242">WSL 遇到了某些套接字实现的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1242">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="cb04f-1243">bug 检查将自身显示为崩溃，并出现错误“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1243">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="cb04f-1244">此问题的最常见表现形式是使用 ssh 时发生崩溃。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1244">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="cb04f-1245">根本原因已在内部版本中修复，将会尽快推送到预览体验版。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1245">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="cb04f-1246">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1246">Fixed</span></span>

- <span data-ttu-id="cb04f-1247">实现了 chroot 系统调用</span><span class="sxs-lookup"><span data-stu-id="cb04f-1247">Implemented the chroot system call</span></span>
- <span data-ttu-id="cb04f-1248">inotifiy 的改进，~~包括支持从 DrvFs 上的 Windows 应用程序生成通知~~</span><span class="sxs-lookup"><span data-stu-id="cb04f-1248">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="cb04f-1249">更正：对源自 Windows 应用程序的更改的 Inotify 支持目前不可用。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1249">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="cb04f-1250">与 IPV6::<port n> 的套接字绑定现在支持 IPV6_V6ONLY（GH #68、#157、#393、#460、#674、#740、#982、#996）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1250">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="cb04f-1251">实现了 waitid 系统调用的 WNOWAIT 行为 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1251">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="cb04f-1252">支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="cb04f-1252">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="cb04f-1253">零长度 read() 应立即返回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1253">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="cb04f-1254">在 .tar 文件中正确处理不包含 NULL 终止符的文件名和文件名前缀。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1254">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="cb04f-1255">对 /dev/null 的 epoll 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1255">epoll support for /dev/null</span></span>
- <span data-ttu-id="cb04f-1256">修复 /dev/alarm 时间源</span><span class="sxs-lookup"><span data-stu-id="cb04f-1256">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="cb04f-1257">Bash -c 现在可以重定向到文件</span><span class="sxs-lookup"><span data-stu-id="cb04f-1257">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="cb04f-1258">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1258">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1259">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1259">LTP Results:</span></span>
<span data-ttu-id="cb04f-1260">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="cb04f-1260">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="cb04f-1261">未通过的测试数（失败、已跳过等）：264</span><span class="sxs-lookup"><span data-stu-id="cb04f-1261">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="cb04f-1262">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1262">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1263">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1263">Syscall Support</span></span>
<span data-ttu-id="cb04f-1264">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1264">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1265">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1265">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="cb04f-1266">内部版本 14931</span><span class="sxs-lookup"><span data-stu-id="cb04f-1266">Build 14931</span></span>

<span data-ttu-id="cb04f-1267">有关内部版本 14931 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1267">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1268">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1268">Fixed</span></span>

 - <span data-ttu-id="cb04f-1269">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1269">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="cb04f-1270">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1270">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="cb04f-1271">内部版本 14926</span><span class="sxs-lookup"><span data-stu-id="cb04f-1271">Build 14926</span></span>

<span data-ttu-id="cb04f-1272">有关内部版本 14926 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1272">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1273">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1273">Fixed</span></span>

- <span data-ttu-id="cb04f-1274">Ping 现在可以在没有管理员特权的控制台中正常运行</span><span class="sxs-lookup"><span data-stu-id="cb04f-1274">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="cb04f-1275">现在支持 Ping6，也无需管理员特权</span><span class="sxs-lookup"><span data-stu-id="cb04f-1275">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="cb04f-1276">对通过 WSL 修改的文件的 Inotify 支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1276">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="cb04f-1277">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1277">(GH #216)</span></span>
  - <span data-ttu-id="cb04f-1278">支持的标志：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1278">Flags supported:</span></span>
    - <span data-ttu-id="cb04f-1279">inotify_init1：LX_O_CLOEXEC、LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="cb04f-1279">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="cb04f-1280">inotify_add_watch 事件：LX_IN_ACCESS、LX_IN_MODIFY、LX_IN_ATTRIB、LX_IN_CLOSE_WRITE、LX_IN_CLOSE_NOWRITE、LX_IN_OPEN、LX_IN_MOVED_FROM、LX_IN_MOVED_TO、LX_IN_CREATE、LX_IN_DELETE、LX_IN_DELETE_SELF、LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="cb04f-1280">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="cb04f-1281">inotify_add_watch 属性：LX_IN_DONT_FOLLOW、LX_IN_EXCL_UNLINK、LX_IN_MASK_ADD、LX_IN_ONESHOT、LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="cb04f-1281">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="cb04f-1282">读取输出：LX_IN_ISDIR、LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="cb04f-1282">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="cb04f-1283">已知问题：修改 Windows 应用程序中的文件不会生成任何事件</span><span class="sxs-lookup"><span data-stu-id="cb04f-1283">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="cb04f-1284">Unix 套接字现在支持 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="cb04f-1284">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="cb04f-1285">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="cb04f-1285">LTP Results:</span></span>
<span data-ttu-id="cb04f-1286">通过的测试数：651</span><span class="sxs-lookup"><span data-stu-id="cb04f-1286">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="cb04f-1287">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="cb04f-1287">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="cb04f-1288">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1288">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="cb04f-1289">内部版本 14915</span><span class="sxs-lookup"><span data-stu-id="cb04f-1289">Build 14915</span></span>

<span data-ttu-id="cb04f-1290">有关内部版本 14915 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1290">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1291">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1291">Fixed</span></span>
-  <span data-ttu-id="cb04f-1292">Unix 数据报套接字的套接字对 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1292">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="cb04f-1293">对 SO_REUSEADDR 的 Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1293">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="cb04f-1294">对 SO_BROADCAST 的 UNIX 套接字支持 (GH #568)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1294">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="cb04f-1295">对 SOCK_SEQPACKET 的 Unix 套接字支持（GH #758、#546）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1295">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="cb04f-1296">添加对 Unix 数据报套接字 send、recv 和 shutdown 的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1296">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="cb04f-1297">修复对非固定地址的无效 mmap 参数验证导致的 bug 检查。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1297">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="cb04f-1298">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1298">(GH #847)</span></span>
- <span data-ttu-id="cb04f-1299">支持暂停/恢复终端状态</span><span class="sxs-lookup"><span data-stu-id="cb04f-1299">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="cb04f-1300">支持使用 TIOCPKT ioctl 阻止 Screen 实用工具 (GH #774)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1300">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="cb04f-1301">已知问题：功能键不起作用</span><span class="sxs-lookup"><span data-stu-id="cb04f-1301">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="cb04f-1302">更正了 TimerFd 中的一种争用状态，该状态可能导致 LxpTimerFdWorkerRoutine 访问已释放的成员“ReaderReady” (GH #814)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1302">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="cb04f-1303">为 futex、poll 和 clock_nanosleep 启用可重启系统调用支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1303">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="cb04f-1304">添加了绑定装载支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1304">Added bind mount support</span></span>
- <span data-ttu-id="cb04f-1305">装载命名空间支持的取消共享</span><span class="sxs-lookup"><span data-stu-id="cb04f-1305">unshare for mount namespace support</span></span>
    - <span data-ttu-id="cb04f-1306">已知问题：使用 `unshare(CLONE_NEWNS)` 创建新的装载命名空间时，当前工作目录将继续指向旧命名空间</span><span class="sxs-lookup"><span data-stu-id="cb04f-1306">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="cb04f-1307">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="cb04f-1307">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="cb04f-1308">内部版本 14905</span><span class="sxs-lookup"><span data-stu-id="cb04f-1308">Build 14905</span></span>

<span data-ttu-id="cb04f-1309">有关内部版本 14905 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1309">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1310">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1310">Fixed</span></span>
- <span data-ttu-id="cb04f-1311">现在支持可重启系统调用（GH #349、GH #520）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1311">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="cb04f-1312">现在可正常使用指向以 / 结尾的目录的符号链接 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1312">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="cb04f-1313">为 /dev/random 实现了 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="cb04f-1313">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="cb04f-1314">实现了 /proc/[pid]/mounts、/proc/[pid]/mountinfo 和 /proc/[pid]/mountstats 文件</span><span class="sxs-lookup"><span data-stu-id="cb04f-1314">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="cb04f-1315">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1315">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="cb04f-1316">内部版本 14901</span><span class="sxs-lookup"><span data-stu-id="cb04f-1316">Build 14901</span></span>
<span data-ttu-id="cb04f-1317">Windows 10 周年更新版的第一个预览体验内部版本。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1317">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="cb04f-1318">有关内部版本 14901 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1318">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1319">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1319">Fixed</span></span>
- <span data-ttu-id="cb04f-1320">修复了尾随斜杠问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1320">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="cb04f-1321">`$ mv a/c/ a/b/` 等命令现在可正常运行</span><span class="sxs-lookup"><span data-stu-id="cb04f-1321">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="cb04f-1322">安装程序现在会提示是否应将 Ubuntu 区域设置指定为 Windows 区域设置</span><span class="sxs-lookup"><span data-stu-id="cb04f-1322">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="cb04f-1323">对 ns 文件夹的 Procfs 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1323">Procfs support for ns folder</span></span>
- <span data-ttu-id="cb04f-1324">添加了 tmpfs、procfs 和 sysfs 文件系统的装入点和卸载点</span><span class="sxs-lookup"><span data-stu-id="cb04f-1324">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="cb04f-1325">修复 mknod [at] 32 位 ABI 签名</span><span class="sxs-lookup"><span data-stu-id="cb04f-1325">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="cb04f-1326">Unix 套接字已移到调度模型</span><span class="sxs-lookup"><span data-stu-id="cb04f-1326">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="cb04f-1327">应遵循使用 setsockopt 设置的 INET 套接字接收缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="cb04f-1327">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="cb04f-1328">实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志</span><span class="sxs-lookup"><span data-stu-id="cb04f-1328">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="cb04f-1329">Linux 进程 stdin/stdout 管道重定向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1329">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="cb04f-1330">允许在 CMD 中使用竖线分隔 bash -c 命令。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1330">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="cb04f-1331">示例：>dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="cb04f-1331">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="cb04f-1332">Bash 现在可以安装在包含多个页面文件的系统上（GH #538、#358）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1332">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="cb04f-1333">默认的 INET 套接字缓冲区大小应与默认 Ubuntu 安装的大小相匹配</span><span class="sxs-lookup"><span data-stu-id="cb04f-1333">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="cb04f-1334">将 xattr syscall 与 listxattr 对齐</span><span class="sxs-lookup"><span data-stu-id="cb04f-1334">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="cb04f-1335">仅返回使用 SIOCGIFCONF 中有效 IPv4 地址的接口</span><span class="sxs-lookup"><span data-stu-id="cb04f-1335">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="cb04f-1336">修复 ptrace 注入时的信号默认操作</span><span class="sxs-lookup"><span data-stu-id="cb04f-1336">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="cb04f-1337">实现 /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="cb04f-1337">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="cb04f-1338">在 sigreturn 中还原上下文时使用计算机上下文寄存器值</span><span class="sxs-lookup"><span data-stu-id="cb04f-1338">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="cb04f-1339">这解决了某些用户遇到的 java 和 javac 挂起问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1339">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="cb04f-1340">实现 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="cb04f-1340">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1341">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1341">Syscall Support</span></span>
<span data-ttu-id="cb04f-1342">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1342">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1343">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1343">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="cb04f-1344">Windows 10 周年更新的内部版本 14388</span><span class="sxs-lookup"><span data-stu-id="cb04f-1344">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="cb04f-1345">有关内部版本 14388 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1345">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1346">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1346">Fixed</span></span>
- <span data-ttu-id="cb04f-1347">修复在 8/2 准备 Windows 10 周年更新时出现的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1347">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="cb04f-1348">可在我们的[博客](https://blogs.msdn.microsoft.com/wsl/)中找到有关周年更新中的 WSL 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1348">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="cb04f-1349">内部版本 14376</span><span class="sxs-lookup"><span data-stu-id="cb04f-1349">Build 14376</span></span>
<span data-ttu-id="cb04f-1350">有关内部版本 14376 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1350">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1351">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1351">Fixed</span></span>
- <span data-ttu-id="cb04f-1352">删除了一些存在 apt-get 挂起问题的实例 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1352">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="cb04f-1353">修复了不正确处理空装入点的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1353">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="cb04f-1354">修复了不正确装载 ramdisk 的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1354">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="cb04f-1355">更改 unix 套接字接受行为以支持标志（在 GH #451 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1355">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="cb04f-1356">修复了与网络相关的常见蓝屏问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1356">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="cb04f-1357">修复了访问 /proc/[pid]/task 时出现蓝屏的问题 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1357">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="cb04f-1358">修复了在某些 pty 方案中 CPU 利用率偏高的问题（GH #488、#504）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1358">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="cb04f-1359">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1359">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="cb04f-1360">内部版本 14371</span><span class="sxs-lookup"><span data-stu-id="cb04f-1360">Build 14371</span></span>
<span data-ttu-id="cb04f-1361">有关内部版本 14371 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1361">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1362">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1362">Fixed</span></span>
- <span data-ttu-id="cb04f-1363">更正了使用 ptrace 时 SIGCHLD 和 wait() 出现计时争用的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1363">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="cb04f-1364">更正了当路径包含尾随 / 时出现的某种行为 (GH #432)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1364">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="cb04f-1365">修复了由于打开子级句柄导致重命名/取消链接失败的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1365">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="cb04f-1366">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1366">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="cb04f-1367">内部版本 14366</span><span class="sxs-lookup"><span data-stu-id="cb04f-1367">Build 14366</span></span>
<span data-ttu-id="cb04f-1368">有关内部版本 14366 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1368">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1369">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1369">Fixed</span></span>
- <span data-ttu-id="cb04f-1370">修复通过符号链接创建文件的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1370">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="cb04f-1371">添加了 Python 的 listxattr (GH 385)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1371">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="cb04f-1372">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1372">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1373">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1373">Syscall Support</span></span>
-   <span data-ttu-id="cb04f-1374">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1374">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1375">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1375">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="cb04f-1376">内部版本 14361</span><span class="sxs-lookup"><span data-stu-id="cb04f-1376">Build 14361</span></span>
<span data-ttu-id="cb04f-1377">有关内部版本 14361 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1377">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1378">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1378">Fixed</span></span>
- <span data-ttu-id="cb04f-1379">现在，在 Windows 上的 Ubuntu Bash 中运行时，DrvFs 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1379">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="cb04f-1380">用户可在其 /mnt/c 驱动器中保存 case.txt 和 CASE.TXT</span><span class="sxs-lookup"><span data-stu-id="cb04f-1380">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="cb04f-1381">只有 Windows 上的 Ubuntu Bash 支持区分大小写。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1381">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="cb04f-1382">在 Bash 外部，NTFS 会正确报告文件，但在与 Windows 中的文件交互时，可能会出现意外的行为。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1382">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="cb04f-1383">每个卷的根目录（即 /mnt/c）不区分大小写</span><span class="sxs-lookup"><span data-stu-id="cb04f-1383">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="cb04f-1384">可在[此处](https://support.microsoft.com/en-us/kb/100625)找到有关处理 Windows 中的这些文件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1384">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="cb04f-1385">大幅增强了 pty/tty 支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1385">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="cb04f-1386">现在支持 TMUX 等应用程序 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1386">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="cb04f-1387">修复了不总会创建用户帐户的安装问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1387">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="cb04f-1388">优化了命令行参数结构，允许极长的参数列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1388">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="cb04f-1389">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1389">(GH #153)</span></span>
- <span data-ttu-id="cb04f-1390">现在可对 DrvFs 中的只读文件执行删除和 chmod</span><span class="sxs-lookup"><span data-stu-id="cb04f-1390">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="cb04f-1391">修复了一些在断开连接时终端会挂起的实例 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1391">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="cb04f-1392">现在可在 tty 设备上正常运行 chmod 和 chown</span><span class="sxs-lookup"><span data-stu-id="cb04f-1392">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="cb04f-1393">允许连接到作为 localhost 的 0.0.0.0 和 :: (GH #388)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1393">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="cb04f-1394">Sendmsg/recvmsg 现在可处理大于 1 的 IO 矢量长度（在 GH #376 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1394">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="cb04f-1395">用户现在可以选择禁用自动生成的 hosts 文件 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1395">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="cb04f-1396">在安装期间自动将 Linux 区域设置与 NT 区域设置进行匹配 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1396">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="cb04f-1397">添加了 /proc/sys/vm/swappiness 文件 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1397">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="cb04f-1398">strace 现在会正常退出</span><span class="sxs-lookup"><span data-stu-id="cb04f-1398">strace now exits correctly</span></span>
- <span data-ttu-id="cb04f-1399">允许通过 /proc/self/fd 重新打开管道 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1399">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="cb04f-1400">在 DrvFs 中隐藏 %LOCALAPPDATA%\lxss 下的目录 (GH #270)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1400">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="cb04f-1401">更好地处理 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1401">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="cb04f-1402">现在支持类似于“bash ~ -c ls”的命令 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1402">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="cb04f-1403">现在，在关闭期间，套接字会通知 epoll read 可用 (GH #271)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1403">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="cb04f-1404">lxrun /uninstall 可以更好地删除文件和文件夹</span><span class="sxs-lookup"><span data-stu-id="cb04f-1404">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="cb04f-1405">更正了 ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1405">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="cb04f-1406">改善了对 xEmacs 等 x11 应用的支持 (GH #481)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1406">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="cb04f-1407">更新了初始线程堆栈大小，以匹配默认的 Ubuntu 设置，并正确地向 get_rlimit syscall 报告大小（GH #172、#258）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1407">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="cb04f-1408">改善了 pico 进程映像名称的报告（例如，用于审核）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1408">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="cb04f-1409">实现了 df 命令的 /proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="cb04f-1409">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="cb04f-1410">修复了子名称 .</span><span class="sxs-lookup"><span data-stu-id="cb04f-1410">Fixed symlink error code for child name .</span></span> <span data-ttu-id="cb04f-1411">和 .. 的符号链接错误代码</span><span class="sxs-lookup"><span data-stu-id="cb04f-1411">and ..</span></span>
- <span data-ttu-id="cb04f-1412">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1412">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1413">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1413">Syscall Support</span></span>
<span data-ttu-id="cb04f-1414">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1414">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1415">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1415">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="cb04f-1416">内部版本 14352</span><span class="sxs-lookup"><span data-stu-id="cb04f-1416">Build 14352</span></span>
<span data-ttu-id="cb04f-1417">有关内部版本 14352 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1417">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1418">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1418">Fixed</span></span>
- <span data-ttu-id="cb04f-1419">修复了不正常下载/创建大型文件的问题。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1419">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="cb04f-1420">这应该可以解除 npm 和其他方案的阻碍（GH #3、GH #313）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1420">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="cb04f-1421">删除了一些存在套接字挂起情况的实例</span><span class="sxs-lookup"><span data-stu-id="cb04f-1421">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="cb04f-1422">更正了一些 ptrace 错误</span><span class="sxs-lookup"><span data-stu-id="cb04f-1422">Corrected some ptrace errors</span></span>
- <span data-ttu-id="cb04f-1423">修复了 WSL 中的问题，允许超过 255 个字符的文件名</span><span class="sxs-lookup"><span data-stu-id="cb04f-1423">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="cb04f-1424">改善了对非英语字符的支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1424">Improved support for non-English characters</span></span>
- <span data-ttu-id="cb04f-1425">添加当前 Windows 时区数据并将其设为默认值</span><span class="sxs-lookup"><span data-stu-id="cb04f-1425">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="cb04f-1426">每个装入点的唯一设备 ID （JRE 修复 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="cb04f-1426">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="cb04f-1427">更正路径中包含“.”</span><span class="sxs-lookup"><span data-stu-id="cb04f-1427">Correct issue with paths containing “.”</span></span> <span data-ttu-id="cb04f-1428">和“..”的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1428">and “..”</span></span>
- <span data-ttu-id="cb04f-1429">添加了 Fifo 支持 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1429">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="cb04f-1430">更新了 resolv.conf 的格式，以匹配本机 Ubuntu 格式</span><span class="sxs-lookup"><span data-stu-id="cb04f-1430">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="cb04f-1431">一些 procfs 清理</span><span class="sxs-lookup"><span data-stu-id="cb04f-1431">Some procfs cleanup</span></span>
- <span data-ttu-id="cb04f-1432">为管理员控制台启用了 ping (GH #18)</span><span class="sxs-lookup"><span data-stu-id="cb04f-1432">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1433">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1433">Syscall Support</span></span>
<span data-ttu-id="cb04f-1434">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1434">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1435">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1435">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="cb04f-1436">内部版本 14342</span><span class="sxs-lookup"><span data-stu-id="cb04f-1436">Build 14342</span></span>
<span data-ttu-id="cb04f-1437">有关内部版本 14342 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1437">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="cb04f-1438">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl)中可以找到有关 VolFs 和 DriveFs 的信息。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1438">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="cb04f-1439">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1439">Fixed</span></span>
- <span data-ttu-id="cb04f-1440">修复了 Windows 用户在用户名中包含 Unicode 字符时出现的安装问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1440">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="cb04f-1441">现在，在首次运行时，默认会提供“常见问题解答”中的 apt-get update udev 解决方法</span><span class="sxs-lookup"><span data-stu-id="cb04f-1441">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="cb04f-1442">在 DriveFs (/mnt/<drive>) 目录中启用了符号链接</span><span class="sxs-lookup"><span data-stu-id="cb04f-1442">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="cb04f-1443">现在可以在 DriveFs 和 VolFs 之间使用符号链接</span><span class="sxs-lookup"><span data-stu-id="cb04f-1443">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="cb04f-1444">解决了顶级路径分析问题：ls .// 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="cb04f-1444">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="cb04f-1445">DriveFs 上的 npm install 和 -g 选项现在可正常工作</span><span class="sxs-lookup"><span data-stu-id="cb04f-1445">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="cb04f-1446">修复了阻止 PHP 服务器启动的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1446">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="cb04f-1447">更新了默认环境值（例如 $PATH），以便与本机 Ubuntu 更匹配</span><span class="sxs-lookup"><span data-stu-id="cb04f-1447">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="cb04f-1448">在 Windows 中添加了每周维护任务以更新 apt 包缓存</span><span class="sxs-lookup"><span data-stu-id="cb04f-1448">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="cb04f-1449">修复了 ELF 标头验证的问题，WSL 现在支持所有 Melkor 选项</span><span class="sxs-lookup"><span data-stu-id="cb04f-1449">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="cb04f-1450">Zsh shell 可正常运行</span><span class="sxs-lookup"><span data-stu-id="cb04f-1450">Zsh shell is functional</span></span>
- <span data-ttu-id="cb04f-1451">现在支持预编译的 Go 二进制文件</span><span class="sxs-lookup"><span data-stu-id="cb04f-1451">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="cb04f-1452">现已正确本地化首次运行 Bash 时出现的提示</span><span class="sxs-lookup"><span data-stu-id="cb04f-1452">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="cb04f-1453">/proc/meminfo 现在会返回正确的信息</span><span class="sxs-lookup"><span data-stu-id="cb04f-1453">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="cb04f-1454">VFS 现在支持套接字</span><span class="sxs-lookup"><span data-stu-id="cb04f-1454">Sockets now supported in VFS</span></span>
- <span data-ttu-id="cb04f-1455">/dev 现在装载为 tempfs</span><span class="sxs-lookup"><span data-stu-id="cb04f-1455">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="cb04f-1456">现在支持 Fifo</span><span class="sxs-lookup"><span data-stu-id="cb04f-1456">Fifo now supported</span></span>
- <span data-ttu-id="cb04f-1457">多核系统现在会在 /proc/cpuinfo 中正确显示</span><span class="sxs-lookup"><span data-stu-id="cb04f-1457">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="cb04f-1458">其他改进以及首次运行期间下载内容时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="cb04f-1458">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="cb04f-1459">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1459">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="cb04f-1460">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1460">Supported syscall list below.</span></span>
- <span data-ttu-id="cb04f-1461">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1461">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="cb04f-1462">已知问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1462">Known Issues</span></span>
- <span data-ttu-id="cb04f-1463">在某些情况下，</span><span class="sxs-lookup"><span data-stu-id="cb04f-1463">Not resolving ‘..’</span></span> <span data-ttu-id="cb04f-1464">不会正确解析 DriveFs 上的“..”</span><span class="sxs-lookup"><span data-stu-id="cb04f-1464">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1465">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1465">Syscall Support</span></span>
<span data-ttu-id="cb04f-1466">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1466">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1467">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1467">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="cb04f-1468">内部版本 14332</span><span class="sxs-lookup"><span data-stu-id="cb04f-1468">Build 14332</span></span>

<span data-ttu-id="cb04f-1469">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1469">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="cb04f-1470">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1470">Fixed</span></span>
- <span data-ttu-id="cb04f-1471">更好地生成 resolv.conf，包括指定 DNS 项的优先级</span><span class="sxs-lookup"><span data-stu-id="cb04f-1471">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="cb04f-1472">在 /mnt 与非 /mnt 驱动器之间移动文件和目录时出现的问题</span><span class="sxs-lookup"><span data-stu-id="cb04f-1472">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="cb04f-1473">现在可以使用符号链接创建 Tar 文件。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1473">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="cb04f-1474">创建实例时会添加默认的 /run/lock 目录</span><span class="sxs-lookup"><span data-stu-id="cb04f-1474">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="cb04f-1475">更新 /dev/null 以返回正确的统计信息</span><span class="sxs-lookup"><span data-stu-id="cb04f-1475">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="cb04f-1476">首次运行期间下载内容时出现的其他错误</span><span class="sxs-lookup"><span data-stu-id="cb04f-1476">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="cb04f-1477">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1477">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="cb04f-1478">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1478">Supported syscall list below.</span></span>
- <span data-ttu-id="cb04f-1479">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1479">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1480">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1480">Syscall Support</span></span>
<span data-ttu-id="cb04f-1481">下面是在 WSL 中具有某种实现的新 syscall。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1481">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="cb04f-1482">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1482">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="cb04f-1483">内部版本 14328</span><span class="sxs-lookup"><span data-stu-id="cb04f-1483">Build 14328</span></span>

<span data-ttu-id="cb04f-1484">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1484">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="cb04f-1485">新功能</span><span class="sxs-lookup"><span data-stu-id="cb04f-1485">New Features</span></span>
* <span data-ttu-id="cb04f-1486">现在支持 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1486">Now support Linux users.</span></span>  <span data-ttu-id="cb04f-1487">安装 Windows 上的 Ubuntu Bash 时会提示创建 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1487">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="cb04f-1488">有关详细信息，请访问 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="cb04f-1488">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="cb04f-1489">现在，主机名将设置为 Windows 计算机名，而不再是 @localhost</span><span class="sxs-lookup"><span data-stu-id="cb04f-1489">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="cb04f-1490">有关内部版本 14328 的详细信息，请访问： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="cb04f-1490">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="cb04f-1491">固定</span><span class="sxs-lookup"><span data-stu-id="cb04f-1491">Fixed</span></span>
* <span data-ttu-id="cb04f-1492">非 /mnt/<drive> 文件的符号链接改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1492">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="cb04f-1493">现在可正常运行 npm install</span><span class="sxs-lookup"><span data-stu-id="cb04f-1493">npm install now works</span></span>
    * <span data-ttu-id="cb04f-1494">现在可以根据[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)的说明安装 jdk/jre。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1494">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="cb04f-1495">已知问题：符号链接不适用于 Windows 装载。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1495">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="cb04f-1496">此功能将在以后的内部版本中可用</span><span class="sxs-lookup"><span data-stu-id="cb04f-1496">Functionality will be available in a later build</span></span>
* <span data-ttu-id="cb04f-1497">现在会显示 top 和 htop</span><span class="sxs-lookup"><span data-stu-id="cb04f-1497">top and htop now display</span></span>
* <span data-ttu-id="cb04f-1498">有关某些安装失败的其他错误消息</span><span class="sxs-lookup"><span data-stu-id="cb04f-1498">Additional error messages for some install failures</span></span>
* <span data-ttu-id="cb04f-1499">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1499">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="cb04f-1500">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1500">Supported syscall list below.</span></span>
* <span data-ttu-id="cb04f-1501">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="cb04f-1501">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="cb04f-1502">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="cb04f-1502">Syscall Support</span></span>
<span data-ttu-id="cb04f-1503">下面是在 WSL 中具有某种实现的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1503">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="cb04f-1504">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="cb04f-1504">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
