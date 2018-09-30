---
title: 使用 Azure CLI 管理 Azure 订阅
description: 使用 Azure CLI 管理 Azure 订阅。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.produdct: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 7bffd91fc31452fc745bc572262f10645e4179eb
ms.sourcegitcommit: f7554c00b5d5dca0ec716cbf996eb6654183ec37
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2018
ms.locfileid: "47237589"
---
# <a name="use-multiple-azure-subscriptions"></a><span data-ttu-id="d04a4-103">使用多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="d04a4-103">Use multiple Azure subscriptions</span></span>

<span data-ttu-id="d04a4-104">大多数 Azure 用户永远只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="d04a4-104">Most Azure users will only ever have a single subscription.</span></span> <span data-ttu-id="d04a4-105">但是，如果你在多家组织中工作，或者所在的组织已根据不同的组划分了对特定的资源的访问权限，则你在 Azure 中可能就有多个订阅。</span><span class="sxs-lookup"><span data-stu-id="d04a4-105">However, if you are part of more than one organization or your organization has divided up access to certain resources across groupings, you may have multiple subscriptions within Azure.</span></span> <span data-ttu-id="d04a4-106">CLI 支持全局选择和按命令选择订阅。</span><span class="sxs-lookup"><span data-stu-id="d04a4-106">The CLI supports selecting a subscription both globally and per command.</span></span>

## <a name="tenants-users-and-subscriptions"></a><span data-ttu-id="d04a4-107">租户、用户和订阅</span><span class="sxs-lookup"><span data-stu-id="d04a4-107">Tenants, users, and subscriptions</span></span>

<span data-ttu-id="d04a4-108">在一定程度上，我们可能会对 Azure 中租户、用户和订阅感到混淆，不理解它们的差别。</span><span class="sxs-lookup"><span data-stu-id="d04a4-108">You might have some confusion over the difference between tenants, users, and subscriptions within Azure.</span></span> <span data-ttu-id="d04a4-109">租户是包含整个组织的 Azure Active Directory 实体。</span><span class="sxs-lookup"><span data-stu-id="d04a4-109">A _tenant_ is the Azure Active Directory entity that encompasses a whole organization.</span></span> <span data-ttu-id="d04a4-110">此租户至少包含一个订阅和用户。</span><span class="sxs-lookup"><span data-stu-id="d04a4-110">This tenant has at least one _subscription_ and _user_.</span></span> <span data-ttu-id="d04a4-111">用户是只与一个租户（即所属的组织）关联的个人。</span><span class="sxs-lookup"><span data-stu-id="d04a4-111">A user is an individual and is associated with only one tenant, the organization that they belong to.</span></span> <span data-ttu-id="d04a4-112">用户是登录到 Azure 以创建、管理和使用资源的帐户。</span><span class="sxs-lookup"><span data-stu-id="d04a4-112">Users are those accounts that sign in to Azure to create, manage, and use resources.</span></span>
<span data-ttu-id="d04a4-113">用户可能有权访问多个订阅，这些订阅是与 Microsoft 签署的有关使用云服务（包括 Azure）的协议。</span><span class="sxs-lookup"><span data-stu-id="d04a4-113">A user may have access to multiple _subscriptions_, which are the agreements with Microsoft to use cloud services, including Azure.</span></span> <span data-ttu-id="d04a4-114">每个资源与某个订阅关联。</span><span class="sxs-lookup"><span data-stu-id="d04a4-114">Every resource is associated with a subscription.</span></span>

<span data-ttu-id="d04a4-115">若要详细了解租户、用户与订阅之间的差别，请参阅 [Azure 云术语字典](/azure/azure-glossary-cloud-terminology)。</span><span class="sxs-lookup"><span data-stu-id="d04a4-115">To learn more about the differences between tenants, users, and subscriptions, see the [Azure cloud terminology dictionary](/azure/azure-glossary-cloud-terminology).</span></span>  <span data-ttu-id="d04a4-116">若要了解如何将新订阅添加到 Azure Active Directory 租户，请参阅[如何将 Azure 订阅添加到 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。</span><span class="sxs-lookup"><span data-stu-id="d04a4-116">To learn how to add a new subscription to your Azure Active Directory tenant, see [How to add an Azure subscription to Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory).</span></span>
<span data-ttu-id="d04a4-117">若要了解如何登录到特定租户，请参阅[使用 Azure CLI 登录](/cli/azure/authenticate-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="d04a4-117">To learn how to sign in to a specific tenant, see [Sign in with Azure CLI](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="change-the-active-subscription"></a><span data-ttu-id="d04a4-118">更改活动订阅</span><span class="sxs-lookup"><span data-stu-id="d04a4-118">Change the active subscription</span></span> 

<span data-ttu-id="d04a4-119">若要访问订阅的资源，请切换活动订阅或使用 `--subscription` 参数。</span><span class="sxs-lookup"><span data-stu-id="d04a4-119">To access the resources for a subscription, switch your active subscription or use the `--subscription` argument.</span></span> <span data-ttu-id="d04a4-120">可以使用 [az account set](/cli/azure/account#az-account-set) 来切换用于所有命令的订阅。</span><span class="sxs-lookup"><span data-stu-id="d04a4-120">Switching your subscription for all commands is done with [az account set](/cli/azure/account#az-account-set).</span></span>

<span data-ttu-id="d04a4-121">切换活动订阅：</span><span class="sxs-lookup"><span data-stu-id="d04a4-121">To switch your active subscription:</span></span>

1. <span data-ttu-id="d04a4-122">使用 [az account list](/cli/azure/account#az-account-list) 命令获取订阅列表。</span><span class="sxs-lookup"><span data-stu-id="d04a4-122">Get a list of your subscriptions with the [az account list](/cli/azure/account#az-account-list) command:</span></span>

    ```azurecli-interactive
    az account list --output table
    ```
2. <span data-ttu-id="d04a4-123">结合你要切换到的订阅 ID 或名称使用 `az account set`。</span><span class="sxs-lookup"><span data-stu-id="d04a4-123">Use `az account set` with the subscription ID or name you want to switch to.</span></span>

    ```azurecli-interactive
    az account set --subscription "My Demos"
    ```

<span data-ttu-id="d04a4-124">如果只是结合不同的订阅运行单个命令，请使用 `--subscription` 参数。</span><span class="sxs-lookup"><span data-stu-id="d04a4-124">To run only a single command with a different subscription, use the `--subscription` argument.</span></span> <span data-ttu-id="d04a4-125">此参数使用订阅 ID 或订阅名称：</span><span class="sxs-lookup"><span data-stu-id="d04a4-125">This argument takes either a subscription ID or subscription name:</span></span>

```azurecli-interactive
az vm create --subscription "My Demos" --resource-group MyGroup --name NewVM --image Ubuntu
```
