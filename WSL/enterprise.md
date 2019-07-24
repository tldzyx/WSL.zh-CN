---
title: 适用于 Linux for Enterprise 的 Windows 子系统
description: 有关如何在企业环境中最好地使用适用于 Linux 的 Windows 子系统的资源和说明。
keywords: BashOnWindows, bash, wsl, windows, 适用于 linux 的 windows 子系统, windowssubsystem, ubuntu, debian, suse, windows 10, 企业, 部署, 脱机, 打包, 存储, 分发, 安装, 安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: cd239efc5c7c25ffbe5de25b2438d44181a838a9
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/14/2019
ms.locfileid: "59063275"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="e7d9e-104">适用于 Linux for Enterprise 的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="e7d9e-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="e7d9e-105">适用于企业的 Microsoft Store 为希望向其公司部署 WSL 的企业提供各种解决方案。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="e7d9e-106">适用于企业的 Microsoft Store 的[联机文档](https://docs.microsoft.com/en-us/microsoft-store/)是一种很好的资源, 用于找出有关应用商店体验的一般信息。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="e7d9e-107">如果你是一家公司, 该公司只是想要开始部署 WSL, 你可以执行以下步骤, 这些步骤将在 Microsoft Store 文档中进行说明:</span><span class="sxs-lookup"><span data-stu-id="e7d9e-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="e7d9e-108">注册企业 Microsoft Store 和入门</span><span class="sxs-lookup"><span data-stu-id="e7d9e-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="e7d9e-109">[管理你的产品和服务 (包括谁可以访问你的专用商店中的应用)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="e7d9e-110">可在此处将 WSL 发行版添加到你的应用商店, 并控制哪些用户可以安装它们</span><span class="sxs-lookup"><span data-stu-id="e7d9e-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="e7d9e-111">使用所选的分发方法将软件部署到公司</span><span class="sxs-lookup"><span data-stu-id="e7d9e-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="e7d9e-112">与有权访问 WSL 发行版的用户通信, 他们可以[使用这些步骤](https://docs.microsoft.com/en-us/windows/wsl/install-win10)安装其所选的发行版或发行版</span><span class="sxs-lookup"><span data-stu-id="e7d9e-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="e7d9e-113">如何脱机分发发行版</span><span class="sxs-lookup"><span data-stu-id="e7d9e-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="e7d9e-114">如果公司中的计算机无权访问 Microsoft Store 或企业 Microsoft Store, 则可以按照以下步骤下载具有脱机许可证的 Linux 发行版的安装程序。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="e7d9e-115">设置 Azure Active Directory (AD) 帐户</span><span class="sxs-lookup"><span data-stu-id="e7d9e-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="e7d9e-116">你需要拥有 Azure AD 帐户, 并是组织的全局管理员才能获取 Microsoft Store 应用程序的安装程序。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="e7d9e-117">如果你已有帐户, 则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="e7d9e-118">可在此处找到注册帐户的说明: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="e7d9e-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="e7d9e-119">登录到企业的应用商店并访问主页</span><span class="sxs-lookup"><span data-stu-id="e7d9e-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="e7d9e-120">在此处登录: www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="e7d9e-120">Sign in here: www.microsoft.com/business-store</span></span>

![适用于企业的 MS Store 主页](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="e7d9e-122">请参阅管理-> 设置并启用 "显示脱机应用"</span><span class="sxs-lookup"><span data-stu-id="e7d9e-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![适用于企业的 MS Store 设置页](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="e7d9e-124">单击 "购买我的组", 返回到主页</span><span class="sxs-lookup"><span data-stu-id="e7d9e-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![适用于企业的 MS Store 主页](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="e7d9e-126">搜索所需的发行版并选择它</span><span class="sxs-lookup"><span data-stu-id="e7d9e-126">Search for your desired distro and select it</span></span>

![具有活动搜索的适用于企业的 MS Store 主页页](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="e7d9e-128">在 "许可证类型" 下拉菜单中选择 "脱机" 许可证, 然后单击 "获取应用程序"</span><span class="sxs-lookup"><span data-stu-id="e7d9e-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![适用于企业的 MICROSOFT 应用 Ubuntu 产品页](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="e7d9e-130">请注意: 某些发行版可能选择不具有脱机许可证</span><span class="sxs-lookup"><span data-stu-id="e7d9e-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="e7d9e-131">单击 "管理" 按钮转到应用的 "产品" 页</span><span class="sxs-lookup"><span data-stu-id="e7d9e-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![适用于企业的 MICROSOFT 应用 Ubuntu 产品页](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="e7d9e-133">选择你的体系结构并下载供脱机使用的包</span><span class="sxs-lookup"><span data-stu-id="e7d9e-133">Select your architecture and download the package for offline use</span></span>

![适用于企业的 MICROSOFT 应用 Ubuntu 产品详细信息页](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="e7d9e-135">然后, 可以将此安装程序分发到你想要在其中安装 WSL 的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="e7d9e-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>