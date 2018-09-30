---
title: 使用 Azure CLI 选择云
description: 使用 Azure CLI 创建、登录和管理多个云。
author: sptramer
manager: carmonm
ms.author: sttramer
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 92910e68a52fad3b3577db1bd01e918b69a895d7
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177702"
---
# <a name="select-clouds-with-the-azure-cli"></a><span data-ttu-id="c61d9-103">使用 Azure CLI 选择云</span><span class="sxs-lookup"><span data-stu-id="c61d9-103">Select clouds with the Azure CLI</span></span> 

<span data-ttu-id="c61d9-104">如果跨不同的区域工作或使用 [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/)，可能需要使用多个云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-104">If you work across different regions or use [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/), you may need to use more than one cloud.</span></span> <span data-ttu-id="c61d9-105">Microsoft 提供符合区域法规和客户用途的云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-105">Microsoft provides clouds for compliance with regional laws, which are available for your use.</span></span> <span data-ttu-id="c61d9-106">本文介绍如何获取有关云的信息、更改当前云，以及注册或取消注册新云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-106">This article shows you how to get information on clouds, change the current cloud, and register or unregister new clouds.</span></span>

## <a name="list-available-clouds"></a><span data-ttu-id="c61d9-107">可用云的列表</span><span class="sxs-lookup"><span data-stu-id="c61d9-107">List available clouds</span></span>

<span data-ttu-id="c61d9-108">可以使用 [az cloud list](/cli/azure/cloud#az-cloud-list) 命令列出可用的云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-108">You can list available clouds with the [az cloud list](/cli/azure/cloud#az-cloud-list) command.</span></span> <span data-ttu-id="c61d9-109">此命令显示当前处于活动状态的云和当前的配置文件，以及有关区域后缀和主机名的信息。</span><span class="sxs-lookup"><span data-stu-id="c61d9-109">This command shows which cloud is currently active, what its current profile is, and information on regional suffixes and host names.</span></span>

<span data-ttu-id="c61d9-110">获取活动的云以及所有可用云的列表：</span><span class="sxs-lookup"><span data-stu-id="c61d9-110">To get the active cloud and a list of all the available clouds:</span></span>

```azurecli-interactive
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

<span data-ttu-id="c61d9-111">在 `IsActive` 列中，当前处于活动状态的云的值为 `True`。</span><span class="sxs-lookup"><span data-stu-id="c61d9-111">The currently active cloud has `True` in the `IsActive` column.</span></span> <span data-ttu-id="c61d9-112">在任何时候，只能有一个云处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="c61d9-112">Only one cloud can be active at any time.</span></span> <span data-ttu-id="c61d9-113">若要获取有关某个云的更多详细信息，包括它对 Azure 服务使用的终结点，请使用 `cloud show` 命令：</span><span class="sxs-lookup"><span data-stu-id="c61d9-113">To get more detailed information on a cloud, including the endpoints that it uses for Azure services, use the `cloud show` command:</span></span>

```azurecli-interactive
az cloud show --name AzureChinaCloud --output json
```

```output
{
  "endpoints": {
    "activeDirectory": "https://login.chinacloudapi.cn",
    "activeDirectoryDataLakeResourceId": null,
    "activeDirectoryGraphResourceId": "https://graph.chinacloudapi.cn/",
    "activeDirectoryResourceId": "https://management.core.chinacloudapi.cn/",
    "batchResourceId": "https://batch.chinacloudapi.cn/",
    "gallery": "https://gallery.chinacloudapi.cn/",
    "management": "https://management.core.chinacloudapi.cn/",
    "resourceManager": "https://management.chinacloudapi.cn",
    "sqlManagement": "https://management.core.chinacloudapi.cn:8443/",
    "vmImageAliasDoc": "https://raw.githubusercontent.com/Azure/azure-rest-api-specs/master/arm-compute/quickstart-templates/aliases.json"
  },
  "isActive": false,
  "name": "AzureChinaCloud",
  "profile": "latest",
  "suffixes": {
    "azureDatalakeAnalyticsCatalogAndJobEndpoint": null,
    "azureDatalakeStoreFileSystemEndpoint": null,
    "keyvaultDns": ".vault.azure.cn",
    "sqlServerHostname": ".database.chinacloudapi.cn",
    "storageEndpoint": "core.chinacloudapi.cn"
  }
}
```

## <a name="switch-the-active-cloud"></a><span data-ttu-id="c61d9-114">切换活动的云</span><span class="sxs-lookup"><span data-stu-id="c61d9-114">Switch the active cloud</span></span>

<span data-ttu-id="c61d9-115">若要切换当前处于活动状态的云，请运行 [az cloud set](/cli/azure/cloud#az-cloud-set) 命令。</span><span class="sxs-lookup"><span data-stu-id="c61d9-115">To switch the currently active cloud, run the [az cloud set](/cli/azure/cloud#az-cloud-set) command.</span></span> <span data-ttu-id="c61d9-116">此命令采用一个必需参数，即云的名称。</span><span class="sxs-lookup"><span data-stu-id="c61d9-116">This command takes one required argument, the name of the cloud.</span></span>

```azurecli-interactive
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="c61d9-117">如果已激活的云的身份验证已过期，则在执行其他任何 CLI 任务之前，需要重新进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="c61d9-117">If your authentication for the activated cloud has expired, you need to re-authenticate before performing any other CLI tasks.</span></span> <span data-ttu-id="c61d9-118">首次切换到新云时，还需要设置活动的订阅。</span><span class="sxs-lookup"><span data-stu-id="c61d9-118">If this is your first time switching to the new cloud, you also need to set the active subscription.</span></span>
> <span data-ttu-id="c61d9-119">有关身份验证的说明，请参阅[使用 Azure CLI 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="c61d9-119">For instructions on authenticating, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span> <span data-ttu-id="c61d9-120">有关订阅管理的信息，请参阅[使用 Azure CLI 管理 Azure 订阅](manage-azure-subscriptions-azure-cli.md)</span><span class="sxs-lookup"><span data-stu-id="c61d9-120">For information on subscription management, see [Manage Azure subscriptions with Azure CLI](manage-azure-subscriptions-azure-cli.md)</span></span>

## <a name="register-a-new-cloud"></a><span data-ttu-id="c61d9-121">注册新云</span><span class="sxs-lookup"><span data-stu-id="c61d9-121">Register a new cloud</span></span>

<span data-ttu-id="c61d9-122">如果对 Azure Stack 使用了自己的终结点，请注册新云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-122">Register a new cloud if you have your own endpoints for Azure Stack.</span></span> <span data-ttu-id="c61d9-123">可以使用 [az cloud register](/cli/azure/cloud#az-cloud-register) 命令创建云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-123">Creating a cloud is done with the [az cloud register](/cli/azure/cloud#az-cloud-register) command.</span></span> <span data-ttu-id="c61d9-124">此命令需要一个名称和一组服务终结点。</span><span class="sxs-lookup"><span data-stu-id="c61d9-124">This command requires a name and a set of service endpoints.</span></span> <span data-ttu-id="c61d9-125">若要了解如何注册用于 Azure Stack 的云，请参阅[在 Azure Stack 中配合 Azure CLI 使用 API 版本配置文件](/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack)。</span><span class="sxs-lookup"><span data-stu-id="c61d9-125">To learn how to register a cloud for use with Azure Stack, see [Use API version profiles with Azure CLI in Azure Stack](/azure/azure-stack/user/azure-stack-version-profiles-azurecli2#connect-to-azure-stack).</span></span>

<span data-ttu-id="c61d9-126">在中国、美国政府或德国区域，不需要注册自己的云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-126">You do don't to register your own cloud for the China, US Government, or German regions.</span></span> <span data-ttu-id="c61d9-127">这些云由 Microsoft 管理，并且默认已开通。</span><span class="sxs-lookup"><span data-stu-id="c61d9-127">These clouds are managed by Microsoft and available by default.</span></span>  <span data-ttu-id="c61d9-128">有关所有可用终结点设置的详细信息，请参阅 [`az cloud register` 的文档](/cli/azure/cloud#az-cloud-register)。</span><span class="sxs-lookup"><span data-stu-id="c61d9-128">For more information on all of the available endpoint settings, see the [documentation for `az cloud register`](/cli/azure/cloud#az-cloud-register).</span></span>

<span data-ttu-id="c61d9-129">注册某个云不会自动切换到该云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-129">Registering a cloud doesn't automatically switch to it.</span></span> <span data-ttu-id="c61d9-130">使用 `az cloud set` 命令选择新建的云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-130">Use the `az cloud set` command to select the newly created cloud.</span></span>

## <a name="update-an-existing-cloud"></a><span data-ttu-id="c61d9-131">更新现有的云</span><span class="sxs-lookup"><span data-stu-id="c61d9-131">Update an existing cloud</span></span>

<span data-ttu-id="c61d9-132">如果拥有所需权限的话，则还可以更新现有的云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-132">If you have permissions, you can also update an existing cloud.</span></span> <span data-ttu-id="c61d9-133">更新某个云会切换到不同的 Azure 服务配置文件或修改连接终结点。</span><span class="sxs-lookup"><span data-stu-id="c61d9-133">Updating a cloud switches to a different Azure services profile or modifies the connection endpoints.</span></span>
<span data-ttu-id="c61d9-134">使用 [az cloud update](/cli/azure/cloud#az-cloud-update) 命令并添加与 `az cloud register` 相同的参数来更新云。</span><span class="sxs-lookup"><span data-stu-id="c61d9-134">Update a cloud with the [az cloud update](/cli/azure/cloud#az-cloud-update) command, which takes the same arguments as `az cloud register`.</span></span>

## <a name="unregister-a-cloud"></a><span data-ttu-id="c61d9-135">注销云</span><span class="sxs-lookup"><span data-stu-id="c61d9-135">Unregister a cloud</span></span>

<span data-ttu-id="c61d9-136">如果不再需要某个已创建的云，可以使用 [cloud unregister](/cli/azure/cloud#az-cloud-unregister) 命令将它取消注册：</span><span class="sxs-lookup"><span data-stu-id="c61d9-136">If you no longer need a created cloud, it can be unregistered with the [az cloud unregister](/cli/azure/cloud#az-cloud-unregister) command:</span></span>

```azurecli-interactive
az cloud unregister --name MyCloud
```
