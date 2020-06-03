---
title: 更新 WSL 2 Linux 内核
description: 有关如何手动更新 WSL 2 Linux 内核的说明
keywords: wsl, windows, linux 内核, 适用于 Linux 的 Windows 子系统, 内核
ms.date: 03/12/2020
ms.topic: article
ms.localizationpriority: high
ms.openlocfilehash: 1628bea2f1bae590928b055425413e5b085dffef
ms.sourcegitcommit: 90f7caeefe886bf6c0ba2b90c1b56b5f9795ad1b
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/28/2020
ms.locfileid: "84153043"
---
# <a name="updating-the-wsl-2-linux-kernel"></a>更新 WSL 2 Linux 内核

若要手动更新 WSL 2 内的 Linux 内核，请按照以下步骤执行操作。

> [!NOTE] 
> 如果安装程序找不到 WSL 1，请右键单击 Linux 内核更新安装程序，然后按“卸载”，并重新运行安装程序

## <a name="download-the-linux-kernel-update-package"></a>下载 Linux 内核更新包

请[下载适用于 x64 计算机的最新 WSL2 Linux 内核](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_x64.msi)更新包。

> [!NOTE]
> 如果使用的是 ARM64 计算机，请下载 [ARM64 包](https://wslstorestorage.blob.core.windows.net/wslblob/wsl_update_arm64.msi)。

## <a name="install-the-linux-kernel-update-package"></a>安装 Linux 内核更新包

若要安装 Linux 内核更新包，请执行以下操作：

  1. 运行上一步中下载的更新包。

  2. 系统将提示你提供提升的权限，选择“是”以批准此安装。

  3. 安装完成后，便可以开始使用 WSL2 了！

## <a name="future-plans-for-updating-the-wsl2-linux-kernel"></a>有关更新 WSL2 Linux 内核的未来计划

有关详细信息，请参阅 [Windows 命令行博客](https://aka.ms/cliblog)上的文章[对更新 WSL2 Linux 内核的更改](https://devblogs.microsoft.com/commandline/wsl2-will-be-generally-available-in-windows-10-version-2004)。
