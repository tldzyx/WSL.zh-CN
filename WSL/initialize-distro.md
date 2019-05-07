---
title: 初始化新的 WSL Linux 发行版
description: 后安装 WSL 的 Linux 发行版，请按照以下简单步骤完成初始化
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
一旦下载并安装你的发行，您将需要完成初始化新的发行版：

## <a name="launch-a-distro"></a>启动发行版
若要完成初始化的新安装发行版，启动新实例。 通过单击 Windows 应用商店应用中的"启动"按钮或启动从开始菜单的发行版，可以执行此操作：

> 提示：你可能想要固定到开始菜单，和/或任务栏将使用频率最高发行版 ！

![启动从开始菜单的发行版](media/start-menu.png)

> 在 Windows 服务器上，可以启动可执行文件的发行版的启动器`<distro>.exe`发行版安装文件夹中。

第一次新安装的发行版运行时，的控制台窗口将打开，并将询问您等待一两分钟才能完成安装。

> 在安装此最终阶段，发行版的文件是取消压缩和存储在您 PC 上，供使用。 这可能需要一分钟或更多具体取决于你的电脑的存储设备的性能。 此初始安装阶段才需要清理的安装的发行版时所有将来的启动应采取少于一秒。

## <a name="setting-up-a-new-linux-user-account"></a>设置新的 Linux 用户帐户

安装完成后，系统会提示您创建新的用户帐户 （和其密码）。 

![解包 Windows 控制台中的 Ubuntu](media/UbuntuInstall.png)

此用户帐户是正常的非管理员用户，就可以登录的作为默认情况下启动发行版时。

> 可以选择任何用户名和密码想-你的 Windows 用户名没有任何关系。 

打开新的发行版实例时，您不会被提示输入你的密码，但**如果进程使用提升`sudo`，将需要输入密码**，因此请确保你选择可以很容易记住的密码 ！ 请参阅[用户支持](user-support.md)的详细信息页。

## <a name="update--upgrade-your-distros-packages"></a>更新和升级你的发行包

大多数发行版所附带的最小空/包目录。 我们强烈建议定期更新您的包目录，并升级已安装的包使用发行版的首选的包管理器。 在 Debian/Ubuntu 上使用 apt:

```bash
sudo apt update && sudo apt upgrade
```

> Windows 不会不会自动更新或升级 Linux distro(s):这是 Linux 用户想控制自己的任务。

操作完成！ 喜欢在 WSL 上使用新的 Linux 发行版 ！ 若要了解有关 WSL 的详细信息，请查看其他[WSL docs](https://aka.ms/wsldocs)，或[WSL 学习资源页面](https://aka.ms/learnwsl)。

![喜欢使用 Linux 上 WSL](media/linux-on-wsl.png)

## <a name="troubleshooting"></a>疑难解答

以下是相关的错误的建议修补程序。 请参阅[WSL 故障排除页](troubleshooting.md)其他常见的错误和其解决方案。

> **安装失败，出现错误 0x8007007e**系统不支持从应用商店 Linux 时发生此错误。  请确保：
> * 正在运行 Windows 生成 16215 或更高版本。 [检查你的生成](troubleshooting.md#check-your-build-number)。
> * Linux 可选组件的 Windows 子系统，并重新启动计算机。  [请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
