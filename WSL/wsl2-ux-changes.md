---
title: WSL 1 与 WSL 2 之间的用户体验更改
description: WSL 1 与 WSL 2 之间的用户体验更改
keywords: BashOnWindows, bash, wsl, wsl2, Windows, 适用于 Linux 的 Windows 子系统, windowssubsystem, ubuntu, debian, suse, Windows 10
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 1965a22a2e290777b207d9ded099ce4a79e1ed38
ms.sourcegitcommit: 0a001ada2131f80dd77b114fc14f2fde43c947ad
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/25/2020
ms.locfileid: "80256330"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a>WSL 1 与 WSL 2 之间的用户体验更改

本页介绍了 WSL 1 与 WSL 2 预览版之间的用户体验差异。 需要注意的关键更改有：

- 请将 Linux 应用将访问的文件放在 Linux 根文件系统中，以提升文件执行速度
- 在 WSL 2 预览版的初始版本中，你将需要使用 IP 地址（而不是使用 localhost）访问网络应用程序

下面是你可能会注意到的其他更改的完整列表：

- WSL 2 使用[虚拟硬件磁盘](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) 来存储文件，如果达到其最大大小，则可能需要对其进行扩展
- 启动时，WSL 2 现在将使用少量内存
- 在初始预览版中，跨 OS 的文件访问速度将变慢

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a>将 Linux 文件放在 Linux 根文件系统中
请确保将你要使用 Linux 应用程序频繁访问的文件放在 Linux 根文件系统中，以享受文件性能优势。 这些文件必须位于 Linux 根文件系统内，以便较快地访问文件系统。 我们还使 Windows 应用能够访问 Linux 根文件系统（例如文件资源管理器！ 请尝试在 Linux 发行版的主目录中运行：`explorer.exe .`，并查看发生的情况），这将大大简化这一过渡。 

## <a name="accessing-network-applications"></a>访问网络应用程序
在 WSL 2 预览版的初始版本中，你需要使用主机的 IP 地址从 Linux 访问任何 Windows 服务器。

### <a name="accessing-windows-applications-from-linux"></a>从 Linux 访问 Windows 应用程序
若要访问 Windows 网络应用程序，需要使用主机的 IP 地址。 可以通过以下步骤来执行该操作：

- 通过运行命令 `cat /etc/resolv.conf` 并复制词语 `nameserver` 后的 IP 地址来获取主机的 IP 地址。 
- 使用复制的 IP 地址连接到任何 Windows 服务器。

下图显示了一个示例，该示例说明如何通过 curl 连接到在 Windows 中运行的 Node.js 服务器。 

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a>从 Windows 访问 Linux 应用程序

根据你使用的 Windows 版本，你可能需要检索虚拟机的 IP 地址。 如果你的版本为 18945 或更高版本，则可以像在常规情况下一样使用 `localhost`。 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a>在低于 [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/) 的版本上访问 Linux

如果服务器在 WSL 发行版上运行，则需要找到为你的发行版提供支持的虚拟机的 IP 地址，并使用该 IP 地址连接到服务器。 可以通过以下步骤来执行该操作：

- 通过在 WSL 发行版中运行命令 `ip addr` 来获取发行版的 IP 地址，可以在 `eth0` 接口的 `inet` 值下找到该地址。
   - 可以使用 grep 来筛选此命令的输出以更轻松地找到该地址，如下所示：`ip addr | grep eth0`。
- 使用上面找到的 IP 连接到 Linux 服务器。

下图显示了一个示例，该示例使用 Edge 浏览器连接到 Node.js 服务器。

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a>其他网络注意事项

#### <a name="connecting-via-remote-ip-addresses"></a>通过远程 IP 地址进行连接

当使用远程 IP 地址连接到应用程序时，它们将被视为来自局域网 (LAN) 的连接。 这意味着你需要确保你的应用程序可以接受 LAN 连接，即：你可能需要将应用程序绑定到 `0.0.0.0` 而非 `127.0.0.1`。 例如，在使用 flask 的 python 中，可以通过以下命令执行此操作：`app.run(host='0.0.0.0')`。 进行这些更改时请注意安全性，因为这将允许来自你的 LAN 的连接。 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a>从局域网 (LAN) 访问 WSL2 发行版

当使用 WSL1 发行版时，如果计算机设置为可供在 LAN 中访问，那么在 WSL 中运行的应用程序也可供在 LAN 中访问。 在 WSL2 中，这不是默认情况，因为 WSL2 有一个具有其自己的 IP 地址的虚拟化以太网适配器。 目前，若要启用此工作流，你需要执行与常规虚拟机相同的步骤。 我们正在寻找改善此体验的方法！

#### <a name="ipv6-access"></a>IPv6 访问

WSL2 发行版目前无法访问纯 IPv6 地址。 我们正在致力于添加此功能。

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a>了解 WSL 2 使用的是 VHD，如果达到其最大大小，该怎么办
WSL 2 将所有 Linux 文件都存储在使用 ext4 文件系统的 VHD 中。 此 VHD 会自动调整大小以满足你的存储需求。 此 VHD 的初始最大大小为 256GB。 如果你的发行版大小增长到大于 256GB，则会出现错误，指出磁盘空间不足。 可以通过扩展 VHD 大小来解决这些问题。 下面是有关如何执行此操作的说明：

1. 使用 `wsl --shutdown` 命令终止所有 WSL 实例
2. 查找你的发行版安装包名称“PackageFamilyName”
   - 在 powershell 提示符下键入以下命令（其中，“distro”是你的发行版名称）：
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. 找到 WSL 2 安装使用的 VHD 文件完整路径，这将是“pathToVHD”：
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. 通过完成以下命令调整 WSL 2 VHD 的大小
   - 使用管理员权限打开命令提示符窗口，并运行以下命令：
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. 启动 WSL 发行版
6. 让 WSL 知道它可以扩展其文件系统的大小
   - 在 WSL 发行版中运行以下命令：
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - 复制此项的名称，如下所示：/dev/sdXX（X 表示任何其他字符）
      - `sudo resize2fs /dev/sdXX`
         - 请确保使用前面复制的值，并且可能需要使用：`apt install resize2fs`。

请注意：通常情况下，不要使用 Windows 工具或编辑器来修改、移动或访问 AppData 文件夹中与 WSL 相关的文件。 这样做可能会导致 Linux 发行版损坏。

## <a name="wsl-2-will-use-some-memory-on-startup"></a>WSL 2 在启动时将使用一些内存
WSL 2 在真实的 Linux 内核上使用一个轻量级实用工具 VM 来提供良好的文件系统性能和完全的系统调用兼容性，同时仍然像 WSL 1一样轻巧、快速、全面集成且反应敏捷。 此实用工具 VM 的内存占用较小，在启动时将分配虚拟地址支持的内存。 它配置为从总内存的一小部分开始。

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a>在初始预览版中，跨 OS 的文件速度将变慢
你会注意到，当从 Linux 应用程序访问 Windows 文件时，或者从 Windows 应用程序访问 Linux 文件时，与 WSL 1 相比，文件速度变慢。 这是 WSL 2 体系结构变化所导致的结果，WSL 团队正在积极研究如何改进此体验。
