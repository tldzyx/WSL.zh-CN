---
title: 适用于 Linux 的企业的 Windows 子系统
description: 资源和如何最的说明使用适用于 Linux Windows 子系统在企业环境中。
keywords: BashOnWindows，bash、 wsl、 windows、 linux、 windowssubsystem、 ubuntu、 debian、 suse、 windows 10、 企业、 部署、 脱机、 打包、 存储、 分发、 安装，适用于 windows 子系统安装
author: mscraigloewen
ms.author: mscraigloewen
ms.date: 09/04/2018
ms.topic: article
ms.assetid: 7afaeacf-435a-4e58-bff0-a9f0d75b8a51
ms.custom: seodec18
ms.openlocfilehash: 9d867654d1b66fc14b58bc5e111986a7d38ef79c
ms.sourcegitcommit: ca08a78925880ed3eccf88edb30def16c83f2543
ms.translationtype: MT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2019
ms.locfileid: "59063275"
---
# <a name="windows-subsystem-for-linux-for-enterprise"></a><span data-ttu-id="7df90-104">适用于 Linux 的企业的 Windows 子系统</span><span class="sxs-lookup"><span data-stu-id="7df90-104">Windows Subsystem for Linux for Enterprise</span></span>

<span data-ttu-id="7df90-105">Microsoft Store for Business 到想要将 WSL 部署到其公司的企业提供了各种各样的解决方案。</span><span class="sxs-lookup"><span data-stu-id="7df90-105">The Microsoft Store for Business offers a variety of solutions to Enterprises who want to deploy WSL to their company.</span></span> <span data-ttu-id="7df90-106">[联机文档](https://docs.microsoft.com/en-us/microsoft-store/)为业务 Microsoft Store 是一个不错的资源，若要了解有关存储体验的常规信息。</span><span class="sxs-lookup"><span data-stu-id="7df90-106">The [online docs](https://docs.microsoft.com/en-us/microsoft-store/) for the Microsoft Store for Business are a great resource to find out general information about the Store experience.</span></span>

<span data-ttu-id="7df90-107">如果您只想要获取或设置的公司注册要开始部署 WSL 可以遵循这些步骤中，在 Microsoft Store docs 部分将进行介绍：</span><span class="sxs-lookup"><span data-stu-id="7df90-107">If you’re a company that’s just looking to get set up to start deploying WSL you can follow these steps, which are explained inside of the Microsoft Store docs:</span></span>

* [<span data-ttu-id="7df90-108">注册 Microsoft Store for Business 并开始</span><span class="sxs-lookup"><span data-stu-id="7df90-108">Sign up for the Microsoft Store for Business and get started</span></span>](https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business-overview)
* <span data-ttu-id="7df90-109">[管理您的产品和服务 （包括谁可以访问哪些应用在专用应用商店中的）](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview)。</span><span class="sxs-lookup"><span data-stu-id="7df90-109">[Manage your products and services (including who can access which apps in your private store)](https://docs.microsoft.com/en-us/microsoft-store/manage-apps-microsoft-store-for-business-overview).</span></span> <span data-ttu-id="7df90-110">可以在此处添加 WSL 发行版应用商店和控制可以安装它们</span><span class="sxs-lookup"><span data-stu-id="7df90-110">Here you can add WSL distros to your store and control who can install them</span></span>
* [<span data-ttu-id="7df90-111">使用所选的分发方法来将软件部署到你的公司</span><span class="sxs-lookup"><span data-stu-id="7df90-111">Use a distribution method of your choice to deploy the software to your company</span></span>](https://docs.microsoft.com/en-us/microsoft-store/distribute-apps-to-your-employees-microsoft-store-for-business)
* <span data-ttu-id="7df90-112">向用户有权 WSL 发行版，他们可以传达[使用以下步骤](https://docs.microsoft.com/en-us/windows/wsl/install-win10)安装发行版或所选的发行版</span><span class="sxs-lookup"><span data-stu-id="7df90-112">Communicate to users who have access to WSL distros that they can [use these steps](https://docs.microsoft.com/en-us/windows/wsl/install-win10) to install the distro or distros of their choice</span></span> 

## <a name="how-to-distribute-a-distro-offline"></a><span data-ttu-id="7df90-113">如何分发的发行版，脱机</span><span class="sxs-lookup"><span data-stu-id="7df90-113">How to Distribute a Distro Offline</span></span>

<span data-ttu-id="7df90-114">如果你的公司中的计算机没有到 Microsoft Store 或 Microsoft Store for Business 的访问，您可以下载具有脱机许可证通过执行以下步骤的 Linux 发行版的安装程序。</span><span class="sxs-lookup"><span data-stu-id="7df90-114">If the computers in your company don’t have access to the Microsoft Store or the Microsoft Store for Business, then you can download the installer of a Linux distro that has an offline license by following these steps.</span></span> 

### <a name="set-up-an-azure-active-directory-ad-account"></a><span data-ttu-id="7df90-115">设置 Azure Active Directory (AD) 帐户</span><span class="sxs-lookup"><span data-stu-id="7df90-115">Set up an Azure Active Directory (AD) Account</span></span> 

<span data-ttu-id="7df90-116">您需要具有 Azure AD 帐户并且是为你的组织的全局管理员以获取安装的 Microsoft Store 应用程序。</span><span class="sxs-lookup"><span data-stu-id="7df90-116">You need to have an Azure AD account and be the global administrator for your organization to get the installer of Microsoft Store apps.</span></span> <span data-ttu-id="7df90-117">如果已有帐户，则可以跳过此步骤。</span><span class="sxs-lookup"><span data-stu-id="7df90-117">If you already have an account, you can skip this step.</span></span>

<span data-ttu-id="7df90-118">若要注册一个帐户的说明可在此处找到： https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span><span class="sxs-lookup"><span data-stu-id="7df90-118">The instructions to register an account can be found here: https://docs.microsoft.com/en-us/microsoft-store/sign-up-microsoft-store-for-business</span></span>

### <a name="sign-into-the-store-for-business-and-go-to-the-homepage"></a><span data-ttu-id="7df90-119">适用于企业登录到应用商店，并转到主页</span><span class="sxs-lookup"><span data-stu-id="7df90-119">Sign into the Store for Business and go to the homepage</span></span>
<span data-ttu-id="7df90-120">在此处登录： www.microsoft.com/business-store</span><span class="sxs-lookup"><span data-stu-id="7df90-120">Sign in here: www.microsoft.com/business-store</span></span>

![MS 应用商店的公司主页](media/offlineinstallscreens/1-screen.png)

### <a name="go-to-manage-settings-and-enable-show-offline-apps"></a><span data-ttu-id="7df90-122">转到管理-> 设置并启用显示脱机应用</span><span class="sxs-lookup"><span data-stu-id="7df90-122">Go to Manage->Settings and enable 'Show offline apps'</span></span>

![For business 设置页面的 MS 应用商店](media/offlineinstallscreens/2-screen.png)

### <a name="go-back-to-the-main-page-by-clicking-shop-for-my-group"></a><span data-ttu-id="7df90-124">请返回到主页，通过单击购买我的组</span><span class="sxs-lookup"><span data-stu-id="7df90-124">Go back to the main page by clicking 'Shop for my group'</span></span>

![MS 应用商店的公司主页](media/offlineinstallscreens/1-screen.png)

### <a name="search-for-your-desired-distro-and-select-it"></a><span data-ttu-id="7df90-126">搜索你所需的发行版并选择它</span><span class="sxs-lookup"><span data-stu-id="7df90-126">Search for your desired distro and select it</span></span>

![适用于业务活动搜索与主页上的 MS 应用商店](media/offlineinstallscreens/3-screen.png)

### <a name="select-an-offline-license-in-the-license-type-dropdown-menu-and-click-get-the-app"></a><span data-ttu-id="7df90-128">在许可证类型下拉列表菜单中选择脱机许可证，然后单击获取应用</span><span class="sxs-lookup"><span data-stu-id="7df90-128">Select an ‘Offline’ license in the License type dropdown menu and click ‘Get the app’</span></span>

![MS 应用商店的业务 Ubuntu 产品页](media/offlineinstallscreens/4-screen.png)

<span data-ttu-id="7df90-130">请注意： 某些发行版可能选择不具有脱机许可证</span><span class="sxs-lookup"><span data-stu-id="7df90-130">Please note: some distros may elect not to have an offline license</span></span>

### <a name="click-the-manage-button-to-get-to-the-apps-product-page"></a><span data-ttu-id="7df90-131">单击管理按钮，转到应用程序的产品页面</span><span class="sxs-lookup"><span data-stu-id="7df90-131">Click the ‘Manage’ button to get to the app’s product page</span></span>

![MS 应用商店的业务 Ubuntu 产品页](media/offlineinstallscreens/5-screen.png)

### <a name="select-your-architecture-and-download-the-package-for-offline-use"></a><span data-ttu-id="7df90-133">选择您的体系结构并下载离线使用的包</span><span class="sxs-lookup"><span data-stu-id="7df90-133">Select your architecture and download the package for offline use</span></span>

![适用于业务 Ubuntu 产品详细信息页的 MS 应用商店](media/offlineinstallscreens/6-screen.png)

<span data-ttu-id="7df90-135">然后，此安装程序都可以分发到你想要安装 WSL 的任何计算机。</span><span class="sxs-lookup"><span data-stu-id="7df90-135">This installer can then be distributed to any computer where you would like to install WSL.</span></span>