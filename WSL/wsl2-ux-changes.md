---
title: WSL 1 与 WSL 2 的用户体验差异
description: WSL 1 与 WSL 2 的用户体验差异
keywords: BashOnWindows、bash、wsl、wsl2、windows、适用于 linux、windowssubsystem、ubuntu、debian、suse、windows 10 的 windows 子系统
author: craigloewen-msft
ms.author: crloewen
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 347c965dbbc2a328590d3a8149a8316979d6793d
ms.sourcegitcommit: ebc6ae7e7546a6d33644e68788fa0215028859b2
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/17/2019
ms.locfileid: "71070320"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="3c495-104">WSL 1 与 WSL 2 的用户体验差异</span><span class="sxs-lookup"><span data-stu-id="3c495-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="3c495-105">此页主要描述 WSL 1 和 WSL 2 预览版之间的用户体验差异。</span><span class="sxs-lookup"><span data-stu-id="3c495-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="3c495-106">关键差异包括：</span><span class="sxs-lookup"><span data-stu-id="3c495-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="3c495-107">将 Linux 应用需要访问的文件放在 Linux 根文件系统中可以提高文件访问速度</span><span class="sxs-lookup"><span data-stu-id="3c495-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="3c495-108">在 WSL 2 预览版的初始版本中，你需要使用 IP 地址而不是 localhost 来访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="3c495-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="3c495-109">下面是可能会注意到的差异的完整列表：</span><span class="sxs-lookup"><span data-stu-id="3c495-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="3c495-110">WSL 2 使用[虚拟硬件磁盘](https://en.wikipedia.org/wiki/VHD_(file_format))（VHD）来存储文件，如果达到其最大大小，则可能需要将其扩展</span><span class="sxs-lookup"><span data-stu-id="3c495-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="3c495-111">启动时，WSL 2 现在将使用少量内存</span><span class="sxs-lookup"><span data-stu-id="3c495-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="3c495-112">初始预览版本中，跨 OS 文件访问速度会变慢</span><span class="sxs-lookup"><span data-stu-id="3c495-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="3c495-113">将 Linux 文件放在 Linux 根文件系统中</span><span class="sxs-lookup"><span data-stu-id="3c495-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="3c495-114">请务必将使用 Linux 应用程序频繁访问的文件放在 Linux 根文件系统中，从而获取文件性能方面的优势。</span><span class="sxs-lookup"><span data-stu-id="3c495-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="3c495-115">这些文件只有在 Linux 根文件系统中才能实现更快的文件系统访问。</span><span class="sxs-lookup"><span data-stu-id="3c495-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="3c495-116">我们还使 Windows 应用能访问 Linux 根文件系统（如文件资源管理器！</span><span class="sxs-lookup"><span data-stu-id="3c495-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="3c495-117">尝试在 Linux 发行版的 home 目录中运行：`explorer.exe .`，看看会发生什么)， 这会使文件转移更加便捷。</span><span class="sxs-lookup"><span data-stu-id="3c495-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="3c495-118">访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="3c495-118">Accessing network applications</span></span>
<span data-ttu-id="3c495-119">在 WSL 2 预览版的初始版本中，需要使用主机的 IP 地址从 Linux 访问任何 Windows server。</span><span class="sxs-lookup"><span data-stu-id="3c495-119">In the initial builds of the WSL 2 preview, you will need to access any Windows server from Linux using the IP address of your host machine.</span></span>

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="3c495-120">从 Linux 访问 Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="3c495-120">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="3c495-121">若要访问 Windows 网络应用程序，需要使用主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="3c495-121">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="3c495-122">为此，可以执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="3c495-122">You can do so with these steps:</span></span>

- <span data-ttu-id="3c495-123">通过运行命令`cat /etc/resolv.conf`并复制该字词`nameserver`后面的 ip 地址来获取主机的 ip 地址。</span><span class="sxs-lookup"><span data-stu-id="3c495-123">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="3c495-124">使用复制的 IP 地址连接到任何 Windows server。</span><span class="sxs-lookup"><span data-stu-id="3c495-124">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="3c495-125">下图显示了一个示例，该示例通过连接到通过曲线在 Windows 中运行的 node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="3c495-125">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows-only-in-builds-lower-than-18945"></a><span data-ttu-id="3c495-127">从 Windows 访问 Linux 应用程序（仅在版本低于18945的版本中）</span><span class="sxs-lookup"><span data-stu-id="3c495-127">Accessing Linux applications from Windows (only in builds lower than 18945)</span></span>
<span data-ttu-id="3c495-128">如果在 WSL 发行版中有服务器，需要查找运行 Linux 发行版的虚拟机的 IP 地址并使用该 IP 地址连接它。</span><span class="sxs-lookup"><span data-stu-id="3c495-128">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="3c495-129">可以通过以下步骤来实现此目的：</span><span class="sxs-lookup"><span data-stu-id="3c495-129">You can do that by following these steps:</span></span>

- <span data-ttu-id="3c495-130">通过在 WSL 发行版中运行命令`ip addr` ，并`inet`在该`eth0`接口的值下面查找，来获取发行版的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="3c495-130">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="3c495-131">可以通过使用 grep 筛选命令的输出来更轻松地找到此内容，如下所`ip addr | grep eth0`示：。</span><span class="sxs-lookup"><span data-stu-id="3c495-131">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="3c495-132">使用上面找到的 IP 连接到 Linux 服务器。</span><span class="sxs-lookup"><span data-stu-id="3c495-132">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="3c495-133">下图显示了一个示例，该示例通过使用 Edge 浏览器连接到 node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="3c495-133">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

<span data-ttu-id="3c495-135">如果生成为18945或更高版本，则可以像平时一样使用 localhost。</span><span class="sxs-lookup"><span data-stu-id="3c495-135">If your build is 18945 or higher, you can use localhost just like normal.</span></span> 

### <a name="other-networking-considerations"></a><span data-ttu-id="3c495-136">其他网络注意事项</span><span class="sxs-lookup"><span data-stu-id="3c495-136">Other networking considerations</span></span>

<span data-ttu-id="3c495-137">当使用远程 IP 地址连接到应用程序时，它们将被视为来自局域网（LAN）的连接。</span><span class="sxs-lookup"><span data-stu-id="3c495-137">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="3c495-138">这意味着你将需要确保你的应用程序可以接受 LAN 连接，例如：你可能需要将应用程序绑定到`0.0.0.0` ， `127.0.0.1`而不是。</span><span class="sxs-lookup"><span data-stu-id="3c495-138">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="3c495-139">例如，在 python 中使用 flask，可以使用以下命令完成此`app.run(host='0.0.0.0')`操作：。</span><span class="sxs-lookup"><span data-stu-id="3c495-139">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="3c495-140">进行这些更改时，请牢记安全，因为这将允许来自 LAN 的连接。</span><span class="sxs-lookup"><span data-stu-id="3c495-140">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="3c495-141">了解 WSL 2 使用 VHD，如果达到其最大大小，会发生什么情况</span><span class="sxs-lookup"><span data-stu-id="3c495-141">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="3c495-142">WSL 2 将所有 Linux 文件都存储在使用 ext4 文件系统的 VHD 中。</span><span class="sxs-lookup"><span data-stu-id="3c495-142">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="3c495-143">此 VHD 会自动调整大小以满足你的存储需求。</span><span class="sxs-lookup"><span data-stu-id="3c495-143">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="3c495-144">此 VHD 的初始最大大小为256GB。</span><span class="sxs-lookup"><span data-stu-id="3c495-144">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="3c495-145">如果发行版大小增长到大于256GB，则会看到错误，指出磁盘空间不足。</span><span class="sxs-lookup"><span data-stu-id="3c495-145">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="3c495-146">可以通过扩展 VHD 大小来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="3c495-146">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="3c495-147">下面是有关如何执行此操作的说明：</span><span class="sxs-lookup"><span data-stu-id="3c495-147">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="3c495-148">使用`wsl --shutdown`命令终止所有 WSL 实例</span><span class="sxs-lookup"><span data-stu-id="3c495-148">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="3c495-149">查找你的发行版安装包名称 "PackageFamilyName"</span><span class="sxs-lookup"><span data-stu-id="3c495-149">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="3c495-150">在 powershell 提示符下（其中，"发行版" 是你的分发名称）键入：</span><span class="sxs-lookup"><span data-stu-id="3c495-150">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="3c495-151">找到 WSL 2 安装使用的 VHD 文件 fullpath，这将是 "pathToVHD"：</span><span class="sxs-lookup"><span data-stu-id="3c495-151">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="3c495-152">通过完成以下命令调整 WSL 2 VHD 的大小</span><span class="sxs-lookup"><span data-stu-id="3c495-152">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="3c495-153">使用管理员权限打开命令提示符窗口，并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="3c495-153">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="3c495-154">启动 WSL 发行版</span><span class="sxs-lookup"><span data-stu-id="3c495-154">Launch your WSL distro</span></span>
6. <span data-ttu-id="3c495-155">请注意，WSL 可以扩展其文件系统的大小</span><span class="sxs-lookup"><span data-stu-id="3c495-155">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="3c495-156">在 WSL 发行版中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="3c495-156">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="3c495-157">复制此项的名称，如下所示：/dev/sdXX （X 表示任何其他字符）</span><span class="sxs-lookup"><span data-stu-id="3c495-157">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="3c495-158">请确保使用前面复制的值，并且可能需要使用： `apt install resize2fs`。</span><span class="sxs-lookup"><span data-stu-id="3c495-158">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="3c495-159">请注意：通常，不要使用 Windows 工具或编辑器修改、移动或访问位于 AppData 文件夹内的 WSL 相关文件。</span><span class="sxs-lookup"><span data-stu-id="3c495-159">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="3c495-160">这样做可能会导致 Linux 发行版损坏。</span><span class="sxs-lookup"><span data-stu-id="3c495-160">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="3c495-161">WSL 2 将在启动时使用一些内存</span><span class="sxs-lookup"><span data-stu-id="3c495-161">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="3c495-162">WSL 2 在实际 Linux 内核上使用轻型实用程序 VM，以提供高性能的文件系统性能和系统调用的完全兼容性，同时仍然像 WSL 1 一样快速、快速、集成且响应迅速。</span><span class="sxs-lookup"><span data-stu-id="3c495-162">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="3c495-163">此实用程序 VM 的内存占用较小，将在启动时分配虚拟地址支持的内存。</span><span class="sxs-lookup"><span data-stu-id="3c495-163">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="3c495-164">将其配置为从总体内存的小部分开始。</span><span class="sxs-lookup"><span data-stu-id="3c495-164">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="3c495-165">在初始预览版中，跨 OS 文件速度会变慢</span><span class="sxs-lookup"><span data-stu-id="3c495-165">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="3c495-166">从 Linux 应用程序访问 Windows 文件或从 Windows 应用程序访问 Linux 文件时，与 WSL 1 相比，你会注意到文件速度更慢。</span><span class="sxs-lookup"><span data-stu-id="3c495-166">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="3c495-167">这是 WSL 2 中体系结构更改的结果，WSL 团队正在积极地调查如何改进此体验。</span><span class="sxs-lookup"><span data-stu-id="3c495-167">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
