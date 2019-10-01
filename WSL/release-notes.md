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
ms.openlocfilehash: 0dcf4519877fac5b838d4542dfd088cb6d233353
ms.sourcegitcommit: 0fa3b02b36dc49779e165e689dfded4f3b727124
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71249188"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a><span data-ttu-id="1ff03-105">适用于 Linux 的 Windows 子系统发行说明</span><span class="sxs-lookup"><span data-stu-id="1ff03-105">Release Notes for Windows Subsystem for Linux</span></span>

## <a name="build-18990"></a><span data-ttu-id="1ff03-106">版本 18990</span><span class="sxs-lookup"><span data-stu-id="1ff03-106">Build 18990</span></span>
<span data-ttu-id="1ff03-107">有关版本 18990 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-107">For general Windows information on build 18990 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/24/announcing-windows-10-insider-preview-build-18990/).</span></span>

* <span data-ttu-id="1ff03-108">提高 \\wsl$ 中目录列表的性能</span><span class="sxs-lookup"><span data-stu-id="1ff03-108">Improve the performance for directory listings in \\wsl$</span></span>
* <span data-ttu-id="1ff03-109">[WSL2] 注入额外的启动熵 [GH 4416]</span><span class="sxs-lookup"><span data-stu-id="1ff03-109">[WSL2] Inject additional boot entropy [GH 4416]</span></span>
* <span data-ttu-id="1ff03-110">[WSL2] 修复使用 su/sudo 时的 Windows 互操作 [GH 4465]</span><span class="sxs-lookup"><span data-stu-id="1ff03-110">[WSL2] Fix for Windows interop when using su / sudo [GH 4465]</span></span>


## <a name="build-18980"></a><span data-ttu-id="1ff03-111">内部版本 18980</span><span class="sxs-lookup"><span data-stu-id="1ff03-111">Build 18980</span></span>
<span data-ttu-id="1ff03-112">有关内部版本 18980 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-112">For general Windows information on build 18980 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/11/announcing-windows-10-insider-preview-build-18980/).</span></span>

* <span data-ttu-id="1ff03-113">修复拒绝 FILE_READ_DATA 的读取符号链接。</span><span class="sxs-lookup"><span data-stu-id="1ff03-113">Fix reading symlinks that deny FILE_READ_DATA.</span></span> <span data-ttu-id="1ff03-114">这包括 Windows 为了实现后向兼容而创建的所有符号链接（例如“C:\Document and Settings”），以及用户配置文件目录中的一些符号链接。</span><span class="sxs-lookup"><span data-stu-id="1ff03-114">This includes all the symlinks Windows creates for backwards compatibility such as "C:\Document and Settings" and a bunch of symlinks in the user profile directory</span></span>
* <span data-ttu-id="1ff03-115">使意外的文件系统状态变得不严重 [GH 4334、4305]</span><span class="sxs-lookup"><span data-stu-id="1ff03-115">Make unexpected filesystem state non-fatal [GH 4334, 4305]</span></span>
* <span data-ttu-id="1ff03-116">[WSL2] 添加当 CPU/固件支持虚拟化时对 arm64 的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-116">[WSL2] Add support for arm64 if your CPU / firmware supports virtualization</span></span>
* <span data-ttu-id="1ff03-117">[WSL2] 允许无特权用户查看内核日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-117">[WSL2] Allow unprivileged users to view kernel log</span></span>
* <span data-ttu-id="1ff03-118">[WSL2] 修复关闭 stdout/stderr 套接字后的输出中继 [GH 4375]</span><span class="sxs-lookup"><span data-stu-id="1ff03-118">[WSL2] Fix output relay when stdout / stderr sockets have been closed [GH 4375]</span></span>
* <span data-ttu-id="1ff03-119">[WSL2] 支持电池和交流适配器直通</span><span class="sxs-lookup"><span data-stu-id="1ff03-119">[WSL2] Support battery and AC adapter passthrough</span></span>
* <span data-ttu-id="1ff03-120">[WSL2] 将 Linux 内核更新到 4.19.67</span><span class="sxs-lookup"><span data-stu-id="1ff03-120">[WSL2] Update Linux kernel to 4.19.67</span></span>
* <span data-ttu-id="1ff03-121">添加在 /etc/wsl.conf 中设置默认用户名的功能：</span><span class="sxs-lookup"><span data-stu-id="1ff03-121">Add the ability to set default username in /etc/wsl.conf:</span></span>
```
[user]
default=root
```

## <a name="build-18975"></a><span data-ttu-id="1ff03-122">内部版本 18975</span><span class="sxs-lookup"><span data-stu-id="1ff03-122">Build 18975</span></span>
<span data-ttu-id="1ff03-123">有关内部版本 18975 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-123">For general Windows information on build 18975 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/09/06/announcing-windows-10-insider-preview-build-18975/).</span></span>

* <span data-ttu-id="1ff03-124">[WSL2] 修复大量 localhost 可靠性问题 [GH 4340]</span><span class="sxs-lookup"><span data-stu-id="1ff03-124">[WSL2] Fixed a number of localhost reliability issues [GH 4340]</span></span>

## <a name="build-18970"></a><span data-ttu-id="1ff03-125">内部版本 18970</span><span class="sxs-lookup"><span data-stu-id="1ff03-125">Build 18970</span></span>
<span data-ttu-id="1ff03-126">有关内部版本 18970 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-126">For general Windows information on build 18970 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/08/29/announcing-windows-10-insider-preview-build-18970/).</span></span>

* <span data-ttu-id="1ff03-127">[WSL2] 当系统从睡眠状态恢复时，使时间与主机时间同步 [GH 4245]</span><span class="sxs-lookup"><span data-stu-id="1ff03-127">[WSL2] Sync time with host time when system resumes from sleep state [GH 4245]</span></span>
* <span data-ttu-id="1ff03-128">[WSL2] 在可能的情况下，在 Windows 卷上创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="1ff03-128">[WSL2] Create NT symlinks on the Windows volumes when possible.</span></span>
* <span data-ttu-id="1ff03-129">[WSL2] 在 UTS、IPC、PID 和 Mount 命名空间中创建分发版。</span><span class="sxs-lookup"><span data-stu-id="1ff03-129">[WSL2] Create distros in UTS, IPC, PID, and Mount namespaces.</span></span>
* <span data-ttu-id="1ff03-130">[WSL2] 修复当服务器直接绑定到 localhost 时的 localhost 端口中继 [GH 4353]</span><span class="sxs-lookup"><span data-stu-id="1ff03-130">[WSL2] Fix localhost port relay when server binds to localhost directly [GH 4353]</span></span>
* <span data-ttu-id="1ff03-131">[WSL2] 修复重定向输出时的 interop [GH 4337]</span><span class="sxs-lookup"><span data-stu-id="1ff03-131">[WSL2] Fix interop when output is redirected [GH 4337]</span></span>
* <span data-ttu-id="1ff03-132">[WSL2] 支持转换绝对 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="1ff03-132">[WSL2] Support translating absolute NT symlinks.</span></span>
* <span data-ttu-id="1ff03-133">[WSL2] 将内核更新到 4.19.59</span><span class="sxs-lookup"><span data-stu-id="1ff03-133">[WSL2] Update kernel to 4.19.59</span></span>
* <span data-ttu-id="1ff03-134">[WSL2] 正确设置 eth0 的子网掩码。</span><span class="sxs-lookup"><span data-stu-id="1ff03-134">[WSL2] Properly set subnet mask for eth0.</span></span>
* <span data-ttu-id="1ff03-135">[WSL2] 发出退出事件信号时更改逻辑，以中断控制台工作线程循环。</span><span class="sxs-lookup"><span data-stu-id="1ff03-135">[WSL2] Change logic to break out of console worker loop when exit event is signaled.</span></span>
* <span data-ttu-id="1ff03-136">[WSL2] 分发版未运行时弹出分发版 VHD。</span><span class="sxs-lookup"><span data-stu-id="1ff03-136">[WSL2] Eject distribution vhd when the distro is not running.</span></span>
* <span data-ttu-id="1ff03-137">[WSL2] 修复配置分析库以正确处理空值。</span><span class="sxs-lookup"><span data-stu-id="1ff03-137">[WSL2] Fix config parsing library to correctly handle empty values.</span></span>
* <span data-ttu-id="1ff03-138">[WSL2] 通过创建跨分发版装入点来支持 Docker Desktop。</span><span class="sxs-lookup"><span data-stu-id="1ff03-138">[WSL2] Support Docker Desktop by creating cross distro mounts.</span></span> <span data-ttu-id="1ff03-139">分发版可以通过将以下行添加到 /etc/wsl.conf 文件来启用此行为：</span><span class="sxs-lookup"><span data-stu-id="1ff03-139">A distro can opt-in to this behavior by adding the following line to the /etc/wsl.conf file:</span></span>
```
[automount]
crossDistro = true
```

## <a name="build-18945"></a><span data-ttu-id="1ff03-140">内部版本 18945</span><span class="sxs-lookup"><span data-stu-id="1ff03-140">Build 18945</span></span>
<span data-ttu-id="1ff03-141">有关内部版本 18945 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-141">For general Windows information on build 18945 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-142">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-142">WSL</span></span>
* <span data-ttu-id="1ff03-143">[WSL2] 允许侦听可使用 localhost:port 通过主机访问的 WSL2 中的 TCP 套接字</span><span class="sxs-lookup"><span data-stu-id="1ff03-143">[WSL2] Allow listening tcp sockets in WSL2 to be accessible from the host by using localhost:port</span></span>
* <span data-ttu-id="1ff03-144">[WSL2] 修复安装/转换失败和其他诊断，以跟踪将来的问题 [GH 4105]</span><span class="sxs-lookup"><span data-stu-id="1ff03-144">[WSL2] Fixes for install / conversion failures and additional diagnostics to track down future issues [GH 4105]</span></span> 
* <span data-ttu-id="1ff03-145">[WSL2] 改善 WSL2 网络问题的诊断</span><span class="sxs-lookup"><span data-stu-id="1ff03-145">[WSL2] Improve diagnosability of WSL2 network issues</span></span>
* <span data-ttu-id="1ff03-146">[WSL2] 将内核版本更新到 4.19.55</span><span class="sxs-lookup"><span data-stu-id="1ff03-146">[WSL2] Update kernel version to 4.19.55</span></span>
* <span data-ttu-id="1ff03-147">[WSL2] 使用 Docker 所需的配置选项更新了内核 [GH 4165]</span><span class="sxs-lookup"><span data-stu-id="1ff03-147">[WSL2] Update kernel with config options required for docker [GH 4165]</span></span>
* <span data-ttu-id="1ff03-148">[WSL2] 增加分配给轻型实用程序 VM 的 CPU 数目，使其与主机相同（以前，内核配置中的 CONFIG_NR_CPUS 将数目限制为 8 个）[GH 4137]</span><span class="sxs-lookup"><span data-stu-id="1ff03-148">[WSL2] Increase the number of CPUs assigned to the lightweight utility VM to be the same as the host (was previously capped at 8 by CONFIG_NR_CPUS in the kernel config) [GH 4137]</span></span>
* <span data-ttu-id="1ff03-149">[WSL2] 为 WSL2 轻型 VM 创建交换文件</span><span class="sxs-lookup"><span data-stu-id="1ff03-149">[WSL2] Create a swap file for the WSL2 lightweight VM</span></span>
* <span data-ttu-id="1ff03-150">[WSL2] 允许通过 \\\\wsl$\\distro（例如 sshfs）显示用户装入点 [GH 4172]</span><span class="sxs-lookup"><span data-stu-id="1ff03-150">[WSL2] Allow user mounts to be visible via \\\\wsl$\\distro (for example sshfs) [GH 4172]</span></span>
* <span data-ttu-id="1ff03-151">[WSL2] 改善 9p 文件系统的性能</span><span class="sxs-lookup"><span data-stu-id="1ff03-151">[WSL2] Improve 9p filesystem performance</span></span>
* <span data-ttu-id="1ff03-152">[WSL2] 确保 VHD ACL 不会无限增长 [GH 4126]</span><span class="sxs-lookup"><span data-stu-id="1ff03-152">[WSL2] Ensure vhd ACL does not grow unbounded [GH 4126]</span></span>
* <span data-ttu-id="1ff03-153">[WSL2] 更新内核配置以支持 squashfs 和 xt_conntrack [GH 4107、4123]</span><span class="sxs-lookup"><span data-stu-id="1ff03-153">[WSL2] Update kernel config to support squashfs and xt_conntrack [GH 4107, 4123]</span></span>
* <span data-ttu-id="1ff03-154">[WSL2] 修复 interop.enabled /etc/wsl.conf 选项 [GH 4140]</span><span class="sxs-lookup"><span data-stu-id="1ff03-154">[WSL2] Fix for interop.enabled /etc/wsl.conf option [GH 4140]</span></span>
* <span data-ttu-id="1ff03-155">[WSL2] 如果文件系统不支持 EA，则返回 ENOTSUP</span><span class="sxs-lookup"><span data-stu-id="1ff03-155">[WSL2] Return ENOTSUP if the file system does not support EAs</span></span>
* <span data-ttu-id="1ff03-156">[WSL2] 修复 \\\\wsl$ 时 CopyFile 挂起的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-156">[WSL2] Fix CopyFile hang with \\\\wsl$</span></span>
* <span data-ttu-id="1ff03-157">将默认 umask 切换为 0022，并将 filesystem.umask 设置添加到 /etc/wsl.conf</span><span class="sxs-lookup"><span data-stu-id="1ff03-157">Switch default umask to 0022 and add filesystem.umask setting to /etc/wsl.conf</span></span>
* <span data-ttu-id="1ff03-158">修复 wslpath 以正确解析符号链接，这是19h1 中的回归 [GH 4078]</span><span class="sxs-lookup"><span data-stu-id="1ff03-158">Fix wslpath to properly resolve symlinks, this was regressed in 19h1 [GH 4078]</span></span>
* <span data-ttu-id="1ff03-159">引入 %UserProfile%\\.wslconfig 文件用于调整 WSL2 设置</span><span class="sxs-lookup"><span data-stu-id="1ff03-159">Introduce %UserProfile%\\.wslconfig file for tweaking WSL2 settings</span></span>
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

## <a name="build-18917"></a><span data-ttu-id="1ff03-160">内部版本 18917</span><span class="sxs-lookup"><span data-stu-id="1ff03-160">Build 18917</span></span>
<span data-ttu-id="1ff03-161">有关内部版本 18917 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-161">For general Windows information on build 18917 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-162">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-162">WSL</span></span>
* <span data-ttu-id="1ff03-163">WSL 2 现已推出！</span><span class="sxs-lookup"><span data-stu-id="1ff03-163">WSL 2 is now available!</span></span> <span data-ttu-id="1ff03-164">有关更多详细信息，请参阅[博客](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-164">Please see [blog](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/) for more details.</span></span>
* <span data-ttu-id="1ff03-165">修复一个回归问题：无法通过符号链接启动 Windows 进程 [GH 3999]</span><span class="sxs-lookup"><span data-stu-id="1ff03-165">Fix a regression where launching Windows processes via symlinks did not work correctly [GH 3999]</span></span>
* <span data-ttu-id="1ff03-166">将 wsl.exe --list --verbose、wsl.exe --list --quiet 和 wsl.exe --import --version 选项添加到 wsl.exe</span><span class="sxs-lookup"><span data-stu-id="1ff03-166">Add wsl.exe --list --verbose, wsl.exe --list --quiet, and wsl.exe --import --version options to wsl.exe</span></span>
* <span data-ttu-id="1ff03-167">添加 wsl.exe --shutdown 选项</span><span class="sxs-lookup"><span data-stu-id="1ff03-167">Add wsl.exe --shutdown option</span></span>
* <span data-ttu-id="1ff03-168">Plan 9：允许打开目录以使写入成功</span><span class="sxs-lookup"><span data-stu-id="1ff03-168">Plan 9: Allow opening a directory for write to succeed</span></span>

## <a name="build-18890"></a><span data-ttu-id="1ff03-169">内部版本 18890</span><span class="sxs-lookup"><span data-stu-id="1ff03-169">Build 18890</span></span>
<span data-ttu-id="1ff03-170">有关内部版本 18890 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-170">For general Windows information on build 18890 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-171">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-171">WSL</span></span>
* <span data-ttu-id="1ff03-172">非阻塞套接字泄露 [GH 2913]</span><span class="sxs-lookup"><span data-stu-id="1ff03-172">Non-blocking socket leak [GH 2913]</span></span>
* <span data-ttu-id="1ff03-173">在终端中输入 EOF 可能会阻塞后续读取 [GH 3421]</span><span class="sxs-lookup"><span data-stu-id="1ff03-173">EOF input to terminal can block subsequent reads [GH 3421]</span></span>
* <span data-ttu-id="1ff03-174">更新 resolv.conf 标头以引用 wsl.conf [在 GH 3928 中介绍]</span><span class="sxs-lookup"><span data-stu-id="1ff03-174">Update resolv.conf header to refer to wsl.conf [discussed in GH 3928]</span></span>
* <span data-ttu-id="1ff03-175">epoll delete 代码中的死锁 [GH 3922]</span><span class="sxs-lookup"><span data-stu-id="1ff03-175">Deadlock in epoll delete code [GH 3922]</span></span>
* <span data-ttu-id="1ff03-176">处理 --import 和 –export 的参数中的空格 [GH 3932]</span><span class="sxs-lookup"><span data-stu-id="1ff03-176">Handle spaces in arguments to --import and –export [GH 3932]</span></span>
* <span data-ttu-id="1ff03-177">无法正常扩展 mmap 的文件 [GH 3939]</span><span class="sxs-lookup"><span data-stu-id="1ff03-177">Extending mmap’d files does not work properly [GH 3939]</span></span>
* <span data-ttu-id="1ff03-178">修复无法正常访问 ARM64 \\wsl $ 的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-178">Fix issue with ARM64 \\wsl$ access not working properly</span></span>
* <span data-ttu-id="1ff03-179">为 wsl.exe 添加更好的默认图标</span><span class="sxs-lookup"><span data-stu-id="1ff03-179">Add better default icon for wsl.exe</span></span>

## <a name="build-18342"></a><span data-ttu-id="1ff03-180">内部版本 18342</span><span class="sxs-lookup"><span data-stu-id="1ff03-180">Build 18342</span></span>
<span data-ttu-id="1ff03-181">有关内部版本 18342 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-181">For general Windows information on build 18342 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-182">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-182">WSL</span></span>
* <span data-ttu-id="1ff03-183">我们添加了相应的功能，使用户能够从 Windows 访问 WSL 分发版中的 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-183">We've added the ability for users to access Linux files in a WSL distro from Windows.</span></span> <span data-ttu-id="1ff03-184">可以通过命令行访问这些文件，此外，文件资源管理器、VSCode 等 Windows 应用可与这些文件交互。</span><span class="sxs-lookup"><span data-stu-id="1ff03-184">These files can be accessed through the command line, and also Windows apps, like file explorer, VSCode, etc. can interact with these files.</span></span> <span data-ttu-id="1ff03-185">通过导航到 \\\\wsl$\\<分发版名称> 访问文件，或通过导航到 \\\\wsl$ 来查看正在运行的分发版列表</span><span class="sxs-lookup"><span data-stu-id="1ff03-185">Access your files by navigating to \\\\wsl$\\<distro_name>, or see a list of running distributions by navigating to \\\\wsl$</span></span>
* <span data-ttu-id="1ff03-186">添加额外的 CPU 信息标记，并修复 Cpus_allowed[_list] 值 [GH 2234]</span><span class="sxs-lookup"><span data-stu-id="1ff03-186">Add additional CPU info tags and fix Cpus_allowed[_list] values [GH 2234]</span></span>
* <span data-ttu-id="1ff03-187">支持从非领先线程执行 [GH 3800]</span><span class="sxs-lookup"><span data-stu-id="1ff03-187">Support exec from non-leader thread [GH 3800]</span></span>
* <span data-ttu-id="1ff03-188">将配置更新失败视为非严重错误 [GH 3785]</span><span class="sxs-lookup"><span data-stu-id="1ff03-188">Treat configuration update failures as non-fatal [GH 3785]</span></span>
* <span data-ttu-id="1ff03-189">更新 binfmt 以正确处理偏移 [GH 3768]</span><span class="sxs-lookup"><span data-stu-id="1ff03-189">Update binfmt to properly handle offsets [GH 3768]</span></span>
* <span data-ttu-id="1ff03-190">为 Plan 9 启用映射网络驱动器 [GH 3854]</span><span class="sxs-lookup"><span data-stu-id="1ff03-190">Enable mapping network drives for Plan 9 [GH 3854]</span></span>
* <span data-ttu-id="1ff03-191">支持对绑定载入点执行“Windows -> Linux”和“Linux -> Windows”路径转换</span><span class="sxs-lookup"><span data-stu-id="1ff03-191">Support Windows -> Linux and Linux -> Windows path translation for bind mounts</span></span>
* <span data-ttu-id="1ff03-192">为以只读方式打开的文件中的映射创建只读节</span><span class="sxs-lookup"><span data-stu-id="1ff03-192">Create read-only sections for mappings on files opened read-only</span></span>

## <a name="build-18334"></a><span data-ttu-id="1ff03-193">内部版本 18334</span><span class="sxs-lookup"><span data-stu-id="1ff03-193">Build 18334</span></span>
<span data-ttu-id="1ff03-194">有关内部版本 18334 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-194">For general Windows information on build 18334 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-195">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-195">WSL</span></span>
* <span data-ttu-id="1ff03-196">重新设计 Windows 时区映射到 Linux 时区的方式 [GH 3747]</span><span class="sxs-lookup"><span data-stu-id="1ff03-196">Redesign the way that Windows time zone is mapped to a  Linux time zone [GH 3747]</span></span>
* <span data-ttu-id="1ff03-197">修复内存泄漏，并添加新的字符串转换函数 [GH 3746]</span><span class="sxs-lookup"><span data-stu-id="1ff03-197">Fix memory leaks and add new string translation functions [GH 3746]</span></span>
* <span data-ttu-id="1ff03-198">不包含任何线程的线程组上的 SIGCONT 是一个 no-op [GH 3741]</span><span class="sxs-lookup"><span data-stu-id="1ff03-198">SIGCONT on a threadgroup with no threads is a no-op [GH 3741]</span></span> 
* <span data-ttu-id="1ff03-199">在 /proc/self/fd 中正确显示套接字和 epoll 文件描述符</span><span class="sxs-lookup"><span data-stu-id="1ff03-199">Correctly display socket and epoll file descriptors in /proc/self/fd</span></span>

## <a name="build-18305"></a><span data-ttu-id="1ff03-200">内部版本 18305</span><span class="sxs-lookup"><span data-stu-id="1ff03-200">Build 18305</span></span>
<span data-ttu-id="1ff03-201">有关内部版本 18305 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-201">For general Windows information on build 18305 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-202">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-202">WSL</span></span>
* <span data-ttu-id="1ff03-203">当主线程退出时，pthreads 失去对文件的访问权限 [GH 3589]</span><span class="sxs-lookup"><span data-stu-id="1ff03-203">pthreads lose access to files when the primary thread exits [GH 3589]</span></span>
* <span data-ttu-id="1ff03-204">除非有必要，否则 TIOCSCTTY 应忽略“force”参数 [GH 3652]</span><span class="sxs-lookup"><span data-stu-id="1ff03-204">TIOCSCTTY should ignore the “force” parameter unless it is required [GH 3652]</span></span>
* <span data-ttu-id="1ff03-205">改善 wsl.exe 命令行，并添加导入/导出功能。</span><span class="sxs-lookup"><span data-stu-id="1ff03-205">wsl.exe command line improvements and addition of import / export functionality.</span></span>
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

## <a name="build-18277"></a><span data-ttu-id="1ff03-206">内部版本 18277</span><span class="sxs-lookup"><span data-stu-id="1ff03-206">Build 18277</span></span>
<span data-ttu-id="1ff03-207">有关内部版本 18277 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-207">For general Windows information on build 18277 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-208">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-208">WSL</span></span>
* <span data-ttu-id="1ff03-209">修复内部版本 18272 中引入的“不支持此类接口”错误 [GH 3645]</span><span class="sxs-lookup"><span data-stu-id="1ff03-209">Fix "no such interface supported" error introduced in build 18272 [GH 3645]</span></span>
* <span data-ttu-id="1ff03-210">忽略 umount syscall 的 MNT_FORCE 标志 [GH 3605]</span><span class="sxs-lookup"><span data-stu-id="1ff03-210">Ignore the MNT_FORCE flag for umount syscall [GH 3605]</span></span>
* <span data-ttu-id="1ff03-211">切换 WSL interop 以使用官方的 CreatePseudoConsole API</span><span class="sxs-lookup"><span data-stu-id="1ff03-211">Switch WSL interop to use the official CreatePseudoConsole API</span></span>
* <span data-ttu-id="1ff03-212">FUTEX_WAIT 重启时不保留超时值</span><span class="sxs-lookup"><span data-stu-id="1ff03-212">Maintain no timeout value when FUTEX_WAIT restarts</span></span>

## <a name="build-18272"></a><span data-ttu-id="1ff03-213">内部版本 18272</span><span class="sxs-lookup"><span data-stu-id="1ff03-213">Build 18272</span></span>
<span data-ttu-id="1ff03-214">有关内部版本 18272 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-214">For general Windows information on build 18272 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-215">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-215">WSL</span></span>
* <span data-ttu-id="1ff03-216">**警告：** 此版本中存在一个导致 WSL 不可操作的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-216">**WARNING:** There is an issue in this build that makes WSL inoperable.</span></span> <span data-ttu-id="1ff03-217">尝试启动分发版时，会看到“不支持此类接口”错误。</span><span class="sxs-lookup"><span data-stu-id="1ff03-217">When trying to launch your distribution you will see a “No such interface supported” error.</span></span> <span data-ttu-id="1ff03-218">该问题已修复，下周发布的 Insider Fast 内部版本将会应用修复程序。</span><span class="sxs-lookup"><span data-stu-id="1ff03-218">The issue has been fixed and will be in next week's Insider Fast build.</span></span> <span data-ttu-id="1ff03-219">如果已安装此内部版本，可以使用“设置”->“更新和安全”>“恢复”中的“回退到 Windows 10 的上一个版本”回滚到上一 Windows 内部版本。</span><span class="sxs-lookup"><span data-stu-id="1ff03-219">If you've installed this build you can roll back to the previous Windows build using “Go back to the previous version of Windows 10” in Settings->Update & Security->Recovery.</span></span>

## <a name="build-18267"></a><span data-ttu-id="1ff03-220">内部版本 18267</span><span class="sxs-lookup"><span data-stu-id="1ff03-220">Build 18267</span></span>
<span data-ttu-id="1ff03-221">有关内部版本 18267 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-221">For general Windows information on build 18267 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-222">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-222">WSL</span></span>
* <span data-ttu-id="1ff03-223">修复 zombie 进程不会回收，而是无限期保留的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-223">Fix issue where zombie process may not be reaped and remain indefinitely.</span></span>
* <span data-ttu-id="1ff03-224">如果错误消息超过最大长度，WslRegisterDistribution 将会挂起 [GH 3592]</span><span class="sxs-lookup"><span data-stu-id="1ff03-224">WslRegisterDistribution hangs if error message exceeds max length [GH 3592]</span></span>
* <span data-ttu-id="1ff03-225">允许 fsync 针对 DrvFs 上的只读文件成功运行 [GH 3556]</span><span class="sxs-lookup"><span data-stu-id="1ff03-225">Allow fsync to succeed for read-only files on DrvFs [GH 3556]</span></span>
* <span data-ttu-id="1ff03-226">在内部创建符号链接之前，确保 /bin 和 /sbin 目录存在 [GH 3584]</span><span class="sxs-lookup"><span data-stu-id="1ff03-226">Ensure that /bin and /sbin directories exist before creating symlinks inside [GH 3584]</span></span>
* <span data-ttu-id="1ff03-227">为 WSL 实例添加了实例终止超时机制。</span><span class="sxs-lookup"><span data-stu-id="1ff03-227">Added an instance termination timeout mechanism for WSL instances.</span></span> <span data-ttu-id="1ff03-228">超时目前设置为 15 秒，这意味着，实例将在上一个 WSL 进程退出 15 秒后终止。</span><span class="sxs-lookup"><span data-stu-id="1ff03-228">The timeout is currently set to 15 seconds, meaning the instance will terminate 15 seconds after the last WSL process exits.</span></span> <span data-ttu-id="1ff03-229">若要立即终止分发版，请使用：</span><span class="sxs-lookup"><span data-stu-id="1ff03-229">To terminate a distribution immediately, use:</span></span>
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a><span data-ttu-id="1ff03-230">内部版本 17763 (1809)</span><span class="sxs-lookup"><span data-stu-id="1ff03-230">Build 17763 (1809)</span></span>
<span data-ttu-id="1ff03-231">有关内部版本 17763 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-231">For general Windows information on build 17763 visit the [Windows blog](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-232">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-232">WSL</span></span>
* <span data-ttu-id="1ff03-233">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="1ff03-233">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="1ff03-234">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="1ff03-234">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="1ff03-235">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="1ff03-235">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="1ff03-236">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="1ff03-236">Better handling of threadgroup leader file descriptor cleanup.</span></span>
* <span data-ttu-id="1ff03-237">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="1ff03-237">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="1ff03-238">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="1ff03-238">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="1ff03-239">修复多个 AF_UNIX 相关问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="1ff03-239">Fix several AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="1ff03-240">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="1ff03-240">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>
* <span data-ttu-id="1ff03-241">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="1ff03-241">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="1ff03-242">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="1ff03-242">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="1ff03-243">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-243">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="1ff03-244">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="1ff03-244">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="1ff03-245">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="1ff03-245">Pipe filesystem inadvertently clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="1ff03-246">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="1ff03-246">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>
* <span data-ttu-id="1ff03-247">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="1ff03-247">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="1ff03-248">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="1ff03-248">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="1ff03-249">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="1ff03-249">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="1ff03-250">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="1ff03-250">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="1ff03-251">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="1ff03-251">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="1ff03-252">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="1ff03-252">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="1ff03-253">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="1ff03-253">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="1ff03-254">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-254">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="1ff03-255">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="1ff03-255">Windows UI apps should execute even when launched in the background.</span></span>
* <span data-ttu-id="1ff03-256">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="1ff03-256">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="1ff03-257">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="1ff03-257">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="1ff03-258">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="1ff03-258">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="1ff03-259">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="1ff03-259">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="1ff03-260">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="1ff03-260">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="1ff03-261">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-261">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="1ff03-262">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="1ff03-262">Add wslconfig /terminate to stop running distributions.</span></span>
* <span data-ttu-id="1ff03-263">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-263">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="1ff03-264">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="1ff03-264">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="1ff03-265">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="1ff03-265">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="1ff03-266">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-266">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="1ff03-267">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="1ff03-267">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>
* <span data-ttu-id="1ff03-268">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="1ff03-268">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="1ff03-269">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="1ff03-269">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="1ff03-270">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="1ff03-270">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="1ff03-271">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="1ff03-271">Atomically create case sensitive directories in DrvFs.</span></span>
* <span data-ttu-id="1ff03-272">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="1ff03-272">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="1ff03-273">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="1ff03-273">[GH 2712]</span></span>
* <span data-ttu-id="1ff03-274">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-274">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="1ff03-275">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="1ff03-275">[GH 3020]</span></span>
* <span data-ttu-id="1ff03-276">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-276">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="1ff03-277">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="1ff03-277">To use, hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="1ff03-278">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="1ff03-278">Fix Unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="1ff03-279">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-279">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="1ff03-280">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-280">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="1ff03-281">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-281">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="1ff03-282">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-282">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="1ff03-283">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="1ff03-283">Add --distribution option for wsl.exe to select a specific distro.</span></span>
* <span data-ttu-id="1ff03-284">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-284">Limited support for dmesg.</span></span> <span data-ttu-id="1ff03-285">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="1ff03-285">Applications can now log to dmesg.</span></span> <span data-ttu-id="1ff03-286">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="1ff03-286">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="1ff03-287">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-287">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="1ff03-288">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="1ff03-288">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="1ff03-289">尚不支持 `syslog` syscall 接口。</span><span class="sxs-lookup"><span data-stu-id="1ff03-289">`syslog` syscall interface is not yet supported.</span></span> <span data-ttu-id="1ff03-290">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-290">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="1ff03-291">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="1ff03-291">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="1ff03-292">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="1ff03-292">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="1ff03-293">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="1ff03-293">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="1ff03-294">不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="1ff03-294">Some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-18252-skip-ahead"></a><span data-ttu-id="1ff03-295">内部版本 18252 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="1ff03-295">Build 18252 (Skip Ahead)</span></span>
<span data-ttu-id="1ff03-296">有关内部版本 18252 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-296">For general Windows information on build 18252 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-297">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-297">WSL</span></span>
* <span data-ttu-id="1ff03-298">将 init 和 bsdtar 二进制文件移出 lxssmanager dll，移入单独的 tools 文件夹</span><span class="sxs-lookup"><span data-stu-id="1ff03-298">Move init and bsdtar binaries out of lxssmanager dll and into a separate tools folder</span></span>
* <span data-ttu-id="1ff03-299">修复在使用 CLONE_FILES 的情况下，关闭文件描述符时出现的争用</span><span class="sxs-lookup"><span data-stu-id="1ff03-299">Fix race around closing file descriptor when using CLONE_FILES</span></span>
* <span data-ttu-id="1ff03-300">处理转换 DrvFs 路径时 /proc/pid/mountinfo 中的可选字段</span><span class="sxs-lookup"><span data-stu-id="1ff03-300">Handle optional fields in /proc/pid/mountinfo when translating DrvFs paths</span></span>
* <span data-ttu-id="1ff03-301">允许 DrvFs mknod 成功，但不为 S_IFREG 提供元数据支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-301">Allow DrvFs mknod to succeed without metadata support for S_IFREG</span></span>
* <span data-ttu-id="1ff03-302">应为 DrvFs 上创建的只读文件设置只读属性 [GH 3411]</span><span class="sxs-lookup"><span data-stu-id="1ff03-302">Readonly files created on DrvFs should have the readonly attribute set [GH 3411]</span></span>
* <span data-ttu-id="1ff03-303">添加 /sbin/mount.drvfs 帮助器用于处理 DrvFs 装载</span><span class="sxs-lookup"><span data-stu-id="1ff03-303">Add /sbin/mount.drvfs helper to handle DrvFs mounting</span></span>
* <span data-ttu-id="1ff03-304">在 DrvFs 中使用 POSIX rename。</span><span class="sxs-lookup"><span data-stu-id="1ff03-304">Use POSIX rename in DrvFs.</span></span>
* <span data-ttu-id="1ff03-305">允许在无卷 GUID 的卷上执行路径转换。</span><span class="sxs-lookup"><span data-stu-id="1ff03-305">Allow path translation on volumes without a volume GUID.</span></span>

## <a name="build-17738-fast"></a><span data-ttu-id="1ff03-306">内部版本 17738 (Fast)</span><span class="sxs-lookup"><span data-stu-id="1ff03-306">Build 17738 (Fast)</span></span>
<span data-ttu-id="1ff03-307">有关内部版本 17738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-307">For general Windows information on build 17738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-308">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-308">WSL</span></span>
* <span data-ttu-id="1ff03-309">Setpriority syscall 权限检查过于严格，导致无法更改同一线程的优先级 [GH 1838]</span><span class="sxs-lookup"><span data-stu-id="1ff03-309">Setpriority syscall permission check too strict for changing same thread priority [GH 1838]</span></span>
* <span data-ttu-id="1ff03-310">确保对启动时间使用无偏差的中断时间，以避免返回 clock_gettime(CLOCK_BOOTTIME) 的负值 [GH 3434]</span><span class="sxs-lookup"><span data-stu-id="1ff03-310">Ensure that unbiased interrupt time is used for boot time to avoid returning negative values for clock_gettime(CLOCK_BOOTTIME) [GH 3434]</span></span>
* <span data-ttu-id="1ff03-311">在 WSL binfmt 解释器中处理符号链接 [GH 3424]</span><span class="sxs-lookup"><span data-stu-id="1ff03-311">Handle symlinks in the WSL binfmt interpreter [GH 3424]</span></span>
* <span data-ttu-id="1ff03-312">更好地处理线程组领先者文件描述符清理。</span><span class="sxs-lookup"><span data-stu-id="1ff03-312">Better handling of threadgroup leader file descriptor cleanup.</span></span>

## <a name="build-17728-fast"></a><span data-ttu-id="1ff03-313">内部版本 17728 (Fast)</span><span class="sxs-lookup"><span data-stu-id="1ff03-313">Build 17728 (Fast)</span></span>
<span data-ttu-id="1ff03-314">有关内部版本 17728 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-314">For general Windows information on build 17728 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-315">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-315">WSL</span></span>
* <span data-ttu-id="1ff03-316">切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter，以避免溢出 [GH 3252]</span><span class="sxs-lookup"><span data-stu-id="1ff03-316">Switch WSL to use KeQueryInterruptTimePrecise instead of KeQueryPerformanceCounter to avoid overflow [GH 3252]</span></span>
* <span data-ttu-id="1ff03-317">Ptrace attach 可能导致系统调用返回错误值 [GH 1731]</span><span class="sxs-lookup"><span data-stu-id="1ff03-317">Ptrace attach may cause bad return value from system calls [GH 1731]</span></span>
* <span data-ttu-id="1ff03-318">修复一些 AF_UNIX 相关的问题 [GH 3371]</span><span class="sxs-lookup"><span data-stu-id="1ff03-318">Fix a number of AF_UNIX related issues [GH 3371]</span></span>
* <span data-ttu-id="1ff03-319">修复以下问题：如果当前工作目录的长度少于 5 个字符，可能导致 WSL interop 失败 [GH 3379]</span><span class="sxs-lookup"><span data-stu-id="1ff03-319">Fix issue that could cause WSL interop to fail if the current working directory is less than 5 characters long [GH 3379]</span></span>

## <a name="build-18204-skip-ahead"></a><span data-ttu-id="1ff03-320">内部版本 18204 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="1ff03-320">Build 18204 (Skip Ahead)</span></span>
<span data-ttu-id="1ff03-321">有关内部版本 18204 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-321">For general Windows information on build 18204 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-322">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-322">WSL</span></span>
* <span data-ttu-id="1ff03-323">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="1ff03-323">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="1ff03-324">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="1ff03-324">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17723-fast"></a><span data-ttu-id="1ff03-325">内部版本 17723 (Fast)</span><span class="sxs-lookup"><span data-stu-id="1ff03-325">Build 17723 (Fast)</span></span>
<span data-ttu-id="1ff03-326">有关内部版本 17723 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-326">For general Windows information on build 17723 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-327">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-327">WSL</span></span>
* <span data-ttu-id="1ff03-328">避免导致无法与不存在的端口建立环回连接的一秒延迟 [GH 3286]</span><span class="sxs-lookup"><span data-stu-id="1ff03-328">Avoid one second delay failing loopback connections to non-existent ports [GH 3286]</span></span>
* <span data-ttu-id="1ff03-329">添加 /proc/sys/fs/file-max 存根文件 [GH 2893]</span><span class="sxs-lookup"><span data-stu-id="1ff03-329">Add /proc/sys/fs/file-max stub file [GH 2893]</span></span>
* <span data-ttu-id="1ff03-330">更准确的 IPV6 范围信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-330">More accurate IPV6 scope information.</span></span>
* <span data-ttu-id="1ff03-331">PR_SET_PTRACER 支持 [GH 3053]</span><span class="sxs-lookup"><span data-stu-id="1ff03-331">PR_SET_PTRACER support [GH 3053]</span></span>
* <span data-ttu-id="1ff03-332">管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]</span><span class="sxs-lookup"><span data-stu-id="1ff03-332">Pipe filesystem inadvertenly clearing edge-triggered epoll event [GH 3276]</span></span>
* <span data-ttu-id="1ff03-333">通过 NTFS 符号链接启动的 Win32 可执行文件不遵循符号链接命名约定 [GH 2909]</span><span class="sxs-lookup"><span data-stu-id="1ff03-333">Win32 executable launched via NTFS symlink doesn't respect symlink name [GH 2909]</span></span>

## <a name="build-17713"></a><span data-ttu-id="1ff03-334">内部版本 17713</span><span class="sxs-lookup"><span data-stu-id="1ff03-334">Build 17713</span></span>
<span data-ttu-id="1ff03-335">有关内部版本 17713 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-335">For general Windows information on build 17713 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-336">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-336">WSL</span></span>
* <span data-ttu-id="1ff03-337">改善了 zombie 支持 [GH 1353]</span><span class="sxs-lookup"><span data-stu-id="1ff03-337">Improved zombie support [GH 1353]</span></span>
* <span data-ttu-id="1ff03-338">添加 wsl.conf 项用于控制 Windows interop 行为 [GH 1493]</span><span class="sxs-lookup"><span data-stu-id="1ff03-338">Add wsl.conf entries for controlling Windows interop behavior [GH 1493]</span></span>
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* <span data-ttu-id="1ff03-339">修复 getsockname 不是始终返回 UNIX 套接字系列类型的问题 [GH 1774]</span><span class="sxs-lookup"><span data-stu-id="1ff03-339">Fix for getsockname not always returning UNIX socket family type [GH 1774]</span></span>
* <span data-ttu-id="1ff03-340">添加对 TIOCSTI 的支持 [GH 1863]</span><span class="sxs-lookup"><span data-stu-id="1ff03-340">Add support for TIOCSTI [GH 1863]</span></span>
* <span data-ttu-id="1ff03-341">连接进程中的非阻塞套接字应返回写入尝试的 EAGAIN [GH 2846]</span><span class="sxs-lookup"><span data-stu-id="1ff03-341">Non-blocking sockets in the process of connecting should return EAGAIN for write attempts [GH 2846]</span></span>
* <span data-ttu-id="1ff03-342">支持已装载的 VHD 上的 interop [GH 3246、3291]</span><span class="sxs-lookup"><span data-stu-id="1ff03-342">Support interop on mounted VHDs [GH 3246, 3291]</span></span>
* <span data-ttu-id="1ff03-343">修复根文件夹的权限检查问题 [GH 3304]</span><span class="sxs-lookup"><span data-stu-id="1ff03-343">Fix permission checking issue on root folder [GH 3304]</span></span>
* <span data-ttu-id="1ff03-344">对 TTY 键盘 ioctl KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-344">Limited support for TTY keyboard ioctls KDGKBTYPE, KDGKBMODE and KDSKBMODE.</span></span>
* <span data-ttu-id="1ff03-345">即使在后台启动，Windows UI 应用也应该能够执行。</span><span class="sxs-lookup"><span data-stu-id="1ff03-345">Windows UI apps should execute even when launched in the background.</span></span>

## <a name="build-17704"></a><span data-ttu-id="1ff03-346">内部版本 17704</span><span class="sxs-lookup"><span data-stu-id="1ff03-346">Build 17704</span></span>
<span data-ttu-id="1ff03-347">有关内部版本 17704 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-347">For general Windows information on build 17704 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-348">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-348">WSL</span></span>
* <span data-ttu-id="1ff03-349">添加 wsl -u 或 --user 选项 [GH 1203]</span><span class="sxs-lookup"><span data-stu-id="1ff03-349">Add wsl -u or --user option [GH 1203]</span></span>
* <span data-ttu-id="1ff03-350">修复启用快速启动时的 WSL 启动问题 [GH 2576]</span><span class="sxs-lookup"><span data-stu-id="1ff03-350">Fix WSL launch issues when fast startup is enabled [GH 2576]</span></span>
* <span data-ttu-id="1ff03-351">Unix 套接字需要保留断开连接的对等凭据 [GH 3183]</span><span class="sxs-lookup"><span data-stu-id="1ff03-351">Unix sockets need to retain disconnected peer credentials [GH 3183]</span></span>
* <span data-ttu-id="1ff03-352">使用 EAGAIN 时非阻塞 Unix 套接字无限期失败 [GH 3191]</span><span class="sxs-lookup"><span data-stu-id="1ff03-352">Non-blocking Unix sockets failing indefinitely with EAGAIN [GH 3191]</span></span>
* <span data-ttu-id="1ff03-353">case=off 是新的默认 drvfs 装入点类型 [GH 2937、3212、3328]</span><span class="sxs-lookup"><span data-stu-id="1ff03-353">case=off is the new default drvfs mount type [GH 2937, 3212, 3328]</span></span>
    * <span data-ttu-id="1ff03-354">有关详细信息，请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-354">See [blog](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/) for more information.</span></span>
* <span data-ttu-id="1ff03-355">添加 wslconfig/terminate 以停止正在运行的分发版。</span><span class="sxs-lookup"><span data-stu-id="1ff03-355">Add wslconfig /terminate to stop running distributions.</span></span>

## <a name="build-17692"></a><span data-ttu-id="1ff03-356">版本 17692</span><span class="sxs-lookup"><span data-stu-id="1ff03-356">Build 17692</span></span>
<span data-ttu-id="1ff03-357">有关内部版本 17692 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-357">For general Windows information on build 17692 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-358">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-358">WSL</span></span>
* <span data-ttu-id="1ff03-359">修复 WSL shell 上下文菜单项无法正确处理包含空格的路径的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-359">Fix issue with the WSL shell context menu entries that do not correctly handle paths with spaces.</span></span>
* <span data-ttu-id="1ff03-360">公开按目录区分大小写作为扩展属性</span><span class="sxs-lookup"><span data-stu-id="1ff03-360">Expose per-directory case sensitivity as an extended attribute</span></span>
* <span data-ttu-id="1ff03-361">ARM64：模拟缓存维护操作。</span><span class="sxs-lookup"><span data-stu-id="1ff03-361">ARM64: Emulate cache maintenance operations.</span></span> <span data-ttu-id="1ff03-362">解决 [.NET 问题](https://github.com/dotnet/core/issues/1561)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-362">Resolve [dotnet issue](https://github.com/dotnet/core/issues/1561).</span></span>
* <span data-ttu-id="1ff03-363">DrvFs：只取消转义专用范围中与已转义字符对应的字符。</span><span class="sxs-lookup"><span data-stu-id="1ff03-363">DrvFs: only unescape characters in the private range that correspond to an escaped character.</span></span>

## <a name="build-17686"></a><span data-ttu-id="1ff03-364">版本 17686</span><span class="sxs-lookup"><span data-stu-id="1ff03-364">Build 17686</span></span>
<span data-ttu-id="1ff03-365">有关内部版本 17686 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-365">For general Windows information on build 17686 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-366">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-366">WSL</span></span>
* <span data-ttu-id="1ff03-367">修复 ELF 分析程序解释器长度验证中的一位偏移错误 [GH 3154]</span><span class="sxs-lookup"><span data-stu-id="1ff03-367">Fix off-by-one error in ELF parser interpreter length validation [GH 3154]</span></span>
* <span data-ttu-id="1ff03-368">包含过去时间的 WSL 绝对计时器不会激发 [GH 3091]</span><span class="sxs-lookup"><span data-stu-id="1ff03-368">WSL absolute timers with a time in the past do not fire [GH 3091]</span></span>
* <span data-ttu-id="1ff03-369">确保新建的重分析点在父目录中以此类类型列出。</span><span class="sxs-lookup"><span data-stu-id="1ff03-369">Ensure newly created reparse points are listed as such in the parent directory.</span></span>
* <span data-ttu-id="1ff03-370">以原子方式在 DrvFs 中创建区分大小写的目录。</span><span class="sxs-lookup"><span data-stu-id="1ff03-370">Atomically create case sensitive directories in DrvFs.</span></span>

## <a name="build-17677"></a><span data-ttu-id="1ff03-371">内部版本 17677</span><span class="sxs-lookup"><span data-stu-id="1ff03-371">Build 17677</span></span>
<span data-ttu-id="1ff03-372">有关内部版本 17677 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-372">For general Windows information on build 17677 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-373">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-373">WSL</span></span>
* <span data-ttu-id="1ff03-374">修复一个附加的问题：即使文件存在，多线程操作也可能返回 ENOENT。</span><span class="sxs-lookup"><span data-stu-id="1ff03-374">Fixed an additional issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="1ff03-375">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="1ff03-375">[GH 2712]</span></span>
* <span data-ttu-id="1ff03-376">修复了启用 UMCI 时 WSL 启动失败的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-376">Fixed WSL launch failure when UMCI is enabled.</span></span> <span data-ttu-id="1ff03-377">[GH 3020]</span><span class="sxs-lookup"><span data-stu-id="1ff03-377">[GH 3020]</span></span>

## <a name="build-17666"></a><span data-ttu-id="1ff03-378">内部版本 17666</span><span class="sxs-lookup"><span data-stu-id="1ff03-378">Build 17666</span></span>
<span data-ttu-id="1ff03-379">有关内部版本 17666 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-379">For general Windows information on build 17666 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-380">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-380">WSL</span></span>
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a><span data-ttu-id="1ff03-381">警告：某个问题会阻止 WSL 在某些 AMD 芯片组上运行 [GH 3134]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-381">WARNING: There is an issue preventing WSL from running on some AMD chipsets [GH 3134].</span></span> <span data-ttu-id="1ff03-382">修复程序已准备就绪，即将在 Insider Build 分支中发布。</span><span class="sxs-lookup"><span data-stu-id="1ff03-382">A fix is ready and making its way to the Insider Build branch.</span></span>
* <span data-ttu-id="1ff03-383">添加浏览器上下文菜单用于启动 WSL [GH 437、603、1836]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-383">Add explorer context menu to launch WSL [GH 437, 603, 1836].</span></span> <span data-ttu-id="1ff03-384">若要使用此菜单，请在资源管理器窗口中按住 Shift 键的同时单击右键。</span><span class="sxs-lookup"><span data-stu-id="1ff03-384">To use hold shift and right-click when in an explorer window.</span></span>
* <span data-ttu-id="1ff03-385">修复 Unix 套接字非阻塞行为 [GH 2822、3100]</span><span class="sxs-lookup"><span data-stu-id="1ff03-385">Fix unix socket non-blocking behavior [GH 2822, 3100]</span></span>
* <span data-ttu-id="1ff03-386">修复 GH 2026 中报告的 NETLINK 命令挂起问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-386">Fix hanging NETLINK command as reported in GH 2026.</span></span>
* <span data-ttu-id="1ff03-387">添加对装载传播标志的支持 [GH 2911]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-387">Add support for mount propagation flags [GH 2911].</span></span>
* <span data-ttu-id="1ff03-388">修复截断后不会导致 inotify 事件的问题 [GH 2978]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-388">Fix issue with truncate not causing inotify events [GH 2978].</span></span>
* <span data-ttu-id="1ff03-389">为 wsl.exe 添加 --exec 选项，以便在不使用 shell 的情况下调用单个二进制文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-389">Add --exec option for wsl.exe to invoke a single binary without a shell.</span></span>
* <span data-ttu-id="1ff03-390">为 wsl.exe 添加 --distribution 选项，以选择特定的分发版。</span><span class="sxs-lookup"><span data-stu-id="1ff03-390">Add --distribution option for wsl.exe to select a specific distro.</span></span>

## <a name="build-17655-skip-ahead"></a><span data-ttu-id="1ff03-391">内部版本 17655 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="1ff03-391">Build 17655 (Skip Ahead)</span></span>
<span data-ttu-id="1ff03-392">有关内部版本 17655 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-392">For general Windows information on build 17655 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-393">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-393">WSL</span></span>
* <span data-ttu-id="1ff03-394">对 dmesg 的有限支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-394">Limited support for dmesg.</span></span> <span data-ttu-id="1ff03-395">现在，应用程序会将日志记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="1ff03-395">Applications can now log to dmesg.</span></span> <span data-ttu-id="1ff03-396">WSL 驱动程序会将有限的信息记录到 dmesg。</span><span class="sxs-lookup"><span data-stu-id="1ff03-396">WSL driver logs limited information to dmesg.</span></span> <span data-ttu-id="1ff03-397">将来，此功能可能会扩展，以便从驱动程序发送其他信息/诊断数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-397">In future, this can be extended to carry other information/diagnostics from the driver.</span></span>
    * <span data-ttu-id="1ff03-398">注意：目前通过 `/dev/kmsg` 设备接口支持 dmesg。</span><span class="sxs-lookup"><span data-stu-id="1ff03-398">Note: dmesg is currently supported through the `/dev/kmsg` device interface.</span></span> <span data-ttu-id="1ff03-399">尚不支持 `syslog` sycall 接口。</span><span class="sxs-lookup"><span data-stu-id="1ff03-399">`syslog` sycall interface is not yet supported.</span></span> <span data-ttu-id="1ff03-400">此外，某些 `dmesg` 命令行选项（例如 `-S`、`-C`）不起作用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-400">And, so, some of the `dmesg` command line options such as `-S`, `-C` don't work.</span></span>
* <span data-ttu-id="1ff03-401">修复了即使文件存在，多线程操作也可能返回 ENOENT 的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-401">Fixed an issue where multithreaded operations could return ENOENT even though the file exists.</span></span> <span data-ttu-id="1ff03-402">[GH 2712]</span><span class="sxs-lookup"><span data-stu-id="1ff03-402">[GH 2712]</span></span>

## <a name="build-17639-skip-ahead"></a><span data-ttu-id="1ff03-403">内部版本 17639 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="1ff03-403">Build 17639 (Skip Ahead)</span></span>
<span data-ttu-id="1ff03-404">有关内部版本 17639 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-404">For general Windows information on build 17639 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-405">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-405">WSL</span></span>
* <span data-ttu-id="1ff03-406">更改串行设备的默认 gid 和模式，以匹配本机 [GH 3042]</span><span class="sxs-lookup"><span data-stu-id="1ff03-406">Change default gid and mode of serial devices to match native [GH 3042]</span></span>
* <span data-ttu-id="1ff03-407">DrvFs 现在支持扩展属性。</span><span class="sxs-lookup"><span data-stu-id="1ff03-407">DrvFs now supports extended attributes.</span></span>
    * <span data-ttu-id="1ff03-408">注意：DrvFs 对扩展属性的名称施加一些限制。</span><span class="sxs-lookup"><span data-stu-id="1ff03-408">Note: DrvFs has some limitations on the name of extended attributes.</span></span> <span data-ttu-id="1ff03-409">具体而言，不允许使用某些字符（例如“/”、“:”和“\*”），并且扩展属性名称在 DrvFs 上不区分大小写</span><span class="sxs-lookup"><span data-stu-id="1ff03-409">In particular, some characters (like '/', ':' and '\*') are not allowed, and extended attribute names are not case sensitive on DrvFs</span></span>

## <a name="build-17133-fast"></a><span data-ttu-id="1ff03-410">内部版本 17133 (Fast)</span><span class="sxs-lookup"><span data-stu-id="1ff03-410">Build 17133 (Fast)</span></span>
<span data-ttu-id="1ff03-411">有关内部版本 17133 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-411">For general Windows information on build 17133 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-412">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-412">WSL</span></span>
* <span data-ttu-id="1ff03-413">修复 WSL 中的挂起问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-413">Fix for hang in WSL.</span></span> <span data-ttu-id="1ff03-414">[GH 3039、3034]</span><span class="sxs-lookup"><span data-stu-id="1ff03-414">[GH 3039, 3034]</span></span>

## <a name="build-17128-fast"></a><span data-ttu-id="1ff03-415">内部版本 17128 (Fast)</span><span class="sxs-lookup"><span data-stu-id="1ff03-415">Build 17128 (Fast)</span></span>
<span data-ttu-id="1ff03-416">有关内部版本 17128 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-416">For general Windows information on build 17128 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-417">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-417">WSL</span></span>
* <span data-ttu-id="1ff03-418">无</span><span class="sxs-lookup"><span data-stu-id="1ff03-418">None</span></span>

## <a name="build-17627-skip-ahead"></a><span data-ttu-id="1ff03-419">内部版本 17627 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="1ff03-419">Build 17627 (Skip Ahead)</span></span>
<span data-ttu-id="1ff03-420">有关内部版本 17627 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-420">For general Windows information on build 17627 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-421">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-421">WSL</span></span>
* <span data-ttu-id="1ff03-422">添加对 futex pi 感知操作的支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-422">Add support for the futex pi-aware operations.</span></span> <span data-ttu-id="1ff03-423">[GH 1006]</span><span class="sxs-lookup"><span data-stu-id="1ff03-423">[GH 1006]</span></span>
    * <span data-ttu-id="1ff03-424">请注意，WSL 功能目前不支持优先级，因此存在一些限制，但标准用法应该不会受到阻止。</span><span class="sxs-lookup"><span data-stu-id="1ff03-424">Note that priorities are not currently a supported WSL feature so there are limitations, but standard usage should be unblocked.</span></span>
* <span data-ttu-id="1ff03-425">对 WSL 进程的 Windows 防火墙支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-425">Windows firewall support for WSL processes.</span></span> <span data-ttu-id="1ff03-426">[GH 1852]</span><span class="sxs-lookup"><span data-stu-id="1ff03-426">[GH 1852]</span></span>
    * <span data-ttu-id="1ff03-427">例如，若要允许 WSL python 进程侦听任何端口，请使用提升的 Windows cmd：```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span><span class="sxs-lookup"><span data-stu-id="1ff03-427">For example, to allow the WSL python process to listen on any port, use the elevated Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```</span></span>
    * <span data-ttu-id="1ff03-428">有关如何添加防火墙规则的更多详细信息，请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span><span class="sxs-lookup"><span data-stu-id="1ff03-428">For additional details on how to add firewall rules, see [link](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)</span></span>
* <span data-ttu-id="1ff03-429">使用 wsl.exe 时遵循用户的默认 shell。</span><span class="sxs-lookup"><span data-stu-id="1ff03-429">Respect user's default shell when using wsl.exe.</span></span> <span data-ttu-id="1ff03-430">[GH 2372]</span><span class="sxs-lookup"><span data-stu-id="1ff03-430">[GH 2372]</span></span>
* <span data-ttu-id="1ff03-431">将所有网络接口报告为以太网。</span><span class="sxs-lookup"><span data-stu-id="1ff03-431">Report all network interfaces as ethernet.</span></span> <span data-ttu-id="1ff03-432">[GH 2996]</span><span class="sxs-lookup"><span data-stu-id="1ff03-432">[GH 2996]</span></span>
* <span data-ttu-id="1ff03-433">更好地处理损坏的 /etc/passwd 文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-433">Better handling of corrupt /etc/passwd file.</span></span> <span data-ttu-id="1ff03-434">[GH 3001]</span><span class="sxs-lookup"><span data-stu-id="1ff03-434">[GH 3001]</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-435">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-435">Console</span></span>
* <span data-ttu-id="1ff03-436">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-436">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-437">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-437">LTP Results:</span></span>
<span data-ttu-id="1ff03-438">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-438">Testing in progress.</span></span>

## <a name="build-17618-skip-ahead"></a><span data-ttu-id="1ff03-439">内部版本 17618 (Skip Ahead)</span><span class="sxs-lookup"><span data-stu-id="1ff03-439">Build 17618 (Skip Ahead)</span></span>
<span data-ttu-id="1ff03-440">有关内部版本 17618 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-440">For general Windows information on build 17618 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-441">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-441">WSL</span></span>
* <span data-ttu-id="1ff03-442">引入用于 NT interop 的伪控制台功能 [GH 988、1366、1433、1542、2370、2406]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-442">Introduce pseudoconsole functionality for NT interop [GH 988, 1366, 1433, 1542, 2370, 2406].</span></span>
* <span data-ttu-id="1ff03-443">传统的安装机制 (lxrun.exe) 已弃用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-443">The legacy install mechanism (lxrun.exe) has been deprecated.</span></span> <span data-ttu-id="1ff03-444">支持用于安装分发版的机制是 Microsoft Store。</span><span class="sxs-lookup"><span data-stu-id="1ff03-444">The supported mechanism for installing distributions is through the Microsoft Store.</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-445">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-445">Console</span></span>
* <span data-ttu-id="1ff03-446">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-446">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-447">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-447">LTP Results:</span></span>
<span data-ttu-id="1ff03-448">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-448">Testing in progress.</span></span>

## <a name="build-17110"></a><span data-ttu-id="1ff03-449">版本 17110</span><span class="sxs-lookup"><span data-stu-id="1ff03-449">Build 17110</span></span>
<span data-ttu-id="1ff03-450">有关内部版本 17110 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-450">For general Windows information on build 17110 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-451">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-451">WSL</span></span>
* <span data-ttu-id="1ff03-452">允许从 Windows 终止 /init [GH 2928]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-452">Allow /init to be terminated from Windows [GH 2928].</span></span>
* <span data-ttu-id="1ff03-453">现在，DrvFs 默认使用按目录区分大小写（相当于使用“case=dir”装载选项）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-453">DrvFs now uses per-directory case sensitivity by default (equivalent to the “case=dir” mount option).</span></span>
    * <span data-ttu-id="1ff03-454">使用“case=dir”（旧行为）需要设置注册表项。</span><span class="sxs-lookup"><span data-stu-id="1ff03-454">Using “case=force” (the old behavior) requires setting a registry key.</span></span> <span data-ttu-id="1ff03-455">如果需要使用“case=dir”，请运行以下命令来启用它：reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1</span><span class="sxs-lookup"><span data-stu-id="1ff03-455">Run the following command to enable “case=force” if you need to use it: reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1</span></span>
    * <span data-ttu-id="1ff03-456">如果在旧版 Windows 中使用 WSL 创建的现有目录需要区分大小写，请使用 fsutil.exe 将其标记为区分大小写：fsutil.exe file setcasesensitiveinfo <path> enable</span><span class="sxs-lookup"><span data-stu-id="1ff03-456">If you have existing directories created with WSL in older version of Windows which need to be case sensitive, use fsutil.exe to mark them as case sensitive: fsutil.exe file setcasesensitiveinfo <path> enable</span></span>
* <span data-ttu-id="1ff03-457">NULL 终止从 uname syscall 返回的字符串。</span><span class="sxs-lookup"><span data-stu-id="1ff03-457">NULL terminate strings returned from the uname syscall.</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-458">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-458">Console</span></span>
* <span data-ttu-id="1ff03-459">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-459">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-460">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-460">LTP Results:</span></span>
<span data-ttu-id="1ff03-461">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-461">Testing in progress.</span></span>

## <a name="build-17107"></a><span data-ttu-id="1ff03-462">内部版本 17107</span><span class="sxs-lookup"><span data-stu-id="1ff03-462">Build 17107</span></span>
<span data-ttu-id="1ff03-463">有关内部版本 17107 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-463">For general Windows information on build 17107 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-464">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-464">WSL</span></span>
* <span data-ttu-id="1ff03-465">支持主 pty 终结点上的 TCSETSF 和 TCSETSW [GH 2552]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-465">Support TCSETSF and TCSETSW on master pty endpoints [GH 2552].</span></span>
* <span data-ttu-id="1ff03-466">启动同步 interop 进程可能会导致 EINVAL [GH 2813]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-466">Starting simultaneous interop processes can result in EINVAL [GH 2813].</span></span>
* <span data-ttu-id="1ff03-467">修复 PTRACE_ATTACH 以在 /proc/pid/status 中显示正确的跟踪状态。</span><span class="sxs-lookup"><span data-stu-id="1ff03-467">Fix PTRACE_ATTACH to show proper tracing status in /proc/pid/status.</span></span>
* <span data-ttu-id="1ff03-468">修复以下争用问题：在不清除 TID 地址的情况下，通过 CLEARTID 和 SETTID 标志克隆的生存期较短的进程可能会退出。</span><span class="sxs-lookup"><span data-stu-id="1ff03-468">Fix race where short-lived processes cloned with both the CLEARTID and SETTID flags could exit without clearing the TID address.</span></span>
* <span data-ttu-id="1ff03-469">在从 17093 以前的内部版本迁移期间，升级 Linux 文件系统目录时会显示一条消息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-469">Display a message when upgrading the Linux file system directories when moving from a pre-17093 build.</span></span> <span data-ttu-id="1ff03-470">有关 17093 文件系统更改的更多详细信息，请参阅 [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093) 的发行说明。</span><span class="sxs-lookup"><span data-stu-id="1ff03-470">For more details on the 17093 file system changes, see the release notes for [17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093).</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-471">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-471">Console</span></span>
* <span data-ttu-id="1ff03-472">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-472">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-473">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-473">LTP Results:</span></span>
<span data-ttu-id="1ff03-474">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-474">Testing in progress.</span></span>

## <a name="build-17101"></a><span data-ttu-id="1ff03-475">内部版本 17101</span><span class="sxs-lookup"><span data-stu-id="1ff03-475">Build 17101</span></span>
<span data-ttu-id="1ff03-476">有关内部版本 17101 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-476">For general Windows information on build 17101 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-477">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-477">WSL</span></span>
* <span data-ttu-id="1ff03-478">signalfd 支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-478">Support for signalfd.</span></span> <span data-ttu-id="1ff03-479">[GH 129]</span><span class="sxs-lookup"><span data-stu-id="1ff03-479">[GH 129]</span></span>
* <span data-ttu-id="1ff03-480">支持包含非法 NTFS 字符的文件名，现在会将这些字符编码为专用 Unicode 字符。</span><span class="sxs-lookup"><span data-stu-id="1ff03-480">Support file-names containing illegal NTFS characters by encoding them as private Unicode characters.</span></span> <span data-ttu-id="1ff03-481">[GH 1514]</span><span class="sxs-lookup"><span data-stu-id="1ff03-481">[GH 1514]</span></span>
* <span data-ttu-id="1ff03-482">不支持写入时，自动装载将回退到只读。</span><span class="sxs-lookup"><span data-stu-id="1ff03-482">Auto mount will fallback to read-only when write is not supported.</span></span> <span data-ttu-id="1ff03-483">[GH 2603]</span><span class="sxs-lookup"><span data-stu-id="1ff03-483">[GH 2603]</span></span>
* <span data-ttu-id="1ff03-484">允许粘贴 Unicode 代理项对（类似于表情符号）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-484">Allow pasting of Unicode surrogate pairs (like emoji characters).</span></span> <span data-ttu-id="1ff03-485">[GH 2765]</span><span class="sxs-lookup"><span data-stu-id="1ff03-485">[GH 2765]</span></span>
* <span data-ttu-id="1ff03-486">/proc 和/sys 中的伪文件应从 select、poll、epoll 等命令返回 read 和 write ready [GH 2838]</span><span class="sxs-lookup"><span data-stu-id="1ff03-486">Pseudo-files in /proc and /sys should return read and write ready from select, poll, epoll, et al. [GH 2838]</span></span>
* <span data-ttu-id="1ff03-487">修复当注册表被篡改或损坏时，可能导致服务进入无限循环的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-487">Fix issue that could cause service to go into infinite loop when the registry has been tampered with or is corrupt.</span></span>
* <span data-ttu-id="1ff03-488">修复 netlink 消息，以便能够使用更新版本（上游 4.14）的 iproute2。</span><span class="sxs-lookup"><span data-stu-id="1ff03-488">Fix netlink messages to work with newer (upstream 4.14) version of iproute2.</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-489">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-489">Console</span></span>
* <span data-ttu-id="1ff03-490">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-490">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-491">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-491">LTP Results:</span></span>
<span data-ttu-id="1ff03-492">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-492">Testing in progress.</span></span>

## <a name="build-17093"></a><span data-ttu-id="1ff03-493">内部版本 17093</span><span class="sxs-lookup"><span data-stu-id="1ff03-493">Build 17093</span></span>
<span data-ttu-id="1ff03-494">有关内部版本 17093 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-494">For general Windows information on build 17093 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/).</span></span>

#### <a name="important"></a><span data-ttu-id="1ff03-495">重要提示：</span><span class="sxs-lookup"><span data-stu-id="1ff03-495">Important:</span></span>
<span data-ttu-id="1ff03-496">升级到此内部版本后，首次启动 WSL 时，需要执行一些操作来升级 Linux 文件系统目录。</span><span class="sxs-lookup"><span data-stu-id="1ff03-496">When starting WSL for the first time after upgrading to this build, it needs to perform some work upgrading the Linux file system directories.</span></span> <span data-ttu-id="1ff03-497">这可能需要几分钟时间，因此 WSL 的启动速度看上去可能很慢。</span><span class="sxs-lookup"><span data-stu-id="1ff03-497">This may take up to several minutes, so WSL may appear to start slowly.</span></span> <span data-ttu-id="1ff03-498">对于从 Store 安装的每个分发版，只需执行此操作一次。</span><span class="sxs-lookup"><span data-stu-id="1ff03-498">This should only happen once for each distribution you have installed from the store.</span></span>
* <span data-ttu-id="1ff03-499">改善了 DrvFs 中的区分大小写支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-499">Improved case sensitivity support in DrvFs.</span></span>
    * <span data-ttu-id="1ff03-500">DrvFs 现在支持按目录区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-500">DrvFs now supports per-directory case sensitivity.</span></span> <span data-ttu-id="1ff03-501">这是一个可对目录设置的新标志，用于指示应将这些目录中的所有操作视为区分大小写，使得 Windows 应用程序能够正确打开按大小写区分的文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-501">This is a new flag that can be set on directories to indicate all operations in those directories should be treated as case sensitive, which allows even Windows applications to correctly open files that differ only by case.</span></span>
    * <span data-ttu-id="1ff03-502">DrvFs 提供新的装载选项用于按目录控制区分大小写状态</span><span class="sxs-lookup"><span data-stu-id="1ff03-502">DrvFs has new mount options controlling case sensitivity on a per-directory basis</span></span>
        * <span data-ttu-id="1ff03-503">case=force：将所有目录视为区分大小写（驱动器根目录除外）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-503">case=force: all directories are treated as case sensitive (except for the drive root).</span></span> <span data-ttu-id="1ff03-504">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-504">New directories created with WSL are marked as case sensitive.</span></span> <span data-ttu-id="1ff03-505">这也是一种传统行为，不过，它会将新目录标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-505">This is the legacy behavior except for marking new directories case sensitive.</span></span>
        * <span data-ttu-id="1ff03-506">case=dir：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-506">case=dir: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="1ff03-507">使用 WSL 创建的新目录将标记为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-507">New directories created with WSL are marked as case sensitive.</span></span>
        * <span data-ttu-id="1ff03-508">case=off：只将带有按目录区分大小写标志的目录视为区分大小写；其他目录不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-508">case=off: only directories with the per-directory case sensitivity flag are treated as case sensitive; other directories are case insensitive.</span></span> <span data-ttu-id="1ff03-509">使用 WSL 创建的新目录将标记为不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-509">New directories created with WSL are marked as case insensitive.</span></span>
    * <span data-ttu-id="1ff03-510">注意：不会对旧版本中的 WSL 创建的目录设置此标志，因此，如果使用“case=dir”选项，则不会将这些目录视为区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-510">Note: directories created by WSL in previous releases do not have this flag set, so will not be treated as case sensitive if you use the “case=dir” option.</span></span> <span data-ttu-id="1ff03-511">即将推出一种对现有目录设置此标志的方法。</span><span class="sxs-lookup"><span data-stu-id="1ff03-511">A way to set this flag on existing directories is coming soon.</span></span>
    * <span data-ttu-id="1ff03-512">使用这些选项进行装载的示例（对于现有的驱动器，必须先卸载，然后才能使用不同选项装载）：sudo mount -t drvfs C: /mnt/c -o case=dir</span><span class="sxs-lookup"><span data-stu-id="1ff03-512">Example of mounting with these options (for existing drives, you must first unmount before you can mount with different options): sudo mount -t drvfs C: /mnt/c -o case=dir</span></span>
    * <span data-ttu-id="1ff03-513">目前，case=force 仍是默认选项。</span><span class="sxs-lookup"><span data-stu-id="1ff03-513">For now, case=force is still the default option.</span></span> <span data-ttu-id="1ff03-514">以后将更改为 case=dir。</span><span class="sxs-lookup"><span data-stu-id="1ff03-514">This will be changed to case=dir in the future.</span></span>
* <span data-ttu-id="1ff03-515">现在，在装载 DrvFs 时，可以在 Windows 路径中使用正斜杠，例如：sudo mount -t drvfs //server/share /mnt/share</span><span class="sxs-lookup"><span data-stu-id="1ff03-515">You can now use forward slashes in Windows paths when mounting DrvFs, e.g.: sudo mount -t drvfs //server/share /mnt/share</span></span>
* <span data-ttu-id="1ff03-516">WSL 现在会在实例启动期间处理 /etc/fstab 文件 [GH 2636]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-516">WSL now processes the /etc/fstab file during instance start [GH 2636].</span></span>
    * <span data-ttu-id="1ff03-517">这种处理是在自动装载 DrvFs 驱动器之前完成的；fstab 已装载的任何驱动器不会自动重新装载，使你可以更改特定驱动器的装入点。</span><span class="sxs-lookup"><span data-stu-id="1ff03-517">This is done prior to automatically mounting DrvFs drives; any drives that were already mounted by fstab will not be remounted automatically, allowing you to change the mount point for specific drives.</span></span>
    * <span data-ttu-id="1ff03-518">可以使用 wsl.conf 禁用此行为。</span><span class="sxs-lookup"><span data-stu-id="1ff03-518">This behavior can be turned off using wsl.conf.</span></span>
* <span data-ttu-id="1ff03-519">/proc 中的 mount、mountinfo 和 mountstats 文件会正确转义反斜杠和空格等特殊字符 [GH 2799]</span><span class="sxs-lookup"><span data-stu-id="1ff03-519">The mount, mountinfo and mountstats files in /proc properly escape special characters like backslashes and spaces [GH 2799]</span></span>
* <span data-ttu-id="1ff03-520">在启用元数据的情况下使用 DrvFs 创建的特殊文件（例如 WSL 符号链接，或 fifos 和 sockets）现在可以从 Windows 复制和移动。</span><span class="sxs-lookup"><span data-stu-id="1ff03-520">Special files created with DrvFs such as WSL symbolic links, or fifos and sockets when metadata is enabled, can now be copied and moved from Windows.</span></span>

#### <a name="wsl-is-more-configurable-with-wslconf"></a><span data-ttu-id="1ff03-521">可以使用 wsl.conf 更方便地配置 WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-521">WSL is more configurable with wsl.conf</span></span>
<span data-ttu-id="1ff03-522">我们添加了一个方法，用于自动配置 WSL 中每次启动子系统时要应用的某些功能。</span><span class="sxs-lookup"><span data-stu-id="1ff03-522">We added a method for you to automatically configure certain functionality in WSL that will be applied every time you launch the subsystem.</span></span> <span data-ttu-id="1ff03-523">这包括自动装载选项和网络配置。</span><span class="sxs-lookup"><span data-stu-id="1ff03-523">This includes automount options and network configuration.</span></span> <span data-ttu-id="1ff03-524">有关详细信息，请参阅博客文章： https://aka.ms/wslconf</span><span class="sxs-lookup"><span data-stu-id="1ff03-524">Learn more about it in our blog post at: https://aka.ms/wslconf</span></span>

#### <a name="af_unix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a><span data-ttu-id="1ff03-525">AF_UNIX 允许在 WSL 上的 Linux 进程与 Windows 本机进程之间建立套接字连接</span><span class="sxs-lookup"><span data-stu-id="1ff03-525">AF_UNIX allows socket connections between Linux processes on WSL and Windows native processes</span></span>
<span data-ttu-id="1ff03-526">现在，WSL 和 Windows 应用程序可以通过 Unix 套接字相互通信。</span><span class="sxs-lookup"><span data-stu-id="1ff03-526">WSL and Windows applications can now communicate with each other over Unix sockets.</span></span> <span data-ttu-id="1ff03-527">假设你要在 Windows 中运行某个服务，并使其可在 Windows 和 WSL 应用中使用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-527">Imagine you want to run a service in Windows and make it available to both Windows and WSL apps.</span></span> <span data-ttu-id="1ff03-528">现在可以通过 Unix 套接字实现此目的。</span><span class="sxs-lookup"><span data-stu-id="1ff03-528">Now, that’s possible with Unix sockets.</span></span> <span data-ttu-id="1ff03-529">有关详细信息，请参阅博客文章： https://aka.ms/afunixinterop</span><span class="sxs-lookup"><span data-stu-id="1ff03-529">Read more in our blog post at https://aka.ms/afunixinterop</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-530">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-530">WSL</span></span>
* <span data-ttu-id="1ff03-531">支持使用 MAP_NORESERVE 的 mmap() [GH 121、2784]</span><span class="sxs-lookup"><span data-stu-id="1ff03-531">Support mmap() with MAP_NORESERVE [GH 121, 2784]</span></span>
* <span data-ttu-id="1ff03-532">支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="1ff03-532">Support CLONE_PTRACE and CLONE_UNTRACED [GH 121, 2781]</span></span>
* <span data-ttu-id="1ff03-533">处理克隆中的非 SIGCHLD 终止信号 [GH 121、2781]</span><span class="sxs-lookup"><span data-stu-id="1ff03-533">Handle non-SIGCHLD termination signal in clone [GH 121, 2781]</span></span>
* <span data-ttu-id="1ff03-534">存根 /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]</span><span class="sxs-lookup"><span data-stu-id="1ff03-534">Stub /proc/sys/fs/inotify/max_user_instances and /proc/sys/fs/inotify/max_user_watches [GH 1705]</span></span>
* <span data-ttu-id="1ff03-535">加载包含偏移量非零的负载标头的 ELF 二进制文件时出错 [GH 1884]</span><span class="sxs-lookup"><span data-stu-id="1ff03-535">Error loading ELF binaries that contain load headers with non-zero offsets [GH 1884]</span></span>
* <span data-ttu-id="1ff03-536">加载映像时将尾随页字节归零。</span><span class="sxs-lookup"><span data-stu-id="1ff03-536">Zero out trailing page bytes when loading images.</span></span>
* <span data-ttu-id="1ff03-537">减少 execve 以静默方式终止进程的情况</span><span class="sxs-lookup"><span data-stu-id="1ff03-537">Reduce cases where execve silently terminates process</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-538">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-538">Console</span></span>
* <span data-ttu-id="1ff03-539">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-539">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-540">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-540">LTP Results:</span></span>
<span data-ttu-id="1ff03-541">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-541">Testing in progress.</span></span>

## <a name="build-17083"></a><span data-ttu-id="1ff03-542">版本 17083</span><span class="sxs-lookup"><span data-stu-id="1ff03-542">Build 17083</span></span>
<span data-ttu-id="1ff03-543">有关内部版本 17083 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-543">For general Windows information on build 17083 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-544">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-544">WSL</span></span>
* <span data-ttu-id="1ff03-545">修复了与 epoll 相关的 bug 检查 [GH 2798、2801、2857]</span><span class="sxs-lookup"><span data-stu-id="1ff03-545">Fixed bugcheck related to epoll [GH 2798, 2801, 2857]</span></span>
* <span data-ttu-id="1ff03-546">修复了关闭 ASLR 时挂起的问题 [GH 1185、2870]</span><span class="sxs-lookup"><span data-stu-id="1ff03-546">Fixed hangs when turning off ASLR [GH 1185, 2870]</span></span>
* <span data-ttu-id="1ff03-547">确保 mmap 操作显示原子性 [GH 2732]</span><span class="sxs-lookup"><span data-stu-id="1ff03-547">Ensure mmap operations appear atomic [GH 2732]</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-548">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-548">Console</span></span>
* <span data-ttu-id="1ff03-549">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-549">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-550">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-550">LTP Results:</span></span>
<span data-ttu-id="1ff03-551">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-551">Testing in progress.</span></span>

## <a name="build-17074"></a><span data-ttu-id="1ff03-552">内部版本 17074</span><span class="sxs-lookup"><span data-stu-id="1ff03-552">Build 17074</span></span>
<span data-ttu-id="1ff03-553">有关内部版本 17074 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-553">For general Windows information on build 17074 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-554">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-554">WSL</span></span>
* <span data-ttu-id="1ff03-555">固定了 DrvFs 元数据的存储格式 [GH 2777]</span><span class="sxs-lookup"><span data-stu-id="1ff03-555">Fixed storage format of DrvFs metadata [GH 2777]</span></span> </br>
<span data-ttu-id="1ff03-556">**重要说明：** 在此内部版本之前创建的 DrvFs 元数据将不正确地显示或根本不显示。</span><span class="sxs-lookup"><span data-stu-id="1ff03-556">**Important:** DrvFs metadata created before this build will show up incorrectly or not at all.</span></span> <span data-ttu-id="1ff03-557">若要修复受影响的文件，请使用 chmod 和 chown 重新应用元数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-557">To fix affected files, use chmod and chown to re-apply the metadata.</span></span>
* <span data-ttu-id="1ff03-558">修复了多个信号和可重启 syscall 的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-558">Fixed issue with multiple signals and restartable syscalls.</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-559">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-559">Console</span></span>
* <span data-ttu-id="1ff03-560">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-560">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-561">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-561">LTP Results:</span></span>
<span data-ttu-id="1ff03-562">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-562">Testing in progress.</span></span>

## <a name="build-17063"></a><span data-ttu-id="1ff03-563">内部版本 17063</span><span class="sxs-lookup"><span data-stu-id="1ff03-563">Build 17063</span></span>
<span data-ttu-id="1ff03-564">有关内部版本 17063 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-564">For general Windows information on build 17063 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/).</span></span>

### <a name="wsl"></a><span data-ttu-id="1ff03-565">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-565">WSL</span></span>
* <span data-ttu-id="1ff03-566">DrvFs 支持其他 Linux 元数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-566">DrvFs supports additional Linux metadata.</span></span> <span data-ttu-id="1ff03-567">这样，就可以使用 chmod/chown 设置文件的所有者和模式，并可以创建特殊文件，例如 fifos、Unix 套接字和设备文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-567">This allows setting the owner and mode of files using chmod/chown, and also the creation of special files such as fifos, unix sockets and device files.</span></span> <span data-ttu-id="1ff03-568">默认情况下，此功能暂时处于禁用状态，因为它仍是试验性的。</span><span class="sxs-lookup"><span data-stu-id="1ff03-568">This is disabled by default for now since it's still experimental.</span></span>
<span data-ttu-id="1ff03-569">**注意：** 修复了 DrvFs 使用的元数据格式的 bug。</span><span class="sxs-lookup"><span data-stu-id="1ff03-569">**Note:**  We fixed a bug in the metadata format used by DrvFs.</span></span> <span data-ttu-id="1ff03-570">尽管试验性的元数据可在此内部版本中正常工作，但将来的内部版本无法正确读取此内部版本创建的元数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-570">While metadata works on this build for experimentation, future builds will not correctly read metadata created by this build.</span></span>  <span data-ttu-id="1ff03-571">你可能需要手动更新已修改的文件的所有者，并且必须重新创建使用自定义设备 ID 的设备。</span><span class="sxs-lookup"><span data-stu-id="1ff03-571">You might need to manually update owner for modified files and devices with a custom device ID will have to be recreated.</span></span>

  <span data-ttu-id="1ff03-572">若要启用元数据，请使用 metadata 选项装载 DrvFs（若要在现有装入点上启用，必须先将其卸载）：</span><span class="sxs-lookup"><span data-stu-id="1ff03-572">To enable, mount DrvFs with the metadata option (to enable it on an existing mount, you must first unmount it):</span></span>

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  <span data-ttu-id="1ff03-573">Linux 权限将作为附加元数据添加到文件；它们不会影响 Windows 权限。</span><span class="sxs-lookup"><span data-stu-id="1ff03-573">Linux permissions are added as additional metadata to the file; they do not affect the Windows permissions.</span></span>  <span data-ttu-id="1ff03-574">请记住，使用 Windows 编辑器编辑文件可能会删除元数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-574">Remember, editing a file using a Windows editor may remove the metadata.</span></span> <span data-ttu-id="1ff03-575">在这种情况下，文件将还原为默认权限。</span><span class="sxs-lookup"><span data-stu-id="1ff03-575">In this case, the file will revert to its default permissions.</span></span>

* <span data-ttu-id="1ff03-576">已将 mount 选项添加到 DrvFs，用于控制不包含元数据的文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-576">Added mount options to DrvFs to control files without metadata.</span></span>
  * <span data-ttu-id="1ff03-577">uid：所有文件的所有者使用的用户 ID。</span><span class="sxs-lookup"><span data-stu-id="1ff03-577">uid: the user ID used for the owner of all files.</span></span>
  * <span data-ttu-id="1ff03-578">gid：所有文件的所有者使用的组 ID。</span><span class="sxs-lookup"><span data-stu-id="1ff03-578">gid: the group ID used for the owner of all files.</span></span>
  * <span data-ttu-id="1ff03-579">umask：要对所有文件和目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="1ff03-579">umask: an octal mask of permissions to exclude for all files and directories.</span></span>
  * <span data-ttu-id="1ff03-580">fmask：要对所有常规文件排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="1ff03-580">fmask: an octal mask of permissions to exclude for all regular files.</span></span>
  * <span data-ttu-id="1ff03-581">dmask：要对所有目录排除的权限的八进制掩码。</span><span class="sxs-lookup"><span data-stu-id="1ff03-581">dmask: an octal mask of permissions to exclude for all directories.</span></span>

  <span data-ttu-id="1ff03-582">例如：</span><span class="sxs-lookup"><span data-stu-id="1ff03-582">For example:</span></span>
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  <span data-ttu-id="1ff03-583">与 metadata 选项相结合可以指定不包含元数据的文件的默认权限。</span><span class="sxs-lookup"><span data-stu-id="1ff03-583">Combine with the metadata option to specify default permissions for files without metadata.</span></span>

* <span data-ttu-id="1ff03-584">引入了新的环境变量 `WSLENV`，用于配置环境变量在 WSL 与 Win32 之间的流动方式。</span><span class="sxs-lookup"><span data-stu-id="1ff03-584">Introduced a new environment variable, `WSLENV`, to configure how environment variables flow between WSL and Win32.</span></span>

  <span data-ttu-id="1ff03-585">例如：</span><span class="sxs-lookup"><span data-stu-id="1ff03-585">For example:</span></span>

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  <span data-ttu-id="1ff03-586">`WSLENV` 是在从 Win32 启动 WSL 进程或者从 WSL 启动 Win32 进程时可以包含的环境变量的冒号分隔列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-586">`WSLENV` is a colon-delimited list of environment variables that can be included when launching WSL processes from Win32 or Win32 processes from WSL.</span></span>  <span data-ttu-id="1ff03-587">每个变量可以使用斜杠后接一个用于指定其转换方式的标志作为后缀。</span><span class="sxs-lookup"><span data-stu-id="1ff03-587">Each variable can be suffixed with a slash followed by flags to specify how it is translated.</span></span>
  * <span data-ttu-id="1ff03-588">p：值是应在 WSL 路径与 Win32 路径之间进行转换的路径。</span><span class="sxs-lookup"><span data-stu-id="1ff03-588">p: The value is a path that should be translated between WSL paths and Win32 paths.</span></span>
  * <span data-ttu-id="1ff03-589">l：值是路径列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-589">l: The value is a list of paths.</span></span> <span data-ttu-id="1ff03-590">在 WSL 中，它是冒号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-590">In WSL, it is a colon-delimited list.</span></span> <span data-ttu-id="1ff03-591">在 Win32 中，它是分号分隔的列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-591">In Win32, it is a semicolon-delimited list.</span></span>
  * <span data-ttu-id="1ff03-592">u：仅当从 Win32 调用 WSL 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="1ff03-592">u: The value should only be included when invoking WSL from Win32</span></span>
  * <span data-ttu-id="1ff03-593">w：仅当从 WSL 调用 Win32 时才应该包含该值</span><span class="sxs-lookup"><span data-stu-id="1ff03-593">w: The value should only be included when invoking Win32 from WSL</span></span>

  <span data-ttu-id="1ff03-594">可以在 .bashrc 中或者在用户的自定义 Windows 环境中设置 `WSLENV`。</span><span class="sxs-lookup"><span data-stu-id="1ff03-594">You can set `WSLENV` in .bashrc or in the custom Windows environment for your user.</span></span>

* <span data-ttu-id="1ff03-595">drvfs 装入点会正确保留 tar、cp -p 中的时间戳 (GH 1939)</span><span class="sxs-lookup"><span data-stu-id="1ff03-595">drvfs mounts correctly preserves timestamps from tar, cp -p (GH 1939)</span></span>
* <span data-ttu-id="1ff03-596">drvfs 符号链接会报告正确的大小 (GH 2641)</span><span class="sxs-lookup"><span data-stu-id="1ff03-596">drvfs symlinks report the correct size (GH 2641)</span></span>
* <span data-ttu-id="1ff03-597">read/write 适用于极大的 IO 大小 (GH 2653)</span><span class="sxs-lookup"><span data-stu-id="1ff03-597">read/write works for very large IO sizes (GH 2653)</span></span>
* <span data-ttu-id="1ff03-598">waitpid 适用于进程组 ID (GH 2534)</span><span class="sxs-lookup"><span data-stu-id="1ff03-598">waitpid works with process group IDs (GH 2534)</span></span>
* <span data-ttu-id="1ff03-599">极大改善了大型保留区域的 mmap 性能；改善了 ghc 性能 (GH 1671)</span><span class="sxs-lookup"><span data-stu-id="1ff03-599">significantly improved mmap performance for large reserve regions; improves ghc performance (GH 1671)</span></span>
* <span data-ttu-id="1ff03-600">READ_IMPLIES_EXEC 的个性化支持；修复 maxima 和 clisp (GH 1185)</span><span class="sxs-lookup"><span data-stu-id="1ff03-600">personality supports for READ_IMPLIES_EXEC; fixes maxima and clisp (GH 1185)</span></span>
* <span data-ttu-id="1ff03-601">mprotect 支持 PROT_GROWSDOWN；修复 clisp (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="1ff03-601">mprotect supports PROT_GROWSDOWN; fixes clisp (GH 1128)</span></span>
* <span data-ttu-id="1ff03-602">overcommit 模式的页面错误修复；修复 sbcl (GH 1128)</span><span class="sxs-lookup"><span data-stu-id="1ff03-602">page fault fixes in overcommit mode; fixes sbcl (GH 1128)</span></span>
* <span data-ttu-id="1ff03-603">clone 支持更多标志组合</span><span class="sxs-lookup"><span data-stu-id="1ff03-603">clone supports more flags combinations</span></span>
* <span data-ttu-id="1ff03-604">支持 epoll 文件的 select/epoll（以前为 no-op）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-604">Support select/epoll of epoll files (previously a no-op).</span></span>
* <span data-ttu-id="1ff03-605">通知未实现的 syscall 的 ptrace。</span><span class="sxs-lookup"><span data-stu-id="1ff03-605">Notify ptrace of unimplemented syscalls.</span></span>
* <span data-ttu-id="1ff03-606">忽略生成 resolv.conf 名称服务器时不启动的接口 [GH 2694]</span><span class="sxs-lookup"><span data-stu-id="1ff03-606">Ignore interfaces that are not up when generating resolv.conf nameservers [GH 2694]</span></span>
* <span data-ttu-id="1ff03-607">枚举没有物理地址的网络接口。</span><span class="sxs-lookup"><span data-stu-id="1ff03-607">Enumerate network interfaces with no physical address.</span></span> <span data-ttu-id="1ff03-608">[GH 2685]</span><span class="sxs-lookup"><span data-stu-id="1ff03-608">[GH 2685]</span></span>
* <span data-ttu-id="1ff03-609">其他 bug 修复和改进。</span><span class="sxs-lookup"><span data-stu-id="1ff03-609">Additional bug fixes and improvements.</span></span>

### <a name="linux-tools-available-to-developers-on-windows"></a><span data-ttu-id="1ff03-610">适用于 Windows 上的开发人员的 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="1ff03-610">Linux tools available to developers on Windows</span></span>

* <span data-ttu-id="1ff03-611">Windows 命令行工具链包括 bsdtar (tar) 和 curl。</span><span class="sxs-lookup"><span data-stu-id="1ff03-611">Windows Command line Toolchain includes bsdtar (tar) and curl.</span></span>
  <span data-ttu-id="1ff03-612">请阅读[此博客](https://aka.ms/tarcurlwindows)来详细了解如何添加这两个新工具，以及它们如何打造 Windows 上的开发人员体验。</span><span class="sxs-lookup"><span data-stu-id="1ff03-612">Read [this blog](https://aka.ms/tarcurlwindows) to learn more about the addition of these two new tools and see how they’re shaping the developer experience on Windows.</span></span>

*   <span data-ttu-id="1ff03-613">`AF_UNIX` 适用于 Windows 预览体验成员 SDK (17061+)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-613">`AF_UNIX` is available in the Windows Insider SDK (17061+).</span></span>
  <span data-ttu-id="1ff03-614">请阅读[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)来详细了解 `AF_UNIX`，以及 Windows 上的开发人员如何使用它。</span><span class="sxs-lookup"><span data-stu-id="1ff03-614">Read [this blog](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/) to learn more about `AF_UNIX` and how developers on Windows can use it.</span></span>

### <a name="console"></a><span data-ttu-id="1ff03-615">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-615">Console</span></span>
* <span data-ttu-id="1ff03-616">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-616">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-617">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-617">LTP Results:</span></span>
<span data-ttu-id="1ff03-618">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-618">Testing in progress.</span></span>


## <a name="build-17046"></a><span data-ttu-id="1ff03-619">内部版本 17046</span><span class="sxs-lookup"><span data-stu-id="1ff03-619">Build 17046</span></span>

<span data-ttu-id="1ff03-620">有关内部版本 17046 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-620">For general Windows information on build 17046 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc).</span></span>

### <a name="fixed"></a><span data-ttu-id="1ff03-621">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-621">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-622">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-622">WSL</span></span>
- <span data-ttu-id="1ff03-623">允许进程在没有活动终端的情况下运行。</span><span class="sxs-lookup"><span data-stu-id="1ff03-623">Allow processes to run without an active terminal.</span></span> <span data-ttu-id="1ff03-624">[GH 709、1007、1511、2252、2391 等]</span><span class="sxs-lookup"><span data-stu-id="1ff03-624">[GH 709, 1007, 1511, 2252, 2391, et al.]</span></span>
- <span data-ttu-id="1ff03-625">更好地支持 CLONE_VFORK 和 CLONE_VM。</span><span class="sxs-lookup"><span data-stu-id="1ff03-625">Better support of CLONE_VFORK and CLONE_VM.</span></span> <span data-ttu-id="1ff03-626">[GH 1878、2615]</span><span class="sxs-lookup"><span data-stu-id="1ff03-626">[GH 1878, 2615]</span></span>
- <span data-ttu-id="1ff03-627">跳过 WSL 网络操作的 TDI 筛选器驱动程序。</span><span class="sxs-lookup"><span data-stu-id="1ff03-627">Skip TDI filter drivers for WSL networking operations.</span></span> <span data-ttu-id="1ff03-628">[GH 1554]</span><span class="sxs-lookup"><span data-stu-id="1ff03-628">[GH 1554]</span></span>
- <span data-ttu-id="1ff03-629">在满足特定的条件时，DrvFs 将创建 NT 符号链接。</span><span class="sxs-lookup"><span data-stu-id="1ff03-629">DrvFs creates NT symlinks when certain conditions are met.</span></span> <span data-ttu-id="1ff03-630">[GH 353、1475、2602]</span><span class="sxs-lookup"><span data-stu-id="1ff03-630">[GH 353, 1475, 2602]</span></span>
    - <span data-ttu-id="1ff03-631">链接目标必须是相对性的，不能跨任何装入点或符号链接，并且必须存在。</span><span class="sxs-lookup"><span data-stu-id="1ff03-631">The link target must be relative, must not cross any mount points or symlinks, and must exist.</span></span>
    - <span data-ttu-id="1ff03-632">除非已启用开发人员模式，否则用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE（这通常需要以提升的权限启动 wsl.exe）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-632">The user must have SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (this normally requires you to launch wsl.exe elevated), unless Developer Mode is turned on.</span></span>
    - <span data-ttu-id="1ff03-633">在所有其他情况下，DrvFs 仍会创建 WSL 符号链接。</span><span class="sxs-lookup"><span data-stu-id="1ff03-633">In all other situations, DrvFs still creates WSL symlinks.</span></span>
- <span data-ttu-id="1ff03-634">允许同时运行提升和未提升的 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="1ff03-634">Allow running elevated and non-elevated WSL instances simultaneously.</span></span>
- <span data-ttu-id="1ff03-635">支持 /proc/sys/kernel/yama/ptrace_scope</span><span class="sxs-lookup"><span data-stu-id="1ff03-635">Support /proc/sys/kernel/yama/ptrace_scope</span></span>
- <span data-ttu-id="1ff03-636">添加 wslpath 用于执行 WSL<->Windows 路径转换。</span><span class="sxs-lookup"><span data-stu-id="1ff03-636">Add wslpath to do WSL<->Windows path conversions.</span></span> <span data-ttu-id="1ff03-637">[GH 522、1243、1834、2327 等]</span><span class="sxs-lookup"><span data-stu-id="1ff03-637">[GH 522, 1243, 1834, 2327, et al.]</span></span>
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a><span data-ttu-id="1ff03-638">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-638">Console</span></span>
- <span data-ttu-id="1ff03-639">无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-639">No fixes.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-640">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-640">LTP Results:</span></span>
<span data-ttu-id="1ff03-641">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-641">Testing in progress.</span></span>


## <a name="build-17040"></a><span data-ttu-id="1ff03-642">内部版本 17040</span><span class="sxs-lookup"><span data-stu-id="1ff03-642">Build 17040</span></span>

<span data-ttu-id="1ff03-643">有关内部版本 17040 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-643">For general Windows information on build 17040 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-644">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-644">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-645">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-645">WSL</span></span>
- <span data-ttu-id="1ff03-646">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-646">No fixes since 17035.</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-647">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-647">Console</span></span>
- <span data-ttu-id="1ff03-648">自 17035 以来无修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-648">No fixes since 17035.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-649">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-649">LTP Results:</span></span>
<span data-ttu-id="1ff03-650">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-650">Testing in progress.</span></span>

## <a name="build-17035"></a><span data-ttu-id="1ff03-651">内部版本 17035</span><span class="sxs-lookup"><span data-stu-id="1ff03-651">Build 17035</span></span>

<span data-ttu-id="1ff03-652">有关内部版本 17035 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-652">For general Windows information on build 17035 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-653">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-653">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-654">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-654">WSL</span></span>
- <span data-ttu-id="1ff03-655">访问 DrvFs 上的文件偶尔会失败并出现 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="1ff03-655">Accessing files on DrvFs could occasionally fail with EINVAL.</span></span> <span data-ttu-id="1ff03-656">[GH 2448]</span><span class="sxs-lookup"><span data-stu-id="1ff03-656">[GH 2448]</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-657">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-657">Console</span></span>
- <span data-ttu-id="1ff03-658">在 VT 模式下插入/删除行时丢失一些颜色。</span><span class="sxs-lookup"><span data-stu-id="1ff03-658">Some color loss when inserting/deleting lines in VT mode.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-659">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-659">LTP Results:</span></span>
<span data-ttu-id="1ff03-660">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-660">Testing in progress.</span></span>

## <a name="build-17025"></a><span data-ttu-id="1ff03-661">内部版本 17025</span><span class="sxs-lookup"><span data-stu-id="1ff03-661">Build 17025</span></span>

<span data-ttu-id="1ff03-662">有关内部版本 17025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-662">For general Windows information on build 17025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-663">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-663">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-664">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-664">WSL</span></span>
- <span data-ttu-id="1ff03-665">在新的前台进程组中启动初始进程 [GH 1653、2510]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-665">Start initial processes in a new foreground process group [GH 1653, 2510].</span></span>
- <span data-ttu-id="1ff03-666">SIGHUP 传递修复 [GH 2496]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-666">SIGHUP delivery fixes [GH 2496].</span></span>
- <span data-ttu-id="1ff03-667">如果未提供虚拟网桥名称，将生成默认名称 [GH 2497]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-667">Generate default virtual bridge name if none provided [GH 2497].</span></span>
- <span data-ttu-id="1ff03-668">实现 /proc/sys/kernel/random/boot_id [GH 2518]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-668">Implement /proc/sys/kernel/random/boot_id [GH 2518].</span></span>
- <span data-ttu-id="1ff03-669">更多 interop stdout/stderr 管道修复措施。</span><span class="sxs-lookup"><span data-stu-id="1ff03-669">More interop stdout/stderr pipe fixes.</span></span>
- <span data-ttu-id="1ff03-670">存根 syncfs 系统调用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-670">Stub syncfs system call.</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-671">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-671">Console</span></span>
- <span data-ttu-id="1ff03-672">修复第三方控制台的输入 VT 转换 [GH 111]</span><span class="sxs-lookup"><span data-stu-id="1ff03-672">Fix input VT translation for third party consoles [GH 111]</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-673">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-673">LTP Results:</span></span>
<span data-ttu-id="1ff03-674">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-674">Testing in progress.</span></span>

## <a name="build-17017"></a><span data-ttu-id="1ff03-675">内部版本 17017</span><span class="sxs-lookup"><span data-stu-id="1ff03-675">Build 17017</span></span>

<span data-ttu-id="1ff03-676">有关内部版本 17017 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-676">For general Windows information on build 17017 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-677">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-677">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-678">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-678">WSL</span></span>
- <span data-ttu-id="1ff03-679">忽略空的 ELF 程序标头 [GH 330]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-679">Ignore empty ELF program headers [GH 330].</span></span>
- <span data-ttu-id="1ff03-680">允许 LxssManager 为非交互式用户创建 WSL 实例（ssh 和计划任务支持）[GH 777、1602]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-680">Allow LxssManager to create WSL instances for non-interactive users (ssh and scheduled task support) [GH 777, 1602].</span></span>
- <span data-ttu-id="1ff03-681">支持 WSL->Win32->WSL（“起始”）方案 [GH 1228]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-681">Support WSL->Win32->WSL ("inception") scenarios [GH 1228].</span></span>
- <span data-ttu-id="1ff03-682">有限支持终止通过 interop 调用的控制台应用 [GH 1614]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-682">Limited support for termination of console apps invoked via interop [GH 1614].</span></span>
- <span data-ttu-id="1ff03-683">支持 devpts 的装载选项 [GH 1948]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-683">Support mount options for devpts [GH 1948].</span></span>
- <span data-ttu-id="1ff03-684">Ptrace 阻止子级启动 [GH 2333]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-684">Ptrace blocking child startup [GH 2333].</span></span>
- <span data-ttu-id="1ff03-685">EPOLLET 缺少某些事件 [GH 2462]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-685">EPOLLET missing some events [GH 2462].</span></span>
- <span data-ttu-id="1ff03-686">返回 PTRACE_GETSIGINFO 的更多数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-686">Return more data for PTRACE_GETSIGINFO.</span></span>
- <span data-ttu-id="1ff03-687">结合 lseek 运行 Getdents 会提供错误的结果。</span><span class="sxs-lookup"><span data-stu-id="1ff03-687">Getdents with lseek gives incorrect results.</span></span>
- <span data-ttu-id="1ff03-688">修复某些 Win32 interop 应用挂起，并等待在没有更多数据的管道中提供输入的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-688">Fix some Win32 interop app hangs, waiting for input on a pipe that has no more data.</span></span>
- <span data-ttu-id="1ff03-689">tty/pty 文件的 O_ASYNC 支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-689">O_ASYNC support for tty/pty files.</span></span>
- <span data-ttu-id="1ff03-690">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-690">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-691">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-691">Console</span></span>
- <span data-ttu-id="1ff03-692">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-692">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-693">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-693">LTP Results:</span></span>
<span data-ttu-id="1ff03-694">正在测试。</span><span class="sxs-lookup"><span data-stu-id="1ff03-694">Testing in progress.</span></span>

## <a name="fall-creators-update"></a><span data-ttu-id="1ff03-695">Fall Creators Update</span><span class="sxs-lookup"><span data-stu-id="1ff03-695">Fall Creators Update</span></span>

## <a name="build-16288"></a><span data-ttu-id="1ff03-696">内部版本 16288</span><span class="sxs-lookup"><span data-stu-id="1ff03-696">Build 16288</span></span>

<span data-ttu-id="1ff03-697">有关内部版本 16288 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-697">For general Windows information on build 16288 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-698">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-698">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-699">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-699">WSL</span></span>
- <span data-ttu-id="1ff03-700">正确初始化和报告套接字文件描述符的 uid、gid 和模式 [GH 2490]</span><span class="sxs-lookup"><span data-stu-id="1ff03-700">Correctly initialize and report uid, gid, and mode for socket file descriptors [GH 2490]</span></span>
- <span data-ttu-id="1ff03-701">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-701">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-702">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-702">Console</span></span>
- <span data-ttu-id="1ff03-703">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-703">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-704">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-704">LTP Results:</span></span>
<span data-ttu-id="1ff03-705">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-705">No change since 16273</span></span>

## <a name="build-16278"></a><span data-ttu-id="1ff03-706">内部版本 16278</span><span class="sxs-lookup"><span data-stu-id="1ff03-706">Build 16278</span></span>

<span data-ttu-id="1ff03-707">有关内部版本 162738 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-707">For general Windows information on build 162738 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-708">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-708">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-709">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-709">WSL</span></span>
- <span data-ttu-id="1ff03-710">分解 LX MM 状态时显式取消映射文件后备节的映射视图 [GH 2415]</span><span class="sxs-lookup"><span data-stu-id="1ff03-710">Explicitly unmap mapped views of file backed sections when tearing down LX MM state [GH 2415]</span></span>
- <span data-ttu-id="1ff03-711">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-711">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-712">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-712">Console</span></span>
- <span data-ttu-id="1ff03-713">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-713">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-714">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-714">LTP Results:</span></span>
<span data-ttu-id="1ff03-715">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-715">No change since 16273</span></span>

## <a name="build-16275"></a><span data-ttu-id="1ff03-716">内部版本 16275</span><span class="sxs-lookup"><span data-stu-id="1ff03-716">Build 16275</span></span>

<span data-ttu-id="1ff03-717">有关内部版本 162735 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-717">For general Windows information on build 162735 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-718">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-718">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-719">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-719">WSL</span></span>
- <span data-ttu-id="1ff03-720">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-720">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-721">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-721">Console</span></span>
- <span data-ttu-id="1ff03-722">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-722">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-723">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-723">LTP Results:</span></span>
<span data-ttu-id="1ff03-724">自 16273 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-724">No change since 16273</span></span>

## <a name="build-16273"></a><span data-ttu-id="1ff03-725">内部版本 16273</span><span class="sxs-lookup"><span data-stu-id="1ff03-725">Build 16273</span></span>

<span data-ttu-id="1ff03-726">有关内部版本 16273 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-726">For general Windows information on build 16273 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-727">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-727">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-728">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-728">WSL</span></span>
- <span data-ttu-id="1ff03-729">修复了 DrvFs 有时报告目录的错误文件类型的问题 [GH 2392]</span><span class="sxs-lookup"><span data-stu-id="1ff03-729">Fixed an issue where DrvFs sometimes reported the wrong file type for directories [GH 2392]</span></span>
- <span data-ttu-id="1ff03-730">允许创建 NETLINK_KOBJECT_UEVENT 套接字来取消阻止使用 UEVENT 的程序 [GH 1121、2293、2242、2295、2235、648、637]</span><span class="sxs-lookup"><span data-stu-id="1ff03-730">Allow creation of NETLINK_KOBJECT_UEVENT sockets to unblock programs that use uevent [GH 1121, 2293, 2242, 2295, 2235, 648, 637]</span></span>
- <span data-ttu-id="1ff03-731">添加对非阻塞连接的支持 [GH 903、1391、1584、1585、1829、2290、2314]</span><span class="sxs-lookup"><span data-stu-id="1ff03-731">Add support for non-blocking connect [GH 903, 1391, 1584, 1585, 1829, 2290, 2314]</span></span>
- <span data-ttu-id="1ff03-732">实现 CLONE_FS 克隆系统调用标志 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="1ff03-732">Implement CLONE_FS clone system call flag [GH 2242]</span></span>
- <span data-ttu-id="1ff03-733">修复有关在 NT interop 中不会正确处理制表符或引号的问题 [GH 1625、2164]</span><span class="sxs-lookup"><span data-stu-id="1ff03-733">Fix issues around not handling tabs or quotes correctly in NT interop [GH 1625, 2164]</span></span>
- <span data-ttu-id="1ff03-734">解决尝试重新启动 WSL 实例时发生的拒绝访问错误 [GH 651、2095]</span><span class="sxs-lookup"><span data-stu-id="1ff03-734">Resolve access denied error when trying to re-launch WSL instances [GH 651, 2095]</span></span>
- <span data-ttu-id="1ff03-735">实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]</span><span class="sxs-lookup"><span data-stu-id="1ff03-735">Implement futex FUTEX_REQUEUE and FUTEX_CMP_REQUEUE operations [GH 2242]</span></span>
- <span data-ttu-id="1ff03-736">修复各种 SysFs 文件的权限 [GH 2214]</span><span class="sxs-lookup"><span data-stu-id="1ff03-736">Fix permissions for various SysFs files [GH 2214]</span></span>
- <span data-ttu-id="1ff03-737">修复设置过程中 Haskell 堆栈挂起的问题 [GH 2290]</span><span class="sxs-lookup"><span data-stu-id="1ff03-737">Fix Haskell stack hang during setup [GH 2290]</span></span>
- <span data-ttu-id="1ff03-738">实现 binfmt_misc“C”、“O”和“P”标志 [GH 2103]</span><span class="sxs-lookup"><span data-stu-id="1ff03-738">Implement binfmt_misc 'C' 'O' and 'P' flags [GH 2103]</span></span>
- <span data-ttu-id="1ff03-739">添加 /proc/sys/kernel /shmmax /shmmni 和 /threads-max [GH 1753]</span><span class="sxs-lookup"><span data-stu-id="1ff03-739">Add /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]</span></span>
- <span data-ttu-id="1ff03-740">添加对 ioprio_set 系统调用的部分支持 [GH 498]</span><span class="sxs-lookup"><span data-stu-id="1ff03-740">Add partial support for ioprio_set system call [GH 498]</span></span>
- <span data-ttu-id="1ff03-741">存根 SO_REUSEPORT 和添加 netlink 套接字的 SO_PASSCRED 支持 [GH 69]</span><span class="sxs-lookup"><span data-stu-id="1ff03-741">Stub SO_REUSEPORT & adding support for SO_PASSCRED for netlink sockets [GH 69]</span></span>
- <span data-ttu-id="1ff03-742">如果当前正在安装或卸载分发版，将从 RegisterDistribuiton 返回不同的错误代码。</span><span class="sxs-lookup"><span data-stu-id="1ff03-742">Return different error codes from RegisterDistribuiton if a distribution is currently being installed or uninstalled.</span></span>
- <span data-ttu-id="1ff03-743">允许通过 wslconfig.exe 取消注册部分安装的 WSL 分发版</span><span class="sxs-lookup"><span data-stu-id="1ff03-743">Allow unregistration of partially installed WSL distributions via wslconfig.exe</span></span>
- <span data-ttu-id="1ff03-744">修复 udp::msg_peek 的 python 套接字测试挂起问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-744">Fix python socket test hang from udp::msg_peek</span></span>
- <span data-ttu-id="1ff03-745">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-745">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-746">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-746">Console</span></span>
- <span data-ttu-id="1ff03-747">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-747">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-748">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-748">LTP Results:</span></span>
<span data-ttu-id="1ff03-749">测试总数：1904</span><span class="sxs-lookup"><span data-stu-id="1ff03-749">Total Tests: 1904</span></span><br/>
<span data-ttu-id="1ff03-750">跳过的测试总数：209</span><span class="sxs-lookup"><span data-stu-id="1ff03-750">Total Skipped Tests: 209</span></span><br/>
<span data-ttu-id="1ff03-751">失败总数：229</span><span class="sxs-lookup"><span data-stu-id="1ff03-751">Total Failures: 229</span></span><br/>
[<span data-ttu-id="1ff03-752">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-752">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a><span data-ttu-id="1ff03-753">版本 16257</span><span class="sxs-lookup"><span data-stu-id="1ff03-753">Build 16257</span></span>

<span data-ttu-id="1ff03-754">有关内部版本 16257 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-754">For general Windows information on build 16257 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-755">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-755">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-756">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-756">WSL</span></span>
- <span data-ttu-id="1ff03-757">实现 prlimit64 系统调用</span><span class="sxs-lookup"><span data-stu-id="1ff03-757">Implement prlimit64 system call</span></span>
- <span data-ttu-id="1ff03-758">添加对 ulimit -n 的支持 (setrlimit RLIMIT_NOFILE) [GH 1688]</span><span class="sxs-lookup"><span data-stu-id="1ff03-758">Add support for ulimit -n (setrlimit RLIMIT_NOFILE) [GH 1688]</span></span>
- <span data-ttu-id="1ff03-759">TCP 套接字的存根 MSG_MORE [GH 2351]</span><span class="sxs-lookup"><span data-stu-id="1ff03-759">Stub MSG_MORE for TCP sockets [GH 2351]</span></span>
- <span data-ttu-id="1ff03-760">修复无效的 AT_EXECFN 辅助矢量行为 [GH 2133]</span><span class="sxs-lookup"><span data-stu-id="1ff03-760">Fix invalid AT_EXECFN auxiliary vector behavior [GH 2133]</span></span>
- <span data-ttu-id="1ff03-761">修复 console/tty 的 copy/paste 行为，并添加更适当的完整缓冲区处理 [GH 2204、2131]</span><span class="sxs-lookup"><span data-stu-id="1ff03-761">Fix copy/paste behavior for console/tty, and add better full buffer handling [GH 2204, 2131]</span></span>
- <span data-ttu-id="1ff03-762">在 set-user-ID 和 set-group-ID 程序的辅助矢量中设置 AT_SECURE [GH 2031]</span><span class="sxs-lookup"><span data-stu-id="1ff03-762">Set AT_SECURE in auxiliary vector for set-user-ID and set-group-ID programs [GH 2031]</span></span>
- <span data-ttu-id="1ff03-763">伪终端主终结点不处理 TIOCPGRP [GH 1063]</span><span class="sxs-lookup"><span data-stu-id="1ff03-763">Psuedo-terminal master endpoint not handling TIOCPGRP [GH 1063]</span></span>
- <span data-ttu-id="1ff03-764">修复 lseek 在 LxFs 中的回退目录行为 [GH 2310]</span><span class="sxs-lookup"><span data-stu-id="1ff03-764">Fix lseek does to rewind directories in LxFs [GH 2310]</span></span>
- <span data-ttu-id="1ff03-765">重度使用后 /dev/ptmx 锁定 [GH 1882]</span><span class="sxs-lookup"><span data-stu-id="1ff03-765">/dev/ptmx locks up after heavy usage [GH 1882]</span></span>
- <span data-ttu-id="1ff03-766">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-766">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-767">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-767">Console</span></span>
- <span data-ttu-id="1ff03-768">修复横线/下划线四处可见的问题 [GH 2168]</span><span class="sxs-lookup"><span data-stu-id="1ff03-768">Fix for horizontal Lines/Underscores Everywhere [GH 2168]</span></span>
- <span data-ttu-id="1ff03-769">修复进程顺序更改，使 NPM 更难以关闭的问题 [GH 2170]</span><span class="sxs-lookup"><span data-stu-id="1ff03-769">Fix for process order changed making NPM harder to close [GH 2170]</span></span>
- <span data-ttu-id="1ff03-770">添加了新的色彩方案： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span><span class="sxs-lookup"><span data-stu-id="1ff03-770">Added our new color scheme: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-771">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-771">LTP Results:</span></span>
<span data-ttu-id="1ff03-772">自 16251 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-772">No change since 16251</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-773">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-773">Syscall Support</span></span>
<span data-ttu-id="1ff03-774">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-774">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-775">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-775">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`prlimit64`<br/>

### <a name="known-issues"></a><span data-ttu-id="1ff03-776">已知问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-776">Known Issues</span></span>
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[<span data-ttu-id="1ff03-777">GitHub 问题 2392：WSL 无法识别 Windows 文件夹 ...</span><span class="sxs-lookup"><span data-stu-id="1ff03-777">GitHub Issue 2392: Windows Folders not recognized by WSL ...</span></span>](https://github.com/Microsoft/BashOnWindows/issues/2392)
<span data-ttu-id="1ff03-778">在内部版本 16257 中，WSL 在通过 `/mnt/c/...` 枚举 Windows 文件/文件夹时会出现问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-778">In build 16257, WSL has issues when enumerating Windows files/folders via `/mnt/c/...`.</span></span>
<span data-ttu-id="1ff03-779">此问题已修复，修复程序将在 2017 年 8 月 14 日开始的周内，在预览体验成员内部版本中发布。</span><span class="sxs-lookup"><span data-stu-id="1ff03-779">This issue has been fixed and should be released in Insiders build during week commencing 8/14/2017.</span></span>

<br/>

## <a name="build-16251"></a><span data-ttu-id="1ff03-780">内部版本 16251</span><span class="sxs-lookup"><span data-stu-id="1ff03-780">Build 16251</span></span>

<span data-ttu-id="1ff03-781">有关内部版本 16251 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-781">For general Windows information on build 16251 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-782">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-782">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-783">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-783">WSL</span></span>
- <span data-ttu-id="1ff03-784">从 WSL 可选组件中删除 beta 标记，有关详细信息，请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-784">Remove beta tag from WSL optional component, see [blog post](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/) for details.</span></span>
- <span data-ttu-id="1ff03-785">在执行时正确初始化 set-user-ID 和 set-group-ID 二进制文件的 saved-set uid 和 gid [GH 962、1415、2072]</span><span class="sxs-lookup"><span data-stu-id="1ff03-785">Correctly initialize saved-set uid and gid for set-user-ID and set-group-ID binaries on exec [GH 962, 1415, 2072]</span></span>
- <span data-ttu-id="1ff03-786">添加了对 ptrace PTRACE_O_TRACEEXIT 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="1ff03-786">Added support for ptrace PTRACE_O_TRACEEXIT [GH 555]</span></span>
- <span data-ttu-id="1ff03-787">添加了对包含 NT_FPREGSET 的 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支持 [GH 555]</span><span class="sxs-lookup"><span data-stu-id="1ff03-787">Added support for ptrace PTRACE_GETFPREGS and PTRACE_GETREGSET with NT_FPREGSET [GH 555]</span></span>
- <span data-ttu-id="1ff03-788">修复了 ptrace 在忽略信号时停止的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-788">Fixed ptrace to stop on ignored signals</span></span>
- <span data-ttu-id="1ff03-789">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-789">Additional improvements and bug fixes</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-790">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-790">Console</span></span>
- <span data-ttu-id="1ff03-791">此版本中没有控制台相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-791">No Console related changes in this release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-792">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-792">LTP Results:</span></span>
<span data-ttu-id="1ff03-793">通过的测试数：768</span><span class="sxs-lookup"><span data-stu-id="1ff03-793">Number of Passing Tests: 768</span></span></br>
<span data-ttu-id="1ff03-794">失败的测试数：244</span><span class="sxs-lookup"><span data-stu-id="1ff03-794">Number of Failing Tests: 244</span></span></br>
<span data-ttu-id="1ff03-795">跳过的测试数：96</span><span class="sxs-lookup"><span data-stu-id="1ff03-795">Number of Skipped Tests: 96</span></span></br>
[<span data-ttu-id="1ff03-796">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-796">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a><span data-ttu-id="1ff03-797">内部版本 16241</span><span class="sxs-lookup"><span data-stu-id="1ff03-797">Build 16241</span></span>

<span data-ttu-id="1ff03-798">有关内部版本 16241 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-798">For general Windows information on build 16241 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-799">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-799">Fixed</span></span>
#### <a name="wsl"></a><span data-ttu-id="1ff03-800">WSL</span><span class="sxs-lookup"><span data-stu-id="1ff03-800">WSL</span></span>
- <span data-ttu-id="1ff03-801">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-801">No WSL related changes in this release.</span></span>

#### <a name="console"></a><span data-ttu-id="1ff03-802">控制台</span><span class="sxs-lookup"><span data-stu-id="1ff03-802">Console</span></span>
- <span data-ttu-id="1ff03-803">修复输出跨行 DEC 的错误字符的问题，最初报告位于[此处](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span><span class="sxs-lookup"><span data-stu-id="1ff03-803">Fix for outputting the wrong character for the crossing-lines DEC, originally reported [here](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)</span></span>
- <span data-ttu-id="1ff03-804">修复代码页 65001 (utf8) 中不显示输出文本的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-804">Fix for no output text being displayed in codepage 65001 (utf8)</span></span>
- <span data-ttu-id="1ff03-805">更改选择内容时，不会将对某种颜色的 RGB 值所做的更改传输到调色板的其他部分。</span><span class="sxs-lookup"><span data-stu-id="1ff03-805">Do not transfer changes made to one color's RGB values to other parts of the palette on selection change.</span></span> <span data-ttu-id="1ff03-806">这在一定程度上使得控制台属性表变得更易于使用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-806">This will make the console properties sheet a lot easier to use.</span></span>
- <span data-ttu-id="1ff03-807">Ctrl+S 似乎不起作用</span><span class="sxs-lookup"><span data-stu-id="1ff03-807">Ctrl+S doesn't appear to work correctly</span></span>
- <span data-ttu-id="1ff03-808">ANSI 转义代码中根本没有 Un-Bold/-Dim [GH 2174]</span><span class="sxs-lookup"><span data-stu-id="1ff03-808">Un-Bold/-Dim completely absent from ANSI escape codes [GH 2174]</span></span>
- <span data-ttu-id="1ff03-809">控制台不正常支持 Vim 色彩主题 [GH 1706]</span><span class="sxs-lookup"><span data-stu-id="1ff03-809">Console doesn't correctly support Vim color themes [GH 1706]</span></span>
- <span data-ttu-id="1ff03-810">无法粘贴特定的字符 [GH 2149]</span><span class="sxs-lookup"><span data-stu-id="1ff03-810">Cannot paste particular characters [GH 2149]</span></span>
- <span data-ttu-id="1ff03-811">当编辑/命令行上有内容时，重复流的调整大小操作以奇怪的方式与 bash 窗口调整大小操作交互 [GH ConEmu 1123]</span><span class="sxs-lookup"><span data-stu-id="1ff03-811">Reflow resize interacts strangely with resizing a bash window when stuff is on the edit/command line [GH ConEmu 1123]</span></span>
- <span data-ttu-id="1ff03-812">按 Ctrl-L 不会清屏 [GH 1978]</span><span class="sxs-lookup"><span data-stu-id="1ff03-812">Ctrl-L leaves the screen dirty [GH 1978]</span></span>
- <span data-ttu-id="1ff03-813">在 HDPI 上显示 VT 时的控制台呈现 bug [GH 1907]</span><span class="sxs-lookup"><span data-stu-id="1ff03-813">Console rendering bug when displaying VT on HDPI [GH 1907]</span></span>
- <span data-ttu-id="1ff03-814">日文字符出现乱码和 Unicode 字符 U+30FB [GH 2146]</span><span class="sxs-lookup"><span data-stu-id="1ff03-814">Japansese characters look strange with Unicode Character U+30FB [GH 2146]</span></span>
- <span data-ttu-id="1ff03-815">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-815">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16237"></a><span data-ttu-id="1ff03-816">版本 16237</span><span class="sxs-lookup"><span data-stu-id="1ff03-816">Build 16237</span></span>

<span data-ttu-id="1ff03-817">有关内部版本 16237 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-817">For general Windows information on build 16237 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-818">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-818">Fixed</span></span>
- <span data-ttu-id="1ff03-819">对 lxfs 中不包含 EA 的文件使用默认属性 (root, root, 0000)</span><span class="sxs-lookup"><span data-stu-id="1ff03-819">Use default attributes for files without EAs in lxfs (root, root, 0000)</span></span>
- <span data-ttu-id="1ff03-820">添加了对使用扩展属性的分发版的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-820">Added support for distributions that use extended attributes</span></span>
- <span data-ttu-id="1ff03-821">修复 getdents 和 getdents64 返回的项的填充</span><span class="sxs-lookup"><span data-stu-id="1ff03-821">Fix padding for entries returned by getdents and getdents64</span></span>
- <span data-ttu-id="1ff03-822">修复针对 shmctl SHM_STAT 系统调用的权限检查 [GH 2068]</span><span class="sxs-lookup"><span data-stu-id="1ff03-822">Fix permissions check for the shmctl SHM_STAT system call [GH 2068]</span></span>
- <span data-ttu-id="1ff03-823">修复了 tty 的错误初始 epoll 状态 [GH 2231]</span><span class="sxs-lookup"><span data-stu-id="1ff03-823">Fixed incorrect initial epoll state for ttys [GH 2231]</span></span>
- <span data-ttu-id="1ff03-824">修复 DrvFs readdir 不返回所有项的问题 [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="1ff03-824">Fix DrvFs readdir not returning all entries [GH 2077]</span></span>
- <span data-ttu-id="1ff03-825">修复取消链接文件时的 LxFs readdir [GH 2077]</span><span class="sxs-lookup"><span data-stu-id="1ff03-825">Fix LxFs readdir when files are unlinked [GH 2077]</span></span>
- <span data-ttu-id="1ff03-826">允许通过 procfs 重新打开未链接的 drvfs 文件</span><span class="sxs-lookup"><span data-stu-id="1ff03-826">Allow unlinked drvfs files to be reopened through procfs</span></span>
- <span data-ttu-id="1ff03-827">添加了用于禁用 WSL 功能的全局注册表项重写（interop/驱动器装载）</span><span class="sxs-lookup"><span data-stu-id="1ff03-827">Added global registry key override for disabling WSL features (interop / drive mounting)</span></span>
- <span data-ttu-id="1ff03-828">修复 DrvFs（和 LxFs）的“统计信息”中的错误块计数 [GH 1894]</span><span class="sxs-lookup"><span data-stu-id="1ff03-828">Fix incorrect block count in "stat" for DrvFs (and LxFs) [GH 1894]</span></span>
- <span data-ttu-id="1ff03-829">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-829">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16232"></a><span data-ttu-id="1ff03-830">内部版本 16232</span><span class="sxs-lookup"><span data-stu-id="1ff03-830">Build 16232</span></span>

<span data-ttu-id="1ff03-831">有关内部版本 16232 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-831">For general Windows information on build 16232 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-832">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-832">Fixed</span></span>
- <span data-ttu-id="1ff03-833">此版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-833">No WSL related changes in this release.</span></span>

</br>

## <a name="build-16226"></a><span data-ttu-id="1ff03-834">内部版本 16226</span><span class="sxs-lookup"><span data-stu-id="1ff03-834">Build 16226</span></span>

<span data-ttu-id="1ff03-835">有关内部版本 16226 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-835">For general Windows information on build 16226 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-836">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-836">Fixed</span></span>
- <span data-ttu-id="1ff03-837">xattr 相关的 syscall 支持（getxattr、setxattr、listxattr、removexattr）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-837">xattr related syscalls support (getxattr, setxattr, listxattr, removexattr).</span></span>
- <span data-ttu-id="1ff03-838">security.capablity xattr 支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-838">security.capablity xattr support.</span></span>
- <span data-ttu-id="1ff03-839">改善了与某些文件系统和筛选器（包括非 MS SMB 服务器）的兼容性。</span><span class="sxs-lookup"><span data-stu-id="1ff03-839">Improved compatibility with certain file systems and filters, including non-MS SMB servers.</span></span> <span data-ttu-id="1ff03-840">[GH #1952]</span><span class="sxs-lookup"><span data-stu-id="1ff03-840">[GH #1952]</span></span>
- <span data-ttu-id="1ff03-841">改善了对 OneDrive 占位符、GVFS 占位符和精简 OS 压缩文件的支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-841">Improved support for OneDrive placeholders, GVFS placeholders, and Compact OS compressed files.</span></span>
- <span data-ttu-id="1ff03-842">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-842">Additional improvements and bug fixes</span></span>

</br>

## <a name="build-16215"></a><span data-ttu-id="1ff03-843">内部版本 16215</span><span class="sxs-lookup"><span data-stu-id="1ff03-843">Build 16215</span></span>

<span data-ttu-id="1ff03-844">有关内部版本 16215 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-844">For general Windows information on build 16215 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-845">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-845">Fixed</span></span>
- <span data-ttu-id="1ff03-846">WSL 不再需要开发人员模式。</span><span class="sxs-lookup"><span data-stu-id="1ff03-846">WSL no longer requires developer mode.</span></span>
- <span data-ttu-id="1ff03-847">支持 drvfs 中的目录接合。</span><span class="sxs-lookup"><span data-stu-id="1ff03-847">Support directory junctions in drvfs.</span></span>
- <span data-ttu-id="1ff03-848">处理 WSL appx 分发包的卸载。</span><span class="sxs-lookup"><span data-stu-id="1ff03-848">Handle uninstalling of WSL distribution appx packages.</span></span>
- <span data-ttu-id="1ff03-849">更新 procfs 以显示专用映射和共享映射。</span><span class="sxs-lookup"><span data-stu-id="1ff03-849">Update procfs to show private and shared mappings.</span></span>
- <span data-ttu-id="1ff03-850">为 wslconfig.exe 添加清理部分安装或已卸载的分发版的功能。</span><span class="sxs-lookup"><span data-stu-id="1ff03-850">Add ability for wslconfig.exe to clean up distributions that are partially installed or uninstalled.</span></span>
- <span data-ttu-id="1ff03-851">添加了对 TCP 套接字的 IP_MTU_DISCOVER 的支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-851">Added support for IP_MTU_DISCOVER for TCP sockets.</span></span> <span data-ttu-id="1ff03-852">[GH 1639、2115、2205]</span><span class="sxs-lookup"><span data-stu-id="1ff03-852">[GH 1639, 2115, 2205]</span></span>
- <span data-ttu-id="1ff03-853">推断 AF_INADDR 路由的协议系列。</span><span class="sxs-lookup"><span data-stu-id="1ff03-853">Infer protocol family for routes to AF_INADDR.</span></span>
- <span data-ttu-id="1ff03-854">串行设备改进 [GH 1929]。</span><span class="sxs-lookup"><span data-stu-id="1ff03-854">Serial device improvements [GH 1929].</span></span>

</br>

## <a name="build-16199"></a><span data-ttu-id="1ff03-855">内部版本 16199</span><span class="sxs-lookup"><span data-stu-id="1ff03-855">Build 16199</span></span>

<span data-ttu-id="1ff03-856">有关内部版本 16199 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-856">For general Windows information on build 16199 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-857">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-857">Fixed</span></span>
- <span data-ttu-id="1ff03-858">这些版本中没有 WSL 相关的更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-858">No WSL related changes in these releases.</span></span>

</br>

## <a name="build-16193"></a><span data-ttu-id="1ff03-859">内部版本 16193</span><span class="sxs-lookup"><span data-stu-id="1ff03-859">Build 16193</span></span>

<span data-ttu-id="1ff03-860">有关内部版本 16193 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-860">For general Windows information on build 16193 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-861">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-861">Fixed</span></span>
- <span data-ttu-id="1ff03-862">发送 SIGCONT 与终止线程组之间的争用状态 [GH 1973]</span><span class="sxs-lookup"><span data-stu-id="1ff03-862">Race condition between sending SIGCONT and a threadgroup terminating [GH 1973]</span></span>
- <span data-ttu-id="1ff03-863">更改 tty 和 pty 设备以报告 FILE_DEVICE_NAMED_PIPE 而不是 FILE_DEVICE_CONSOLE [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="1ff03-863">change tty and pty devices to report FILE_DEVICE_NAMED_PIPE instead of FILE_DEVICE_CONSOLE [GH 1840]</span></span>
- <span data-ttu-id="1ff03-864">IP_OPTIONS 的 SSH 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-864">SSH fix for IP_OPTIONS</span></span>
- <span data-ttu-id="1ff03-865">已将 DrvFs 装载移到初始化守护程序 [GH 1862、1968、1767、1933]</span><span class="sxs-lookup"><span data-stu-id="1ff03-865">Moved DrvFs mounting to init daemon [GH 1862, 1968, 1767, 1933]</span></span>
- <span data-ttu-id="1ff03-866">在 DrvFs 中添加了遵循 NT 符号链接的支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-866">Added support in DrvFs for following NT symlinks.</span></span>

</br>

## <a name="build-16184"></a><span data-ttu-id="1ff03-867">内部版本 16184</span><span class="sxs-lookup"><span data-stu-id="1ff03-867">Build 16184</span></span>

<span data-ttu-id="1ff03-868">有关内部版本 16184 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-868">For general Windows information on build 16184 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-869">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-869">Fixed</span></span>
- <span data-ttu-id="1ff03-870">删除了 apt 包维护任务 (lxrun.exe /update)</span><span class="sxs-lookup"><span data-stu-id="1ff03-870">Removed apt package maintenance task (lxrun.exe /update)</span></span>
- <span data-ttu-id="1ff03-871">修复了 node.js 中的 Windows 进程不显示输出的问题 [GH 1840]</span><span class="sxs-lookup"><span data-stu-id="1ff03-871">Fixed output not showing up in from Windows processes in node.js [GH 1840]</span></span>
- <span data-ttu-id="1ff03-872">放宽 lxcore 中的对齐要求 [GH 1794]</span><span class="sxs-lookup"><span data-stu-id="1ff03-872">Relax alignment requirements in lxcore [GH 1794]</span></span>
- <span data-ttu-id="1ff03-873">修复了许多系统调用中处理 AT_EMPTY_PATH 标志的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-873">Fixed handling of the AT_EMPTY_PATH flag in a numer of system calls.</span></span>
- <span data-ttu-id="1ff03-874">修复了删除存在已打开句柄的 DrvFs 文件时，导致文件出现未定义的行为的问题 [GH 544、966、1357、1535、1615]</span><span class="sxs-lookup"><span data-stu-id="1ff03-874">Fixed issue where deleting DrvFs files with open handles will cause the file to exhibit undefined behavior [GH 544,966,1357,1535,1615]</span></span>
- <span data-ttu-id="1ff03-875">/etc/hosts 现在会从 Windows hosts 文件 (%windir%\system32\drivers\etc\hosts) 继承项 [GH 1495]</span><span class="sxs-lookup"><span data-stu-id="1ff03-875">/etc/hosts will now inherit entries from the Windows hosts file (%windir%\system32\drivers\etc\hosts) [GH 1495]</span></span>

</br>

## <a name="build-16179"></a><span data-ttu-id="1ff03-876">内部版本 16179</span><span class="sxs-lookup"><span data-stu-id="1ff03-876">Build 16179</span></span>

<span data-ttu-id="1ff03-877">有关内部版本 16179 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-877">For general Windows information on build 16179 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-878">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-878">Fixed</span></span>
- <span data-ttu-id="1ff03-879">本周没有 WSL 更改。</span><span class="sxs-lookup"><span data-stu-id="1ff03-879">No WSL changes this week.</span></span>

</br>

## <a name="build-16176"></a><span data-ttu-id="1ff03-880">内部版本 16176</span><span class="sxs-lookup"><span data-stu-id="1ff03-880">Build 16176</span></span>

<span data-ttu-id="1ff03-881">有关内部版本 16176 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-881">For general Windows information on build 16176 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-882">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-882">Fixed</span></span>

- [<span data-ttu-id="1ff03-883">已启用串行支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-883">Enabled serial support</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- <span data-ttu-id="1ff03-884">添加了 IP 套接字选项 IP_OPTIONS [GH 1116]</span><span class="sxs-lookup"><span data-stu-id="1ff03-884">Added IP socket option IP_OPTIONS [GH 1116]</span></span>
- <span data-ttu-id="1ff03-885">实现了 pwritev 函数（将文件上传到 nginx/PHP-FPM 时）[GH 1506]</span><span class="sxs-lookup"><span data-stu-id="1ff03-885">Implemented pwritev function (while uploading file to nginx/PHP-FPM) [GH 1506]</span></span>
- <span data-ttu-id="1ff03-886">添加了 IP 套接字选项 IP_MULTICAST_IF 和 IPV6_MULTICAST_IF [GH 990]</span><span class="sxs-lookup"><span data-stu-id="1ff03-886">Added IP socket options IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]</span></span>
- <span data-ttu-id="1ff03-887">支持套接字选项 IP_MULTICAST_LOOP 和 IPV6_MULTICAST_LOOP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="1ff03-887">Support for socket option IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]</span></span>
- <span data-ttu-id="1ff03-888">为应用节点、traceroute、dig、nslookup、主机添加了 IP(V6)_MTU 套接字选项</span><span class="sxs-lookup"><span data-stu-id="1ff03-888">Added IP(V6)_MTU socket option for apps node, traceroute, dig, nslookup, host</span></span>
- <span data-ttu-id="1ff03-889">添加了 IP 套接字选项 IPV6_UNICAST_HOPS</span><span class="sxs-lookup"><span data-stu-id="1ff03-889">Added IP socket option IPV6_UNICAST_HOPS</span></span>
- [<span data-ttu-id="1ff03-890">文件系统改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-890">Filesystem Improvements</span></span>](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * <span data-ttu-id="1ff03-891">允许装载 UNC 路径</span><span class="sxs-lookup"><span data-stu-id="1ff03-891">Allow mounting of UNC paths</span></span>
    * <span data-ttu-id="1ff03-892">在 drvfs 中启用 CDFS 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-892">Enable CDFS support in drvfs</span></span>
    * <span data-ttu-id="1ff03-893">正确处理 drvfs 中网络文件系统的权限</span><span class="sxs-lookup"><span data-stu-id="1ff03-893">Correctly handle permissions for network file systems in drvfs</span></span>
    * <span data-ttu-id="1ff03-894">在 drvfs 中添加远程驱动器的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-894">Add support for remote drives to drvfs</span></span>
    * <span data-ttu-id="1ff03-895">在 drvfs 中启用 FAT 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-895">Enable FAT support in drvfs</span></span>
- <span data-ttu-id="1ff03-896">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-896">Additional fixes and Improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-897">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="1ff03-897">LTP Results</span></span>
<span data-ttu-id="1ff03-898">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-898">No changes since 15042</span></span>

</br>

## <a name="build-16170"></a><span data-ttu-id="1ff03-899">内部版本 16170</span><span class="sxs-lookup"><span data-stu-id="1ff03-899">Build 16170</span></span>

<span data-ttu-id="1ff03-900">有关内部版本 16170 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-900">For general Windows information on build 16170 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/).</span></span><br/>

<span data-ttu-id="1ff03-901">我们发布的新[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)中介绍了我们在测试 WSL 方面所做的努力。</span><span class="sxs-lookup"><span data-stu-id="1ff03-901">We released a new [blog post](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/) discussing our efforts to test WSL.</span></span>

### <a name="fixed"></a><span data-ttu-id="1ff03-902">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-902">Fixed</span></span>

- <span data-ttu-id="1ff03-903">支持套接字选项 IP_ADD_MEMBERSHIP 和 IPV6_ADD_MEMBERSHIP [GH 1678]</span><span class="sxs-lookup"><span data-stu-id="1ff03-903">Support socket option IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]</span></span>
- <span data-ttu-id="1ff03-904">添加对 PTRACE_OLDSETOPTIONS 的支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-904">Add support for PTRACE_OLDSETOPTIONS.</span></span> <span data-ttu-id="1ff03-905">[GH 1692]</span><span class="sxs-lookup"><span data-stu-id="1ff03-905">[GH 1692]</span></span>
- <span data-ttu-id="1ff03-906">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-906">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-907">LTP 结果</span><span class="sxs-lookup"><span data-stu-id="1ff03-907">LTP Results</span></span>
<span data-ttu-id="1ff03-908">自 15042 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-908">No changes since 15042</span></span>

</br>

## <a name="build-15046-to-windows-10-creators-update"></a><span data-ttu-id="1ff03-909">内部版本 15046 到 Windows 10 创意者更新</span><span class="sxs-lookup"><span data-stu-id="1ff03-909">Build 15046 to Windows 10 Creators Update</span></span>
<span data-ttu-id="1ff03-910">我们未计划在 Windows 10 创意者更新中包含其他 WSL 修复或功能。</span><span class="sxs-lookup"><span data-stu-id="1ff03-910">There are no more WSL fixes or features planned for inclusion in the Creators Update to Windows 10.</span></span> <span data-ttu-id="1ff03-911">WSL 的发行说明将在未来几周恢复发布，其中补充了面向下一个 Windows 更新主要版本的信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-911">Release notes for WSL will resume in the coming weeks for additions targeting the next major Windows Update.</span></span> <span data-ttu-id="1ff03-912">有关内部版本 15046 和将来的预览体验版的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-912">For general Windows information on build 15046 and future Insider releases visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/).</span></span> <br/><br/>
 <br/>

## <a name="build-15042"></a><span data-ttu-id="1ff03-913">内部版本 15042</span><span class="sxs-lookup"><span data-stu-id="1ff03-913">Build 15042</span></span>

<span data-ttu-id="1ff03-914">有关内部版本 15042 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-914">For general Windows information on build 15042 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-915">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-915">Fixed</span></span>

- <span data-ttu-id="1ff03-916">修复删除以“...”结尾的路径时出现死锁的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-916">Fix for a deadlock when removing a path ending in ".."</span></span>
- <span data-ttu-id="1ff03-917">修复了 FIONBIO 在成功时不返回 0 的问题 [GH 1683]</span><span class="sxs-lookup"><span data-stu-id="1ff03-917">Fixed an issue where FIONBIO not returning 0 on success [GH 1683]</span></span>
- <span data-ttu-id="1ff03-918">修复了 inet 数据报套接字的零长度读取问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-918">Fixed issue with zero-length reads of inet datagram sockets</span></span>
- <span data-ttu-id="1ff03-919">修复 drvfs inode 查找中的争用状况可能导致死锁的问题 [GH 1675]</span><span class="sxs-lookup"><span data-stu-id="1ff03-919">Fix possible deadlock due to race condition in drvfs inode lookup [GH 1675]</span></span>
- <span data-ttu-id="1ff03-920">扩展了对 unix 套接字辅助数据的支持；SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514、613、1326]</span><span class="sxs-lookup"><span data-stu-id="1ff03-920">Extended support for unix socket ancillary data; SCM_CREDENTIALS and SCM_RIGHTS [GH 514, 613, 1326]</span></span>
- <span data-ttu-id="1ff03-921">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-921">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-922">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-922">LTP Results:</span></span>
<span data-ttu-id="1ff03-923">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="1ff03-923">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="1ff03-924">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="1ff03-924">Number of non-Passing (failing, skipped, etc…): 255</span></span>

</br>

## <a name="build-15031"></a><span data-ttu-id="1ff03-925">内部版本 15031</span><span class="sxs-lookup"><span data-stu-id="1ff03-925">Build 15031</span></span>

<span data-ttu-id="1ff03-926">有关内部版本 15031 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-926">For general Windows information on build 15031 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-927">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-927">Fixed</span></span>

- <span data-ttu-id="1ff03-928">修复了 time(2) 偶尔行为异常的 bug。</span><span class="sxs-lookup"><span data-stu-id="1ff03-928">Fixed a bug where time(2) would sporadically misbehave.</span></span>
- <span data-ttu-id="1ff03-929">修复了 \*SIGPROCMASK syscall 可能损坏信号掩码的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-929">Fixed and issue where \*SIGPROCMASK syscalls could corrupt signal mask.</span></span>
- <span data-ttu-id="1ff03-930">现在会在 WSL 进程创建通知中返回完整的命令行长度。</span><span class="sxs-lookup"><span data-stu-id="1ff03-930">Now return full command line length in WSL process creation notification.</span></span> <span data-ttu-id="1ff03-931">[GH 1632]</span><span class="sxs-lookup"><span data-stu-id="1ff03-931">[GH 1632]</span></span>
- <span data-ttu-id="1ff03-932">WSL 现在会针对 GDB 挂起通过 ptrace 报告线程退出。</span><span class="sxs-lookup"><span data-stu-id="1ff03-932">WSL now reports thread exit through ptrace for GDB hangs.</span></span> <span data-ttu-id="1ff03-933">[GH 1196]</span><span class="sxs-lookup"><span data-stu-id="1ff03-933">[GH 1196]</span></span>
- <span data-ttu-id="1ff03-934">修复了在收到繁重 tmux IO 后 ptys 挂起的 bug。</span><span class="sxs-lookup"><span data-stu-id="1ff03-934">Fixed bug where ptys would hang after heavy tmux IO.</span></span> <span data-ttu-id="1ff03-935">[GH 1358]</span><span class="sxs-lookup"><span data-stu-id="1ff03-935">[GH 1358]</span></span>
- <span data-ttu-id="1ff03-936">修复了许多系统调用中的超时验证（futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create）</span><span class="sxs-lookup"><span data-stu-id="1ff03-936">Fixed timeout validation in many system calls (futex, semtimedop, ppoll, sigtimedwait, itimer, timer_create)</span></span>
- <span data-ttu-id="1ff03-937">添加了 eventfd EFD_SEMAPHORE 支持 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="1ff03-937">Added eventfd EFD_SEMAPHORE support [GH 452]</span></span>
- <span data-ttu-id="1ff03-938">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-938">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-939">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-939">LTP Results:</span></span>
<span data-ttu-id="1ff03-940">通过的测试数：737</span><span class="sxs-lookup"><span data-stu-id="1ff03-940">Number of Passing Test: 737</span></span></br>
<span data-ttu-id="1ff03-941">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="1ff03-941">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="1ff03-942">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-942">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a><span data-ttu-id="1ff03-943">内部版本 15025</span><span class="sxs-lookup"><span data-stu-id="1ff03-943">Build 15025</span></span>

<span data-ttu-id="1ff03-944">有关内部版本 15025 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-944">For general Windows information on build 15025 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-945">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-945">Fixed</span></span>

- <span data-ttu-id="1ff03-946">修复破坏 grep 2.27 的 bug [GH 1578]</span><span class="sxs-lookup"><span data-stu-id="1ff03-946">Fix for bug that broke grep 2.27 [GH 1578]</span></span>
- <span data-ttu-id="1ff03-947">为 eventfd2 syscall 实现了 EFD_SEMAPHORE 标志 [GH 452]</span><span class="sxs-lookup"><span data-stu-id="1ff03-947">Implemented EFD_SEMAPHORE flag for eventfd2 syscall [GH 452]</span></span>
- <span data-ttu-id="1ff03-948">实现了 /proc/[pid]/net/ipv6_route [GH 1608]</span><span class="sxs-lookup"><span data-stu-id="1ff03-948">Implemented /proc/[pid]/net/ipv6_route [GH 1608]</span></span>
- <span data-ttu-id="1ff03-949">针对 unix 流套接字的信号驱动 IO 支持 [GH 393、68]</span><span class="sxs-lookup"><span data-stu-id="1ff03-949">Signal driven IO support for unix stream sockets [GH 393, 68]</span></span>
- <span data-ttu-id="1ff03-950">支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]</span><span class="sxs-lookup"><span data-stu-id="1ff03-950">Support F_GETPIPE_SZ and F_SETPIPE_SZ [GH 1012]</span></span>
- <span data-ttu-id="1ff03-951">实现 recvmmsg() syscall [GH 1531]</span><span class="sxs-lookup"><span data-stu-id="1ff03-951">Implement recvmmsg() syscall [GH 1531]</span></span>
- <span data-ttu-id="1ff03-952">修复了 epoll_wait() 不等待的 bug [GH 1609]</span><span class="sxs-lookup"><span data-stu-id="1ff03-952">Fixed bug where epoll_wait() wasn't waiting [GH 1609]</span></span>
- <span data-ttu-id="1ff03-953">实现 /proc/version_signature</span><span class="sxs-lookup"><span data-stu-id="1ff03-953">Implement /proc/version_signature</span></span>
- <span data-ttu-id="1ff03-954">现在，如果两个文件描述符引用同一管道，则 syscall 会返回失败</span><span class="sxs-lookup"><span data-stu-id="1ff03-954">Tee syscall now returns failure if both file descriptors refer to the same pipe</span></span>
- <span data-ttu-id="1ff03-955">为 Unix 套接字的 SO_PEERCRED 实现了正确的行为</span><span class="sxs-lookup"><span data-stu-id="1ff03-955">Implemented correct behavior for SO_PEERCRED for Unix sockets</span></span>
- <span data-ttu-id="1ff03-956">修复了 tkill syscall 处理无效参数的方法</span><span class="sxs-lookup"><span data-stu-id="1ff03-956">Fixed tkill syscall invalid parameter handling</span></span>
- <span data-ttu-id="1ff03-957">做出更改以提高 drvfs 的性能</span><span class="sxs-lookup"><span data-stu-id="1ff03-957">Changes to increase the preformace of drvfs</span></span>
- <span data-ttu-id="1ff03-958">针对 Ruby IO 阻塞的次要修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-958">Minor fix for Ruby IO blocking</span></span>
- <span data-ttu-id="1ff03-959">修复了 recvmsg() 对 inet 套接字的 MSG_DONTWAIT 标志返回 EINVAL 的问题 [GH 1296]</span><span class="sxs-lookup"><span data-stu-id="1ff03-959">Fixed recvmsg() returning EINVAL for the MSG_DONTWAIT flag for inet sockets [GH 1296]</span></span>
- <span data-ttu-id="1ff03-960">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-960">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-961">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-961">LTP Results:</span></span>
<span data-ttu-id="1ff03-962">通过的测试数：732</span><span class="sxs-lookup"><span data-stu-id="1ff03-962">Number of Passing Test: 732</span></span></br>
<span data-ttu-id="1ff03-963">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="1ff03-963">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="1ff03-964">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-964">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a><span data-ttu-id="1ff03-965">内部版本 15019</span><span class="sxs-lookup"><span data-stu-id="1ff03-965">Build 15019</span></span>

<span data-ttu-id="1ff03-966">有关内部版本 15019 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-966">For general Windows information on build 15019 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-967">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-967">Fixed</span></span>

- <span data-ttu-id="1ff03-968">修复了 htop 等工具在 procfs 中错误报告 CPU 使用率的 bug（GH 823、945、971）</span><span class="sxs-lookup"><span data-stu-id="1ff03-968">Fixed bug that incorrectly reported CPU usage in procfs for tools like htop (GH 823, 945, 971)</span></span>
- <span data-ttu-id="1ff03-969">对现有的文件结合 O_TRUNC 调用 open() 时，inotify 现在会在 IN_OPEN 的前面生成 IN_MODIFY</span><span class="sxs-lookup"><span data-stu-id="1ff03-969">When calling open() with O_TRUNC on an existing file inotify now generates IN_MODIFY before IN_OPEN</span></span>
- <span data-ttu-id="1ff03-970">修复 unix 套接字 getsockopt SO_ERROR 以启用 postgress [GH 61、1354]</span><span class="sxs-lookup"><span data-stu-id="1ff03-970">Fixes to unix socket getsockopt SO_ERROR to enable postgress [GH 61, 1354]</span></span>
- <span data-ttu-id="1ff03-971">为 GO 语言实现 /proc/sys/net/core/somaxconn</span><span class="sxs-lookup"><span data-stu-id="1ff03-971">Implement /proc/sys/net/core/somaxconn for the GO language</span></span>
- <span data-ttu-id="1ff03-972">Apt-get package update 后台任务现在会在视图中以隐藏方式运行</span><span class="sxs-lookup"><span data-stu-id="1ff03-972">Apt-get package update background task now runs hidden from view</span></span>
- <span data-ttu-id="1ff03-973">清除 ipv6 localhost 的范围（Spring-Framework(Java) 失败）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-973">Clear scope for ipv6 localhost (Spring-Framework(Java) failure).</span></span>
- <span data-ttu-id="1ff03-974">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-974">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-975">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-975">LTP Results:</span></span>
<span data-ttu-id="1ff03-976">通过的测试数：714</span><span class="sxs-lookup"><span data-stu-id="1ff03-976">Number of Passing Test: 714</span></span> </br>
<span data-ttu-id="1ff03-977">未通过的测试数（失败、已跳过等）：249</span><span class="sxs-lookup"><span data-stu-id="1ff03-977">Number of non-Passing (failing, skipped, etc…): 249</span></span> </br>
[<span data-ttu-id="1ff03-978">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-978">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a><span data-ttu-id="1ff03-979">内部版本 15014</span><span class="sxs-lookup"><span data-stu-id="1ff03-979">Build 15014</span></span>

<span data-ttu-id="1ff03-980">有关内部版本 15014 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-980">For general Windows information on build 15014 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-981">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-981">Fixed</span></span>

- <span data-ttu-id="1ff03-982">Ctrl+C 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="1ff03-982">Ctrl+C now works as intended</span></span>
- <span data-ttu-id="1ff03-983">htop 和 ps auxw 现在会显示正确的资源利用率 (GH #516)</span><span class="sxs-lookup"><span data-stu-id="1ff03-983">htop and ps auxw now show correct resource utilization (GH #516)</span></span>
- <span data-ttu-id="1ff03-984">NT 异常到信号的基本转换。</span><span class="sxs-lookup"><span data-stu-id="1ff03-984">Basic translation of NT exceptions to signals.</span></span> <span data-ttu-id="1ff03-985">(GH #513)</span><span class="sxs-lookup"><span data-stu-id="1ff03-985">(GH #513)</span></span>
- <span data-ttu-id="1ff03-986">当空间耗尽时，fallocate 现在会失败并返回 ENOSPC，而不是返回 EINVAL (GH #1571)</span><span class="sxs-lookup"><span data-stu-id="1ff03-986">fallocate now fails with ENOSPC  when running out of space instead of EINVAL (GH #1571)</span></span>
- <span data-ttu-id="1ff03-987">添加了 /proc/sys/kernel/sem。</span><span class="sxs-lookup"><span data-stu-id="1ff03-987">Added /proc/sys/kernel/sem.</span></span>
- <span data-ttu-id="1ff03-988">实现了 semop 和 semtimedop 系统调用</span><span class="sxs-lookup"><span data-stu-id="1ff03-988">Implemented semop and semtimedop system calls</span></span>
- <span data-ttu-id="1ff03-989">修复了 IP_RECVTOS 和 IPV6_RECVTCLASS 套接字选项的 nslookup 错误 (GH 69)</span><span class="sxs-lookup"><span data-stu-id="1ff03-989">Fixed nslookup errors with IP_RECVTOS & IPV6_RECVTCLASS socket option (GH 69)</span></span>
- <span data-ttu-id="1ff03-990">支持套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT</span><span class="sxs-lookup"><span data-stu-id="1ff03-990">Support for socket options IP_RECVTTL and IPV6_RECVHOPLIMIT</span></span>
- <span data-ttu-id="1ff03-991">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-991">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-992">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-992">LTP Results:</span></span>
<span data-ttu-id="1ff03-993">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="1ff03-993">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="1ff03-994">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="1ff03-994">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="1ff03-995">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-995">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a><span data-ttu-id="1ff03-996">Syscall 摘要</span><span class="sxs-lookup"><span data-stu-id="1ff03-996">Syscall Summary</span></span>
<span data-ttu-id="1ff03-997">Syscall 总数：384</span><span class="sxs-lookup"><span data-stu-id="1ff03-997">Total Syscalls: 384</span></span> </br>
<span data-ttu-id="1ff03-998">已实现总数：235</span><span class="sxs-lookup"><span data-stu-id="1ff03-998">Total Implemented: 235</span></span> </br>
<span data-ttu-id="1ff03-999">已存根总数：22</span><span class="sxs-lookup"><span data-stu-id="1ff03-999">Total Stubbed: 22</span></span> </br>
<span data-ttu-id="1ff03-1000">未实现总数：127</span><span class="sxs-lookup"><span data-stu-id="1ff03-1000">Total Unimplemented: 127</span></span> </br>
[<span data-ttu-id="1ff03-1001">详细分解</span><span class="sxs-lookup"><span data-stu-id="1ff03-1001">Detailed Breakdown</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a><span data-ttu-id="1ff03-1002">内部版本 15007</span><span class="sxs-lookup"><span data-stu-id="1ff03-1002">Build 15007</span></span>

<span data-ttu-id="1ff03-1003">有关内部版本 15007 的一般 Windows 信息，请访问 [Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1003">For general Windows information on build 15007 visit the [Windows Blog]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="1ff03-1004">已知问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1004">Known Issue</span></span>

- <span data-ttu-id="1ff03-1005">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1005">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="1ff03-1006">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1006">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="1ff03-1007">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1007">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="1ff03-1008">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1008">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="1ff03-1009">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="1ff03-1009">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="1ff03-1010">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="1ff03-1010">Users can explore the option to include this in their `.bashrc`</span></span>

### <a name="fixed"></a><span data-ttu-id="1ff03-1011">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1011">Fixed</span></span>

- <span data-ttu-id="1ff03-1012">更正了运行 WSL 会消耗 100% 的 CPU 核心的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1012">Corrected the issue where running WSL would consume 100% of a CPU core</span></span>
- <span data-ttu-id="1ff03-1013">现在支持套接字选项 IP_PKTINFO、IPV6_RECVPKTINFO。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1013">Socket option IP_PKTINFO, IPV6_RECVPKTINFO now supported.</span></span> <span data-ttu-id="1ff03-1014">（GH #851、987）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1014">(GH #851, 987)</span></span>
- <span data-ttu-id="1ff03-1015">在 lxcore 中将网络接口物理地址截断为 16 个字节（GH #1452、1414、1343、468、308）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1015">Truncate network interface physical address to 16 bytes in lxcore (GH #1452, 1414, 1343, 468, 308)</span></span>
- <span data-ttu-id="1ff03-1016">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1016">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1017">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1017">LTP Results:</span></span>
<span data-ttu-id="1ff03-1018">通过的测试数：709</span><span class="sxs-lookup"><span data-stu-id="1ff03-1018">Number of Passing Test: 709</span></span> </br>
<span data-ttu-id="1ff03-1019">未通过的测试数（失败、已跳过等）：255</span><span class="sxs-lookup"><span data-stu-id="1ff03-1019">Number of non-Passing (failing, skipped, etc…): 255</span></span> </br>
[<span data-ttu-id="1ff03-1020">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1020">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a><span data-ttu-id="1ff03-1021">内部版本 15002</span><span class="sxs-lookup"><span data-stu-id="1ff03-1021">Build 15002</span></span>

<span data-ttu-id="1ff03-1022">有关内部版本 15002 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1022">For general Windows information on build 15002 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/).</span></span><br/>


### <a name="known-issue"></a><span data-ttu-id="1ff03-1023">已知问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1023">Known Issue</span></span>

<span data-ttu-id="1ff03-1024">两个已知问题：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1024">Two known issues:</span></span>
- <span data-ttu-id="1ff03-1025">已知 bug：控制台无法识别某些 Ctrl + <key> 输入。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1025">There is a known bug where the console does not recognize some Ctrl + <key> input.</span></span>  <span data-ttu-id="1ff03-1026">这包括将充当普通“c”按键的 ctrl-c 命令。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1026">This includes the ctrl-c command which will act as a normal ‘c’ keypress.</span></span>

  - <span data-ttu-id="1ff03-1027">解决方法：将备用键映射到 Ctrl+C。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1027">Workaround: Map an alternate key to Ctrl+C.</span></span> <span data-ttu-id="1ff03-1028">例如，若要将 Ctrl+K 映射到 Ctrl+C，请执行：`stty intr \^k`。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1028">For example, to map Ctrl+K to Ctrl+C do: `stty intr \^k`.</span></span>  <span data-ttu-id="1ff03-1029">这种映射是按终端进行的，每次启动 bash 都必须执行。 </span><span class="sxs-lookup"><span data-stu-id="1ff03-1029">This mapping is per terminal and will have to be done *every* time bash is launched.</span></span> <span data-ttu-id="1ff03-1030">用户可以探索该选项，以将此映射包含在其 `.bashrc` 中</span><span class="sxs-lookup"><span data-stu-id="1ff03-1030">Users can explore the option to include this in their `.bashrc`</span></span>

- <span data-ttu-id="1ff03-1031">当 WSL 运行时，系统线程将消耗 100% 的 CPU 核心。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1031">While WSL is running a system thread will consume 100% of a CPU core.</span></span>  <span data-ttu-id="1ff03-1032">根本原因已解决并已在内部修复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1032">The root cause has been addressed and fixed internally.</span></span>

### <a name="fixed"></a><span data-ttu-id="1ff03-1033">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1033">Fixed</span></span>

- <span data-ttu-id="1ff03-1034">现在，必须在同一权限级别创建所有 bash 会话。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1034">All bash sessions must now be created at the same permission level.</span></span>  <span data-ttu-id="1ff03-1035">尝试在不同级别启动会话将遭到阻止。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1035">Attempting to start a session at a different level will be blocked.</span></span>  <span data-ttu-id="1ff03-1036">这意味着，管理员和非管理员控制台不能同时运行。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1036">This means admin and non-admin consoles cannot run at the same time.</span></span> <span data-ttu-id="1ff03-1037">(GH #626)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1037">(GH #626)</span></span>
<br/>
- <span data-ttu-id="1ff03-1038">实现了以下 NETLINK_ROUTE 消息（需要 Windows 管理员）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1038">Implemented the following NETLINK_ROUTE messages (requires Windows admin)</span></span>
     - <span data-ttu-id="1ff03-1039">RTM_NEWADDR（支持 `ip addr add`）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1039">RTM_NEWADDR (supports `ip addr add`)</span></span>
     - <span data-ttu-id="1ff03-1040">RTM_NEWROUTE（支持 `ip route add`）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1040">RTM_NEWROUTE (supports `ip route add`)</span></span>
     - <span data-ttu-id="1ff03-1041">RTM_DELADDR（支持 `ip addr del`）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1041">RTM_DELADDR (supports `ip addr del`)</span></span>
     - <span data-ttu-id="1ff03-1042">RTM_DELROUTE（支持 `ip route del`）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1042">RTM_DELROUTE (supports `ip route del`)</span></span>
- <span data-ttu-id="1ff03-1043">用于检查要更新的包的计划任务将不再在按流量计费的连接上运行 (GH #1371)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1043">Scheduled task checking for packages to update will no longer run on a metered connection (GH #1371)</span></span>
- <span data-ttu-id="1ff03-1044">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1044">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="1ff03-1045">实现了 TCP_KEEPCNT 套接字选项 (GH #843)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1045">Implemented TCP_KEEPCNT socket option (GH #843)</span></span>
- <span data-ttu-id="1ff03-1046">实现了 IP_MTU_DISCOVER INET 套接字选项（GH #720、717、170、69）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1046">Implemented IP_MTU_DISCOVER INET socket option (GH #720, 717, 170, 69)</span></span>
- <span data-ttu-id="1ff03-1047">删除了旧功能，以通过 NT 路径查找从 init 运行 NT 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1047">Removed legacy functionality to run NT binaries from init with NT path lookup.</span></span> <span data-ttu-id="1ff03-1048">(GH #1325)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1048">(GH #1325)</span></span>
- <span data-ttu-id="1ff03-1049">修复 /dev/kmsg 的模式，以允许进行组访问/其他读取访问 (0644) (GH #1321)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1049">Fix mode of /dev/kmsg to allow group / other read access (0644) (GH #1321)</span></span>
- <span data-ttu-id="1ff03-1050">实现了 /proc/sys/kernel/random/uuid (GH #1092)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1050">Implemented /proc/sys/kernel/random/uuid  (GH #1092)</span></span>
- <span data-ttu-id="1ff03-1051">更正了进程开始时间显示为 2432 年的错误 (GH #974)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1051">Corrected error where process start time was showing as year 2432 (GH #974)</span></span>
- <span data-ttu-id="1ff03-1052">已将默认 TERM 环境变量切换为 xterm-256color (GH #1446)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1052">Switched default TERM environment variable to xterm-256color (GH #1446)</span></span>
- <span data-ttu-id="1ff03-1053">修改了进程分叉期间进程提交的计算方式。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1053">Modified the way that process commit is calculated during process fork.</span></span> <span data-ttu-id="1ff03-1054">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1054">(GH #1286)</span></span>
- <span data-ttu-id="1ff03-1055">实现了 /proc/sys/vm/overcommit_memory。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1055">Implemented /proc/sys/vm/overcommit_memory.</span></span> <span data-ttu-id="1ff03-1056">(GH #1286)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1056">(GH #1286)</span></span>
- <span data-ttu-id="1ff03-1057">实现了 /proc/net/route 文件 (GH #69)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1057">Implemented /proc/net/route file (GH #69)</span></span>
- <span data-ttu-id="1ff03-1058">修复了不正确本地化快捷方式名称的错误 (GH #696)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1058">Fixed error where shortcut name was incorrectly localized (GH #696)</span></span>
- <span data-ttu-id="1ff03-1059">修复了错误地验证程序标头必须小于（或等于）PATH_MAX 的 elf 分析逻辑。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1059">Fixed elf parsing logic that is incorrectly validating the program headers must be less than (or equal to) PATH_MAX.</span></span> <span data-ttu-id="1ff03-1060">(GH #1048)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1060">(GH #1048)</span></span>
- <span data-ttu-id="1ff03-1061">为 procfs、sysfs、cgroupfs 和 binfmtfs 实现了 statfs 回调 (GH #1378)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1061">Implemented statfs callback for procfs, sysfs, cgroupfs, and binfmtfs (GH #1378)</span></span>
- <span data-ttu-id="1ff03-1062">修复了 AptPackageIndexUpdate 窗口不会关闭的问题（GH #1184，GH #1193 中也有描述）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1062">Fixed AptPackageIndexUpdate windows that won’t close (GH #1184, also discussed in GH #1193)</span></span>
- <span data-ttu-id="1ff03-1063">添加了 ASLR 个性化 ADDR_NO_RANDOMIZE 支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1063">Added ASLR personality  ADDR_NO_RANDOMIZE support.</span></span> <span data-ttu-id="1ff03-1064">（GH #1148、1128）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1064">(GH #1148, 1128)</span></span>
- <span data-ttu-id="1ff03-1065">改善了 PTRACE_GETSIGINFO、SIGSEGV，在 AV 期间会提供正确的 gdb 堆栈跟踪 (GH #875)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1065">Improved PTRACE_GETSIGINFO, SIGSEGV, for proper gdb stack traces during AV (GH #875)</span></span>
- <span data-ttu-id="1ff03-1066">针对 patchelf 二进制文件的 Elf 分析不再失败。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1066">Elf parsing no longer fails for patchelf binaries.</span></span> <span data-ttu-id="1ff03-1067">(GH #471)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1067">(GH #471)</span></span>
- <span data-ttu-id="1ff03-1068">VPN DNS 已传播到 /etc/resolv.conf（GH #416、1350）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1068">VPN DNS propagated to /etc/resolv.conf (GH #416, 1350)</span></span>
- <span data-ttu-id="1ff03-1069">TCP 关闭改进，可以更可靠地传输数据。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1069">Improvements to TCP close for more reliable data transfer.</span></span> <span data-ttu-id="1ff03-1070">（GH #610、616、1025、1335）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1070">(GH #610, 616, 1025, 1335)</span></span>
- <span data-ttu-id="1ff03-1071">现在，在打开过多的文件时可返回正确的错误代码 (EMFILE)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1071">Now return correct error code when too many files are opened (EMFILE).</span></span> <span data-ttu-id="1ff03-1072">（GH #1126、2090）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1072">(GH #1126, 2090)</span></span>
- <span data-ttu-id="1ff03-1073">Windows 审核日志现在会在进程创建审核中报告映像名称。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1073">Windows Audit log now reports the image name in process create audit.</span></span>
- <span data-ttu-id="1ff03-1074">现在，在从 bash 窗口内部启动 bash 时会正常失败</span><span class="sxs-lookup"><span data-stu-id="1ff03-1074">Now gracefully fail when launching bash.exe from within a bash window</span></span>
- <span data-ttu-id="1ff03-1075">添加了在 interop 无法访问 LxFs 下的工作目录（即 notepad.exe .bashrc）时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="1ff03-1075">Added error message when interop is unable to access a working directory under LxFs (i.e. notepad.exe .bashrc)</span></span>
- <span data-ttu-id="1ff03-1076">修复了 Windows 路径在 WSL 中截断的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1076">Fixed issue where Windows path was truncated in WSL</span></span>
- <span data-ttu-id="1ff03-1077">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1077">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1078">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1078">LTP Results:</span></span>
<span data-ttu-id="1ff03-1079">通过的测试数：690</span><span class="sxs-lookup"><span data-stu-id="1ff03-1079">Number of Passing Test: 690</span></span> </br>
<span data-ttu-id="1ff03-1080">未通过的测试数（失败、已跳过等）：274</span><span class="sxs-lookup"><span data-stu-id="1ff03-1080">Number of non-Passing (failing, skipped, etc…): 274</span></span> </br>
[<span data-ttu-id="1ff03-1081">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1081">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1082">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1082">Syscall Support</span></span>
<span data-ttu-id="1ff03-1083">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1083">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1084">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1084">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a><span data-ttu-id="1ff03-1085">内部版本 14986</span><span class="sxs-lookup"><span data-stu-id="1ff03-1085">Build 14986</span></span>

<span data-ttu-id="1ff03-1086">有关内部版本 14986 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1086">For general Windows information on build 14986 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1087">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1087">Fixed</span></span>

- <span data-ttu-id="1ff03-1088">修复了 Netlink 和 Pty IOCTL 的 bug 检查</span><span class="sxs-lookup"><span data-stu-id="1ff03-1088">Fixed bugchecks with Netlink and Pty IOCTLs</span></span>
- <span data-ttu-id="1ff03-1089">内核版本现在会报告 4.4.0-43，以便与 Xenial 保持一致</span><span class="sxs-lookup"><span data-stu-id="1ff03-1089">Kernel version now reports 4.4.0-43 for consistency with Xenial</span></span>
- <span data-ttu-id="1ff03-1090">现在，当输入定向到 'nul:' 时会启动 Bash.exe (GH #1259)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1090">Bash.exe now launches when input directed to 'nul:' (GH #1259)</span></span>
- <span data-ttu-id="1ff03-1091">现在，procfs 中会正确报告线程 ID (GH #967)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1091">Thread IDs now reported correctly in procfs (GH #967)</span></span>
- <span data-ttu-id="1ff03-1092">现在，inotify_add_watch() 中支持 IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR 标志 (GH #1280)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1092">IN_UNMOUNT | IN_Q_OVERFLOW | IN_IGNORED | IN_ISDIR flags now supported in inotify_add_watch() (GH #1280)</span></span>
- <span data-ttu-id="1ff03-1093">实现 timer_create 和相关的系统调用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1093">Implement timer_create and related system calls.</span></span>  <span data-ttu-id="1ff03-1094">这会启用 GHC 支持 (GH #307)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1094">This enables GHC support (GH #307)</span></span>
- <span data-ttu-id="1ff03-1095">修复了 ping 返回时间 0.000ms 的问题 (GH #1296)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1095">Fixed issue where ping returned a time of 0.000ms (GH #1296)</span></span>
- <span data-ttu-id="1ff03-1096">打开过多的文件时返回正确的错误代码。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1096">Return correct error code when too many files are opened.</span></span>
- <span data-ttu-id="1ff03-1097">修复了 WSL 中的问题：如果网络接口的硬件地址为 32 字节（例如 Teredo 接口），则针对该网络接口数据的 Netlink 请求将会失败并返回 EINVAL。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1097">Fixed issue in WSL where Netlink request for network interface data would fail with EINVAL if the interface's hardware address is 32-bytes (such as the Teredo interface)</span></span>
   - <span data-ttu-id="1ff03-1098">请注意，Linux“ip”实用工具包含一个 bug：如果 WSL 报告 32 字节硬件地址，该实用工具将会崩溃。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1098">Note that the Linux "ip" utility contains a bug where it will crash if WSL reports a 32-byte hardware address.</span></span> <span data-ttu-id="1ff03-1099">这是“ip”（而不是 WSL）中的一个 bug。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1099">This is a bug in "ip", not WSL.</span></span> <span data-ttu-id="1ff03-1100">“ip”实用工具会将用于输出硬件地址的字符串缓冲区的长度硬编码，而该缓冲区太小，无法输出 32 字节硬件地址。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1100">The “ip” utility hard-codes the length of the string buffer used to print the hardware address, and that buffer is too small to print a 32-byte hardware address.</span></span>
- <span data-ttu-id="1ff03-1101">其他修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1101">Additional fixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1102">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1102">LTP Results:</span></span>
<span data-ttu-id="1ff03-1103">通过的测试数：669</span><span class="sxs-lookup"><span data-stu-id="1ff03-1103">Number of Passing Test: 669</span></span> </br>
<span data-ttu-id="1ff03-1104">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="1ff03-1104">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="1ff03-1105">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1105">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1106">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1106">Syscall Support</span></span>
<span data-ttu-id="1ff03-1107">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1107">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1108">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1108">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a><span data-ttu-id="1ff03-1109">内部版本 14971</span><span class="sxs-lookup"><span data-stu-id="1ff03-1109">Build 14971</span></span>

<span data-ttu-id="1ff03-1110">有关内部版本 14971 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1110">For general Windows information on build 14971 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1111">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1111">Fixed</span></span>

 - <span data-ttu-id="1ff03-1112">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1112">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="1ff03-1113">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1113">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1114">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1114">LTP Results:</span></span>
<span data-ttu-id="1ff03-1115">自 14965 以来无更改</span><span class="sxs-lookup"><span data-stu-id="1ff03-1115">Unchanged from 14965</span></span> </br>
<span data-ttu-id="1ff03-1116">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="1ff03-1116">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="1ff03-1117">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1117">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1118">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1118">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a><span data-ttu-id="1ff03-1119">内部版本 14965</span><span class="sxs-lookup"><span data-stu-id="1ff03-1119">Build 14965</span></span>

<span data-ttu-id="1ff03-1120">有关内部版本 14965 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1120">For general Windows information on build 14965 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1121">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1121">Fixed</span></span>

- <span data-ttu-id="1ff03-1122">支持 Netlink 套接字 NETLINK_ROUTE 协议的 RTM_GETLINK 和 RTM_GETADDR (GH #468)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1122">Support for Netlink sockets NETLINK_ROUTE protocol's RTM_GETLINK and RTM_GETADDR (GH #468)</span></span>
  - <span data-ttu-id="1ff03-1123">为网络枚举启用 ifconfig 和 ip 命令</span><span class="sxs-lookup"><span data-stu-id="1ff03-1123">Enables ifconfig and ip commands for network enumeration</span></span>
  - <span data-ttu-id="1ff03-1124">在 [WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)中可以找到详细信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1124">More information can be found in our [WSL Networking blog post](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/).</span></span>

- <span data-ttu-id="1ff03-1125">/sbin 现在默认位于用户的路径中</span><span class="sxs-lookup"><span data-stu-id="1ff03-1125">/sbin is now in the user's path by default</span></span>
- <span data-ttu-id="1ff03-1126">NT 用户路径现在默认会追加到 WSL 路径（即，现在可以键入 notepad.exe，无需将 System32 添加到 Linux 路径）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1126">NT user path now appended to the WSL path by default (i.e. you can now type notepad.exe without adding System32 to the Linux path)</span></span>
- <span data-ttu-id="1ff03-1127">添加了对 /proc/sys/kernel/cap_last_cap 的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1127">Added support for /proc/sys/kernel/cap_last_cap</span></span>
- <span data-ttu-id="1ff03-1128">现在，如果当前工作目录包含非 ANSI 字符，则可以从 WSL 启动 NT 二进制文件 (GH #1254)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1128">NT Binaries can now be launched from WSL when the current working directory contains non-ansi characters (GH #1254)</span></span>
- <span data-ttu-id="1ff03-1129">允许在断开连接的 unix 流套接字上关闭。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1129">Allow shutdown on disconnected unix stream socket.</span></span>
- <span data-ttu-id="1ff03-1130">添加了对 PR_GET_PDEATHSIG 的支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1130">Added support for PR_GET_PDEATHSIG.</span></span>
- <span data-ttu-id="1ff03-1131">添加了对 CLONE_PARENT 的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1131">Added support for CLONE_PARENT</span></span>
- <span data-ttu-id="1ff03-1132">修复了运行 bash -c "ls -alR /" | bash -c "cat" 时管道停滞的错误 (GH #1214)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1132">Fixed error where piping gets stuck i.e. bash -c "ls -alR /" | bash -c "cat" (GH #1214)</span></span>
- <span data-ttu-id="1ff03-1133">处理连接到当前终端的请求。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1133">Handle requests to connect to the current terminal.</span></span>
- <span data-ttu-id="1ff03-1134">将 /proc/<pid>/oom_score_adj 标记为可写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1134">Mark /proc/<pid>/oom_score_adj as writable.</span></span>
- <span data-ttu-id="1ff03-1135">添加 /sys/fs/cgroup 文件夹。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1135">Add /sys/fs/cgroup folder.</span></span>
- <span data-ttu-id="1ff03-1136">sched_setaffinity 应返回关联位掩码的数目</span><span class="sxs-lookup"><span data-stu-id="1ff03-1136">sched_setaffinity should return number of affinity bits mask</span></span>
- <span data-ttu-id="1ff03-1137">修复错误地假设解释器路径长度必须小于 64 个字符的 ELF 验证逻辑。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1137">Fix ELF validation logic which incorrectly assumes interpreter paths must be less than 64 characters long.</span></span> <span data-ttu-id="1ff03-1138">(GH #743)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1138">(GH #743)</span></span>
- <span data-ttu-id="1ff03-1139">打开文件描述符会使控制台窗口保持打开状态 (GH #1187)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1139">Open file descriptors can keep console window open (GH #1187)</span></span>
- <span data-ttu-id="1ff03-1140">修复了当目标名称包含尾随斜杠时 rename() 失败的错误 (GH #1008)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1140">Fixeed error where rename() failed with trailing slash on target name (GH #1008)</span></span>
- <span data-ttu-id="1ff03-1141">实现 /proc/net/dev 文件</span><span class="sxs-lookup"><span data-stu-id="1ff03-1141">Implement /proc/net/dev file</span></span>
- <span data-ttu-id="1ff03-1142">修复了计时器精度导致的 0.000ms ping 错误。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1142">Fixed 0.000ms pings due to timer resolution.</span></span>
- <span data-ttu-id="1ff03-1143">实现了 /proc/self/environ (GH #730)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1143">Implemented /proc/self/environ (GH #730)</span></span>
- <span data-ttu-id="1ff03-1144">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1144">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1145">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1145">LTP Results:</span></span>
<span data-ttu-id="1ff03-1146">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="1ff03-1146">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="1ff03-1147">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1147">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1148">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1148">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a><span data-ttu-id="1ff03-1149">内部版本 14959</span><span class="sxs-lookup"><span data-stu-id="1ff03-1149">Build 14959</span></span>

<span data-ttu-id="1ff03-1150">有关内部版本 14959 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1150">For general Windows information on build 14959 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1151">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1151">Fixed</span></span>

- <span data-ttu-id="1ff03-1152">改善了 Windows 的 Pico 进程通知。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1152">Improved Pico Process notification for Windows.</span></span>  <span data-ttu-id="1ff03-1153">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)中可以找到更多信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1153">Additional information found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/).</span></span>
- <span data-ttu-id="1ff03-1154">改善了 Windows 互操作的稳定性</span><span class="sxs-lookup"><span data-stu-id="1ff03-1154">Improved stability with Windows interoperability</span></span>
- <span data-ttu-id="1ff03-1155">修复了在启用企业数据保护 (EDP) 后启动 bash.exe 时出现的错误 0x80070057</span><span class="sxs-lookup"><span data-stu-id="1ff03-1155">Fixed error 0x80070057 when launching bash.exe when Enterprise Data Protection (EDP) is enabled</span></span>
- <span data-ttu-id="1ff03-1156">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1156">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1157">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1157">LTP Results:</span></span>
<span data-ttu-id="1ff03-1158">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="1ff03-1158">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="1ff03-1159">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1159">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1160">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1160">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a><span data-ttu-id="1ff03-1161">内部版本 14955</span><span class="sxs-lookup"><span data-stu-id="1ff03-1161">Build 14955</span></span>

<span data-ttu-id="1ff03-1162">有关内部版本 14955 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1162">For general Windows information on build 14955 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1163">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1163">Fixed</span></span>

 - <span data-ttu-id="1ff03-1164">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1164">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="1ff03-1165">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1165">Regularly scheduled updates will resume on the next release.</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1166">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1166">LTP Results:</span></span>
<span data-ttu-id="1ff03-1167">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="1ff03-1167">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="1ff03-1168">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1168">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1169">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1169">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a><span data-ttu-id="1ff03-1170">内部版本 14951</span><span class="sxs-lookup"><span data-stu-id="1ff03-1170">Build 14951</span></span>

<span data-ttu-id="1ff03-1171">有关内部版本 14951 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1171">For general Windows information on build 14951 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/).</span></span><br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a><span data-ttu-id="1ff03-1172">新功能：Windows/Ubuntu 互操作性</span><span class="sxs-lookup"><span data-stu-id="1ff03-1172">New Feature: Windows / Ubuntu Interoperability</span></span>
<span data-ttu-id="1ff03-1173">现在可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1173">Windows binaries can now be invoked directly from the WSL command line.</span></span>  <span data-ttu-id="1ff03-1174">这样，用户便可以通过前所未有的方式来与其 Windows 环境和系统交互。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1174">This gives users the ability to interact with their Windows environment and system in a way that has not been possible.</span></span>  <span data-ttu-id="1ff03-1175">举个简单的例子，用户现在可以运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1175">As a quick example, it is now possible for users to run the following commands:</span></span>

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

<span data-ttu-id="1ff03-1176">可在以下资源中找到详细信息：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1176">More information can be found at:</span></span>

- [<span data-ttu-id="1ff03-1177">WSL 团队的互操作博客</span><span class="sxs-lookup"><span data-stu-id="1ff03-1177">WSL Team Blog for Interop</span></span>](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [<span data-ttu-id="1ff03-1178">MSDN 互操作文档</span><span class="sxs-lookup"><span data-stu-id="1ff03-1178">MSDN Interop Documentation</span></span>](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1179">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1179">Fixed</span></span>

- <span data-ttu-id="1ff03-1180">现在将为所有新的 WSL 实例安装 Ubuntu 16.04 (Xenial)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1180">Ubuntu 16.04 (Xenial) is now installed for all new WSL instances.</span></span>  <span data-ttu-id="1ff03-1181">使用现有 14.04 (Trusty) 实例的用户不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1181">Users with existing 14.04 (Trusty) instances will not be automatically upgraded.</span></span>
- <span data-ttu-id="1ff03-1182">现在会显示安装过程中指定的区域设置</span><span class="sxs-lookup"><span data-stu-id="1ff03-1182">Locale set during install is now displayed</span></span>
- <span data-ttu-id="1ff03-1183">终端改进，包括修复了不是总能将 WSL 进程重定向到文件的 bug</span><span class="sxs-lookup"><span data-stu-id="1ff03-1183">Terminal improvements including bug where redirecting a WSL process to a file does not always work</span></span>
- <span data-ttu-id="1ff03-1184">控制台生存期应与 bash.exe 生存期密切关联</span><span class="sxs-lookup"><span data-stu-id="1ff03-1184">Console lifetime should be tied to bash.exe lifetime</span></span>
- <span data-ttu-id="1ff03-1185">控制台窗口大小应使用可视大小，而不是缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="1ff03-1185">Console window size should use visible size, not buffer size</span></span>
- <span data-ttu-id="1ff03-1186">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1186">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1187">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1187">LTP Results:</span></span>
<span data-ttu-id="1ff03-1188">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="1ff03-1188">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="1ff03-1189">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1189">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1190">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1190">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a><span data-ttu-id="1ff03-1191">内部版本 14946</span><span class="sxs-lookup"><span data-stu-id="1ff03-1191">Build 14946</span></span>

<span data-ttu-id="1ff03-1192">有关内部版本 14946 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1192">For general Windows information on build 14946 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1193">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1193">Fixed</span></span>

- <span data-ttu-id="1ff03-1194">修复了阻止使用包含空格或引号的 NT 用户名为用户创建 WSL 用户帐户的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1194">Fixed an issue that prevented creating WSL user accounts for users with NT usernames that contain spaces or quotes.</span></span> 
- <span data-ttu-id="1ff03-1195">更改 VolFs 和 DrvFs，以在统计信息中返回 0 作为目录的链接计数</span><span class="sxs-lookup"><span data-stu-id="1ff03-1195">Change VolFs and DrvFs to return 0 for directory's link count in stat</span></span>
- <span data-ttu-id="1ff03-1196">支持 IPV6_MULTICAST_HOPS 套接字选项。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1196">Support IPV6_MULTICAST_HOPS socket option.</span></span>
- <span data-ttu-id="1ff03-1197">限制为每个 tty 只有一个控制台 I/O 循环。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1197">Limit to a single console I/O loop per tty.</span></span> <span data-ttu-id="1ff03-1198">例如，可运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1198">Example: the following command is possible:</span></span>
  - <span data-ttu-id="1ff03-1199">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span><span class="sxs-lookup"><span data-stu-id="1ff03-1199">bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"</span></span>

- <span data-ttu-id="1ff03-1200">在 /proc/cpuinfo 中将空格替换为制表符 (GH #1115)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1200">replace spaces with tabs in /proc/cpuinfo (GH #1115)</span></span>
- <span data-ttu-id="1ff03-1201">DrvFs 现在会显示在 mountinfo 中，其中包含一个与已装载的 Windows 卷匹配的名称</span><span class="sxs-lookup"><span data-stu-id="1ff03-1201">DrvFs now appears in mountinfo with a name that matches mounted Windows volume</span></span>
- <span data-ttu-id="1ff03-1202">/home 和 /root 现在会显示在 mountinfo 中，并显示正确的名称</span><span class="sxs-lookup"><span data-stu-id="1ff03-1202">/home and /root now appear in mountinfo with correct names</span></span>
- <span data-ttu-id="1ff03-1203">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1203">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1204">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1204">LTP Results:</span></span>
<span data-ttu-id="1ff03-1205">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="1ff03-1205">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="1ff03-1206">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1206">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1207">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1207">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a><span data-ttu-id="1ff03-1208">内部版本 14942</span><span class="sxs-lookup"><span data-stu-id="1ff03-1208">Build 14942</span></span>

<span data-ttu-id="1ff03-1209">有关内部版本 14942 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/onefourninefourtwoooooo)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1209">For general Windows information on build 14942 visit the [Windows Blog](https://aka.ms/onefourninefourtwoooooo).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1210">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1210">Fixed</span></span>

- <span data-ttu-id="1ff03-1211">解决了一些 bug 检查，包括阻止 SSH 的“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”网络崩溃</span><span class="sxs-lookup"><span data-stu-id="1ff03-1211">A number of bugchecks addressed, including the “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY” networking crash which was blocking SSH</span></span>
- <span data-ttu-id="1ff03-1212">inotifiy 现在支持从 DrvFs 上的 Windows 应用程序生成通知</span><span class="sxs-lookup"><span data-stu-id="1ff03-1212">inotifiy support for notifications generated from Windows applications on DrvFs is now in</span></span>
- <span data-ttu-id="1ff03-1213">实现 mongod 的 TCP_KEEPIDLE 和 TCP_KEEPINTVL。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1213">Implement TCP_KEEPIDLE and TCP_KEEPINTVL for mongod.</span></span> <span data-ttu-id="1ff03-1214">(GH #695)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1214">(GH #695)</span></span>
- <span data-ttu-id="1ff03-1215">实现 pivot_root 系统调用</span><span class="sxs-lookup"><span data-stu-id="1ff03-1215">Implement the pivot_root system call</span></span>
- <span data-ttu-id="1ff03-1216">实现 SO_DONTROUTE 的套接字选项</span><span class="sxs-lookup"><span data-stu-id="1ff03-1216">Implement socket option for SO_DONTROUTE</span></span>
- <span data-ttu-id="1ff03-1217">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1217">Additional bugfixes and improvements</span></span>


### <a name="ltp-results"></a><span data-ttu-id="1ff03-1218">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1218">LTP Results:</span></span>
<span data-ttu-id="1ff03-1219">通过的测试数：665</span><span class="sxs-lookup"><span data-stu-id="1ff03-1219">Number of Passing Test: 665</span></span> </br>
<span data-ttu-id="1ff03-1220">未通过的测试数（失败、已跳过等）：263</span><span class="sxs-lookup"><span data-stu-id="1ff03-1220">Number of non-Passing (failing, skipped, etc…): 263</span></span> </br>
[<span data-ttu-id="1ff03-1221">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1221">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1222">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1222">Syscall Support</span></span>
<span data-ttu-id="1ff03-1223">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1223">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1224">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1224">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a><span data-ttu-id="1ff03-1225">内部版本 14936</span><span class="sxs-lookup"><span data-stu-id="1ff03-1225">Build 14936</span></span>

<span data-ttu-id="1ff03-1226">有关内部版本 14936 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1226">For general Windows information on build 14936 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/).</span></span><br/>


<span data-ttu-id="1ff03-1227">注意：在即将发布的版本中，WSL 将会安装 Ubuntu 版本16.04 (Xenial) 而不是 Ubuntu 14.04 (Trusty)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1227">Note: WSL will install Ubuntu version 16.04 (Xenial) instead of Ubuntu 14.04 (Trusty) in an upcoming release.</span></span>  <span data-ttu-id="1ff03-1228">此更改将应用到安装新实例的预览体验版（lxrun /install 或首次运行 bash.exe）。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1228">This change will apply to Insiders installing new instances (lxrun.exe /install or first run of bash.exe).</span></span>  <span data-ttu-id="1ff03-1229">包含 Trusty 的现有实例不会自动升级。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1229">Existing instances with Trusty will not be upgraded automatically.</span></span> <span data-ttu-id="1ff03-1230">用户可以使用 do-release-upgrade 命令将其 Trusty 映像升级到 Xenial。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1230">Users can upgrade their Trusty image to Xenial using the do-release-upgrade command.</span></span>

### <a name="known-issue"></a><span data-ttu-id="1ff03-1231">已知问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1231">Known Issue</span></span>
<span data-ttu-id="1ff03-1232">WSL 遇到了某些套接字实现的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1232">WSL is experiencing an issue with some socket implementations.</span></span>  <span data-ttu-id="1ff03-1233">bug 检查将自身显示为崩溃，并出现错误“ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1233">The bugcheck manifests itself as a crash with the error “ATTEMPTED EXECUTE OF NOEXECUTE MEMORY”.</span></span>  <span data-ttu-id="1ff03-1234">此问题的最常见表现形式是使用 ssh 时发生崩溃。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1234">The most common manifestation of this issue is a crash when using ssh.</span></span>  <span data-ttu-id="1ff03-1235">根本原因已在内部版本中修复，将会尽快推送到预览体验版。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1235">The root cause is fixed on internal builds and will be pushed to Insiders at the earliest opportunity.</span></span>

### <a name="fixed"></a><span data-ttu-id="1ff03-1236">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1236">Fixed</span></span>

- <span data-ttu-id="1ff03-1237">实现了 chroot 系统调用</span><span class="sxs-lookup"><span data-stu-id="1ff03-1237">Implemented the chroot system call</span></span>
- <span data-ttu-id="1ff03-1238">inotifiy 的改进，~~包括支持从 DrvFs 上的 Windows 应用程序生成通知~~</span><span class="sxs-lookup"><span data-stu-id="1ff03-1238">Improvements in inotify ~~including support for notifications generated from Windows applications on DrvFs~~</span></span>
  - <span data-ttu-id="1ff03-1239">更正：对源自 Windows 应用程序的更改的 Inotify 支持目前不可用。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1239">Correction: Inotify support for changes originating from Windows applications not available at this time.</span></span>
- <span data-ttu-id="1ff03-1240">与 IPV6::<port n> 的套接字绑定现在支持 IPV6_V6ONLY（GH #68、#157、#393、#460、#674、#740、#982、#996）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1240">Socket binding to IPV6::<port n> now supports IPV6_V6ONLY  (GH #68, #157, #393, #460, #674, #740, #982, #996)</span></span>
- <span data-ttu-id="1ff03-1241">实现了 waitid 系统调用的 WNOWAIT 行为 (GH #638)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1241">WNOWAIT behavior for waitid systemcall implemented (GH #638)</span></span>
- <span data-ttu-id="1ff03-1242">支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL</span><span class="sxs-lookup"><span data-stu-id="1ff03-1242">Support for IP socket options IP_HDRINCL and IP_TTL</span></span>
- <span data-ttu-id="1ff03-1243">零长度 read() 应立即返回 (GH #975)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1243">Zero-length read() should return immediately (GH #975)</span></span>
- <span data-ttu-id="1ff03-1244">在 .tar 文件中正确处理不包含 NULL 终止符的文件名和文件名前缀。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1244">Correctly handle filenames and filename prefixes that don't include a NULL terminator in a .tar file.</span></span>
- <span data-ttu-id="1ff03-1245">对 /dev/null 的 epoll 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1245">epoll support for /dev/null</span></span>
- <span data-ttu-id="1ff03-1246">修复 /dev/alarm 时间源</span><span class="sxs-lookup"><span data-stu-id="1ff03-1246">Fix /dev/alarm time source</span></span>
- <span data-ttu-id="1ff03-1247">Bash -c 现在可以重定向到文件</span><span class="sxs-lookup"><span data-stu-id="1ff03-1247">Bash -c now able to redirect to a file</span></span>
- <span data-ttu-id="1ff03-1248">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1248">Additional bugfixes and improvements</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1249">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1249">LTP Results:</span></span>
<span data-ttu-id="1ff03-1250">通过的测试数：664</span><span class="sxs-lookup"><span data-stu-id="1ff03-1250">Number of Passing Test: 664</span></span> </br>
<span data-ttu-id="1ff03-1251">未通过的测试数（失败、已跳过等）：264</span><span class="sxs-lookup"><span data-stu-id="1ff03-1251">Number of non-Passing (failing, skipped, etc…): 264</span></span> </br>
[<span data-ttu-id="1ff03-1252">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1252">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1253">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1253">Syscall Support</span></span>
<span data-ttu-id="1ff03-1254">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1254">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1255">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1255">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`chroot`<br/>
<br/>

## <a name="build-14931"></a><span data-ttu-id="1ff03-1256">内部版本 14931</span><span class="sxs-lookup"><span data-stu-id="1ff03-1256">Build 14931</span></span>

<span data-ttu-id="1ff03-1257">有关内部版本 14931 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1257">For general Windows information on build 14931 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1258">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1258">Fixed</span></span>

 - <span data-ttu-id="1ff03-1259">由于这种情况超出了我们的控制，在此内部版本的适用于 Linux 的 Windows 子系统中未做更新。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1259">Due to circumstances beyond our control there are no updates in this build for the Windows Subsystem for Linux.</span></span>  <span data-ttu-id="1ff03-1260">定期计划的更新将在下一版本中恢复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1260">Regularly scheduled updates will resume in the next release.</span></span>

<br/>

## <a name="build-14926"></a><span data-ttu-id="1ff03-1261">内部版本 14926</span><span class="sxs-lookup"><span data-stu-id="1ff03-1261">Build 14926</span></span>

<span data-ttu-id="1ff03-1262">有关内部版本 14926 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1262">For general Windows information on build 14926 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1263">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1263">Fixed</span></span>

- <span data-ttu-id="1ff03-1264">Ping 现在可以在没有管理员特权的控制台中正常运行</span><span class="sxs-lookup"><span data-stu-id="1ff03-1264">Ping now works in consoles which do not have administrator privileges</span></span>
- <span data-ttu-id="1ff03-1265">现在支持 Ping6，也无需管理员特权</span><span class="sxs-lookup"><span data-stu-id="1ff03-1265">Ping6 now supported, also without administrator privileges</span></span>
- <span data-ttu-id="1ff03-1266">对通过 WSL 修改的文件的 Inotify 支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1266">Inotify support for files modified through WSL.</span></span> <span data-ttu-id="1ff03-1267">(GH #216)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1267">(GH #216)</span></span>
  - <span data-ttu-id="1ff03-1268">支持的标志：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1268">Flags supported:</span></span>
    - <span data-ttu-id="1ff03-1269">inotify_init1：LX_O_CLOEXEC、LX_O_NONBLOCK</span><span class="sxs-lookup"><span data-stu-id="1ff03-1269">inotify_init1: LX_O_CLOEXEC, LX_O_NONBLOCK</span></span>
    - <span data-ttu-id="1ff03-1270">inotify_add_watch 事件：LX_IN_ACCESS、LX_IN_MODIFY、LX_IN_ATTRIB、LX_IN_CLOSE_WRITE、LX_IN_CLOSE_NOWRITE、LX_IN_OPEN、LX_IN_MOVED_FROM、LX_IN_MOVED_TO、LX_IN_CREATE、LX_IN_DELETE、LX_IN_DELETE_SELF、LX_IN_MOVE_SELF</span><span class="sxs-lookup"><span data-stu-id="1ff03-1270">inotify_add_watch events: LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF</span></span>
    - <span data-ttu-id="1ff03-1271">inotify_add_watch 属性：LX_IN_DONT_FOLLOW、LX_IN_EXCL_UNLINK、LX_IN_MASK_ADD、LX_IN_ONESHOT、LX_IN_ONLYDIR</span><span class="sxs-lookup"><span data-stu-id="1ff03-1271">inotify_add_watch attributes: LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR</span></span>
    - <span data-ttu-id="1ff03-1272">读取输出：LX_IN_ISDIR、LX_IN_IGNORED</span><span class="sxs-lookup"><span data-stu-id="1ff03-1272">read output: LX_IN_ISDIR, LX_IN_IGNORED</span></span>
  - <span data-ttu-id="1ff03-1273">已知问题：修改 Windows 应用程序中的文件不会生成任何事件</span><span class="sxs-lookup"><span data-stu-id="1ff03-1273">Known issue: Modifying files from Windows applications does not generate any events</span></span>
- <span data-ttu-id="1ff03-1274">Unix 套接字现在支持 SCM_CREDENTIALS</span><span class="sxs-lookup"><span data-stu-id="1ff03-1274">Unix socket now supports SCM_CREDENTIALS</span></span>

### <a name="ltp-results"></a><span data-ttu-id="1ff03-1275">LTP 结果：</span><span class="sxs-lookup"><span data-stu-id="1ff03-1275">LTP Results:</span></span>
<span data-ttu-id="1ff03-1276">通过的测试数：651</span><span class="sxs-lookup"><span data-stu-id="1ff03-1276">Number of Passing Test: 651</span></span> </br>
<span data-ttu-id="1ff03-1277">未通过的测试数（失败、已跳过等）：258</span><span class="sxs-lookup"><span data-stu-id="1ff03-1277">Number of non-Passing (failing, skipped, etc…): 258</span></span> </br>
[<span data-ttu-id="1ff03-1278">LTP 测试运行日志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1278">LTP Test Run Logs</span></span>](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a><span data-ttu-id="1ff03-1279">内部版本 14915</span><span class="sxs-lookup"><span data-stu-id="1ff03-1279">Build 14915</span></span>

<span data-ttu-id="1ff03-1280">有关内部版本 14915 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1280">For general Windows information on build 14915 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1281">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1281">Fixed</span></span>
-  <span data-ttu-id="1ff03-1282">Unix 数据报套接字的套接字对 (GH #262)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1282">Socketpair for unix datagram sockets (GH #262)</span></span>
- <span data-ttu-id="1ff03-1283">对 SO_REUSEADDR 的 Unix 套接字支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1283">Unix socket support for SO_REUSEADDR</span></span>
- <span data-ttu-id="1ff03-1284">对 SO_BROADCAST 的 UNIX 套接字支持 (GH #568)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1284">UNIX socket support for SO_BROADCAST (GH #568)</span></span>
- <span data-ttu-id="1ff03-1285">对 SOCK_SEQPACKET 的 Unix 套接字支持（GH #758、#546）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1285">Unix socket support for SOCK_SEQPACKET (GH #758, #546)</span></span>
- <span data-ttu-id="1ff03-1286">添加对 Unix 数据报套接字 send、recv 和 shutdown 的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1286">Adding support for unix datagram socket send, recv and shutdown</span></span>
- <span data-ttu-id="1ff03-1287">修复对非固定地址的无效 mmap 参数验证导致的 bug 检查。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1287">Fix bugcheck due to invalid mmap parameter validation for non-fixed addresses.</span></span> <span data-ttu-id="1ff03-1288">(GH #847)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1288">(GH #847)</span></span>
- <span data-ttu-id="1ff03-1289">支持暂停/恢复终端状态</span><span class="sxs-lookup"><span data-stu-id="1ff03-1289">Support for suspend / resume of terminal states</span></span>
- <span data-ttu-id="1ff03-1290">支持使用 TIOCPKT ioctl 阻止 Screen 实用工具 (GH #774)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1290">Support for TIOCPKT ioctl to unblock the Screen utility (GH #774)</span></span>
    - <span data-ttu-id="1ff03-1291">已知问题：功能键不起作用</span><span class="sxs-lookup"><span data-stu-id="1ff03-1291">Known issue: Function keys not operational</span></span>
- <span data-ttu-id="1ff03-1292">更正了 TimerFd 中的一种争用状态，该状态可能导致 LxpTimerFdWorkerRoutine 访问已释放的成员“ReaderReady” (GH #814)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1292">Corrected a race in TimerFd that could cause a freed member 'ReaderReady' to be accessed by LxpTimerFdWorkerRoutine (GH #814)</span></span>
- <span data-ttu-id="1ff03-1293">为 futex、poll 和 clock_nanosleep 启用可重启系统调用支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1293">Enable restartable system call support for futex, poll, and clock_nanosleep</span></span>
- <span data-ttu-id="1ff03-1294">添加了绑定装载支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1294">Added bind mount support</span></span>
- <span data-ttu-id="1ff03-1295">装载命名空间支持的取消共享</span><span class="sxs-lookup"><span data-stu-id="1ff03-1295">unshare for mount namespace support</span></span>
    - <span data-ttu-id="1ff03-1296">已知问题：使用 `unshare(CLONE_NEWNS)` 创建新的装载命名空间时，当前工作目录将继续指向旧命名空间</span><span class="sxs-lookup"><span data-stu-id="1ff03-1296">Known issue: When creating a new mount namespace with `unshare(CLONE_NEWNS)` the current working directory will continue to point to the old namespace</span></span>
- <span data-ttu-id="1ff03-1297">其他改进和 bug 修复</span><span class="sxs-lookup"><span data-stu-id="1ff03-1297">Additional improvements and bug fixes</span></span>

<br/>

## <a name="build-14905"></a><span data-ttu-id="1ff03-1298">内部版本 14905</span><span class="sxs-lookup"><span data-stu-id="1ff03-1298">Build 14905</span></span>

<span data-ttu-id="1ff03-1299">有关内部版本 14905 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1299">For general Windows information on build 14905 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1300">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1300">Fixed</span></span>
- <span data-ttu-id="1ff03-1301">现在支持可重启系统调用（GH #349、GH #520）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1301">Restartable system calls are now supported (GH #349, GH #520)</span></span>
- <span data-ttu-id="1ff03-1302">现在可正常使用指向以 / 结尾的目录的符号链接 (GH #650)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1302">Symlinks to directories ending in / now operational (GH #650)</span></span>
- <span data-ttu-id="1ff03-1303">为 /dev/random 实现了 RNDGETENTCNT ioctl</span><span class="sxs-lookup"><span data-stu-id="1ff03-1303">Implemented RNDGETENTCNT ioctl for /dev/random</span></span>
- <span data-ttu-id="1ff03-1304">实现了 /proc/[pid]/mounts、/proc/[pid]/mountinfo 和 /proc/[pid]/mountstats 文件</span><span class="sxs-lookup"><span data-stu-id="1ff03-1304">Implemented the /proc/[pid]/mounts, /proc/[pid]/mountinfo and /proc/[pid]/mountstats files</span></span>
- <span data-ttu-id="1ff03-1305">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1305">Additional bugfixes and improvements</span></span>

</br>

## <a name="build-14901"></a><span data-ttu-id="1ff03-1306">内部版本 14901</span><span class="sxs-lookup"><span data-stu-id="1ff03-1306">Build 14901</span></span>
<span data-ttu-id="1ff03-1307">Windows 10 周年更新版的第一个预览体验内部版本。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1307">First Insider build for the post Windows 10 Anniversary Update release.</span></span>

<span data-ttu-id="1ff03-1308">有关内部版本 14901 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1308">For general Windows information on build 14901 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1309">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1309">Fixed</span></span>
- <span data-ttu-id="1ff03-1310">修复了尾随斜杠问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1310">Fixed trailing slash issue</span></span>
    - <span data-ttu-id="1ff03-1311">`$ mv a/c/ a/b/` 等命令现在可正常运行</span><span class="sxs-lookup"><span data-stu-id="1ff03-1311">Commands such as `$ mv a/c/ a/b/` now work</span></span>
- <span data-ttu-id="1ff03-1312">安装程序现在会提示是否应将 Ubuntu 区域设置指定为 Windows 区域设置</span><span class="sxs-lookup"><span data-stu-id="1ff03-1312">Installing now prompts if Ubuntu locale should be set to Windows locale</span></span>
- <span data-ttu-id="1ff03-1313">对 ns 文件夹的 Procfs 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1313">Procfs support for ns folder</span></span>
- <span data-ttu-id="1ff03-1314">添加了 tmpfs、procfs 和 sysfs 文件系统的装入点和卸载点</span><span class="sxs-lookup"><span data-stu-id="1ff03-1314">Added mount and unmount for tmpfs, procfs and sysfs file systems</span></span>
- <span data-ttu-id="1ff03-1315">修复 mknod [at] 32 位 ABI 签名</span><span class="sxs-lookup"><span data-stu-id="1ff03-1315">Fix mknod[at] 32-bit ABI signature</span></span>
- <span data-ttu-id="1ff03-1316">Unix 套接字已移到调度模型</span><span class="sxs-lookup"><span data-stu-id="1ff03-1316">Unix sockets moved to dispatch model</span></span>
- <span data-ttu-id="1ff03-1317">应遵循使用 setsockopt 设置的 INET 套接字接收缓冲区大小</span><span class="sxs-lookup"><span data-stu-id="1ff03-1317">INET socket recv buffer size set using the setsockopt should be honored</span></span>
- <span data-ttu-id="1ff03-1318">实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志</span><span class="sxs-lookup"><span data-stu-id="1ff03-1318">Implement MSG_CMSG_CLOEXEC unix socket receive message flag</span></span>
- <span data-ttu-id="1ff03-1319">Linux 进程 stdin/stdout 管道重定向 (GH #2)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1319">Linux process stdin/stdout pipe redirection (GH #2)</span></span>
    - <span data-ttu-id="1ff03-1320">允许在 CMD 中使用竖线分隔 bash -c 命令。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1320">Allows for piping of bash -c commands in CMD.</span></span>  <span data-ttu-id="1ff03-1321">示例：>dir | bash -c "grep foo"</span><span class="sxs-lookup"><span data-stu-id="1ff03-1321">Example:  >dir | bash -c "grep foo"</span></span>
- <span data-ttu-id="1ff03-1322">Bash 现在可以安装在包含多个页面文件的系统上（GH #538、#358）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1322">Bash can now be installed on systems with multiple pagefiles (GH #538, #358)</span></span>
- <span data-ttu-id="1ff03-1323">默认的 INET 套接字缓冲区大小应与默认 Ubuntu 安装的大小相匹配</span><span class="sxs-lookup"><span data-stu-id="1ff03-1323">Default INET Socket buffer size should match that of default Ubuntu setup</span></span>
- <span data-ttu-id="1ff03-1324">将 xattr syscall 与 listxattr 对齐</span><span class="sxs-lookup"><span data-stu-id="1ff03-1324">Align xattr syscalls to listxattr</span></span>
- <span data-ttu-id="1ff03-1325">仅返回使用 SIOCGIFCONF 中有效 IPv4 地址的接口</span><span class="sxs-lookup"><span data-stu-id="1ff03-1325">Only return interfaces with a valid IPv4 address from SIOCGIFCONF</span></span>
- <span data-ttu-id="1ff03-1326">修复 ptrace 注入时的信号默认操作</span><span class="sxs-lookup"><span data-stu-id="1ff03-1326">Fix signal default action when injected by ptrace</span></span>
- <span data-ttu-id="1ff03-1327">实现 /proc/sys/vm/min_free_kbytes</span><span class="sxs-lookup"><span data-stu-id="1ff03-1327">implement /proc/sys/vm/min_free_kbytes</span></span>
- <span data-ttu-id="1ff03-1328">在 sigreturn 中还原上下文时使用计算机上下文寄存器值</span><span class="sxs-lookup"><span data-stu-id="1ff03-1328">Use machine context register values when restoring context in sigreturn</span></span>
    - <span data-ttu-id="1ff03-1329">这解决了某些用户遇到的 java 和 javac 挂起问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1329">This resolves the issue where java and javac were hanging for some users</span></span>
- <span data-ttu-id="1ff03-1330">实现 /proc/sys/kernel/hostname</span><span class="sxs-lookup"><span data-stu-id="1ff03-1330">Implement /proc/sys/kernel/hostname</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1331">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1331">Syscall Support</span></span>
<span data-ttu-id="1ff03-1332">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1332">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1333">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1333">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a><span data-ttu-id="1ff03-1334">Windows 10 周年更新的内部版本 14388</span><span class="sxs-lookup"><span data-stu-id="1ff03-1334">Build 14388 to Windows 10 Anniversary Update</span></span>
<span data-ttu-id="1ff03-1335">有关内部版本 14388 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/14388wip)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1335">For general Windows information on build 14388 visit the [Windows Blog](https://aka.ms/14388wip).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1336">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1336">Fixed</span></span>
- <span data-ttu-id="1ff03-1337">修复在 8/2 准备 Windows 10 周年更新时出现的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1337">Fixes to prepare for the Windows 10 Anniversary Update on 8/2</span></span>
  - <span data-ttu-id="1ff03-1338">可在我们的[博客](https://blogs.msdn.microsoft.com/wsl/)中找到有关周年更新中的 WSL 的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1338">More information about WSL in the Anniversary Update can be found on our [blog](https://blogs.msdn.microsoft.com/wsl/)</span></span>

<br/>

## <a name="build-14376"></a><span data-ttu-id="1ff03-1339">内部版本 14376</span><span class="sxs-lookup"><span data-stu-id="1ff03-1339">Build 14376</span></span>
<span data-ttu-id="1ff03-1340">有关内部版本 14376 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1340">For general Windows information on build 14376 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1341">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1341">Fixed</span></span>
- <span data-ttu-id="1ff03-1342">删除了一些存在 apt-get 挂起问题的实例 (GH #493)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1342">Removed some instances where apt-get hangs (GH #493)</span></span>
- <span data-ttu-id="1ff03-1343">修复了不正确处理空装入点的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1343">Fixed an issue where empty mounts were not handled correctly</span></span>
- <span data-ttu-id="1ff03-1344">修复了不正确装载 ramdisk 的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1344">Fixed an issue where ramdisks were not mounted correctly</span></span>
- <span data-ttu-id="1ff03-1345">更改 unix 套接字接受行为以支持标志（在 GH #451 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1345">Change unix socket accept to support flags (partial GH #451)</span></span>
- <span data-ttu-id="1ff03-1346">修复了与网络相关的常见蓝屏问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1346">Fixed common network related bluescreen</span></span>
- <span data-ttu-id="1ff03-1347">修复了访问 /proc/[pid]/task 时出现蓝屏的问题 (GH #523)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1347">Fixed bluescreen when accessing /proc/[pid]/task (GH #523)</span></span>
- <span data-ttu-id="1ff03-1348">修复了在某些 pty 方案中 CPU 利用率偏高的问题（GH #488、#504）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1348">Fixed high CPU utilization for some pty scenarios (GH #488, #504)</span></span>
- <span data-ttu-id="1ff03-1349">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1349">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14371"></a><span data-ttu-id="1ff03-1350">内部版本 14371</span><span class="sxs-lookup"><span data-stu-id="1ff03-1350">Build 14371</span></span>
<span data-ttu-id="1ff03-1351">有关内部版本 14371 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1351">For general Windows information on build 14371 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1352">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1352">Fixed</span></span>
- <span data-ttu-id="1ff03-1353">更正了使用 ptrace 时 SIGCHLD 和 wait() 出现计时争用的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1353">Corrected timing race with SIGCHLD and wait() when using ptrace</span></span>
- <span data-ttu-id="1ff03-1354">更正了当路径包含尾随 / 时出现的某种行为 (GH #432)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1354">Corrected some behavior when paths have a trailing /  (GH #432)</span></span>
- <span data-ttu-id="1ff03-1355">修复了由于打开子级句柄导致重命名/取消链接失败的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1355">Fixed issue with rename/unlink failing due to open handles to children</span></span>
- <span data-ttu-id="1ff03-1356">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1356">Additional bugfixes and improvements</span></span>

<br/>

## <a name="build-14366"></a><span data-ttu-id="1ff03-1357">内部版本 14366</span><span class="sxs-lookup"><span data-stu-id="1ff03-1357">Build 14366</span></span>
<span data-ttu-id="1ff03-1358">有关内部版本 14366 的一般 Windows 信息，请访问 [Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1358">For general Windows information on build 14366 visit the [Windows Blog](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1359">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1359">Fixed</span></span>
- <span data-ttu-id="1ff03-1360">修复通过符号链接创建文件的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1360">Fix in file creation through symlinks</span></span>
-   <span data-ttu-id="1ff03-1361">添加了 Python 的 listxattr (GH 385)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1361">Added listxattr for Python (GH 385)</span></span>
-   <span data-ttu-id="1ff03-1362">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1362">Additional bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1363">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1363">Syscall Support</span></span>
-   <span data-ttu-id="1ff03-1364">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1364">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1365">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1365">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`listxattr`<br/>
<br/>

## <a name="build-14361"></a><span data-ttu-id="1ff03-1366">内部版本 14361</span><span class="sxs-lookup"><span data-stu-id="1ff03-1366">Build 14361</span></span>
<span data-ttu-id="1ff03-1367">有关内部版本 14361 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14361)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1367">For general Windows information on build 14361 visit the [Windows Blog](https://aka.ms/wip14361).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1368">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1368">Fixed</span></span>
- <span data-ttu-id="1ff03-1369">现在，在 Windows 上的 Ubuntu Bash 中运行时，DrvFs 区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1369">DrvFs is now case sensitive when running in Bash on Ubuntu on Windows.</span></span>
  - <span data-ttu-id="1ff03-1370">用户可在其 /mnt/c 驱动器中保存 case.txt 和 CASE.TXT</span><span class="sxs-lookup"><span data-stu-id="1ff03-1370">Users may case.txt and CASE.TXT on their /mnt/c drives</span></span>
  - <span data-ttu-id="1ff03-1371">只有 Windows 上的 Ubuntu Bash 支持区分大小写。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1371">Case sensitivity is only supported within Bash on Ubuntu on Windows.</span></span> <span data-ttu-id="1ff03-1372">在 Bash 外部，NTFS 会正确报告文件，但在与 Windows 中的文件交互时，可能会出现意外的行为。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1372">When outside of Bash NTFS will report the files correctly, but unexpected behavior may occur interacting with the files from Windows.</span></span>
  - <span data-ttu-id="1ff03-1373">每个卷的根目录（即 /mnt/c）不区分大小写</span><span class="sxs-lookup"><span data-stu-id="1ff03-1373">The root of each volume (i.e. /mnt/c) is not case sensitive</span></span>
  - <span data-ttu-id="1ff03-1374">可在[此处](https://support.microsoft.com/en-us/kb/100625)找到有关处理 Windows 中的这些文件的详细信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1374">More information on handling these files in Windows can be found [here](https://support.microsoft.com/en-us/kb/100625).</span></span>
- <span data-ttu-id="1ff03-1375">大幅增强了 pty/tty 支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1375">Greatly enhanced pty / tty support.</span></span>  <span data-ttu-id="1ff03-1376">现在支持 TMUX 等应用程序 (GH #40)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1376">Applications like TMUX now supported (GH #40)</span></span>
- <span data-ttu-id="1ff03-1377">修复了不总会创建用户帐户的安装问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1377">Fixed install issue where user accounts not always created</span></span>
- <span data-ttu-id="1ff03-1378">优化了命令行参数结构，允许极长的参数列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1378">Optimized command line arg structure allowing for extremely long argument list.</span></span> <span data-ttu-id="1ff03-1379">(GH #153)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1379">(GH #153)</span></span>
- <span data-ttu-id="1ff03-1380">现在可对 DrvFs 中的只读文件执行删除和 chmod</span><span class="sxs-lookup"><span data-stu-id="1ff03-1380">Now able to delete and chmod read_only files from DrvFs</span></span>
- <span data-ttu-id="1ff03-1381">修复了一些在断开连接时终端会挂起的实例 (GH #43)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1381">Fixed some instances where the terminal hangs on disconnect (GH #43)</span></span>
- <span data-ttu-id="1ff03-1382">现在可在 tty 设备上正常运行 chmod 和 chown</span><span class="sxs-lookup"><span data-stu-id="1ff03-1382">chmod and chown now work on tty devices</span></span>
- <span data-ttu-id="1ff03-1383">允许连接到作为 localhost 的 0.0.0.0 和 :: (GH #388)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1383">Allow connection to 0.0.0.0 and :: as localhost (GH #388)</span></span>
- <span data-ttu-id="1ff03-1384">Sendmsg/recvmsg 现在可处理大于 1 的 IO 矢量长度（在 GH #376 中做了部分描述）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1384">Sendmsg/recvmsg now handle an IO vector length of >1 (partial GH #376)</span></span>
- <span data-ttu-id="1ff03-1385">用户现在可以选择禁用自动生成的 hosts 文件 (GH #398)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1385">Users can now opt-out of auto-generated hosts file (GH #398)</span></span>
- <span data-ttu-id="1ff03-1386">在安装期间自动将 Linux 区域设置与 NT 区域设置进行匹配 (GH #11)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1386">Automatically match Linux locale to the NT locale during install (GH #11)</span></span>
- <span data-ttu-id="1ff03-1387">添加了 /proc/sys/vm/swappiness 文件 (GH #306)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1387">Added the /proc/sys/vm/swappiness file (GH #306)</span></span>
- <span data-ttu-id="1ff03-1388">strace 现在会正常退出</span><span class="sxs-lookup"><span data-stu-id="1ff03-1388">strace now exits correctly</span></span>
- <span data-ttu-id="1ff03-1389">允许通过 /proc/self/fd 重新打开管道 (GH #222)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1389">Allow pipes to be reopened through /proc/self/fd (GH #222)</span></span>
- <span data-ttu-id="1ff03-1390">在 DrvFs 中隐藏 %LOCALAPPDATA%\lxss 下的目录 (GH #270)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1390">Hide directories under %LOCALAPPDATA%\lxss from DrvFs (GH #270)</span></span>
- <span data-ttu-id="1ff03-1391">更好地处理 bash.exe ~。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1391">Better handling of bash.exe ~.</span></span>  <span data-ttu-id="1ff03-1392">现在支持类似于“bash ~ -c ls”的命令 (GH #467)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1392">Commands like “bash ~ -c ls” now supported (GH #467)</span></span>
- <span data-ttu-id="1ff03-1393">现在，在关闭期间，套接字会通知 epoll read 可用 (GH #271)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1393">Sockets now notify epoll read available during shutdown (GH #271)</span></span>
- <span data-ttu-id="1ff03-1394">lxrun /uninstall 可以更好地删除文件和文件夹</span><span class="sxs-lookup"><span data-stu-id="1ff03-1394">lxrun /uninstall does a better job of deleting the files and folders</span></span>
- <span data-ttu-id="1ff03-1395">更正了 ps -f (GH #246)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1395">Corrected ps -f (GH #246)</span></span>
- <span data-ttu-id="1ff03-1396">改善了对 xEmacs 等 x11 应用的支持 (GH #481)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1396">Improved support for x11 apps such as xEmacs (GH #481)</span></span>
- <span data-ttu-id="1ff03-1397">更新了初始线程堆栈大小，以匹配默认的 Ubuntu 设置，并正确地向 get_rlimit syscall 报告大小（GH #172、#258）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1397">Updated initial thread stack size to match default Ubuntu setting and reporting the size correctly to the get_rlimit syscall (GH #172, #258)</span></span>
- <span data-ttu-id="1ff03-1398">改善了 pico 进程映像名称的报告（例如，用于审核）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1398">Improved reporting of pico process image names (e.g., for auditing)</span></span>
- <span data-ttu-id="1ff03-1399">实现了 df 命令的 /proc/mountinfo</span><span class="sxs-lookup"><span data-stu-id="1ff03-1399">Implemented /proc/mountinfo for df command</span></span>
- <span data-ttu-id="1ff03-1400">修复了子名称 .</span><span class="sxs-lookup"><span data-stu-id="1ff03-1400">Fixed symlink error code for child name .</span></span> <span data-ttu-id="1ff03-1401">和 .. 的符号链接错误代码</span><span class="sxs-lookup"><span data-stu-id="1ff03-1401">and ..</span></span>
- <span data-ttu-id="1ff03-1402">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1402">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1403">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1403">Syscall Support</span></span>
<span data-ttu-id="1ff03-1404">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1404">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1405">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1405">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a><span data-ttu-id="1ff03-1406">内部版本 14352</span><span class="sxs-lookup"><span data-stu-id="1ff03-1406">Build 14352</span></span>
<span data-ttu-id="1ff03-1407">有关内部版本 14352 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14352)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1407">For general Windows information on build 14352 visit the [Windows Blog](https://aka.ms/wip14352).</span></span><br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1408">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1408">Fixed</span></span>
- <span data-ttu-id="1ff03-1409">修复了不正常下载/创建大型文件的问题。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1409">Fixed issue where large files were not downloaded / created correctly.</span></span>  <span data-ttu-id="1ff03-1410">这应该可以解除 npm 和其他方案的阻碍（GH #3、GH #313）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1410">This should unblock npm and other scenarios (GH #3, GH #313)</span></span>
- <span data-ttu-id="1ff03-1411">删除了一些存在套接字挂起情况的实例</span><span class="sxs-lookup"><span data-stu-id="1ff03-1411">Removed some instances where sockets hang</span></span>
- <span data-ttu-id="1ff03-1412">更正了一些 ptrace 错误</span><span class="sxs-lookup"><span data-stu-id="1ff03-1412">Corrected some ptrace errors</span></span>
- <span data-ttu-id="1ff03-1413">修复了 WSL 中的问题，允许超过 255 个字符的文件名</span><span class="sxs-lookup"><span data-stu-id="1ff03-1413">Fixed issue with WSL allowing filenames longer than 255 characters</span></span>
- <span data-ttu-id="1ff03-1414">改善了对非英语字符的支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1414">Improved support for non-English characters</span></span>
- <span data-ttu-id="1ff03-1415">添加当前 Windows 时区数据并将其设为默认值</span><span class="sxs-lookup"><span data-stu-id="1ff03-1415">Add current Windows timezone data and set as default</span></span>
- <span data-ttu-id="1ff03-1416">每个装入点的唯一设备 ID （JRE 修复 – GH #49）</span><span class="sxs-lookup"><span data-stu-id="1ff03-1416">Unique device id’s for each mount point (jre fix – GH #49)</span></span>
- <span data-ttu-id="1ff03-1417">更正路径中包含“.”</span><span class="sxs-lookup"><span data-stu-id="1ff03-1417">Correct issue with paths containing “.”</span></span> <span data-ttu-id="1ff03-1418">和“..”的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1418">and “..”</span></span>
- <span data-ttu-id="1ff03-1419">添加了 Fifo 支持 (GH #71)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1419">Added Fifo support (GH #71)</span></span>
- <span data-ttu-id="1ff03-1420">更新了 resolv.conf 的格式，以匹配本机 Ubuntu 格式</span><span class="sxs-lookup"><span data-stu-id="1ff03-1420">Updated format of resolv.conf to match native Ubuntu format</span></span>
- <span data-ttu-id="1ff03-1421">一些 procfs 清理</span><span class="sxs-lookup"><span data-stu-id="1ff03-1421">Some procfs cleanup</span></span>
- <span data-ttu-id="1ff03-1422">为管理员控制台启用了 ping (GH #18)</span><span class="sxs-lookup"><span data-stu-id="1ff03-1422">Enabled ping for Administrator consoles (GH #18)</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1423">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1423">Syscall Support</span></span>
<span data-ttu-id="1ff03-1424">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1424">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1425">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1425">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a><span data-ttu-id="1ff03-1426">内部版本 14342</span><span class="sxs-lookup"><span data-stu-id="1ff03-1426">Build 14342</span></span>
<span data-ttu-id="1ff03-1427">有关内部版本 14342 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14342)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1427">For general Windows information on build 14342 the [Windows Blog](https://aka.ms/wip14342).</span></span> <br/>

<span data-ttu-id="1ff03-1428">在 [WSL 博客](https://blogs.msdn.microsoft.com/wsl)中可以找到有关 VolFs 和 DriveFs 的信息。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1428">Information on VolFs and DriveFs can be found on the [WSL Blog](https://blogs.msdn.microsoft.com/wsl).</span></span> <br/>

### <a name="fixed"></a><span data-ttu-id="1ff03-1429">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1429">Fixed</span></span>
- <span data-ttu-id="1ff03-1430">修复了 Windows 用户在用户名中包含 Unicode 字符时出现的安装问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1430">Fixed install issue when the Windows user had Unicode characters in the username</span></span>
- <span data-ttu-id="1ff03-1431">现在，在首次运行时，默认会提供“常见问题解答”中的 apt-get update udev 解决方法</span><span class="sxs-lookup"><span data-stu-id="1ff03-1431">The apt-get update udev workaround in the FAQ is now provided by default on first run</span></span>
- <span data-ttu-id="1ff03-1432">在 DriveFs (/mnt/<drive>) 目录中启用了符号链接</span><span class="sxs-lookup"><span data-stu-id="1ff03-1432">Enabled symlinks in DriveFs (/mnt/<drive>) directories</span></span>
- <span data-ttu-id="1ff03-1433">现在可以在 DriveFs 和 VolFs 之间使用符号链接</span><span class="sxs-lookup"><span data-stu-id="1ff03-1433">Symlinks now work between DriveFs and VolFs</span></span>
- <span data-ttu-id="1ff03-1434">解决了顶级路径分析问题：ls .// 现在可按预期方式工作</span><span class="sxs-lookup"><span data-stu-id="1ff03-1434">Addressed top level path parsing issue: ls .// will now work as expected</span></span>
- <span data-ttu-id="1ff03-1435">DriveFs 上的 npm install 和 -g 选项现在可正常工作</span><span class="sxs-lookup"><span data-stu-id="1ff03-1435">npm install on DriveFs and the -g options are now working</span></span>
- <span data-ttu-id="1ff03-1436">修复了阻止 PHP 服务器启动的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1436">Fixed issue preventing PHP server from launching</span></span>
- <span data-ttu-id="1ff03-1437">更新了默认环境值（例如 $PATH），以便与本机 Ubuntu 更匹配</span><span class="sxs-lookup"><span data-stu-id="1ff03-1437">Updated default environment values, such as $PATH to closer match native Ubuntu</span></span>
- <span data-ttu-id="1ff03-1438">在 Windows 中添加了每周维护任务以更新 apt 包缓存</span><span class="sxs-lookup"><span data-stu-id="1ff03-1438">Added a weekly maintenance task in Windows to update the apt package cache</span></span>
- <span data-ttu-id="1ff03-1439">修复了 ELF 标头验证的问题，WSL 现在支持所有 Melkor 选项</span><span class="sxs-lookup"><span data-stu-id="1ff03-1439">Fixed issue with ELF header validation, WSL now supports all Melkor options</span></span>
- <span data-ttu-id="1ff03-1440">Zsh shell 可正常运行</span><span class="sxs-lookup"><span data-stu-id="1ff03-1440">Zsh shell is functional</span></span>
- <span data-ttu-id="1ff03-1441">现在支持预编译的 Go 二进制文件</span><span class="sxs-lookup"><span data-stu-id="1ff03-1441">Precompiled Go binaries are now supported</span></span>
- <span data-ttu-id="1ff03-1442">现已正确本地化首次运行 Bash 时出现的提示</span><span class="sxs-lookup"><span data-stu-id="1ff03-1442">Prompting on Bash.exe first run is now localized correctly</span></span>
- <span data-ttu-id="1ff03-1443">/proc/meminfo 现在会返回正确的信息</span><span class="sxs-lookup"><span data-stu-id="1ff03-1443">/proc/meminfo now returns correct information</span></span>
- <span data-ttu-id="1ff03-1444">VFS 现在支持套接字</span><span class="sxs-lookup"><span data-stu-id="1ff03-1444">Sockets now supported in VFS</span></span>
- <span data-ttu-id="1ff03-1445">/dev 现在装载为 tempfs</span><span class="sxs-lookup"><span data-stu-id="1ff03-1445">/dev now mounted as tempfs</span></span>
- <span data-ttu-id="1ff03-1446">现在支持 Fifo</span><span class="sxs-lookup"><span data-stu-id="1ff03-1446">Fifo now supported</span></span>
- <span data-ttu-id="1ff03-1447">多核系统现在会在 /proc/cpuinfo 中正确显示</span><span class="sxs-lookup"><span data-stu-id="1ff03-1447">Multi-core systems now showing correctly in /proc/cpuinfo</span></span>
- <span data-ttu-id="1ff03-1448">其他改进以及首次运行期间下载内容时显示的错误消息</span><span class="sxs-lookup"><span data-stu-id="1ff03-1448">Additional improvements and error messages downloading during first run</span></span>
- <span data-ttu-id="1ff03-1449">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1449">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="1ff03-1450">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1450">Supported syscall list below.</span></span>
- <span data-ttu-id="1ff03-1451">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1451">Additional bugfixes and improvements</span></span>

### <a name="known-issues"></a><span data-ttu-id="1ff03-1452">已知问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1452">Known Issues</span></span>
- <span data-ttu-id="1ff03-1453">在某些情况下，</span><span class="sxs-lookup"><span data-stu-id="1ff03-1453">Not resolving ‘..’</span></span> <span data-ttu-id="1ff03-1454">不会正确解析 DriveFs 上的“..”</span><span class="sxs-lookup"><span data-stu-id="1ff03-1454">correctly on DriveFs in some cases</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1455">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1455">Syscall Support</span></span>
<span data-ttu-id="1ff03-1456">下面是在 WSL 中具有某种实现的新的或增强的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1456">Below are a list of new or enhanced syscalls that have some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1457">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1457">The syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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

## <a name="build-14332"></a><span data-ttu-id="1ff03-1458">内部版本 14332</span><span class="sxs-lookup"><span data-stu-id="1ff03-1458">Build 14332</span></span>

<span data-ttu-id="1ff03-1459">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14332)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1459">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14332).</span></span> <br/>


### <a name="fixed"></a><span data-ttu-id="1ff03-1460">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1460">Fixed</span></span>
- <span data-ttu-id="1ff03-1461">更好地生成 resolv.conf，包括指定 DNS 项的优先级</span><span class="sxs-lookup"><span data-stu-id="1ff03-1461">Better resolv.conf generation including prioritizing DNS entries</span></span>
- <span data-ttu-id="1ff03-1462">在 /mnt 与非 /mnt 驱动器之间移动文件和目录时出现的问题</span><span class="sxs-lookup"><span data-stu-id="1ff03-1462">Issue with moving files and directories between /mnt and non-/mnt drives</span></span>
- <span data-ttu-id="1ff03-1463">现在可以使用符号链接创建 Tar 文件。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1463">Tar files can now be created with symlinks</span></span>
- <span data-ttu-id="1ff03-1464">创建实例时会添加默认的 /run/lock 目录</span><span class="sxs-lookup"><span data-stu-id="1ff03-1464">Added default /run/lock directory on instance creation</span></span>
- <span data-ttu-id="1ff03-1465">更新 /dev/null 以返回正确的统计信息</span><span class="sxs-lookup"><span data-stu-id="1ff03-1465">Update /dev/null to return proper stat info</span></span>
- <span data-ttu-id="1ff03-1466">首次运行期间下载内容时出现的其他错误</span><span class="sxs-lookup"><span data-stu-id="1ff03-1466">Additional errors when downloading during first run</span></span>
- <span data-ttu-id="1ff03-1467">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1467">Syscall improvements and bugfixes.</span></span> <span data-ttu-id="1ff03-1468">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1468">Supported syscall list below.</span></span>
- <span data-ttu-id="1ff03-1469">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1469">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1470">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1470">Syscall Support</span></span>
<span data-ttu-id="1ff03-1471">下面是在 WSL 中具有某种实现的新 syscall。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1471">Below is the new syscall that has some implementation in WSL.</span></span> <span data-ttu-id="1ff03-1472">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1472">The syscall on this list is supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a><span data-ttu-id="1ff03-1473">内部版本 14328</span><span class="sxs-lookup"><span data-stu-id="1ff03-1473">Build 14328</span></span>

<span data-ttu-id="1ff03-1474">有关内部版本 14332 的一般 Windows 信息，请访问 [Windows 博客](https://aka.ms/wip14328)。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1474">For general Windows information on build 14332 visit the [Windows Blog](https://aka.ms/wip14328).</span></span> <br/>


### <a name="new-features"></a><span data-ttu-id="1ff03-1475">新功能</span><span class="sxs-lookup"><span data-stu-id="1ff03-1475">New Features</span></span>
* <span data-ttu-id="1ff03-1476">现在支持 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1476">Now support Linux users.</span></span>  <span data-ttu-id="1ff03-1477">安装 Windows 上的 Ubuntu Bash 时会提示创建 Linux 用户。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1477">Installing Bash on Ubuntu on Windows will prompt for creation of a Linux user.</span></span>  <span data-ttu-id="1ff03-1478">有关详细信息，请访问 https://aka.ms/wslusers</span><span class="sxs-lookup"><span data-stu-id="1ff03-1478">For more information, visit https://aka.ms/wslusers</span></span>
* <span data-ttu-id="1ff03-1479">现在，主机名将设置为 Windows 计算机名，而不再是 @localhost</span><span class="sxs-lookup"><span data-stu-id="1ff03-1479">Hostname is now set to the Windows computer name, no more @localhost</span></span>
* <span data-ttu-id="1ff03-1480">有关内部版本 14328 的详细信息，请访问： https://aka.ms/wip14328</span><span class="sxs-lookup"><span data-stu-id="1ff03-1480">For more information on build 14328, visit: https://aka.ms/wip14328</span></span>

### <a name="fixed"></a><span data-ttu-id="1ff03-1481">固定</span><span class="sxs-lookup"><span data-stu-id="1ff03-1481">Fixed</span></span>
* <span data-ttu-id="1ff03-1482">非 /mnt/<drive> 文件的符号链接改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1482">Symlink improvements for non /mnt/<drive> files</span></span>
    * <span data-ttu-id="1ff03-1483">现在可正常运行 npm install</span><span class="sxs-lookup"><span data-stu-id="1ff03-1483">npm install now works</span></span>
    * <span data-ttu-id="1ff03-1484">现在可以根据[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)的说明安装 jdk/jre。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1484">jdk / jre now installable using instructions found [here](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html).</span></span>
    * <span data-ttu-id="1ff03-1485">已知问题：符号链接不适用于 Windows 装载。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1485">known issue: symlinks do not work for Windows mounts.</span></span>  <span data-ttu-id="1ff03-1486">此功能将在以后的内部版本中可用</span><span class="sxs-lookup"><span data-stu-id="1ff03-1486">Functionality will be available in a later build</span></span>
* <span data-ttu-id="1ff03-1487">现在会显示 top 和 htop</span><span class="sxs-lookup"><span data-stu-id="1ff03-1487">top and htop now display</span></span>
* <span data-ttu-id="1ff03-1488">有关某些安装失败的其他错误消息</span><span class="sxs-lookup"><span data-stu-id="1ff03-1488">Additional error messages for some install failures</span></span>
* <span data-ttu-id="1ff03-1489">Syscall 改进和 bug 修复。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1489">Syscall improvements and bugfixes.</span></span>  <span data-ttu-id="1ff03-1490">下面列出了支持的 syscall。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1490">Supported syscall list below.</span></span>
* <span data-ttu-id="1ff03-1491">其他 bug 修复和改进</span><span class="sxs-lookup"><span data-stu-id="1ff03-1491">Additional improvements bugfixes and improvements</span></span>

### <a name="syscall-support"></a><span data-ttu-id="1ff03-1492">Syscall 支持</span><span class="sxs-lookup"><span data-stu-id="1ff03-1492">Syscall Support</span></span>
<span data-ttu-id="1ff03-1493">下面是在 WSL 中具有某种实现的 syscall 列表。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1493">Below is a list of syscalls that have some implementation in WSL.</span></span>  <span data-ttu-id="1ff03-1494">此列表中的 syscall 至少在一种方案中受支持，但目前其所有参数不一定都受支持。</span><span class="sxs-lookup"><span data-stu-id="1ff03-1494">Syscalls on this list are supported in at least one scenario, but may not have all parameters supported at this time.</span></span>

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
