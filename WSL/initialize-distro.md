---
title: 初始化新的 WSL Linux 分发版
description: 安装适用于 WSL 的 Linux 分发版后，请执行以下简单步骤来完成初始化
keywords: BashOnWindows, bash, wsl, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122717"
---
# <a name="initializing-a-newly-installed-distro"></a>初始化新安装的分发版
下载并安装分发版后，需要对新的分发版完成初始化：

## <a name="launch-a-distro"></a>启动分发版
若要完成新安装的分发版的初始化，请启动新实例。 为此，可以单击 Microsoft Store 应用中的“启动”按钮，或者从“开始”菜单启动分发版：

> 提示：可将最常用的分发版固定到“开始”菜单和/或任务栏！

![从“开始”菜单启动分发版](media/start-menu.png)

> 在 Windows Server 上，可以从分发版的安装文件夹启动分发版的启动程序可执行文件 `<distro>.exe`。

首次运行新安装的分发版时，会打开一个控制台窗口，其中指出需要等待一两分钟时间来完成安装。

> 在这最后一个安装阶段，分发版的文件将会解压缩，并存储在电脑上供你使用。 这可能需要一分钟或更长时间，具体取决于电脑存储设备的性能。 仅当分发版是干净安装的版本时，才需要执行此初始安装阶段 - 将来在不到一秒内即可启动分发版。

## <a name="setting-up-a-new-linux-user-account"></a>设置新的 Linux 用户帐户

安装完成后，系统会提示创建新的用户帐户（及其密码）。 

![Windows 控制台中的 Ubuntu 解包](media/UbuntuInstall.png)

此用户帐户用于启动分发版时默认登录的非管理员用户。

> 可根据需要选择任何用户名和密码 - 它们与 Windows 用户名无关。 

打开新的分发版实例时，系统不会提示你输入密码，但**如果使用 `sudo` 提升了进程的权限，则需要输入密码**，因此请确保选择一个容易记住的密码！ 有关详细信息，请参阅[用户支持](user-support.md)页。

## <a name="update--upgrade-your-distros-packages"></a>更新和升级分发版的包

大多数分发版随附了一个空的/精简的包目录。 我们强烈建议定期更新包目录，并使用分发版的首选包管理器升级已安装的包。 在 Debian/Ubuntu 上使用 apt：

```bash
sudo apt update && sudo apt upgrade
```

> Windows 不会自动更新或升级 Linux 分发版：Linux 用户往往倾向于自行控制此任务。

大功告成！ 现在，可以在 WSL 上享用新的 Linux 分发版！ 若要详细了解 WSL，请查看其他 [WSL 文档](https://aka.ms/wsldocs)或 [WSL 学习资源页](https://aka.ms/learnwsl)。

![在 WSL 上享用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>疑难解答

下面是相关的错误和建议的修复措施。 有关其他常见错误及其解决方法，请参阅 [WSL 故障排除页](troubleshooting.md)。

> **安装失败并出现错误 0x8007007e** 如果系统不支持从 Store 安装的 Linux，则会出现此错误。  请确保：
> * 运行 Windows 内部版本 16215 或更高版本。 [检查内部版本](troubleshooting.md#check-your-build-number)。
> * 已启用“适用于 Linux 的 Windows 子系统”可选组件，并已重启计算机。  [确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
