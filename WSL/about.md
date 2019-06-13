---
title: 了解适用于 Linux 的 Windows 子系统
description: 了解有关适用于 Linux 的 Windows 子系统的工作原理的详细信息。
keywords: BashOnWindows，bash、 wsl、 windows、 windowssubsystem、 gnu、 linux
author: scooley
ms.author: scooley
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: High
ms.openlocfilehash: f2df3c06d6c56aa8bc5a41ea9f075635b70c8685
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040803"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="2d307-104">Linux 文档的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="2d307-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="2d307-105">适用于 Linux 的 Windows 子系统运行-包括大多数命令行工具、 实用工具和应用程序-GNU/Linux 环境的开发人员可以直接在 Windows，以未经修改的无需使用的虚拟机上。</span><span class="sxs-lookup"><span data-stu-id="2d307-105">The Windows Subsystem for Linux lets developers run GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="2d307-106">你可以：</span><span class="sxs-lookup"><span data-stu-id="2d307-106">You can:</span></span>

1. <span data-ttu-id="2d307-107">选择你最喜爱的 GNU/Linux 分发[从 Windows 应用商店](https://aka.ms/wslstore)。</span><span class="sxs-lookup"><span data-stu-id="2d307-107">Choose your favorite GNU/Linux distributions [from the Windows Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="2d307-108">运行常见命令行的免费软件，如`grep`， `sed`， `awk`，或其他 ELF 64 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="2d307-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="2d307-109">运行 Bash shell 脚本和 GNU/Linux 命令行应用程序包括：</span><span class="sxs-lookup"><span data-stu-id="2d307-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="2d307-110">工具： vim、 emacs、 tmux</span><span class="sxs-lookup"><span data-stu-id="2d307-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="2d307-111">语言：Javascript/node.js、 Ruby、 Python、 C /C++， C# & F#、 信任、 转，等等。</span><span class="sxs-lookup"><span data-stu-id="2d307-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="2d307-112">服务： sshd，MySQL、 Apache，lighttpd</span><span class="sxs-lookup"><span data-stu-id="2d307-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="2d307-113">安装其他软件使用自己的 GNU/Linux 分发包管理器。</span><span class="sxs-lookup"><span data-stu-id="2d307-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="2d307-114">调用使用类似于 Unix 的命令行 shell 的 Windows 应用程序。</span><span class="sxs-lookup"><span data-stu-id="2d307-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="2d307-115">调用在 Windows 上的 GNU/Linux 应用程序。</span><span class="sxs-lookup"><span data-stu-id="2d307-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="2d307-116">入门</span><span class="sxs-lookup"><span data-stu-id="2d307-116">Getting Started</span></span>

* [<span data-ttu-id="2d307-117">Windows 10 上安装 Linux</span><span class="sxs-lookup"><span data-stu-id="2d307-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="2d307-118">请访问命令参考</span><span class="sxs-lookup"><span data-stu-id="2d307-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="2d307-119">读取方面的常见问题</span><span class="sxs-lookup"><span data-stu-id="2d307-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="2d307-120">团队博客</span><span class="sxs-lookup"><span data-stu-id="2d307-120">Team Blogs</span></span>
*  [<span data-ttu-id="2d307-121">概述了一系列视频和博客文章</span><span class="sxs-lookup"><span data-stu-id="2d307-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="2d307-122">[命令行博客](https://blogs.msdn.microsoft.com/commandline/)（活动）</span><span class="sxs-lookup"><span data-stu-id="2d307-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="2d307-123">[Linux 博客的 Windows 子系统](https://blogs.msdn.microsoft.com/wsl/)（历史）</span><span class="sxs-lookup"><span data-stu-id="2d307-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="2d307-124">帖子和文章</span><span class="sxs-lookup"><span data-stu-id="2d307-124">Posts & Articles</span></span>
* [<span data-ttu-id="2d307-125">在 Windows 上运行 Ubuntu 上的 Bash</span><span class="sxs-lookup"><span data-stu-id="2d307-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="2d307-126">开发人员可以在 Windows 10 上运行 Bash 和 Usermode Ubuntu Linux 二进制文件</span><span class="sxs-lookup"><span data-stu-id="2d307-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="2d307-127">Ubuntu 上 Windows – Windows 开发人员 Ubuntu 用户空间</span><span class="sxs-lookup"><span data-stu-id="2d307-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="2d307-128">提供反馈</span><span class="sxs-lookup"><span data-stu-id="2d307-128">Provide Feedback</span></span>
* [<span data-ttu-id="2d307-129">GitHub 问题跟踪程序</span><span class="sxs-lookup"><span data-stu-id="2d307-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="2d307-130">命令行 UserVoice 门户</span><span class="sxs-lookup"><span data-stu-id="2d307-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
