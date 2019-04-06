---
title: 安装或删除在 Windows 10 周年更新或创意者更新
description: 旧版、 beta 发行版在 Windows 10 周年更新或创意者更新的安装和卸载说明
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10，旧版、 beta 版的 windows 子系统安装、 删除、 卸载，请卸载，删除，不推荐使用
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b31bb3a542b8481c723df42292e20e364680722d
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063585"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>若要安装或卸载适用于 Windows 10 周年更新和创意者更新上的 Linux 的 Windows 子系统的指南 

如果要运行 Windows 10 创意者更新或更高版本，请[按照 Windows 10 安装说明进行操作](install-win10.md)。

<strong><em><span style="color: #f28014">以下说明适用于运行 Windows 10 周年更新或 Windows 10 创意者更新的用户</span></em></strong>

在 Windows 10 Fall Creators Update （版本 1709年） 之前, WSL 作为 beta 版功能发布和安装单个 Ubuntu 实例"的 Bash 在 Ubuntu 上 Windows"（或 Bash.exe） 首次运行时。

> 尽管在早期的 Windows 10 版本上，可以使用 WSL，"旧发行版"此测试版现已被淘汰。 我们强烈建议你运行 Windows 10 个可用的最新版本。 每个新的 Windows 10 版本包括在 WSL 独立的允许更 Linux 工具和应用，以便在 WSL 上正确运行数百个修复和改进。

如果您不能升级为 Fall Creators Update 或更高版本，请执行以下步骤来启用和使用 WSL:

1. 打开开发人员模式为 Windows 10 周年更新或创意者更新上运行 WSL，必须启用开发人员模式：

    打开**设置** -> **更新和安全** -> **面向开发人员**

    选择开发人员模式下的单选按钮  
    ![启用开发人员模式](media/updateAndSecurity.png)

    > 若要启用开发人员模式的要求是[在 Windows 10 Fall Creators Update 中删除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)

1. 打开命令提示符。  类型`bash`并按 enter

    首次 Bash 在 Ubuntu 运行 Windows，系统会提示接受 Canonical 的许可证。 一次 accpted，WSL 将下载并安装到您计算机上的 Ubuntu 实例以及"Bash 在 Ubuntu 上 Windows"快捷方式将添加到开始菜单。

    ![提示安装 Ubuntu](media/bashShellInstall.png)

    首次 Bash 在 Ubuntu 运行 Windows，系统会提示创建 UNIX 用户名和密码。 请按照[发行版的新实例指令](initialize-distro.md)可完成安装

1. 通过以下任一方法启动新的 Ubuntu 外壳程序：
    * 运行`bash`从命令提示符
    * 单击开始菜单"Bash 在 Ubuntu 上 Windows"快捷方式

    
## <a name="uninstallingremoving-the-legacy-distro"></a>卸载/删除旧的发行版
如果您从在其安装 WSL 早期 Windows 10 版本升级到 Windows 10 Fall Creators Update，则你现有的发行版将保持不变。 但是，我们强烈建议您安装的新应用商店提供发行版，ASAP，并将任何必要的文件、 数据等从旧发行版迁移到新发行版。

若要从计算机中删除旧的发行版，从命令行或 PowerShell 实例运行以下命令：

```console
lxrun /uninstall /full
```

### <a name="manually-deleting-the-legacy-distro"></a>手动删除旧的发行版
如果您愿意，可以手动删除旧实例。 如果遇到问题卸载旧的发行版使用这可能是所需`lxrun.exe`，或在运行 Windows 10 Spring 2018 Update （或更高版本） 的不会随附于`lxrun.exe`。

若要强制删除旧的 WSL 发行版，删除`%localappdata%\lxss\`文件夹 (和所有它的子内容) 使用 Windows 的文件资源管理器或命令行：

使用 PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

使用 Cmd:
```console
DEL /S %localappdata%\lxss\
```
