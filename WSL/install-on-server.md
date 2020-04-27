---
title: 在 Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, windows server
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 8859929fe45c9989d367af5f82191162963e6b4f
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256390"
---
# <a name="windows-server-installation-guide"></a>Windows Server 安装指南

> 适用于 Windows Server 2019 及更高版本

在 //Build2017 时，Microsoft 宣布适用于 Linux 的 Windows 子系统将[在 Windows Server 上可用](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)。  这些说明将介绍如何在 Windows Server 1709 及更高版本上运行适用于 Linux 的 Windows 子系统。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>启用适用于 Linux 的 Windows 子系统 (WSL)

必须启用“适用于 Linux 的 Windows 子系统”可选功能并重启，然后才能在 Windows 上运行 Linux 发行版。

1. 以管理员身份打开 PowerShell 并运行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出现提示时，重启计算机。 为了确保 WSL 可以启动可信的执行环境，**必须进行此重启**。

## <a name="download-a-linux-distro"></a>下载 Linux 发行版

按照[这些说明](install-manual.md)下载你最喜爱的 Linux 发行版。

## <a name="extract-and-install-a-linux-distro"></a>提取并安装 Linux 发行版
下载发行版后，请提取其内容，并手动安装该发行版：

1. 提取 `<distro>.appx` 包的内容，例如，使用 PowerShell：

    ```powershell
    Rename-Item .\Ubuntu.appx .\Ubuntu.zip
    Expand-Archive .\Ubuntu.zip .\Ubuntu
    ```

2. 运行发行版启动器来完成安装，请在名为 `<distro>.exe` 的目标文件夹中运行发行版启动器应用程序。 例如：`ubuntu.exe`，等等。

    ![Windows Server 上展开的 Ubuntu 发行版](media/server-appx-expand.png)

    > **疑难解答**
    > * **安装失败并出现错误 0x8007007e**：当系统不支持 WSL 时会出现此错误。 请确保：
    >   * 运行 Windows 内部版本 16215 或更高版本。 [检查内部版本](troubleshooting.md#check-your-build-number)。
    >   * 已启用“适用于 Linux 的 Windows 子系统”可选组件，并已重启计算机。  [确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. 将你的发行版路径添加到 Windows 环境 PATH 中（在本例中为 `C:\Users\Administrator\Ubuntu`），例如，使用 Powershell：
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    现在，你可以从任何路径通过键入 `<distro>.exe` 来启动你的发行版。 例如：`ubuntu.exe`

安装你的 Linux 发行版后，必须先[初始化新的发行版实例](initialize-distro.md)，然后才能使用该发行版。
