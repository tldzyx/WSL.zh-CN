---
title: 关于 WSL 2
description: 关于 WSL 2 适用于 Linux 的 Windows 子系统的新体系结构
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: e9c1f043207193a5c00ecf6176f54f240aa48680
ms.sourcegitcommit: 5844c6dbf692780b86b30bd65e11820fff43b3bd
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/02/2019
ms.locfileid: "67499259"
---
# <a name="about-wsl-2"></a>关于 WSL 2

WSL 2 是体系结构的一种新版本, 它支持适用于 Linux 的 Windows 子系统在 Windows 上运行 ELF64 Linux 二进制文件。 它的主要目标是提高文件系统的性能, 并增加系统调用的完全兼容性。 这一新的体系结构更改了这些 Linux 二进制文件如何与 Windows 和计算机的硬件交互, 但仍提供与 WSL 1 (当前广泛可用的版本) 相同的用户体验。 单个 Linux 发行版可以作为 WSL 1 发行版或 WSL 2 发行版运行, 随时可以进行升级或降级, 还可以同时运行 WSL 1 和 WSL 2 发行版。 WSL 2 使用全新的体系结构, 该体系结构使用实际 Linux 内核。

## <a name="linux-kernel-in-wsl-2"></a>WSL 2 中的 Linux 内核

WSL 2 中的 Linux 内核内置于最新稳定分支中, 基于 kernel.org 提供的源。此内核已专门针对 WSL 2 进行了优化。 它已针对大小和性能进行了优化, 可在 Windows 上提供令人惊叹的 Linux 体验, 并将通过 Windows 更新提供服务, 这意味着你将获得最新的安全修补程序和内核改进, 而无需你自行管理。

此外, 此内核将为开源。 可在[此处](https://github.com/microsoft/WSL2-Linux-Kernel)找到 Linux 内核的完整源代码。 如果你想要了解有关此内核的详细信息, 可以查看[此博客文章](https://devblogs.microsoft.com/commandline/shipping-a-linux-kernel-with-windows/), 其中由生成它的团队撰写。

## <a name="brief-overview-of-the-wsl-2-architecture"></a>WSL 2 体系结构的简要概述

WSL 2 使用最新和最高的虚拟化技术在轻型实用程序虚拟机 (VM) 内部运行 Linux 内核。 但是, WSL 2 不会成为传统的 VM 体验。 传统的 VM 体验启动速度慢, 隔离, 消耗大量资源, 需要你的时间进行管理。 WSL 2 没有这些属性。 它仍将为 WSL 1 带来优异的好处:Windows 和 Linux 的高级集成、极快的启动时间、小资源占用量, 并且最重要的是, 不需要 VM 配置或管理。 尽管 WSL 2 使用 VM, 但会管理并在后台运行, 从而使你拥有与 WSL 1 相同的用户体验。

## <a name="increased-file-io-performance"></a>文件 IO 性能提高

文件密集型操作 (如 git 克隆、npm 安装、apt 更新、apt 升级等) 都将以更快的速度显著提高。 实际的速度提高将取决于正在运行的应用以及与文件系统交互的方式。 WSL 2 的初始版本与 WSL 1 相比, 在打开 zipped tarball 时, 运行最多20倍速度, 在使用 git 克隆时, 可在不同项目中安装和 npm cmake。

## <a name="full-system-call-compatibility"></a>完全系统调用兼容性

Linux 二进制文件使用系统调用来执行许多功能, 例如访问文件、请求内存、创建进程等。 尽管 WSL 1 使用 WSL 团队生成的翻译层, WSL 2 还包括其自己的 Linux 内核, 并且具有完全系统调用兼容性。 这会引入一个全新的应用程序集, 这些应用程序可在 WSL 内运行, 例如 Docker 等。 此外, 对 Linux 内核的任何更新都可以立即准备好添加到计算机, 而不是等待 WSL 团队实施更改, 然后再添加它们。