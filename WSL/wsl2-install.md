---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0220d642854f9fc7fe2a85357ad2e70e0b888ed8
ms.sourcegitcommit: f878e88921d36e01e32624a9c60ee9de3d706a2e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/19/2019
ms.locfileid: "69620099"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 的安装说明

若要安装并开始使用 WSL 2，请完成以下步骤：

- 确保已安装 WSL (可以在[此处](./install-win10.md)找到相关说明), 并且运行的是 Windows 10 内部版本18917或更高版本
- 启用“虚拟机平台”可选组件
- 使用命令行设置要由 WSL 2 支持的发行版
- 验证发行版使用的 WSL 版本

## <a name="enable-the-virtual-machine-platform-optional-component"></a>启用“虚拟机平台”可选组件

以管理员身份打开 PowerShell 并运行：

`Enable-WindowsOptionalFeature -Online -FeatureName VirtualMachinePlatform`

启用这些更改后，需要重新启动计算机。

## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>使用命令行设置要由 WSL 2 支持的发行版

在 PowerShell 中运行：

`wsl --set-version <Distro> 2`

并且确保将 `<Distro>` 替换为你的发行版的实际名称。 （可使用以下命令找到这些内容：`wsl -l`）。 可以随时更改回 WSL 1，方法是运行与上面相同的命令，但将“2”替换为“1”。

此外，如果要使 WSL 2 成为你的默认体系结构，可以通过此命令执行该操作：

`wsl --set-default-version 2`

这会使你安装的任何新发行版均初始化为 WSL 2 发行版。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>完成验证发行版使用的 WSL 版本

若要验证每个发行版使用的 WSL 版本，请使用以下命令：

`wsl --list --verbose` 或 `wsl -l -v`

上面选择的发行版现在应在“version”列下显示“2”。 既然已经完成，便可以随时开始使用 WSL 2 发行版了！ 

## <a name="troubleshooting"></a>疑难解答： 

下面是安装 WSL 2 时的相关错误和建议的修补程序。 请参阅 [WSL 故障排除页](troubleshooting.md)以了解其他常见的 WSL 错误及其解决方案。

* **安装失败，出现错误 0x80070003 或错误 0x80370102**
    * 请确保在计算机的 BIOS 内已启用虚拟化。 有关如何执行此操作的说明因计算机而异，并且很可能在 CPU 相关选项下。
   
* **尝试升级时出错：`Invalid command line option: wsl --set-version Ubuntu 2`**
    * 请确保已启用适用于 Linux 的 Windows 子系统，并且你使用的是 Windows 内部版本 18917 或更高版本。 若要启用 WSL，请在 Powershell 提示符下以具有管理员权限的身份运行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。 可在[此处](./install-win10.md)找到完整的 WSL 安装说明。