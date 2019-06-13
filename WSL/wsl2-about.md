---
title: 有关 WSL 2
description: 有关 WSL 2 于 Linux 的 Windows 子系统的新体系结构
keywords: BashOnWindows，bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: b3b0b1ce0f55fed0b4cf223ccc18a509dcf81788
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038127"
---
WSL 2 是为在 Windows 上运行 ELF64 Linux 二进制文件的 linux 操作系统的 Windows 子系统提供支持的体系结构的新版本。 其主要目标是提高文件系统性能，以及添加完整的系统调用兼容性。 此新体系结构更改这些 Linux 二进制文件如何与 Windows 和计算机的硬件进行交互，但仍提供了相同的用户体验，如 WSL 1 （当前广泛可用版本） 中所示。 可以升级或降级在任何时候，单个 Linux 作为 WSL 1 的发行版，或 WSL 2 发行版中，可以运行发行版，您可以运行 WSL 1 和 WSL 2 发行版本并排显示。 WSL 2 使用使用真实的 Linux 内核的全新体系结构。

## <a name="linux-kernel-in-wsl-2"></a>在 WSL 2 中的 Linux 内核

Linux 内核在 WSL 2 构建最新稳定分支，基于 kernel.org 在源中的内部。此类内核专门优化 WSL 2。 它已针对大小和性能，以便在 Windows 上的令人惊叹的 Linux 体验进行优化，并将接受通过 Windows 更新，这意味着您将获得最新安全修补程序和内核改进而无需自行管理。

此外，此类内核将是开放源代码。 Linux 内核中可找到完整的源代码[此处](https://thirdpartysource.microsoft.com/download/Windows%20Subsystem%20for%20Linux%20v2/May%202019/WSLv2-Linux-Kernel-master.zip)。 如果你想要阅读更多有关您可以签出此内核[这篇博客文章](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/)由构建它的团队编写。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 体系结构的简要概述

WSL 2 使用最新和最大虚拟化技术中运行其轻量级实用工具虚拟机 (VM) 内部的 Linux 内核。 但是，WSL 2 就不是传统的 VM 体验。 传统 VM 体验可能启动较慢，是隔离、 会消耗大量资源，需要您的时间来对其进行管理。 WSL 2 不具有这些属性。 它仍具有 WSL 1 的非凡优势：高级别的 Windows 和 Linux、 极快的启动时间、 小型资源占用量和最重要的是之间的集成，需要没有 VM 配置或管理。 虽然 WSL 2 使用 VM，它将管理并且只会留下 WSL 1 相同的用户体验与在后台运行。

## <a name="increased-file-io-performance"></a>增加的文件的 IO 性能

之类的 git 克隆文件密集型操作，npm 安装、 apt 更新、 apt 升级和的详细信息所有将明显更快。 实际速度增加将取决于哪些应用上正在运行且如何与文件系统进行交互。 初始版本 WSL 2 的运行速度更快达 20 个 x 解压缩的压缩的 tarball 和围绕比 WSL 1 2-5 x 的各种项目使用 git 克隆、 npm 安装和 cmake 时更快。

## <a name="full-system-call-compatibility"></a>完整的系统调用兼容性

Linux 二进制文件使用系统调用来执行许多功能，如访问文件、 请求内存，创建过程，和的详细信息。 WSL 1 使用由 WSL 团队生成一个转换层，而 WSL 2 包括完整的系统调用兼容其自己的 Linux 内核。 这就引入了一整套全新的应用程序可以在 WSL，如 Docker 等内运行。 此外，对 Linux 内核的任何更新可能会立即准备好添加到您的计算机，而不是等待 WSL 团队实现所做的更改，然后让这些添加。