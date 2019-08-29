---
title: 适用于 Linux 的 Windows 子系统疑难解答
description: 提供有关在适用于 Linux 的 Windows 子系统上运行 Linux 时遇到的常见错误和问题的详细信息。
keywords: BashOnWindows、bash、wsl、windows、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.localizationpriority: high
ms.openlocfilehash: 6a5fec8b8e054b4d3399ee9bcd903acebca7aace
ms.sourcegitcommit: 7af6b7a3f8cfa66cb25115bc26f44aa64ef22811
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/28/2019
ms.locfileid: "70122695"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统疑难解答

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>在连接到 VPN 后, Bash 失去网络连接

如果在连接到 Windows 上的 VPN 后, bash 失去网络连接, 请从 bash 内尝试此解决方法。 此解决方法可让你通过`/etc/resolv.conf`手动替代 DNS 解析。

1. 记下 VPN 的 DNS 服务器`ipconfig.exe /all`
2. 创建现有 resolv.conf 的副本`sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 取消当前 resolv.conf 的链接`sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 打开`/etc/resolv.conf`并 <br/>
   a. 删除文件中的第一行, 其中显示 "\#此文件是由 WSL 自动生成的。 若要停止自动生成此文件, 请删除此行。 "。 <br/>
   b. 在 DNS 服务器列表中, 从 (1) 添加 DNS 条目, 作为第一个条目。 <br/>
   c. 关闭该文件。 <br/>

断开 VPN 连接后, 必须将更改还原为`/etc/resolv.conf`。 为此, 请执行以下操作:
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>启动 WSL 或安装分发返回了错误代码

按照[这些说明](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)收集 GitHub 上的详细日志并记录问题。

### <a name="updating-bash-on-ubuntu-on-windows"></a>在 Windows 上更新在 Ubuntu 上的 Bash

Windows 上的 Bash 上有两个需要更新的组件。 

1. 适用于 Linux 的 Windows 子系统
  
   在 Windows 上的 Ubuntu 上升级此部分 Bash 会启用[发行说明](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)中的任何新的修补程序概述。 确保你已订阅 Windows 预览体验计划, 并且你的生成是最新版本。 为了获得更精细的控制, 包括重置 Ubuntu 实例, 请签出 "[命令引用" 页](https://msdn.microsoft.com/en-us/commandline/wsl/reference)。

2. Ubuntu 用户二进制文件 

   在 Windows 上的 Ubuntu 上升级此部分 Bash 会将任何更新安装到 Ubuntu 用户二进制文件, 包括已通过 apt 安装的应用程序。 若要更新, 请在 Bash 中运行以下命令:
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Apt-获取升级错误
某些包使用我们尚未实现的功能。 `udev`例如, 尚不支持, 并导致几个`apt-get upgrade`错误。

若要解决与相关`udev`的问题, 请执行以下步骤:

1. 将以下项写入`/usr/sbin/policy-rc.d`到中, 并保存所做的更改。
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 向添加执行权限`/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 运行以下命令
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>条0x80040306 "安装时
这与我们不支持旧版控制台这一事实有关。
关闭旧版控制台:

1. 打开 cmd.exe
1. 右键单击标题栏-> 属性-> 取消选中 "使用旧版控制台"
1. 单击“确定”

### <a name="error-0x80040154-after-windows-update"></a>条0x80040154 "Windows 更新后
Windows 更新时, 适用于 Linux 的 Windows 子系统功能可能处于禁用状态。 如果出现这种情况, 则必须重新启用 Windows 功能。 有关启用适用于 Linux 的 Windows 子系统的说明, 请参阅[安装指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

### <a name="changing-the-display-language"></a>更改显示语言
WSL 安装将尝试自动更改 Ubuntu 区域设置以与 Windows 安装的区域设置相匹配。  如果不想要此行为, 可以在安装完成后运行此命令来更改 Ubuntu 区域设置。  要使此更改生效, 您必须重新启动 bash。

下面的示例将区域设置更改为 en-us:
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 系统还原后的安装问题
1.  删除该`%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`文件夹。 <br/>
  **注意：如果可选功能已完全安装并且工作正常, 请不要执行此操作。**
2.  启用 WSL 可选功能 (如果尚未这样做)
3.  重新启动
4.  lxrun/uninstall/full
5.  安装 bash

### <a name="no-internet-access-in-wsl"></a>WSL 中无 internet 访问权限
某些用户已报告在 WSL 中阻止 internet 访问的特定防火墙应用程序的问题。  报告的防火墙包括:

1. Kaspersky 等
1. AVG
1. Avast

在某些情况下, 关闭防火墙允许进行访问。  在某些情况下, 只需安装防火墙即可阻止访问。

### <a name="permission-denied-error-when-using-ping"></a>使用 ping 时权限被拒绝错误
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14388-to-windows-10-anniversary-update"></a>[周年更新](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

Windows 中的管理员权限需要在 WSL 中运行 ping。  若要运行 ping, 请在 Windows 上的 Ubuntu 上以管理员身份运行 Bash, 或从具有管理员权限的 CMD/PowerShell 提示符运行 bash。

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslrelease_notesbuild-14926"></a>[生成 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  不再需要管理员权限。

### <a name="bash-is-hung"></a>Bash 挂起
如果使用 bash, 你会发现 bash 挂起 (或死锁), 不响应输入, 请通过收集和报告内存转储来帮助我们诊断问题。 请注意, 这些步骤会使你的系统崩溃。 如果您不熟悉此操作或在执行此操作之前保存您的工作, 请不要这样做。  <br/>
收集内存转储:
1. 将内存转储类型更改为 "完成内存转储"。 更改转储类型时, 请记下当前类型。
2. 使用键盘控制[步骤](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/)来配置故障。
3. 重现挂起或死锁。
4. 使用 (2) 中的密钥序列来崩溃系统。
5. 系统将崩溃并收集内存转储。
6. 系统重新启动后, 会将 dmp 报告给secure@microsoft.com。 转储文件的默认位置是%SystemRoot%\memory.dmp 或 C:\Windows\memory.dmp (如果 C: 是系统驱动器)。 请注意, 在电子邮件中, 此转储适用于 Windows 团队上的 WSL 或 Bash。
7. 将内存转储类型还原为原始设置。

### <a name="check-your-build-number"></a>检查生成号

若要查找你的电脑体系结构和 Windows 内部版本号, 请打开  
**设置** > **系统**有关 > 

查找 "**操作系统生成**" 和 "**系统类型**" 字段。  
    !["生成" 和 "系统类型" 字段的屏幕截图](media/system.png) 


若要查找 Windows Server 内部版本号, 请在 PowerShell 中运行以下内容:  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>确认 WSL 已启用
可以通过在 PowerShell 中运行以下内容来确认是否已启用适用于 Linux 的 Windows 子系统:  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH-服务器连接问题
尝试连接 SSH 服务器失败, 出现以下错误:"连接被127.0.0.1 端口22关闭"。
1. 请确保 OpenSSH 服务器正在运行:
   ``` BASH
   sudo service ssh status
   ```
   你已按照本教程进行操作: https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. 停止 sshd 服务并在调试模式下启动 sshd:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 检查启动日志并确保 HostKeys 可用, 并且看不到日志消息, 如:
   ```
   debug1: sshd version OpenSSH_7.2, OpenSSL 1.0.2g  1 Mar 2016
   debug1: key_load_private: incorrect passphrase supplied to decrypt private key
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_rsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_dsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ecdsa_key
   debug1: key_load_private: No such file or directory
   debug1: key_load_public: No such file or directory
   Could not load host key: /etc/ssh/ssh_host_ed25519_key
   ```

如果看不到下面`/etc/ssh/`这样的消息, 则需要重新生成密钥, 或者只是清除 & 安装 openssh-服务器:
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

