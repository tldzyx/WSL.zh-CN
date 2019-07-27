---
title: 适用于 Linux 的 Windows 子系统的发行说明
description: 适用于 Linux 的 Windows 子系统的发行说明。  每周更新。
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu
author: benhillis
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 36ea641e-4d49-4881-84eb-a9ca85b1cdf4
ms.custom: seodec18
ms.openlocfilehash: c262ddb359507c1654f0089050bfd15ec16402f9
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/26/2019
ms.locfileid: "68523786"
---
# <a name="release-notes-for-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的发行说明


## <a name="build-18945"></a>生成18945
有关生成18945的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)。

### <a name="wsl"></a>WSL
* [WSL2]允许使用 localhost: port 通过主机访问 WSL2 中的侦听 tcp 套接字
* [WSL2]修复了安装/转换失败和其他诊断以跟踪未来的问题 [GH 4105] 
* [WSL2]提高 WSL2 网络问题的诊断
* [WSL2]将内核版本更新为4.19.55
* [WSL2]更新 docker 所需的配置选项的内核 [GH 4165]
* [WSL2]增加分配给轻型实用程序 VM 的 Cpu 数量, 使其与主机相同 (以前的内核配置中的 CONFIG_NR_CPUS 上限为 8) [GH 4137]
* [WSL2]为 WSL2 轻型 VM 创建交换文件
* [WSL2]允许通过\\ \\wsl$\\发行版 (例如 sshfs) 查看用户装载 [GH 4172]
* [WSL2]提高9p 文件系统性能
* [WSL2]确保 vhd ACL 不会增长无限 [GH 4126]
* [WSL2]更新内核配置以支持 squashfs 和 xt_conntrack [GH 4107, 4123]
* [WSL2]修复了互操作。 enabled/etc/wsl.conf 选项 [GH 4140]
* [WSL2]如果文件系统不支持 EAs, 则返回 ENOTSUP
* [WSL2]Fix CopyFile 挂起 with \\ \\wsl $
* 将默认 umask 切换到 0022, 并将 umask 设置设置为/etc/wsl.conf
* 修复 wslpath 以正确解析符号链接, 这是19h1 中的回归 [GH 4078]
* 引入% UserProfile%\.wslconfig 文件以调整 WSL2 设置
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

## <a name="build-18917"></a>生成18917
有关生成18917的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/06/12/announcing-windows-10-insider-preview-build-18917/)。

### <a name="wsl"></a>WSL
* WSL 2 现已可用! 有关更多详细信息, 请参阅[博客](https://devblogs.microsoft.com/commandline/wsl-2-is-now-available-in-windows-insiders/)。
* 解决通过符号链接启动 Windows 进程时无法正常工作的回归 [GH 3999]
* 将 wsl--list--verbose、wsl--list--quiet 和 wsl--import--import-
* 添加 wsl--shutdown 选项
* 计划 9:允许打开目录进行写入成功

## <a name="build-18890"></a>生成18890
有关生成18890的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。

### <a name="wsl"></a>WSL
* 非阻塞套接字泄露 [GH 2913]
* 到 terminal 的 EOF 输入会阻止后续读取 [GH 3421]
* 更新 resolv.conf 标头以引用 wsl [在 GH 3928 中讨论]
* Epoll 删除代码中的死锁 [GH 3922]
* 处理中的空格--import 和– export [GH 3932]
* 扩展 mmap 的文件无法正常工作 [GH 3939]
* 解决 ARM64 \\wsl $ access 无法正常工作的问题
* 为 wsl 添加更好的默认图标

## <a name="build-18342"></a>生成18342
有关生成18342的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。

### <a name="wsl"></a>WSL
* 我们添加了一项功能, 使用户能够从 Windows 访问 WSL 发行版中的 Linux 文件。 可以通过命令行访问这些文件, 并且 Windows 应用 (如文件资源管理器、VSCode 等) 可与这些文件进行交互。 通过\\\\ \\导航到\\wsl $ < distro_name > 访问文件, 或通过导航到 wsl $ 查看正在运行的分发的列表\\
* 添加额外的 CPU 信息标记并修复 Cpus_allowed [_list] 值 [GH 2234]
* 支持非前导线程中的 exec [GH 3800]
* 将配置更新失败视为非致命的 [GH 3785]
* 更新 binfmt 以正确处理偏移量 [GH 3768]
* 为计划9启用映射网络驱动器 [GH 3854]
* 支持 Windows > Linux 和 Linux-> 用于绑定装载的 Windows 路径转换
* 为以只读打开的文件中的映射创建只读部分

## <a name="build-18334"></a>生成18334
有关生成18334的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。

### <a name="wsl"></a>WSL
* 重新设计 Windows 时区映射到 Linux 时区的方式 [GH 3747]
* 修复内存泄漏并添加新的字符串转换函数 [GH 3746]
* 不带线程的 threadgroup 上的 SIGCONT 是一种无操作 [GH 3741] 
* 正确显示/proc/self/fd 中的套接字和 epoll 文件描述符

## <a name="build-18305"></a>生成18305
有关生成18305的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。

### <a name="wsl"></a>WSL
* 主线程退出时, pthreads 将失去对文件的访问权限 [GH 3589]
* 除非需要, 否则 TIOCSCTTY 应忽略 "force" 参数 [GH 3652]
* wsl 命令行改进并添加了导入/导出功能。
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

## <a name="build-18277"></a>生成18277
有关生成18277的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。

### <a name="wsl"></a>WSL
* 修复了生成 18272 [GH 3645] 中引入的 "不支持此类接口" 错误
* 忽略卸载 syscall [GH 3605] 的 MNT_FORCE 标志
* 切换 WSL 互操作以使用官方 CreatePseudoConsole API
* FUTEX_WAIT 重新启动时保持无超时值

## <a name="build-18272"></a>生成18272
有关生成18272的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。

### <a name="wsl"></a>WSL
* **警告：** 在此版本中, 导致 WSL 不可操作的问题。 尝试启动分发时, 将看到 "不支持此类接口" 错误。 此问题已修复, 将在下一周的预览体验期内提供。 如果已安装此版本, 则可以使用 "设置-> 更新 & 安全 > 恢复", 在 "设置-更新" 中回滚到以前的 Windows 版本。

## <a name="build-18267"></a>生成18267
有关生成18267的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。

### <a name="wsl"></a>WSL
* 修复了傀儡过程不会 reaped 并始终处于无限期的问题。
* 如果错误消息超过最大长度, 则 WslRegisterDistribution 挂起 [GH 3592]
* 允许 fsync 对 DrvFs 上的只读文件成功 [GH 3556]
* 在 [GH 3584] 中创建符号链接之前, 请确保/bin 和/sbin 目录存在
* 添加了 WSL 实例的实例终止超时机制。 超时值当前设置为15秒, 这意味着实例将在上一个 WSL 进程退出15秒后终止。 若要立即终止分发, 请使用:
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>版本 17763 (1809)
有关生成17763的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 权限检查太严格, 无法更改相同的线程优先级 [GH 1838]
* 确保使用无偏差中断时间进行启动时间, 以避免返回 clock_gettime (CLOCK_BOOTTIME) 的负值 [GH 3434]
* 在 WSL binfmt 解释器中处理符号链接 [GH 3424]
* 更好地处理 threadgroup 前导文件描述符清理。
* 切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter 来避免溢出 [GH 3252]
* Ptrace attach 可能会导致来自系统调用的错误返回值 [GH 1731]
* 解决几个 AF_UNIX 相关问题 [GH 3371]
* 修复了以下问题: 如果当前工作目录长度少于5个字符, 则可能导致 WSL 互操作失败 [GH 3379]
* 避免与不存在的端口发生环回连接时出现一秒钟延迟失败 [GH 3286]
* 添加/proc/sys/fs/file-max 存根文件 [GH 2893]
* 更准确的 IPV6 作用域信息。
* PR_SET_PTRACER 支持 [GH 3053]
* 管道文件系统意外清除边缘触发的 epoll 事件 [GH 3276]
* 通过 NTFS 符号启动的 Win32 可执行文件不遵守符号名称 [GH 2909]
* 改善了傀儡支持 [GH 1353]
* 添加 wsl 项以控制 Windows 互操作行为 [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修复 getsockname not always 返回 UNIX 套接字系列类型 [GH 1774]
* 添加对 TIOCSTI 的支持 [GH 1863]
* 连接过程中的非阻止套接字应为写入尝试返回 EAGAIN [GH 2846]
* 支持已装入 Vhd 上的互操作 [GH 3246, 3291]
* 修复根文件夹的权限检查问题 [GH 3304]
* 对 TTY 键盘 ioctls KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。
* 即使在后台启动, 也应执行 Windows UI 应用。
* 添加 wsl 或--user 选项 [GH 1203]
* 启用快速启动时修复 WSL 启动问题 [GH 2576]
* Unix 套接字需要保留断开连接的对等凭据 [GH 3183]
* 非阻止 Unix 套接字通过 EAGAIN 无限期失败 [GH 3191]
* case = off 是新的默认 drvfs 装载类型 [GH 2937, 3212, 3328]
    * 有关详细信息, 请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。
* 添加 wslconfig/terminate 以停止正在运行的分发。
* 解决了无法正确处理带有空格的路径的 WSL shell 上下文菜单项的问题。
* 公开作为扩展属性的每目录大小写敏感度
* ARM64：模拟缓存维护操作。 解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。
* DrvFs: 只有专用范围中对应于转义字符的 unescape 字符。
* 修复 ELF 分析器解释器长度验证 [GH 3154] 中的一个错误
* WSL 包含过去时间的绝对计时器 [GH 3091]
* 确保新创建的重新分析点在父目录中列出为这样。
* 以原子方式创建 DrvFs 中的区分大小写的目录。
* 修复了一个额外的问题, 即即使文件存在, 多线程操作也可能返回 ENOENT。 [GH 2712]
* 修复了 UMCI 启用时的 WSL 启动失败。 [GH 3020]
* 添加浏览器上下文菜单以启动 WSL [GH 437, 603, 1836]。 若要使用, 请在浏览器窗口中按住 shift 键并右键单击。
* 修复 Unix 套接字非阻止行为 [GH 2822, 3100]
* 修复 GH 2026 中报告的挂起 NETLINK 命令。
* 添加对装载传播标志的支持 [GH 2911]。
* 修复了截断不会导致 inotify 事件 [GH 2978] 的问题。
* 添加--exec 选项, 用于 wsl, 以便在不使用 shell 的情况下调用单个二进制文件。
* 添加--wsl 的分发选项, 以选择特定的发行版。
* 对 dmesg 的有限支持。 现在, 应用程序可以登录到 dmesg。 WSL 驱动程序将有限的信息记录到 dmesg。 将来, 可以通过扩展此功能从驱动程序携带其他信息/诊断。
    * 注意: 当前支持通过`/dev/kmsg`设备接口进行 dmesg。 `syslog`目前尚不支持 syscall 接口。 而且, 某些`dmesg`命令行选项`-S`(如) `-C`不起作用。
* 更改串行设备的默认 gid 和模式以匹配本机 [GH 3042]
* DrvFs 现在支持扩展属性。
    * 注意:DrvFs 对扩展属性的名称有一些限制。 不允许使用某些字符 (如 "/"、":\*" 和 ""), 并且扩展属性名称在 DrvFs 上不区分大小写

## <a name="build-18252-skip-ahead"></a>生成 18252 (向前跳过)
有关生成18252的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。

### <a name="wsl"></a>WSL
* 将 init 和 bsdtar 二进制文件从 lxssmanager dll 移到单独的工具文件夹中
* 解决使用 CLONE_FILES 时关闭文件描述符的争用
* 转换 DrvFs 路径时处理/proc/pid/mountinfo 中的可选字段
* 允许 DrvFs mknod 成功而不支持 S_IFREG 的元数据
* 在 DrvFs 上创建的 readonly 文件应具有 readonly 属性集 [GH 3411]
* 添加/sbin/mount.drvfs helper 以处理 DrvFs 挂载
* 在 DrvFs 中使用 POSIX rename。
* 允许无卷 GUID 的卷上的路径转换。

## <a name="build-17738-fast"></a>生成 17738 (快速)
有关生成17738的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 权限检查太严格, 无法更改相同的线程优先级 [GH 1838]
* 确保使用无偏差中断时间进行启动时间, 以避免返回 clock_gettime (CLOCK_BOOTTIME) 的负值 [GH 3434]
* 在 WSL binfmt 解释器中处理符号链接 [GH 3424]
* 更好地处理 threadgroup 前导文件描述符清理。

## <a name="build-17728-fast"></a>生成 17728 (快速)
有关生成17728的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。

### <a name="wsl"></a>WSL
* 切换 WSL 以使用 KeQueryInterruptTimePrecise 而不是 KeQueryPerformanceCounter 来避免溢出 [GH 3252]
* Ptrace attach 可能会导致来自系统调用的错误返回值 [GH 1731]
* 解决与 AF_UNIX 相关的问题 [GH 3371]
* 修复了以下问题: 如果当前工作目录长度少于5个字符, 则可能导致 WSL 互操作失败 [GH 3379]

## <a name="build-18204-skip-ahead"></a>生成 18204 (向前跳过)
有关生成18204的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 管道文件系统 inadvertenly 清除边缘-触发的 epoll 事件 [GH 3276]
* 通过 NTFS 符号启动的 Win32 可执行文件不遵守符号名称 [GH 2909]

## <a name="build-17723-fast"></a>生成 17723 (快速)
有关生成17723的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 避免与不存在的端口发生环回连接时出现一秒钟延迟失败 [GH 3286]
* 添加/proc/sys/fs/file-max 存根文件 [GH 2893]
* 更准确的 IPV6 作用域信息。
* PR_SET_PTRACER 支持 [GH 3053]
* 管道文件系统 inadvertenly 清除边缘-触发的 epoll 事件 [GH 3276]
* 通过 NTFS 符号启动的 Win32 可执行文件不遵守符号名称 [GH 2909]

## <a name="build-17713"></a>生成17713
有关生成17713的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。

### <a name="wsl"></a>WSL
* 改善了傀儡支持 [GH 1353]
* 添加 wsl 项以控制 Windows 互操作行为 [GH 1493]
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修复 getsockname not always 返回 UNIX 套接字系列类型 [GH 1774]
* 添加对 TIOCSTI 的支持 [GH 1863]
* 连接过程中的非阻止套接字应为写入尝试返回 EAGAIN [GH 2846]
* 支持已装入 Vhd 上的互操作 [GH 3246, 3291]
* 修复根文件夹的权限检查问题 [GH 3304]
* 对 TTY 键盘 ioctls KDGKBTYPE、KDGKBMODE 和 KDSKBMODE 的有限支持。
* 即使在后台启动, 也应执行 Windows UI 应用。

## <a name="build-17704"></a>生成17704
有关生成17704的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。

### <a name="wsl"></a>WSL
* 添加 wsl 或--user 选项 [GH 1203]
* 启用快速启动时修复 WSL 启动问题 [GH 2576]
* Unix 套接字需要保留断开连接的对等凭据 [GH 3183]
* 非阻止 Unix 套接字通过 EAGAIN 无限期失败 [GH 3191]
* case = off 是新的默认 drvfs 装载类型 [GH 2937, 3212, 3328]
    * 有关详细信息, 请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)。
* 添加 wslconfig/terminate 以停止正在运行的分发。

## <a name="build-17692"></a>版本 17692
有关生成17692的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。

### <a name="wsl"></a>WSL
* 解决了无法正确处理带有空格的路径的 WSL shell 上下文菜单项的问题。
* 公开作为扩展属性的每目录大小写敏感度
* ARM64：模拟缓存维护操作。 解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。
* DrvFs: 只有专用范围中对应于转义字符的 unescape 字符。

## <a name="build-17686"></a>版本 17686
有关生成17686的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。

### <a name="wsl"></a>WSL
* 修复 ELF 分析器解释器长度验证 [GH 3154] 中的一个错误
* WSL 包含过去时间的绝对计时器 [GH 3091]
* 确保新创建的重新分析点在父目录中列出为这样。
* 以原子方式创建 DrvFs 中的区分大小写的目录。

## <a name="build-17677"></a>生成17677
有关生成17677的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。

### <a name="wsl"></a>WSL
* 修复了一个额外的问题, 即即使文件存在, 多线程操作也可能返回 ENOENT。 [GH 2712]
* 修复了 UMCI 启用时的 WSL 启动失败。 [GH 3020]

## <a name="build-17666"></a>生成17666
有关生成17666的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>警告：某些 AMD 芯片组上出现阻止 WSL 运行的问题 [GH 3134]。 修补程序已准备就绪, 并将其转移到有问必答生成分支。
* 添加浏览器上下文菜单以启动 WSL [GH 437, 603, 1836]。 在资源管理器窗口中使用按住 shift 键并右键单击。
* 修复 unix 套接字非阻止行为 [GH 2822, 3100]
* 修复 GH 2026 中报告的挂起 NETLINK 命令。
* 添加对装载传播标志的支持 [GH 2911]。
* 修复了截断不会导致 inotify 事件 [GH 2978] 的问题。
* 添加--exec 选项, 用于 wsl, 以便在不使用 shell 的情况下调用单个二进制文件。
* 添加--wsl 的分发选项, 以选择特定的发行版。

## <a name="build-17655-skip-ahead"></a>生成 17655 (向前跳过)
有关生成17655的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 对 dmesg 的有限支持。 现在, 应用程序可以登录到 dmesg。 WSL 驱动程序将有限的信息记录到 dmesg。 将来, 可以通过扩展此功能从驱动程序携带其他信息/诊断。
    * 注意: 当前支持通过`/dev/kmsg`设备接口进行 dmesg。 `syslog`尚不支持 sycall 接口。 而且, 某些`dmesg`命令行选项`-S`(如) `-C`不起作用。
* 修复了即使文件存在, 多线程操作可以返回 ENOENT 的问题。 [GH 2712]

## <a name="build-17639-skip-ahead"></a>生成 17639 (向前跳过)
有关生成17639的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 更改串行设备的默认 gid 和模式以匹配本机 [GH 3042]
* DrvFs 现在支持扩展属性。
    * 注意:DrvFs 对扩展属性的名称有一些限制。 特别是, 不允许使用某些字符 (如 "/"、":\*" 和 ""), 并且扩展属性名称在 DrvFs 上不区分大小写

## <a name="build-17133-fast"></a>生成 17133 (快速)
有关生成17133的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。

### <a name="wsl"></a>WSL
* 修复 WSL 中的挂起问题。 [GH 3039, 3034]

## <a name="build-17128-fast"></a>生成 17128 (快速)
有关生成17128的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。

### <a name="wsl"></a>WSL
* 无

## <a name="build-17627-skip-ahead"></a>生成 17627 (向前跳过)
有关生成17627的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 添加对 futex pi 感知操作的支持。 [GH 1006]
    * 请注意, 目前不支持优先级, 因此存在一些限制, 但应解除标准使用的 WSL。
* Windows 防火墙对 WSL 进程的支持。 [GH 1852]
    * 例如, 若要允许 WSL python 进程侦听任何端口, 请使用提升的 Windows cmd:```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * 有关如何添加防火墙规则的其他详细信息, 请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* 使用 wsl 时, 请尊重用户的默认外壳。 [GH 2372]
* 将所有网络接口报告为以太网。 [GH 2996]
* 更好地处理损坏的/etc/passwd 文件。 [GH 3001]

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17618-skip-ahead"></a>生成 17618 (向前跳过)
有关生成17618的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。

### <a name="wsl"></a>WSL
* 介绍用于 NT 互操作的 pseudoconsole 功能 [GH 988、1366、1433、1542、2370、2406]。
* 旧安装机制 (lxrun) 已弃用。 安装分发的支持机制是通过 Microsoft Store。

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17110"></a>版本 17110
有关生成17110的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。

### <a name="wsl"></a>WSL
* 允许从 Windows 终止/init [GH 2928]。
* 默认情况下, DrvFs 在默认情况下使用每个目录的区分大小写 (相当于 "case = dir" 装载选项)。
    * 使用 "case = force" (旧行为) 需要设置注册表项。 如果需要使用, 请运行以下命令启用 "case = force": reg add HKLM\SYSTEM\CurrentControlSet\Services\lxss/v DrvFsAllowForceCaseSensitivity/t REG_DWORD/d 1
    * 如果在较早版本的 Windows 中使用 WSL 创建了现有目录 (需要区分大小写), 请使用 dism.exe 将它们标记为区分大小写: setcasesensitiveinfo <path> enable
* NULL 终止从 uname syscall 返回的字符串。

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17107"></a>生成17107
有关生成17107的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。

### <a name="wsl"></a>WSL
* 支持在 master pty 终结点上的 TCSETSF 和 TCSETSW [GH 2552]。
* 启动并发互操作进程可能会导致 EINVAL [GH 2813]。
* 修复 PTRACE_ATTACH 以在/proc/pid/status. 中显示正确的跟踪状态
* 修复了在不清除 TID 地址的情况下, 通过 CLEARTID 和 SETTID 标志克隆的生存期较短的进程可能退出的争用。
* 在从17093之前的版本迁移时, 在升级 Linux 文件系统目录时显示一条消息。 有关17093文件系统更改的更多详细信息, 请参阅[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)的发行说明。

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17101"></a>生成17101
有关生成17101的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。

### <a name="wsl"></a>WSL
* 支持 signalfd。 [GH 129]
* 支持包含非法 NTFS 字符的文件名, 方法是将它们编码为私有 Unicode 字符。 [GH 1514]
* 当不支持写入时, 自动装入将回退为只读。 [GH 2603]
* 允许粘贴 Unicode 代理项对 (如表情符号)。 [GH 2765]
* /Proc 和/sys 中的伪文件应从 select、轮询、epoll、et al 返回读取和写入准备就绪。 [GH 2838]
* 修复问题: 当注册表被篡改或损坏时, 可能导致服务进入无限循环。
* 修复 netlink 消息以使用 iproute2 的更新版本 (上游 4.14)。

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17093"></a>生成17093
有关生成17093的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。

#### <a name="important"></a>重要提示：
升级到此版本后首次启动 WSL 时, 需要执行一些操作来升级 Linux 文件系统目录。 这可能需要几分钟, 因此 WSL 的启动速度可能会很慢。 对于从应用商店中安装的每个分发, 此操作应只发生一次。
* 改进了 DrvFs 中的区分大小写支持。
    * DrvFs 现在支持每个目录的区分大小写。 这是一种新的标志, 可对目录进行设置, 以指示应将这些目录中的所有操作视为区分大小写, 甚至允许 Windows 应用程序正确打开仅大小写不同的文件。
    * DrvFs 有新的装载选项, 这些选项控制每个目录的区分大小写
        * case = force: 所有目录都被视为区分大小写 (驱动器根除外)。 用 WSL 创建的新目录将标记为区分大小写。 这是旧的行为, 但将新目录标记为区分大小写。
        * case = dir: 只有具有每个目录大小写区分标志的目录才被视为区分大小写;其他目录不区分大小写。 用 WSL 创建的新目录将标记为区分大小写。
        * case = off: 仅将具有每个目录大小写敏感度标志的目录视为区分大小写;其他目录不区分大小写。 用 WSL 创建的新目录标记为不区分大小写。
    * 注意: 以前版本中的 WSL 创建的目录未设置此标志, 因此, 如果使用 "case = dir" 选项, 则不会将其视为区分大小写。 即将推出一种在现有目录上设置此标志的方法。
    * 装载这些选项的示例 (对于现有驱动器, 必须先卸载, 然后才能装载不同选项): sudo mount-t drvfs C:/mnt/c-o case = dir
    * 目前, case = force 仍是默认选项。 以后将更改为 case = dir。
* 你现在可以在安装 DrvFs 时使用 Windows 路径中的正斜杠, 例如: sudo mount-t DrvFs//server/share/mnt/share
* WSL 现在会在实例启动期间处理/etc/fstab 文件 [GH 2636]。
    * 这是在自动装载 DrvFs 驱动器之前完成的;fstab 已装载的任何驱动器都不会自动重新装载, 使你可以更改特定驱动器的装入点。
    * 使用 wsl 可以关闭此行为。
* /Proc 中的 mount、mountinfo 和 mountstats 文件正确地转义特殊字符, 如反斜杠和空格 [GH 2799]
* 启用元数据后, 通过 DrvFs 创建的特殊文件 (如 WSL 符号链接或 fifos 和套接字) 现在可以从 Windows 复制和移动。

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL 更易于配置 WSL
添加了一种方法, 用于在 WSL 中自动配置某些功能, 这些功能将在每次启动子系统时应用。 这包括自动装载选项和网络配置。 在博客文章中了解更多相关信息: https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX 允许在 WSL 和 Windows 本机进程上的 Linux 进程之间进行套接字连接
现在, WSL 和 Windows 应用程序可以通过 Unix 套接字彼此通信。 假设你想要在 Windows 中运行服务, 并使其可用于 Windows 和 WSL 应用。 现在, 可以通过 Unix 套接字实现。 有关详细信息, 请阅读我们的博客文章 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* 支持带有 MAP_NORESERVE 的 mmap () [GH 121, 2784]
* 支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121, 2781]
* 处理克隆中的非 SIGCHLD 终止信号 [GH 121, 2781]
* 存根/proc/sys/fs/inotify/max_user_instances 和/proc/sys/fs/inotify/max_user_watches [GH 1705]
* 加载包含非零偏移量的负载标头的 ELF 二进制文件时出错 [GH 1884]
* 加载图像时, 为零个尾随页字节。
* 减少 execve 以静默方式终止进程的情况

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17083"></a>版本 17083
有关生成17083的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。

### <a name="wsl"></a>WSL
* 修复了与 epoll 相关的检测错误 [GH 2798、2801、2857]
* 修复了关闭 ASLR 时挂起 [GH 1185, 2870]
* 确保 mmap 操作出现原子 [GH 2732]

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17074"></a>生成17074
有关生成17074的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。

### <a name="wsl"></a>WSL
* 固定存储格式的 DrvFs 元数据 [GH 2777] </br>
**重要说明：** 在此生成之前创建的 DrvFs 元数据将错误显示或根本不显示。 若要修复受影响的文件, 请使用 chmod 和 chown 重新应用元数据。
* 修复了多个信号和可重启 syscall 的问题。

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17063"></a>生成17063
有关生成17063的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。

### <a name="wsl"></a>WSL
* DrvFs 支持其他 Linux 元数据。 这允许使用 chmod/chown 设置文件的所有者和模式, 还可以创建特殊文件 (如 fifos、unix 套接字和设备文件)。 默认情况下, 此功能处于禁用状态, 因为它仍在实验中。
**注意：** 修复了 DrvFs 使用的元数据格式的错误。 当元数据在此生成上适用于试验时, 将来的生成将无法正确读取此生成创建的元数据。  你可能需要手动更新已修改文件的所有者, 并且必须重新创建具有自定义设备 ID 的设备。

  若要启用, 请使用 metadata 选项装载 DrvFs (若要在现有装载上启用它, 必须先卸载它):

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 权限作为附加的元数据添加到文件;它们不会影响 Windows 权限。  请记住, 使用 Windows 编辑器编辑文件可能会删除元数据。 在这种情况下, 该文件将恢复为默认权限。

* 向 DrvFs 添加了装载选项, 以控制没有元数据的文件。
  * uid: 用于所有文件所有者的用户 ID。
  * gid: 用于所有文件的所有者的组 ID。
  * umask: 要排除所有文件和目录的权限的八进制掩码。
  * fmask: 为所有常规文件排除的权限的八进制掩码。
  * dmask: 为所有目录排除的权限的八进制掩码。

  例如：
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  与 metadata 选项结合, 可指定没有元数据的文件的默认权限。

* 引入了一个新的环境`WSLENV`变量, 用于配置环境变量在 WSL 和 Win32 之间的流动方式。

  例如：

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV`以冒号分隔的环境变量列表, 可以在从 WSL 启动 Win32 或 Win32 进程中的 WSL 进程时包含这些变量。  每个变量可以用斜杠 (后跟标志) 作为后缀, 以指定它的转换方式。
  * h-p值是应在 WSL 路径与 Win32 路径之间进行转换的路径。
  * l值是路径的列表。 在 WSL 中, 它是用冒号分隔的列表。 在 Win32 中, 它是一个以分号分隔的列表。
  * 形仅应在从 Win32 调用 WSL 时包含值
  * 水平仅应在从 WSL 调用 Win32 时包括该值

  可以在 .bashrc `WSLENV`中或在用户的自定义 Windows 环境中设置。

* drvfs 装入正确保留 tar、cp-p (GH 1939) 的时间戳
* drvfs 符号链接报告正确大小 (GH 2641)
* 读/写适用于非常大的 IO 大小 (GH 2653)
* waitpid 适用于进程组 Id (GH 2534)
* 显著提高了大型保留区域的 mmap 性能;提高 ghc 性能 (GH 1671)
* 个性支持 READ_IMPLIES_EXEC;修复最大值和 clisp (GH 1185)
* mprotect 支持 PROT_GROWSDOWN;修补 clisp (GH 1128)
* 过载模式下的页错误修复;修补 sbcl (GH 1128)
* 克隆支持更多标志组合
* 支持 epoll 文件的 select/epoll (以前为无操作)。
* 通知 ptrace 未实现的 syscall。
* 生成 resolv.conf 名称服务器时忽略未启动的接口 [GH 2694]
* 枚举没有物理地址的网络接口。 [GH 2685]
* 其他 bug 修复和改进。

### <a name="linux-tools-available-to-developers-on-windows"></a>适用于 Windows 上的开发人员的 Linux 工具

* Windows 命令行工具链包括 bsdtar (tar) 和曲线。
  阅读[此博客](https://aka.ms/tarcurlwindows), 了解有关添加这两个新工具的详细信息, 并了解如何在 Windows 上形成开发人员体验。

*   `AF_UNIX`适用于 Windows 有问必答 SDK (17061 +)。
  阅读[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/), 了解有关如何`AF_UNIX`在 Windows 上使用开发人员以及如何使用它的详细信息。

### <a name="console"></a>控制台
* 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。


## <a name="build-17046"></a>生成17046

有关生成17046的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。

### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 允许在没有活动终端的情况下运行进程。 [GH 709, 1007, 1511, 2252, 2391, et al]
- 更好地支持 CLONE_VFORK 和 CLONE_VM。 [GH 1878, 2615]
- 跳过 WSL 网络操作的 TDI 筛选器驱动程序。 [GH 1554]
- 满足某些条件时, DrvFs 将创建 NT 符号链接。 [GH 353, 1475, 2602]
    - 链接目标必须是相对的, 不能跨任何装入点或符号链接, 并且必须存在。
    - 用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE (这通常需要你启动 wsl), 除非已打开开发人员模式。
    - 在所有其他情况下, DrvFs 仍创建 WSL 符号链接。
- 允许同时运行提升和非提升的 WSL 实例。
- 支持/proc/sys/kernel/yama/ptrace_scope
- 添加 wslpath 以执行 WSL < > Windows 路径转换。 [GH 522, 1243, 1834, 2327, et al]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>控制台
- 无修补程序。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。


## <a name="build-17040"></a>生成17040

有关生成17040的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 自17035以来没有修复。

#### <a name="console"></a>控制台
- 自17035以来没有修复。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17035"></a>生成17035

有关生成17035的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 访问 DrvFs 上的文件有时会因 EINVAL 而失败。 [GH 2448]

#### <a name="console"></a>控制台
- 在 VT 模式下插入/删除行时的一些颜色损失。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17025"></a>生成17025

有关生成17025的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 启动新的前台进程组中的初始进程 [GH 1653, 2510]。
- SIGHUP 传递修复 [GH 2496]。
- 如果未提供, 则生成默认的虚拟桥名称 [GH 2497]。
- 实现/proc/sys/kernel/random/boot_id [GH 2518]。
- 更多互操作 stdout/stderr 管道修补程序。
- 存根 syncfs 系统调用。

#### <a name="console"></a>控制台
- 修复第三方控制台的输入 VT 转换 [GH 111]

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="build-17017"></a>生成17017

有关生成17017的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 忽略空的 ELF 程序头 [GH 330]。
- 允许 LxssManager 为非交互式用户 (ssh 和计划任务支持) 创建 WSL 实例 [GH 777, 1602]。
- 支持 WSL-> Win32 > WSL ("开始") 方案 [GH 1228]。
- 对通过互操作调用的控制台应用终止的有限支持 [GH 1614]。
- 支持 devpts [GH 1948] 的装载选项。
- Ptrace 阻止子启动 [GH 2333]。
- EPOLLET 缺少某些事件 [GH 2462]。
- 返回 PTRACE_GETSIGINFO 的更多数据。
- 带有 lseek 的 Getdents 提供了不正确的结果。
- 修复某些 Win32 互操作应用挂起, 并等待管道中没有更多数据的输入。
- O_ASYNC 支持 tty/pty 文件。
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 此版本中没有与控制台相关的更改。

### <a name="ltp-results"></a>LTP 结果:
正在进行测试。

## <a name="fall-creators-update"></a>秋季创意者更新

## <a name="build-16288"></a>生成16288

有关生成16288的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 正确初始化和报告套接字文件描述符的 uid、gid 和模式 [GH 2490]
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 此版本中没有与控制台相关的更改。

### <a name="ltp-results"></a>LTP 结果:
自16273以来无更改

## <a name="build-16278"></a>生成16278

有关生成162738的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 当撕裂 LX MM 状态 [GH 2415] 时, 显式取消文件所支持节的映射视图
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 此版本中没有与控制台相关的更改。

### <a name="ltp-results"></a>LTP 结果:
自16273以来无更改

## <a name="build-16275"></a>生成16275

有关生成162735的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 此版本中没有与 WSL 相关的更改。

#### <a name="console"></a>控制台
- 此版本中没有与控制台相关的更改。

### <a name="ltp-results"></a>LTP 结果:
自16273以来无更改

## <a name="build-16273"></a>生成16273

有关生成16273的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 解决了 DrvFs 有时报告了目录的错误文件类型 [GH 2392] 的问题
- 允许创建 NETLINK_KOBJECT_UEVENT 套接字来取消阻止使用 UEVENT 的程序 [GH 1121、2293、2242、2295、2235、648、637]
- 添加对非阻止连接的支持 [GH 903、1391、1584、1585、1829、2290、2314]
- 实现 CLONE_FS 克隆系统调用标志 [GH 2242]
- 解决了在 NT 互操作中无法正确处理选项卡或引号的问题 [GH 1625, 2164]
- 尝试重新启动 WSL 实例时解决拒绝访问错误 [GH 651, 2095]
- 实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]
- 修补各种 SysFs 文件的权限 [GH 2214]
- 在安装过程中修复 Haskell stack 挂起 [GH 2290]
- 实现 binfmt_misc "C"、"O" 和 "P" 标志 [GH 2103]
- 添加/proc/sys/kernel/shmmax/shmmni &/threads-max [GH 1753]
- 添加对 ioprio_set 系统调用的部分支持 [GH 498]
- 存根 SO_REUSEPORT & 为 netlink 套接字添加对 SO_PASSCRED 的支持 [GH 69]
- 如果当前正在安装或卸载分发, 则从 RegisterDistribuiton 返回不同的错误代码。
- 允许通过 wslconfig 取消注册部分安装的 WSL 分发
- 从 udp:: msg_peek 修复 python 套接字测试挂起
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 此版本中没有与控制台相关的更改。

### <a name="ltp-results"></a>LTP 结果:
总测试数:1904<br/>
跳过的测试总数:209<br/>
失败总数:229<br/>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>版本 16257

有关生成16257的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 实现 prlimit64 系统调用
- 添加对 ulimit 的支持-n (setrlimit RLIMIT_NOFILE) [GH 1688]
- 用于 TCP 套接字的存根 MSG_MORE [GH 2351]
- 修复无效的 AT_EXECFN 辅助矢量行为 [GH 2133]
- 修复 console/tty 的复制/粘贴行为, 并添加更好的完整缓冲区处理 [GH 2204, 2131]
- 设置用户 ID 和组-ID 程序的辅助向量中的 AT_SECURE [GH 2031]
- 伪类-终端主终结点未处理 TIOCPGRP [GH 1063]
- 修复 lseek 在 LxFs 中倒带目录 [GH 2310]
- 使用繁重的/dev/ptmx 锁 [GH 1882]
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 在任何位置修复水平线条/下划线 [GH 2168]
- 解决处理顺序更改, 使 NPM 更难关闭 [GH 2170]
- 添加了新的配色方案: https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP 结果:
自16251以来无更改

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`prlimit64`<br/>

### <a name="known-issues"></a>已知问题
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub 问题 2392:WSL 无法识别的 Windows 文件夹 .。。](https://github.com/Microsoft/BashOnWindows/issues/2392)
在版本16257中, WSL 在通过`/mnt/c/...`枚举 Windows 文件/文件夹时遇到问题。
此问题已修复, 应在第一周的第一8/14/2017 周的内部版本中发布。

<br/>

## <a name="build-16251"></a>生成16251

有关生成16251的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 从 WSL 可选组件中删除 beta 标记, 有关详细信息, 请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)。
- 正确地为 exec [GH 962, 1415, 2072] 上的设置用户 ID 和组 ID 二进制文件初始化已保存的设置的 uid 和 gid
- 添加了对 ptrace PTRACE_O_TRACEEXIT 的支持 [GH 555]
- 添加了对 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 的支持, NT_FPREGSET [GH 555]
- 修复了在忽略信号时停止的 ptrace
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 此版本中没有与控制台相关的更改。

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:768</br>
失败的测试数:244</br>
跳过的测试数:96</br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>生成16241

有关生成16241的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 此版本中没有与 WSL 相关的更改。

#### <a name="console"></a>控制台
- 修复了[以下](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)问题, 以便为每12月的交叉行输出错误的字符。
- 修复代码页 65001 (utf8) 中没有显示的输出文本
- 不要将对一种颜色的 RGB 值所做的更改传输到选定内容更改的调色板的其他部分。 这会使控制台属性表更易于使用。
- Ctrl + S 似乎无法正常工作
- ANSI 转义代码中完全不存在的粗体/-Dim [GH 2174]
- 控制台无法正确支持 Vim 颜色主题 [GH 1706]
- 无法粘贴特定字符 [GH 2149]
- 当内容在编辑/命令行上时, 重新调整大小会与奇怪交互, 同时调整 bash 窗口的大小 [GH ConEmu 1123]
- 按住 Ctrl 的同时屏幕会脏 [GH 1978]
- 在 HDPI 上显示 VT 时的控制台呈现 bug [GH 1907]
- Unicode 字符 U + 30FB 的 Japansese 字符看起来很奇怪 [GH 2146]
- 其他改进和 bug 修复

</br>

## <a name="build-16237"></a>版本 16237

有关生成16237的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。<br/>


### <a name="fixed"></a>固定
- 在 lxfs 中使用不带 Ea 的文件的默认属性 (root、root、0000)
- 添加了对使用扩展属性的分发的支持
- 修复 getdents 和 getdents64 返回的项的填充
- 针对 shmctl SHM_STAT 系统调用修复权限检查 [GH 2068]
- 修复了 tty 的初始 epoll 状态 [GH 2231]
- 修复 DrvFs readdir 不返回所有条目 [GH 2077]
- 取消链接文件时修复 LxFs readdir [GH 2077]
- 允许通过 procfs 重新打开未链接的 drvfs 文件
- 添加了用于禁用 WSL 功能的全局注册表项替代 (互操作性/驱动器安装)
- 修复 DrvFs (和 LxFs) 的 "stat" 中错误的块计数 [GH 1894]
- 其他改进和 bug 修复

</br>

## <a name="build-16232"></a>生成16232

有关生成16232的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。<br/>


### <a name="fixed"></a>固定
- 此版本中没有与 WSL 相关的更改。

</br>

## <a name="build-16226"></a>生成16226

有关生成16226的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。<br/>


### <a name="fixed"></a>固定
- xattr 相关 syscall 支持 (getxattr、setxattr、listxattr、removexattr)。
- capablity xattr 支持。
- 提高了与某些文件系统和筛选器 (包括非 MS SMB 服务器) 的兼容性。 [GH #1952]
- 改进了对 OneDrive 占位符、GVFS 占位符和精简操作系统压缩文件的支持。
- 其他改进和 bug 修复

</br>

## <a name="build-16215"></a>生成16215

有关生成16215的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。<br/>


### <a name="fixed"></a>固定
- WSL 不再需要开发人员模式。
- 支持 drvfs 中的目录联接。
- 处理 WSL 分发 appx 包的卸载。
- 更新 procfs 以显示专用和共享映射。
- 添加 wslconfig 的功能以清理部分安装或卸载的分发。
- 添加了对 TCP 套接字 IP_MTU_DISCOVER 的支持。 [GH 1639, 2115, 2205]
- 推断协议系列以便路由到 AF_INADDR。
- 串行设备改进 [GH 1929]。

</br>

## <a name="build-16199"></a>生成16199

有关生成16199的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。<br/>


### <a name="fixed"></a>固定
- 这些版本中没有与 WSL 相关的更改。

</br>

## <a name="build-16193"></a>生成16193

有关生成16193的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。<br/>


### <a name="fixed"></a>固定
- 发送 SIGCONT 和 threadgroup 终止之间的争用条件 [GH 1973]
- 将 tty 和 pty 设备更改为 report FILE_DEVICE_NAMED_PIPE, 而不是 FILE_DEVICE_CONSOLE [GH 1840]
- IP_OPTIONS 的 SSH 修补程序
- 已将 DrvFs 装载迁移到 init daemon [GH 1862、1968、1767、1933]
- 为以下 NT 符号链接添加了 DrvFs 中的支持。

</br>

## <a name="build-16184"></a>生成16184

有关生成16184的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。<br/>


### <a name="fixed"></a>固定
- 删除 apt 包维护任务 (lxrun/update)
- 固定输出不显示在 node.js 中的 Windows 进程中 [GH 1840]
- 放宽 lxcore 中的对齐要求 [GH 1794]
- 修复了 AT_EMPTY_PATH 标志在系统调用收藏中的处理。
- 修复了删除 DrvFs 文件和打开句柄的问题时, 文件会显示未定义的行为 [GH 544、966、1357、1535、1615]
- /etc/hosts 现在将从 Windows hosts 文件 (%windir%\system32\drivers\etc\hosts) 继承条目 [GH 1495]

</br>

## <a name="build-16179"></a>生成16179

有关生成16179的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。<br/>


### <a name="fixed"></a>固定
- 本周不会更改 WSL。

</br>

## <a name="build-16176"></a>生成16176

有关生成16176的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。<br/>


### <a name="fixed"></a>固定

- [启用的串行支持](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 添加了 IP 套接字选项 IP_OPTIONS [GH 1116]
- 实现的 pwritev 函数 (在将文件上传到 nginx/PHP-PHP-FPM) [GH 1506]
- 添加的 IP 套接字选项 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- 支持套接字选项 IP_MULTICAST_LOOP & IPV6_MULTICAST_LOOP [GH 1678]
- 添加了适用于 apps 节点、traceroute、挖掘、nslookup、主机的 IP (V6) _MTU 套接字选项
- 添加的 IP 套接字选项 IPV6_UNICAST_HOPS
- [文件系统改进](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * 允许装载 UNC 路径
    * 在 drvfs 中启用 CDFS 支持
    * 正确处理 drvfs 中网络文件系统的权限
    * 向 drvfs 添加远程驱动器支持
    * 在 drvfs 中启用 FAT 支持
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果
自15042以来无更改

</br>

## <a name="build-16170"></a>生成16170

有关生成16170的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。<br/>

我们发布了新的[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/), 讨论了测试 WSL 的努力。

### <a name="fixed"></a>固定

- Support socket 选项 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- 添加对 PTRACE_OLDSETOPTIONS 的支持。 [GH 1692]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果
自15042以来无更改

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>生成15046到 Windows 10 创意者更新
没有更多的 WSL 修补程序或功能已计划包含在 Windows 10 的创意者更新中。 WSL 的发行说明将在接下来的几周内恢复, 添加目标为下一个主要 Windows 更新。 有关生成15046和未来的内部版本的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。 <br/><br/>
 <br/>

## <a name="build-15042"></a>生成15042

有关生成15042的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。<br/>


### <a name="fixed"></a>固定

- 解决在删除以 "..." 结尾的路径时出现死锁的问题
- 修复了 FIONBIO 在成功时不返回0的问题 [GH 1683]
- 修复了 inet 数据报套接字的长度为零的问题
- 由于 drvfs inode 查找中的争用条件, 修复可能的死锁 [GH 1675]
- 扩展了对 unix 套接字辅助数据的支持;SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514, 613, 1326]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:737</br>
未通过的数目 (失败，已跳过，等等...):255

</br>

## <a name="build-15031"></a>生成15031

有关生成15031的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。<br/>


### <a name="fixed"></a>固定

- 修复了时间 (2) 偶尔错误行为的 bug。
- 已修复并发出 * SIGPROCMASK syscall 可能会损坏信号掩码。
- 现在, 在 WSL 进程创建通知中返回完整的命令行长度。 [GH 1632]
- WSL 现在报告通过 ptrace 的线程退出, 以获得 GDB 挂起。 [GH 1196]
- 修复了严重 tmux IO 后 ptys 将挂起的 bug。 [GH 1358]
- 修复了许多系统调用中的超时验证 (futex、semtimedop、ppoll、sigtimedwait、itimer、timer_create)
- 添加了 eventfd EFD_SEMAPHORE 支持 [GH 452]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:737</br>
未通过的数目 (失败，已跳过，等等...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>生成15025

有关生成15025的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。<br/>


### <a name="fixed"></a>固定

- 修复破坏 grep 2.27 [GH 1578] 的 bug
- Eventfd2 syscall 的已实现 EFD_SEMAPHORE 标志 [GH 452]
- 已实现的/proc/[pid]/net/ipv6_route [GH 1608]
- 面向 unix 流套接字的信号驱动 IO 支持 [GH 393, 68]
- 支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]
- 实现 recvmmsg () syscall [GH 1531]
- 修复了 epoll_wait () 未在等待的 bug [GH 1609]
- 实现/proc/version_signature
- 如果两个文件说明符引用同一管道, 则
- 为 SO_PEERCRED for Unix 套接字实现了正确行为
- Fixed tkill syscall 无效的参数处理
- 更改以提高 drvfs 的 preformace
- Ruby IO 阻止的次要修补程序
- Fixed recvmsg () 为 inet 套接字的 MSG_DONTWAIT 标志返回 EINVAL [GH 1296]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:732</br>
未通过的数目 (失败，已跳过，等等...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>生成15019

有关生成15019的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。<br/>


### <a name="fixed"></a>固定

- 修复了在 procfs 中错误报告了 CPU 使用率的 bug, 如 htop (GH 823、945、971)
- 在现有文件上对 O_TRUNC 调用 open () 时, inotify 现在会在 IN_OPEN 之前生成 IN_MODIFY
- 修复了 unix 套接字 getsockopt SO_ERROR 以启用 postgress [GH 61, 1354]
- 为中转语言实现/proc/sys/net/core/somaxconn
- Apt-获取包更新后台任务现在从视图中运行隐藏
- 清除 ipv6 localhost 的作用域 (弹簧框架 (Java) 故障)。
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:714 </br>
未通过的数目 (失败，已跳过，等等...):249 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>生成15014

有关生成15014的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定

- Ctrl + C 现在按预期方式工作
- htop 和 ps auxw 现在显示正确的资源利用率 (GH #516)
- 将 NT 异常转换为信号的基本转换。 (GH #513)
- 当空间不足而不是 EINVAL (GH #1571) 时, fallocate 现在会失败 ENOSPC
- 添加的/proc/sys/kernel/sem。
- 实现 semop 和 semtimedop 系统调用
- 修复了 IP_RECVTOS & IPV6_RECVTCLASS 套接字选项的 nslookup 错误 (GH 69)
- 支持套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:709 </br>
未通过的数目 (失败，已跳过，等等...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 摘要
总 Syscall:384 </br>
已实现的总数:235 </br>
总用作存根:22 </br>
未实现总数:127 </br>
[详细细目](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>生成15007

有关生成15007的常规 Windows 信息, 请访问[Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。<br/>


### <a name="known-issue"></a>已知问题

- 有一个已知 bug, 控制台无法识别某些 Ctrl + <key>输入。  这包括将充当普通 "c" 按键的 ctrl-c 命令。

  - 解决方法：将备用键映射到 Ctrl + C。 例如, 若要将 Ctrl + K 映射到 Ctrl + C, `stty intr \^k`请执行:。  此映射按终端进行, 并且*每*次启动 bash 时都必须执行此映射。 用户可以在其`.bashrc`

### <a name="fixed"></a>固定

- 更正了运行 WSL 会消耗 100% 的 CPU 内核的问题
- 套接字选项 IP_PKTINFO、IPV6_RECVPKTINFO 现在支持。 (GH #851, 987)
- 在 lxcore (GH #1452, 1414, 1343, 468, 308) 中将网络接口物理地址截断为16字节
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:709 </br>
未通过的数目 (失败，已跳过，等等...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>生成15002

有关生成15002的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。<br/>


### <a name="known-issue"></a>已知问题

两个已知问题:
- 有一个已知 bug, 控制台无法识别某些 Ctrl + <key>输入。  这包括将充当普通 "c" 按键的 ctrl-c 命令。

  - 解决方法：将备用键映射到 Ctrl + C。 例如, 若要将 Ctrl + K 映射到 Ctrl + C, `stty intr \^k`请执行:。  此映射按终端进行, 并且*每*次启动 bash 时都必须执行此映射。 用户可以在其`.bashrc`

- 当 WSL 运行时, 系统线程将消耗 100% 的 CPU 内核。  根本原因已解决并在内部修复。

### <a name="fixed"></a>固定

- 现在必须在同一权限级别创建所有 bash 会话。  尝试在不同级别启动会话将被阻止。  这意味着管理员和非管理员控制台不能同时运行。 (GH #626)
<br/>
- 实现以下 NETLINK_ROUTE 消息 (需要 Windows 管理员)
     - RTM_NEWADDR (支持`ip addr add`)
     - RTM_NEWROUTE (支持`ip route add`)
     - RTM_DELADDR (支持`ip addr del`)
     - RTM_DELROUTE (支持`ip route del`)
- 要更新的包的计划任务检查将不再对按流量计费的连接运行 (GH #1371)
- 修复了管道停滞的错误, 即 bash-c "ls-alR/" |bash-c "cat" (GH #1214)
- 已实现 TCP_KEEPCNT 套接字选项 (GH #843)
- 实现的 IP_MTU_DISCOVER INET 套接字选项 (GH #720、717、170、69)
- 删除了旧功能, 可通过 NT 路径查找从 init 运行 NT 二进制文件。 (GH #1325)
- 修复/dev/kmsg 模式以允许组/其他读访问 (0644) (GH #1321)
- 实现的/proc/sys/kernel/random/uuid (GH #1092)
- 更正了进程开始时间显示为2432年的错误 (GH #974)
- 切换到 xterm-256color (GH #1446) 的默认术语环境变量
- 修改了处理分叉期间计算处理提交的方式。 (GH #1286)
- 实现的/proc/sys/vm/overcommit_memory。 (GH #1286)
- 实现的/proc/net/route 文件 (GH #69)
- 修复了快捷方式名称错误本地化的错误 (GH #696)
- 已修复不正确验证程序标头的 elf 解析逻辑必须小于 (或等于) PATH_MAX。 (GH #1048)
- 为 procfs、sysfs、cgroupfs 和 binfmtfs (GH #1378) 实现了 statfs 回调
- 修复了不会关闭的 AptPackageIndexUpdate 窗口 (GH #1184, 还会在 GH #1193 中讨论)
- 添加了 ASLR 个性 ADDR_NO_RANDOMIZE 支持。 (GH #1148, 1128)
- 改善了 PTRACE_GETSIGINFO、SIGSEGV, 适用于 AV 期间的适当 gdb 堆栈跟踪 (GH #875)
- Patchelf 二进制文件的 Elf 分析不再失败。 (GH #471)
- VPN DNS 传播到/etc/resolv.conf (GH #416, 1350)
- 提高 TCP 关闭以实现更可靠的数据传输。 (GH #610, 616, 1025, 1335)
- 现在, 在打开太多文件时返回正确的错误代码 (EMFILE)。 (GH #1126, 2090)
- Windows 审核日志现在会报告进程创建审核中的映像名称。
- 从 bash 窗口中启动 bash 时, 现在正常失败
- 在互操作无法访问 LxFs 下的工作目录时添加了错误消息 (例如 .bashrc)
- 修复了在 WSL 中截断 Windows 路径的问题
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:690 </br>
未通过的数目 (失败，已跳过，等等...):274 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>生成14986

有关生成14986的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。<br/>


### <a name="fixed"></a>固定

- 修复了与 Netlink 和 Pty IOCTLs 的错误检查
- 内核版本现在报告 4.4.0-43 与 Xenial 的一致性
- 当输入定向到 "nul:" (GH #1259) 时, Bash 立即启动
- 线程 Id 现在在 procfs 中报告正确 (GH #967)
- IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |Inotify_add_watch () 中现支持 IN_ISDIR 标志 (GH #1280)
- 实现 timer_create 和相关的系统调用。  这将启用 GHC 支持 (GH #307)
- 修复了 ping 返回时间 0.000 ms 的问题 (GH #1296)
- 当打开太多文件时, 返回正确的错误代码。
- 修复了 WSL 中的问题: 如果接口的硬件地址为32字节 (如 Teredo 接口), 则网络接口数据的 Netlink 请求将会失败, 并出现 EINVAL。
   - 请注意, Linux "ip" 实用工具包含一个 bug, 如果 WSL 报告了32字节的硬件地址, 它会崩溃。 这是 "ip" 中的错误, 而不是 WSL。 "Ip" 实用工具将用于打印硬件地址的字符串缓冲区的长度硬编码, 而该缓冲区太小, 无法打印32字节的硬件地址。
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:669 </br>
未通过的数目 (失败，已跳过，等等...):258 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>生成14971

有关生成14971的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。<br/>


### <a name="fixed"></a>固定

 - 由于控件之外的情况, 对于适用于 Linux 的 Windows 子系统, 此版本中没有更新。  定期计划的更新将在下一版本中继续进行。

### <a name="ltp-results"></a>LTP 结果:
从14965无变化 </br>
通过的测试数:664 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>生成14965

有关生成14965的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。<br/>


### <a name="fixed"></a>固定

- 支持 Netlink socket NETLINK_ROUTE 协议的 RTM_GETLINK 和 RTM_GETADDR (GH #468)
  - 为网络枚举启用 ifconfig 和 ip 命令
  - 有关详细信息, 请参阅[WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。

- 默认情况下,/sbin 现在位于用户的路径中
- 默认情况下, NT 用户路径现在追加到 WSL 路径 (即, 你现在可以键入 notepad.exe, 无需向 Linux 路径添加 System32)
- 添加了对/proc/sys/kernel/cap_last_cap 的支持
- 当当前工作目录包含非 ansi 字符时, 现在可以从 WSL 启动 NT 二进制文件 (GH #1254)
- 允许在断开连接的 unix 流套接字上关闭。
- 添加了对 PR_GET_PDEATHSIG 的支持。
- 添加了对 CLONE_PARENT 的支持
- 修复了管道停滞的错误, 即 bash-c "ls-alR/" |bash-c "cat" (GH #1214)
- 处理连接到当前终端的请求。
- 将/proc/<pid>/oom_score_adj 标记为可写。
- 添加/sys/fs/cgroup 文件夹。
- sched_setaffinity 应返回关联位掩码的数目
- 修复不正确假定解释器路径的 ELF 验证逻辑长度必须小于64个字符。 (GH #743)
- 打开文件描述符会使控制台窗口保持打开状态 (GH #1187)
- Fixeed 错误, 其中重命名 () 失败, 目标名称上有尾随斜杠 (GH #1008)
- 实现/proc/net/dev 文件
- 已修复 0.000 ms ping, 因为计时器分辨率。
- 实现的/proc/self/environ (GH #730)
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:664 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>生成14959

有关生成14959的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。<br/>


### <a name="fixed"></a>固定

- 改善了 Windows 的 Pico 过程通知。  [WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)上的其他信息。
- 提高了 Windows 互操作性的稳定性
- 修复了在启用企业数据保护 (EDP) 时启动 bash 时出现的错误0x80070057
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:665 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>生成14955

有关生成14955的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。<br/>


### <a name="fixed"></a>固定

 - 由于控件之外的情况, 对于适用于 Linux 的 Windows 子系统, 此版本中没有更新。  定期计划的更新将在下一版本中继续进行。

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:665 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>生成14951

有关生成14951的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>新功能:Windows/Ubuntu 互操作性
现在可以从 WSL 命令行直接调用 Windows 二进制文件。  这使用户能够以一种不可能的方式与其 Windows 环境和系统交互。  作为一个快速示例, 用户现在可以运行以下命令:

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

有关详细信息, 请参阅:

- [互操作的 WSL 团队博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN 互操作文档](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>固定

- 现在为所有新的 WSL 实例安装了 Ubuntu 16.04 (Xenial)。  将不会自动升级具有现有 14.04 (t) 实例的用户。
- 现在会显示安装过程中设置的区域设置
- 包含 bug 的终端改进, 其中将 WSL 进程重定向到文件并不总是有效
- 控制台生存期应该与 bash 生存期相关联
- 控制台窗口大小应使用可见大小, 而不是缓冲区大小
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:665 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>生成14946

有关生成14946的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。<br/>


### <a name="fixed"></a>固定

- 修复了阻止为具有包含空格或引号的 NT 用户名的用户创建 WSL 用户帐户的问题。 
- 更改 VolFs 和 DrvFs, 以在 stat 中为目录的链接计数返回0
- 支持 IPV6_MULTICAST_HOPS 套接字选项。
- 仅限每 tty 使用单个控制台 i/o 循环。 示例: 可以执行以下命令:
  - bash-c "回显数据" |bash-c "ssh user@example.com " cat > foo .txt ""

- 用/proc/cpuinfo 中的制表符替换空格 (GH #1115)
- DrvFs 现在显示在 mountinfo 中, 其名称与已装入的 Windows 卷匹配
- /home 和/root 现在显示在具有正确名称的 mountinfo 中
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:665 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>生成14942

有关生成14942的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/onefourninefourtwoooooo)。<br/>


### <a name="fixed"></a>固定

- 解决了多个错误检查, 包括正在阻止 SSH 的 "尝试执行 NOEXECUTE 内存" 网络崩溃
- inotifiy 对 DrvFs 上的 Windows 应用程序生成的通知的支持现已在
- 实现 TCP_KEEPIDLE 和 TCP_KEEPINTVL for mongod.exe。 (GH #695)
- 实现 pivot_root 系统调用
- 为 SO_DONTROUTE 实现套接字选项
- 其他 bug 修复和改进


### <a name="ltp-results"></a>LTP 结果:
通过的测试数:665 </br>
未通过的数目 (失败，已跳过，等等...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>生成14936

有关生成14936的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。<br/>


注意:在即将发布的版本中, WSL 将安装 Ubuntu 版本 16.04 (Xenial), 而不是 Ubuntu 14.04 (t)。  此更改将应用于安装新实例的预览体验 (lxrun/install 或首次运行 bash)。  具有 t 的现有实例将不自动升级。 用户可以使用 "t-升级" 命令将其 "" 映像升级到 Xenial。

### <a name="known-issue"></a>已知问题
WSL 遇到一些套接字实现问题。  错误检查会将自身视为崩溃, 并出现错误 "已尝试执行 NOEXECUTE 内存"。  此问题的最常见表现形式是使用 ssh 时出现故障。  根本原因是在内部版本中修复的, 将按最早的机会推送到内部版本。

### <a name="fixed"></a>固定

- 实现了 chroot 系统调用
- Inotify 中的改进~~, 包括支持在 DrvFs 上的 Windows 应用程序中生成的通知~~
  - 更正Inotify 对源自 Windows 应用程序的更改的支持目前不可用。
- 将套接字绑定到 IPV6<port n> :: 现在支持 IPV6_V6ONLY (GH #68、#157、#393、#460、#674、#740、#982、#996)
- Waitid systemcall 实现的 WNOWAIT 行为 (GH #638)
- 支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL
- 长度为零的读取 () 应立即返回 (GH #975)
- 正确处理在 tar 文件中不包括 NULL 终止符的文件名和文件名前缀。
- epoll 对/dev/null 的支持
- 修复/dev/alarm 时间源
- Bash-c 现在可以重定向到文件
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:664 </br>
未通过的数目 (失败，已跳过，等等...):264 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`chroot`<br/>
<br/>

## <a name="build-14931"></a>生成14931

有关生成14931的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。<br/>


### <a name="fixed"></a>固定

 - 由于控件之外的情况, 对于适用于 Linux 的 Windows 子系统, 此版本中没有更新。  定期计划的更新将在下一版本中继续进行。

<br/>

## <a name="build-14926"></a>生成14926

有关生成14926的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。<br/>


### <a name="fixed"></a>固定

- Ping 现在适用于没有管理员权限的控制台
- 现在还支持 Ping6, 无需管理员权限
- Inotify 支持通过 WSL 修改的文件。 (GH #216)
  - 支持的标志:
    - inotify_init1:LX_O_CLOEXEC, LX_O_NONBLOCK
    - inotify_add_watch 事件:LX_IN_ACCESS, LX_IN_MODIFY, LX_IN_ATTRIB, LX_IN_CLOSE_WRITE, LX_IN_CLOSE_NOWRITE, LX_IN_OPEN, LX_IN_MOVED_FROM, LX_IN_MOVED_TO, LX_IN_CREATE, LX_IN_DELETE, LX_IN_DELETE_SELF, LX_IN_MOVE_SELF
    - inotify_add_watch 属性:LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 读取输出:LX_IN_ISDIR, LX_IN_IGNORED
  - 已知问题:修改 Windows 应用程序中的文件不会生成任何事件
- Unix 套接字现在支持 SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP 结果:
通过的测试数:651 </br>
未通过的数目 (失败，已跳过，等等...):258 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>生成14915

有关生成14915的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定
-  Socketpair for unix 数据报套接字 (GH #262)
- 适用于 SO_REUSEADDR 的 Unix 套接字支持
- UNIX 套接字支持 SO_BROADCAST (GH #568)
- 适用于 SOCK_SEQPACKET (GH #758, #546) 的 Unix 套接字支持
- 添加对 unix 数据报套接字发送、接收和关闭的支持
- 由于非固定地址的 mmap 参数验证无效, 因此修复了检测错误。 (GH #847)
- 支持暂停/继续停止状态
- 支持 TIOCPKT ioctl 阻止屏幕实用工具 (GH #774)
    - 已知问题:功能键不可操作
- 更正了 TimerFd 中的争用, 这可能导致 LxpTimerFdWorkerRoutine (GH #814) 访问已释放的成员 "ReaderReady"
- 为 futex、投票和 clock_nanosleep 启用可重启的系统调用支持
- 添加了 bind 装载支持
- 用于装载命名空间支持的取消共享
    - 已知问题:使用`unshare(CLONE_NEWNS)`当前工作目录创建新的装载命名空间时, 将继续指向旧命名空间
- 其他改进和 bug 修复

<br/>

## <a name="build-14905"></a>生成14905

有关生成14905的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。<br/>


### <a name="fixed"></a>固定
- 现在支持可重启的系统调用 (GH #349, GH #520)
- 符号链接结束/立即操作的目录 (GH #650)
- 为/dev/random 实现了 RNDGETENTCNT ioctl
- 实现了/proc/[pid]/mounts、/proc/[pid]/mountinfo 和/proc/[pid]/mountstats 文件
- 其他 bug 修复和改进

</br>

## <a name="build-14901"></a>生成14901
Windows 10 周年更新版本的第一批内幕构建。

有关生成14901的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。<br/>


### <a name="fixed"></a>固定
- 修复了尾随斜杠问题
    - 像现在这样`$ mv a/c/ a/b/`的命令
- 如果 Ubuntu 区域设置应设置为 Windows 区域设置, 则立即安装
- Procfs 支持 ns 文件夹
- 添加了 tmpfs、procfs 和 sysfs 文件系统的装载和卸载
- 修复 mknod [at] 32 位 ABI 签名
- Unix 套接字已移动到调度模型
- INET 套接字接收使用 setsockopt 设置的缓冲区大小应遵守
- 实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志
- Linux 进程 stdin/stdout 管道重定向 (GH #2)
    - 允许在 CMD 中管道的 bash 命令。  示例: > dir |bash-c "grep foo"
- Bash 现在可以安装在具有多个页面页面 (GH #538, #358) 的系统上
- 默认的 INET 套接字缓冲区大小应与默认 Ubuntu 安装程序的大小匹配
- 将 xattr syscall 与 listxattr 对齐
- 仅返回具有 SIOCGIFCONF 的有效 IPv4 地址的接口
- 修复 ptrace 注入的信号默认操作
- 实现/proc/sys/vm/min_free_kbytes
- 还原 sigreturn 中的上下文时使用计算机上下文寄存器值
    - 这解决了某些用户的 java 和 javac 挂起的问题
- 实现/proc/sys/kernel/hostname

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>生成14388到 Windows 10 周年更新
有关生成14388的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/14388wip)。 <br/>

### <a name="fixed"></a>固定
- 修复了8/2 上 Windows 10 周年更新的准备工作
  - 有关周年更新中的 WSL 的详细信息, 请参阅我们的[博客](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>生成14376
有关生成14376的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。 <br/>

### <a name="fixed"></a>固定
- 删除了一些实例, 其中 apt 挂起 (GH #493)
- 修复了未正确处理空装载的问题
- 修复了 ramdisks 未正确装载的问题
- 更改 unix 套接字接受以支持标志 (部分 GH #451)
- 修复了与通用网络相关的蓝屏
- 修复了访问/proc/时的蓝屏 [pid]/task (GH #523)
- 修复了某些 pty 方案的高 CPU 使用率 (GH #488, #504)
- 其他 bug 修复和改进

<br/>

## <a name="build-14371"></a>生成14371
有关生成14371的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。 <br/>

### <a name="fixed"></a>固定
- 使用 ptrace 更正计时争用与 SIGCHLD 和 wait ()
- 当路径具有尾随/(GH #432) 时更正了某些行为
- 修复了重命名/取消链接因打开子句柄而失败的问题
- 其他 bug 修复和改进

<br/>

## <a name="build-14366"></a>生成14366
有关生成14366的常规 Windows 信息, 请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。 <br/>

### <a name="fixed"></a>固定
- 通过符号链接在文件创建中修复
-   添加了适用于 Python 的 listxattr (GH 385)
-   其他 bug 修复和改进

### <a name="syscall-support"></a>Syscall 支持
-   下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>生成14361
有关生成14361的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14361)。 <br/>

### <a name="fixed"></a>固定
- 在 Windows 上的 Ubuntu 上运行 Bash 时, DrvFs 现在区分大小写。
  - 用户可以为 .txt 和 CASE。/Mnt/c 驱动器上的 TXT
  - Windows 上的 Bash 中仅支持区分大小写。 在 Bash NTFS 外, 会正确报告文件, 但可能会发生意外行为, 与 Windows 中的文件交互。
  - 每个卷的根目录 (即/mnt/c) 不区分大小写
  - 可在[此处](https://support.microsoft.com/en-us/kb/100625)找到有关如何处理 Windows 中的这些文件的详细信息。
- 大大增强了 pty/tty 支持。  现在支持 TMUX 等应用程序 (GH #40)
- 修复了不总是创建用户帐户的安装问题
- 优化的命令行 arg 结构, 允许非常长的参数列表。 (GH #153)
- 现可从 DrvFs 删除和 chmod read_only 文件
- 修复了终端在断开连接时挂起的某些实例 (GH #43)
- chmod 和 chown 现在可在 tty 设备上工作
- 允许连接到0.0.0.0 和:: 作为 localhost (GH #388)
- Sendmsg/recvmsg 现在处理 > 1 (partial GH #376) 的 IO 矢量长度
- 用户现在可以选择退出自动生成的 hosts 文件 (GH #398)
- 在安装期间自动将 Linux 区域设置与 NT 区域设置匹配 (GH #11)
- 添加了/proc/sys/vm/swappiness 文件 (GH #306)
- 跟踪来现已正确退出
- 允许通过/proc/self/fd 重新打开管道 (GH #222)
- 隐藏%LOCALAPPDATA%\lxss 中的目录 DrvFs (GH #270)
- 更好地处理 bash ~。  现在支持类似于 "bash ~-c ls" 的命令 (GH #467)
- 插座现在会通知 epoll 读取在关闭期间可用 (GH #271)
- lxrun/uninstall 更好地删除文件和文件夹
- 更正的 ps-f (GH #246)
- 改善了对 x11 应用的支持, 如 xEmacs (GH #481)
- 已更新初始线程堆栈大小以匹配默认 Ubuntu 设置, 并正确报告 get_rlimit syscall 的大小 (GH #172, #258)
- 改善了 pico 进程映像名称 (例如, 审核) 的报告
- 为 df 命令实现了/proc/mountinfo
- 修复了子名称的符号链接错误代码。 和。
- 其他改进 bug 修复和改进

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>生成14352
有关生成14352的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14352)。<br/>


### <a name="fixed"></a>固定
- 修复了找不到正确下载/创建大型文件的问题。  这应取消阻止 npm 和其他方案 (GH #3, GH #313)
- 删除了套接字挂起的一些实例
- 更正了一些 ptrace 错误
- 修复了 WSL 的问题, 允许文件名超过255个字符
- 改进了对非英语字符的支持
- 添加当前 Windows 时区数据并将其设置为默认值
- 每个装入点的唯一设备 id (jre fix – GH #49)
- 更正包含 "." 的路径的问题 和 "..."
- 添加了 Fifo 支持 (GH #71)
- 已更新 resolv.conf 格式, 以匹配本地 Ubuntu 格式
- 某些 procfs 清理
- 为管理员控制台启用了 ping (GH #18)

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>生成14342
有关[Windows 博客](https://aka.ms/wip14342)上版本14342的常规 windows 信息。 <br/>

有关 VolFs 和 DriveFs 的信息, 请参阅[WSL 博客](https://blogs.msdn.microsoft.com/wsl)。 <br/>

### <a name="fixed"></a>固定
- 修复了 Windows 用户在用户名中包含 Unicode 字符时的安装问题
- 默认情况下, 在首次运行时, 默认情况下提供常见问题中的 apt-get update udev 解决方法
- 已启用 DriveFs (/mnt/<drive>) 目录中的符号链接
- 符号链接在 DriveFs 和 VolFs 之间工作
- 解决了顶层路径分析问题: ls.//现在将按预期方式工作
- npm 安装在 DriveFs 上并且-g 选项现在正在工作
- 修复了阻止 PHP 服务器启动的问题
- 更新了默认环境值, 例如 $PATH 以便更接近本地 Ubuntu
- 在 Windows 中添加了每周维护任务以更新 apt 包缓存
- 修复了 ELF 标头验证问题, WSL 现在支持所有 Melkor 选项
- Zsh shell 正常运行
- 现在支持预编译的中转二进制文件
- 在 Bash 首次运行时提示现在已正确本地化
- /proc/meminfo 现在返回正确的信息
- VFS 现在支持套接字
- /dev 现在装载为 tempfs
- 现在支持 Fifo
- 多核系统现在在/proc/cpuinfo 中显示正确
- 首次运行时下载的其他改进和错误消息
- Syscall 改进和 bug 修复。 下面支持的 syscall 列表。
- 其他 bug 修复和改进

### <a name="known-issues"></a>已知问题
- 不解析 "..." 在某些情况下, 在 DriveFs 上正确

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新的或增强的 syscall 的列表。 此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

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

## <a name="build-14332"></a>生成14332

有关生成14332的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14332)。 <br/>


### <a name="fixed"></a>固定
- 更好的 resolv.conf 生成, 包括优先级 DNS 条目
- 在/mnt 和非/mnt 驱动器之间移动文件和目录时出现的问题
- 现在可以通过符号链接创建 Tar 文件。
- 创建实例时添加了默认的/run/lock 目录
- 更新/dev/null 以返回正确的 stat 信息
- 首次运行期间下载时出现的其他错误
- Syscall 改进和 bug 修复。 下面支持的 syscall 列表。
- 其他改进 bug 修复和改进

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的新 syscall。 此列表中的 syscall 至少在一种方案中受支持, 但目前不支持所有参数。

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>生成14328

有关生成14332的常规 Windows 信息, 请访问[Windows 博客](https://aka.ms/wip14328)。 <br/>


### <a name="new-features"></a>新功能
* 现在支持 Linux 用户。  在 Windows 上的 Ubuntu 上安装 Bash 将提示创建 Linux 用户。  有关详细信息, 请访问 https://aka.ms/wslusers
* 现在, 主机名设置为 Windows 计算机名称, 不能再@localhost
* 有关生成14328的详细信息, 请访问: https://aka.ms/wip14328

### <a name="fixed"></a>固定
* 非/mnt/<drive>文件的符号改进
    * npm 安装现可正常运行
    * 现在使用[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)的说明可安装 jdk/jre。
    * 已知问题: 符号链接不适用于 Windows 安装。  功能将在以后的版本中提供
* 顶部和 htop 现在显示
* 某些安装失败的其他错误消息
* Syscall 改进和 bug 修复。  下面支持的 syscall 列表。
* 其他改进 bug 修复和改进

### <a name="syscall-support"></a>Syscall 支持
下面是在 WSL 中具有一些实现的 syscall 的列表。  此列表上的 syscall 在至少一个方案中受支持, 但目前不支持所有参数。

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
