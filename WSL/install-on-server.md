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
ms.openlocfilehash: c0b8af08a06428ebd292b8c6b9b275726988bdbe
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063615"
---
# <a name="windows-server-installation-guide"></a>Windows Server 安装指南

> 适用于 Windows Server 2019 和更高版本

在 / / Build2017，Microsoft 宣布将适用于 Linux 的 Windows 子系统[可在 Windows Server 上](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。  这些说明了解如何运行适用于 Linux 的 Windows Server 1709 及更高版本的 Windows 子系统。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>适用于 Linux (WSL) 启用的 Windows 子系统

您可以在 Windows 上运行的 Linux 发行版之前，必须启用"Windows 子系统适用于 Linux"可选功能，并重新启动。

1. 以管理员身份打开 PowerShell 并运行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 重新启动计算机时提示。 **需要此重新启动后**为了确保 WSL 可以启动的可信的执行环境。

## <a name="download-a-linux-distro"></a>下载的 Linux 发行版

请按照[这些说明](install-manual.md)若要下载你最喜爱的 Linux 分发。

## <a name="extract-and-install-a-linux-distro"></a>提取和安装的 Linux 发行版
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
    >   * 正在运行 Windows 生成 16215 或更高版本。 [检查你的生成](troubleshooting.md#check-your-build-number)。
    >   * Linux 可选组件的 Windows 子系统，并重新启动计算机。  [请确保启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. 将你的发行版路径添加到 Windows 环境路径 (`C:\Users\Administrator\Ubuntu`在此示例中)，例如，使用 Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + "C:\Users\Administrator\Ubuntu", "User")
    ```
    现在可以启动任何路径从发行版，通过键入`<distro>.exe`。 例如： `ubuntu.exe`

安装 Linux 发行版后，您必须[初始化新的发行版实例](initialize-distro.md)之前使用发行版。
