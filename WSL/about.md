---
title: 了解适用于 Linux 的 Windows 子系统
description: 详细了解适用于 Linux 的 Windows 子系统的工作方式。
keywords: BashOnWindows, bash, wsl, windows, windowssubsystem, gnu, linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 7c8e3b3f7ec13109485d7efa29739dadc8bfacf7
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122672"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="2727c-104">适用于 Linux 的 Windows 子系统文档</span><span class="sxs-lookup"><span data-stu-id="2727c-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="2727c-105">使用适用于 Linux 的 Windows 子系统, 开发人员可运行 GNU/Linux 环境 (包括大多数命令行工具、实用程序和应用程序), 直接在 Windows 上进行修改, 而不会造成虚拟机的系统开销。</span><span class="sxs-lookup"><span data-stu-id="2727c-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="2727c-106">你可以：</span><span class="sxs-lookup"><span data-stu-id="2727c-106">You can:</span></span>

1. <span data-ttu-id="2727c-107">[从 Microsoft Store 中](https://aka.ms/wslstore)选择你最喜爱的 GNU/Linux 分发。</span><span class="sxs-lookup"><span data-stu-id="2727c-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="2727c-108">运行常见命令行的自由软件，如`grep`， `sed`， `awk`，或其他 ELF 64 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="2727c-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="2727c-109">运行 Bash shell 脚本和 GNU/Linux 命令行应用程序，这包括：</span><span class="sxs-lookup"><span data-stu-id="2727c-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="2727c-110">工具: vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="2727c-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="2727c-111">语言：Javascript/node.js、Ruby、Python、C /C++、C# & F#、Rust、Go 等。</span><span class="sxs-lookup"><span data-stu-id="2727c-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="2727c-112">服务：sshd、MySQL、Apache、lighttpd</span><span class="sxs-lookup"><span data-stu-id="2727c-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="2727c-113">使用自己的 GNU/Linux 发行版包管理器安装其他软件。</span><span class="sxs-lookup"><span data-stu-id="2727c-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="2727c-114">使用类似于 Unix 的命令行 shell 调用 Windows 应用程序。</span><span class="sxs-lookup"><span data-stu-id="2727c-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="2727c-115">在 Windows 上调用 GNU/Linux 应用程序。</span><span class="sxs-lookup"><span data-stu-id="2727c-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="2727c-116">入门</span><span class="sxs-lookup"><span data-stu-id="2727c-116">Getting Started</span></span>

* [<span data-ttu-id="2727c-117">在 Windows 10 上安装 Linux</span><span class="sxs-lookup"><span data-stu-id="2727c-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="2727c-118">访问命令引用</span><span class="sxs-lookup"><span data-stu-id="2727c-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="2727c-119">阅读常见问题解答</span><span class="sxs-lookup"><span data-stu-id="2727c-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="2727c-120">团队博客</span><span class="sxs-lookup"><span data-stu-id="2727c-120">Team Blogs</span></span>
*  [<span data-ttu-id="2727c-121">概述使用视频和博客的集合</span><span class="sxs-lookup"><span data-stu-id="2727c-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="2727c-122">[命令行博客](https://blogs.msdn.microsoft.com/commandline/)（活跃）</span><span class="sxs-lookup"><span data-stu-id="2727c-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="2727c-123">[适用于 Linux 的 Windows 子系统博客](https://blogs.msdn.microsoft.com/wsl/)记录</span><span class="sxs-lookup"><span data-stu-id="2727c-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="2727c-124">文章 & 文章</span><span class="sxs-lookup"><span data-stu-id="2727c-124">Posts & Articles</span></span>
* [<span data-ttu-id="2727c-125">在 Windows 上的 Ubuntu 上运行 Bash</span><span class="sxs-lookup"><span data-stu-id="2727c-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="2727c-126">开发人员可以在 Windows 10 上运行 Bash 和 Usermode Ubuntu Linux 二进制文件</span><span class="sxs-lookup"><span data-stu-id="2727c-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="2727c-127">Windows 上的 ubuntu –适用于 Windows 开发人员的 Ubuntu Userspace</span><span class="sxs-lookup"><span data-stu-id="2727c-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="2727c-128">提供反馈</span><span class="sxs-lookup"><span data-stu-id="2727c-128">Provide Feedback</span></span>
* [<span data-ttu-id="2727c-129">GitHub 问题跟踪器</span><span class="sxs-lookup"><span data-stu-id="2727c-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="2727c-130">命令行 UserVoice 门户</span><span class="sxs-lookup"><span data-stu-id="2727c-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
