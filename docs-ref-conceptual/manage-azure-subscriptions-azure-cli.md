---
title: "使用 Azure CLI 2.0 管理 Azure 订阅"
description: "在 Linux、Mac 或 Windows 上使用 Azure CLI 2.0 管理 Azure 订阅。"
keywords: "Azure CLI 2.0, Linux, Mac, Windows, OS X, 订阅"
author: kamaljit
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 98fb955e-6dbf-47e2-80ac-170d6d95cb70
ms.openlocfilehash: 383fb6ebd90ac79f60869187b402d53d4f1791fd
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/05/2017
---
# <a name="manage-multiple-azure-subscriptions"></a><span data-ttu-id="82e65-104">管理多个 Azure 订阅</span><span class="sxs-lookup"><span data-stu-id="82e65-104">Manage multiple Azure subscriptions</span></span>

<span data-ttu-id="82e65-105">如果你是 Azure 的新手，也许只有一个订阅。</span><span class="sxs-lookup"><span data-stu-id="82e65-105">If you are brand new to Azure, you probably only have a single subscription.</span></span>
<span data-ttu-id="82e65-106">但如果你使用 Azure 有一段时间，可能已创建了多个 Azure 订阅。</span><span class="sxs-lookup"><span data-stu-id="82e65-106">But if you have been using Azure for a while, you may have created multiple Azure subscriptions.</span></span>
<span data-ttu-id="82e65-107">如果是这样，可将 Azure CLI 2.0 配置为针对特定的订阅执行命令。</span><span class="sxs-lookup"><span data-stu-id="82e65-107">If so, you can configure Azure CLI 2.0 to execute commands against a particular subscription.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

1. <span data-ttu-id="82e65-108">获取帐户中所有订阅的列表。</span><span class="sxs-lookup"><span data-stu-id="82e65-108">Get a list of all subscriptions in your account.</span></span>

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

1. <span data-ttu-id="82e65-109">设置默认值。</span><span class="sxs-lookup"><span data-stu-id="82e65-109">Set the default.</span></span>
 
   ```azurecli-interactive
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > <span data-ttu-id="82e65-110">`--subscription` 参数采用订阅名称或订阅 ID。</span><span class="sxs-lookup"><span data-stu-id="82e65-110">The `--subscription` parameter takes either the subscription name or the subscription ID.</span></span>

<span data-ttu-id="82e65-111">可通过再次运行 `az account list --output table` 命令来验证更改。</span><span class="sxs-lookup"><span data-stu-id="82e65-111">You can verify the change by running the `az account list --output table` command again.</span></span>

<span data-ttu-id="82e65-112">设置默认订阅后，所有后续 Azure CLI 命令将针对此订阅运行。</span><span class="sxs-lookup"><span data-stu-id="82e65-112">Once you set your default subscription, all subsequent Azure CLI commands run against this subscription.</span></span>