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
# <a name="managing-multiple-clouds-with-azure-cli-20"></a>使用 Azure CLI 2.0 管理多个云

如果有多个订阅与 Azure 关联，则可以获得多个可用的云。 每个云有自身的关联终结点和功能，并且通常与具有不同数据保护标准或要求的特定区域相关联。

若要有效使用多个云，需要能够切换当前处于活动状态的云，并且可能需要创建新云。

## <a name="listing-clouds"></a>列出云

可以使用 [cloud list](/cli/azure/cloud#list) 命令列出可用的云。 此命令会告知当前哪个云处于活动状态及其当前配置文件是什么，并可提供有关区域后缀和主机名的信息。

获取可用云以及当前处于活动状态的云的列表：

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

## <a name="switching-the-active-cloud"></a>切换活动的云

若要切换当前处于活动状态的云，请运行 [cloud set](/cli/azure/cloud#set) 命令。 此命令采用一个必需参数，即云的名称。

```azurecli
az cloud set --name AzureChinaCloud
```

> [!IMPORTANT]
> 如果从未针对活动的云执行过身份验证，则需要先执行身份验证，然后才能执行其他任何 CLI 操作。 有关身份验证的说明，请参阅[使用 Azure CLI 2.0 登录](/cli/azure/authenticate-azure-cli)。

## <a name="register-or-unregister-a-cloud"></a>注册或注销云

如果有自己的终结点或需要不同的配置文件，请注册新云。 可以使用 [cloud register](/cli/azure/cloud#register) 命令创建云。 此命令需要一个名称，有时还需要一组功能和终结点指定值。

使用特定的配置文件为资源管理器创建包含专用终结点的云：

```azurecli
az cloud register --name MyCloud --endpoint-resource-manager "https://my.endpoint.manager" --profile 2017-03-09-profile
```

这会创建云，但不会自动选择该云。

如果不再需要创建的云，可以使用 [cloud unregister](/cli/azure/cloud#unregister) 命令将它注销：

```azurecli
az cloud unregister --name MyCloud
```

