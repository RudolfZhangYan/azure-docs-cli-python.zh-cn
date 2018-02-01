---
title: "使用 Azure CLI 2.0 管理 Azure 订阅"
description: "在 Linux、Mac 或 Windows 上使用 Azure CLI 2.0 管理 Azure 订阅。"
keywords: "Azure CLI 2.0, Linux, Mac, Windows, OS X, 订阅"
author: kamaljit
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: 0f453ad1bff621250c8aa3147b5f5e916e712e30
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2018
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="79c3f-104">管理多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="79c3f-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="79c3f-105">大多数 Azure 用户永远只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="79c3f-105">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="79c3f-106">但是，如果你在多家组织中工作，或者所在的组织已根据不同的组划分了对特定的资源的访问权限，则你在 Azure 中可能就有多个订阅。</span><span class="sxs-lookup"><span data-stu-id="79c3f-106">However, if you are part of multiple organizations or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="79c3f-107">可以使用 CLI 轻松管理多个订阅，并通过选择订阅执行操作。</span><span class="sxs-lookup"><span data-stu-id="79c3f-107">Multiple subscriptions can be easily managed with the CLI, and operations can be performed by selecting a subscription.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="79c3f-108">租户、用户和订阅</span><span class="sxs-lookup"><span data-stu-id="79c3f-108">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="79c3f-109">在一定程度上，我们可能会对 Azure 中租户、用户和订阅感到混淆，不理解它们的差别。</span><span class="sxs-lookup"><span data-stu-id="79c3f-109">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="79c3f-110">一般而言，租户是包含整个组织的 Azure Active Directory 实体。</span><span class="sxs-lookup"><span data-stu-id="79c3f-110">In general, a _tenant_ is the Azure Active Directory entity which encompasses a whole organization.</span></span> <span data-ttu-id="79c3f-111">此租户至少包含一个订阅和用户。</span><span class="sxs-lookup"><span data-stu-id="79c3f-111">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="79c3f-112">用户是只与一个租户（即所属的组织）关联的个人。</span><span class="sxs-lookup"><span data-stu-id="79c3f-112">A user is an individual, and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="79c3f-113">用户是登录到 Azure 以预配和使用资源的帐户。</span><span class="sxs-lookup"><span data-stu-id="79c3f-113">Users are those accounts which log in to Azure to provision and use resources.</span></span> <span data-ttu-id="79c3f-114">用户可能有权访问多个订阅，这些订阅是与 Microsoft 签署的有关使用云服务（包括 Azure）的协议。</span><span class="sxs-lookup"><span data-stu-id="79c3f-114">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="79c3f-115">每个资源与某个订阅关联。</span><span class="sxs-lookup"><span data-stu-id="79c3f-115">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="79c3f-116">若要详细了解租户、用户与订阅之间的差别，请参阅 [Azure 云术语字典](/azure/azure-glossary-cloud-terminology)。</span><span class="sxs-lookup"><span data-stu-id="79c3f-116">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>
<span data-ttu-id="79c3f-117">若要了解如何将新订阅添加到 Azure Active Directory 租户，请参阅[如何将 Azure 订阅添加到 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。</span><span class="sxs-lookup"><span data-stu-id="79c3f-117">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>

## <a name="working-with-multiple-subscriptions"></a><span data-ttu-id="79c3f-118">使用多个订阅</span><span class="sxs-lookup"><span data-stu-id="79c3f-118">Working with multiple subscriptions</span></span>

<span data-ttu-id="79c3f-119">若要访问订阅中包含的资源，需要切换活动的订阅。</span><span class="sxs-lookup"><span data-stu-id="79c3f-119">To access the resources contained within a subscription, you need to switch your active subscription.</span></span> <span data-ttu-id="79c3f-120">针对订阅执行的所有操作将会参考订阅代表的服务协议（而不是个人帐户），通过 `az account` 命令完成。</span><span class="sxs-lookup"><span data-stu-id="79c3f-120">All work with subscriptions is done through the `az account` command, which refers to the service agreement that a subscription represents and not your individual account.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

<span data-ttu-id="79c3f-121">若要开始使用可用的订阅，请获取帐户中提供的订阅列表：</span><span class="sxs-lookup"><span data-stu-id="79c3f-121">To start working with your available subscriptions, get a list of those available in your account:</span></span>

```azurecli-interactive
az account list --output table
```

```Output
Name                                         CloudName    SubscriptionId                        State     IsDefault
-------------------------------------------  -----------  ------------------------------------  --------  -----------
My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
```

<span data-ttu-id="79c3f-122">若要更改活动的订阅，可以使用 `az account set`：</span><span class="sxs-lookup"><span data-stu-id="79c3f-122">In order to change the active subscription, you can use `az account set`:</span></span>

```azurecli-interactive
az account set --subscription "My Demos"
```

<span data-ttu-id="79c3f-123">可以使用订阅 ID 或订阅名称来选择订阅。</span><span class="sxs-lookup"><span data-stu-id="79c3f-123">You can use either the subscription ID or the subscription name to select the subscription.</span></span>
