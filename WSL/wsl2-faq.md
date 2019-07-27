---
title: WSL 2 常见问题
description: 有关适用于 Linux 2 的 Windows 子系统的常见问题
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10, 安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a74f5e3f5879d0af274d2e2b10aaf05e95a97a6f
ms.sourcegitcommit: 44da0f435986598e6067e36ddca9369d27064793
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/26/2019
ms.locfileid: "67587144"
---
# <a name="wsl-2-faq"></a>WSL 2 常见问题

下面是有关适用于 Linux 2 的 Windows 子系统的常见问题 (FAQ) 列表。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 是否使用 Hyper-v？ 它是否可用于 Windows 10 家庭版？

WSL 2 将在所有 WSL 当前可用的 Sku 上可用, 包括 Windows 10 家庭版。

最新版本的 WSL 使用 Hyper-v 体系结构来实现其虚拟化。 此体系结构将出现在 "虚拟机平台" 可选组件中。 此可选组件将在所有 Sku 上可用。 当我们更深入地了解 WSL 2 版本时, 可以看到更多有关此体验的详细信息。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 将发生什么情况？ 是否放弃？

目前没有计划弃用 WSL 1。 你可以并行运行 WSL 1 和 WSL 2 发行版, 还可以随时升级和降级任何发行版。 将 WSL 2 添加为新的体系结构, 为 WSL 团队提供了一个更好的平台, 使其能够提供 WSL 一种令人惊叹的方式在 Windows 中运行 Linux 环境的功能。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>我是否能够运行 WSL 2 和其他第三方虚拟化工具 (如 VMware) 或 VirtualBox？

当使用 Hyper-v 时, 某些第三方应用程序无法正常工作, 这意味着当启用 WSL 2 时, 这些应用程序将无法运行。 遗憾的是, 在2018年12月6日发布的 VirtualBox 6.0.0 之前, 这包括 VMware 和 VirtualBox 的版本,[现在支持在 Windows 主机上将 hyper-v 作为回退执行核心][1]!)

我们正在研究帮助解决此问题的方法。 例如, 我们公开一组称为[虚拟机监控程序平台][2]的 api, 第三方虚拟化提供程序可以使用它来使软件与 hyper-v 兼容。 这样, 应用程序就可以使用 Hyper-v 体系结构进行仿真, 如[Google Android Emulator][3], 以及 VirtualBox 6 及更高版本, 它们现在都与 hyper-v 兼容。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>能否在 WSL 2 中访问 GPU？ 是否计划增加硬件支持？

在 WSL 2 的初始版本中, 将限制硬件访问支持, 例如: 你将无法访问 GPU、串行或 USBs。 但是, 在积压工作 (backlog) 上添加更好的设备支持更高, 因为这会为希望与这些设备进行交互的开发人员打开更多用例。 同时, 你始终可以使用具有串行端口和 USB 访问权限的 WSL 1。 请继续关注此博客并 WSL Twitter 上的团队成员, 随时了解即将到来的内部版本的最新功能, 并向我们提供有关你想要与之交互的设备的反馈!

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 是否能够使用网络应用程序？

是的, 在常规网络应用程序中, 可以更快、更好地工作, 因为我们具有完全的系统调用兼容性。 但是, 新的体系结构使用虚拟化的网络组件。 这意味着, 在初始预览版本中, WSL 2 的行为将更类似于虚拟机, 例如:WSL 2 的 IP 地址将与主机不同。 我们承诺使 WSL 2 感觉与 WSL 1 相同, 这包括改善我们的网络故事。 我们希望尽快添加改进, 如使用 localhost 从 Linux 或 Windows 访问所有网络应用。 我们将在 WSL 2 的发布时, 公布有关网络故事和改进的更多详细信息。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>能否在虚拟机中运行 WSL 2？

可以！ 你需要确保虚拟机已启用嵌套虚拟化。 在 Hyper-v 中, 可以通过使用管理员权限在 PowerShell 窗口中运行以下命令来启用此功能:

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

请确保将 "&lt;VMName&gt;" 替换为虚拟机的名称。

## <a name="can-i-use-wslconf-in-wsl-2"></a>能否在 WSL 2 中使用 wsl？

WSL 2 支持 WSL 1 使用的同一个 WSL 文件。 这意味着, 在 WSL 1 发行版中设置的任何配置选项 (如 automounting Windows 驱动器、启用或禁用互操作、更改 Windows 驱动器将装载到的目录等) 都将在 WSL 2 内部工作。 可在[发行版管理](./wsl-config.md)页的 WSL 中了解有关配置选项的详细信息。 

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/