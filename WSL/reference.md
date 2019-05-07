---
title: 有关 Linux 命令参考的 Windows 子系统
description: 管理适用于 Linux 的 Windows 子系统的命令列表
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu 的 windows 子系统
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 978a35d593e37877949c24cbd833a519888d54bf
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063575"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a><span data-ttu-id="800bc-104">适用于 Linux 的 Windows 子系统的命令参考</span><span class="sxs-lookup"><span data-stu-id="800bc-104">Command Reference for Windows Subsystem for Linux</span></span>

> <span data-ttu-id="800bc-105">`lxrun.exe` 是不推荐使用截至 Windows 10 1803年和更高版本。</span><span class="sxs-lookup"><span data-stu-id="800bc-105">`lxrun.exe` is deprecated as of Windows 10 1803 and later.</span></span>

<span data-ttu-id="800bc-106">该命令`lxrun.exe`可用于与交互[Windows 子系统用于 Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)直接。</span><span class="sxs-lookup"><span data-stu-id="800bc-106">The command `lxrun.exe` can be used to interact with the [Windows Subsystem for Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-) directly.</span></span>  <span data-ttu-id="800bc-107">这些命令安装到`\Windows\System32`目录，并且可能在 Windows 命令提示符或 PowerShell 中运行。</span><span class="sxs-lookup"><span data-stu-id="800bc-107">These commands are installed into the `\Windows\System32` directory and may be run within a Windows command prompt or in PowerShell.</span></span>

* <span data-ttu-id="800bc-108">`lxrun.exe` 用于管理 WSL。</span><span class="sxs-lookup"><span data-stu-id="800bc-108">`lxrun.exe` is used to manage WSL.</span></span>  <span data-ttu-id="800bc-109">此命令可用于安装或卸载的 Ubuntu 映像。</span><span class="sxs-lookup"><span data-stu-id="800bc-109">This command can be used to install or uninstall the Ubuntu image.</span></span>


| <span data-ttu-id="800bc-110">Command</span><span class="sxs-lookup"><span data-stu-id="800bc-110">Command</span></span>                     | <span data-ttu-id="800bc-111">描述</span><span class="sxs-lookup"><span data-stu-id="800bc-111">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `bash`                      | <span data-ttu-id="800bc-112">将启动当前目录中的 Bash shell。</span><span class="sxs-lookup"><span data-stu-id="800bc-112">Launches the Bash shell in the current directory.</span></span>  <span data-ttu-id="800bc-113">如果未自动安装 Bash shell 运行 `lxrun /install`</span><span class="sxs-lookup"><span data-stu-id="800bc-113">If the Bash shell is not installed automatically runs `lxrun /install`</span></span> |
| `bash ~`                    | <span data-ttu-id="800bc-114">到用户的 Ubuntu 主目录中启动 bash shell。</span><span class="sxs-lookup"><span data-stu-id="800bc-114">Launches the bash shell into the user's Ubuntu home directory.</span></span>  <span data-ttu-id="800bc-115">类似于运行 cd ~</span><span class="sxs-lookup"><span data-stu-id="800bc-115">Similar to running cd ~</span></span>            |
| `bash -c "<command>"`       | <span data-ttu-id="800bc-116">运行该命令，将输出传输并返回到 Windows 命令提示符下退出。</span><span class="sxs-lookup"><span data-stu-id="800bc-116">Runs the command, prints the output and exits back to the Windows command prompt.</span></span> <br/> <br/> <span data-ttu-id="800bc-117">示例： **bash-c"ls"**</span><span class="sxs-lookup"><span data-stu-id="800bc-117">Example:  **bash -c "ls"**</span></span> |

<p>

| <span data-ttu-id="800bc-118">Command</span><span class="sxs-lookup"><span data-stu-id="800bc-118">Command</span></span>                     | <span data-ttu-id="800bc-119">描述</span><span class="sxs-lookup"><span data-stu-id="800bc-119">Description</span></span>                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | <span data-ttu-id="800bc-120">Lxrun 命令用于管理 WSL 实例。</span><span class="sxs-lookup"><span data-stu-id="800bc-120">The lxrun command is used to manage the WSL instance.</span></span> |
| `lxrun /install`            | <span data-ttu-id="800bc-121">开始下载和安装过程。</span><span class="sxs-lookup"><span data-stu-id="800bc-121">Starts the download and install process.</span></span> <br/> <span data-ttu-id="800bc-122">**/y**可能添加绕过所有提示。</span><span class="sxs-lookup"><span data-stu-id="800bc-122">**/y** may be added to bypass all prompts.</span></span>  <span data-ttu-id="800bc-123">自动接受确认提示和默认用户设置为根。</span><span class="sxs-lookup"><span data-stu-id="800bc-123">The confirmation prompt is automatically accepted and the default user is set to root.</span></span>          |
| `lxrun /uninstall`          | <span data-ttu-id="800bc-124">卸载和删除的 Ubuntu 映像。</span><span class="sxs-lookup"><span data-stu-id="800bc-124">Uninstalls and deletes the Ubuntu image.</span></span>  <span data-ttu-id="800bc-125">默认情况下这不会删除用户的 Ubuntu 主目录。</span><span class="sxs-lookup"><span data-stu-id="800bc-125">By default this does not remove the user's Ubuntu home directory.</span></span> <br/> <span data-ttu-id="800bc-126">**/y**可能添加自动接受确认提示</span><span class="sxs-lookup"><span data-stu-id="800bc-126">**/y** may be added to automatically accept the confirmation prompt</span></span> <br/><span data-ttu-id="800bc-127">**/ 完整**会卸载并删除用户的 Ubuntu 主目录</span><span class="sxs-lookup"><span data-stu-id="800bc-127">**/full** uninstalls and deletes the user's Ubuntu home directory</span></span>         |
| `lxrun /setdefaultuser <userName>`     | <span data-ttu-id="800bc-128">设置默认 Bash on Ubuntu 用户。</span><span class="sxs-lookup"><span data-stu-id="800bc-128">Sets the default Bash on Ubuntu user.</span></span> <span data-ttu-id="800bc-129">如果指定的用户不存在，将提示输入密码。</span><span class="sxs-lookup"><span data-stu-id="800bc-129">Will prompt for a password if the specified user does not exist.</span></span>  <span data-ttu-id="800bc-130">有关详细信息，请访问： https://aka.ms/wslusers。</span><span class="sxs-lookup"><span data-stu-id="800bc-130">For more information visit: https://aka.ms/wslusers.</span></span> <br/> <span data-ttu-id="800bc-131">**/y**免验证 promping 的密码。</span><span class="sxs-lookup"><span data-stu-id="800bc-131">**/y** Bypasses promping for the password.</span></span>  <span data-ttu-id="800bc-132">密码的情况下，将创建该用户。</span><span class="sxs-lookup"><span data-stu-id="800bc-132">The user will be created without a password.</span></span>|
| `lxrun /update`            | <span data-ttu-id="800bc-133">子系统的包索引中更新</span><span class="sxs-lookup"><span data-stu-id="800bc-133">Updates the subsystem's package index</span></span>          |
