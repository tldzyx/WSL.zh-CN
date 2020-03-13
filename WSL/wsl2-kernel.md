---
title: 更新 WSL 2 Linux 内核
description: 有关如何手动更新 WSL 2 Linux 内核的说明
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, wsl.conf, wslconfig
ms.date: 03/12/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: edc7ea35d8ebe0c71488763017cde2bb45c53b6d
ms.sourcegitcommit: 8795e1c4c5d2efdc8a9c78af05fb7be3ac1eef3d
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/12/2020
ms.locfileid: "79138186"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>更新 WSL 2 Linux 内核

若要手动更新 WSL 2 内的 Linux 内核，请遵循以下步骤。 

## <a name="download-the-linux-kernel-update-package"></a>下载 Linux 内核更新包

请单击[此链接](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)，下载适用于 AMD64 计算机的最新 WSL2 Linux 内核更新包。

> [!NOTE] 如果使用的是 ARM64 计算机，请改为下载[此包](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)。

## <a name="install-the-linux-kernel-update-package"></a>安装 Linux 内核更新包

若要安装 Linux 内核更新包：
    1. 运行上一步中下载的更新包。
    2. 系统将提示你提供提升的权限，选择 "是" 以批准此安装。
    3. 安装完成后，便可以开始使用 WSL2 了！

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>更新 WSL2 Linux 内核的未来计划

有关这些更改的详细信息，请在[Windows 命令行博客](https://aka.ms/cliblog)上阅读[此博客文章](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)。