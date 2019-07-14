---
title: 初始化新的 WSL Linux 发行版
description: 在为 WSL 安装 Linux 发行版之后，按照以下简单步骤完成初始化
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统
author: taraj
ms.author: taraj
ms.date: 07/24/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 7f1ce521b248c873fa7f81c6363eb506c0363fed
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/22/2019
ms.locfileid: "59902044"
---
# <a name="initializing-a-newly-installed-distro"></a>初始化新安装的发行版
下载并安装完发行版之后，您需要完成新发行版的初始化：

## <a name="launch-a-distro"></a>启动发行版
若要完成新安装发行版的初始化，请启动新实例。您可以通过单击 Microsoft Store 应用程序中的"启动"按钮，或从“开始”菜单启动发行版来执行此操作：

> 提示：您可能希望将最常用的发行版固定到“开始”菜单和/或任务栏！

![启动从开始菜单的发行版](media/start-menu.png)

> 在 Windows Server 上，您可以从发行版安装文件夹中启动发行版的可执行文件`<distro>.exe`。

新安装的发行版第一次运行时，将打开一个控制台窗口，您将被要求等待一两分钟才能完成安装。

> 在安装的最后阶段，发行版的文件被解压缩并存储在您的PC上，随时可以使用。这可能需要大约一分钟或更长时间，具体取决于PC存储设备的性能。只有在安装清洁安装发行版时才需要此初始安装阶段 - 所有未来发布的都需要不到一秒钟。

## <a name="setting-up-a-new-linux-user-account"></a>设置新的 Linux 用户帐户

安装完成后，系统会提示您创建新的用户帐户（及其密码）。 

![解包 Windows 控制台中的 Ubuntu](media/UbuntuInstall.png)

此用户帐户是普通的非管理员用户，可以作为您在启动发行版时默认登录的帐户。

> 您可以选择任何您想要的用户名和密码 - 它们与您的 Windows 用户名无关。

当您打开新的发行版实例时，您不会被提示输入密码，但**如果使用`sudo`提升进程，将需要输入密码**，因此请确保选择一个易于记忆的密码！有关详细信息，请参阅[用户支持](user-support.md)页面。

## <a name="update--upgrade-your-distros-packages"></a>更新和升级你的发行包

大多数发行版都附带一个空的/最小的包目录。我们强烈建议定期更新您的包目录，并使用您发行版的首选包管理器升级已安装的包。在 Debian/Ubuntu 上使用 apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows 不会自动更新或升级 Linux 发行版：这是 Linux 用户更喜欢自行控制的任务。

操作完成！ 喜欢在 WSL 上使用新的 Linux 发行版 ！ 若要了解有关 WSL 的详细信息，请查看其他[WSL docs](https://aka.ms/wsldocs)，或[WSL 学习资源页面](https://aka.ms/learnwsl)。

![喜欢使用 Linux 上 WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>疑难解答

以下是相关的错误的建议修补程序。有关其他常见错误及其解决方案，请参阅[WSL 故障排除页](troubleshooting.md)。

> **安装失败，出现错误 0x8007007e**当您的系统不支持来自商店的 Linux 时，会发生此错误。请确保：
> * 正在运行 Windows build 16215 或更高版本。[检查您的版本号](troubleshooting.md#check-your-build-number)。
> * 适用于 Linux 的 Windows 子系统可选组件已启用，并重新启动计算机。[请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
