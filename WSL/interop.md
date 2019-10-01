---
title: Windows 与 Linux 的互操作性
description: 介绍 Windows 与适用于 Linux 的 Windows 子系统上运行的 Linux 分发版之间的互操作性。
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: f8b0150c044f5011b84e80cac4befd752c4dc552
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269797"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="665af-103">适用于 Linux 的 Windows 子系统与 Windows 的互操作性</span><span class="sxs-lookup"><span data-stu-id="665af-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="665af-104">**已针对 Fall Creators Update 更新。**</span><span class="sxs-lookup"><span data-stu-id="665af-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="665af-105">如果你运行的是创意者更新或周年更新，请跳转到[创意者/周年更新部分](interop.md#creators-update-and-anniversary-update)。</span><span class="sxs-lookup"><span data-stu-id="665af-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="665af-106">适用于 Linux 的 Windows 子系统 (WSL) 正在持续改进 Windows 与 Linux 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="665af-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="665af-107">你可以：</span><span class="sxs-lookup"><span data-stu-id="665af-107">You can:</span></span>

1. <span data-ttu-id="665af-108">从 Linux 控制台调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="665af-109">从 Windows 控制台调用 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="665af-110">**Windows 预览体验成员内部版本 17063+** 在 Linux 与 Windows 之间共享环境变量。</span><span class="sxs-lookup"><span data-stu-id="665af-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="665af-111">这可以在 Windows 与 WSL 之间提供无缝的体验。</span><span class="sxs-lookup"><span data-stu-id="665af-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="665af-112">[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)中提供了技术详细信息。</span><span class="sxs-lookup"><span data-stu-id="665af-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="665af-113">从 Windows 命令行运行 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="665af-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="665af-114">使用 `wsl.exe <command>` 从 Windows 命令提示符（CMD 或 PowerShell）运行 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="665af-115">以这种方式调用二进制文件：</span><span class="sxs-lookup"><span data-stu-id="665af-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="665af-116">使用当前 CMD 或 PowerShell 提示符中提到的同一工作目录。</span><span class="sxs-lookup"><span data-stu-id="665af-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="665af-117">以 WSL 默认用户的身份运行。</span><span class="sxs-lookup"><span data-stu-id="665af-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="665af-118">拥有与调用方进程和终端相同的 Windows 管理权限。</span><span class="sxs-lookup"><span data-stu-id="665af-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="665af-119">例如：</span><span class="sxs-lookup"><span data-stu-id="665af-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="665af-120">`wsl.exe` 后面的 Linux 命令的处理方式与 WSL 中运行的任何命令的处理方式类似。</span><span class="sxs-lookup"><span data-stu-id="665af-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="665af-121">可以执行 sudo、管道处理和文件重定向等操作。</span><span class="sxs-lookup"><span data-stu-id="665af-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="665af-122">使用 sudo 的示例：</span><span class="sxs-lookup"><span data-stu-id="665af-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="665af-123">混合 WSL 和 Windows 命令的示例：</span><span class="sxs-lookup"><span data-stu-id="665af-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="665af-124">传入 `wsl.exe` 的命令将按原样转发到 WSL 进程。</span><span class="sxs-lookup"><span data-stu-id="665af-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="665af-125">文件路径必须以 WSL 格式指定。</span><span class="sxs-lookup"><span data-stu-id="665af-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="665af-126">使用路径的示例：</span><span class="sxs-lookup"><span data-stu-id="665af-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="665af-127">从 WSL 运行 Windows 工具</span><span class="sxs-lookup"><span data-stu-id="665af-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="665af-128">WSL 可以使用 `[binary name].exe` 直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="665af-129">例如， `notepad.exe`。</span><span class="sxs-lookup"><span data-stu-id="665af-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="665af-130">为使 Windows 可执行文件更易于运行，Windows 路径将包含在 Fall Creators Update 中的 Linux `$PATH` 内。</span><span class="sxs-lookup"><span data-stu-id="665af-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="665af-131">以这种方式运行的应用程序具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="665af-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="665af-132">按 WSL 命令提示保留工作目录（大部分情况下是这样 -- 下面所述的情况除外）。</span><span class="sxs-lookup"><span data-stu-id="665af-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="665af-133">拥有与 WSL 进程相同的权限。</span><span class="sxs-lookup"><span data-stu-id="665af-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="665af-134">以活动 Windows 用户的身份运行。</span><span class="sxs-lookup"><span data-stu-id="665af-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="665af-135">显示在 Windows 任务管理器中，就如同直接从 CMD 提示符执行的一样。</span><span class="sxs-lookup"><span data-stu-id="665af-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="665af-136">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="665af-137">在 WSL 中运行的 Windows 可执行文件的处理方式类似于本机 Linux 可执行文件 - 管道处理、重定向，甚至后台处理都可按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="665af-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="665af-138">使用管道的示例：</span><span class="sxs-lookup"><span data-stu-id="665af-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="665af-139">使用混合 Windows 和 WSL 命令的示例：</span><span class="sxs-lookup"><span data-stu-id="665af-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="665af-140">Windows 二进制文件必须包含文件扩展名，匹配文件大小写，并且可执行。</span><span class="sxs-lookup"><span data-stu-id="665af-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="665af-141">包含批处理脚本的不可执行文件。</span><span class="sxs-lookup"><span data-stu-id="665af-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="665af-142">`dir` 等 CMD 本机命令可与 `cmd.exe /C` 命令一起运行。</span><span class="sxs-lookup"><span data-stu-id="665af-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="665af-143">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="665af-144">参数将按原样传递到 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="665af-145">例如，以下命令将在 `C:\temp\foo.txt` 中打开 `notepad.exe`：</span><span class="sxs-lookup"><span data-stu-id="665af-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="665af-146">不支持使用 WSL 中的 Windows 应用程序修改位于 VolFs 中的文件（不是在 `/mnt/<x>` 下的文件）。</span><span class="sxs-lookup"><span data-stu-id="665af-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="665af-147">默认情况下，WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录，但如果工作目录位于 VolFs 中，则会回退到实例创建目录。</span><span class="sxs-lookup"><span data-stu-id="665af-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="665af-148">例如，`wsl.exe` 最初是从 `C:\temp` 启动的，而当前 WSL 目录已更改为用户的主目录。</span><span class="sxs-lookup"><span data-stu-id="665af-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="665af-149">如果从用户的主目录调用 `notepad.exe`，WSL 将自动还原到 `C:\temp`（notepad.exe 工作目录）：</span><span class="sxs-lookup"><span data-stu-id="665af-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> wsl
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit

exit
C:\temp>dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="665af-150">在 Windows 与 WSL 之间共享环境变量</span><span class="sxs-lookup"><span data-stu-id="665af-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="665af-151">在 Windows 预览体验成员内部版本 17063 和更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="665af-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="665af-152">在 17063 以前，只有 WSL 可访问的 Windows 环境变量是 `PATH`（因此可以从 WSL 下启动 Win32 可执行文件）。</span><span class="sxs-lookup"><span data-stu-id="665af-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="665af-153">从 17063 开始，WSL 和 Windows 共享 `WSLENV`（为了桥接在 WSL 上运行的 Windows 和 Linux 分发版而创建的特殊环境变量）。</span><span class="sxs-lookup"><span data-stu-id="665af-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="665af-154">`WSLENV` 的属性：</span><span class="sxs-lookup"><span data-stu-id="665af-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="665af-155">它是共享的；它同时在 Windows 和 WSL 环境中存在。</span><span class="sxs-lookup"><span data-stu-id="665af-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="665af-156">它是要在 Windows 与 WSL 之间共享的环境变量列表。</span><span class="sxs-lookup"><span data-stu-id="665af-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="665af-157">它可以设置环境变量的格式，使其能够在 Windows 和 WSL 中正常运行。</span><span class="sxs-lookup"><span data-stu-id="665af-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="665af-158">`WSLENV` 中的四个标志可以影响该环境变量的转换方式。</span><span class="sxs-lookup"><span data-stu-id="665af-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="665af-159">`WSLENV` 标志：</span><span class="sxs-lookup"><span data-stu-id="665af-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="665af-160">`/p` - 在 WSL/Linux 样式路径与 Win32 路径之间转换路径。</span><span class="sxs-lookup"><span data-stu-id="665af-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="665af-161">`/l` - 指示环境变量是路径列表。</span><span class="sxs-lookup"><span data-stu-id="665af-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="665af-162">`/u` - 指示仅当从 Win32 运行 WSL 时，才应包含此环境变量。</span><span class="sxs-lookup"><span data-stu-id="665af-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="665af-163">`/w` - 指示仅当从 WSL 运行 Win32 时，才应包含此环境变量。</span><span class="sxs-lookup"><span data-stu-id="665af-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="665af-164">可按需组合标志。</span><span class="sxs-lookup"><span data-stu-id="665af-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="665af-165">禁用互操作</span><span class="sxs-lookup"><span data-stu-id="665af-165">Disable Interop</span></span>

<span data-ttu-id="665af-166">用户可以使用 root 身份运行以下命令，禁用针对单个 WSL 会话运行 Windows 二进制文件的功能。</span><span class="sxs-lookup"><span data-stu-id="665af-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="665af-167">若要重新启用 Windows 二进制文件，请退出所有 WSL 会话并重新运行 bash.exe，或者以 root 身份运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="665af-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="665af-168">每次切换 WSL 会话后，禁用互操作的结果不会持久保留 -- 启动新会话后，会再次启用互操作。</span><span class="sxs-lookup"><span data-stu-id="665af-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="665af-169">创意者更新和周年更新</span><span class="sxs-lookup"><span data-stu-id="665af-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="665af-170">尽管 Fall Creators Update 以前的互操作体验与近来的互操作体验类似，但它们存在很多重大差别。</span><span class="sxs-lookup"><span data-stu-id="665af-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="665af-171">总结：</span><span class="sxs-lookup"><span data-stu-id="665af-171">To summarize:</span></span>

* <span data-ttu-id="665af-172">`bash.exe` 已弃用，现已由 `wsl.exe` 取代。</span><span class="sxs-lookup"><span data-stu-id="665af-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="665af-173">在 `wsl.exe` 中不需要指定用于运行单个命令的 `-c` 选项。</span><span class="sxs-lookup"><span data-stu-id="665af-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="665af-174">Windows 路径包含在 WSL `$PATH` 中</span><span class="sxs-lookup"><span data-stu-id="665af-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="665af-175">禁用互操作的过程未有变化。</span><span class="sxs-lookup"><span data-stu-id="665af-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="665af-176">从 Windows 命令行调用 WSL</span><span class="sxs-lookup"><span data-stu-id="665af-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="665af-177">可以从 Windows 命令提示符或 PowerShell 调用 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="665af-178">以这种方式调用的二进制文件具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="665af-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="665af-179">使用 CMD 或 PowerShell 提示符中提到的同一工作目录。</span><span class="sxs-lookup"><span data-stu-id="665af-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="665af-180">以 WSL 默认用户的身份运行。</span><span class="sxs-lookup"><span data-stu-id="665af-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="665af-181">拥有与调用方进程和终端相同的 Windows 管理权限。</span><span class="sxs-lookup"><span data-stu-id="665af-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="665af-182">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="665af-183">以这种方式调用的 Linux 命令的处理方式与任何其他 Windows 应用程序类似。</span><span class="sxs-lookup"><span data-stu-id="665af-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="665af-184">可按预期方式执行输入、管道处理和文件重定向等操作。</span><span class="sxs-lookup"><span data-stu-id="665af-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="665af-185">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-185">Examples:</span></span>

```console
C:\temp>bash -c "sudo apt-get update"
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

```console
C:\temp> bash -c "ls -la" | findstr foo
C:\temp> dir | bash -c "grep foo"
C:\temp> bash -c "ls -la" > out.txt
```

<span data-ttu-id="665af-186">传入 `bash -c` 的 WSL 命令将按原样转发到 WSL 进程。</span><span class="sxs-lookup"><span data-stu-id="665af-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="665af-187">必须以 WSL 格式指定文件路径，并且必须谨慎转义相关字符。</span><span class="sxs-lookup"><span data-stu-id="665af-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="665af-188">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="665af-189">从 WSL 调用 Windows 二进制文件</span><span class="sxs-lookup"><span data-stu-id="665af-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="665af-190">适用于 Linux 的 Windows 子系统可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="665af-191">以这种方式运行的应用程序具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="665af-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="665af-192">按 WSL 命令提示保留工作目录，但下面所述的情况除外。</span><span class="sxs-lookup"><span data-stu-id="665af-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="665af-193">拥有与 `bash.exe` 进程相同的权限。</span><span class="sxs-lookup"><span data-stu-id="665af-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="665af-194">以活动 Windows 用户的身份运行。</span><span class="sxs-lookup"><span data-stu-id="665af-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="665af-195">显示在 Windows 任务管理器中，就如同直接从 CMD 提示符执行的一样。</span><span class="sxs-lookup"><span data-stu-id="665af-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="665af-196">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="665af-197">在 WSL 中，这些可执行文件的处理方式类似于本机 Linux 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="665af-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="665af-198">这意味着，可按预期方式将目录添加到 Linux 路径，以及在命令之间进行管道处理。</span><span class="sxs-lookup"><span data-stu-id="665af-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="665af-199">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="665af-200">Windows 二进制文件必须包含文件扩展名，匹配文件大小写，并且可执行。</span><span class="sxs-lookup"><span data-stu-id="665af-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="665af-201">不可执行文件（包括批处理脚本）和 `dir` 等命令可与 `/mnt/c/Windows/System32/cmd.exe /C` 命令一起运行。</span><span class="sxs-lookup"><span data-stu-id="665af-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="665af-202">示例：</span><span class="sxs-lookup"><span data-stu-id="665af-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="665af-203">参数将按原样传递到 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="665af-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="665af-204">例如，以下命令将在 `C:\temp\foo.txt` 中打开 `notepad.exe`：</span><span class="sxs-lookup"><span data-stu-id="665af-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="665af-205">不支持使用 Windows 应用程序修改位于 VolFs 中的文件（不是在 `/mnt/<x>` 下的文件）。</span><span class="sxs-lookup"><span data-stu-id="665af-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="665af-206">默认情况下，WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录，但如果工作目录位于 VolFs 中，则会回退到实例创建目录。</span><span class="sxs-lookup"><span data-stu-id="665af-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="665af-207">例如，`bash.exe` 最初是从 `C:\temp` 启动的，而当前 WSL 目录已更改为用户的主目录。</span><span class="sxs-lookup"><span data-stu-id="665af-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="665af-208">如果从用户的主目录调用 `notepad.exe`，WSL 将自动还原到 `C:\temp`（notepad.exe 工作目录）：</span><span class="sxs-lookup"><span data-stu-id="665af-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

``` BASH
C:\temp> bash
/mnt/c/temp/$ cd ~
~$ notepad.exe foo.txt
~$ ls | grep foo.txt
~$ exit
exit

C:\temp> dir | findstr foo.txt
09/27/2016  02:15 PM                14 foo.txt
```
