---
title: 为 WSL 分发版创建和更新用户帐户
description: 适用于 Linux 的 Windows 子系统的用户帐户和权限管理参考。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, 用户帐户
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 30dea11adb68639f645ca800a695b0404661845a
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "76973677"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a><span data-ttu-id="8cd3a-104">为 WSL 分发版创建和更新用户帐户</span><span class="sxs-lookup"><span data-stu-id="8cd3a-104">Create and update user accounts for WSL distributions</span></span>

<span data-ttu-id="8cd3a-105">启用 WSL 并从 Microsoft Store 中安装 Linux 分发版后，在打开新安装的 Linux 分发版时将要求你完成的第一步是创建帐户，包括**用户名**和**密码**。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-105">Once you have enabled WSL and installed a Linux distribution from the Microsoft Store, the first step you will be asked to complete when opening your newly installed Linux distribution is to create an account, including a **User Name** and **Password**.</span></span>

- <span data-ttu-id="8cd3a-106">此**用户名**和**密码**特定于 Linux 分发版，与 Windows 用户名无关。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-106">This **User Name** and **Password** is specific to your Linux distribution and has no bearing on your Windows user name.</span></span>

- <span data-ttu-id="8cd3a-107">创建此**用户名**和**密码**后，该帐户将是分发版的默认用户，并将在启动时自动登录。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-107">Once you create this **User Name** and **Password**, the account will be your default user for the distribution and automatically sign-in on launch.</span></span>

- <span data-ttu-id="8cd3a-108">此帐户将被视为 Linux 管理员，能够运行 `sudo` (Super User Do) 管理命令。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-108">This account will be considered the Linux administrator, with the ability to run `sudo` (Super User Do) administrative commands.</span></span>

- <span data-ttu-id="8cd3a-109">在适用于 Linux 的 Windows 子系统上运行的每个 Linux 分发版都有其自身的 Linux 用户帐户和密码。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-109">Each Linux distribution running on the Windows Subsystem for Linux has its own Linux user accounts and passwords.</span></span>  <span data-ttu-id="8cd3a-110">每当添加分发版、重新安装或重置时，都必须配置一个 Linux 用户帐户。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-110">You will have to configure a Linux user account every time you add a distribution, reinstall, or reset.</span></span>

## <a name="reset-your-linux-password"></a><span data-ttu-id="8cd3a-111">重置 Linux 密码</span><span class="sxs-lookup"><span data-stu-id="8cd3a-111">Reset your Linux password</span></span>

<span data-ttu-id="8cd3a-112">若要更改密码，请打开 Linux 分发版（例如 Ubuntu）并输入以下命令：`passwd`</span><span class="sxs-lookup"><span data-stu-id="8cd3a-112">To change your password, open your Linux distribution (Ubuntu for example) and enter the command: `passwd`</span></span>

<span data-ttu-id="8cd3a-113">系统会要求你输入当前密码，然后要求输入新密码，之后再确认新密码。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-113">You will be asked to enter your current password, then asked to enter your new password, and then to confirm your new password.</span></span>

### <a name="forgot-your-password"></a><span data-ttu-id="8cd3a-114">忘记密码</span><span class="sxs-lookup"><span data-stu-id="8cd3a-114">Forgot your password</span></span>

<span data-ttu-id="8cd3a-115">如果忘记了 Linux 分发版的密码：</span><span class="sxs-lookup"><span data-stu-id="8cd3a-115">If you forgot the password for your Linux distribution:</span></span>

1. <span data-ttu-id="8cd3a-116">请打开 PowerShell，并使用以下命令进入默认 WSL 分发版的根目录：`wsl -u root`</span><span class="sxs-lookup"><span data-stu-id="8cd3a-116">Open PowerShell and enter the root of your default WSL distribution using the command: `wsl -u root`</span></span>

> <span data-ttu-id="8cd3a-117">如果需要在非默认分发版中更新忘记的密码，请使用命令：`wsl -d Debian -u root`，并将 `Debian` 替换为目标分发版的名称。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-117">If you need to update the forgotten password on a distribution that is not your default, use the command: `wsl -d Debian -u root`, replacing `Debian` with the name of your targeted distribution.</span></span>

2. <span data-ttu-id="8cd3a-118">在 PowerShell 内的根级别打开 WSL 分发版后，可以使用此命令更新密码：`passwd`</span><span class="sxs-lookup"><span data-stu-id="8cd3a-118">Once your WSL distribution has been opened at the root level inside PowerShell, you can use this command to update your password: `passwd`</span></span>

3. <span data-ttu-id="8cd3a-119">系统将提示你输入新的 UNIX 密码，然后确认该密码。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-119">You will be prompted to enter a new UNIX password and then confirm that password.</span></span> <span data-ttu-id="8cd3a-120">在被告知密码已成功更新后，请使用以下命令在 PowerShell 内关闭 WSL：`exit`</span><span class="sxs-lookup"><span data-stu-id="8cd3a-120">Once you're told that the password has updated successfully, close WSL inside of PowerShell using the command: `exit`</span></span>

> [!NOTE]
> <span data-ttu-id="8cd3a-121">如果运行的是早期版本的 Windows 操作系统，例如 1703（创意者更新）或 1709 (Fall Creators Update)，请参阅[此用户帐户更新文档的存档版本](./user-support-archived.md)。</span><span class="sxs-lookup"><span data-stu-id="8cd3a-121">If you are running an early version of Windows operating system, like 1703 (Creators Update) or 1709 (Fall Creators Update), see the [archived version of this user account update doc](./user-support-archived.md).</span></span>
