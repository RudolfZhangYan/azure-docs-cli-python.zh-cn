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
ms.sourcegitcommit: 16426a08c0f2f62d0b9dca3df8132cece659acff
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/21/2017
---
# <a name="manage-multiple-azure-subscriptions"></a>管理多个 Azure 订阅

大多数 Azure 用户永远只有一个订阅。 但是，如果你在多家组织中工作，或者所在的组织已根据不同的组划分了对特定的资源的访问权限，则你在 Azure 中可能就有多个订阅。 可以使用 CLI 轻松管理多个订阅，并通过选择订阅执行操作。

## <a name="tenants-users-and-subscriptions"></a>租户、用户和订阅

在一定程度上，我们可能会对 Azure 中租户、用户和订阅感到混淆，不理解它们的差别。 一般而言，租户是包含整个组织的 Azure Active Directory 实体。 此租户至少包含一个订阅和用户。 用户是只与一个租户（即所属的组织）关联的个人。 用户是登录到 Azure 以预配和使用资源的帐户。 用户可能有权访问多个订阅，这些订阅是与 Microsoft 签署的有关使用云服务（包括 Azure）的协议。 每个资源与某个订阅关联。

若要详细了解租户、用户与订阅之间的差别，请参阅 [Azure 云术语字典](/azure/azure-glossary-cloud-terminology)。
若要了解如何将新订阅添加到 Azure Active Directory 租户，请参阅[如何将 Azure 订阅添加到 Azure Active Directory](/azure/active-directory/active-directory-how-subscriptions-associated-directory)。

## <a name="working-with-multiple-subscriptions"></a>使用多个订阅

若要访问订阅中包含的资源，需要切换活动的订阅。 针对订阅执行的所有操作将会参考订阅代表的服务协议（而不是个人帐户），通过 `az account` 命令完成。

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

若要开始使用可用的订阅，请获取帐户中提供的订阅列表：

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

若要更改活动的订阅，可以使用 `az account set`：

```azurecli-interactive
az account set --subscription "My Demos"
```

可以使用订阅 ID 或订阅名称来选择订阅。
