---
title: WSL 2 方面的常见问题
description: Frequently Asked Questions about Windows 子系统适用于 Linux 2
keywords: BashOnWindows，bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 84805278abaeb6334c662e1dfab1bced3e0ddb0b
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038087"
---
# <a name="wsl-2-faq"></a>WSL 2 常见问题

下面是一组常见问题 (FAQ) Windows 子系统 Linux 2。

## <a name="does-wsl-2-use-hyper-v-will-it-be-available-on-windows-10-home"></a>WSL 2 是否使用 HYPER-V？ 它将在 Windows 10 家庭版？

WSL 2 将在所有 Sku 上可用的 WSL 是目前不可用，包括 Windows 10 家庭版。

最新版本的 WSL 使用 HYPER-V 体系结构用于支持其虚拟化。 此体系结构可在一个可选组件，是 HYPER-V 功能的子集。 此可选组件将在所有 Sku 上可用。 您有望看到更多详细信息这种体验即将随着我们更接近于 WSL 2 版本。

## <a name="what-will-happen-to-wsl-1-will-it-be-abandoned"></a>WSL 1 会受到什么影响？ 将放弃它？

我们目前尚未计划不推荐使用的 WSL 1。 您可以运行 WSL 1 和 WSL 2 发行版本并排显示，并可以升级和降级任何发行版在任何时间。 将 WSL 2 添加为新的体系结构提供了更好的平台为 WSL 团队提供功能，使 WSL 令人惊叹的方式在 Windows 中运行的 Linux 环境。

## <a name="will-i-be-able-to-run-wsl-2-and-other-3rd-party-virtualization-tools-such-as-vmware-or-virtualbox"></a>我是否能够运行 WSL 2 和 VMware 或 VirtualBox 等其他第三方虚拟化工具？

HYPER-V 是在使用中，这意味着它们将不能启用 WSL 2 时运行，则无法使用某些第三方应用程序。 遗憾的是，此时间包括 VMware 和 VirtualBox VirtualBox 6 之前的版本 (发布于 2018 年 12 月 6.0.0 VirtualBox[现在支持为回退执行核心 Windows 主机上的 HYPER-V] [ 1]!)

我们正在调查的方法，帮助解决此问题。 例如，我们公开了一组 Api 调用[虚拟机监控程序平台][ 2] ，可以使用第三方虚拟化提供程序，使其软件与 HYPER-V 的兼容 这使应用程序使用 HYPER-V 体系结构如其仿真[Google Android 仿真器][3]，和 6 和更高版本的 VirtualBox 均现在与 HYPER-V 兼容。

## <a name="can-i-access-the-gpu-in-wsl-2-are-there-plans-to-increase-hardware-support"></a>可以访问 WSL 2 中的 GPU？ 是否有计划以提高硬件支持？

在 WSL 2 硬件访问的初始版本中支持将受到限制，例如： 你将不能访问 GPU，串行或 USBs。 但是，添加更好的设备支持是我们积压工作上高，因为这将很多更多的使用情况下打开面向开发人员想要对与这些设备进行交互。 在此期间，可以始终使用串行端口和 USB 访问 WSL 1。 请继续关注此博客和 twitter，随时了解最新功能到 insider WSL 团队成员生成，并会在你想要与之交互的设备上提供反馈 ！

## <a name="will-wsl-2-be-able-to-use-networking-applications"></a>WSL 2 能够使用网络应用程序？

是的一般情况下应用程序的网络将更快并更好地工作，因为我们有完整的系统调用兼容性。 但是，新的体系结构使用虚拟化网络组件。 这意味着，在初始预览版中生成 WSL 2 将更类似行为与虚拟机，例如：WSL 2 将具有与主机计算机不同的 IP 地址。 我们致力于 WSL 2 感觉与 WSL 1 相同，包括提高我们网络的故事。 我们预计会快速可以例如在 Linux 或 Windows 使用 localhost 访问网络的所有应用中添加的改进。 我们将发布我们网络的情景和改进有关详细信息如临近 WSL 2 的版本。

## <a name="can-i-run-wsl-2-in-a-virtual-machine"></a>可以在虚拟机中运行 WSL 2？

是的！ 您需要确保虚拟机具有嵌套虚拟化启用。 通过使用管理员权限的 PowerShell 窗口中运行以下命令，可以在 HYPER-V 中启用此：

`Set-VMProcessor -VMName <VMName> -ExposeVirtualizationExtensions $true`

请务必替换&lt;VMName&gt;与虚拟机的名称。

 [1]: https://www.virtualbox.org/wiki/Changelog-6.0
 [2]: https://docs.microsoft.com/en-us/virtualization/api/
 [3]: https://devblogs.microsoft.com/visualstudio/hyper-v-android-emulator-support/