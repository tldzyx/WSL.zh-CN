---
title: 为 WSL 构建的自定义 Linux 发行版
description: 了解如何创建适用于 Linux 的 Windows 子系统的自定义的 Linux 分发版。
keywords: BashOnWindows，bash、 wsl、 windows、 windows 子系统、 发行版、 自定义
author: taraj
ms.author: taraj
ms.date: 03/27/2018
ms.topic: article
ms.assetid: a5095219-0c82-4ce5-9a6d-5c2fc00835a3
ms.custom: seodec18
ms.openlocfilehash: b98101c19d7d450548531521c3f8ee15ce62f9f1
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063255"
---
# <a name="creating-a-custom-linux-distro-for-wsl"></a>创建的自定义 Linux 发行版，适用于 WSL

若要生成的 Microsoft Store WSL 发行版包和/或创建自定义 Linux 发行版程序包以进行旁加载，请使用我们开放源代码 WSL 示例。 您可以找到[发行版启动器存储库](https://github.com/Microsoft/WSL-DistroLauncher)GitHub 上。

此项目启用：
* Linux 分发 maintainer 打包和提交在 WSL 运行一个 appx 作为一种 Linux 分发
* 开发人员能够创建自定义可以是旁的加载到其开发计算机上的 Linux 分发

## <a name="background"></a>后台
我们为 WSL 作为 UWP 应用程序可以通过 Microsoft Store 分发的 Linux 发行版。 你可以安装这些应用程序，然后将在 WSL-位于 Windows 内核的子系统上运行。 早期的博客文章中所述，此传送机制具有诸多优点。

## <a name="sideloading-a-custom-linux-distro-package"></a>旁加载自定义 Linux 发行版包
可以在你的个人计算机上为旁加载应用程序中创建自定义的 Linux 发行版包。 请注意，除非您作为分发 maintainer 提交后，不会自定义包通过 Microsoft Store 中分发。
若要设置在计算机旁加载应用程序，你将需要"面向开发人员"下的系统设置中启用此功能。  请务必包含开发人员模式或所选旁加载应用

## <a name="for-linux-distro-maintainers"></a>对于 Linux 发行版维护人员
若要提交到应用商店，你将需要与我们通过发布审批。 如果您是希望添加到 Microsoft Store 分发的 Linux 分发所有者，请联系wslpartners@microsoft.com。

## <a name="getting-started"></a>入门
按照上的说明[发行版启动器 GitHub 存储库](https://github.com/Microsoft/WSL-DistroLauncher)创建自定义的 Linux 发行版包。

 
## <a name="team-blogs"></a>团队博客
*  [打开 Linux 分发 Maintainer 和旁加载自定义 Linux 分发版溯源 WSL 示例](https://blogs.msdn.microsoft.com/commandline/2018/03/26/wsl-distro-launcher/)
* [命令行的博客](https://blogs.msdn.microsoft.com/commandline/)

## <a name="provide-feedback"></a>提供反馈
* [发行版启动器 Gitub 存储库](https://github.com/Microsoft/WSL-DistroLauncher)
* [GitHub 问题跟踪程序 WSL](https://github.com/Microsoft/BashOnWindows/issues)
* [命令行 UserVoice 门户](https://wpdev.uservoice.com/forums/266908-command-prompt-console-bash-on-ubuntu-on-windo/category/161892-bash)
