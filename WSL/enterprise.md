---
title: 适用于 Linux for Enterprise 的 Windows 子系统
description: 资源和如何最的说明使用适用于 Linux Windows 子系统在企业环境中。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10、 企业、 部署、 脱机、 打包、 存储、 分发、 安装，适用于 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ae0956bc0543b1c45765f3620ce9a55c9afe55da
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/18/2019
ms.locfileid: "59063275"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a>适用于 Linux for Enterprise 的 Windows 子系统

Microsoft Store for Business 到想要将 WSL 部署到其公司的企业提供了各种各样的解决方案。 [联机文档](https://docs.microsoft.com/en-us/microsoft-store/)为业务 Microsoft Store 是一个不错的资源，若要了解有关存储体验的常规信息。

如果您只想要获取或设置的公司注册要开始部署 WSL 可以遵循这些步骤中，在 Microsoft Store docs 部分将进行介绍：

* [注册 Microsoft Store for Business 并开始](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* [管理您的产品和服务 （包括谁可以访问哪些应用在专用应用商店中的）](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。 可以在此处添加 WSL 发行版应用商店和控制可以安装它们
* [使用所选的分发方法来将软件部署到你的公司](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* 向用户有权 WSL 发行版，他们可以传达[使用以下步骤](https://docs.microsoft.com/en-us/windows/wsl/install-win10)安装发行版或所选的发行版 

## <a name="how-to-distribute-a-distro-offline"></a>如何分发的发行版，脱机

如果你的公司中的计算机没有到 Microsoft Store 或 Microsoft Store for Business 的访问，您可以下载具有脱机许可证通过执行以下步骤的 Linux 发行版的安装程序。 

### <a name="set-up-an-azure-active-directory-ad-account"></a>设置 Azure Active Directory (AD) 帐户 

您需要具有 Azure AD 帐户并且是为你的组织的全局管理员以获取安装的 Microsoft Store 应用程序。 如果已有帐户，则可以跳过此步骤。

若要注册一个帐户的说明可在此处找到： https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a>适用于企业登录到应用商店，并转到主页
在此处登录： www.microsoft.com/business-store

![MS 应用商店的公司主页](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a>转到管理-> 设置并启用显示脱机应用

![For business 设置页面的 MS 应用商店](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a>请返回到主页，通过单击购买我的组

![MS 应用商店的公司主页](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a>搜索你所需的发行版并选择它

![适用于业务活动搜索与主页上的 MS 应用商店](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a>在许可证类型下拉列表菜单中选择脱机许可证，然后单击获取应用

![MS 应用商店的业务 Ubuntu 产品页](media/offlineinstallscreens/4-screen.png)

请注意： 某些发行版可能选择不具有脱机许可证

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a>单击管理按钮，转到应用程序的产品页面

![MS 应用商店的业务 Ubuntu 产品页](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a>选择您的体系结构并下载离线使用的包

![适用于业务 Ubuntu 产品详细信息页的 MS 应用商店](media/offlineinstallscreens/6-screen.png)

然后，此安装程序都可以分发到你想要安装 WSL 的任何计算机。