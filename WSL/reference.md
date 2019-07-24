---
title: 适用于 Linux 的 Windows 子系统命令参考
description: 管理适用于 Linux 的 Windows 子系统的命令列表
keywords: BashOnWindows、bash、wsl、windows、适用于 linux 的 windows 子系统、windowssubsystem、ubuntu
author: scooley
ms.author: scooley
ms.date: 07/31/2017
ms.topic: article
ms.assetid: 82908295-a6bd-483c-a995-613674c2677e
ms.custom: seodec18
ms.openlocfilehash: 465f55f8ba210cd366adc66d433f1873e295136f
ms.sourcegitcommit: ead64b13501d6cb7170adafbb5624f4984a0af16
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/21/2019
ms.locfileid: "67307657"
---
# <a name="command-reference-for-windows-subsystem-for-linux"></a>适用于 Linux 的 Windows 子系统的命令参考

与适用于 Linux 的 Windows 子系统交互的最佳方式是使用`wsl.exe`命令。 

## `wsl.exe` 

下面是在使用 Windows 版本1903时使用`wsl.exe`的所有选项的列表。

* 用于运行 Linux 二进制文件的参数:

    * 如果未提供命令行, wsl 将启动默认 shell。

    * --exec,-e<CommandLine>
        * 执行指定的命令, 而不使用默认的 Linux shell。

    * --
        * 按原样传递剩余的命令行。

* 选项：
    * --分发,-d<Distro>
        * 运行指定的分发。

    * --user,-u<UserName>
        * 以指定用户身份运行。

* 用于管理适用于 Linux 的 Windows 子系统的参数:

    * --export <Distro><FileName>
        * 将分发导出到 tar 文件。
        文件名可以是-标准输出。

    * --import <Distro> <InstallLocation>[Options <FileName> ]
        * 导入指定的 tar 文件作为新的分发。
        文件名可以是-标准输入。

        * 选项：
            * --version <Version>指定要用于新分发的版本。

    * --list,-l [Options]
        * 列出分布。

        * 选项：
            * --all
                * 列出所有分发, 包括当前正在安装或卸载的分发。

            * --正在运行
                * 仅列出当前正在运行的分发。

    * --set-默认值,-s<Distro>
        * 将分布设置为默认值。

    * --set-默认-版本<Version>
        * 更改新分发版的默认安装版本。

    * --set-版本<Distro><Version>
        * 更改指定分发的版本。

    * --terminate,-t<Distro>
        * 终止指定的分发。

    * --取消注册<Distro>
        * 注销分布。

    * --help
        * 显示用法信息。

## <a name="additional-commands"></a>其他命令

还有历史命令可与适用于 Linux 的 Windows 子系统交互。 它们的功能包含在`wsl.exe`中, 但仍可供使用。 

### `wslconfig.exe`

此命令可让你配置 WSL 分布。 下面是其选项的列表。

* /l,/list [选项]
    * 列出已注册的分发。
        * /all-(可选) 列出所有分发, 包括当前正在安装或卸载的分发。

        * /running-仅列出当前正在运行的分发。

* /s、/setdefault<DistributionName>
    * 将分布设置为默认值。

* /t、/terminate<DistributionName>
    * 终止分布。

* /u,/unregister<DistributionName>
    * 注销分布。

### `bash.exe`

此命令用于启动 bash shell。 下面是可用于此命令的选项。

* 未给定选项
    * 在当前目录中启动 Bash shell。 如果未自动安装 Bash shell, 则运行`lxrun /install`

* bash ~
    * 在用户的主目录中启动 bash shell。  类似于运行`cd ~`。

* bash-c "&lt;command&gt;"
    * 运行命令, 打印输出并退出到 Windows 命令提示符。 <br/> <br/> 实例`bash -c "ls"`

## <a name="deprecated-commands"></a>弃用的命令

`lxrun.exe`是用于安装和管理适用于 Linux 的 Windows 子系统的第一个命令。 它在 Windows 10 1803 和更高版本中已弃用。

命令`lxrun.exe`可用于直接与适用于 Linux 的[Windows 子系统 (WSL)](https://msdn.microsoft.com/en-us/commandline/wsl/faq#what-windows-subsystem-for-linux-wsl-)交互。  这些命令安装`\Windows\System32`在目录中, 可以在 Windows 命令提示符下或在 PowerShell 中运行。

| Command                     | 描述                     |
|:----------------------------|:---------------------------|
| `lxrun`                     | Lxrun 命令用于管理 WSL 实例。 |
| `lxrun /install`            | 开始下载和安装过程。 <br/> 可以添加 **/y**来绕过所有提示。  系统会自动接受确认提示, 并将 "默认用户" 设置为 "root"。          |
| `lxrun /uninstall`          | 卸载并删除 Ubuntu 映像。  默认情况下, 这不会删除用户的 Ubuntu 主目录。 <br/> 可以添加 **/y**来自动接受确认提示 <br/>**/full**卸载并删除用户的 Ubuntu 主目录         |
| `lxrun /setdefaultuser <userName>`     | 设置 Ubuntu 用户上的默认 Bash。 如果指定的用户不存在, 将提示输入密码。  有关详细信息, 请 https://aka.ms/wslusers 访问:。 <br/> **/y**绕过密码的 promping。  将创建不带密码的用户。|
| `lxrun /update`            | 更新子系统的包索引          |
