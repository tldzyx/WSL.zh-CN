---
title: WSL 1 与 WSL 2 的用户体验差异
description: WSL 1 与 WSL 2 的用户体验差异
keywords: BashOnWindows，bash、 wsl、 wsl2、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10 的 windows 子系统
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 0660f9f726811008685de9f1ff457e7515add67a
ms.sourcegitcommit: bb88269eb37405192625fa81ff91162393fb491f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/12/2019
ms.locfileid: "67038097"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 与 WSL 2 的用户体验差异

此页主要描述 WSL 1 和 WSL 2 预览版之间的用户体验差异。 关键差异包括：

- 将 Linux 应用需要访问的文件放在 Linux 根文件系统中可以提高文件访问速度
- 在 WSL 2 预览版的初始版本中，你需要使用 IP 地址而不是 localhost 来访问网络应用程序

下面是可能会注意到的差异的完整列表：

- WSL 2 使用 VHD 来存储你的文件，如果达到其最大大小可能需要将其展开
- 在启动时，WSL 2 现在将使用内存的一小部分
- 初始预览版本中，跨 OS 文件访问速度会变慢

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>将 Linux 文件放在 Linux 根文件系统中
请务必将使用 Linux 应用程序频繁访问的文件放在 Linux 根文件系统中，从而获取文件性能方面的优势。这些文件只有在 Linux 根文件系统中才能实现更快的文件系统访问。 我们还使 Windows 应用能访问 Linux 根文件系统（如文件资源管理器！尝试在 Linux 发行版的 home 目录中运行：`explorer.exe .`，看看会发生什么)， 这会使文件转移更加便捷。

## <a name="accessing-network-applications"></a>访问网络的应用程序
在 WSL 2 预览版的初始版本中，需要使用 Linux 发行版的 IP 地址从 Windows 中访问 Linux 服务器并使用主机的 IP 地址从 Linux 中访问 Windows 服务器。 这不是临时性的问题，而是需要解决的首要问题之一。

### <a name="accessing-linux-applications-from-windows"></a>从 Windows 访问 Linux 应用程序
如果在 WSL 发行版中有服务器，需要查找运行 Linux 发行版的虚拟机的 IP 地址并使用该 IP 地址连接它。 可以通过以下步骤来实现此目的：

- 通过运行命令获得的发行版的 IP 地址`ip addr`WSL 发行版和查找下将其内部`inet`的值`eth0`接口。
   - 通过筛选使用 grep 命令的输出，可以更轻松地找到此如下所示： `ip addr | grep eth0`。
- 连接到 Linux 服务器使用的 IP 上面找到。

下面的图片显示出现这种通过连接到使用 Edge 浏览器的 nodeJS 服务器。

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a>从 Linux 访问 Windows 应用程序
若要访问 Windows 网络应用程序将需要使用您的主机的 IP 地址。 可以通过以下步骤进行操作：

- 通过运行命令来获取您的主机的 IP 地址`cat /etc/resolv.conf`并复制以下术语的 IP 地址`nameserver`。 
- 连接到使用复制的 IP 地址的任何 Windows 服务器。

下面的图片显示出现这种通过连接到通过 curl 在 Windows 中运行的 python 服务器。 

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>了解 WSL 2 使用 VHD，以及要执行的操作如果达到其最大大小
WSL 2 将存储的 VHD，使用 ext4 文件系统内的所有 Linux 文件。 此 VHD 自动调整大小以满足你的存储需求。 此 VHD 还具有初始最大大小为 256 GB。 如果你的发行增长的大小大于 256 GB，将看到错误消息指出已耗尽磁盘空间。 您可以解决这些通过扩展的 VHD 大小。 有关如何执行此操作的说明如下所示：

1. 终止所有 WSL 实例使用`wsl --shutdown`命令
2. 通过完成以下命令调整 WSL 2 VHD 的大小
   - 使用管理员权限打开命令提示符窗口并运行以下命令：
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. 启动 WSL 发行版
4. 请注意，它可以扩展其文件系统大小 WSL
   - 在 WSL 发行版中运行以下命令：
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 复制看起来类似于此项的名称: / sdXX (带有 X 表示任何其他字符)
      - `sudo resize2fs /dev/sdXX`
         - 请确保要使用的值之前复制，并且可能需要使用： `apt install resize2fs`。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 将在启动时使用一些内存
WSL 2 在真实的 Linux 内核上使用轻量级实用工具 VM 提供很好的文件系统性能和完整的系统调用兼容性时仍是只需为轻，快速、 集成和 WSL 1 的响应速度。 此实用程序 VM 具有小的内存需求量，并将备份的虚拟地址上分配内存启动。 它配置为启动与总内存的一小部分。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>跨 OS 文件速度会变慢初始预览版本中
您将注意到文件的速度比 WSL 1 从 Linux 应用程序，或从 Windows 应用程序访问 Linux 文件访问 Windows 文件时。 这是在 WSL 2 中，体系结构的更改的结果，是指 WSL 团队正在调查上我们可以如何改进此体验。
