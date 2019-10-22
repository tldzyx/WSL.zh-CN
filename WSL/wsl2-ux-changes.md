---
title: WSL 1 与 WSL 2 的用户体验差异
description: WSL 1 与 WSL 2 的用户体验差异
keywords: BashOnWindows、bash、wsl、wsl2、windows、适用于 linux、windowssubsystem、ubuntu、debian、suse、windows 10 的 windows 子系统
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 1af9646b9b5bb845dd60e5bf2312f8d806fca5dc
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269876"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 与 WSL 2 的用户体验差异

此页主要描述 WSL 1 和 WSL 2 预览版之间的用户体验差异。 关键差异包括：

- 将 Linux 应用需要访问的文件放在 Linux 根文件系统中可以提高文件访问速度
- 在 WSL 2 预览版的初始版本中，你需要使用 IP 地址而不是 localhost 来访问网络应用程序

下面是可能会注意到的差异的完整列表：

- WSL 2 使用[虚拟硬件磁盘](https://en.wikipedia.org/wiki/VHD_(file_format))（VHD）来存储文件，如果达到其最大大小，则可能需要将其扩展
- 启动时，WSL 2 现在将使用少量内存
- 初始预览版本中，跨 OS 文件访问速度会变慢

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>将 Linux 文件放在 Linux 根文件系统中
请务必将使用 Linux 应用程序频繁访问的文件放在 Linux 根文件系统中，从而获取文件性能方面的优势。 这些文件只有在 Linux 根文件系统中才能实现更快的文件系统访问。 我们还使 Windows 应用能访问 Linux 根文件系统（如文件资源管理器！ 尝试在 Linux 发行版的 home 目录中运行：`explorer.exe .`，看看会发生什么)， 这会使文件转移更加便捷。 

## <a name="accessing-network-applications"></a>访问网络应用程序
在 WSL 2 预览版的初始版本中，需要使用主机的 IP 地址从 Linux 访问任何 Windows server。

### <a name="accessing-windows-applications-from-linux"></a>从 Linux 访问 Windows 应用程序
若要访问 Windows 网络应用程序，需要使用主机的 IP 地址。 为此，可以执行以下步骤：

- 通过运行命令`cat /etc/resolv.conf`并复制该字词`nameserver`后面的 ip 地址来获取主机的 ip 地址。 
- 使用复制的 IP 地址连接到任何 Windows server。

下图展示了一个示例，该示例通过 curl 连接到在 Windows 中运行的 Node.js 服务器。


![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows-only-in-builds-lower-than-18945"></a>从 Windows 访问 Linux 应用程序（仅在版本低于18945的版本中）
如果在 WSL 发行版中有服务器，需要查找运行 Linux 发行版的虚拟机的 IP 地址并使用该 IP 地址连接它。 可以通过以下步骤来实现此目的：

- 通过在 WSL 发行版中运行命令`ip addr` ，并`inet`在该`eth0`接口的值下面查找，来获取发行版的 IP 地址。
   - 可以通过使用 grep 筛选命令的输出来更轻松地找到此内容，如下所`ip addr | grep eth0`示：。
- 使用上面找到的 IP 连接到 Linux 服务器。

下图显示了一个示例，该示例通过使用 Edge 浏览器连接到 node.js 服务器。

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

如果生成为18945或更高版本，则可以像平时一样使用 localhost。 

### <a name="other-networking-considerations"></a>其他网络注意事项

当使用远程 IP 地址连接到应用程序时，它们将被视为来自局域网（LAN）的连接。 这意味着你将需要确保你的应用程序可以接受 LAN 连接，例如：你可能需要将应用程序绑定到`0.0.0.0` ， `127.0.0.1`而不是。 例如，在 python 中使用 flask，可以使用以下命令完成此`app.run(host='0.0.0.0')`操作：。 进行这些更改时，请牢记安全，因为这将允许来自 LAN 的连接。 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>了解 WSL 2 使用 VHD，如果达到其最大大小，会发生什么情况
WSL 2 将所有 Linux 文件都存储在使用 ext4 文件系统的 VHD 中。 此 VHD 会自动调整大小以满足你的存储需求。 此 VHD 的初始最大大小为256GB。 如果发行版大小增长到大于256GB，则会看到错误，指出磁盘空间不足。 可以通过扩展 VHD 大小来解决这些问题。 下面是有关如何执行此操作的说明：

1. 使用`wsl --shutdown`命令终止所有 WSL 实例
2. 查找你的发行版安装包名称 "PackageFamilyName"
   - 在 powershell 提示符下（其中，"发行版" 是你的分发名称）键入：
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. 找到 WSL 2 安装使用的 VHD 文件 fullpath，这将是 "pathToVHD"：
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 通过完成以下命令调整 WSL 2 VHD 的大小
   - 使用管理员权限打开命令提示符窗口，并运行以下命令：
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. 启动 WSL 发行版
6. 请注意，WSL 可以扩展其文件系统的大小
   - 在 WSL 发行版中运行以下命令：
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 复制此项的名称，如下所示：/dev/sdXX （X 表示任何其他字符）
      - `sudo resize2fs /dev/sdXX`
         - 请确保使用前面复制的值，并且可能需要使用： `apt install resize2fs`。

请注意：通常，不要使用 Windows 工具或编辑器修改、移动或访问位于 AppData 文件夹内的 WSL 相关文件。 这样做可能会导致 Linux 发行版损坏。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 将在启动时使用一些内存
WSL 2 在实际 Linux 内核上使用轻型实用程序 VM，以提供高性能的文件系统性能和系统调用的完全兼容性，同时仍然像 WSL 1 一样快速、快速、集成且响应迅速。 此实用程序 VM 的内存占用较小，将在启动时分配虚拟地址支持的内存。 将其配置为从总体内存的小部分开始。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>在初始预览版中，跨 OS 文件速度会变慢
从 Linux 应用程序访问 Windows 文件或从 Windows 应用程序访问 Linux 文件时，与 WSL 1 相比，你会注意到文件速度更慢。 这是 WSL 2 中体系结构更改的结果，WSL 团队正在积极地调查如何改进此体验。
