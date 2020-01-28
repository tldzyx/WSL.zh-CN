---
title: 为 WSL 分发版创建和更新用户帐户
description: 适用于 Linux 的 Windows 子系统的用户帐户和权限管理参考。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, 用户帐户
ms.date: 01/20/2020
ms.topic: article
ms.assetid: f70e685f-24c6-4908-9546-bf4f0291d8fd
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 85bd8f05d041181c2cfb16f6fb55aaeea15b332c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520576"
---
# <a name="create-and-update-user-accounts-for-wsl-distributions"></a>为 WSL 分发版创建和更新用户帐户

启用 WSL 并从 Microsoft Store 中安装 Linux 分发版后，在打开新安装的 Linux 分发版时将要求你完成的第一步是创建帐户，包括**用户名**和**密码**。

- 此**用户名**和**密码**特定于 Linux 分发版，与 Windows 用户名无关。

- 创建此**用户名**和**密码**后，该帐户将是分发版的默认用户，并将在启动时自动登录。

- 此帐户将被视为 Linux 管理员，能够运行 `sudo` (Super User Do) 管理命令。

- 在适用于 Linux 的 Windows 子系统上运行的每个 Linux 分发版都有其自身的 Linux 用户帐户和密码。  每当添加分发版、重新安装或重置时，都必须配置一个 Linux 用户帐户。

## <a name="reset-your-linux-password"></a>重置 Linux 密码

若要更改密码，请打开 Linux 分发版（例如 Ubuntu）并输入以下命令：`passwd`

系统会要求你输入当前密码，然后要求输入新密码，之后再确认新密码。

### <a name="forgot-your-password"></a>忘记密码

如果忘记了 Linux 分发版的密码：

1. 请打开 PowerShell，并使用以下命令进入默认 WSL 分发版的根目录：`wsl -u root`

-- 如果需要在非默认分发版中更新忘记的密码，请使用命令：`wsl -d Debian -u root`，并将 `Debian` 替换为目标分发版的名称。

2. 在 PowerShell 内的根级别打开 WSL 分发版后，可以使用此命令更新密码：`passwd`

3. 系统将提示你输入新的 UNIX 密码，然后确认该密码。 在被告知密码已成功更新后，请使用以下命令在 PowerShell 内关闭 WSL：`exit`

> [!NOTE]
> 如果运行的是早期版本的 Windows 操作系统，例如 1703（创意者更新）或 1709 (Fall Creators Update)，请参阅[此用户帐户更新文档的存档版本](./user-support-archived.md)。
