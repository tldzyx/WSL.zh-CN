---
title: 安装 WSL 2
description: WSL 2 的安装说明
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 91bd479e922fc29bf11b89dcfe06fa381632c4fa
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520546"
---
# <a name="installation-instructions-for-wsl-2"></a>WSL 2 的安装说明

你可以观看下面的视频，或者继续阅读本文以了解如何安装 WSL2。 

> [!VIDEO https://channel9.msdn.com/Blogs/One-Dev-Minute/Learn-how-to-install-WSL-2/player]

若要安装并开始使用 WSL 2，请完成以下步骤：

> WSL 2 仅适用于 Windows 10 版本 18917 或更高版本

- 请确保你已安装 WSL（可以在[此处](./install-win10.md)找到有关执行此操作的说明），并且运行的是 Windows 10 **版本 18917** 或更高版本
   - 若要确保使用的是版本 18917 或更高版本，请加入 [Windows 预览体验计划](https://insider.windows.com/en-us/)并选择“快速”环或“慢速”环形。 
   - 可以通过打开命令提示符并运行 `ver` 命令来检查 Windows 版本。
- 启用“虚拟机平台”可选组件
- 使用命令行设置要由 WSL 2 支持的发行版
- 验证发行版使用的 WSL 版本

## <a name="enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled"></a>启用“虚拟机平台”可选组件并确保启用了 WSL

你需要确保同时安装了”适用于 Linux 的 Windows 子系统”和”虚拟机平台”可选组件。 可以通过在 PowerShell 中运行以下命令来执行该操作： 

```powershell
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

请重启计算机来完成两个组件的安装。


## <a name="set-a-distro-to-be-backed-by-wsl-2-using-the-command-line"></a>使用命令行设置要由 WSL 2 支持的发行版

如果尚未安装 Linux 发行版，请参阅[在 Windows 10 上安装](./install-win10.md#install-your-linux-distribution-of-choice)文档页，以获取有关进行安装的说明。 

若要设置发行版，请运行： 

```
wsl --set-version <Distro> 2
```

并且确保将 `<Distro>` 替换为你的发行版的实际名称。 （可使用以下命令找到这些内容：`wsl -l`）。 可以随时更改回 WSL 1，方法是运行与上面相同的命令，但将“2”替换为“1”。

此外，如果要使 WSL 2 成为你的默认体系结构，可以通过此命令执行该操作：

```
wsl --set-default-version 2
```

这会使你安装的任何新发行版均初始化为 WSL 2 发行版。

## <a name="finish-with-verifying-what-versions-of-wsl-your-distro-are-using"></a>完成验证发行版使用的 WSL 版本

若要验证每个发行版使用的 WSL 版本，请使用以下命令（仅在 Windows 版本 18917 或更高版本中可用）：

`wsl --list --verbose` 或 `wsl -l -v`

上面选择的发行版现在应在“version”列下显示“2”。 既然已经完成，便可以随时开始使用 WSL 2 发行版了！ 

## <a name="troubleshooting"></a>故障排除： 

下面是安装 WSL 2 时的相关错误和建议的修补程序。 请参阅 [WSL 故障排除页](troubleshooting.md)以了解其他常见的 WSL 错误及其解决方案。

* **安装失败，出现错误 0x80070003 或错误 0x80370102**
    * 请确保在计算机的 BIOS 内已启用虚拟化。 有关如何执行此操作的说明因计算机而异，并且很可能在 CPU 相关选项下。
   
* **尝试升级时出错：`Invalid command line option: wsl --set-version Ubuntu 2`**
    * 请确保已启用适用于 Linux 的 Windows 子系统，并且你使用的是 Windows 内部版本 18917 或更高版本。 若要启用 WSL，请在 Powershell 提示符下以具有管理员权限的身份运行此命令：`Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux`。 可在[此处](./install-win10.md)找到完整的 WSL 安装说明。

* **由于虚拟磁盘系统的某个限制，无法完成所请求的操作。虚拟硬盘文件必须是解压缩的且未加密的，并且不能是稀疏的。**
    * 请检查 [WSL Github 主题 #4103](https://github.com/microsoft/WSL/issues/4103)，其中跟踪了此问题以提供更新的信息。

* **无法将词语“wsl”识别为 cmdlet、函数、脚本文件或可运行程序的名称。** 
    * 请确保[已安装“适用于 Linux 的 Windows 子系统”可选组件](./wsl2-install.md#enable-the-virtual-machine-platform-optional-component-and-make-sure-wsl-is-enabled)。<br> 此外，如果你使用的是 Arm64 设备，并从 PowerShell 运行此命令，则会收到此错误。 请改为从 [PowerShell Core](https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-windows?view=powershell-6) 或从命令提示符运行 `wsl.exe`。 
