---
title: "使用 Azure CLI 2.0 管理多个云"
description: "使用 Azure CLI 2.0 创建、登录和管理不同的云。"
keywords: "Azure CLI 2.0, Azure, 云, 数据中心, 政府, 区域, 中国, 德国"
author: sptramer
manager: routlaw
ms.author: sttramer
ms.date: 10/20/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.openlocfilehash: cb470d179daf7cb4ecf535903adb12071602034e
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a><span data-ttu-id="8a8d8-104">使用 Azure CLI 2.0 管理多个云</span><span class="sxs-lookup"><span data-stu-id="8a8d8-104">Managing multiple clouds with Azure CLI 2.0</span></span>

<span data-ttu-id="8a8d8-105">如果跨不同的区域工作或使用 [Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/user/)，可能需要使用多个云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-105">If you work across different regions or use [Azure Stack](https://docs.microsoft.com/en-us/azure/azure-stack/user/), you may need to use more than one cloud.</span></span> <span data-ttu-id="8a8d8-106">Microsoft 提供符合区域法规和客户用途的云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-106">Microsoft provides clouds for compliance with regional laws, which are available for your use.</span></span> <span data-ttu-id="8a8d8-107">本文介绍如何获取有关帐户可用的云、更改当前云，以及注册或注销用于 Azure Stack 的新云的信息。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-107">This article shows you how to get information on clouds available to your account, change the current cloud, and register or unregister new clouds for use with Azure Stack.</span></span>

## <a name="listing-clouds"></a><span data-ttu-id="8a8d8-108">列出云</span><span class="sxs-lookup"><span data-stu-id="8a8d8-108">Listing clouds</span></span>

<span data-ttu-id="8a8d8-109">可以使用 [cloud list](/cli/azure/cloud#list) 命令列出可用的云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-109">You can list available clouds with the [cloud list](/cli/azure/cloud#list) command.</span></span> <span data-ttu-id="8a8d8-110">此命令会告知当前处于活动状态的云和当前的配置文件，以及有关区域后缀和主机名的信息。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-110">This tells you which cloud is currently active, what its current profile is, and information on regional suffixes and host names.</span></span>

<span data-ttu-id="8a8d8-111">获取活动的云以及所有可用云的列表：</span><span class="sxs-lookup"><span data-stu-id="8a8d8-111">To get the active cloud and a list of all the available clouds:</span></span>

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

<span data-ttu-id="8a8d8-112">在 `IsActive` 列中，当前处于活动状态的云的值为 `True`。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-112">The currently active cloud has `True` in the `IsActive` column.</span></span> <span data-ttu-id="8a8d8-113">在任何时候，只能有一个云处于活动状态。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-113">Only one cloud can be active at any time.</span></span> <span data-ttu-id="8a8d8-114">若要获取有关某个云的更多详细信息，包括它对 Azure 服务使用的终结点，请使用 `cloud show` 命令：</span><span class="sxs-lookup"><span data-stu-id="8a8d8-114">To get more detailed information on a cloud, including the endpoints that it uses for Azure services, use the `cloud show` command:</span></span>

```azurecli
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

## <a name="switching-the-active-cloud"></a><span data-ttu-id="8a8d8-115">切换活动的云</span><span class="sxs-lookup"><span data-stu-id="8a8d8-115">Switching the active cloud</span></span>

<span data-ttu-id="8a8d8-116">若要切换当前处于活动状态的云，请运行 [cloud set](/cli/azure/cloud#set) 命令。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-116">To switch the currently active cloud, run the [cloud set](/cli/azure/cloud#set) command.</span></span> <span data-ttu-id="8a8d8-117">此命令采用一个必需参数，即云的名称。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-117">This command takes one required argument, the name of the cloud.</span></span>

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> <span data-ttu-id="8a8d8-118">如果已激活的云的身份验证已过期，则在执行其他任何 CLI 任务之前，需要重新进行身份验证。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-118">If your authentication for the activated cloud has expired, you need to re-authenticate before performing any other CLI tasks.</span></span> <span data-ttu-id="8a8d8-119">首次切换到新云时，还需要设置活动的订阅。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-119">If this is your first time switching to the new cloud, you also need to set the active subscription.</span></span>
> <span data-ttu-id="8a8d8-120">有关身份验证的说明，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-120">For instructions on authenticating, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span> <span data-ttu-id="8a8d8-121">有关订阅管理的信息，请参阅[使用 Azure CLI 2.0 管理 Azure 订阅](manage-azure-subscriptions-azure-cli.md)</span><span class="sxs-lookup"><span data-stu-id="8a8d8-121">For information on subscription management, see [Manage Azure subscriptions with Azure CLI 2.0](manage-azure-subscriptions-azure-cli.md)</span></span>

## <a name="register-a-cloud"></a><span data-ttu-id="8a8d8-122">注册云</span><span class="sxs-lookup"><span data-stu-id="8a8d8-122">Register a cloud</span></span>

<span data-ttu-id="8a8d8-123">如果对 Azure Stack 使用了自己的终结点，请注册新云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-123">Register a new cloud if you have your own endpoints for Azure Stack.</span></span> <span data-ttu-id="8a8d8-124">可以使用 [cloud register](/cli/azure/cloud#register) 命令创建云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-124">Creating a cloud is done with the [cloud register](/cli/azure/cloud#register) command.</span></span> <span data-ttu-id="8a8d8-125">此命令需要一个名称，以及一组具有关联终结点的功能。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-125">This command requires a name and a set of capabilities with associated endpoints.</span></span> <span data-ttu-id="8a8d8-126">若要了解如何注册用于 Azure Stack 的云，请参阅[安装和配置用于 Azure Stack 的 CLI](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack)。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-126">To learn how to register a cloud for use with Azure Stack, see [Install and configure CLI for use with Azure Stack](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack).</span></span>  

<span data-ttu-id="8a8d8-127">在中国、美国政府或德国区域，不需要注册自己的云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-127">You do not need to register your own cloud for China, US Government, or German regions.</span></span> <span data-ttu-id="8a8d8-128">这些设置由 Microsoft 管理，并根据默认情况开通。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-128">These are managed by Microsoft and available by default.</span></span>  <span data-ttu-id="8a8d8-129">有关所有可用终结点设置的详细信息，请参阅 [`az cloud register` 的文档](/cli/azure/cloud?view=azure-cli-latest#az_cloud_register)。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-129">For more information on all of the available endpoint settings, see the [documentation for `az cloud register`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_register).</span></span>

<span data-ttu-id="8a8d8-130">注册某个云不会自动切换到该云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-130">Registering a cloud does not automatically switch to it.</span></span> <span data-ttu-id="8a8d8-131">如前所述使用 `az cloud set` 命令可以选择新建的云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-131">Use the `az cloud set` command to select the newly created cloud as described above.</span></span>

## <a name="update-an-existing-cloud"></a><span data-ttu-id="8a8d8-132">更新现有的云</span><span class="sxs-lookup"><span data-stu-id="8a8d8-132">Update an existing cloud</span></span>

<span data-ttu-id="8a8d8-133">如果拥有所需权限的话，则还可以更新现有的云。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-133">If you have permissions, you can also update an existing cloud.</span></span> <span data-ttu-id="8a8d8-134">请在需要切换到不同 Azure 配置文件、添加终结点或更改终结点的情况下执行此操作。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-134">Do this when you need to switch to a different Azure profile, add an endpoint, or change an endpoint.</span></span>
<span data-ttu-id="8a8d8-135">为此，可以使用 `az cloud update` 命令并添加与 `az cloud register` 相同的参数。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-135">You do this with the `az cloud update` command, which takes the same arguments as `az cloud register`.</span></span> <span data-ttu-id="8a8d8-136">有关详细信息，请参阅 [`az cloud update` 的文档](/cli/azure/cloud?view=azure-cli-latest#az_cloud_update)。</span><span class="sxs-lookup"><span data-stu-id="8a8d8-136">For more information, see the [documentation for `az cloud update`](/cli/azure/cloud?view=azure-cli-latest#az_cloud_update).</span></span>

## <a name="unregister-a-cloud"></a><span data-ttu-id="8a8d8-137">注销云</span><span class="sxs-lookup"><span data-stu-id="8a8d8-137">Unregister a cloud</span></span>

<span data-ttu-id="8a8d8-138">如果不再需要某个已注册的云，可以使用 [cloud unregister](/cli/azure/cloud#unregister) 命令将其注销：</span><span class="sxs-lookup"><span data-stu-id="8a8d8-138">If you no longer require a registered cloud, it can be unregistered with the [cloud unregister](/cli/azure/cloud#unregister) command:</span></span>

```azurecli
az cloud unregister --name MyCloud
```
