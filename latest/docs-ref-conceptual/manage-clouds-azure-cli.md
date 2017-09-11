---
title: "使用 Azure CLI 2.0 管理多个云"
description: "使用 Azure CLI 2.0 创建、登录和管理不同的云。"
keywords: "Azure CLI 2.0, Azure, 云, 数据中心, 政府, 区域, 中国, 德国"
author: sptramer
manager: douge
ms.author: sttramer
ms.date: 06/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: 0222b7339e46346ef6c7e9ad98616d9b71129942
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="0a0b2-104">使用 Azure CLI 2.0 管理多个云</span><span class="sxs-lookup"><span data-stu-id="0a0b2-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="0a0b2-105">如果有多个订阅与 Azure 关联，则可以获得多个可用的云。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-105">If you have multiple subscriptions associated with Azure, you may have more than one cloud available.</span></span> <span data-ttu-id="0a0b2-106">每个云有自身的关联终结点和功能，并且通常与具有不同数据保护标准或要求的特定区域相关联。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-106">Each cloud has its own associated endpoints and capabilities, and is often associated with a particular region that has different data protection standards or requirements.</span></span>

<span data-ttu-id="0a0b2-107">若要有效使用多个云，需要能够切换当前处于活动状态的云，并且可能需要创建新云。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-107">To effectively work with multiple clouds, you will need to be able to switch between which is currently active, and possibly create new clouds.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="0a0b2-108">列出云</span><span class="sxs-lookup"><span data-stu-id="0a0b2-108">Listing clouds</span></span>

<span data-ttu-id="0a0b2-109">可以使用 [cloud list](/cli/azure/cloud#list) 命令列出可用的云。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-109">You may list your available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="0a0b2-110">此命令会告知当前哪个云处于活动状态及其当前配置文件是什么，并可提供有关区域后缀和主机名的信息。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-110">This will tell you which cloud is currently active, what its current profile is, and can provide information on regional suffixes and host names.</span></span>

<span data-ttu-id="0a0b2-111">获取可用云以及当前处于活动状态的云的列表：</span><span class="sxs-lookup"><span data-stu-id="0a0b2-111">To get a list of the available clouds and the currently active one:</span></span>

```azurecli
az cloud list --output table
```

```output
IsActive    Name               Profile
----------  -----------------  ---------
True        AzureCloud         latest
            AzureChinaCloud    latest
            AzureUSGovernment  latest
            AzureGermanCloud   latest
```

## <a name="switching-the-active-cloud"></a><span data-ttu-id="0a0b2-112">切换活动的云</span><span class="sxs-lookup"><span data-stu-id="0a0b2-112">Switching the active cloud</span></span>

<span data-ttu-id="0a0b2-113">若要切换当前处于活动状态的云，请运行 [cloud set](/cli/azure/cloud#set) 命令。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-113">In order to switch the currently active cloud, you run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="0a0b2-114">此命令采用一个必需参数，即云的名称。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-114">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="0a0b2-115">如果从未针对活动的云执行过身份验证，则需要先执行身份验证，然后才能执行其他任何 CLI 操作。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-115">If you have never authenticated for the active cloud, you will need to do so before performing any other CLI operations.</span></span> <span data-ttu-id="0a0b2-116">有关身份验证的说明，请参阅[使用 Azure CLI 2.0 登录](/cli/azure/authenticate-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-116">For instructions on authenticating, see [Log in with Azure CLI 2.0](/cli/azure/authenticate-azure-cli).</span></span>

## <a name="register-or-unregister-a-cloud"></a><span data-ttu-id="0a0b2-117">注册或注销云</span><span class="sxs-lookup"><span data-stu-id="0a0b2-117">Register or unregister a cloud</span></span>

<span data-ttu-id="0a0b2-118">如果有自己的终结点或需要不同的配置文件，请注册新云。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-118">Register a new cloud if you have your own endpoints or require a different profile.</span></span> <span data-ttu-id="0a0b2-119">可以使用 [cloud register](/cli/azure/cloud#register) 命令创建云。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-119">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="0a0b2-120">此命令需要一个名称，有时还需要一组功能和终结点指定值。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-120">This command requires a name, and optionally a set of capabilities and endpoint designations.</span></span>

<span data-ttu-id="0a0b2-121">使用特定的配置文件为资源管理器创建包含专用终结点的云：</span><span class="sxs-lookup"><span data-stu-id="0a0b2-121">To create a cloud with a specialized endpoint for the resource manager, with a specific profile:</span></span>

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

<span data-ttu-id="0a0b2-122">这会创建云，但不会自动选择该云。</span><span class="sxs-lookup"><span data-stu-id="0a0b2-122">This creates the cloud, but does _not_ automatically select it.</span></span>

<span data-ttu-id="0a0b2-123">如果不再需要创建的云，可以使用 [cloud unregister](/cli/azure/cloud#unregister) 命令将它注销：</span><span class="sxs-lookup"><span data-stu-id="0a0b2-123">If you no longer require the created cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```

