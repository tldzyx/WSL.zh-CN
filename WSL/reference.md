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
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063575"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的命令参考

> `lxrun.exe` 是不推荐使用截至 Windows 10 1803年和更高版本。

该命令`lxrun.exe`可用于与交互[Windows 子系统用于 Linux (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)直接。  这些命令安装到`\Windows\System32`目录，并且可能在 Windows 命令提示符或 PowerShell 中运行。

* `lxrun.exe` 用于管理 WSL。  此命令可用于安装或卸载的 Ubuntu 映像。


| Command                     | 描述                     |
|:----------------------------|:---------------------------|
| `bash`                      | 将启动当前目录中的 Bash shell。  如果未自动安装 Bash shell 运行 `lxrun /install` |
| `bash ~`                    | 到用户的 Ubuntu 主目录中启动 bash shell。  类似于运行 cd ~            |
| `bash -c "<command>"`       | 运行该命令，将输出传输并返回到 Windows 命令提示符下退出。 <br/> <br/> 示例： **bash-c"ls"** |

<p>

| Command                     | 描述                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun 命令用于管理 WSL 实例。 |
| `lxrun /install`            | 开始下载和安装过程。 <br/> **/y**可能添加绕过所有提示。  自动接受确认提示和默认用户设置为根。          |
| `lxrun /uninstall`          | 卸载和删除的 Ubuntu 映像。  默认情况下这不会删除用户的 Ubuntu 主目录。 <br/> **/y**可能添加自动接受确认提示 <br/>**/ 完整**会卸载并删除用户的 Ubuntu 主目录         |
| `lxrun /setdefaultuser <userName>`     | 设置默认 Bash on Ubuntu 用户。 如果指定的用户不存在，将提示输入密码。  有关详细信息，请访问： https://aka.ms/wslusers。 <br/> **/y**免验证 promping 的密码。  密码的情况下，将创建该用户。|
| `lxrun /update`            | 子系统的包索引中更新          |
