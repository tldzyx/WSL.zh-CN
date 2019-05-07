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
# <a name="release-notes-for-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的发行说明

## <a name="build-18890"></a>生成 18890
有关常规 Windows 上生成 18890 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/05/01/announcing-windows-10-insider-preview-build-18890/)。

### <a name="wsl"></a>WSL
* 非阻塞套接字泄漏 [GH 2913]
* 终端的 EOF 输入可以阻止后续读取 [GH 3421]
* 更新 resolv.conf 标头来指代 wsl.conf [所述 GH 3928]
* 死锁中 epoll 删除代码 [GH 3922]
* 处理参数-导入和 – 导出 [GH 3932] 中的空格
* 扩展 mmap 处理的文件无法正常工作 [GH 3939]
* 修复问题的 ARM64 \\wsl$ 访问不能正常工作
* 添加 wsl.exe 更好的默认图标

## <a name="build-18342"></a>生成 18342
有关常规 Windows 上生成 18342 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/20/announcing-windows-10-insider-preview-build-18342/)。

### <a name="wsl"></a>WSL
* 我们已添加了用户从 Windows 访问 WSL 发行版中的 Linux 文件的能力。 可以通过命令行中，以及 Windows 应用，如文件资源管理器，VSCode 访问这些文件，等可以使用这些文件进行交互。 通过导航到访问的文件\\ \\wsl$\\< distro_name >，或查看运行的分布的方法是导航到列表\\ \\wsl$
* 添加更多的 CPU 信息标记和修复 Cpus_allowed [列表 （_l)] 值 [GH 2234]
* 支持从非领导线程 [GH 3800] exec
* 配置更新失败视为非致命性 [GH 3785]
* 更新 binfmt 能够正确处理偏移量 [GH 3768]
* 为计划 9 [GH 3854] 启用映射网络驱动器
* 支持 Windows-> Linux 和 Linux-> Windows 路径转换为绑定挂载
* 在打开的文件上创建映射的只读的部分，只读的

## <a name="build-18334"></a>生成 18334
有关常规 Windows 上生成 18334 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2019/02/08/announcing-windows-10-insider-preview-build-18334/)。

### <a name="wsl"></a>WSL
* 重新设计 Windows 时区映射到 Linux 时区 [GH 3747] 的方式
* 修复内存泄漏，并添加新的字符串转换函数 [GH 3746]
* 在无线程 threadgroup SIGCONT 是一个无操作 [GH 3741] 
* 正确显示在 /proc/self/fd 套接字和 epoll 文件描述符

## <a name="build-18305"></a>生成 18305
有关常规 Windows 上生成 18305 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/12/19/announcing-windows-10-insider-preview-build-18305/)。

### <a name="wsl"></a>WSL
* pthreads 失去对文件访问权限，当主线程退出 [GH 3589]
* TIOCSCTTY 应忽略"force"参数，除非必需，否则 [GH 3652]
* wsl.exe 命令行改进和添加导入/导出功能。
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

## <a name="build-18277"></a>生成 18277
有关常规 Windows 上生成 18277 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/11/07/announcing-windows-10-insider-preview-build-18277/)。

### <a name="wsl"></a>WSL
* 修复在生成 18272 [GH 3645] 中引入的"不支持此类接口"错误
* 忽略 umount syscall [GH 3605] MNT_FORCE 标志
* 若要使用官方 CreatePseudoConsole API 的交换机 WSL 互操作
* FUTEX_WAIT 重新启动时维护任何超时值

## <a name="build-18272"></a>生成 18272
有关常规 Windows 上生成 18272 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/31/announcing-windows-10-insider-preview-build-18272/)。

### <a name="wsl"></a>WSL
* **警告：** 使 WSL 无法运行此生成时出现问题。 尝试启动你的分发时您将看到"不支持此类接口"错误。 此问题已修复，并且将在下一步一周的快速深入了解生成。 如果已安装此您可以回滚到以前的 Windows 内部版本使用"转到返回到以前版本的 Windows 10"在设置生成-> 更新和安全-> 恢复。

## <a name="build-18267"></a>生成 18267
有关常规 Windows 上生成 18267 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/24/announcing-windows-10-insider-preview-build-18267/)。

### <a name="wsl"></a>WSL
* 解决的问题，其中僵停进程可能会不 reaped 和无限期地保持。
* 如果错误消息超过最大长度 [GH 3592] WslRegisterDistribution 挂起
* 允许 fsync DrvFs [GH 3556] 上的只读文件成功
* 确保创建符号链接 [GH 3584] 内的之前存在 /bin 和 /sbin 目录
* 添加 WSL 实例的实例终止超时机制。 超时时间当前设置为 15 秒，这意味着该实例将终止 15 秒的最新的 WSL 进程退出后。 若要立即终止分发，请使用：
```
wslconfig.exe /terminate <DistributionName>
```

## <a name="build-17763-1809"></a>生成 17763 (1809)
有关常规 Windows 上生成 17763 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/02/how-to-get-the-windows-10-october-2018-update/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 权限检查太严格的更改相同的线程优先级 [GH 1838]
* 确保公平的中断时间使用启动时若要避免返回负数值的 clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* 在 WSL binfmt 解释器 [GH 3424] 中的句柄符号链接
* 更好地处理 threadgroup 领导文件描述符清理。
* 切换 WSL 使用而不是 KeQueryPerformanceCounter KeQueryInterruptTimePrecise 以避免溢出 [GH 3252]
* Ptrace 连接可能会返回的值不正确导致从系统调用 [GH 1731]
* 修复多个 AF_UNIX 相关问题 [GH 3371]
* 解决问题可能导致 WSL 互操作，如果当前工作目录为小于 5 个字符长 [GH 3379] 失败
* 避免一个失败的环回连接到不存在的端口 [GH 3286] 的第二个延迟
* 添加 /proc/sys/fs/file-max 存根 （stub） 文件 [GH 2893]
* 更准确的 IPV6 范围信息。
* PR_SET_PTRACER 支持 [GH 3053]
* 通过管道传递无意中清除边缘触发 epoll 事件 [GH 3276] 的文件系统
* Win32 可执行文件启动通过 NTFS 符号链接不遵循符号链接名称 [GH 2909]
* 改进了僵停的支持 [GH 1353]
* 添加用于控制 Windows 互操作行为 [GH 1493] wsl.conf 条目
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修复 getsockname 不总是返回 UNIX 套接字系列类型 [GH 1774]
* 添加对 TIOCSTI [GH 1863] 的支持
* 非阻塞套接字连接的过程中应返回 EAGAIN 的写入尝试 [GH 2846]
* 在已装载的 Vhd [GH 3246，3291] 上支持互操作
* 修复权限检查在根文件夹 [GH 3304] 上的问题
* TTY 键盘 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支持。
* Windows UI 应用程序应执行，即使在后台启动。
* 添加 wsl-u 或--用户选项 [GH 1203]
* 启用快速启动时，解决 WSL 启动问题 [GH 2576]
* Unix 套接字需要保留已断开连接的对等凭据 [GH 3183]
* 非阻塞 Unix 套接字失败，而无限期地 EAGAIN [GH 3191]
* 用例 = off 是新的默认 drvfs 装载类型 [GH 2937，3212，3328]
    * 请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)有关详细信息。
* 添加 wslconfig/终止停止正在运行的分发版。
* 修复 WSL shell 上下文菜单项未正确处理包含空格的路径的问题。
* 公开每个目录区分大小写为扩展属性
* ARM64：模拟缓存维护操作。 解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。
* DrvFs： 只能恢复原义私有范围相对应的字符为转义字符。
* 在 ELF 分析器解释器长度验证 [GH 3154] 修复关闭--一个错误
* 在过去的时间 WSL 绝对计时器不会激发 [GH 3091]
* 确保新的父目录中这种情况下列出创建重新分析点。
* 以原子方式在 DrvFs 创建区分大小写的目录。
* 修复了其他问题，多线程的操作可能返回 ENOENT，即使该文件存在。 [GH 2712]
* 固定的 WSL 启用 UMCI 后启动失败。 [GH 3020]
* 添加用于启动 WSL [GH 437，603、 1836年] 的资源管理器上下文菜单。 若要使用，请按住 shift 并在资源管理器窗口中右键单击。
* 修复 Unix 套接字非阻塞行为 [GH 2822，3100]
* 修复 GH 2026 中报告挂起 NETLINK 命令。
* 添加对装入传播标志 [GH 2911] 的支持。
* 截断不导致 inotify 事件 [GH 2978] 修复问题。
* 添加了--exec wsl.exe 调用单一的二进制文件而无需 shell 的选项。
* 添加了--wsl.exe 以选择特定的发行版的分发选项。
* 对 dmesg 的有限的支持。 现在，应用程序可以将记录到 dmesg。 WSL 驱动程序记录到 dmesg 有限的信息。 在将来，这可以扩展来执行其他来自驱动程序的信息/诊断。
    * 注意： 当前支持通过 dmesg`/dev/kmsg`设备接口。 `syslog` 尚不支持 syscall 接口。 和，因此，某些`dmesg`命令行选项，例如`-S`，`-C`不起作用。
* 更改默认 gid 和模式的串行设备以匹配本机 [GH 3042]
* DrvFs 现在支持扩展的属性。
    * 注意：DrvFs 上的扩展属性名称具有一些限制。 某些字符 (如 /、: 和\*) 不允许，并且扩展属性名称不区分大小写上 DrvFs

## <a name="build-18252-skip-ahead"></a>生成 18252 （提前跳过）
有关常规 Windows 上生成 18252 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/10/03/announcing-windows-10-insider-preview-build-18252/)。

### <a name="wsl"></a>WSL
* 移动 init 和 bsdtar 二进制文件，带 lxssmanager dll 和到单独的工具文件夹
* 修复周围使用 CLONE_FILES 时关闭文件描述符的争用
* 转换 DrvFs 路径时处理 /proc/pid/mountinfo 中的可选字段
* 允许 DrvFs mknod 也不会对 S_IFREG 的元数据支持
* DrvFs 上创建 Readonly 文件应具有设置 [GH 3411] 的 readonly 属性
* 添加 /sbin/mount.drvfs 帮助器来处理 DrvFs 装载
* 使用中 DrvFs POSIX 重命名。
* 允许对卷不包括卷 GUID 路径翻译。

## <a name="build-17738-fast"></a>生成 17738 (Fast)
有关常规 Windows 上生成 17738 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/08/14/announcing-windows-10-insider-preview-build-17738/)。

### <a name="wsl"></a>WSL
* Setpriority syscall 权限检查太严格的更改相同的线程优先级 [GH 1838]
* 确保公平的中断时间使用启动时若要避免返回负数值的 clock_gettime(CLOCK_BOOTTIME) [GH 3434]
* 在 WSL binfmt 解释器 [GH 3424] 中的句柄符号链接
* 更好地处理 threadgroup 领导文件描述符清理。

## <a name="build-17728-fast"></a>生成 17728 (Fast)
有关常规 Windows 上生成 17728 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/31/announcing-windows-10-insider-preview-build-17728/)。

### <a name="wsl"></a>WSL
* 切换 WSL 使用而不是 KeQueryPerformanceCounter KeQueryInterruptTimePrecise 以避免溢出 [GH 3252]
* Ptrace 连接可能会返回的值不正确导致从系统调用 [GH 1731]
* 修复 AF_UNIX 的大量相关问题 [GH 3371]
* 解决问题可能导致 WSL 互操作，如果当前工作目录为小于 5 个字符长 [GH 3379] 失败

## <a name="build-18204-skip-ahead"></a>生成 18204 （提前跳过）
有关常规 Windows 上生成 18204 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 通过管道将文件系统 inadvertenly 清除边缘触发 epoll 事件 [GH 3276]
* Win32 可执行文件启动通过 NTFS 符号链接不遵循符号链接名称 [GH 2909]

## <a name="build-17723-fast"></a>生成 17723 (Fast)
有关常规 Windows 上生成 17723 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/25/announcing-windows-10-insider-preview-build-17723-and-build-18204/)。

### <a name="wsl"></a>WSL
* 避免一个失败的环回连接到不存在的端口 [GH 3286] 的第二个延迟
* 添加 /proc/sys/fs/file-max 存根 （stub） 文件 [GH 2893]
* 更准确的 IPV6 范围信息。
* PR_SET_PTRACER 支持 [GH 3053]
* 通过管道将文件系统 inadvertenly 清除边缘触发 epoll 事件 [GH 3276]
* Win32 可执行文件启动通过 NTFS 符号链接不遵循符号链接名称 [GH 2909]

## <a name="build-17713"></a>生成 17713
有关常规 Windows 上生成 17713 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/07/11/announcing-windows-10-insider-preview-build-17713/)。

### <a name="wsl"></a>WSL
* 改进了僵停的支持 [GH 1353]
* 添加用于控制 Windows 互操作行为 [GH 1493] wsl.conf 条目
  ```
    [interop]

    enabled=false # enable launch of Windows binaries; default is true

    appendWindowsPath=false # append Windows path to $PATH variable; default is true
  ```
* 修复 getsockname 不总是返回 UNIX 套接字系列类型 [GH 1774]
* 添加对 TIOCSTI [GH 1863] 的支持
* 非阻塞套接字连接的过程中应返回 EAGAIN 的写入尝试 [GH 2846]
* 在已装载的 Vhd [GH 3246，3291] 上支持互操作
* 修复权限检查在根文件夹 [GH 3304] 上的问题
* TTY 键盘 ioctl KDGKBTYPE、 KDGKBMODE 和 KDSKBMODE 的有限的支持。
* Windows UI 应用程序应执行，即使在后台启动。

## <a name="build-17704"></a>生成 17704
有关常规 Windows 上生成 17704 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/27/announcing-windows-10-insider-preview-build-17704/)。

### <a name="wsl"></a>WSL
* 添加 wsl-u 或--用户选项 [GH 1203]
* 启用快速启动时，解决 WSL 启动问题 [GH 2576]
* Unix 套接字需要保留已断开连接的对等凭据 [GH 3183]
* 非阻塞 Unix 套接字失败，而无限期地 EAGAIN [GH 3191]
* 用例 = off 是新的默认 drvfs 装载类型 [GH 2937，3212，3328]
    * 请参阅[博客](https://blogs.msdn.microsoft.com/commandline/2018/06/14/improved-per-directory-case-sensitivity-support-in-wsl/)有关详细信息。
* 添加 wslconfig/终止停止正在运行的分发版。

## <a name="build-17692"></a>版本 17692
有关常规 Windows 上生成 17692 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/14/announcing-windows-10-insider-preview-build-17692)。

### <a name="wsl"></a>WSL
* 修复 WSL shell 上下文菜单项未正确处理包含空格的路径的问题。
* 公开每个目录区分大小写为扩展属性
* ARM64：模拟缓存维护操作。 解决[dotnet 问题](https://github.com/dotnet/core/issues/1561)。
* DrvFs： 只能恢复原义私有范围相对应的字符为转义字符。

## <a name="build-17686"></a>版本 17686
有关常规 Windows 上生成 17686 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/06/06/announcing-windows-10-insider-preview-build-17686)。

### <a name="wsl"></a>WSL
* 在 ELF 分析器解释器长度验证 [GH 3154] 修复关闭--一个错误
* 在过去的时间 WSL 绝对计时器不会激发 [GH 3091]
* 确保新的父目录中这种情况下列出创建重新分析点。
* 以原子方式在 DrvFs 创建区分大小写的目录。

## <a name="build-17677"></a>生成 17677
有关常规 Windows 上生成 17677 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/24/announcing-windows-10-insider-preview-build-17677/)。

### <a name="wsl"></a>WSL
* 修复了其他问题，多线程的操作可能返回 ENOENT，即使该文件存在。 [GH 2712]
* 固定的 WSL 启用 UMCI 后启动失败。 [GH 3020]

## <a name="build-17666"></a>生成 17666
有关常规 Windows 上生成 17666 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/05/09/announcing-windows-10-insider-preview-build-17666/)。

### <a name="wsl"></a>WSL
#### <a name="warning-there-is-an-issue-preventing-wsl-from-running-on-some-amd-chipsets-gh-3134-a-fix-is-ready-and-making-its-way-to-the-insider-build-branch"></a>警告：出现了问题导致无法 WSL 一些 AMD 芯片集 [GH 3134] 上运行。 解决方法是准备就绪，并可使发送给预览体验内部版本分支。
* 添加用于启动 WSL [GH 437，603、 1836年] 的资源管理器上下文菜单。 若要使用按住 shift 键并右键单击资源管理器窗口中。
* 修复 unix 套接字非阻塞行为 [GH 2822，3100]
* 修复 GH 2026 中报告挂起 NETLINK 命令。
* 添加对装入传播标志 [GH 2911] 的支持。
* 截断不导致 inotify 事件 [GH 2978] 修复问题。
* 添加了--exec wsl.exe 调用单一的二进制文件而无需 shell 的选项。
* 添加了--wsl.exe 以选择特定的发行版的分发选项。

## <a name="build-17655-skip-ahead"></a>生成 17655 （提前跳过）
有关常规 Windows 上生成 17655 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/25/announcing-windows-10-insider-preview-build-17655-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 对 dmesg 的有限的支持。 现在，应用程序可以将记录到 dmesg。 WSL 驱动程序记录到 dmesg 有限的信息。 在将来，这可以扩展来执行其他来自驱动程序的信息/诊断。
    * 注意： 当前支持通过 dmesg`/dev/kmsg`设备接口。 `syslog` 尚不支持 sycall 接口。 和，因此，某些`dmesg`命令行选项，例如`-S`，`-C`不起作用。
* 修复了问题，多线程的操作可能返回 ENOENT，即使该文件存在。 [GH 2712]

## <a name="build-17639-skip-ahead"></a>生成 17639 （提前跳过）
有关常规 Windows 上生成 17639 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/04/04/announcing-windows-10-insider-preview-build-17639-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 更改默认 gid 和模式的串行设备以匹配本机 [GH 3042]
* DrvFs 现在支持扩展的属性。
    * 注意：DrvFs 上的扩展属性名称具有一些限制。 具体而言，某些字符 (如 /、: 和\*) 不允许，并且扩展属性名称不区分大小写上 DrvFs

## <a name="build-17133-fast"></a>生成 17133 (Fast)
有关常规 Windows 上生成 17133 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/27/announcing-windows-10-insider-preview-build-17133-for-fast/)。

### <a name="wsl"></a>WSL
* 在 WSL 中挂起的修复。 [GH 3039，3034]

## <a name="build-17128-fast"></a>生成 17128 (Fast)
有关常规 Windows 上生成 17128 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/23/announcing-windows-10-insider-preview-build-17128-for-fast/)。

### <a name="wsl"></a>WSL
* 无

## <a name="build-17627-skip-ahead"></a>生成 17627 （提前跳过）
有关常规 Windows 上生成 17627 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/21/announcing-windows-10-insider-preview-build-17627-for-skip-ahead/)。

### <a name="wsl"></a>WSL
* 添加对 futex pi 注意操作的支持。 [GH 1006]
    * 请注意，优先级目前不受支持的 WSL 功能以便存在一些限制，但应解除对标准使用情况。
* WSL 进程的 Windows 防火墙支持。 [GH 1852]
    * 例如，若要允许 WSL python 处理任何端口上侦听，请使用提升的 Windows cmd: ```netsh.exe advfirewall firewall add rule name=wsl_python dir=in action=allow program="C:\users\<username>\appdata\local\packages\canonicalgrouplimited.ubuntuonwindows_79rhkp1fndgsc\localstate\rootfs\usr\bin\python2.7" enable=yes```
    * 有关如何添加防火墙规则的其他详细信息，请参阅[链接](https://support.microsoft.com/en-us/help/947709/how-to-use-the-netsh-advfirewall-firewall-context-instead-of-the-netsh)
* 使用 wsl.exe 时遵从用户的默认外壳。 [GH 2372]
* 报告为以太网的所有网络接口。 [GH 2996]
* 更好地处理已损坏的 /etc/passwd 文件。 [GH 3001]

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17618-skip-ahead"></a>生成 17618 （提前跳过）
有关常规 Windows 上生成 17618 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/03/07/announcing-windows-10-insider-preview-build-17618-skip-ahead/)。

### <a name="wsl"></a>WSL
* 引入 pseudoconsole NT 互操作的功能 [GH 988，1366，1433年、 1542年、 2370年、 2406年]。
* 已弃用旧安装机制 (lxrun.exe)。 安装发行版的受支持的机制是通过 Microsoft Store。

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17110"></a>版本 17110
有关常规 Windows 上生成 17110 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/27/announcing-windows-10-insider-preview-build-17110-fast/)。

### <a name="wsl"></a>WSL
* 允许 /init 从 Windows [GH 2928] 终止。
* DrvFs 现在默认情况下使用每个目录的区分大小写 (等效于"用例为 dir"装载选项)。
    * 使用"用例 = 强制"（旧行为） 需要设置注册表项。 运行以下命令以启用"用例 = 强制"如果需要使用它： reg 添加 HKLM\SYSTEM\CurrentControlSet\Services\lxss /v DrvFsAllowForceCaseSensitivity /t REG_DWORD /d 1
    * 如果必须使用 WSL 较旧版本的 Windows 需要区分大小写的中创建的现有目录，请使用 fsutil.exe 以便将它们标记为区分大小写： fsutil.exe 文件 setcasesensitiveinfo<path>启用
* Uname syscall 从返回的字符串以 NULL 结尾。

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17107"></a>生成 17107
有关常规 Windows 上生成 17107 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/23/announcing-windows-10-insider-preview-build-17107-fast-ring/)。

### <a name="wsl"></a>WSL
* 主 pty 终结点 [GH 2552] 上支持 TCSETSF 和 TCSETSW。
* 启动同时进行互操作的进程可能会导致 EINVAL [GH 2813]。
* 修复 PTRACE_ATTACH /proc/pid/status 中显示正确的跟踪状态。
* 修复争用生存期较短的进程，克隆 CLEARTID 和 SETTID 标志无法退出而不清除 TID 地址。
* 从预 17093 生成移动时升级 Linux 文件系统目录时，将显示一条消息。 17093 文件系统更改的更多详细信息，请参阅发行说明[17093](https://github.com/MicrosoftDocs/WSL/blob/live/WSL/release-notes.md#build-17093)。

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17101"></a>生成 17101
有关常规 Windows 上生成 17101 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/14/announcing-windows-10-insider-preview-build-17101-fast-build-17604-skip-ahead/)。

### <a name="wsl"></a>WSL
* 对 signalfd 的支持。 [GH 129]
* 支持文件名称包含非法 NTFS 字符编码为专用的 Unicode 字符。 [GH 1514]
* 不支持写时，自动装入将回退到只读的。 [GH 2603]
* 允许粘贴 Unicode 代理项对 （如表情符号字符为单位）。 [GH 2765]
* /Proc 和 /sys 中的伪文件应返回读取和写入就绪 select、 轮询、 epoll，et 都 [GH 2838]
* 修复可能导致服务注册表被篡改或损坏时进入无限循环的问题。
* 修复 netlink 消息要替换的 iproute2 更新 (上游 4.14) 版本。

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17093"></a>生成 17093
有关常规 Windows 上生成 17093 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/02/07/announcing-windows-10-insider-preview-build-17093-pc/)。

#### <a name="important"></a>重要提示：
时从 WSL 开始第一次后升级到此版本，它需要执行一些升级 Linux 文件系统目录的工作。 这可能需要几分钟时间，因此 WSL 可能看起来启动慢。 安装从应用商店的每个分布区后，仅应发生这种情况。
* 改进了在 DrvFs 区分大小写支持。
    * DrvFs 现在支持每个目录的区分大小写。 这是新标志可设置目录以指示在这些目录中的所有操作应被都视为区分大小写，这样即使 Windows 应用程序就可正确打开仅大小写不同的文件。
    * DrvFs 具有新的装入选项控制在每个目录的基础上区分大小写
        * 用例 = 强制： 所有目录将被都视为区分大小写 （除外驱动器根目录中）。 使用 WSL 创建的新目录将标记为区分大小写。 这是除标记区分大小写的新目录的旧行为。
        * 用例为 dir： 仅使用每个目录的区分大小写标志的目录将被视为区分大小写;其他目录是不区分大小写。 使用 WSL 创建的新目录将标记为区分大小写。
        * 用例 = 关闭： 仅使用每个目录的区分大小写标志的目录将被视为区分大小写;其他目录是不区分大小写。 使用 WSL 创建的新目录将标记为不区分大小写。
    * 注意： 在以前版本中创建 WSL 目录没有此标志设置，因此将不被视为区分大小写如果使用"用例为 dir"选项。 在现有目录上设置此标志的方法即将推出。
    * 装载与这些选项的示例 （对于现有的驱动器，您必须首先卸载之前可以使用不同选项装载）： sudo mount-t drvfs c: mnt/c o 用例为 dir
    * 现在，本例 = 强制仍是默认选项。 这将更改为用例在将来为 dir。
* 你现在可以使用正斜杠 Windows 路径中时装载 DrvFs，例如： sudo 装载-t drvfs //server/share /mnt/share
* WSL 现将在实例启动 [GH 2636] 处理 /etc/fstab 文件。
    * 这是在自动装载 DrvFs 驱动器; 之前任何已由 fstab 已装载的驱动器，将不重新装入自动，从而允许您更改特定驱动器的装入点。
    * 此行为可以关闭使用 wsl.conf。
* /Proc 中的装入、 mountinfo 和 mountstats 文件会正确地转义特殊字符，如反斜杠和空格 [GH 2799]
* 特殊文件使用创建 DrvFs 如 WSL 符号链接，或 fifos 和套接字启用元数据后，现在可以复制和从 Windows 移动。

#### <a name="wsl-is-more-configurable-with-wslconf"></a>WSL 是更多可配置为 wsl.conf
我们添加了一个方法，以便自动在每次启动子系统将应用的 WSL 中配置的特定功能。 这包括自动装载选项和网络配置。 在我们的博客文章中了解其详细信息： https://aka.ms/wslconf

#### <a name="afunix-allows-socket-connections-between-linux-processes-on-wsl-and-windows-native-processes"></a>AF_UNIX 允许 Linux 进程在 WSL 和 Windows 本机进程之间的套接字连接
通过 Unix 套接字，现在相互 WSL 和 Windows 应用程序可以通信。 想象你想要在 Windows 中运行服务并使其可供 Windows 和 WSL 应用。 现在，这是可能使用 Unix 套接字。 读取在我们的博客文章 https://aka.ms/afunixinterop

### <a name="wsl"></a>WSL
* 支持使用 MAP_NORESERVE [GH 121，2784年] mmap()
* 支持 CLONE_PTRACE 和 CLONE_UNTRACED [GH 121，2781年]
* 在克隆 [GH 121，2781年] 中的句柄非 SIGCHLD 终止信号
* 存根 （stub) /proc/sys/fs/inotify/max_user_instances 和 /proc/sys/fs/inotify/max_user_watches [GH 1705]
* 加载包含非零值的偏移量 [GH 1884] 的负载标头的 ELF 二进制文件时出错
* 加载图像时尾随页字节清零。
* 减少 execve 以无提示方式终止进程的情况下

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17083"></a>版本 17083
有关常规 Windows 上生成 17083 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/24/announcing-windows-10-insider-preview-build-17083-for-pc/)。

### <a name="wsl"></a>WSL
* 固定的 epoll [GH 2798，2801，2857年] 与相关的错误检查
* 固定的挂起时关闭 ASLR [GH 1185，2870年]
* 确保 mmap 操作出现原子 [GH 2732]

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17074"></a>生成 17074
有关常规 Windows 上生成 17074 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2018/01/11/announcing-windows-10-insider-preview-build-17074-pc/)。

### <a name="wsl"></a>WSL
* 固定的存储格式的 DrvFs 元数据 [GH 2777] </br>
**重要说明：** 此生成不正确或根本不会显示之前创建的 DrvFs 元数据。 若要修复受影响的文件，请使用 chmod 和 chown 重新应用元数据。
* 多个信号和可重新启动 syscall 已修复的问题。

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17063"></a>生成 17063
有关常规 Windows 上生成 17063 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/12/19/announcing-windows-10-insider-preview-build-17063-pc/)。

### <a name="wsl"></a>WSL
* DrvFs 支持 Linux 的其他元数据。 这允许设置所有者和使用 chmod/chown 和特殊文件，如 fifos、 unix 套接字和设备文件创建的文件模式。 这是默认情况下禁用现在由于它是仍处于实验阶段。
**注意：** 我们修复了 bug 中使用 DrvFs 的元数据格式。 而元数据适用于此生成的试验，将来的内部版本将不正确地读取元数据创建此生成的。  可能需要手动更新已修改的文件的所有者和使用自定义设备 ID 的设备将需要重新创建。

  若要启用，装入 DrvFs 使用元数据选项 （若要在现有安装上启用它，您必须首先卸载该映像）：

  ```bash
  mount -t drvfs C: /mnt/c -o metadata
  ```

  Linux 权限为附加元数据添加到该文件;它们不会影响 Windows 权限。  请记住，编辑文件使用 Windows 编辑器可能删除的元数据。 在这种情况下，该文件将恢复为其默认权限。

* 添加的装载到不包含元数据的控制文件 DrvFs 的选项。
  * uid： 用于所有文件的所有者的用户 ID。
  * gid： 用于所有文件的所有者的组 ID。
  * umask： 若要排除的所有文件和目录的权限的八进制掩码。
  * fmask： 权限以排除所有常规的文件的八进制掩码。
  * dmask： 权限以排除所有目录的八进制掩码。

  例如：
  ```
  mount -t drvfs C: /mnt/c -o uid=1000,gid=1000,umask=22,fmask=111
  ```

  将与指定的文件不包含元数据的默认权限的元数据选项。

* 引入了一个新的环境变量， `WSLENV`，可以配置环境变量如何在 WSL 和 Win32 之间流动。

  例如：

  ``` bash
  WSLENV=GOPATH/l:USERPROFILE/pu:DISPLAY
  ```

  `WSLENV` 是可以包含来自 Win32 的 WSL 进程或从 WSL 的 Win32 进程启动时的环境变量的分号分隔列表。  标志以指定如何对其进行转换后跟反斜杠结尾，每个变量可以作为后缀。
  * p:值是应翻译 WSL 路径和 Win32 路径之间的路径。
  * L:值为一系列路径。 在 WSL，它是一个冒号分隔的列表。 在 Win32 中，它是以分号分隔列表。
  * U:更改在调用来自 Win32 的 WSL 时只应包含值
  * w:更改在调用 Win32 从 WSL 时只应包含值

  可以设置`WSLENV`.bashrc 或你的用户自定义 Windows 环境中。

* drvfs 装载正确保留 tar 文件，从时间戳 cp-p (GH 1939)
* drvfs 符号链接报告正确的大小 (GH 2641)
* 读/写适用于非常大的 IO 大小 (GH 2653)
* waitpid 适用于进程组 Id (GH 2534)
* 显著的性能改进的 mmap 大型保留区域;改进了 ghc 性能 (GH 1671)
* READ_IMPLIES_EXEC; 的个性支持修复了最大值和 clisp (GH 1185)
* mprotect 支持 PROT_GROWSDOWN;修复了 clisp (GH 1128)
* 中的页错误修复过载模式;修复了 sbcl (GH 1128)
* 克隆支持更多的标志组合
* 支持 epoll 文件 （之前执行任何操作） 的选择/epoll。
* 通知未实现 syscall ptrace。
* 忽略接口时，将不会生成 resolv.conf 名称服务器 [GH 2694]
* 枚举与没有物理地址的网络接口。 [GH 2685]
* 其他 bug 修复和改进。

### <a name="linux-tools-available-to-developers-on-windows"></a>供开发人员在 Windows 上的 Linux 工具

* Windows 命令行工具链包含 bsdtar (tar) 和 curl 配合使用。
  读取[此博客](https://aka.ms/tarcurlwindows)若要了解有关新增的两个新工具的详细信息并查看它们如何调整 Windows 上的开发人员体验。

*   `AF_UNIX` 现已推出 Windows Insider SDK （17061 +）。
  读取[此博客](https://blogs.msdn.microsoft.com/commandline/2017/12/19/af_unix-comes-to-windows/)若要详细了解`AF_UNIX`和 Windows 上的开发人员可以使用它。

### <a name="console"></a>控制台
* 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。


## <a name="build-17046"></a>生成 17046

有关常规 Windows 上生成 17046 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/22/announcing-windows-10-insider-preview-build-17046-pc)。

### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 允许进程运行时没有活动的终端。 [GH 709，1007，1511年、 2252年、 2391，et al。]
- CLONE_VFORK 和 CLONE_VM 的更好的支持。 [GH 1878，2615年]
- 跳过网络操作的 WSL TDI 筛选器驱动程序。 [GH 1554]
- 当满足某些条件时，DrvFs 创建 NT 符号链接。 [GH 353，1475，2602年]
    - 链接目标必须是相对路径，不能跨越任何装入点或符号链接，并且必须存在。
    - 用户必须具有 SE_CREATE_SYMBOLIC_LINK_PRIVILEGE （这通常要求您启动 wsl.exe 提升），除非打开开发人员模式。
    - 在所有其他情况下，DrvFs 仍会 WSL 符号链接。
- 允许同时运行提升和非提升 WSL 实例。
- Support /proc/sys/kernel/yama/ptrace_scope
- 添加 wslpath 为 WSL <>-Windows 路径转换。 [GH 522，1243，1834年、 2327，et al。]
  ```
    wslpath usage:
      -a    force result to absolute path format
      -u    translate from a Windows path to a WSL path (default)
      -w    translate from a WSL path to a Windows path
      -m    translate from a WSL path to a Windows path, with ‘/’ instead of ‘\\’

      EX: wslpath ‘c:\users’
  ```
  #### <a name="console"></a>控制台
- 任何修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。


## <a name="build-17040"></a>生成 17040

有关常规 Windows 上生成 17040 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/16/announcing-windows-10-insider-preview-build-17040-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 无 17035 以来的修补程序。

#### <a name="console"></a>控制台
- 无 17035 以来的修补程序。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17035"></a>生成 17035

有关常规 Windows 上生成 17035 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/11/08/announcing-windows-10-insider-preview-build-17035-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 访问 DrvFs 上的文件无法与 EINVAL 偶尔也会失败。 [GH 2448]

#### <a name="console"></a>控制台
- 插入/删除 VT 模式中的行时，某些颜色丢失。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17025"></a>内部版本 17025

有关常规 Windows 内部版本 17025 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/25/announcing-windows-10-insider-preview-build-17025-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 启动新的前台进程组 [GH 1653，2510年] 中的初始进程。
- SIGHUP 交付修补程序 [GH 2496]。
- 如果未提供 [GH 2497]，生成默认虚拟桥的名称。
- 实现 /proc/sys/kernel/random/boot_id [GH 2518]。
- 修复了多互操作的 stdout/stderr 管道。
- 存根 syncfs 系统调用。

#### <a name="console"></a>控制台
- 修复输入的 VT 转换为第三方控制台 [GH 111]

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="build-17017"></a>生成 17017

有关常规 Windows 上生成 17017 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/10/13/announcing-windows-10-insider-preview-build-17017-pc)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 忽略空 ELF 程序标头 [GH 330]。
- 允许 LxssManager 创建非交互式用户的 WSL 实例 (ssh 和计划任务支持) [GH 777，1602年]。
- 支持 WSL-> Win32-> WSL （"开始"） 方案 [GH 1228]。
- 终止通过互操作 [GH 1614] 调用的控制台应用程序的有限的支持。
- Devpts [GH 1948] 的支持装载选项。
- 阻止子启动 [GH 2333] 的 Ptrace。
- EPOLLET 缺少某些事件 [GH 2462]。
- 为 PTRACE_GETSIGINFO 返回更多的数据。
- 使用 lseek Getdents 提供不正确的结果。
- 修复在已没有更多数据的管道上等待输入一些 Win32 互操作应用挂起。
- O_ASYNC 支持 tty/pty 文件。
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 没有控制台相关的此版本中的更改。

### <a name="ltp-results"></a>LTP 结果：
测试正在进行中。

## <a name="fall-creators-update"></a>秋季创意者更新

## <a name="build-16288"></a>生成 16288

有关常规 Windows 上生成 16288 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/09/12/announcing-windows-10-insider-preview-build-16288-pc-build-15250-mobile/#7pLWQbj23JisfzV5.97/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 正确初始化并报告 uid 和 gid，模式套接字文件描述符 [GH 2490]
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 没有控制台相关的此版本中的更改。

### <a name="ltp-results"></a>LTP 结果：
16273 以来未更改

## <a name="build-16278"></a>生成 16278

有关常规 Windows 上生成 162738 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/29/announcing-windows-10-insider-preview-build-16278-pc/#HMz6Xq7Su68WKi0t.97/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 显式取消的备份文件的部分映射的视图映射时关闭 LX MM 状态 [GH 2415]
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 没有控制台相关的此版本中的更改。

### <a name="ltp-results"></a>LTP 结果：
16273 以来未更改

## <a name="build-16275"></a>生成 16275

有关常规 Windows 上生成 162735 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/25/announcing-windows-10-insider-preview-build-16275-pc-build-15245-mobile/#8QkxWqQbY37yZslV.97/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 没有 WSL 相关的此版本中的更改。

#### <a name="console"></a>控制台
- 没有控制台相关的此版本中的更改。

### <a name="ltp-results"></a>LTP 结果：
16273 以来未更改

## <a name="build-16273"></a>生成 16273

有关常规 Windows 上生成 16273 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/23/announcing-windows-10-insider-preview-build-16273-pc/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 修复了 DrvFs 有时报告目录 [GH 2392] 的错误的文件类型
- 允许的 NETLINK_KOBJECT_UEVENT 套接字，若要取消阻止程序创建该使用 uevent [GH 1121，2293，2242年、 2295年、 2235，648、 637]
- 添加对非阻止连接的支持 [GH 903，1391，1584年、 1585年、 1829年、 2290年、 2314年]
- 实现 CLONE_FS 克隆系统调用标志 [GH 2242]
- 修复不处理选项卡或 NT 互操作 [GH 1625，2164年] 中正确的引号等事宜
- 解决拒绝访问错误时尝试重新启动 WSL 实例 [GH 651，2095年]
- 实现 futex FUTEX_REQUEUE 和 FUTEX_CMP_REQUEUE 操作 [GH 2242]
- 修复各种 SysFs 文件 [GH 2214] 的权限
- 在安装程序 [GH 2290] 期间修复 Haskell 堆栈挂起
- 实现 binfmt_misc 'C' O 和 P 标志 [GH 2103]
- 添加 /proc/sys/kernel /shmmax /shmmni & /threads-max [GH 1753]
- 添加对 ioprio_set 系统调用 [GH 498] 的部分支持
- 存根 SO_REUSEPORT 和添加支持 SO_PASSCRED netlink 套接字 [GH 69]
- 从 RegisterDistribuiton 返回不同的错误代码，如果当前正在分发安装或卸载。
- 允许通过 wslconfig.exe 部分安装 WSL 分发的注销
- 修复从 udp::msg_peek python 套接字测试挂起
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 没有控制台相关的此版本中的更改。

### <a name="ltp-results"></a>LTP 结果：
测试总数：1904<br/>
总跳过测试：209<br/>
故障总数：229<br/>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16273)<br/>

## <a name="build-16257"></a>版本 16257

有关常规 Windows 上生成 16257 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/08/02/announcing-windows-10-insider-preview-build-16257-pc-build-15237-mobile/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 实现 prlimit64 系统调用
- 添加对 ulimit-n (setrlimit RLIMIT_NOFILE) 的支持 [GH 1688]
- 存根 MSG_MORE 针对 TCP 套接字 [GH 2351]
- 修复无效 AT_EXECFN 辅助向量行为 [GH 2133]
- 修复控制台/tty 的复制/粘贴行为并添加更好地处理 [GH 2204，2131年] 已满缓冲区
- 有关设置用户 ID 和组-组 ID 程序 [GH 2031] 的辅助向量中设置 AT_SECURE
- 仿真终端主终结点不处理 TIOCPGRP [GH 1063]
- 修复 lseek 执行的操作以 rewind LxFs [GH 2310] 中的目录
- /dev/ptmx 锁定的时间之后的高使用率 [GH 1882]
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 修复水平行/下划线无处不在 [GH 2168]
- 修复处理订单更改使 NPM 难关闭 [GH 2170]
- 添加我们新的配色方案： https://blogs.msdn.microsoft.com/commandline/2017/08/02/updating-the-windows-console-colors/

### <a name="ltp-results"></a>LTP 结果：
16251 以来未更改

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`prlimit64`<br/>

### <a name="known-issues"></a>已知问题
#### <a name="github-issue-2392-windows-folders-not-recognized-by-wsl-httpsgithubcommicrosoftbashonwindowsissues2392"></a>[GitHub 问题 2392年:Windows 无法识别的 WSL 文件夹...](https://github.com/Microsoft/BashOnWindows/issues/2392)
在生成 16257，WSL 有问题，枚举通过 Windows 文件/文件夹时`/mnt/c/...`。
此问题已修复，并且应在释放预览体验成员版本官员在 2017 年 8 月 14 日开始的一周内。

<br/>

## <a name="build-16251"></a>生成 16251

有关常规 Windows 上生成 16251 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/26/announcing-windows-10-insider-preview-build-16251-pc-build-15235-mobile/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 删除 beta 标记从 WSL 可选组件，请参阅[博客文章](https://blogs.msdn.microsoft.com/commandline/2017/07/28/windows-subsystem-for-linux-out-of-beta/)有关详细信息。
- 保存设置 uid 和 gid exec [GH 962，1415、 2072年] 上的设置用户 ID 和组-组 ID 的二进制文件的正确初始化
- 添加了的对 ptrace PTRACE_O_TRACEEXIT [GH 555]
- 添加了对 ptrace PTRACE_GETFPREGS 和 PTRACE_GETREGSET 与 NT_FPREGSET [GH 555]
- 已修复的 ptrace 上停止忽略信号
- 其他改进和 bug 修复

#### <a name="console"></a>控制台
- 没有控制台相关的此版本中的更改。

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：768</br>
未通过的测试数：244</br>
已跳过的测试数：96</br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/16251)<br/>

</br>

## <a name="build-16241"></a>生成 16241

有关常规 Windows 上生成 16241 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/13/announcing-windows-10-insider-preview-build-16241-pc-build-15230-mobile/)。<br/>


### <a name="fixed"></a>固定
#### <a name="wsl"></a>WSL
- 没有 WSL 相关的此版本中的更改。

#### <a name="console"></a>控制台
- 修复错误的字符输出跨越行 dec，最初报告[此处](https://www.reddit.com/r/Windows10/comments/6in82t/i_believe_ive_found_the_most_obscure_bug_ever/)
- 修复了显示在代码页 65001 (utf8) 没有输出文本
- 不会传输到所选内容更改调色板的其他部分的一种颜色的 RGB 值所做的更改。 这将使控制台属性表更易于使用。
- Ctrl + S 似乎不正常工作
- 未加粗 /-维度完全不存在从 ANSI 转义码 [GH 2174]
- 控制台不会正确地支持 Vim 颜色主题 [GH 1706]
- 不能粘贴特定字符 [GH 2149]
- 重排调整大小与当内容在编辑/命令行 [GH ConEmu 1123] 时调整大小的 bash 窗口奇怪交互
- Ctrl-L 离开屏幕已更新 [GH 1978]
- 控制台呈现 bug 上 HDPI [GH 又回到了 1907] 显示 VT 时
- Japansese 字符看起来很奇怪的 Unicode 字符 U + 30FB [GH 2146]
- 其他改进和 bug 修复

</br>

## <a name="build-16237"></a>版本 16237

有关常规 Windows 上生成 16237 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/07/07/announcing-windows-10-insider-preview-build-16237-pc/)。<br/>


### <a name="fixed"></a>固定
- 中的文件而无需 EAs lxfs （根、 根，0000） 使用默认属性
- 添加了的对使用扩展的属性的分发
- 修复 getdents 和 getdents64 返回项的填充
- 修复 shmctl SHM_STAT 系统调用 [GH 2068] 的权限检查
- Tty [GH 2231] 的固定不正确的初始 epoll 状态
- 修复 DrvFs readdir 未返回所有条目 [GH 2077]
- 修复 LxFs readdir 文件时已取消链接 [GH 2077]
- 允许通过 procfs 重新打开取消链接的 drvfs 文件
- 添加全局注册表禁用 WSL 功能密钥替代 (互操作 / 驱动器装载)
- 适用于 DrvFs （和 LxFs） 解决"状态"中的不正确的块计数 [GH 1894]
- 其他改进和 bug 修复

</br>

## <a name="build-16232"></a>生成 16232

有关常规 Windows 上生成 16232 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/28/announcing-windows-10-insider-preview-build-16232-pc-build-15228-mobile/)。<br/>


### <a name="fixed"></a>固定
- 没有 WSL 相关的此版本中的更改。

</br>

## <a name="build-16226"></a>生成 16226

有关常规 Windows 上生成 16226 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/21/announcing-windows-10-insider-preview-build-16226-pc/)。<br/>


### <a name="fixed"></a>固定
- xattr 相关 syscall 支持 （getxattr、 setxattr、 listxattr、 removexattr）。
- security.capablity xattr 支持。
- 改进与特定的文件系统和筛选器，包括非 MS SMB 服务器的兼容性。 [GH #1952]
- 改进了对 OneDrive 的占位符、 GVFS 占位符和 Compact OS 支持压缩文件。
- 其他改进和 bug 修复

</br>

## <a name="build-16215"></a>生成 16215

有关常规 Windows 上生成 16215 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/06/08/announcing-windows-10-insider-preview-build-16215-pc-build-15222-mobile/)。<br/>


### <a name="fixed"></a>固定
- WSL 不再要求开发人员模式。
- 支持 drvfs 目录接合点。
- 处理卸载的 WSL 分发 appx 包。
- 更新 procfs 显示专用和共享的映射。
- 添加 wslconfig.exe 清理的部分安装或卸载分发版的功能。
- 针对 TCP 套接字 IP_MTU_DISCOVER 添加的支持。 [GH 1639，2115，2205年]
- 推断 AF_INADDR 的路由的协议家族。
- 串行设备改进 [GH 1929]。

</br>

## <a name="build-16199"></a>生成 16199

有关常规 Windows 上生成 16199 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/17/announcing-windows-10-insider-preview-build-16199-pc-build-15215-mobile/)。<br/>


### <a name="fixed"></a>固定
- 没有 WSL 相关的这些版本中的更改。

</br>

## <a name="build-16193"></a>生成 16193

有关常规 Windows 上生成 16193 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/05/11/announcing-windows-10-insider-preview-build-16193-pc-build-15213-mobile/)。<br/>


### <a name="fixed"></a>固定
- 发送 SIGCONT 和终止 [GH 1973] threadgroup 之间的争用条件
- 更改报表而不是 FILE_DEVICE_CONSOLE [GH 1840] FILE_DEVICE_NAMED_PIPE tty 和 pty 设备
- SSH IP_OPTIONS 修复
- 移动 DrvFs 装载到 init 守护程序 [GH 1862，1968，1767年、 1933年]
- 添加了的对在 DrvFs 遵循 NT 符号链接。

</br>

## <a name="build-16184"></a>生成 16184

有关常规 Windows 上生成 16184 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/28/announcing-windows-10-insider-preview-build-16184-pc-build-15208-mobile/)。<br/>


### <a name="fixed"></a>固定
- 已删除的 apt 包维护任务 （lxrun.exe/更新）
- 固定的输出中未显示从 node.js [GH 1840] 中的 Windows 进程
- 放宽 lxcore [GH 1794] 中的对齐需求
- 修复了处理的系统调用数中的 AT_EMPTY_PATH 标志。
- 修复了在其中删除带有开放句柄 DrvFs 文件将导致出现未定义的行为 [GH 544,966,1357,1535,1615] 的文件的问题
- / 主机将从 Windows 主机文件 (%windir%\system32\drivers\etc\hosts) 现在继承项 [GH 1495]

</br>

## <a name="build-16179"></a>生成 16179

有关常规 Windows 上生成 16179 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/19/announcing-windows-10-insider-preview-build-16179-pc-build-15205-mobile/)。<br/>


### <a name="fixed"></a>固定
- 没有 WSL 更改这一周。

</br>

## <a name="build-16176"></a>生成 16176

有关常规 Windows 上生成 16176 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/14/announcing-windows-10-insider-preview-build-16176-pc-build-15204-mobile/)。<br/>


### <a name="fixed"></a>固定

- [已启用串行支持](https://blogs.msdn.microsoft.com/wsl/2017/04/14/serial-support-on-the-windows-subsystem-for-linux/)
- 添加了的 IP 套接字选项 IP_OPTIONS [GH 1116]
- （同时将文件上传到 nginx/PHP-FPM） 实现 pwritev 函数 [GH 1506]
- 添加了 IP 套接字选项 IP_MULTICAST_IF & IPV6_MULTICAST_IF [GH 990]
- 支持的套接字选项 IP_MULTICAST_LOOP 和 IPV6_MULTICAST_LOOP [GH 1678]
- 添加的应用程序节点、 traceroute、 dig、 nslookup、 主机的 IP (V6) _MTU 套接字选项
- 添加了的 IP 套接字选项 IPV6_UNICAST_HOPS
- [文件系统的改进](https://blogs.msdn.microsoft.com/wsl/2017/04/18/file-system-improvements-to-the-windows-subsystem-for-linux/)
    * 允许 UNC 路径的装载
    * 启用在 drvfs CDFS 支持
    * 正确处理 drvfs 中的网络文件系统权限
    * 将对远程驱动器的支持添加到 drvfs
    * 启用 FAT 支持 drvfs 中
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果
15042 之后的任何更改

</br>

## <a name="build-16170"></a>生成 16170

有关常规 Windows 上生成 16170 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/04/07/announcing-windows-10-insider-preview-build-16170-pc/)。<br/>

我们发布了新[博客文章](https://blogs.msdn.microsoft.com/wsl/2017/04/11/testing-the-windows-subsystem-for-linux/)讨论测试 WSL 我们努力。

### <a name="fixed"></a>固定

- 支持套接字选项 IP_ADD_MEMBERSHIP & IPV6_ADD_MEMBERSHIP [GH 1678]
- 添加对 PTRACE_OLDSETOPTIONS 的支持。 [GH 1692]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果
15042 之后的任何更改

</br>

## <a name="build-15046-to-windows-10-creators-update"></a>生成 15046 到 Windows 10 创意者更新
没有更多 WSL 修复或计划到 Windows 10 创意者更新中包含的功能。 WSL 的发行说明将在未来几周定目标到下一步的主要 Windows Update 中添加的恢复。 为常规 Windows 的生成 15046 和将来的内部版本信息，请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/28/announcing-windows-10-insider-preview-build-15046-pc/)。 <br/><br/>
 <br/>

## <a name="build-15042"></a>生成 15042

有关常规 Windows 上生成 15042 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/24/announcing-windows-10-insider-preview-build-15042-pc-build-15043-mobile/)。<br/>


### <a name="fixed"></a>固定

- 修复出现死锁时删除路径以"..."
- 修复了在其中 FIONBIO 未成功 [GH 1683] 返回 0
- 已修复的问题的 inet 数据报套接字的长度为零的读取
- 修复由于争用条件可能死锁中 drvfs inode 查找 [GH 1675]
- 扩展对 unix 套接字的辅助数据; 支持SCM_CREDENTIALS 和 SCM_RIGHTS [GH 514，613、 1326年]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：737</br>
未通过的数目 (失败，已跳过，等等。...):255

</br>

## <a name="build-15031"></a>生成 15031

有关常规 Windows 上生成 15031 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/08/announcing-windows-10-insider-preview-build-15031-pc/)。<br/>


### <a name="fixed"></a>固定

- 修复了 bug time(2) 错误偶尔行为。
- 已修复并发出 where * SIGPROCMASK syscall 可能会损坏信号掩码。
- 在 WSL 进程创建通知现在返回完整的命令行长度。 [GH 1632]
- WSL 现在将报告线程退出时通过 GDB 挂起的 ptrace。 [GH 1196]
- 修复了 bug，其中 ptys 会挂起后大量 tmux IO。 [GH 1358]
- 许多系统调用 （futex、 semtimedop、 ppoll、 sigtimedwait、 itimer、 timer_create） 中的固定的超时验证
- 添加了的 eventfd EFD_SEMAPHORE 支持 [GH 452]
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：737</br>
未通过的数目 (失败，已跳过，等等。...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15031)<br/>

<br/>

## <a name="build-15025"></a>生成 15025

有关常规 Windows 上生成 15025 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/02/01/announcing-windows-10-insider-preview-build-15025-pc/)。<br/>


### <a name="fixed"></a>固定

- Bug 修复该坏 grep 2.27 [GH 1578]
- 实现的 EFD_SEMAPHORE 标志 eventfd2 syscall [GH 452]
- 实现 /proc/ [pid] / net/ipv6_route [GH 1608]
- 信号驱动 IO 支持 unix 流套接字 [GH 393，68]
- 支持 F_GETPIPE_SZ 和 F_SETPIPE_SZ [GH 1012]
- 实现 recvmmsg() syscall [GH 1531]
- 修复了 bug 其中 epoll_wait() 不等待 [GH 1609]
- 实现 /proc/version_signature
- Tee syscall 现在返回失败，如果这两个文件描述符是指同一管道
- 实现正确的 Unix 套接字 SO_PEERCRED 行为
- 固定的 tkill syscall 无效参数处理
- 若要增加的 drvfs preformace 的更改
- 微调了 Ruby IO 阻塞
- 固定的 recvmsg() inet 套接字 [GH 1296] MSG_DONTWAIT 标志返回 EINVAL
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：732</br>
未通过的数目 (失败，已跳过，等等。...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15025)<br/>

<br/>

## <a name="build-15019"></a>生成 15019

有关常规 Windows 上生成 15019 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/27/announcing-windows-10-insider-preview-build-15019-pc/)。<br/>


### <a name="fixed"></a>固定

- 修复了 bug 的不正确地报告中的 CPU 使用率 procfs htop (GH 823，945、 971) 等工具
- 在现有调用 open （） 方法与 O_TRUNC 时文件 inotify 现在会生成之前 IN_OPEN IN_MODIFY
- Unix 套接字 getsockopt SO_ERROR 启用 postgress [GH 61，1354年] 的修补程序
- 实现针对 GO 语言 /proc/sys/net/core/somaxconn
- Pt-get 包更新后台任务现在在隐藏模式运行从视图
- Ipv6 localhost （Spring-Framework(Java) 失败） 的清除范围。
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：714 </br>
未通过的数目 (失败，已跳过，等等。...):249 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15019)<br/>

<br/>

## <a name="build-15014"></a>生成 15014

有关常规 Windows 上生成 15014 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/19/announcing-windows-10-insider-preview-build-15014-for-pc-and-mobile-hello-windows-insiders-today-we-are-excited-to-be-releasing-windows-10-insider-preview-build-15014-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定

- Ctrl + C 现在可按预期方式
- htop 和 ps auxw 现在显示正确的资源利用率 (GH #516)
- NT 异常信号的基本转换。 (GH #513)
- fallocate 现在 ENOSPC 与运行时失败而不是 EINVAL (GH #1571) 空间不足
- 添加了的 /proc/sys/kernel/sem。
- 实现的 semop 和 semtimedop 系统调用
- 固定的 nslookup 错误的 IP_RECVTOS & IPV6_RECVTCLASS 套接字选项 (GH 69)
- 对套接字选项 IP_RECVTTL 和 IPV6_RECVHOPLIMIT 的支持
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：709 </br>
未通过的数目 (失败，已跳过，等等。...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014)<br/>

### <a name="syscall-summary"></a>Syscall 摘要
总 Syscall:384 </br>
实现的总计：235 </br>
用作存根的总计：22 </br>
未实现的总计：127 </br>
[详细的分解结构](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15014/Syscalls.txt)<br/>

<br/>

## <a name="build-15007"></a>生成 15007

有关常规 Windows 上生成 15007 信息请访问[Windows 博客]( https://blogs.windows.com/windowsexperience/2017/01/12/announcing-windows-10-insider-preview-build-15007-pc-mobile)。<br/>


### <a name="known-issue"></a>已知的问题

- 是一个已知的 bug，控制台不识别某些 Ctrl +<key>输入。  这包括将充当正常的 c 按键的 ctrl + c 命令。

  - 解决方法：将备用键映射到 Ctrl + C。 例如，若要映射到 Ctrl + C Ctrl + K 执行： `stty intr \^k`。  此映射的每个终端，将需要进行*每个*启动时间 bash。 用户可以浏览选项，此操作在其 `.bashrc`

### <a name="fixed"></a>固定

- 更正了在其中运行 WSL 会占用 100%的 CPU 内核的问题
- 套接字选项 IP_PKTINFO，IPV6_RECVPKTINFO 现在支持。 (GH #851, 987)
- 截断到 lxcore 以 16 个字节的网络接口物理地址 (GH #1452，1414，1343，468，308)
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：709 </br>
未通过的数目 (失败，已跳过，等等。...):255 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15007)<br/>

<br/>

## <a name="build-15002"></a>生成 15002

有关常规 Windows 上生成 15002 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2017/01/09/announcing-windows-10-insider-preview-build-15002-pc/)。<br/>


### <a name="known-issue"></a>已知的问题

两个已知的问题：
- 是一个已知的 bug，控制台不识别某些 Ctrl +<key>输入。  这包括将充当正常的 c 按键的 ctrl + c 命令。

  - 解决方法：将备用键映射到 Ctrl + C。 例如，若要映射到 Ctrl + C Ctrl + K 执行： `stty intr \^k`。  此映射的每个终端，将需要进行*每个*启动时间 bash。 用户可以浏览选项，此操作在其 `.bashrc`

- WSL 正在运行时系统线程将占用 100%的 CPU 核心。  解决并在内部修复根本原因。

### <a name="fixed"></a>固定

- 现在必须在相同的权限级别创建所有的 bash 会话。  尝试在不同级别上启动会话将被阻止。  这意味着管理员和非管理员控制台不能在同一时间运行。 (GH #626)
<br/>
- 实现以下 NETLINK_ROUTE 消息 （需要 Windows 管理员）
     - RTM_NEWADDR (支持`ip addr add`)
     - RTM_NEWROUTE (支持`ip route add`)
     - RTM_DELADDR (支持`ip addr del`)
     - RTM_DELROUTE (支持`ip route del`)
- 检查要更新的包的计划的任务运行将不再按流量计费的连接 (GH #1371)
- 修复了错误卡在何处通过管道将获取即 bash-c"ls alR /"|bash-c"cat"(GH #1214)
- 实现的 TCP_KEEPCNT 套接字选项 (GH #843)
- 实现的 IP_MTU_DISCOVER INET 套接字选项 (GH #720、 717，170，69)
- 删除旧的功能，若要从使用 NT 路径查找 init 运行 NT 二进制文件。 (GH #1325)
- 修复/kmsg 以允许组 / 其他读取访问权限 (0644) （GH # 1321） 哈希模式
- 实现的 /proc/sys/kernel/random/uuid (GH #1092)
- 更正了的错误的进程启动时间显示为 2432 年 (GH #974)
- 切换的默认术语环境变量为 xterm 256color (GH #1446)
- 修改后在进程分叉期间计算处理提交的方式。 (GH #1286)
- 实现的 /proc/sys/vm/overcommit_memory。 (GH #1286)
- 实现的 /proc/net/route 文件 (GH #69)
- 修复了快捷方式名称不正确的错误本地化 (GH #696)
- 固定的 elf 分析错误地验证程序标头的逻辑必须是小于 （或等于） PATH_MAX。 (GH #1048)
- 实现的 statfs 回调 procfs，sysfs、 cgroupfs，和 binfmtfs (GH #1378)
- 不会关闭 (GH #1184，GH # 1193年中也讨论了) 的固定的 AptPackageIndexUpdate windows
- 添加了的 ASLR 个性 ADDR_NO_RANDOMIZE 支持。 (GH #1148, 1128)
- 改进了的 PTRACE_GETSIGINFO，SIGSEGV 的适当 gdb AV (GH #875) 期间的堆栈跟踪
- Elf 不再解析为 patchelf 二进制文件无法正常工作。 (GH #471)
- VPN DNS 传播到 /etc/resolv.conf (GH #416，1350年)
- 对 TCP 的改进关闭的更可靠的数据传输。 (GH #610 616、 1025，1335年)
- 现在返回正确的错误代码的文件太多时打开 (EMFILE)。 (GH # 1126年 2090年)
- Windows 审核过程中的映像名称日志现在报表创建审核。
- 正常失败时启动 bash 窗口中的从 bash.exe
- 互操作时，添加了的错误消息无法访问工作目录下 LxFs (即 notepad.exe.bashrc)
- 修复了问题，Windows 路径已被截断 WSL
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：690 </br>
未通过的数目 (失败，已跳过，等等。...):274 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/15002)<br/>

<br/>

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`shmctl`<br/>
`shmget`<br/>
`shmdt`<br/>
`shmat`<br/>
<br/>

## <a name="build-14986"></a>生成 14986

有关常规 Windows 上生成 14986 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/12/07/announcing-windows-10-insider-preview-build-14986-pc/)。<br/>


### <a name="fixed"></a>固定

- 使用 Netlink 和 Pty Ioctl 固定错误检查
- 内核版本现在将报告 4.4.0-43 与 Xenial 的一致性
- Bash.exe 现在启动时输入定向到 nul: (GH #1259)
- 线程 Id 现在可以正确报告中 procfs (GH #967)
- IN_UNMOUNT |IN_Q_OVERFLOW |IN_IGNORED |现在支持在 inotify_add_watch() (GH #1280) IN_ISDIR 标志
- 实现 timer_create 和相关的系统调用。  这使 GHC 支持 (GH #307)
- 修复了 ping 返回的时间为 0.000ms (GH #1296) 的位置的问题
- 打开的文件太多时，请返回正确的错误代码。
- 其中的网络接口数据 Netlink 请求接口的硬件地址为 32 字节 （如 Teredo 接口） 将失败并 EINVAL WSL 中修复的问题
   - 请注意，Linux"ip"实用程序包含一个 bug，它会崩溃如果 WSL 报告 32 字节硬件地址。 这是"ip"，不 WSL 中的 bug。 "Ip"实用程序硬编码的字符串缓冲区长度用于打印硬件地址，并且该缓冲区因过小，若要打印的 32 字节硬件地址。
- 其他修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：669 </br>
未通过的数目 (失败，已跳过，等等。...):258 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14986)<br/>

<br/>

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`timer_create`<br/>
`timer_delete`<br/>
`timer_gettime`<br/>
`timer_settime`<br/>
<br/>

## <a name="build-14971"></a>生成 14971

有关常规 Windows 上生成 14971 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/17/announcing-windows-10-insider-preview-build-14971-for-pc/)。<br/>


### <a name="fixed"></a>固定

 - 由于超出我们的控制范围的情况适用于 Linux 的 Windows 子系统本版本中没有的更新。  定期计划的更新将在下一版本上继续进行。

### <a name="ltp-results"></a>LTP 结果：
14965 相比并无变化 </br>
通过的测试数：664 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14965"></a>生成 14965

有关常规 Windows 上生成 14965 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/09/announcing-windows-10-insider-preview-build-14965-for-mobile-and-pc/)。<br/>


### <a name="fixed"></a>固定

- 支持 Netlink 套接字 NETLINK_ROUTE 协议 RTM_GETLINK 和 RTM_GETADDR (GH #468)
  - 启用网络枚举 ifconfig 和 ip 命令
  - 详细信息可在我们[WSL 网络博客文章](https://blogs.msdn.microsoft.com/wsl/2016/11/08/225/)。

- /sbin 现在在默认情况下的用户的 path
- 现在默认情况下 （即可以现在键入 notepad.exe 而无需添加到 Linux 路径 System32） 追加到 WSL 路径的 NT 用户路径
- 添加了的对 /proc/sys/kernel/cap_last_cap
- 现在 NT 二进制文件可以启动从 WSL 中，如果当前工作目录包含非 ansi 字符 (GH #1254)
- 允许断开连接的 unix 流套接字上的关闭。
- 添加了的对 PR_GET_PDEATHSIG。
- 添加了的对 CLONE_PARENT
- 修复了错误卡在何处通过管道将获取即 bash-c"ls alR /"|bash-c"cat"(GH #1214)
- 若要连接到当前终端的处理请求。
- 将标记 /proc/<pid>/oom_score_adj 为可写入。
- 添加 /sys/fs/cgroup 文件夹。
- sched_setaffinity 应返回关联位掩码的数
- 修复错误地假设它解释器路径必须少于 64 个字符长 ELF 验证逻辑。 (GH #743)
- 打开的文件描述符可以保留控制台窗口处于打开状态 (GH #1187)
- Fixeed 错误其中 rename （） 失败，出现尾部反斜杠目标名称 (GH #1008)
- 实现 /proc/net/dev 文件
- 由于计时器分辨率，固定的 0.000ms 执行 ping 操作。
- 实现的 /proc/self/environ (GH #730)
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：664 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14965)<br/>

<br/>

## <a name="build-14959"></a>生成 14959

有关常规 Windows 上生成 14959 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/11/03/announcing-windows-10-insider-preview-build-14959-for-mobile-and-pc/#iI82GufJxMF3POU1.97)。<br/>


### <a name="fixed"></a>固定

- 改进了的 Windows 的 Pico 进程通知。  上找到其他信息[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/11/01/wsl-antivirus-and-firewall-compatibility/)。
- 使用 Windows 的互操作性的改进了的稳定性
- 修复了错误 0x80070057 时启动 bash.exe 时启用了企业数据保护 (EDP)
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：665 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14959)<br/>

<br/>

## <a name="build-14955"></a>生成 14955

有关常规 Windows 上生成 14955 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/25/announcing-windows-10-insider-preview-build-14955-for-mobile-and-pc/#guGXQzKVFrZIDUYR.97)。<br/>


### <a name="fixed"></a>固定

 - 由于超出我们的控制范围的情况适用于 Linux 的 Windows 子系统本版本中没有的更新。  定期计划的更新将在下一版本上继续进行。

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：665 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14955)<br/>

<br/>

## <a name="build-14951"></a>生成 14951

有关常规 Windows 上生成 14951 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/19/announcing-windows-10-insider-preview-build-14951-for-mobile-and-pc/)。<br/>


### <a name="new-feature-windows--ubuntu-interoperability"></a>新功能：Windows / Ubuntu 的互操作性
现在可以直接从 WSL 命令行调用 Windows 二进制文件。  这使用户能够使用其 Windows 环境和系统中已不可能的方式进行交互。  作为快速示例中，是现在用户可以运行以下命令：

    ```
    $ export PATH=$PATH:/mnt/c/Windows/System32
    $ notepad.exe
    $ ipconfig.exe | grep IPv4 | cut -d: -f2
    $ ls -la | findstr.exe foo.txt
    $ cmd.exe /c dir
    ```

可以在找到详细信息：

- [互操作的 WSL 团队博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)<br/>
- [MSDN 互操作文档](https://msdn.microsoft.com/en-us/commandline/wsl/interop)<br/>

### <a name="fixed"></a>固定

- Ubuntu 16.04 (Xenial) 现已安装的所有新 WSL 实例。  具有现有 14.04 （值得信赖） 实例的用户将不会自动升级。
- 现在显示在安装过程中设置的区域设置
- 终端的改进包括的 bug 其中不始终将 WSL 过程重定向到一个文件不起作用
- 控制台生存期应取决于 bash.exe 生存期
- 控制台窗口大小应使用可见的大小，不缓冲区大小
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：665 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14951)<br/>

<br/>

## <a name="build-14946"></a>生成 14946

有关常规 Windows 上生成 14946 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/10/13/announcing-windows-10-insider-preview-build-14946-for-pc-and-mobile/#xj8GdVooEqo4H7H7.97)。<br/>


### <a name="fixed"></a>固定

- 修复了阻止使用包含空格或引号的 NT 用户名创建 WSL 的用户的用户帐户。 
- 更改 VolFs 和 DrvFs 统计信息中返回 0 表示目录的链接计数
- 支持 IPV6_MULTICAST_HOPS 套接字选项。
- 限制到单个控制台 I/O 循环每 tty。 示例： 可能是以下命令：
  - bash -c "echo data" | bash -c "ssh user@example.com 'cat > foo.txt'"

- 空格替换为 /proc/cpuinfo (GH #1115) 中的选项卡
- DrvFs 现在将显示在名称匹配已安装的 Windows 卷 mountinfo
- /home 和 /root 现在出现在正确的名称与 mountinfo
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：665 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14946)<br/>

<br/>

## <a name="build-14942"></a>生成 14942

有关常规 Windows 上生成 14942 信息请访问[Windows 博客](https://aka.ms/onefourninefourtwoooooo)。<br/>


### <a name="fixed"></a>固定

- 错误检查，包括"尝试执行的 NOEXECUTE 内存"网络已阻止 SSH 的故障数
- 在现 inotifiy 支持来自 DrvFs 上的 Windows 应用程序生成的通知
- 实施 mongod TCP_KEEPIDLE 和 TCP_KEEPINTVL。 (GH #695)
- 实现 pivot_root 系统调用
- 实现 SO_DONTROUTE 的套接字选项
- 其他 bug 修复和改进


### <a name="ltp-results"></a>LTP 结果：
通过的测试数：665 </br>
未通过的数目 (失败，已跳过，等等。...):263 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14942)<br/>

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`pivot_root`<br/>
<br/>

## <a name="build-14936"></a>生成 14936

有关常规 Windows 上生成 14936 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/28/announcing-windows-10-insider-preview-build-14936-for-pc/)。<br/>


注意：WSL 将在即将发布的版本中安装 Ubuntu 版本 16.04 (Xenial) 而不是 Ubuntu 14.04 （可信赖）。  此更改将应用于预览体验成员安装新实例 （lxrun.exe /install 或首次运行 bash.exe）。  可信赖的现有实例将不自动升级。 用户可以升级其值得信赖的映像为 Xenial 使用执行版本升级命令。

### <a name="known-issue"></a>已知的问题
WSL 遇到某些套接字实现的问题。  检测的错误表现为崩溃并出现错误"尝试执行的 NOEXECUTE 内存"。  使用 ssh 配合使用时，此问题的最常见的表现是崩溃。  在内部版本中已修复并尽早将被推送到内部人员根本原因。

### <a name="fixed"></a>固定

- 实现 chroot 系统调用
- 改进 inotify~~包括对来自 DrvFs 上的 Windows 应用程序生成的通知的支持~~
  - 更正：Inotify 更改源自 Windows 应用程序在此时间不可用的支持。
- 套接字绑定到 IPV6::<port n>现在支持 IPV6_V6ONLY (GH #68、 #157、 #393、 #460，#674、 #740、 #982、 #996)
- Waitid systemcall WNOWAIT 行为实现 (GH #638)
- 支持 IP 套接字选项 IP_HDRINCL 和 IP_TTL
- 应立即返回长度为零的 read （） (GH #975)
- 正确处理文件名和文件名的前缀，.tar 文件中不包括 NULL 终止符。
- epoll /dev/null 时支持
- 修复 /dev/alarm 时间源
- Bash-c 现在可以将重定向到文件
- 其他 bug 修复和改进

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：664 </br>
未通过的数目 (失败，已跳过，等等。...):264 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14936)<br/>

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`chroot`<br/>
<br/>

## <a name="build-14931"></a>生成 14931

有关常规 Windows 上生成 14931 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/21/announcing-windows-10-insider-preview-build-14931-for-pc/)。<br/>


### <a name="fixed"></a>固定

 - 由于超出我们的控制范围的情况适用于 Linux 的 Windows 子系统本版本中没有的更新。  定期计划的更新将继续进行下一版本中。

<br/>

## <a name="build-14926"></a>生成 14926

有关常规 Windows 上生成 14926 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/09/14/announcing-windows-10-insider-preview-build-14926-for-pc-and-mobile/)。<br/>


### <a name="fixed"></a>固定

- 成功进行 ping 操作现在具有管理员特权的控制台中的工作原理
- Ping6 现在支持，也无需管理员权限
- Inotify 支持通过 WSL 修改的文件。 (GH #216)
  - 支持的标志：
    - inotify_init1:LX_O_CLOEXEC LX_O_NONBLOCK
    - inotify_add_watch 事件：LX_IN_ACCESS、 LX_IN_MODIFY、 LX_IN_ATTRIB、 LX_IN_CLOSE_WRITE、 LX_IN_CLOSE_NOWRITE、 LX_IN_OPEN、 LX_IN_MOVED_FROM、 LX_IN_MOVED_TO、 LX_IN_CREATE、 LX_IN_DELETE、 LX_IN_DELETE_SELF、 LX_IN_MOVE_SELF
    - inotify_add_watch 属性：LX_IN_DONT_FOLLOW, LX_IN_EXCL_UNLINK, LX_IN_MASK_ADD, LX_IN_ONESHOT, LX_IN_ONLYDIR
    - 读取输出：LX_IN_ISDIR LX_IN_IGNORED
  - 已知的问题：修改文件从 Windows 应用程序不会生成任何事件
- Unix 套接字现在支持 SCM_CREDENTIALS

### <a name="ltp-results"></a>LTP 结果：
通过的测试数：651 </br>
未通过的数目 (失败，已跳过，等等。...):258 </br>
[LTP 测试运行日志](https://github.com/Microsoft/CommandLine-Documentation/tree/live/LTP_Results/14926)<br/>

<br/>

## <a name="build-14915"></a>生成 14915

有关常规 Windows 上生成 14915 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/31/announcing-windows-10-insider-preview-build-14915-for-pc-and-mobile)。<br/>


### <a name="fixed"></a>固定
-  Socketpair unix 数据报套接字 (GH #262)
- SO_REUSEADDR Unix 套接字支持
- UNIX 套接字支持 SO_BROADCAST (GH #568)
- Unix 套接字支持 SOCK_SEQPACKET (GH #758，#546)
- 添加对 unix 数据报套接字发送、 接收和关闭的支持
- 解决由于非固定地址无效 mmap 参数验证错误检查。 (GH #847)
- 支持暂停 / 恢复终端状态的
- 对 TIOCPKT ioctl，若要取消阻止屏幕实用程序 (GH #774) 的支持
    - 已知的问题：功能键不可操作
- 更正可能导致已释放的成员 ReaderReady LxpTimerFdWorkerRoutine (GH #814) 访问的 TimerFd 的争用问题
- 启用可重新启动系统调用支持 futex、 投票、 和 clock_nanosleep
- 添加了的绑定装入支持
- 取消共享装入命名空间支持
    - 已知的问题：创建与新的装入命名空间时`unshare(CLONE_NEWNS)`当前工作目录将继续指向旧的命名空间
- 其他改进和 bug 修复

<br/>

## <a name="build-14905"></a>生成 14905

有关常规 Windows 上生成 14905 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/17/announcing-windows-10-insider-preview-build-14905-for-pc-mobile/)。<br/>


### <a name="fixed"></a>固定
- 可重新启动系统调用现支持 (GH #349，GH #520)
- 符号链接到目录结束在 / 现在操作 (GH #650)
- 实现的 RNDGETENTCNT ioctl 用于 /dev/random
- 实现 /proc/ [pid] / 装载 /proc/ [pid] / mountinfo 和 /proc/ [pid] / mountstats 文件
- 其他 bug 修复和改进

</br>

## <a name="build-14901"></a>生成 14901
第一个预览体验内部版本的 Windows 10 周年更新发布的文章。

有关常规 Windows 上生成 14901 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/08/11/announcing-windows-10-insider-preview-build-14901-for-pc/)。<br/>


### <a name="fixed"></a>固定
- 修复了尾随斜杠问题
    - 命令，如`$ mv a/c/ a/b/`现在工作
- 如果 Ubuntu 区域设置应设置为 Windows 区域设置安装现在会提示
- Procfs 支持 ns 文件夹
- 添加装载和卸载 tmpfs，procfs 和 sysfs 文件系统
- [32 位 ABI 签名在] 修复 mknod
- Unix 套接字移动调度模型
- 应遵循设置使用 setsockopt INET 套接字接收缓冲区大小
- 实现 MSG_CMSG_CLOEXEC unix 套接字接收消息标志
- Linux 进程 stdin/stdout 管道重定向 (GH #2)
    - 允许在命令中的 bash-c 命令的管道  示例： > dir |bash-c"grep foo"
- 现在可以具有多个页面文件 (GH #538，#358) 的系统上安装 bash
- 默认 INET 套接字缓冲区大小应与匹配的默认 Ubuntu 安装程序
- 对齐到 listxattr xattr syscall
- 只能从 SIOCGIFCONF 返回有效的 IPv4 地址的接口
- 修复信号时由 ptrace 注入的默认操作
- implement /proc/sys/vm/min_free_kbytes
- 还原在 sigreturn 上下文时使用计算机上下文寄存器值
    - 这样可以解决问题 java 和 javac 已挂起的位置为一些用户
- 实现 /proc/sys/kernel/hostname

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`waitid`<br/>
`epoll_pwait`<br/>

<br/>

## <a name="build-14388-to-windows-10-anniversary-update"></a>生成 14388 到 Windows 10 周年更新
有关常规 Windows 上生成 14388 信息请访问[Windows 博客](https://aka.ms/14388wip)。 <br/>

### <a name="fixed"></a>固定
- 修复了准备的 Windows 10 周年更新上 8/2
  - 有关 WSL 周年更新中的详细信息可以位于我们[博客](https://blogs.msdn.microsoft.com/wsl/)

<br/>

## <a name="build-14376"></a>生成 14376
有关常规 Windows 上生成 14376 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/28/announcing-windows-10-insider-preview-build-14376-for-pc-and-mobile/)。 <br/>

### <a name="fixed"></a>固定
- 删除某些情况下其中的 apt-get 挂起 (GH #493)
- 修复了在其中空装载了无法正确处理
- 修复了在其中 ramdisks 未正确安装
- 更改 unix 套接字接受以支持标志 (部分 GH #451)
- 固定的常见网络相关 bluescreen
- 修复出现蓝屏时访问 /proc/ [pid] / 任务 (GH #523)
- 对于某些 pty 方案 (GH #488，#504) 的固定高 CPU 使用率
- 其他 bug 修复和改进

<br/>

## <a name="build-14371"></a>生成 14371
有关常规 Windows 上生成 14371 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/22/announcing-windows-10-insider-preview-build-14371-for-pc/)。 <br/>

### <a name="fixed"></a>固定
- 使用的 ptrace 时更正 SIGCHLD 和 wait() 计时争用
- 更正一些行为，当路径中含有尾随 / (GH #432)
- 修复了重命名/取消关联由于打开句柄子级而失败的问题
- 其他 bug 修复和改进

<br/>

## <a name="build-14366"></a>生成 14366
有关常规 Windows 上生成 14366 信息请访问[Windows 博客](https://blogs.windows.com/windowsexperience/2016/06/14/announcing-windows-10-insider-preview-build-14366-mobile-build-14364/)。 <br/>

### <a name="fixed"></a>固定
- 修复中通过符号链接的文件创建
-   用于 Python (GH 385) 添加了的 listxattr
-   其他 bug 修复和改进

### <a name="syscall-support"></a>支持 Syscall
-   下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`listxattr`<br/>
<br/>

## <a name="build-14361"></a>版本 14361
有关常规 Windows 内部版本 14361 信息请访问[Windows 博客](https://aka.ms/wip14361)。 <br/>

### <a name="fixed"></a>固定
- 在中的 Bash 在 Ubuntu 上运行在 Windows 上时，DrvFs 现区分大小写。
  - 用户可能 case.txt 和用例。TXT 上其/mnt/c 驱动器
  - Bash on Ubuntu 上 Windows 仅支持区分大小写。 当 Bash NTFS 的外部将报表文件正确，但可能发生意外的行为与 Windows 中的文件进行交互。
  - 每个卷 (即 /mnt/c) 的根目录不区分大小写
  - 可在处理这些文件在 Windows 中的详细信息[此处](https://support.microsoft.com/en-us/kb/100625)。
- 大大增强 pty / tty 支持。  应用程序，如 TMUX 现在支持 (GH #40)
- 不是始终创建用户帐户的固定的安装问题
- 优化允许相当长参数列表的命令行参数结构。 (GH #153)
- 现在可以删除和 chmod read_only 文件从 DrvFs
- 修复了某些情况下，在终端挂起断开连接 (GH #43)
- chmod 和 chown 现在在 tty 设备上工作
- 允许连接到 0.0.0.0 和:: 为本地主机 (GH #388)
- Sendmsg/recvmsg 现在处理的 IO 向量长度 > 1 (部分 GH #376)
- 用户可以立即选择退出自动生成的主机文件 (GH #398)
- 自动与 Linux 为 NT 区域设置的区域设置匹配 (GH #11) 安装过程
- 添加 /proc/sys/vm/swappiness 文件 (GH #306)
- 跟踪来现在正常退出
- 允许通过 /proc/self/fd (GH #222) 重新打开管道
- 隐藏 %LOCALAPPDATA%\lxss 从 DrvFs (GH #270) 下的目录
- 更好地处理 bash.exe ~。  命令，如"bash ~-c ls"现在支持 (GH #467)
- 套接字现在当 epoll 读取期间关闭 (GH #271) 可用
- lxrun / 卸载更好地删除文件和文件夹
- 已更正的 ps-f (GH #246)
- 改进了对 x11 支持应用程序，例如 xEmacs (GH #481)
- 已更新初始线程堆栈大小，使之与默认 Ubuntu 设置和向 get_rlimit syscall (GH #172，#258) 正确报告大小
- 改进了 pico 进程映像名称 （例如，用于审核） 的报告
- 实现的 /proc/mountinfo df 命令
- 修复子名称的符号链接错误代码。 和...
- 其他改进 bug 修复和改进

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`GETTIMER`<br/>
`MKNODAT`<br/>
`RENAMEAT`<br/>
`SENDFILE`<br/>
`SENDFILE64`<br/>
`SYNC_FILE_RANGE`<br/>
<br/>

## <a name="build-14352"></a>生成 14352
有关常规 Windows 上生成 14352 信息请访问[Windows 博客](https://aka.ms/wip14352)。<br/>


### <a name="fixed"></a>固定
- 其中较大的文件是未下载 / 正确创建的已修复的问题。  这应取消阻止 npm 和其他方案 （GH #3，GH #313）
- 删除某些情况下，套接字会挂起
- 更正了一些的 ptrace 错误
- 已修复的问题 WSL 允许文件名长度超过 255 个字符
- 改进了对非英语字符支持
- 添加当前 Windows 时区数据并将设置为默认值
- 唯一的设备 id 的每个装入点 （jre 修复 – GH #49）
- 更正问题与包含的路径"。" 和"."
- 添加了先进先出的支持 (GH #71)
- Resolv.conf，与本机 Ubuntu 格式匹配的更新的格式
- 一些 procfs 清理
- 管理员控制台 (GH #18) 的已启用的 ping

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`FALLOCATE`<br/>
`EXECVE`<br/>
`LGETXATTR`<br/>
`FGETXATTR`<br/>
<br/>

## <a name="build-14342"></a>生成 14342
常规的 Windows 上的信息生成 14342 [Windows 博客](https://aka.ms/wip14342)。 <br/>

VolFs 和 DriveFs 信息可能位于[WSL 博客](https://blogs.msdn.microsoft.com/wsl)。 <br/>

### <a name="fixed"></a>固定
- 修复 Windows 用户的用户名具有 Unicode 字符时安装的问题
- 默认情况下，首次运行时现在提供常见问题解答中的 apt-get 更新 udev 解决方法
- 启用 DriveFs 中的符号链接 (/mnt/<drive>) 目录
- 符号链接现在 DriveFs 和 VolFs 之间工作
- 分析问题的寻址顶部级别路径： ls。 / / 现在按预期方式工作
- npm 安装上 DriveFs 和-g 选项目前正在处理
- 修复了阻止 PHP 服务器启动的问题
- 更新的默认环境值，例如 $PATH 以更接近匹配本机 Ubuntu
- 在 Windows 更新 apt 包缓存中添加一个每周维护任务
- ELF 标头验证修复的问题，WSL 现在支持所有 Melkor 选项
- Zsh shell 是功能
- 现在支持预编译转到二进制文件
- 在首次运行 Bash.exe 上提示现已正确本地化
- /proc/meminfo 现在返回正确的信息
- 套接字 VFS 中现在支持
- /dev 现在已装载为 tempfs
- 现在支持先进先出
- 多核系统现在/proc/cpuinfo 中正确显示
- 其他改进和下载在首次运行期间的错误消息
- Syscall 改进和 bug 修复。 支持的 syscall 下面的列表。
- 其他 bug 修复和改进

### <a name="known-issues"></a>已知问题
- 未解决... 在某些情况下 DriveFs 上正确

### <a name="syscall-support"></a>支持 Syscall
下面是一系列新的或增强 syscall WSL 中具有一些实现的。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

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

## <a name="build-14332"></a>生成 14332

有关常规 Windows 上生成 14332 信息请访问[Windows 博客](https://aka.ms/wip14332)。 <br/>


### <a name="fixed"></a>固定
- 更好地 resolv.conf 生成包括确定优先级 DNS 条目
- 移动文件和目录之间 /mnt 和非问题-/ mnt 驱动器
- 现在可以使用符号链接创建的 tar 文件
- 添加了的默认 /run/lock 目录上创建实例
- 更新 /dev/null 时要返回正确的状态信息
- 下载期间首次运行时的其他错误
- Syscall 改进和 bug 修复。 支持的 syscall 下面的列表。
- 其他改进 bug 修复和改进

### <a name="syscall-support"></a>支持 Syscall
下面是在 WSL 中具有一些实现新 syscall。 在此列表上的 syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

`READLINKAT`<br/>
<br/>

## <a name="build-14328"></a>内部版本 14328

有关常规 Windows 上生成 14332 信息请访问[Windows 博客](https://aka.ms/wip14328)。 <br/>


### <a name="new-features"></a>新功能
* 现在支持 Linux 用户。  在 Windows 上的 Ubuntu 上安装 Bash 会提示创建的 Linux 用户。  有关详细信息，请访问 https://aka.ms/wslusers
* 主机名现在设置为 Windows 计算机名称，没有更多 @localhost
* 有关详细信息内部版本 14328，请访问： https://aka.ms/wip14328

### <a name="fixed"></a>固定
* 非 /mnt/ 的符号链接改进<drive>文件
    * npm 安装现在的工作原理
    * jdk / 现在可安装的 jre 使用找到的说明[此处](https://xubuntugeek.blogspot.com/2012/09/how-to-install-oracle-jdk-7-manually-in.html)。
    * 已知问题： 对于 Windows 装载符号链接不起作用。  可在更高版本中的功能
* top 和 htop 现在会显示
* 对于某些其他错误消息安装失败
* Syscall 改进和 bug 修复。  支持的 syscall 下面的列表。
* 其他改进 bug 修复和改进

### <a name="syscall-support"></a>支持 Syscall
下面是在 WSL 中有一些实现 syscall 的列表。  在此列表上的 Syscall 支持在至少一个方案中，但可能不具有所有参数都支持这一次。

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
