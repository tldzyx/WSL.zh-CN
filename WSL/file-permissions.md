---
title: 文件权限
description: 了解 WSL 如何确定 Windows 中的文件权限
keywords: BashOnWindows、bash、wsl、wsl2、windows、适用于 linux、windowssubsystem、ubuntu、debian、suse、windows 10、文件和权限的 windows 子系统
ms.date: 01/14/2020
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 4566fc86cf14df986bde80cf3a6cfb9267b23308
ms.sourcegitcommit: 07eb5f2e1f4517928165dda4510012599b0d0e1e
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/22/2020
ms.locfileid: "76520856"
---
# <a name="file-permissions-for-wsl"></a><span data-ttu-id="1ffc7-104">WSL 的文件权限</span><span class="sxs-lookup"><span data-stu-id="1ffc7-104">File Permissions for WSL</span></span>

<span data-ttu-id="1ffc7-105">本页详细说明了如何在适用于 Linux 的 Windows 子系统中解释 Linux 文件权限，尤其是在 NT 文件系统上访问 Windows 中的资源时。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-105">This page details how Linux file permissions are interpreted across the Windows Subsystem for Linux, especially when accessing resources inside of Windows on the NT file system.</span></span> <span data-ttu-id="1ffc7-106">本文档假定你基本了解[Linux 文件系统权限结构](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span><span class="sxs-lookup"><span data-stu-id="1ffc7-106">This documentation assumes a basic understanding of the [Linux file system permissions structure](https://wiki.archlinux.org/index.php/File_permissions_and_attributes)</span></span> <!--TODO: Double check that it's okay to add these links--> <span data-ttu-id="1ffc7-107">和[umask 命令](https://en.wikipedia.org/wiki/Umask)。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-107">and the [umask command](https://en.wikipedia.org/wiki/Umask).</span></span>

<span data-ttu-id="1ffc7-108">从 WSL 访问 Windows 文件时，文件权限是从 Windows 权限计算的，或者是从已由 WSL 添加到文件的元数据中读取的。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-108">When accessing Windows files from WSL the file permissions are either calculated from Windows permissions, or are read from metadata that has been added to the file by WSL.</span></span> <span data-ttu-id="1ffc7-109">默认情况下不启用此元数据。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-109">This metadata is not enabled by default.</span></span> 

## <a name="wsl-metadata-on-windows-files"></a><span data-ttu-id="1ffc7-110">WSL Windows 文件上的元数据</span><span class="sxs-lookup"><span data-stu-id="1ffc7-110">WSL metadata on Windows files</span></span>

<span data-ttu-id="1ffc7-111">如果在 WSL 中启用了元数据作为装载选项，则可以添加和解释 Windows NT 文件上的扩展属性以提供 Linux 文件系统权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-111">When metadata is enabled as a mount option in WSL, extended attributes on Windows NT files can be added and interpreted to supply Linux file system permissions.</span></span> 

<span data-ttu-id="1ffc7-112">WSL 可以添加四个 NTFS 扩展属性：</span><span class="sxs-lookup"><span data-stu-id="1ffc7-112">WSL can add four NTFS extended attributes:</span></span>

| <span data-ttu-id="1ffc7-113">属性名称</span><span class="sxs-lookup"><span data-stu-id="1ffc7-113">Attribute Name</span></span> | <span data-ttu-id="1ffc7-114">说明</span><span class="sxs-lookup"><span data-stu-id="1ffc7-114">Description</span></span> |
| --- | --- |
| <span data-ttu-id="1ffc7-115">$LXUID</span><span class="sxs-lookup"><span data-stu-id="1ffc7-115">$LXUID</span></span> | <span data-ttu-id="1ffc7-116">用户所有者 ID</span><span class="sxs-lookup"><span data-stu-id="1ffc7-116">User Owner ID</span></span> |
| <span data-ttu-id="1ffc7-117">$LXGID</span><span class="sxs-lookup"><span data-stu-id="1ffc7-117">$LXGID</span></span> | <span data-ttu-id="1ffc7-118">组所有者 ID</span><span class="sxs-lookup"><span data-stu-id="1ffc7-118">Group Owner ID</span></span> |
| <span data-ttu-id="1ffc7-119">$LXMOD</span><span class="sxs-lookup"><span data-stu-id="1ffc7-119">$LXMOD</span></span> | <span data-ttu-id="1ffc7-120">文件模式（文件系统权限八进制数字和类型，例如：0777）</span><span class="sxs-lookup"><span data-stu-id="1ffc7-120">File mode (File systems permission octals and type, e.g: 0777)</span></span> |
| <span data-ttu-id="1ffc7-121">$LXDEV</span><span class="sxs-lookup"><span data-stu-id="1ffc7-121">$LXDEV</span></span> | <span data-ttu-id="1ffc7-122">设备（如果它是设备文件）</span><span class="sxs-lookup"><span data-stu-id="1ffc7-122">Device, if it is a device file</span></span> |

<span data-ttu-id="1ffc7-123">此外，任何不是常规文件或目录的文件（例如：符号链接、FIFOs、块设备、unix 套接字和字符设备）也具有 NTFS 重新[分析点](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points)。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-123">Additionally, any file that is not a regular file or directory (e.g: symlinks, FIFOs, block devices, unix sockets, and character devices) also have an NTFS [reparse point](https://docs.microsoft.com/en-us/windows/win32/fileio/reparse-points).</span></span> <span data-ttu-id="1ffc7-124">这样，就可以更快地确定给定目录中的文件类型，而不必查询其扩展属性。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-124">This makes it much faster to determine the kind of file in a given directory without having to query its extended attributes.</span></span> 
<!-- TODO: For the blog include ONeDrive detail -->

## <a name="file-access-scenarios"></a><span data-ttu-id="1ffc7-125">文件访问方案</span><span class="sxs-lookup"><span data-stu-id="1ffc7-125">File Access Scenarios</span></span>

<span data-ttu-id="1ffc7-126">下面说明如何使用适用于 Linux 的 Windows 子系统以不同的方式访问文件时如何确定权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-126">Below is a description of how permissions are determined when accessing files in different ways using the Windows Subsystem for Linux.</span></span>

### <a name="accessing-files-in-the-windows-drive-file-system-drvfs-from-linux"></a><span data-ttu-id="1ffc7-127">从 Linux 访问 Windows 驱动器文件系统（DrvFS）中的文件</span><span class="sxs-lookup"><span data-stu-id="1ffc7-127">Accessing Files in the Windows drive file system (DrvFS) from Linux</span></span>

<span data-ttu-id="1ffc7-128">在从 WSL 访问 Windows 文件（最有可能通过 `/mnt/c`）时，会出现这些情况。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-128">These scenarios occur when you are accessing your Windows files from WSL, most likely via `/mnt/c`.</span></span> 

#### <a name="reading-file-permissions-from-an-existing-windows-file"></a><span data-ttu-id="1ffc7-129">从现有 Windows 文件读取文件权限</span><span class="sxs-lookup"><span data-stu-id="1ffc7-129">Reading file permissions from an existing Windows file</span></span>

<span data-ttu-id="1ffc7-130">结果取决于文件是否已具有现有元数据。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-130">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="1ffc7-131">**该文件没有元数据（默认值）**</span><span class="sxs-lookup"><span data-stu-id="1ffc7-131">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="1ffc7-132">如果文件没有关联的元数据，则我们会将 Windows 用户的有效权限转换为读取/写入/执行 bits，并将其设置为与用户、组和其他相同的值。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-132">If the file has no metadata associated with it then we translate the effective permissions of the Windows user to read/write/execute bits and set them to the this as the same value for user, group, and other.</span></span> <span data-ttu-id="1ffc7-133">例如，如果您的 Windows 用户帐户具有读取和执行访问权限，但不具有对该文件的写访问权限，则该帐户将显示为 "用户"、"组" 和 "其他" `r-x`。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-133">For example, if your Windows user account has read and execute access but not write access to the file then this will be shown as `r-x` for user, group and other.</span></span> <span data-ttu-id="1ffc7-134">如果该文件在 Windows 中设置为 "只读" 属性，则不会在 Linux 中授予写入权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-134">If the file has the 'Read Only' attribute set in Windows then we do not grant write access in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="1ffc7-135">文件包含元数据</span><span class="sxs-lookup"><span data-stu-id="1ffc7-135">The file has metadata</span></span>

<span data-ttu-id="1ffc7-136">如果文件包含元数据，则只需使用这些元数据值，而不是转换 Windows 用户的有效权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-136">If the file has metadata present, we simply use those metadata values instead of translating effective permissions of the Windows user.</span></span>

#### <a name="changing-file-permissions-on-an-existing-windows-file-using-chmod"></a><span data-ttu-id="1ffc7-137">使用 chmod 更改现有 Windows 文件的文件权限</span><span class="sxs-lookup"><span data-stu-id="1ffc7-137">Changing file permissions on an existing Windows file using chmod</span></span>

<span data-ttu-id="1ffc7-138">结果取决于文件是否已具有现有元数据。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-138">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="1ffc7-139">**该文件没有元数据（默认值）**</span><span class="sxs-lookup"><span data-stu-id="1ffc7-139">**The file does not have metadata (default)**</span></span>

<span data-ttu-id="1ffc7-140">Chmod 只有一种效果，如果删除文件的所有写入属性，则会设置 Windows 文件的 "只读" 属性，因为这是与 CIFS （通用 Internet 文件系统）相同的行为，后者是 Linux 中的 SMB （服务器消息块）客户端。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-140">Chmod will only have one effect, if you remove all the write attributes of a file then the 'read only' attribute on the Windows file will be set, since this is the same behaviour as CIFS (Common Internet File System) which is the SMB (Server Message Block) client in Linux.</span></span>

##### <a name="the-file-has-metadata"></a><span data-ttu-id="1ffc7-141">文件包含元数据</span><span class="sxs-lookup"><span data-stu-id="1ffc7-141">The file has metadata</span></span>

<span data-ttu-id="1ffc7-142">Chmod 将根据文件已有的现有元数据更改或添加元数据。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-142">Chmod will change or add metadata depending on the file's already existing metadata.</span></span> 

<span data-ttu-id="1ffc7-143">请记住，您不能为自己授予对 Windows 的访问权限，即使元数据指出这一点也是如此。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-143">Please keep in mind that you cannot give yourself more access than what you have on Windows, even if the metadata says that is the case.</span></span> <span data-ttu-id="1ffc7-144">例如，你可以将元数据设置为显示你对使用 `chmod 777`的文件具有写入权限，但如果你尝试访问该文件，则你仍无法写入该文件。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-144">For example, you could set the metadata to display that you have write permissions to a file using `chmod 777`, but if you tried to access that file you would still not be able to write to it.</span></span> <span data-ttu-id="1ffc7-145">这是因为 interopability，因为 Windows 文件的任何读取或写入命令均通过 Windows 用户权限进行路由。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-145">This is thanks to interopability, as any read or write commands to Windows files are routed through your Windows user permissions.</span></span>

#### <a name="creating-a-file-in-drivefs"></a><span data-ttu-id="1ffc7-146">在 DriveFS 中创建文件</span><span class="sxs-lookup"><span data-stu-id="1ffc7-146">Creating a file in DriveFS</span></span>

<span data-ttu-id="1ffc7-147">结果取决于是否启用了元数据。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-147">The result depends on if metadata is enabled.</span></span>

##### <a name="metadata-is-not-enabled-default"></a><span data-ttu-id="1ffc7-148">未启用元数据（默认值）</span><span class="sxs-lookup"><span data-stu-id="1ffc7-148">Metadata is not enabled (default)</span></span>

<span data-ttu-id="1ffc7-149">新创建的文件的 Windows 权限将与您在没有特定安全描述符的 Windows 中创建文件相同，它将继承父级的权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-149">The Windows permissions of the newly created file will be the same as if you created the file in Windows without a specific security descriptor, it will inherit the parent's permissions.</span></span> 

##### <a name="metadata-is-enabled"></a><span data-ttu-id="1ffc7-150">已启用元数据</span><span class="sxs-lookup"><span data-stu-id="1ffc7-150">Metadata is enabled</span></span>

<span data-ttu-id="1ffc7-151">文件的权限位设置为遵循 Linux umask，文件将随元数据一起保存。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-151">The file's permission bits are set to follow the Linux umask, and the file will be saved with metadata.</span></span>

#### <a name="which-linux-user-and-linux-group-owns-the-file"></a><span data-ttu-id="1ffc7-152">哪个 Linux 用户和 Linux 组拥有该文件？</span><span class="sxs-lookup"><span data-stu-id="1ffc7-152">Which Linux user and Linux group owns the file?</span></span> 

<span data-ttu-id="1ffc7-153">结果取决于文件是否已具有现有元数据。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-153">The result depends on if the file already has existing metadata.</span></span>

##### <a name="the-file-does-not-have-metadata-default"></a><span data-ttu-id="1ffc7-154">**该文件没有元数据（默认值）**</span><span class="sxs-lookup"><span data-stu-id="1ffc7-154">**The file does not have metadata (default)**</span></span>
<span data-ttu-id="1ffc7-155">在默认情况下，当 automounting Windows 驱动器时，我们将指定任何文件的用户 ID （UID）设置为 WSL 用户的用户 ID，并且组 ID （GID）设置为 WSL 用户的主体组 ID。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-155">In the default scenario, when automounting Windows drives, we specify that the user ID (UID) for any file is set to the user ID of your WSL user and the group ID (GID) is set to the principal group ID of your WSL user.</span></span> 

##### <a name="the-file-has-metadata"></a><span data-ttu-id="1ffc7-156">文件包含元数据</span><span class="sxs-lookup"><span data-stu-id="1ffc7-156">The file has metadata</span></span>

<span data-ttu-id="1ffc7-157">在元数据中指定的 UID 和 GID 将应用为该文件的用户所有者和组所有者。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-157">The UID and GID specified in the metadata is applied as the user owner and group owner of the file.</span></span> 

### <a name="accessing-linux-files-from-windows-using-wsl"></a><span data-ttu-id="1ffc7-158">使用 `\\wsl$` 从 Windows 访问 Linux 文件</span><span class="sxs-lookup"><span data-stu-id="1ffc7-158">Accessing Linux files from Windows using `\\wsl$`</span></span>

<span data-ttu-id="1ffc7-159">通过 `\\wsl$` 访问 Linux 文件将使用 WSL 发行版的默认用户。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-159">Accessing Linux files via `\\wsl$` will use the default user of your WSL distro.</span></span> <span data-ttu-id="1ffc7-160">因此，任何访问 Linux 文件的 Windows 应用都具有与默认用户相同的权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-160">Therefore any Windows app accessing Linux files will have the same permissions as the default user.</span></span>

#### <a name="creating-a-new-file"></a><span data-ttu-id="1ffc7-161">创建新文件</span><span class="sxs-lookup"><span data-stu-id="1ffc7-161">Creating a new file</span></span>

<span data-ttu-id="1ffc7-162">在 Windows 的 WSL 发行版内部创建新文件时，将应用默认 umask。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-162">The default umask is applied when creating a new file inside of a WSL distro from Windows.</span></span> <span data-ttu-id="1ffc7-163">默认的 umask 是 `022`的，也就是说，它允许除对组和其他权限以外的所有权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-163">The default umask is `022`, or in other words it allows all permissions except write permissions to groups and others.</span></span> 

### <a name="accessing-files-in-the-linux-root-file-system-from-linux"></a><span data-ttu-id="1ffc7-164">从 Linux 访问 Linux 根文件系统中的文件</span><span class="sxs-lookup"><span data-stu-id="1ffc7-164">Accessing files in the Linux root file system from Linux</span></span>

<span data-ttu-id="1ffc7-165">在 Linux 根文件系统中创建、修改或访问的任何文件都遵循标准 Linux 约定，例如将 umask 应用到新创建的文件。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-165">Any files created, modified, or accessed in the Linux root file system follow standard Linux conventions, such as applying the umask to a newly created file.</span></span>

## <a name="configuring-file-permissions"></a><span data-ttu-id="1ffc7-166">配置文件权限</span><span class="sxs-lookup"><span data-stu-id="1ffc7-166">Configuring file permissions</span></span>

<span data-ttu-id="1ffc7-167">可以使用 wsl 中的装载选项在 Windows 驱动器内配置文件权限。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-167">You can configure your file permissions inside of your Windows drives using the mount options in wsl.conf.</span></span> <span data-ttu-id="1ffc7-168">装载选项允许您设置 `umask`、`dmask` 和 `fmask` 权限掩码。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-168">The mount options allow you to set `umask`, `dmask` and `fmask` permissions masks.</span></span> <span data-ttu-id="1ffc7-169">`umask` 应用于所有文件，`dmask` 只应用于目录，而 `fmask` 只应用于文件。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-169">The `umask` is applied to all files, the `dmask` is applied just to directories and the `fmask` is applied just to files.</span></span> <span data-ttu-id="1ffc7-170">然后，在应用到文件时，这些权限掩码会进行逻辑或操作（例如：如果 `umask` 值为 `023`，将 `fmask` 值 `022`，则会 `023`为文件生成的权限掩码。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-170">These permission masks are then put through a logical OR operation when being applied to files, e.g: If you have a `umask` value of `023` and an `fmask` value of `022` then the resulting permissions mask for files will be `023`.</span></span> 

<span data-ttu-id="1ffc7-171">有关如何执行此操作的说明，请参阅["管理 Linux 分发"](./wsl-config.md)文档页。</span><span class="sxs-lookup"><span data-stu-id="1ffc7-171">Please see the ['Manage Linux Distributions'](./wsl-config.md) document page for instructions on how to do this.</span></span>
<!-- TODO: Add # to the link-->

