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
# <a name="user-experience-changes-between-wsl-1-and-wsl-2"></a><span data-ttu-id="e6669-104">WSL 1 与 WSL 2 的用户体验差异</span><span class="sxs-lookup"><span data-stu-id="e6669-104">User Experience Changes Between WSL 1 and WSL 2</span></span>

<span data-ttu-id="e6669-105">此页主要描述 WSL 1 和 WSL 2 预览版之间的用户体验差异。</span><span class="sxs-lookup"><span data-stu-id="e6669-105">This page goes over the user experience differences between WSL 1 and the WSL 2 preview.</span></span> <span data-ttu-id="e6669-106">关键差异包括：</span><span class="sxs-lookup"><span data-stu-id="e6669-106">The key changes to be aware of are:</span></span>

- <span data-ttu-id="e6669-107">将 Linux 应用需要访问的文件放在 Linux 根文件系统中可以提高文件访问速度</span><span class="sxs-lookup"><span data-stu-id="e6669-107">Place files that your Linux apps will access in your Linux root file system for faster file performance speed</span></span>
- <span data-ttu-id="e6669-108">在 WSL 2 预览版的初始版本中，你需要使用 IP 地址而不是 localhost 来访问网络应用程序</span><span class="sxs-lookup"><span data-stu-id="e6669-108">In initial builds of the WSL 2 preview you will need to access network applications using an IP address and not using localhost</span></span>

<span data-ttu-id="e6669-109">和下面是可能会注意到其他更改的完整列表：</span><span class="sxs-lookup"><span data-stu-id="e6669-109">And below is the full list of other changes that you may notice:</span></span>

- <span data-ttu-id="e6669-110">WSL 2 使用 VHD 来存储你的文件，如果达到其最大大小可能需要将其展开</span><span class="sxs-lookup"><span data-stu-id="e6669-110">WSL 2 uses a VHD to store your files and if you reach its max size you may need to expand it</span></span>
- <span data-ttu-id="e6669-111">在启动时，WSL 2 现在将使用内存的一小部分</span><span class="sxs-lookup"><span data-stu-id="e6669-111">When starting, WSL 2 will now use a small proportion of memory</span></span>
- <span data-ttu-id="e6669-112">跨 OS 文件访问速度会变慢初始预览版本中</span><span class="sxs-lookup"><span data-stu-id="e6669-112">Cross OS file access speed will be slower in initial preview builds</span></span>

## <a name="place-your-linux-files-in-your-linux-root-file-system"></a><span data-ttu-id="e6669-113">将 Linux 文件放在 Linux 根文件系统中</span><span class="sxs-lookup"><span data-stu-id="e6669-113">Place your Linux files in your Linux root file system</span></span>
<span data-ttu-id="e6669-114">请务必将为您将访问频繁使用 Linux 文件放在 Linux 应用程序根文件系统，从而享受文件性能优势。</span><span class="sxs-lookup"><span data-stu-id="e6669-114">Make sure to put the files that you will be accessing frequently with Linux applications inside of your Linux root file system to enjoy the file performance benefits.</span></span> <span data-ttu-id="e6669-115">这些文件一定要在 Linux 根文件系统，从而更快的文件系统访问。</span><span class="sxs-lookup"><span data-stu-id="e6669-115">These files have to be inside of the Linux root file system to have faster file system access.</span></span> <span data-ttu-id="e6669-116">我们还了它的 Windows 应用以访问 Linux 根文件系统 （如文件资源管理器 ！</span><span class="sxs-lookup"><span data-stu-id="e6669-116">We have also made it possible for Windows apps to access the Linux root file system (like File Explorer!</span></span> <span data-ttu-id="e6669-117">尝试运行：`explorer.exe /`在 bash shell 和会发生什么情况，请参阅) 这会使这一转换更加便捷。</span><span class="sxs-lookup"><span data-stu-id="e6669-117">Try running: `explorer.exe /` in your bash shell and see what happens) which will make this transition significantly easier.</span></span> 

## <a name="accessing-network-applications"></a><span data-ttu-id="e6669-118">访问网络的应用程序</span><span class="sxs-lookup"><span data-stu-id="e6669-118">Accessing network applications</span></span>
<span data-ttu-id="e6669-119">在 WSL 2 预览版的初始版本中，需要从 Windows 使用你的 Linux 发行版和从 Linux 使用您的主机的 IP 地址的任何 Windows 服务器的 IP 地址访问的任何 Linux 服务器。</span><span class="sxs-lookup"><span data-stu-id="e6669-119">In the initial builds of the WSL 2 preview, you will need to access any Linux server from Windows using the IP address of your Linux distro, and any Windows server from Linux using the IP address of your host machine.</span></span> <span data-ttu-id="e6669-120">这是临时的且在我们的优先级列表以修复非常高。</span><span class="sxs-lookup"><span data-stu-id="e6669-120">This is something that is temporary, and very high on our priority list to fix.</span></span>

### <a name="accessing-linux-applications-from-windows"></a><span data-ttu-id="e6669-121">从 Windows 访问 Linux 应用程序</span><span class="sxs-lookup"><span data-stu-id="e6669-121">Accessing Linux applications from Windows</span></span>
<span data-ttu-id="e6669-122">如果在 WSL 发行版中的服务器，将需要查找增强发行版虚拟机的 IP 地址并使用该 IP 地址连接到它。</span><span class="sxs-lookup"><span data-stu-id="e6669-122">If you have a server in a WSL distro, you'll need to find the IP address of the virtual machine powering your distro and connect to it with that IP address.</span></span> <span data-ttu-id="e6669-123">可以通过执行以下步骤来执行的操作：</span><span class="sxs-lookup"><span data-stu-id="e6669-123">You can do that by following these steps:</span></span>

- <span data-ttu-id="e6669-124">通过运行命令获得的发行版的 IP 地址`ip addr`WSL 发行版和查找下将其内部`inet`的值`eth0`接口。</span><span class="sxs-lookup"><span data-stu-id="e6669-124">Obtain the IP address of your distro by running the command `ip addr` inside of your WSL distro and finding it under the `inet` value of the `eth0` interface.</span></span>
   - <span data-ttu-id="e6669-125">通过筛选使用 grep 命令的输出，可以更轻松地找到此如下所示： `ip addr | grep eth0`。</span><span class="sxs-lookup"><span data-stu-id="e6669-125">You can find this more easily by filtering the output of the command using grep like so: `ip addr | grep eth0`.</span></span>
- <span data-ttu-id="e6669-126">连接到 Linux 服务器使用的 IP 上面找到。</span><span class="sxs-lookup"><span data-stu-id="e6669-126">Connect to your Linux server using the IP you found above.</span></span>

<span data-ttu-id="e6669-127">下面的图片显示出现这种通过连接到使用 Edge 浏览器的 nodeJS 服务器。</span><span class="sxs-lookup"><span data-stu-id="e6669-127">The picture below shows an example of this by connecting to a nodeJS server using the Edge browser.</span></span>

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-w2l.jpg)

### <a name="accessing-windows-applications-from-linux"></a><span data-ttu-id="e6669-129">从 Linux 访问 Windows 应用程序</span><span class="sxs-lookup"><span data-stu-id="e6669-129">Accessing Windows applications from Linux</span></span>
<span data-ttu-id="e6669-130">若要访问 Windows 网络应用程序将需要使用您的主机的 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="e6669-130">To access a Windows network application you'll need to use the IP address of your host machine.</span></span> <span data-ttu-id="e6669-131">可以通过以下步骤进行操作：</span><span class="sxs-lookup"><span data-stu-id="e6669-131">You can do so with these steps:</span></span>

- <span data-ttu-id="e6669-132">通过运行命令来获取您的主机的 IP 地址`cat /etc/resolv.conf`并复制以下术语的 IP 地址`nameserver`。</span><span class="sxs-lookup"><span data-stu-id="e6669-132">Obtain the IP address of your host machine by running the command `cat /etc/resolv.conf` and copying the IP address following the term `nameserver`.</span></span> 
- <span data-ttu-id="e6669-133">连接到使用复制的 IP 地址的任何 Windows 服务器。</span><span class="sxs-lookup"><span data-stu-id="e6669-133">Connect to any Windows server using the copied IP address.</span></span>

<span data-ttu-id="e6669-134">下面的图片显示出现这种通过连接到通过 curl 在 Windows 中运行的 python 服务器。</span><span class="sxs-lookup"><span data-stu-id="e6669-134">The picture below shows an example of this by connecting to a python server running in Windows via curl.</span></span> 

![从 Windows 访问 Linux 网络应用程序](media/wsl2-network-l2w.png)

## <a name="understanding-wsl-2-uses-a-vhd-and-what-to-do-if-you-reach-its-max-size"></a><span data-ttu-id="e6669-136">了解 WSL 2 使用 VHD，以及要执行的操作如果达到其最大大小</span><span class="sxs-lookup"><span data-stu-id="e6669-136">Understanding WSL 2 uses a VHD, and what to do if you reach its max size</span></span>
<span data-ttu-id="e6669-137">WSL 2 将存储的 VHD，使用 ext4 文件系统内的所有 Linux 文件。</span><span class="sxs-lookup"><span data-stu-id="e6669-137">WSL 2 stores all your Linux files inside of a VHD that uses the ext4 file system.</span></span> <span data-ttu-id="e6669-138">此 VHD 自动调整大小以满足你的存储需求。</span><span class="sxs-lookup"><span data-stu-id="e6669-138">This VHD automatically resizes to meet your storage needs.</span></span> <span data-ttu-id="e6669-139">此 VHD 还具有初始最大大小为 256 GB。</span><span class="sxs-lookup"><span data-stu-id="e6669-139">This VHD also has an initial max size of 256GB.</span></span> <span data-ttu-id="e6669-140">如果你的发行增长的大小大于 256 GB，将看到错误消息指出已耗尽磁盘空间。</span><span class="sxs-lookup"><span data-stu-id="e6669-140">If your distro grows in size to be greater than 256GB you will see errors stating that you've run out of disk space.</span></span> <span data-ttu-id="e6669-141">您可以解决这些通过扩展的 VHD 大小。</span><span class="sxs-lookup"><span data-stu-id="e6669-141">You can fix these by expanding the VHD size.</span></span> <span data-ttu-id="e6669-142">有关如何执行此操作的说明如下所示：</span><span class="sxs-lookup"><span data-stu-id="e6669-142">Instructions on how to do so are below:</span></span>

1. <span data-ttu-id="e6669-143">终止所有 WSL 实例使用`wsl --shutdown`命令</span><span class="sxs-lookup"><span data-stu-id="e6669-143">Terminate all WSL instances using the `wsl --shutdown` command</span></span>
2. <span data-ttu-id="e6669-144">通过完成以下命令调整 WSL 2 VHD 的大小</span><span class="sxs-lookup"><span data-stu-id="e6669-144">Resize your WSL 2 VHD by completing the following commands</span></span>
   - <span data-ttu-id="e6669-145">使用管理员权限打开命令提示符窗口并运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e6669-145">Open a command prompt Window with admin privileges and run the following commands:</span></span>
      - `Select vdisk file="<pathToVHD>"`
      - `expand vdisk maximum="<sizeInMegaBytes>"`
3. <span data-ttu-id="e6669-146">启动 WSL 发行版</span><span class="sxs-lookup"><span data-stu-id="e6669-146">Launch your WSL distro</span></span>
4. <span data-ttu-id="e6669-147">请注意，它可以扩展其文件系统大小 WSL</span><span class="sxs-lookup"><span data-stu-id="e6669-147">Make WSL aware that it can expand its file system's size</span></span>
   - <span data-ttu-id="e6669-148">在 WSL 发行版中运行以下命令：</span><span class="sxs-lookup"><span data-stu-id="e6669-148">Run these commands in your WSL distro:</span></span>
      - `sudo mount -t devtmpfs none /dev`
      - `mount | grep ext4`
         - <span data-ttu-id="e6669-149">复制看起来类似于此项的名称: / sdXX (带有 X 表示任何其他字符)</span><span class="sxs-lookup"><span data-stu-id="e6669-149">Copy the name of this entry, which will look like: /dev/sdXX (with the X representing any other character)</span></span>
      - `sudo resize2fs /dev/sdXX`
         - <span data-ttu-id="e6669-150">请确保要使用的值之前复制，并且可能需要使用： `apt install resize2fs`。</span><span class="sxs-lookup"><span data-stu-id="e6669-150">Make sure to use the value you copied earlier, and you may need to use: `apt install resize2fs`.</span></span>

## <a name="wsl-2-will-use-some-memory-on-startup"></a><span data-ttu-id="e6669-151">WSL 2 将在启动时使用一些内存</span><span class="sxs-lookup"><span data-stu-id="e6669-151">WSL 2 will use some memory on startup</span></span>
<span data-ttu-id="e6669-152">WSL 2 在真实的 Linux 内核上使用轻量级实用工具 VM 提供很好的文件系统性能和完整的系统调用兼容性时仍是只需为轻，快速、 集成和 WSL 1 的响应速度。</span><span class="sxs-lookup"><span data-stu-id="e6669-152">WSL 2 uses a lightweight utility VM on a real Linux kernel to provide great file system performance and full system call compatibility while still being just as light, fast, integrated and responsive as WSL 1.</span></span> <span data-ttu-id="e6669-153">此实用程序 VM 具有小的内存需求量，并将备份的虚拟地址上分配内存启动。</span><span class="sxs-lookup"><span data-stu-id="e6669-153">This utility VM has a small memory footprint and will allocate Virtual Address backed memory on startup.</span></span> <span data-ttu-id="e6669-154">它配置为启动与总内存的一小部分。</span><span class="sxs-lookup"><span data-stu-id="e6669-154">It is configured to start with a small proportion of your total memory.</span></span>

## <a name="cross-os-file-speed-will-be-slower-in-initial-preview-builds"></a><span data-ttu-id="e6669-155">跨 OS 文件速度会变慢初始预览版本中</span><span class="sxs-lookup"><span data-stu-id="e6669-155">Cross OS file speed will be slower in initial preview builds</span></span>
<span data-ttu-id="e6669-156">您将注意到文件的速度比 WSL 1 从 Linux 应用程序，或从 Windows 应用程序访问 Linux 文件访问 Windows 文件时。</span><span class="sxs-lookup"><span data-stu-id="e6669-156">You will notice slower file speeds compared to WSL 1 when accessing Windows files from a Linux application, or accessing Linux files from a Windows application.</span></span> <span data-ttu-id="e6669-157">这是在 WSL 2 中，体系结构的更改的结果，是指 WSL 团队正在调查上我们可以如何改进此体验。</span><span class="sxs-lookup"><span data-stu-id="e6669-157">This is a result of the architectural changes in WSL 2, and is something that the WSL team is actively investigating on how we can improve this experience.</span></span>