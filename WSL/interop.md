---
title: Windows 与 Linux 的互操作性
description: 介绍 Windows 在适用于 Linux 的 Windows 子系统上运行的 Linux 分发的互操作性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 3f3df3337ece75d7af77313f5fc55eb4e18e31cb
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122732"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="dfcfd-103">适用于 Linux 的 windows 子系统与 Windows 的互操作性</span><span class="sxs-lookup"><span data-stu-id="dfcfd-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="dfcfd-104">**更新了秋季创意者更新。**</span><span class="sxs-lookup"><span data-stu-id="dfcfd-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="dfcfd-105">如果正在运行创建者更新或周年周年更新, 请跳转到 "[创建者/周年更新" 部分](interop.md#creators-update-and-anniversary-update)。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="dfcfd-106">适用于 Linux 的 Windows 子系统 (WSL) 不断改进 Windows 和 Linux 的集成。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="dfcfd-107">你可以：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-107">You can:</span></span>

1. <span data-ttu-id="dfcfd-108">从 Linux 控制台调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="dfcfd-109">从 Windows 控制台调用 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="dfcfd-110">**Windows 预览体验内部版本 17063 +** 在 Linux 和 Windows 之间共享环境变量。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="dfcfd-111">这在 Windows 和 WSL 之间提供了无缝体验。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="dfcfd-112">[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)上的技术详细信息。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="dfcfd-113">从 Windows 命令行运行 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="dfcfd-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="dfcfd-114">使用`wsl.exe <command>`从 Windows 命令提示符 (CMD 或 PowerShell) 运行 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="dfcfd-115">以这种方式调用的二进制文件:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="dfcfd-116">使用与当前 CMD 或 PowerShell 提示符相同的工作目录。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="dfcfd-117">以 WSL 默认用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="dfcfd-118">具有与调用进程和终端相同的 Windows 管理权限。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="dfcfd-119">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="dfcfd-120">以下`wsl.exe` Linux 命令的处理方式类似于在 WSL 中运行的任何命令。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="dfcfd-121">例如, sudo、管道和文件重定向的工作方式。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="dfcfd-122">使用 sudo 的示例:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="dfcfd-123">混合 WSL 和 Windows 命令的示例:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="dfcfd-124">传入的命令`wsl.exe`将在不进行修改的情况下转发到 WSL 进程。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="dfcfd-125">文件路径必须以 WSL 格式指定。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="dfcfd-126">路径示例:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="dfcfd-127">从 WSL 运行 Windows 工具</span><span class="sxs-lookup"><span data-stu-id="dfcfd-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="dfcfd-128">WSL 可以使用`[binary name].exe`从 WSL 命令行直接调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="dfcfd-129">例如， `notepad.exe` 。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="dfcfd-130">为了使 windows 可执行文件更易于运行, windows 路径包含在`$PATH`秋季创意者更新中。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="dfcfd-131">以这种方式运行的应用程序具有以下属性:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="dfcfd-132">将工作目录保留为 WSL 命令提示符 (大多数情况下, 以下说明除外)。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="dfcfd-133">具有与 WSL 进程相同的权限。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="dfcfd-134">以活动 Windows 用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="dfcfd-135">在 Windows 任务管理器中显示, 就像直接从 CMD 提示符执行一样。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="dfcfd-136">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="dfcfd-137">在 WSL 中运行的 Windows 可执行文件的处理方式类似于本机 Linux 可执行文件-管道、重定向, 甚至后台处理按预期工作。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="dfcfd-138">使用管道的示例:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="dfcfd-139">使用混合窗口和 WSL 命令的示例:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="dfcfd-140">Windows 二进制文件必须包含文件扩展名, 与文件大小写匹配, 并可执行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="dfcfd-141">包括批处理脚本的不可执行文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="dfcfd-142">CMD 本机命令 ( `dir`如) 可以通过`cmd.exe /C`命令运行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="dfcfd-143">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="dfcfd-144">参数被传递到未修改的 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="dfcfd-145">例如, 以下命令将在中`C:\temp\foo.txt` `notepad.exe`打开:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="dfcfd-146">不支持在 WSL 中使用 Windows 应用程序`/mnt/<x>`修改位于 VolFs (不受下的文件) 上的文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="dfcfd-147">默认情况下, WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录, 但如果工作目录在 VolFs 上, 则将回退到实例创建目录。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="dfcfd-148">例如,`wsl.exe`最初从`C:\temp`开始, 当前的 WSL 目录更改为用户的主目录。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="dfcfd-149">当`notepad.exe`从用户的主目录调用时, WSL 将自动还原为`C:\temp` notepad.exe 工作目录:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="dfcfd-150">在 Windows 和 WSL 之间共享环境变量</span><span class="sxs-lookup"><span data-stu-id="dfcfd-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="dfcfd-151">在 Windows 有问必答版本17063及更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="dfcfd-152">在17063之前, 只有 WSL 可以访问的 Windows 环境变量是`PATH` (因此, 你可以从 WSL 下启动 Win32 可执行文件)。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="dfcfd-153">从17063、WSL 和 Windows 共享`WSLENV`开始, 创建了一个特殊的环境变量, 用于在 WSL 上运行的 Windows 和 Linux 发行版。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="dfcfd-154">`WSLENV`属性:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="dfcfd-155">它是共享的;它存在于 Windows 和 WSL 环境中。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="dfcfd-156">它是要在 Windows 和 WSL 之间共享的环境变量的列表。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="dfcfd-157">它可以设置环境变量的格式, 以便在 Windows 和 WSL 中正常工作。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="dfcfd-158">中`WSLENV`提供了四个标志来影响如何转换该环境变量。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="dfcfd-159">`WSLENV`随意</span><span class="sxs-lookup"><span data-stu-id="dfcfd-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="dfcfd-160">`/p`-翻译 WSL/Linux 样式路径和 Win32 路径之间的路径。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="dfcfd-161">`/l`-指示环境变量是路径的列表。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="dfcfd-162">`/u`-指示此环境变量只应在从 Win32 运行 WSL 时包括在内。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="dfcfd-163">`/w`-指示此环境变量只应在从 WSL 运行 Win32 时包括在内。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="dfcfd-164">可以根据需要组合标志。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="dfcfd-165">禁用互操作</span><span class="sxs-lookup"><span data-stu-id="dfcfd-165">Disable Interop</span></span>

<span data-ttu-id="dfcfd-166">用户可以通过以 root 身份运行以下命令, 禁止为单个 WSL 会话运行 Windows 二进制文件的功能。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="dfcfd-167">若要重新启用 Windows 二进制文件, 请退出所有 WSL 会话并重新运行 bash, 或以 root 身份运行以下命令:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="dfcfd-168">禁用互操作不会在 WSL 会话之间保留--启动新会话时将再次启用互操作。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="dfcfd-169">创意者更新和周年周年更新</span><span class="sxs-lookup"><span data-stu-id="dfcfd-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="dfcfd-170">尽管互操作体验前期编写者更新类似于最新的互操作体验, 但有很多重大差别。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handful of major differences.</span></span>

<span data-ttu-id="dfcfd-171">总结：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-171">To summarize:</span></span>

* <span data-ttu-id="dfcfd-172">`bash.exe`已弃用并已替换为`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="dfcfd-173">`-c`不需要`wsl.exe`用于运行单个命令的选项。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="dfcfd-174">Windows 路径包含在 WSL 中。`$PATH`</span><span class="sxs-lookup"><span data-stu-id="dfcfd-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="dfcfd-175">禁用互操作的过程保持不变。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="dfcfd-176">从 Windows 命令行调用 WSL</span><span class="sxs-lookup"><span data-stu-id="dfcfd-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="dfcfd-177">可以从 Windows 命令提示符或 PowerShell 调用 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="dfcfd-178">以这种方式调用的二进制文件具有以下属性:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="dfcfd-179">使用与 CMD 或 PowerShell 提示符相同的工作目录。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="dfcfd-180">以 WSL 默认用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="dfcfd-181">具有与调用进程和终端相同的 Windows 管理权限。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="dfcfd-182">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="dfcfd-183">以这种方式调用的 Linux 命令的处理方式与任何其他 Windows 应用程序一样。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="dfcfd-184">输入、管道和文件重定向等功能按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="dfcfd-185">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-185">Examples:</span></span>

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

<span data-ttu-id="dfcfd-186">传递给`bash -c`的 WSL 命令将在不进行修改的情况下转发到 WSL 进程。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="dfcfd-187">文件路径必须以 WSL 格式指定, 必须小心才能转义相关字符。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="dfcfd-188">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="dfcfd-189">从 WSL 调用 Windows 二进制文件</span><span class="sxs-lookup"><span data-stu-id="dfcfd-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="dfcfd-190">适用于 Linux 的 Windows 子系统可以直接从 WSL 命令行调用 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="dfcfd-191">以这种方式运行的应用程序具有以下属性:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="dfcfd-192">除了下面所述的方案之外, 将工作目录保留为 WSL 命令提示符。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="dfcfd-193">与该`bash.exe`进程具有相同的权限权限。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="dfcfd-194">以活动 Windows 用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="dfcfd-195">在 Windows 任务管理器中显示, 就像直接从 CMD 提示符执行一样。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="dfcfd-196">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="dfcfd-197">在 WSL 中, 这些可执行文件的处理方式类似于本机 Linux 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="dfcfd-198">这意味着将目录添加到 Linux 路径, 并按预期方式在命令之间进行管道操作。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="dfcfd-199">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="dfcfd-200">Windows 二进制文件必须包含文件扩展名, 与文件大小写匹配, 并可执行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="dfcfd-201">可执行文件 (包括批处理脚本) 和`dir`命令 (如) `/mnt/c/Windows/System32/cmd.exe /C`可以通过命令运行。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="dfcfd-202">例如：</span><span class="sxs-lookup"><span data-stu-id="dfcfd-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="dfcfd-203">参数被传递到未修改的 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="dfcfd-204">例如, 以下命令将在中`C:\temp\foo.txt` `notepad.exe`打开:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="dfcfd-205">不支持使用 Windows 应用程序修改位于 VolFs `/mnt/<x>`(不在下) 的文件。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="dfcfd-206">默认情况下, WSL 会尝试将 Windows 二进制文件的工作目录保留为当前的 WSL 目录, 但如果工作目录在 VolFs 上, 则将回退到实例创建目录。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="dfcfd-207">例如,`bash.exe`最初从`C:\temp`开始, 当前的 WSL 目录更改为用户的主目录。</span><span class="sxs-lookup"><span data-stu-id="dfcfd-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="dfcfd-208">当`notepad.exe`从用户的主目录调用时, WSL 将自动还原为`C:\temp` notepad.exe 工作目录:</span><span class="sxs-lookup"><span data-stu-id="dfcfd-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
