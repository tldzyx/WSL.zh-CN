---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows，bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 2af43a046333fc8c7b4142cdc5077cdfbf29fea7
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038077"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 的安装说明

若要安装和开始使用 WSL 2，请完成以下步骤：

- 启用虚拟机平台可选组件
- 设置要由 WSL 2： 使用命令行支持的发行版
- 验证正在使用的版本的 WSL 在发行版

## <a name="enable-the-virtual-machine-platform-optional-component"></a>启用虚拟机平台可选组件

以管理员身份打开 PowerShell 并运行：

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

这些更改才会启用后，需要重新启动计算机。

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>设置要由 WSL 2： 使用命令行支持的发行版

在 PowerShell 中运行：

`wsl --set-version <Distro> 2`

请务必替换和`<Distro>`发行版的实际名称。 (您可以找到这些命令： `wsl -l`)。 您可以改回为 WSL 1 随时通过按上述方式运行同一命令，但替换为"2"与"1"。

此外，如果你想要 WSL 2 默认体系结构就可以做到使用以下命令：

`wsl --set-default-version 2`

这将使任何新安装的发行版将初始化为 WSL 2 发行版。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>完成并验证 WSL 发行版的版本使用

若要验证哪些版本的 WSL 使用每个发行版，请使用以下命令：

`wsl --list --verbose` 或 `wsl -l -v`

选择上面的发行版此时应显示"2"的版本列下。 现在，完成后随时开始使用 WSL 2 发行版 ！ 