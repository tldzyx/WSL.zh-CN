---
title: 了解适用于 Linux 的 Windows 子系统
description: 详细了解适用于 Linux 的 Windows 子系统的工作原理。
keywords: BashOnWindows, bash, wsl, windows, windows 子系统, windowssubsystem, gnu, linux
ms.date: 07/11/2016
ms.topic: article
ms.assetid: 3cefe0db-7616-4848-a2b6-9296746a178b
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 4e63fd186f11545937a4ce0a0fbd6071a4bf268d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269719"
---
# <a name="windows-subsystem-for-linux-documentation"></a><span data-ttu-id="d3b50-104">适用于 Linux 的 Windows 子系统文档</span><span class="sxs-lookup"><span data-stu-id="d3b50-104">Windows Subsystem for Linux Documentation</span></span>

<span data-ttu-id="d3b50-105">适用于 Linux 的 Windows 子系统可让开发人员按原样运行 GNU/Linux 环境 - 包括大多数命令行工具、实用工具和应用程序 - 且不会产生虚拟机开销。</span><span class="sxs-lookup"><span data-stu-id="d3b50-105">The Windows Subsystem for Linux lets developers run a GNU/Linux environment -- including most command-line tools, utilities, and applications -- directly on Windows, unmodified, without the overhead of a virtual machine.</span></span>  

<span data-ttu-id="d3b50-106">你可以：</span><span class="sxs-lookup"><span data-stu-id="d3b50-106">You can:</span></span>

1. <span data-ttu-id="d3b50-107">[在 Microsoft Store](https://aka.ms/wslstore) 中选择你偏好的 GNU/Linux 分发版。</span><span class="sxs-lookup"><span data-stu-id="d3b50-107">Choose your favorite GNU/Linux distributions [from the Microsoft Store](https://aka.ms/wslstore).</span></span>
1. <span data-ttu-id="d3b50-108">运行常用的无命令行软件（例如 `grep`、`sed`、`awk`）或其他 ELF-64 二进制文件。</span><span class="sxs-lookup"><span data-stu-id="d3b50-108">Run common command-line free software such as `grep`, `sed`, `awk`, or other ELF-64 binaries.</span></span> 
1. <span data-ttu-id="d3b50-109">运行 Bash shell 脚本和 GNU/Linux 命令行应用程序，包括：</span><span class="sxs-lookup"><span data-stu-id="d3b50-109">Run Bash shell scripts and GNU/Linux command-line applications including:</span></span>  
    * <span data-ttu-id="d3b50-110">工具：vim、emacs、tmux</span><span class="sxs-lookup"><span data-stu-id="d3b50-110">Tools: vim, emacs, tmux</span></span>
    * <span data-ttu-id="d3b50-111">语言：Javascript/node.js、Ruby、Python、C/C++、 C# 和 F#、Rust、Go 等等</span><span class="sxs-lookup"><span data-stu-id="d3b50-111">Languages: Javascript/node.js, Ruby, Python, C/C++, C# & F#, Rust, Go, etc.</span></span>
    * <span data-ttu-id="d3b50-112">服务：sshd、MySQL、Apache、lighttpd</span><span class="sxs-lookup"><span data-stu-id="d3b50-112">Services: sshd, MySQL, Apache, lighttpd</span></span>
1. <span data-ttu-id="d3b50-113">使用自己的 GNU/Linux 分发包管理器安装其他软件。</span><span class="sxs-lookup"><span data-stu-id="d3b50-113">Install additional software using own GNU/Linux distribution package manager.</span></span>
1. <span data-ttu-id="d3b50-114">使用类似于 Unix 的命令行 shell 调用 Windows 应用程序。</span><span class="sxs-lookup"><span data-stu-id="d3b50-114">Invoke Windows applications using a Unix-like command-line shell.</span></span>
1. <span data-ttu-id="d3b50-115">在 Windows 上调用 GNU/Linux 应用程序。</span><span class="sxs-lookup"><span data-stu-id="d3b50-115">Invoke GNU/Linux applications on Windows.</span></span>

## <a name="getting-started"></a><span data-ttu-id="d3b50-116">入门</span><span class="sxs-lookup"><span data-stu-id="d3b50-116">Getting Started</span></span>

* [<span data-ttu-id="d3b50-117">在 Windows 10 上安装 Linux</span><span class="sxs-lookup"><span data-stu-id="d3b50-117">Install Linux on Windows 10</span></span>](install-win10.md)
* [<span data-ttu-id="d3b50-118">访问命令参考</span><span class="sxs-lookup"><span data-stu-id="d3b50-118">Visit the command reference</span></span>](reference.md)
* [<span data-ttu-id="d3b50-119">阅读常见问题解答</span><span class="sxs-lookup"><span data-stu-id="d3b50-119">Read frequently asked questions</span></span>](faq.md)

## <a name="team-blogs"></a><span data-ttu-id="d3b50-120">团队博客</span><span class="sxs-lookup"><span data-stu-id="d3b50-120">Team Blogs</span></span>
*  [<span data-ttu-id="d3b50-121">概述文章以及一系列视频和博客</span><span class="sxs-lookup"><span data-stu-id="d3b50-121">Overview post with a collection of videos and blogs</span></span>](https://blogs.msdn.microsoft.com/commandline/learn-about-windows-console-and-windows-subsystem-for-linux-wsl/)
* <span data-ttu-id="d3b50-122">[命令行博客](https://blogs.msdn.microsoft.com/commandline/)（适用于现行版本）</span><span class="sxs-lookup"><span data-stu-id="d3b50-122">[Command-Line blog](https://blogs.msdn.microsoft.com/commandline/) (Active)</span></span>
* <span data-ttu-id="d3b50-123">[适用于 Linux 的 Windows 子系统博客](https://blogs.msdn.microsoft.com/wsl/)（适用于传统版本）</span><span class="sxs-lookup"><span data-stu-id="d3b50-123">[Windows Subsystem for Linux Blog](https://blogs.msdn.microsoft.com/wsl/) (Historical)</span></span>

## <a name="posts--articles"></a><span data-ttu-id="d3b50-124">贴子和文章</span><span class="sxs-lookup"><span data-stu-id="d3b50-124">Posts & Articles</span></span>
* [<span data-ttu-id="d3b50-125">运行 Windows 上的 Ubuntu Bash</span><span class="sxs-lookup"><span data-stu-id="d3b50-125">Run Bash on Ubuntu on Windows</span></span>](https://blogs.windows.com/buildingapps/2016/03/30/run-bash-on-ubuntu-on-windows/)
* [<span data-ttu-id="d3b50-126">开发人员可以在 Windows 10 上运行 Bash 和用户模式 Ubuntu Linux 二进制文件</span><span class="sxs-lookup"><span data-stu-id="d3b50-126">Developers Can Run Bash And Usermode Ubuntu Linux Binaries On Windows 10</span></span>](https://www.hanselman.com/blog/DevelopersCanRunBashShellAndUsermodeUbuntuLinuxBinariesOnWindows10.aspx)
* [<span data-ttu-id="d3b50-127">Windows 上的 Ubuntu – 面向 Windows 开发人员的 Ubuntu 用户空间</span><span class="sxs-lookup"><span data-stu-id="d3b50-127">Ubuntu on Windows – The Ubuntu Userspace for Windows Developers</span></span>](https://insights.ubuntu.com/2016/03/30/ubuntu-on-windows-the-ubuntu-userspace-for-windows-developers/) 

## <a name="provide-feedback"></a><span data-ttu-id="d3b50-128">提供反馈</span><span class="sxs-lookup"><span data-stu-id="d3b50-128">Provide Feedback</span></span>
* [<span data-ttu-id="d3b50-129">GitHub 问题跟踪器</span><span class="sxs-lookup"><span data-stu-id="d3b50-129">GitHub issue tracker</span></span>](https://github.com/Microsoft/BashOnWindows/issues)
* [<span data-ttu-id="d3b50-130">命令行 UserVoice 门户</span><span class="sxs-lookup"><span data-stu-id="d3b50-130">Command-line UserVoice portal</span></span>](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
