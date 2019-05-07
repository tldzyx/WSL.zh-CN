---
title: Windows 与 Linux 的互操作性
description: 介绍在 Windows 子系统上运行适用于 Linux 的 Linux 分发版 Windows 的互操作性。
author: scooley
ms.author: scooley
ms.date: 12/20/2017
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.openlocfilehash: 5dcfe0987ecb6615fbe1ab67d178679ac6ad9317
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063245"
---
# <a name="windows-subsystem-for-linux-interoperability-with-windows"></a><span data-ttu-id="8eb09-103">Windows 与 Linux 互操作性的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="8eb09-103">Windows Subsystem for Linux interoperability with Windows</span></span>

> <span data-ttu-id="8eb09-104">**更新的 Fall Creators Update。**</span><span class="sxs-lookup"><span data-stu-id="8eb09-104">**Updated for Fall Creators Update.**</span></span>  
<span data-ttu-id="8eb09-105">如果您运行创意者更新或周年更新，请跳转到[创建者/周年更新部分](interop.md#creators-update-and-anniversary-update)。</span><span class="sxs-lookup"><span data-stu-id="8eb09-105">If you're running Creators Update or Anniversary Update, jump to the [Creators/Anniversary Update section](interop.md#creators-update-and-anniversary-update).</span></span>

<span data-ttu-id="8eb09-106">Windows 子系统用于 Linux (WSL) 在不断改进 Windows 和 Linux 之间的集成。</span><span class="sxs-lookup"><span data-stu-id="8eb09-106">The Windows Subsystem for Linux (WSL) is continuously improving integration between Windows and Linux.</span></span>  <span data-ttu-id="8eb09-107">你可以：</span><span class="sxs-lookup"><span data-stu-id="8eb09-107">You can:</span></span>

1. <span data-ttu-id="8eb09-108">调用从 Linux 控制台的 Windows 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-108">Invoke Windows binaries from the Linux console.</span></span>
1. <span data-ttu-id="8eb09-109">调用 Windows 控制台中的 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-109">Invoke Linux binaries from a Windows console.</span></span>
1. <span data-ttu-id="8eb09-110">**Windows 预览体验成员版本 17063 +** 共享 Linux 和 Windows 之间的环境变量。</span><span class="sxs-lookup"><span data-stu-id="8eb09-110">**Windows Insiders Builds 17063+** Share environment variables between Linux and Windows.</span></span>

<span data-ttu-id="8eb09-111">这提供了 Windows 和 WSL 之间无缝的体验。</span><span class="sxs-lookup"><span data-stu-id="8eb09-111">This delivers a seamless experience between Windows and WSL.</span></span>  <span data-ttu-id="8eb09-112">技术详细信息位于[WSL 博客](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/)。</span><span class="sxs-lookup"><span data-stu-id="8eb09-112">Technical details are on the [WSL blog](https://blogs.msdn.microsoft.com/wsl/2016/10/19/windows-and-ubuntu-interoperability/).</span></span>

## <a name="run-linux-tools-from-a-windows-command-line"></a><span data-ttu-id="8eb09-113">从 Windows 命令行运行 Linux 工具</span><span class="sxs-lookup"><span data-stu-id="8eb09-113">Run Linux tools from a Windows command line</span></span>

<span data-ttu-id="8eb09-114">从 Windows 命令提示符 （CMD 或 PowerShell） 使用运行 Linux 的二进制文件`wsl.exe <command>`。</span><span class="sxs-lookup"><span data-stu-id="8eb09-114">Run Linux binaries from the Windows Command Prompt (CMD or PowerShell) using `wsl.exe <command>`.</span></span>

<span data-ttu-id="8eb09-115">在这种方式中调用的二进制文件：</span><span class="sxs-lookup"><span data-stu-id="8eb09-115">Binaries invoked in this way:</span></span>

1. <span data-ttu-id="8eb09-116">为当前的 CMD 或 PowerShell 提示符下使用相同的工作目录。</span><span class="sxs-lookup"><span data-stu-id="8eb09-116">Use the same working directory as the current CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="8eb09-117">WSL 默认用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-117">Run as the WSL default user.</span></span>
1. <span data-ttu-id="8eb09-118">具有与调用进程和终端相同的 Windows 管理权限。</span><span class="sxs-lookup"><span data-stu-id="8eb09-118">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="8eb09-119">例如：</span><span class="sxs-lookup"><span data-stu-id="8eb09-119">For example:</span></span>

```console
C:\temp> wsl ls -la
<- contents of C:\temp ->
```

<span data-ttu-id="8eb09-120">以下 Linux 命令`wsl.exe`处理就像在 WSL 中运行任何命令处理。</span><span class="sxs-lookup"><span data-stu-id="8eb09-120">The Linux command following `wsl.exe` is handled like any command run in WSL.</span></span>  <span data-ttu-id="8eb09-121">Sudo、 管道和文件重定向等工作。</span><span class="sxs-lookup"><span data-stu-id="8eb09-121">Things such as sudo, piping, and file redirection work.</span></span>

<span data-ttu-id="8eb09-122">使用 sudo 的示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-122">Example using sudo:</span></span>

```console
C:\temp> wsl sudo apt-get update
[sudo] password for username:
Hit:1 https://archive.ubuntu.com/ubuntu xenial InRelease
Get:2 https://security.ubuntu.com/ubuntu xenial-security InRelease [94.5 kB]
```

<span data-ttu-id="8eb09-123">混合使用 WSL 和 Windows 命令的示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-123">Examples mixing WSL and Windows commands:</span></span>

```console
C:\temp> wsl ls -la | findstr "foo"
-rwxrwxrwx 1 root root     14 Sep 27 14:26 foo.bat

C:\temp> dir | wsl grep foo
09/27/2016  02:26 PM                14 foo.bat

C:\temp> wsl ls -la > out.txt
```

<span data-ttu-id="8eb09-124">这些命令传递到`wsl.exe`转发到 WSL 过程无需修改即可。</span><span class="sxs-lookup"><span data-stu-id="8eb09-124">The commands passed into `wsl.exe` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="8eb09-125">必须在 WSL 格式指定文件路径。</span><span class="sxs-lookup"><span data-stu-id="8eb09-125">File paths must be specified in the WSL format.</span></span>

<span data-ttu-id="8eb09-126">路径示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-126">Example with paths:</span></span>

```console
C:\temp> wsl ls -la /proc/cpuinfo
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> wsl ls -la "/mnt/c/Program Files"
<- contents of C:\Program Files ->
```

## <a name="run-windows-tools-from-wsl"></a><span data-ttu-id="8eb09-127">WSL 从运行 Windows 工具</span><span class="sxs-lookup"><span data-stu-id="8eb09-127">Run Windows tools from WSL</span></span>

<span data-ttu-id="8eb09-128">WSL 可以调用 Windows 二进制文件直接从 WSL 命令行使用`[binary name].exe`。</span><span class="sxs-lookup"><span data-stu-id="8eb09-128">WSL can invoke Windows binaries directly from the WSL command line using `[binary name].exe`.</span></span>  <span data-ttu-id="8eb09-129">例如，`notepad.exe`。</span><span class="sxs-lookup"><span data-stu-id="8eb09-129">For example, `notepad.exe`.</span></span>  <span data-ttu-id="8eb09-130">若要使 Windows 可执行文件更轻松地运行，Windows 路径包括在 Linux `$PATH` Fall Creators Update 中。</span><span class="sxs-lookup"><span data-stu-id="8eb09-130">To make Windows executables easier to run, Windows path is included in the Linux `$PATH` in Fall Creators Update.</span></span>

<span data-ttu-id="8eb09-131">此方式运行的应用程序具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="8eb09-131">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="8eb09-132">保留工作目录为 WSL 命令提示符 （大多数情况下-异常如下说明）。</span><span class="sxs-lookup"><span data-stu-id="8eb09-132">Retain the working directory as the WSL command prompt (for the most part -- exceptions are explained below).</span></span>
1. <span data-ttu-id="8eb09-133">具有相同的权限权限作为 WSL 进程。</span><span class="sxs-lookup"><span data-stu-id="8eb09-133">Have the same permission rights as the WSL process.</span></span>
1. <span data-ttu-id="8eb09-134">作为活动的 Windows 用户运行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-134">Run as the active Windows user.</span></span>
1. <span data-ttu-id="8eb09-135">Windows 任务管理器中显示像直接在命令提示符处执行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-135">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="8eb09-136">例如：</span><span class="sxs-lookup"><span data-stu-id="8eb09-136">Example:</span></span>

``` BASH
$ notepad.exe
```

<span data-ttu-id="8eb09-137">为本机 Linux 可执行文件-通过管道传递重定向，并按预期方式甚至后台处理的工作类似方式处理在 WSL 中运行的 Windows 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-137">Windows executables run in WSL are handled similarly to native Linux executables -- piping, redirects, and even backgrounding work as expected.</span></span>

<span data-ttu-id="8eb09-138">使用管道的示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-138">Examples using pipes:</span></span>

``` BASH
$ ipconfig.exe | grep IPv4 | cut -d: -f2
172.21.240.1
10.159.21.24
```

<span data-ttu-id="8eb09-139">使用混合的 Windows 和 WSL 命令的示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-139">Example using mixed Windows and WSL commands:</span></span>

``` BASH
$ ls -la | findstr.exe foo.txt

$ cmd.exe /c dir
<- contents of C:\ ->
```

<span data-ttu-id="8eb09-140">Windows 二进制文件必须包括文件扩展名、 匹配文件的情况下，并可执行文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-140">Windows binaries must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="8eb09-141">非可执行文件包括批处理脚本。</span><span class="sxs-lookup"><span data-stu-id="8eb09-141">Non-executables including batch scripts.</span></span>  <span data-ttu-id="8eb09-142">CMD 本机命令，如`dir`可以使用运行`cmd.exe /C`命令。</span><span class="sxs-lookup"><span data-stu-id="8eb09-142">CMD native commands like `dir` can be run with `cmd.exe /C` command.</span></span>

<span data-ttu-id="8eb09-143">示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-143">Examples:</span></span>

``` BASH
$ cmd.exe /C dir
<- contents of C:\ ->

$ PING.EXE www.microsoft.com
Pinging e1863.dspb.akamaiedge.net [2600:1409:a:5a2::747] with 32 bytes of data:
Reply from 2600:1409:a:5a2::747: time=2ms
```

<span data-ttu-id="8eb09-144">参数传递给 Windows 二进制以未修改形式。</span><span class="sxs-lookup"><span data-stu-id="8eb09-144">Parameters are passed to the Windows binary unmodified.</span></span>

<span data-ttu-id="8eb09-145">例如，以下命令将打开`C:\temp\foo.txt`在`notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="8eb09-145">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="8eb09-146">修改位于 VolFs 上的文件 (文件不在`/mnt/<x>`) 与 Windows 应用程序在 WSL 中的不支持。</span><span class="sxs-lookup"><span data-stu-id="8eb09-146">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application in WSL is not supported.</span></span>

<span data-ttu-id="8eb09-147">默认情况下，WSL 尝试保留的工作目录的 Windows 二进制数作为当前 WSL 目录，但将回退到的实例创建目录的工作目录是否在 VolFs。</span><span class="sxs-lookup"><span data-stu-id="8eb09-147">By default, WSL tries to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="8eb09-148">作为示例;`wsl.exe`从最初启动`C:\temp`而当前 WSL 目录更改为用户的主页。</span><span class="sxs-lookup"><span data-stu-id="8eb09-148">As an example; `wsl.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="8eb09-149">当`notepad.exe`称为用户的主目录中，从 WSL 将自动恢复为`C:\temp`为 notepad.exe 的工作目录：</span><span class="sxs-lookup"><span data-stu-id="8eb09-149">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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

## <a name="share-environment-variables-between-windows-and-wsl"></a><span data-ttu-id="8eb09-150">Windows 和 WSL 之间共享环境变量</span><span class="sxs-lookup"><span data-stu-id="8eb09-150">Share environment variables between Windows and WSL</span></span>

> <span data-ttu-id="8eb09-151">在 Windows 预览体验成员版本 17063 及更高版本中可用。</span><span class="sxs-lookup"><span data-stu-id="8eb09-151">Available in Windows Insider builds 17063 and later.</span></span>

<span data-ttu-id="8eb09-152">在 17063 之前, 仅 Windows 环境变量可访问 WSL 是`PATH`（因此，可以启动从 WSL 下的 Win32 可执行文件）。</span><span class="sxs-lookup"><span data-stu-id="8eb09-152">Prior to 17063, only Windows environment variable that WSL could access was `PATH` (so you could launch Win32 executables from under WSL).</span></span>

<span data-ttu-id="8eb09-153">从 17063，WSL 和 Windows 共享`WSLENV`，创建桥接在 WSL 上运行的 Windows 和 Linux 发行版的特殊环境变量。</span><span class="sxs-lookup"><span data-stu-id="8eb09-153">Starting in 17063, WSL and Windows share `WSLENV`, a special environment variable created to bridge Windows and Linux distros running on WSL.</span></span>

<span data-ttu-id="8eb09-154">属性的`WSLENV`:</span><span class="sxs-lookup"><span data-stu-id="8eb09-154">Properties of `WSLENV`:</span></span>

* <span data-ttu-id="8eb09-155">共享;它在 Windows 和 WSL 环境中存在。</span><span class="sxs-lookup"><span data-stu-id="8eb09-155">It is shared; it exists in both Windows and WSL environments.</span></span>
* <span data-ttu-id="8eb09-156">它是用于 Windows 和 WSL 之间共享的环境变量的列表。</span><span class="sxs-lookup"><span data-stu-id="8eb09-156">It is a list of environment variables to share between Windows and WSL.</span></span>
* <span data-ttu-id="8eb09-157">它可以设置环境变量中正常运行 Windows 和 WSL 的格式。</span><span class="sxs-lookup"><span data-stu-id="8eb09-157">It can format environment variables to work well in Windows and WSL.</span></span>

<span data-ttu-id="8eb09-158">中提供了四个标志`WSLENV`来影响如何转换该环境变量。</span><span class="sxs-lookup"><span data-stu-id="8eb09-158">There are four flags available in `WSLENV` to influence how that environment variable is translated.</span></span>

<span data-ttu-id="8eb09-159">`WSLENV` 标志：</span><span class="sxs-lookup"><span data-stu-id="8eb09-159">`WSLENV` flags:</span></span>

* <span data-ttu-id="8eb09-160">`/p` -将转换 WSL/Linux 样式的路径和 Win32 路径之间的路径。</span><span class="sxs-lookup"><span data-stu-id="8eb09-160">`/p` - translates the path between WSL/Linux style paths and Win32 paths.</span></span>
* <span data-ttu-id="8eb09-161">`/l` -指示环境变量是路径的列表。</span><span class="sxs-lookup"><span data-stu-id="8eb09-161">`/l` - indicates the environment variable is a list of paths.</span></span>
* <span data-ttu-id="8eb09-162">`/u` -指示从 Win32 运行 WSL 时只应包含此环境变量。</span><span class="sxs-lookup"><span data-stu-id="8eb09-162">`/u` - indicates that this environment variable should only be included when running WSL from Win32.</span></span>
* <span data-ttu-id="8eb09-163">`/w` -指示从 WSL 运行 Win32 时只应包含此环境变量。</span><span class="sxs-lookup"><span data-stu-id="8eb09-163">`/w` - indicates that this environment variable should only be included when running Win32 from WSL.</span></span>

<span data-ttu-id="8eb09-164">根据需要可以结合标志。</span><span class="sxs-lookup"><span data-stu-id="8eb09-164">Flags can be combined as needed.</span></span>

## <a name="disable-interop"></a><span data-ttu-id="8eb09-165">禁用互操作</span><span class="sxs-lookup"><span data-stu-id="8eb09-165">Disable Interop</span></span>

<span data-ttu-id="8eb09-166">用户可能会禁止以根身份运行以下命令为单一的 WSL 会话中运行 Windows 的二进制文件：</span><span class="sxs-lookup"><span data-stu-id="8eb09-166">Users may disable the ability to run Windows binaries for a single WSL session by running the following command as root:</span></span>

``` BASH
$ echo 0 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="8eb09-167">若要重新启用 Windows 二进制文件退出所有 WSL 会话并重新运行 bash.exe 或以 root 身份运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="8eb09-167">To reenable Windows binaries either exit all WSL sessions and re-run bash.exe or run the following command as root:</span></span>

``` BASH
$ echo 1 > /proc/sys/fs/binfmt_misc/WSLInterop
```

<span data-ttu-id="8eb09-168">禁用互操作将不会保留 WSL 会话之间--启动新会话时将再次启用互操作。</span><span class="sxs-lookup"><span data-stu-id="8eb09-168">Disabling interop will not persist between WSL sessions -- interop will be enabled again when a new session is launched.</span></span>

## <a name="creators-update-and-anniversary-update"></a><span data-ttu-id="8eb09-169">创意者更新及周年更新</span><span class="sxs-lookup"><span data-stu-id="8eb09-169">Creators Update and Anniversary Update</span></span>

<span data-ttu-id="8eb09-170">互操作体验预 Fall Creators Update 是类似于较新的互操作体验，尽管有一些主要差异 handfull。</span><span class="sxs-lookup"><span data-stu-id="8eb09-170">While the interop experience pre-Fall Creators Update is similar to more recent interop experiences, there are a handfull of major differences.</span></span>

<span data-ttu-id="8eb09-171">总结：</span><span class="sxs-lookup"><span data-stu-id="8eb09-171">To summarize:</span></span>

* <span data-ttu-id="8eb09-172">`bash.exe` 已弃用，替换为`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="8eb09-172">`bash.exe` has been deprecated and replaced with `wsl.exe`.</span></span>
* <span data-ttu-id="8eb09-173">`-c` 选项为运行单个命令不需要与`wsl.exe`。</span><span class="sxs-lookup"><span data-stu-id="8eb09-173">`-c` option for running a single command isn't needed with `wsl.exe`.</span></span>
* <span data-ttu-id="8eb09-174">Windows 路径包括在 WSL `$PATH`</span><span class="sxs-lookup"><span data-stu-id="8eb09-174">Windows path is included in the WSL `$PATH`</span></span>

<span data-ttu-id="8eb09-175">禁用互操作的过程保持不变。</span><span class="sxs-lookup"><span data-stu-id="8eb09-175">The process for disabling interop is unchanged.</span></span>

### <a name="invoking-wsl-from-the-windows-command-line"></a><span data-ttu-id="8eb09-176">从 Windows 命令行调用 WSL</span><span class="sxs-lookup"><span data-stu-id="8eb09-176">Invoking WSL from the Windows Command Line</span></span>

<span data-ttu-id="8eb09-177">可以从 Windows 命令提示符处或从 PowerShell 调用 Linux 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-177">Linux binaries can be invoked from the Windows Command Prompt or from PowerShell.</span></span>  <span data-ttu-id="8eb09-178">在这种方式中调用的二进制文件具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="8eb09-178">Binaries invoked in this way have the following properties:</span></span>

1. <span data-ttu-id="8eb09-179">为 CMD 或 PowerShell 提示符使用相同的工作目录。</span><span class="sxs-lookup"><span data-stu-id="8eb09-179">Use the same working directory as the CMD or PowerShell prompt.</span></span>
1. <span data-ttu-id="8eb09-180">WSL 默认用户身份运行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-180">Run as the WSL default user.</span></span>
1. <span data-ttu-id="8eb09-181">具有与调用进程和终端相同的 Windows 管理权限。</span><span class="sxs-lookup"><span data-stu-id="8eb09-181">Have the same Windows administrative rights as the calling process and terminal.</span></span>

<span data-ttu-id="8eb09-182">例如：</span><span class="sxs-lookup"><span data-stu-id="8eb09-182">Example:</span></span>

```console
C:\temp> bash -c "ls -la"
```

<span data-ttu-id="8eb09-183">Linux 命令，在这种方式中调用任何其他 Windows 应用程序一样处理。</span><span class="sxs-lookup"><span data-stu-id="8eb09-183">Linux commands called in this way are handled like any other Windows application.</span></span>  <span data-ttu-id="8eb09-184">例如输入、 管道和文件重定向操作按预期方式工作。</span><span class="sxs-lookup"><span data-stu-id="8eb09-184">Things such as input, piping, and file redirection work as expected.</span></span>

<span data-ttu-id="8eb09-185">示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-185">Examples:</span></span>

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

<span data-ttu-id="8eb09-186">WSL 命令传递到`bash -c`转发到 WSL 过程无需修改即可。</span><span class="sxs-lookup"><span data-stu-id="8eb09-186">The WSL commands passed into `bash -c` are forwarded to the WSL process without modification.</span></span>  <span data-ttu-id="8eb09-187">必须在 WSL 格式指定文件路径，并且必须特别注意相关字符进行转义。</span><span class="sxs-lookup"><span data-stu-id="8eb09-187">File paths must be specified in the WSL format and care must be taken to escape relevant characters.</span></span> <span data-ttu-id="8eb09-188">例如：</span><span class="sxs-lookup"><span data-stu-id="8eb09-188">Example:</span></span>

```console
C:\temp> bash -c "ls -la /proc/cpuinfo"
-r--r--r-- 1 root root 0 Sep 28 11:28 /proc/cpuinfo

C:\temp> bash -c "ls -la \"/mnt/c/Program Files\""
<- contents of C:\Program Files ->
```

### <a name="invoking-windows-binaries-from-wsl"></a><span data-ttu-id="8eb09-189">调用 Windows 二进制文件从 WSL</span><span class="sxs-lookup"><span data-stu-id="8eb09-189">Invoking Windows binaries from WSL</span></span>

<span data-ttu-id="8eb09-190">适用于 Linux 的 Windows 子系统可以调用 Windows 二进制文件直接从 WSL 命令行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-190">The Windows Subsystem for Linux can invoke Windows binaries directly from the WSL command line.</span></span>  <span data-ttu-id="8eb09-191">此方式运行的应用程序具有以下属性：</span><span class="sxs-lookup"><span data-stu-id="8eb09-191">Applications run this way have the following properties:</span></span>

1. <span data-ttu-id="8eb09-192">如下所述的方案中除 WSL 命令提示符下作为保留的工作目录。</span><span class="sxs-lookup"><span data-stu-id="8eb09-192">Retain the working directory as the WSL command prompt except in the scenario explained below.</span></span>
1. <span data-ttu-id="8eb09-193">具有相同的权限权限`bash.exe`过程。</span><span class="sxs-lookup"><span data-stu-id="8eb09-193">Have the same permission rights as the `bash.exe` process.</span></span> 
1. <span data-ttu-id="8eb09-194">作为活动的 Windows 用户运行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-194">Run as the active Windows user.</span></span>
1. <span data-ttu-id="8eb09-195">Windows 任务管理器中显示像直接在命令提示符处执行。</span><span class="sxs-lookup"><span data-stu-id="8eb09-195">Appear in the Windows Task Manager as if directly executed from the CMD prompt.</span></span>

<span data-ttu-id="8eb09-196">例如：</span><span class="sxs-lookup"><span data-stu-id="8eb09-196">Example:</span></span>

``` BASH
$ /mnt/c/Windows/System32/notepad.exe
```

<span data-ttu-id="8eb09-197">在 WSL，这些可执行文件的处理类似于本机 Linux 可执行文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-197">In WSL, these executables are handled similar to native Linux executables.</span></span>  <span data-ttu-id="8eb09-198">这意味着将目录添加到 Linux 路径并通过管道将命令的工作原理之间按预期方式。</span><span class="sxs-lookup"><span data-stu-id="8eb09-198">This means adding directories to the Linux path and piping between commands works as expected.</span></span>  <span data-ttu-id="8eb09-199">示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-199">Examples:</span></span>

``` BASH
$ export PATH=$PATH:/mnt/c/Windows/System32
$ notepad.exe
$ ipconfig.exe | grep IPv4 | cut -d: -f2
$ ls -la | findstr.exe foo.txt
$ cmd.exe /c dir
```

<span data-ttu-id="8eb09-200">Windows 二进制文件必须包括文件扩展名、 匹配文件的情况下，并可执行文件。</span><span class="sxs-lookup"><span data-stu-id="8eb09-200">The Windows binary must include the file extension, match the file case, and be executable.</span></span>  <span data-ttu-id="8eb09-201">非可执行文件包括批处理脚本和命令等`dir`可以使用运行`/mnt/c/Windows/System32/cmd.exe /C`命令。</span><span class="sxs-lookup"><span data-stu-id="8eb09-201">Non-executables including batch scripts and command like `dir` can be run with `/mnt/c/Windows/System32/cmd.exe /C` command.</span></span>

<span data-ttu-id="8eb09-202">示例：</span><span class="sxs-lookup"><span data-stu-id="8eb09-202">Examples:</span></span>

``` BASH
$ /mnt/c/Windows/System32/cmd.exe /C dir
$ /mnt/c/Windows/System32/PING.EXE www.microsoft.com
```

<span data-ttu-id="8eb09-203">参数传递给 Windows 二进制以未修改形式。</span><span class="sxs-lookup"><span data-stu-id="8eb09-203">Parameters are passed to the Windows binary unmodified.</span></span>  

<span data-ttu-id="8eb09-204">例如，以下命令将打开`C:\temp\foo.txt`在`notepad.exe`:</span><span class="sxs-lookup"><span data-stu-id="8eb09-204">As an example, the following commands will open `C:\temp\foo.txt` in `notepad.exe`:</span></span>

``` BASH
$ notepad.exe "C:\temp\foo.txt"
$ notepad.exe C:\\temp\\foo.txt
```

<span data-ttu-id="8eb09-205">修改位于 VolFs 上的文件 (文件不在`/mnt/<x>`) 与 Windows 应用程序不支持。</span><span class="sxs-lookup"><span data-stu-id="8eb09-205">Modifying files located on VolFs (files not under `/mnt/<x>`) with a Windows application is not supported.</span></span>  <span data-ttu-id="8eb09-206">默认情况下，WSL 尝试保留的工作目录的 Windows 二进制数作为当前 WSL 目录，但将回退到的实例创建目录的工作目录是否在 VolFs。</span><span class="sxs-lookup"><span data-stu-id="8eb09-206">By default, WSL attempts to keep the working directory of the Windows binary as the current WSL directory, but will fall back on the instance creation directory if the working directory is on VolFs.</span></span>

<span data-ttu-id="8eb09-207">作为示例;`bash.exe`从最初启动`C:\temp`而当前 WSL 目录更改为用户的主页。</span><span class="sxs-lookup"><span data-stu-id="8eb09-207">As an example; `bash.exe` is initially launched from `C:\temp` and the current WSL directory is changed to the user’s home.</span></span>  <span data-ttu-id="8eb09-208">当`notepad.exe`称为用户的主目录中，从 WSL 将自动恢复为`C:\temp`为 notepad.exe 的工作目录：</span><span class="sxs-lookup"><span data-stu-id="8eb09-208">When `notepad.exe` is called from the user’s home directory, WSL automatically reverts to `C:\temp` as the notepad.exe working directory:</span></span>

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
