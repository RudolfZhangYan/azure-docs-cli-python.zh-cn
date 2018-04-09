---
title: Azure CLI 2.0 的可用扩展
description: 官方支持的 Azure CLI 2.0 扩展的完整列表。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/02/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: e7cf22d1611c224e1d7af351210e12fe0124fad0
ms.sourcegitcommit: 26e0816dad17cc3584d1724493feecf5f5faa1f5
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/04/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a>Azure CLI 2.0 的可用扩展

本文是 Microsoft 提供并支持的 Azure CLI 2.0 可用扩展的完整列表。

也可以直接从 CLI 获得该扩展列表。 若要获取该列表，请运行 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available)：

```azurecli
az extension list-available --output table
```

| 名称 | 版本 | 摘要 | 预览 |
|------|---------|---------|---------|
| [aem](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | 管理适用于 SAP 的 Azure 增强型监视扩展。 |  |
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.3.0 | 对命令别名的支持。 | 是 |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.1.0 | 附加的预览版 Azure Batch 命令。 |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.4.1 | 为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层。 |  |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | 对 Azure 专用 DNS 公共预览版的支持。 |  |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | 将映像从一个区域复制到另一个区域。 |  |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 对“管理组”预览版的支持。 | 是 |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 对“管理合作伙伴”预览版的支持。 | 是 |
| [rdbms](https://github.com/Azure/azure-cli-extensions) | 0.0.5 | 对 Azure MySQL 和 Azure PostgreSQL 的支持。 |  |
| [subscription](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | 对订阅定义预览版的支持。 | 是 |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.0 | 创建和部署应用服务资源。 | 是 |
