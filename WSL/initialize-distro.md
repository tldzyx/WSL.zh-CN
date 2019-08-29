---
title: 初始化新的 WSL Linux 发行版
description: 安装适用于 WSL 的 Linux 发行版后, 请按照以下简单步骤完成初始化
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, debian, suse, windows 10
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: e544dc461913c6e044c70f39103cced62167c4b8
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122717"
---
# <a name="initializing-a-newly-installed-distro"></a>初始化新安装的发行版
下载并安装发行版后, 需要完成新发行版的初始化:

## <a name="launch-a-distro"></a>启动发行版
若要完成新安装的发行版的初始化, 请启动新的实例。 要执行此操作, 可以单击 Microsoft Store 应用中的 "启动" 按钮, 或从 "开始" 菜单启动发行版:

> 提示：你可能需要将最常使用的发行版固定到 "开始" 菜单, 并/或任务栏上!

![从 "开始" 菜单启动发行版](media/start-menu.png)

> 在 Windows Server 上, 可以从发行版安装文件夹启动发行版`<distro>.exe`的启动器可执行文件。

首次运行新安装的发行版时, 将打开一个控制台窗口, 系统会要求你等待一分钟或两分钟来完成安装。

> 在安装的最后阶段, 发行版的文件将被取消压缩并存储在你的电脑上, 随时可以使用。 这可能需要一分钟或更长时间, 具体取决于 PC 的存储设备的性能。 仅当发行版干净安装时, 才需要执行此初始安装阶段-所有将来启动的时间应不到一秒钟。

## <a name="setting-up-a-new-linux-user-account"></a>设置新的 Linux 用户帐户

安装完成后, 系统会提示创建新的用户帐户 (及其密码)。 

![Windows 控制台中的 Ubuntu 解包](media/UbuntuInstall.png)

此用户帐户适用于默认情况下, 在启动发行版时将以默认方式登录的非管理员用户。

> 你可以选择所需的任何用户名和密码, 而无需使用 Windows 用户名。 

当您打开新的发行版实例时，您不会被提示输入密码，但**如果使用`sudo`提升进程，将需要输入密码**，因此请确保选择一个易于记忆的密码！ 有关详细信息，请参阅[用户支持](user-support.md)页面。

## <a name="update--upgrade-your-distros-packages"></a>更新 & 升级发行版的包

大多数发行版附带了一个空/最小包目录。 我们强烈建议定期更新包目录, 并使用发行版的首选包管理器升级已安装的包。 在 Debian/Ubuntu 上, 使用 apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows 不会自动更新或升级 Linux 发行版:这是 Linux 用户喜欢自行控制的任务。

操作完成！ 在 WSL 上使用新的 Linux 发行版! 若要了解有关 WSL 的详细信息, 请查看其他[WSL 文档](https://aka.ms/wsldocs)或[WSL 学习资源页](https://aka.ms/learnwsl)。

![在 WSL 上使用 Linux](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>疑难解答

以下是相关的错误和建议的修补措施。 有关其他常见错误及其解决方案，请参阅 [WSL 故障排除页](troubleshooting.md)。

> **安装失败, 出现错误 0x8007007e**当你的系统不支持应用商店中的 Linux 时, 会发生此错误。  请确保：
> * 正在运行 Windows build 16215 或更高版本。 [检查你的版本号](troubleshooting.md#check-your-build-number)。
> * 适用于 Linux 的 Windows 子系统可选组件已启用，并重新启动计算机。  [请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
