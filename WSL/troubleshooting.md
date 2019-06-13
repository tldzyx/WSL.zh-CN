---
title: 适用于 Linux 的疑难解答 Windows Susbystem
description: 提供有关常见的错误详细的信息和发出到运行的人在适用于 Linux 上 Windows Susbystem 运行 Linux 时。
keywords: BashOnWindows，bash、 wsl、 windows、 windowssubsystem、 ubuntu
author: scooley
ms.author: scooley
ms.date: 11/15/2017
ms.topic: article
ms.assetid: 6753f1b2-200e-49cc-93a5-4323e1117246
ms.custom: seodec18
ms.openlocfilehash: feb9e25da73eeb0d7f0cef4014221a42e2ca179b
ms.sourcegitcommit: db69625e26bc141ea379a830790b329e51ed466b
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2019
ms.locfileid: "67040846"
---
# <a name="troubleshooting-windows-subsystem-for-linux"></a>适用于 Linux 的故障排除 Windows 子系统

### <a name="bash-loses-network-connectivity-once-connected-to-a-vpn"></a>Bash 一次连接到 VPN 的网络连接丢失

如果连接到在 Windows 上的 VPN 后，bash 丢失网络连接性，请尝试从 bash 中的此解决方法。 此解决方法便可以手动重写通过 DNS 解析`/etc/resolv.conf`。

1. 记下与执行 VPN 的 DNS 服务器 `ipconfig.exe /all`
2. 制作一份现有 resolv.conf `sudo cp /etc/resolv.conf /etc/resolv.conf.new`
3. 取消链接当前 resolv.con `sudo unlink /etc/resolv.conf`
4. `sudo mv /etc/resolv.conf.new /etc/resolv.conf`
5. 打开`/etc/resolv.conf`和 <br/>
   a. 从该文件，这表示删除的第一行"\# WSL 由自动生成此文件。 若要停止自动生成此文件，请删除此行。"。 <br/>
   b. DNS 服务器列表中的第一个条目，可将 DNS 条目 (1) 添加上面。 <br/>
   c. 关闭该文件。 <br/>

后已断开连接 VPN，你将需要还原到的更改`/etc/resolv.conf`。 若要执行此操作，请执行：
1. `cd /etc`
2. `sudo mv resolv.conf resolv.conf.new`
3. `sudo ln -s ../run/resolvconf/resolv.conf resolv.conf`

### <a name="starting-wsl-or-installing-a-distribution-returns-an-error-code"></a>启动 WSL 或安装分发将返回错误代码

请按照[这些说明](https://github.com/Microsoft/WSL/blob/master/CONTRIBUTING.md#8-detailed-logs)收集详细的日志并在 GitHub 上提出问题。

### <a name="updating-bash-on-ubuntu-on-windows"></a>正在更新 Bash on Ubuntu 上 Windows

有两个组件的 Bash on Ubuntu 上可能需要更新的 Windows。 

1. 适用于 Linux 的 Windows 子系统
  
   升级 Bash on Ubuntu 上 Windows 的此部分将启用在任何新的修补程序大纲[发行说明](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes)。 请确保你已订阅 Windows 预览体验计划以及你的生成是最新。 对于更细粒度控制，包括重置你的 Ubuntu 实例签出[命令参考页](https://msdn.microsoft.com/en-us/commandline/wsl/reference)。

2. Ubuntu 用户二进制文件 

   升级 Bash on Ubuntu 上 Windows 的此部分将安装到 Ubuntu 用户二进制文件包括已通过 apt-get 安装的应用程序的任何更新。 若要更新运行以下命令在 Bash 中：
  
   1. `apt-get update`
   2. `apt-get upgrade`
  
### <a name="apt-get-upgrade-errors"></a>Pt-get 升级错误
某些包使用我们尚未实现的功能。 `udev`例如，尚不支持并导致多`apt-get upgrade`错误。

若要修复与相关的问题`udev`，请执行以下步骤：

1. 写入到以下`/usr/sbin/policy-rc.d`并保存所做的更改。
  
   ``` BASH
   #!/bin/sh
   exit 101
   ```
  
2. 添加将执行权限 `/usr/sbin/policy-rc.d`
   ``` BASH
   chmod +x /usr/sbin/policy-rc.d
   ```
  
3. 运行以下命令
   ``` BASH
   dpkg-divert --local --rename --add /sbin/initctl
   ln -s /bin/true /sbin/initctl
   ```
  
### <a name="error-0x80040306-on-installation"></a>"错误：0x80040306"上安装
这都只需这一事实，我们不支持旧版控制台。
若要关闭旧版控制台：

1. 打开 cmd.exe
1. 右键单击标题栏-> 属性-> 取消选中使用传统控制台
1. 单击“确定”

### <a name="error-0x80040154-after-windows-update"></a>"错误：0x80040154"Windows 更新后
Linux 功能的 Windows 子系统可能会禁用在 Windows 更新过程。 如果发生这种情况必须在重新启用 Windows 功能。 有关启用 Windows 子系统，Linux 可查找中的说明[安装指南](https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui https://msdn.microsoft.com/en-us/commandline/wsl/install_guide#enable-the-windows-subsystem-for-linux-feature-gui)。

### <a name="changing-the-display-language"></a>更改显示语言
WSL 安装将尝试自动更改 Ubuntu 区域设置，以便与 Windows 安装程序的区域设置匹配。  如果您不需要此行为可以运行此命令以安装完成后更改 Ubuntu 区域设置。  必须重新启动 bash.exe 此更改才会生效。

下面的示例更改为 EN-US 区域设置：
``` BASH
sudo update-locale LANG=en_US.UTF8
```

### <a name="installation-issues-after-windows-system-restore"></a>Windows 系统还原后的安装问题
1.  删除`%windir%\System32\Tasks\Microsoft\Windows\Windows Subsystem for Linux`文件夹。 <br/>
  **注意：不这样做如果完全安装可选功能和工作正常。**
2.  启用 WSL 可选功能 （如果尚不存在）
3.  重新启动
4.  lxrun / 卸载 / 完整
5.  安装 bash

### <a name="no-internet-access-in-wsl"></a>在 WSL 中没有 internet 访问
某些用户与特定的防火墙应用程序阻止 internet 访问在 WSL 中的报告的问题。  防火墙报告是：

1. Kaspersky
1. AVG
1. Avast

在某些情况下关闭防火墙允许访问。  只需时安装防火墙的某些情况下看起来以阻止访问。

### <a name="permission-denied-error-when-using-ping"></a>使用 ping 时权限被拒绝错误
#### <a name="anniversary-updatehttpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14388-to-windows-10-anniversary-update"></a>[周年更新](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14388-to-windows-10-anniversary-update) 

在 Windows 中的管理员权限才可在 WSL 中运行 ping。  若要运行 ping，以管理员身份，Windows 上运行 Ubuntu 上的 Bash 或 CMD/PowerShell 提示符下使用管理员特权运行 bash.exe。

#### <a name="build-14926httpsmsdnmicrosoftcomen-uscommandlinewslreleasenotesbuild-14926"></a>[生成 14926 +](https://msdn.microsoft.com/en-us/commandline/wsl/release_notes#build-14926)
  不再需要管理员特权。

### <a name="bash-is-hung"></a>挂起 bash
如果同时使用 bash，发现挂起 （或发生死锁） 的 bash 并不响应输入，帮助我们诊断此问题，通过收集和报告的内存转储。 请注意这些步骤将会使系统崩溃。 如果不熟悉，或者执行此操作之前保存工作，则请执行此操作。  <br/>
收集内存转储：
1. 将内存转储类型更改为"完全内存转储"。 更改时转储类型，记下你当前的类型。
2. 使用[步骤](https://blogs.technet.microsoft.com/askpfeplat/2015/04/05/how-to-force-a-diagnostic-memory-dump-when-a-computer-hangs/)配置故障使用键盘控制。
3. 重现挂起或死锁。
4. 使用键序列 (2) 从系统崩溃。
5. 系统将崩溃，并收集内存转储。
6. 系统重启后，报告到 memory.dmp secure@microsoft.com。 转储文件的默认位置是 %SystemRoot%\memory.dmp 或 C:\Windows\memory.dmp c： 是否在系统驱动器。 在电子邮件，请注意，转储用于 WSL 或 Bash Windows 团队。
7. 内存转储类型恢复为原始设置。

### <a name="check-your-build-number"></a>检查内部版本号

若要查找你的电脑的体系结构和 Windows 内部版本号，请打开  
**设置** > **系统** > **有关**

寻找**OS 内部**并**系统类型**字段。  
    ![生成屏幕快照和系统类型的字段](media/system.png) 


若要查找你的 Windows 服务器内部版本号，在 PowerShell 中运行以下命令：  
``` PowerShell
systeminfo | Select-String "^OS Name","^OS Version"
```

### <a name="confirm-wsl-is-enabled"></a>确认启用 WSL
你可以确认，运行以下命令在 PowerShell 中启用适用于 Linux 的 Windows 子系统：  
``` PowerShell
Get-WindowsOptionalFeature -Online -FeatureName Microsoft-Windows-Subsystem-Linux
```

### <a name="openssh-server-connection-issues"></a>OpenSSH 服务器连接问题
尝试连接 SSH 服务器将失败，出现以下错误："连接已关闭的 127.0.0.1 端口 22"。
1. 请确保你的 OpenSSH 服务器正在运行：
   ``` BASH
   sudo service ssh status
   ```
   并已按照本教程中： https://help.ubuntu.com/lts/serverguide/openssh-server.html.en
2. 停止 sshd 服务和在调试模式下启动 sshd:
   ``` BASH
   sudo service ssh stop
   sudo /usr/sbin/sshd -d
   ```
3. 检查启动日志，并确保主机密钥都可用，并且看不到日志消息，例如：
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

如果你看到此类消息，并且密钥由下缺少`/etc/ssh/`，您将需要重新生成密钥，或只是清除并安装 openssh 服务器：
```BASH
sudo apt-get purge openssh-server
sudo apt-get install openssh-server
```

