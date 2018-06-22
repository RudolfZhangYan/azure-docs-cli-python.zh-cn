---
title: 使用 Azure CLI 管理 Azure 订阅
description: 使用 Azure CLI 管理 Azure 订阅。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/15/2018
ms.topic: conceptual
ms.produdct: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.service: active-directory
ms.openlocfilehash: fdc8ffca38a6a581ae63b0518df72f6e09110d07
ms.sourcegitcommit: 1a38729d6ae93c49137b3d49b6a9ec8a75eff190
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36262703"
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="1a2e2-103">管理多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="1a2e2-103">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="1a2e2-104">大多数 Azure 用户永远只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="1a2e2-105">但是，如果你在多家组织中工作，或者所在的组织已根据不同的组划分了对特定的资源的访问权限，则你在 Azure 中可能就有多个订阅。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-105">However, if you are part of multiple organizations or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="1a2e2-106">可以使用 CLI 轻松管理多个订阅，只需为所有命令设置全局订阅或为每个命令选择一个订阅即可。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-106">Multiple subscriptions can be easily managed with the CLI either by setting a global subscription for all commands, or selecting a subscription on a per-command basis.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="1a2e2-107">租户、用户和订阅</span><span class="sxs-lookup"><span data-stu-id="1a2e2-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="1a2e2-108">在一定程度上，我们可能会对 Azure 中租户、用户和订阅感到混淆，不理解它们的差别。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="1a2e2-109">租户是包含整个组织的 Azure Active Directory 实体。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-109">A _tenant_ is the Azure Active Directory entity which encompasses a whole organization.</span></span> <span data-ttu-id="1a2e2-110">此租户至少包含一个订阅和用户。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="1a2e2-111">用户是只与一个租户（即所属的组织）关联的个人。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="1a2e2-112">用户是登录到 Azure 以预配和使用资源的帐户。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-112">Users are those accounts which log in to Azure to provision and use resources.</span></span>
<span data-ttu-id="1a2e2-113">用户可能有权访问多个订阅，这些订阅是与 Microsoft 签署的有关使用云服务（包括 Azure）的协议。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="1a2e2-114">每个资源与某个订阅关联。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="1a2e2-115">若要详细了解租户、用户与订阅之间的差别，请参阅 [Azure 云术语字典](/azure/azure-glossary-cloud-terminology)。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="1a2e2-116">若要了解如何将新订阅添加到 Azure Active Directory 租户，请参阅[如何将 Azure 订阅添加到 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="1a2e2-117">使用多个租户时，可能需要登录到特定租户。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-117">When working with multiple tenants, you may need to sign in to a specific tenant.</span></span> <span data-ttu-id="1a2e2-118">为此，请参阅[使用 Azure CLI 登录](/cli/azure/authenticate-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-118">To do this, see [Sign in with Azure CLI](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="work-with-multiple-subscriptions"></a><span data-ttu-id="1a2e2-119">使用多个订阅</span><span class="sxs-lookup"><span data-stu-id="1a2e2-119">Work with multiple subscriptions</span></span>

<span data-ttu-id="1a2e2-120">若要访问订阅中包含的资源，需要切换活动的订阅。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-120">To access the resources contained within a subscription, you need to switch your active subscription.</span></span> <span data-ttu-id="1a2e2-121">可以使用 [az account set](/cli/azure/account#az-account-set) 为所有 Azure CLI 命令切换订阅，也可以使用 `--subscription` 参数为单个命令这样做。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-121">Switching your subscription can be done for all Azure CLI commands with [az account set](/cli/azure/account#az-account-set), or done on a per-command basis by using the `--subscription` argument.</span></span>

<span data-ttu-id="1a2e2-122">需提供可用订阅的列表才能开始操作。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-122">To start, you will need a list of your available subscriptions.</span></span> <span data-ttu-id="1a2e2-123">若要获取该列表，请使用 [az account list](/cli/azure/account#az-account-list) 命令：</span><span class="sxs-lookup"><span data-stu-id="1a2e2-123">To get it, use the [az account list](/cli/azure/account#az-account-list) command:</span></span>

```azurecli-interactive
az account list --output table
```

<span data-ttu-id="1a2e2-124">若要以全局方式更改活动订阅，请使用 `az account set` 和订阅 ID 或订阅名称：</span><span class="sxs-lookup"><span data-stu-id="1a2e2-124">To change the active subscription globally, use `az account set` along with either the subscription ID or subscription name:</span></span>

```azurecli-interactive
az account set --subscription "My Demos"
```

<span data-ttu-id="1a2e2-125">若要对某个命令使用特定的订阅，请直接使用 `--subscription` 参数。</span><span class="sxs-lookup"><span data-stu-id="1a2e2-125">To use a specific subscription for a command, just use the `--subscription` argument.</span></span> <span data-ttu-id="1a2e2-126">此参数使用订阅 ID 或订阅名称：</span><span class="sxs-lookup"><span data-stu-id="1a2e2-126">This argument takes either a subscription ID or subscription name:</span></span>

```azurecli-interactive
az vm create --subscription "My Demos" --resource-group MyGroup --name NewVM --image Ubuntu
```
