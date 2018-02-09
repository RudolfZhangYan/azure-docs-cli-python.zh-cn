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
ms.openlocfilehash: 6f4cfec45becc0c4940e9066af53396b41db779d
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2018
---
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>使用 Azure CLI 2.0 管理多个云

如果跨不同的区域工作或使用 [Azure Stack](https://docs.microsoft.com/azure/azure-stack/user/)，可能需要使用多个云。 Microsoft 提供符合区域法规和客户用途的云。 本文介绍如何获取有关帐户可用的云、更改当前云，以及注册或注销用于 Azure Stack 的新云的信息。

## <a name="listing-clouds"></a>列出云

可以使用 [cloud list](/cli/azure/cloud#list) 命令列出可用的云。 此命令会告知当前处于活动状态的云和当前的配置文件，以及有关区域后缀和主机名的信息。

获取活动的云以及所有可用云的列表：

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

在 `IsActive` 列中，当前处于活动状态的云的值为 `True`。 在任何时候，只能有一个云处于活动状态。 若要获取有关某个云的更多详细信息，包括它对 Azure 服务使用的终结点，请使用 `cloud show` 命令：

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

## <a name="switching-the-active-cloud"></a>切换活动的云

若要切换当前处于活动状态的云，请运行 [cloud set](/cli/azure/cloud#set) 命令。 此命令采用一个必需参数，即云的名称。

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> 如果已激活的云的身份验证已过期，则在执行其他任何 CLI 任务之前，需要重新进行身份验证。 首次切换到新云时，还需要设置活动的订阅。
> 有关身份验证的说明，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。 有关订阅管理的信息，请参阅[使用 Azure CLI 2.0 管理 Azure 订阅](manage-azure-subscriptions-azure-cli.md)

## <a name="register-a-cloud"></a>注册云

如果对 Azure Stack 使用了自己的终结点，请注册新云。 可以使用 [cloud register](/cli/azure/cloud#register) 命令创建云。 此命令需要一个名称，以及一组具有关联终结点的功能。 若要了解如何注册用于 Azure Stack 的云，请参阅[安装和配置用于 Azure Stack 的 CLI](/azure/azure-stack/user/azure-stack-connect-cli#connect-to-azure-stack)。

在中国、美国政府或德国区域，不需要注册自己的云。 这些设置由 Microsoft 管理，并根据默认情况开通。  有关所有可用终结点设置的详细信息，请参阅 [`az cloud register` 的文档](/cli/azure/cloud?view=azure-cli-latest#az_cloud_register)。

注册某个云不会自动切换到该云。 如前所述使用 `az cloud set` 命令可以选择新建的云。

## <a name="update-an-existing-cloud"></a>更新现有的云

如果拥有所需权限的话，则还可以更新现有的云。 请在需要切换到不同 Azure 配置文件、添加终结点或更改终结点的情况下执行此操作。
为此，可以使用 `az cloud update` 命令并添加与 `az cloud register` 相同的参数。 有关详细信息，请参阅 [`az cloud update` 的文档](/cli/azure/cloud?view=azure-cli-latest#az_cloud_update)。

## <a name="unregister-a-cloud"></a>注销云

如果不再需要某个已注册的云，可以使用 [cloud unregister](/cli/azure/cloud#unregister) 命令将其注销：

```azurecli
az cloud unregister --name MyCloud
```