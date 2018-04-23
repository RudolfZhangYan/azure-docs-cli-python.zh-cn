---
title: Azure CLI 2.0 的可用扩展
description: 官方支持的 Azure CLI 2.0 扩展的完整列表。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/19/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 049ad9bd657ed76cf80ba0ab3262028458718dec
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a>Azure CLI 2.0 的可用扩展

本文是 Microsoft 提供并支持的 Azure CLI 2.0 可用扩展的完整列表。

也可以直接从 CLI 获得该扩展列表。 若要获取该列表，请运行 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available)：

```azurecli
az extension list-available --output table
```

| 名称 | 版本 | 摘要 | 预览 |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | 管理适用于 SAP 的 Azure 增强型监视扩展 |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.0 | 支持命令别名 | 是 |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.2.1 | 用于操作 Azure Batch 服务的其他命令 |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.4.3 | 为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层 |  |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | 适用于 DNS 区域的 Azure CLI 扩展 |  |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | 用于在不同区域之间复制映像的 Azure CLI 扩展。 |  |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 适用于管理组的 Azure CLI 扩展 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 支持“管理合作伙伴”预览版 |  |
| [rdbms](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | 提供 Azure MySQL 和 Azure PostgreSQL 支持的 Azure CLI 扩展。 |  |
| [subscription](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | 支持订阅管理预览版。 |  |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | 用于管理应用服务资源的 Azure CLI 扩展 | 是 |
