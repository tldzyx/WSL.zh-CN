---
title: 在 Windows 10 上安装适用于 Linux 的 Windows 子系统 (WSL)
description: 有关在 Windows 10 上安装适用于 Linux 的 Windows 子系统的说明。
keywords: BashOnWindows, bash, wsl, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 17ca32db23b426ef1367ff9444b5924d9d7e1716
ms.sourcegitcommit: 3be576f946611cf36e27745bdb7c4c52af1b9928
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2019
ms.locfileid: "74200236"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>适用于 Linux 的 Windows 子系统安装指南 (Windows 10)

## <a name="install-the-windows-subsystem-for-linux"></a>安装适用于 Linux 的 Windows 子系统

在安装适用于 WSL 的任何 Linux 分发版之前，必须确保已启用“适用于 Linux 的 Windows 子系统”可选功能：

1. 以管理员身份打开 PowerShell 并运行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出现提示时，重启计算机。

## <a name="install-your-linux-distribution-of-choice"></a>安装所选的 Linux 分发版
若要下载并安装首选的分发版，可以选择三种做法：
* 从 Microsoft Store 下载并安装（参阅下文）
* 从命令行/脚本下载并安装（[阅读手动安装说明](install-manual.md)）
* 下载并手动解压缩和安装（适用于 Windows Server - [参阅此处的说明](install-on-server.md)）

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 和更高版本：从 Microsoft Store 安装

> 本部分适用于 Windows 内部版本 16215 或更高版本。  遵循以下步骤[检查内部版本](troubleshooting.md#check-your-build-number)。 

1. 打开 Microsoft Store，并选择你偏好的 Linux 分发版。

    ![Microsoft Store 中的 Linux 分发版视图](media/store.png)

    单击以下链接会打开每个分发版的 Microsoft Store 页面：

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [Fedora Remix for WSL](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin Enterprise](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. 在分发版的页面中，选择“获取”

    ![Microsoft Store 中的 Linux 分发版视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>完成分发版的初始化
安装 Linux 分发版后，必须先[初始化新的分发版实例](initialize-distro.md)一次才能使用该分发版。

## <a name="troubleshooting"></a>疑难解答： 

下面是相关的错误和建议的修复措施。 有关其他常见错误及其解决方法，请参阅 [WSL 故障排除页](troubleshooting.md)。

* **安装失败并出现错误 0x80070003**
    * 适用于 Linux 的 Windows 子系统只能在系统驱动器（通常是 `C:` 驱动器）中运行。 请确保将分发版存储在系统驱动器上：  
    * 打开“设置”->“存储”->“更多存储设置:    更改新内容的保存位置”
    ![用于在 C: 驱动器中安装应用的系统设置屏幕截图](media/AppStorage.png)
    
    
 * **WslRegisterDistribution 失败并出现错误 0x8007019e**   
  * 未启用“适用于 Linux 的 Windows 子系统”可选组件： 
   * 打开“控制面板” -> “程序和功能” -> “打开或关闭 Windows 功能”-> 选中“适用于 Linux 的 Windows 子系统”，或使用本文开头所述的 PowerShell cmdlet。    
