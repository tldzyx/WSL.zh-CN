---
title: 在 Windows 10 周年更新或创意者更新上安装或删除
description: 适用于 Windows 10 周年更新或创意者更新的旧版、beta 发行版的安装和卸载说明
keywords: BashOnWindows，bash，wsl，windows，适用于 linux 的 windows 子系统，windowssubsystem，ubuntu，debian，suse，windows 10，旧版，beta，安装，删除，卸载，卸载，删除，已弃用
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 416bed3ed3a0470da2eb5e6beb75e73eb6836200
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269773"
---
# <a name="guide-to-install-or-uninstall-windows-subsystem-for-linux-on-windows-10-anniversary-update-and-creators-update"></a>在 Windows 10 周年更新和创意者更新上安装或卸载适用于 Linux 的 Windows 子系统的指南 

如果运行的是 Windows 10 创意者更新或更高版本，请[遵循 windows 10 安装说明](install-win10.md)。

<strong><em><span style="color: #f28014">以下说明适用于运行 Windows 10 周年更新或 Windows 10 创意者更新的用户</span></em></strong>

在 Windows 10 秋季创意者更新（版本1709）之前，WSL 已作为 beta 功能发布，并在第一次运行 "在 Windows 上的 Bash on Ubuntu 时安装了一个 Ubuntu 实例"。

> 尽管可以在早期版本的 Windows 10 版本上使用 WSL，但此 beta "旧发行版" 现在被视为已过时。 强烈建议运行最新版本的 Windows 10。 每个新的 Windows 10 版本都单独包括 WSL 中的数百个修补程序和改进功能，使更多的 Linux 工具和应用能够在 WSL 上正常运行。

如果无法升级到秋季创意者更新或更高版本，请按照以下步骤启用和使用 WSL：

1. 开启开发人员模式若要在 Windows 10 周年更新或创意者更新上运行 WSL，必须启用开发人员模式：

    **为开发人员**打开 -> **更新和安全** -> 的**设置**

    选择 "开发人员模式" 单选按钮  
    ![启用开发人员模式](media/updateAndSecurity.png)

    > [Windows 10 秋季创意者更新中已删除](https://blogs.msdn.microsoft.com/commandline/2017/06/08/developer-mode-no-longer-required-for-windows-subsystem-for-linux/)启用开发人员模式的要求

1. 打开命令提示符。  键入 `bash` 并按 enter

    首次在 Windows 上的 Ubuntu 上运行 Bash 时，系统将提示你接受规范的许可证。 接受后，WSL 会将 Ubuntu 实例下载并安装到计算机上，并将在 "开始" 菜单中添加 "Bash on Ubuntu on Windows" 快捷方式。

    ![提示安装 Ubuntu](media/bashShellInstall.png)

    首次在 Windows 上的 Ubuntu 上运行 Bash 时，系统将提示你创建 UNIX 用户名和密码。 按照[新的发行版实例说明](initialize-distro.md)完成安装

1. 通过以下方法之一启动新的 Ubuntu shell：
    * 从命令提示符运行 `bash`
    * 单击 "开始" 菜单 "在 Windows 上打开 Ubuntu on Ubuntu" 快捷方式

    
## <a name="uninstallingremoving-the-legacy-distro"></a>卸载/删除旧发行版
如果从安装了 WSL 的早期 Windows 10 版本升级到 Windows 10 秋季创意者更新，则现有发行版将保持不变。 但是，我们强烈建议你尽快安装新的存储提供的发行版，并将所有必要的文件、数据等从旧发行版迁移到新的发行版。

若要从计算机中删除旧的发行版，请从命令行或 PowerShell 实例运行以下命令：

```console
wsl --unregister Legacy
```

如果未使用 Windows 版本1903或更高版本，则可能需要改为运行 `wslconfig /u Legacy` 或 `lxrun /uninstall /full`。 

### <a name="manually-deleting-the-legacy-distro"></a>手动删除旧发行版
如果需要，可以手动删除旧实例。 如果使用 `lxrun.exe`卸载旧的发行版或运行 Windows 10 春季2018更新（或更高版本），但未附带 `lxrun.exe`，则可能需要执行此操作。

若要强制删除旧的 WSL 发行版，请使用 Windows 文件资源管理器或命令行删除 `%localappdata%\lxss\` 文件夹（及其所有子内容）：

使用 PowerShell
```powershell
rm -Recurse $env:localappdata/lxss/
```

使用 Cmd：
```console
DEL /S %localappdata%\lxss\
```
