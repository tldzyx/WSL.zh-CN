---
title: 在 Windows Server 上安装 Linux 子系统
description: Windows Server 上的 Linux 子系统的安装说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, windows server
author: scooley
ms.author: scooley
ms.date: 05/22/2018
ms.topic: article
ms.assetid: 9281ffa2-4fa9-4078-bf6f-b51c967617e3
ms.custom: seodec18
ms.openlocfilehash: d295cf3db99fb45b943369f532f7e807a603061c
ms.sourcegitcommit: 8b5a8d49b63441478dd540887f534dcc6dd0ba41
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2019
ms.locfileid: "67308792"
---
# <a name="windows-server-installation-guide"></a>Windows Server 安装指南

> 适用于 Windows Server 2019 及更高版本

在//Build2017 上, Microsoft 宣布 windows [Server 上将提供](https://blogs.technet.microsoft.com/hybridcloud/2017/05/10/windows-server-for-developers-news-from-microsoft-build-2017/)适用于 Linux 的 windows 子系统。  这些说明介绍了如何在 Windows Server 1709 和更高版本上运行适用于 Linux 的 Windows 子系统。

## <a name="enable-the-windows-subsystem-for-linux-wsl"></a>启用适用于 Linux 的 Windows 子系统 (WSL)

在 Windows 上运行 Linux 发行版之前, 必须启用 "适用于 Linux 的 Windows 子系统" 可选功能, 然后重新启动。

1. 以管理员身份打开 PowerShell 并运行:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出现提示时, 请重新启动计算机。 **需要重新启动**才能确保 WSL 可以启动受信任的执行环境。

## <a name="download-a-linux-distro"></a>下载 Linux 发行版

按照[以下说明](install-manual.md)下载最喜爱的 Linux 分发版。

## <a name="extract-and-install-a-linux-distro"></a>提取并安装 Linux 发行版
下载发行版后, 请提取其内容, 并手动安装发行版:

1. `<distro>.appx`提取包的内容, 例如, 使用 PowerShell:

    ```powershell
    Rename-Item ./Ubuntu.appx ./Ubuntu.zip
    Expand-Archive ./Ubuntu.zip ./Ubuntu
    ```

2. 运行发行版启动器以完成安装, 并在名为`<distro>.exe`的目标文件夹中运行发行版启动器应用程序。 例如: `ubuntu.exe`等。

    ![Windows Server 上的扩展 Ubuntu 发行版](media/server-appx-expand.png)

    > **疑难解答**
    > * **安装失败, 出现错误 0x8007007e**:当你的系统不支持 WSL 时, 会出现此错误。 请确保：
    >   * 你正在运行 Windows 版本16215或更高版本。 [检查生成](troubleshooting.md#check-your-build-number)。
    >   * 已启用适用于 Linux 的 Windows 子系统可选组件, 并已重新启动计算机。  [请确保已启用 WSL](troubleshooting.md#confirm-wsl-is-enabled)。
    
3. 向 Windows 环境路径 (`C:\Users\Administrator\Ubuntu`此示例中为) 添加发行版路径, 例如, 使用 Powershell:
        
    ```powershell
    $userenv = [System.Environment]::GetEnvironmentVariable("Path", "User")
    [System.Environment]::SetEnvironmentVariable("PATH", $userenv + ";C:\Users\Administrator\Ubuntu", "User")
    ```
    你现在可以通过键入`<distro>.exe`从任何路径启动发行版。 例如：`ubuntu.exe`

安装 Linux 发行版后, 必须先[初始化新的发行版实例](initialize-distro.md), 然后才能使用发行版。
