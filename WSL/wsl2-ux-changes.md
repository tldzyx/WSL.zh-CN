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
ms.sourcegitcommit: 39d3a2f0f4184eaec8d8fec740aff800e8ea9ac7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/24/2020
ms.locfileid: "80256330"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="c7e7d-104">WSL 1 与 WSL 2 之间的用户体验更改</span><span class="sxs-lookup"><span data-stu-id="c7e7d-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="c7e7d-105">本页介绍了 WSL 1 与 WSL 2 预览版之间的用户体验差异。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="c7e7d-106">需要注意的关键更改有：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="c7e7d-107">请将 Linux 应用将访问的文件放在 Linux 根文件系统中，以提升文件执行速度</span><span class="sxs-lookup"><span data-stu-id="c7e7d-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="c7e7d-108">在 WSL 2 预览版的初始版本中，你将需要使用 IP 地址（而不是使用 localhost）访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="c7e7d-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="c7e7d-109">下面是你可能会注意到的其他更改的完整列表：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="c7e7d-110">WSL 2 使用[虚拟硬件磁盘](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) 来存储文件，如果达到其最大大小，则可能需要对其进行扩展</span><span class="sxs-lookup"><span data-stu-id="c7e7d-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="c7e7d-111">启动时，WSL 2 现在将使用少量内存</span><span class="sxs-lookup"><span data-stu-id="c7e7d-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="c7e7d-112">在初始预览版中，跨 OS 的文件访问速度将变慢</span><span class="sxs-lookup"><span data-stu-id="c7e7d-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="c7e7d-113">将 Linux 文件放在 Linux 根文件系统中</span><span class="sxs-lookup"><span data-stu-id="c7e7d-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="c7e7d-114">请确保将你要使用 Linux 应用程序频繁访问的文件放在 Linux 根文件系统中，以享受文件性能优势。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="c7e7d-115">这些文件必须位于 Linux 根文件系统内，以便较快地访问文件系统。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="c7e7d-116">我们还使 Windows 应用能够访问 Linux 根文件系统（例如文件资源管理器！</span><span class="sxs-lookup"><span data-stu-id="c7e7d-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="c7e7d-117">请尝试在 Linux 发行版的主目录中运行：`explorer.exe .`，并查看发生的情况），这将大大简化这一过渡。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="c7e7d-118">访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="c7e7d-118">Accessing network applications</span></span>
<span data-ttu-id="c7e7d-119">在 WSL 2 预览版的初始版本中，你需要使用主机的 IP 地址从 Linux 访问任何 Windows 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-119">In the initial builds of the WSL 2 preview, you will need to access any Windows server from Linux using the IP address of your host machine.</span></span>

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="c7e7d-120">从 Linux 访问 Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="c7e7d-120">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="c7e7d-121">若要访问 Windows 网络应用程序，需要使用主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-121">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="c7e7d-122">可以通过以下步骤来执行该操作：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-122">You can do so with these steps:</span></span>

- <span data-ttu-id="c7e7d-123">通过运行命令 `cat /etc/resolv.conf` 并复制词语 `nameserver` 后的 IP 地址来获取主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-123">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="c7e7d-124">使用复制的 IP 地址连接到任何 Windows 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-124">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="c7e7d-125">下图显示了一个示例，该示例说明如何通过 curl 连接到在 Windows 中运行的 Node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-125">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="c7e7d-127">从 Windows 访问 Linux 应用程序</span><span class="sxs-lookup"><span data-stu-id="c7e7d-127">Accessing Linux applications from Windows</span></span>

<span data-ttu-id="c7e7d-128">根据你使用的 Windows 版本，你可能需要检索虚拟机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-128">Depending on which version of Windows you're using, you might need to retrieve the IP address of the virtual machine.</span></span> <span data-ttu-id="c7e7d-129">如果你的版本为 18945 或更高版本，则可以像在常规情况下一样使用 `localhost`。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-129">If your build is 18945 or higher, you can use `localhost` just like normal.</span></span> 

#### <a name="accessing-linux-on-builds-lower-than-18945"></a><span data-ttu-id="c7e7d-130">在低于 [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/) 的版本上访问 Linux</span><span class="sxs-lookup"><span data-stu-id="c7e7d-130">Accessing Linux on Builds lower than [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)</span></span>

<span data-ttu-id="c7e7d-131">如果服务器在 WSL 发行版上运行，则需要找到为你的发行版提供支持的虚拟机的 IP 地址，并使用该 IP 地址连接到服务器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-131">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="c7e7d-132">可以通过以下步骤来执行该操作：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-132">You can do that by following these steps:</span></span>

- <span data-ttu-id="c7e7d-133">通过在 WSL 发行版中运行命令 `ip addr` 来获取发行版的 IP 地址，可以在 `eth0` 接口的 `inet` 值下找到该地址。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-133">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="c7e7d-134">可以使用 grep 来筛选此命令的输出以更轻松地找到该地址，如下所示：`ip addr | grep eth0`。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-134">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="c7e7d-135">使用上面找到的 IP 连接到 Linux 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-135">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="c7e7d-136">下图显示了一个示例，该示例使用 Edge 浏览器连接到 Node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-136">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a><span data-ttu-id="c7e7d-138">其他网络注意事项</span><span class="sxs-lookup"><span data-stu-id="c7e7d-138">Other networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="c7e7d-139">通过远程 IP 地址进行连接</span><span class="sxs-lookup"><span data-stu-id="c7e7d-139">Connecting via remote IP addresses</span></span>

<span data-ttu-id="c7e7d-140">当使用远程 IP 地址连接到应用程序时，它们将被视为来自局域网 (LAN) 的连接。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-140">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="c7e7d-141">这意味着你需要确保你的应用程序可以接受 LAN 连接，即：你可能需要将应用程序绑定到 `0.0.0.0` 而非 `127.0.0.1`。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-141">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="c7e7d-142">例如，在使用 flask 的 python 中，可以通过以下命令执行此操作：`app.run(host='0.0.0.0')`。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-142">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="c7e7d-143">进行这些更改时请注意安全性，因为这将允许来自你的 LAN 的连接。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-143">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a><span data-ttu-id="c7e7d-144">从局域网 (LAN) 访问 WSL2 发行版</span><span class="sxs-lookup"><span data-stu-id="c7e7d-144">Accessing a WSL2 distro from your local area network (LAN)</span></span>

<span data-ttu-id="c7e7d-145">当使用 WSL1 发行版时，如果计算机设置为可供在 LAN 中访问，那么在 WSL 中运行的应用程序也可供在 LAN 中访问。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-145">When using a WSL1 distro, if your computer was set up to be accessed by in your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span> <span data-ttu-id="c7e7d-146">在 WSL2 中，这不是默认情况，因为 WSL2 有一个具有其自己的 IP 地址的虚拟化以太网适配器。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-146">This isn't the default case in WSL2, as WSL2 has a virtualized ethernet adapter with its own IP address.</span></span> <span data-ttu-id="c7e7d-147">目前，若要启用此工作流，你需要执行与常规虚拟机相同的步骤。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-147">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="c7e7d-148">我们正在寻找改善此体验的方法！</span><span class="sxs-lookup"><span data-stu-id="c7e7d-148">We are looking into ways to improve this experience!</span></span>

#### <a name="ipv6-access"></a><span data-ttu-id="c7e7d-149">IPv6 访问</span><span class="sxs-lookup"><span data-stu-id="c7e7d-149">IPv6 access</span></span>

<span data-ttu-id="c7e7d-150">WSL2 发行版目前无法访问纯 IPv6 地址。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-150">WSL2 distros currently cannot reach IPv6 only addresses.</span></span> <span data-ttu-id="c7e7d-151">我们正在致力于添加此功能。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-151">We are working on adding this feature.</span></span>

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="c7e7d-152">了解 WSL 2 使用的是 VHD，如果达到其最大大小，该怎么办</span><span class="sxs-lookup"><span data-stu-id="c7e7d-152">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="c7e7d-153">WSL 2 将所有 Linux 文件都存储在使用 ext4 文件系统的 VHD 中。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-153">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="c7e7d-154">此 VHD 会自动调整大小以满足你的存储需求。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-154">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="c7e7d-155">此 VHD 的初始最大大小为 256GB。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-155">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="c7e7d-156">如果你的发行版大小增长到大于 256GB，则会出现错误，指出磁盘空间不足。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-156">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="c7e7d-157">可以通过扩展 VHD 大小来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-157">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="c7e7d-158">下面是有关如何执行此操作的说明：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-158">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="c7e7d-159">使用 `wsl --shutdown` 命令终止所有 WSL 实例</span><span class="sxs-lookup"><span data-stu-id="c7e7d-159">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="c7e7d-160">查找你的发行版安装包名称“PackageFamilyName”</span><span class="sxs-lookup"><span data-stu-id="c7e7d-160">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="c7e7d-161">在 powershell 提示符下键入以下命令（其中，“distro”是你的发行版名称）：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-161">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="c7e7d-162">找到 WSL 2 安装使用的 VHD 文件完整路径，这将是“pathToVHD”：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-162">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="c7e7d-163">通过完成以下命令调整 WSL 2 VHD 的大小</span><span class="sxs-lookup"><span data-stu-id="c7e7d-163">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="c7e7d-164">使用管理员权限打开命令提示符窗口，并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-164">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="c7e7d-165">启动 WSL 发行版</span><span class="sxs-lookup"><span data-stu-id="c7e7d-165">Launch your WSL distro</span></span>
6. <span data-ttu-id="c7e7d-166">让 WSL 知道它可以扩展其文件系统的大小</span><span class="sxs-lookup"><span data-stu-id="c7e7d-166">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="c7e7d-167">在 WSL 发行版中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="c7e7d-167">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="c7e7d-168">复制此项的名称，如下所示：/dev/sdXX（X 表示任何其他字符）</span><span class="sxs-lookup"><span data-stu-id="c7e7d-168">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="c7e7d-169">请确保使用前面复制的值，并且可能需要使用：`apt install resize2fs`。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-169">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="c7e7d-170">请注意：通常情况下，不要使用 Windows 工具或编辑器来修改、移动或访问 AppData 文件夹中与 WSL 相关的文件。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-170">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="c7e7d-171">这样做可能会导致 Linux 发行版损坏。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-171">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="c7e7d-172">WSL 2 在启动时将使用一些内存</span><span class="sxs-lookup"><span data-stu-id="c7e7d-172">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="c7e7d-173">WSL 2 在真实的 Linux 内核上使用一个轻量级实用工具 VM 来提供良好的文件系统性能和完全的系统调用兼容性，同时仍然像 WSL 1一样轻巧、快速、全面集成且反应敏捷。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-173">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="c7e7d-174">此实用工具 VM 的内存占用较小，在启动时将分配虚拟地址支持的内存。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-174">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="c7e7d-175">它配置为从总内存的一小部分开始。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-175">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="c7e7d-176">在初始预览版中，跨 OS 的文件速度将变慢</span><span class="sxs-lookup"><span data-stu-id="c7e7d-176">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="c7e7d-177">你会注意到，当从 Linux 应用程序访问 Windows 文件时，或者从 Windows 应用程序访问 Linux 文件时，与 WSL 1 相比，文件速度变慢。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-177">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="c7e7d-178">这是 WSL 2 体系结构变化所导致的结果，WSL 团队正在积极研究如何改进此体验。</span><span class="sxs-lookup"><span data-stu-id="c7e7d-178">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
