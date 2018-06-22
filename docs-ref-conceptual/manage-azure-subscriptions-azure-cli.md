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
# <a name="manage-multiple-azure-subscriptions"></a>管理多个 Azure 订阅

大多数 Azure 用户永远只有一个订阅。 但是，如果你在多家组织中工作，或者所在的组织已根据不同的组划分了对特定的资源的访问权限，则你在 Azure 中可能就有多个订阅。 可以使用 CLI 轻松管理多个订阅，只需为所有命令设置全局订阅或为每个命令选择一个订阅即可。

## <a name="tenants-users-and-subscriptions"></a>租户、用户和订阅

在一定程度上，我们可能会对 Azure 中租户、用户和订阅感到混淆，不理解它们的差别。 租户是包含整个组织的 Azure Active Directory 实体。 此租户至少包含一个订阅和用户。 用户是只与一个租户（即所属的组织）关联的个人。 用户是登录到 Azure 以预配和使用资源的帐户。
用户可能有权访问多个订阅，这些订阅是与 Microsoft 签署的有关使用云服务（包括 Azure）的协议。 每个资源与某个订阅关联。

若要详细了解租户、用户与订阅之间的差别，请参阅 [Azure 云术语字典](/azure/azure-glossary-cloud-terminology)。  若要了解如何将新订阅添加到 Azure Active Directory 租户，请参阅[如何将 Azure 订阅添加到 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。
使用多个租户时，可能需要登录到特定租户。 为此，请参阅[使用 Azure CLI 登录](/cli/azure/authenticate-azure-cli)。

## <a name="work-with-multiple-subscriptions"></a>使用多个订阅

若要访问订阅中包含的资源，需要切换活动的订阅。 可以使用 [az account set](/cli/azure/account#az-account-set) 为所有 Azure CLI 命令切换订阅，也可以使用 `--subscription` 参数为单个命令这样做。

需提供可用订阅的列表才能开始操作。 若要获取该列表，请使用 [az account list](/cli/azure/account#az-account-list) 命令：

```azurecli-interactive
az account list --output table
```

若要以全局方式更改活动订阅，请使用 `az account set` 和订阅 ID 或订阅名称：

```azurecli-interactive
az account set --subscription "My Demos"
```

若要对某个命令使用特定的订阅，请直接使用 `--subscription` 参数。 此参数使用订阅 ID 或订阅名称：

```azurecli-interactive
az vm create --subscription "My Demos" --resource-group MyGroup --name NewVM --image Ubuntu
```
