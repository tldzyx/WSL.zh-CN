---
title: 在 Windows 10 上安装适用于 Linux 的 Windows 子系统 (WSL)
description: Windows 10 上适用于 Linux 的 Windows 子系统的安装说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, debian, suse, windows 10, 安装
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 218e3e652d0849f944e8aaceef3fb954294222be
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122769"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>适用于 Linux 的 windows 子系统安装指南 (适用于 Windows 10)

## <a name="install-the-windows-subsystem-for-linux"></a>安装适用于 Linux 的 Windows 子系统

在安装任何 Linux 发行版 for WSL 之前, 必须确保已启用 "适用于 Linux 的 Windows 子系统" 可选功能:

1. 以管理员身份打开 PowerShell 并运行:
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 出现提示时重新启动计算机。

## <a name="install-your-linux-distribution-of-choice"></a>安装所选的 Linux 分发版
若要下载并安装首选发行版, 你有三种选择:
1. 从 Microsoft Store 下载并安装（见下文）
1. 从命令行/脚本下载并安装（[阅读手动安装说明](install-manual.md)）
1. 下载并手动解压缩，然后进行安装（适用于 Windows Server - [此处提供说明](install-on-server.md)）

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 秋季创意者更新及更高版本:从 Microsoft Store 安装

> 此部分适用于 Windows 16215 或更高版本。  请按照相关步骤[检查你的版本](troubleshooting.md#check-your-build-number)。 

1. 打开 Microsoft Store，然后选择你喜爱的 Linux 发行版。

    ![Microsoft Store 中的 Linux 发行版的视图](media/store.png)

    以下链接将打开每个分发的 Microsoft store 页面:

    * [Ubuntu 16.04 LTS](https://www.microsoft.com/store/apps/9pjn388hp8c9)
    * [Ubuntu 18.04 LTS](https://www.microsoft.com/store/apps/9N9TNGVNDL3Q)
    * [OpenSUSE Leap 15](https://www.microsoft.com/store/apps/9n1tb6fpvj8c)
    * [OpenSUSE Leap 42](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SUSE Linux Enterprise Server 12](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [SUSE Linux Enterprise Server 15](https://www.microsoft.com/store/apps/9pmw35d7fnlx)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)
    * [WSL 的 Fedora Remix](https://www.microsoft.com/store/apps/9n6gdm4k2hnc)
    * [Pengwin](https://www.microsoft.com/store/apps/9NV1GV1PXZ6P)
    * [Pengwin 企业](https://www.microsoft.com/store/apps/9N8LP0X93VCP)
    * [Alpine WSL](https://www.microsoft.com/store/apps/9p804crf0395)

1. 在发行版的页面上, 选择 "Get"

    ![Microsoft 应用商店中的 Linux 发行版的视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>完成发行版的初始化
安装 Linux 发行版后，必须先[初始化新的发行版实例](initialize-distro.md)一次，然后才能使用它。

## <a name="troubleshooting"></a>疑难解答： 

以下是相关的错误和建议的修补措施。 有关其他常见错误及其解决方案，请参阅 [WSL 故障排除页](troubleshooting.md)。

* **安装失败, 出现错误0x80070003**
    * 适用于 Linux 的 Windows 子系统仅在系统驱动器（通常为 `C:` 驱动器）上运行。 请确保发行版存储在系统驱动器上：  
    * 打开“设置”->“存储”->“更多存储设置: 更改新内容的保存位置”更改保存**
    新内容的位置,以在C:驱动器上安装应用程序的系统设置图片![](media/AppStorage.png)
    
    
 * **WslRegisterDistribution 失败, 出现错误0x8007019e**   
  * 未启用适用于 Linux 的 Windows 子系统可选组件: 
   * 打开 "**控制面板" "**  -> **程序和功能** ->  **" "打开或关闭 windows" 功能**-> 检查**适用于 Linux 的 windows 子系统**或使用本文开头提到的 PowerShell cmdlet。
