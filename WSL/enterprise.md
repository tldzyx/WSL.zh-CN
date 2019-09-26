---
title: 适用于 Linux for Enterprise 的 Windows 子系统
description: 有关如何在企业环境中最好地使用适用于 Linux 的 Windows 子系统的资源和说明。
keywords: BashOnWindows，bash，wsl，windows，适用于 linux 的 windows 子系统，windowssubsystem，ubuntu，debian，suse，windows 10，企业，部署，脱机，打包，存储，分发，安装，安装
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: c32d62267c77d87fb200cfe43b8e6f43b4e3a56d
ms.sourcegitcommit: 0b5a9f8982dfff07fc8df32d74d97293654f8e12
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2019
ms.locfileid: "71269863"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>适用于 Linux for Enterprise 的 Windows 子系统

适用于企业的 Microsoft Store 为希望向其公司部署 WSL 的企业提供各种解决方案。 适用于企业的 Microsoft Store 的[联机文档](https://docs.microsoft.com/en-us/microsoft-store/)是一种很好的资源，用于找出有关应用商店体验的一般信息。

如果你是一家公司，该公司只是想要开始部署 WSL，你可以执行以下步骤，这些步骤将在 Microsoft Store 文档中进行说明：

* [注册企业 Microsoft Store 和入门](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [管理你的产品和服务（包括谁可以访问你的专用商店中的应用）](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。 可在此处将 WSL 发行版添加到你的应用商店，并控制哪些用户可以安装它们
* [使用所选的分发方法将软件部署到公司](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* 与有权访问 WSL 发行版的用户通信，他们可以[使用这些步骤](https://docs.microsoft.com/en-us/windows/wsl/install-win10)安装其所选的发行版或发行版 

## <a name="how-to-distribute-a-distro-offline"></a>如何脱机分发发行版

如果公司中的计算机无权访问 Microsoft Store 或企业 Microsoft Store，则可以按照以下步骤下载具有脱机许可证的 Linux 发行版的安装程序。 

### <a name="set-up-an-azure-active-directory-ad-account"></a>设置 Azure Active Directory （AD）帐户 

你需要拥有 Azure AD 帐户，并是组织的全局管理员才能获取 Microsoft Store 应用程序的安装程序。 如果你已有帐户，则可以跳过此步骤。

可在此处找到注册帐户的说明： https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>登录到企业的应用商店并访问主页
在此处登录： www.microsoft.com/business-store

![适用于企业的 MS Store 主页](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>请参阅管理-> 设置并启用 "显示脱机应用"

![适用于企业的 MS Store 设置页](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>单击 "购买我的组"，返回到主页

![适用于企业的 MS Store 主页](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>搜索所需的发行版并选择它

![具有活动搜索的适用于企业的 MS Store 主页页](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>在 "许可证类型" 下拉菜单中选择 "脱机" 许可证，然后单击 "获取应用程序"

![适用于企业的 MICROSOFT 应用 Ubuntu 产品页](media/offlineinstallscreens/4-screen.png)

请注意：某些发行版可能选择不具有脱机许可证

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>单击 "管理" 按钮转到应用的 "产品" 页

![适用于企业的 MICROSOFT 应用 Ubuntu 产品页](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>选择你的体系结构并下载供脱机使用的包

![适用于企业的 MICROSOFT 应用 Ubuntu 产品详细信息页](media/offlineinstallscreens/6-screen.png)

然后，可以将此安装程序分发到你想要在其中安装 WSL 的任何计算机。