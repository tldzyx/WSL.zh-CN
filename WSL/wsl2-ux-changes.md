---
title: WSL 1 与 WSL 2 的用户体验差异
description: WSL 1 与 WSL 2 的用户体验差异
keywords: BashOnWindows、bash、wsl、wsl2、windows、适用于 linux、windowssubsystem、ubuntu、debian、suse、windows 10 的 windows 子系统
ms.date: 05/30/2019
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: a8f298a69acf44f152da626a0ba571f6bba1970c
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520556"
---
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="7da68-104">WSL 1 与 WSL 2 的用户体验差异</span><span class="sxs-lookup"><span data-stu-id="7da68-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="7da68-105">此页主要描述 WSL 1 和 WSL 2 预览版之间的用户体验差异。</span><span class="sxs-lookup"><span data-stu-id="7da68-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="7da68-106">关键差异包括：</span><span class="sxs-lookup"><span data-stu-id="7da68-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="7da68-107">将 Linux 应用需要访问的文件放在 Linux 根文件系统中可以提高文件访问速度</span><span class="sxs-lookup"><span data-stu-id="7da68-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="7da68-108">在 WSL 2 预览版的初始版本中，你需要使用 IP 地址而不是 localhost 来访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="7da68-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="7da68-109">下面是可能会注意到的差异的完整列表：</span><span class="sxs-lookup"><span data-stu-id="7da68-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="7da68-110">WSL 2 使用[虚拟硬件磁盘](https://en.wikipedia.org/wiki/VHD_(file_format))（VHD）来存储文件，如果达到其最大大小，则可能需要将其扩展</span><span class="sxs-lookup"><span data-stu-id="7da68-110">WSL 2 uses a [Virtual Hardware Disk](https://en.wikipedia.org/wiki/VHD_(file_format)) (VHD) to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="7da68-111">启动时，WSL 2 现在将使用少量内存</span><span class="sxs-lookup"><span data-stu-id="7da68-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="7da68-112">初始预览版本中，跨 OS 文件访问速度会变慢</span><span class="sxs-lookup"><span data-stu-id="7da68-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="7da68-113">将 Linux 文件放在 Linux 根文件系统中</span><span class="sxs-lookup"><span data-stu-id="7da68-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="7da68-114">请务必将使用 Linux 应用程序频繁访问的文件放在 Linux 根文件系统中，从而获取文件性能方面的优势。</span><span class="sxs-lookup"><span data-stu-id="7da68-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="7da68-115">这些文件只有在 Linux 根文件系统中才能实现更快的文件系统访问。</span><span class="sxs-lookup"><span data-stu-id="7da68-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="7da68-116">我们还使 Windows 应用能访问 Linux 根文件系统（如文件资源管理器！</span><span class="sxs-lookup"><span data-stu-id="7da68-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="7da68-117">尝试在 Linux 发行版的 home 目录中运行：`explorer.exe .`，看看会发生什么)， 这会使文件转移更加便捷。</span><span class="sxs-lookup"><span data-stu-id="7da68-117">Try running: `explorer.exe .` in the home directory of your Linux distro and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="7da68-118">访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="7da68-118">Accessing network applications</span></span>
<span data-ttu-id="7da68-119">在 WSL 2 预览版的初始版本中，需要使用主机的 IP 地址从 Linux 访问任何 Windows server。</span><span class="sxs-lookup"><span data-stu-id="7da68-119">In the initial builds of the WSL 2 preview, you will need to access any Windows server from Linux using the IP address of your host machine.</span></span>

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="7da68-120">从 Linux 访问 Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="7da68-120">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="7da68-121">若要访问 Windows 网络应用程序，需要使用主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7da68-121">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="7da68-122">为此，可以执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="7da68-122">You can do so with these steps:</span></span>

- <span data-ttu-id="7da68-123">通过运行命令 `cat /etc/resolv.conf` 并在 `nameserver`术语后面复制 IP 地址，来获取主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7da68-123">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="7da68-124">使用复制的 IP 地址连接到任何 Windows server。</span><span class="sxs-lookup"><span data-stu-id="7da68-124">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="7da68-125">下图显示了一个示例，该示例通过连接到通过曲线在 Windows 中运行的 node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="7da68-125">The picture below shows an example of this by connecting to a Node.js server running in Windows via curl.</span></span> 

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="7da68-127">从 Windows 访问 Linux 应用程序</span><span class="sxs-lookup"><span data-stu-id="7da68-127">Accessing Linux applications from Windows</span></span>

<span data-ttu-id="7da68-128">根据你使用的 Windows 版本，你可能需要检索虚拟机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="7da68-128">Depending on which version of Windows you're using, you might need to retrieve the IP address of the virtual machine.</span></span> <span data-ttu-id="7da68-129">如果生成为18945或更高版本，则可以使用 `localhost`，就像正常一样。</span><span class="sxs-lookup"><span data-stu-id="7da68-129">If your build is 18945 or higher, you can use `localhost` just like normal.</span></span> 

#### <a name="accessing-linux-on-builds-lower-than-18945httpsblogswindowscomwindowsexperience20190726announcing-windows-10-insider-preview-build-18945"></a><span data-ttu-id="7da68-130">在低于[18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)的版本上访问 Linux</span><span class="sxs-lookup"><span data-stu-id="7da68-130">Accessing Linux on Builds lower than [18945](https://blogs.windows.com/windowsexperience/2019/07/26/announcing-windows-10-insider-preview-build-18945/)</span></span>

<span data-ttu-id="7da68-131">如果在 WSL 发行版中有服务器，需要查找运行 Linux 发行版的虚拟机的 IP 地址并使用该 IP 地址连接它。</span><span class="sxs-lookup"><span data-stu-id="7da68-131">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="7da68-132">可以通过以下步骤来实现此目的：</span><span class="sxs-lookup"><span data-stu-id="7da68-132">You can do that by following these steps:</span></span>

- <span data-ttu-id="7da68-133">通过在 WSL 发行版中运行命令 `ip addr` 来获取发行版的 IP 地址，并在 `eth0` 接口的 `inet` 值下找到它。</span><span class="sxs-lookup"><span data-stu-id="7da68-133">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="7da68-134">可以通过使用 grep （如下所示）筛选命令的输出来更轻松地找到此方法： `ip addr | grep eth0`。</span><span class="sxs-lookup"><span data-stu-id="7da68-134">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="7da68-135">使用上面找到的 IP 连接到 Linux 服务器。</span><span class="sxs-lookup"><span data-stu-id="7da68-135">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="7da68-136">下图显示了一个示例，该示例通过使用 Edge 浏览器连接到 node.js 服务器。</span><span class="sxs-lookup"><span data-stu-id="7da68-136">The picture below shows an example of this by connecting to a Node.js server using the Edge browser.</span></span>

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

### <a name="other-networking-considerations"></a><span data-ttu-id="7da68-138">其他网络注意事项</span><span class="sxs-lookup"><span data-stu-id="7da68-138">Other networking considerations</span></span>

#### <a name="connecting-via-remote-ip-addresses"></a><span data-ttu-id="7da68-139">通过远程 IP 地址连接</span><span class="sxs-lookup"><span data-stu-id="7da68-139">Connecting via remote IP addresses</span></span>

<span data-ttu-id="7da68-140">当使用远程 IP 地址连接到应用程序时，它们将被视为来自局域网（LAN）的连接。</span><span class="sxs-lookup"><span data-stu-id="7da68-140">When using remote IP addresses to connect to your applications, they will be treated as connections from the Local Area Network (LAN).</span></span> <span data-ttu-id="7da68-141">这意味着你将需要确保你的应用程序可以接受 LAN 连接，例如：你可能需要将应用程序绑定到 `0.0.0.0` 而不是 `127.0.0.1`。</span><span class="sxs-lookup"><span data-stu-id="7da68-141">This means that you will need to make sure your application can accept LAN connections, i.e: You might need to bind your application to `0.0.0.0` instead of `127.0.0.1`.</span></span> <span data-ttu-id="7da68-142">例如，在 python 中使用 flask，可以使用以下命令完成此操作： `app.run(host='0.0.0.0')`。</span><span class="sxs-lookup"><span data-stu-id="7da68-142">For example in python using flask this can be done with the command: `app.run(host='0.0.0.0')`.</span></span> <span data-ttu-id="7da68-143">进行这些更改时，请牢记安全，因为这将允许来自 LAN 的连接。</span><span class="sxs-lookup"><span data-stu-id="7da68-143">Please keep security in mind when making these changes, as this will allow connections from your LAN.</span></span> 

#### <a name="accessing-a-wsl2-distro-from-your-local-area-network-lan"></a><span data-ttu-id="7da68-144">通过局域网（LAN）访问 WSL2 发行版</span><span class="sxs-lookup"><span data-stu-id="7da68-144">Accessing a WSL2 distro from your local area network (LAN)</span></span>

<span data-ttu-id="7da68-145">当使用 WSL1 发行版时，如果你的计算机已设置为在你的 LAN 中进行访问，则也可以在你的 LAN 上访问 WSL 中运行的应用程序。</span><span class="sxs-lookup"><span data-stu-id="7da68-145">When using a WSL1 distro, if your computer was set up to be accessed by in your LAN, then applications run in WSL could be accessed on your LAN as well.</span></span> <span data-ttu-id="7da68-146">这并不是 WSL2 中的默认情况，因为 WSL2 有一个具有其自己的 IP 地址的虚拟化以太网适配器。</span><span class="sxs-lookup"><span data-stu-id="7da68-146">This isn't the default case in WSL2, as WSL2 has a virtualized ethernet adapter with its own IP address.</span></span> <span data-ttu-id="7da68-147">目前，若要启用此工作流，需要执行与常规虚拟机相同的步骤。</span><span class="sxs-lookup"><span data-stu-id="7da68-147">Currently, to enable this workflow you will need to go through the same steps as you would for a regular virtual machine.</span></span> <span data-ttu-id="7da68-148">我们正在寻找改善此体验的方法！</span><span class="sxs-lookup"><span data-stu-id="7da68-148">We are looking into ways to improve this experience!</span></span>

#### <a name="ipv6-access"></a><span data-ttu-id="7da68-149">IPv6 访问</span><span class="sxs-lookup"><span data-stu-id="7da68-149">IPv6 access</span></span>

<span data-ttu-id="7da68-150">WSL2 发行版目前无法访问仅限 IPv6 的地址。</span><span class="sxs-lookup"><span data-stu-id="7da68-150">WSL2 distros currently cannot reach IPv6 only addresses.</span></span> <span data-ttu-id="7da68-151">我们正在努力添加此功能。</span><span class="sxs-lookup"><span data-stu-id="7da68-151">We are working on adding this feature.</span></span>

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="7da68-152">了解 WSL 2 使用 VHD，如果达到其最大大小，会发生什么情况</span><span class="sxs-lookup"><span data-stu-id="7da68-152">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="7da68-153">WSL 2 将所有 Linux 文件都存储在使用 ext4 文件系统的 VHD 中。</span><span class="sxs-lookup"><span data-stu-id="7da68-153">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="7da68-154">此 VHD 会自动调整大小以满足你的存储需求。</span><span class="sxs-lookup"><span data-stu-id="7da68-154">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="7da68-155">此 VHD 的初始最大大小为256GB。</span><span class="sxs-lookup"><span data-stu-id="7da68-155">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="7da68-156">如果发行版大小增长到大于256GB，则会看到错误，指出磁盘空间不足。</span><span class="sxs-lookup"><span data-stu-id="7da68-156">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="7da68-157">可以通过扩展 VHD 大小来解决这些问题。</span><span class="sxs-lookup"><span data-stu-id="7da68-157">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="7da68-158">下面是有关如何执行此操作的说明：</span><span class="sxs-lookup"><span data-stu-id="7da68-158">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="7da68-159">使用 `wsl --shutdown` 命令终止所有 WSL 实例</span><span class="sxs-lookup"><span data-stu-id="7da68-159">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="7da68-160">查找你的发行版安装包名称 "PackageFamilyName"</span><span class="sxs-lookup"><span data-stu-id="7da68-160">Find your distro installation package name 'PackageFamilyName'</span></span>
   - <span data-ttu-id="7da68-161">在 powershell 提示符下（其中，"发行版" 是你的分发名称）键入：</span><span class="sxs-lookup"><span data-stu-id="7da68-161">In a powershell prompt (where 'distro' is your distribution name) type:</span></span>
      - `Get-AppxPackage -Name "*<distro>*" | Select PackageFamilyName`
3. <span data-ttu-id="7da68-162">找到 WSL 2 安装使用的 VHD 文件 fullpath，这将是 "pathToVHD"：</span><span class="sxs-lookup"><span data-stu-id="7da68-162">Locate the VHD file fullpath used by your WSL 2 installation, this will be your 'pathToVHD':</span></span>
     - `%LOCALAPPDATA%\Packages\<PackageFamilyName>\LocalState\<disk>.vhdx`
4. <span data-ttu-id="7da68-163">通过完成以下命令调整 WSL 2 VHD 的大小</span><span class="sxs-lookup"><span data-stu-id="7da68-163">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="7da68-164">使用管理员权限打开命令提示符窗口，并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="7da68-164">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `diskpart`
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
5. <span data-ttu-id="7da68-165">启动 WSL 发行版</span><span class="sxs-lookup"><span data-stu-id="7da68-165">Launch your WSL distro</span></span>
6. <span data-ttu-id="7da68-166">请注意，WSL 可以扩展其文件系统的大小</span><span class="sxs-lookup"><span data-stu-id="7da68-166">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="7da68-167">在 WSL 发行版中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="7da68-167">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="7da68-168">复制此项的名称，如下所示：/dev/sdXX （X 表示任何其他字符）</span><span class="sxs-lookup"><span data-stu-id="7da68-168">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="7da68-169">请确保使用之前复制的值，并且可能需要使用： `apt install resize2fs`。</span><span class="sxs-lookup"><span data-stu-id="7da68-169">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

<span data-ttu-id="7da68-170">请注意：一般而言，不要使用 Windows 工具或编辑器修改、移动或访问位于 AppData 文件夹内的 WSL 相关文件。</span><span class="sxs-lookup"><span data-stu-id="7da68-170">Please note: In general do not modify, move, or access the WSL related files located inside of your AppData folder using Windows tools or editors.</span></span> <span data-ttu-id="7da68-171">这样做可能会导致 Linux 发行版损坏。</span><span class="sxs-lookup"><span data-stu-id="7da68-171">Doing so could cause your Linux distro to become corrupted.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="7da68-172">WSL 2 将在启动时使用一些内存</span><span class="sxs-lookup"><span data-stu-id="7da68-172">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="7da68-173">WSL 2 在实际 Linux 内核上使用轻型实用程序 VM，以提供高性能的文件系统性能和系统调用的完全兼容性，同时仍然像 WSL 1 一样快速、快速、集成且响应迅速。</span><span class="sxs-lookup"><span data-stu-id="7da68-173">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="7da68-174">此实用程序 VM 的内存占用较小，将在启动时分配虚拟地址支持的内存。</span><span class="sxs-lookup"><span data-stu-id="7da68-174">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="7da68-175">将其配置为从总体内存的小部分开始。</span><span class="sxs-lookup"><span data-stu-id="7da68-175">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="7da68-176">在初始预览版中，跨 OS 文件速度会变慢</span><span class="sxs-lookup"><span data-stu-id="7da68-176">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="7da68-177">从 Linux 应用程序访问 Windows 文件或从 Windows 应用程序访问 Linux 文件时，与 WSL 1 相比，你会注意到文件速度更慢。</span><span class="sxs-lookup"><span data-stu-id="7da68-177">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="7da68-178">这是 WSL 2 中体系结构更改的结果，WSL 团队正在积极地调查如何改进此体验。</span><span class="sxs-lookup"><span data-stu-id="7da68-178">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>
