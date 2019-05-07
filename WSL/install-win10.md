---
title: Windows 子系统适用于 Linux (WSL) 上 Windows 10 上安装
description: 适用于 Windows 10 上的 Linux 安装说明 Windows 子系统。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: taraj
ms.author: taraj
ms.date: 07/23/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 40bbe73acbfd0483e18ab6ff1696fdb44eaff2e4
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063285"
---
# <a name="windows-subsystem-for-linux-installation-guide-for-windows-10"></a>Linux 安装指南适用于 Windows 10 的 Windows 子系统

## <a name="install-the-windows-subsystem-for-linux"></a>安装适用于 Linux 的 Windows 子系统

在之前安装 WSL 任何 Linux 发行版，您必须确保"Windows 子系统为 Linux"已启用可选功能：

1. 以管理员身份打开 PowerShell 并运行：
    ```powershell
    Enable-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
    ```

2. 重新启动计算机时提示。

## <a name="install-your-linux-distribution-of-choice"></a>安装所选的 Linux 分发版
若要下载并安装你首选的 distro(s)，您具有三个选项：
1. 下载并安装来自 Windows 应用商店 （见下文）
1. 从命令行/脚本下载并安装 ([读取手动安装说明](install-manual.md))
1. 下载和手动解压缩并安装 (适用于 Windows Server-[此处的说明](install-on-server.md))

### <a name="windows-10-fall-creators-update-and-later-install-from-the-microsoft-store"></a>Windows 10 Fall Creators Update 及更高版本：从 Microsoft Store 安装

> 本部分是为 Windows 生成 16215 或更高版本。  请按照这些步骤[检查你的生成](troubleshooting.md#check-your-build-number)。 

1. 打开 Microsoft Store，然后选择你喜爱的 Linux 分发。

    ![在 Windows 应用商店中的 Linux 发行版的视图](media/store.png)

    以下链接将打开每个分布区的 Windows 应用商店页：

    * [Ubuntu](https://www.microsoft.com/store/p/ubuntu/9nblggh4msv6)
    * [OpenSUSE](https://www.microsoft.com/store/apps/9njvjts82tjx)
    * [SLES](https://www.microsoft.com/store/apps/9p32mwbh6cns)
    * [Kali Linux](https://www.microsoft.com/store/apps/9PKR34TNCV07)
    * [Debian GNU/Linux](https://www.microsoft.com/store/apps/9MSVKQC78PK6)

1. 从发行版的页上，选择"Get"

    ![在 Windows 应用商店中的 Linux 发行版的视图](media/UbuntuStore.png)

## <a name="complete-initialization-of-your-distro"></a>完成初始化的发行版
安装 Linux 发行版后，您必须[初始化新的发行版实例](initialize-distro.md)一次，然后才能使用。

## <a name="troubleshooting"></a>疑难解答： 

以下是相关的错误的建议修补程序。 请参阅[WSL 故障排除页](troubleshooting.md)其他常见的错误和其解决方案。

* **安装失败，出现错误 0x80070003**
    * 系统驱动器上仅运行于 Linux 的 Windows 子系统 (通常这是你`C:`驱动器)。 请确保发行版都存储在您的系统驱动器上：  
    * 打开**设置** -> **存储** -> **更多的存储设置：保存新内容的更改**
    ![的系统设置的图片 c： 驱动器上安装应用](media/AppStorage.png)
