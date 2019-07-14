---
title: Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 windows server 的 windows 子系统
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: 25723395212575f8fe2dcbfbd30b59de9431816a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67035075"
---
# <a name="windows-server-installation-guide"></a>Windows Server 安装指南

> 适用于 Windows Server 2019 和更高版本

在 //Build2017，Microsoft 宣布适用于 Linux 的 Windows 子系统[将在 Windows Server 上提供](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。这些说明将介绍如何在 Windows Server 1709 及更高版本上运行适用于 Linux 的 Windows 子系统。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>启用适用于 Linux 的 Windows 子系统 (WSL)

在 Windows 上运行 Linux 发行版之前，您必须启用“适用于 Linux 的 Windows 的子系统”可选功能并重新启动。

1. 以管理员身份打开 PowerShell 并运行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出现提示时重新启动计算机。**需要重新启动**是为了确保 WSL 可以启动受信任的执行环境。

## <a name="download-a-linux-distro"></a>下载 Linux 发行版

请按照[这些说明](install-manual.md)下载您最喜爱的 Linux 发行版。

## <a name="extract-and-install-a-linux-distro"></a>提取并安装 Linux 发行版
既然您已经下载发行版，提取其内容，并手动安装发行版：

1. 提取`<distro>.appx`包的内容，例如，使用 PowerShell:

    ```powershell
    Rename-Item ~/Ubuntu.appx ~/Ubuntu.zip
    Expand-Archive ~/Ubuntu.zip ~/Ubuntu
    ```

2. 运行发行版启动器要完成安装，请运行发行版启动器应用程序目标文件夹中名为`<distro>.exe`。 例如： `ubuntu.exe`，等等。

    ![Windows Server 上的展开的 Ubuntu 发行版](media/server-appx-expand.png)

    > **疑难解答**
    > * **安装失败，出现错误 0x8007007e**:您的系统不支持 WSL 时发生此错误。 请确保：
    >   * 正在运行 Windows build 16215 或更高版本。 [检查你的版本号](troubleshooting.md#check-your-build-number)。
    >   * 适用于 Linux 的 Windows 子系统可选组件已启用，并重新启动计算机。  [请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. 将你的发行版路径添加到 Windows 环境路径 (在此示例中为`C:\Users\Administrator\Ubuntu`)，例如，使用 Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    您现在可以通过键入`<distro>.exe`从任何路径启动发行版。例如：`ubuntu.exe`

安装 Linux 发行版后，您必须在使用发行版之前[初始化新的发行版实例](initialize-distro.md)。
