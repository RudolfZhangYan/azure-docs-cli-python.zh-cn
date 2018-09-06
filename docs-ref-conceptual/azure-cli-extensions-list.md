---
title: Azure CLI 2.0 的可用扩展
description: 官方支持的 Azure CLI 2.0 扩展的完整列表。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 08/31/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 11125445d09ec8f0c62b1f508093bdfef9ad9e44
ms.sourcegitcommit: 252e5e1b5d0ab868044a9c03f2c9fefc22d362b4
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/31/2018
ms.locfileid: "43380911"
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
| [alias](https://github.com/Azure/azure-cli-extensions) | 0.5.1 | 支持命令别名 | 是 |
| [azure-batch-cli-extensions](https://github.com/Azure/azure-batch-cli-extensions) | 2.4.1 | 用于操作 Azure Batch 服务的其他命令 |  |
| [azure-cli-iot-ext](https://github.com/azure/azure-iot-cli-extension) | 0.5.1 | 为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层 |  |
| [botservice](https://github.com/Azure/azure-cli-extensions) | 0.0.3 | 支持 Azure 机器人服务 2017-12-01 预览版功能 | 是 |
| [dev-spaces-preview](https://github.com/Azure/azure-cli-extensions) | 0.1.6 | Dev Spaces 为团队提供快速、迭代的 Kubernetes 开发体验。 | 是 |
| [dns](https://github.com/Azure/azure-cli-extensions) | 0.0.2 | 适用于 DNS 区域的 Azure CLI 扩展 |  |
| [eventgrid](https://github.com/Azure/azure-cli-extensions) | 0.2.1 | 对 Azure EventGrid 2018-05-01-preview 功能的支持 | 是 |
| [express-route-cross-connection](https://github.com/Azure/azure-cli-extensions/tree/master/src/express-route-cross-connection) | 0.1.0 | 使用 ExpressRoute 跨连接管理客户的 ExpressRoute 线路。 |  |
| [find](https://github.com/Azure/azure-cli-extensions/tree/master/src/find) | 0.1.0 | 适用于 CLI 信息的智能查询。 | 是 |
| [image-copy-extension](https://github.com/Azure/azure-cli-extensions) | 0.0.8 | 对在区域之间复制托管 VM 映像的支持 |  |
| [keyvault-preview](https://github.com/Azure/azure-keyvault-cli-extension) | 0.1.3 | 预览 Azure Key Vault 命令。 | 是 |
| [log-analytics](https://github.com/Azure/azure-cli-extensions/tree/master/src/log-analytics) | 0.1.2 | 支持 Azure Log Analytics 查询功能。 | 是 |
| [managementgroups](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 适用于管理组的 Azure CLI 扩展 |  |
| [managementpartner](https://github.com/Azure/azure-cli-extensions) | 0.1.2 | 支持“管理合作伙伴”预览版 |  |
| [mesh](https://github.com/Azure/azure-cli-extensions) | 0.9.1 | 支持 Microsoft Azure Service Fabric 网格 - 公共预览版 | 是 |
| [rdbms-vnet](https://github.com/Azure/azure-cli-extensions) | 10.0.0 | 支持 Azure MySQL 和 Azure PostgreSQL 资源中的虚拟网络规则 |  |
| [signalr](https://github.com/Azure/azure-cli-extensions) | 0.1.0 | 支持 signalr 管理预览版。 | 是 |
| [storage-preview](https://github.com/Azure/azure-cli-extensions/tree/master/src/storage-preview) | 0.1.4 | 提供即将推出的存储功能的预览版。 | 是 |
| [subscription](https://github.com/Azure/azure-cli-extensions) | 0.1.1 | 支持订阅管理预览版。 |  |
| [webapp](https://github.com/Azure/azure-cli-extensions) | 0.2.8 | 用于管理应用服务资源的 Azure CLI 扩展 | 是 |
