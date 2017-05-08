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
ms.openlocfilehash: a28b24dd186fc567f36e52f8a0f5a7c2b0af060c
ms.sourcegitcommit: c2d380f4ad8e7606850530db690855bcccfd6e86
ms.translationtype: HT
ms.contentlocale: zh-CN
---
# <a name="manage-multiple-azure-subscriptions"></a>管理多个 Azure 订阅

如果你是 Azure 的新手，也许只有一个订阅。
但如果你使用 Azure 有一段时间，可能已创建了多个 Azure 订阅。
如果是这样，可将 Azure CLI 2.0 配置为针对特定的订阅执行命令。

1. 获取帐户中所有订阅的列表。

   ```azurecli
   az account list --output table
   ```

   ```Output
   Name                                         CloudName    SubscriptionId                        State     IsDefault
   -------------------------------------------  -----------  ------------------------------------  --------  -----------
   My Production Subscription                   AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   My DevTest Subscription                      AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled   True
   My Demos                                     AzureCloud   XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX  Enabled
   ```

1. 设置默认值。
 
   ```azurecli
   az account set --subscription "My Demos"
   ```

   > [!NOTE]
   > `--subscription` 参数采用订阅名称或订阅 ID。

可通过再次运行 `az account list --output table` 命令来验证更改。

设置默认订阅后，所有后续 Azure CLI 命令将针对此订阅运行。