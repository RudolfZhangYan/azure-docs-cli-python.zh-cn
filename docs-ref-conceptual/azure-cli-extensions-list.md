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
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="5ac59-103">Azure CLI 2.0 的可用扩展</span><span class="sxs-lookup"><span data-stu-id="5ac59-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="5ac59-104">本文是 Microsoft 提供并支持的 Azure CLI 2.0 可用扩展的完整列表。</span><span class="sxs-lookup"><span data-stu-id="5ac59-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="5ac59-105">也可以直接从 CLI 获得该扩展列表。</span><span class="sxs-lookup"><span data-stu-id="5ac59-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="5ac59-106">若要获取该列表，请运行 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available)：</span><span class="sxs-lookup"><span data-stu-id="5ac59-106">To get it, run [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="5ac59-107">名称</span><span class="sxs-lookup"><span data-stu-id="5ac59-107">Name</span></span> | <span data-ttu-id="5ac59-108">版本</span><span class="sxs-lookup"><span data-stu-id="5ac59-108">Version</span></span> | <span data-ttu-id="5ac59-109">摘要</span><span class="sxs-lookup"><span data-stu-id="5ac59-109">Summary</span></span> | <span data-ttu-id="5ac59-110">预览</span><span class="sxs-lookup"><span data-stu-id="5ac59-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="5ac59-111">aem</span><span class="sxs-lookup"><span data-stu-id="5ac59-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-112">0.1.1</span><span class="sxs-lookup"><span data-stu-id="5ac59-112">0.1.1</span></span> | <span data-ttu-id="5ac59-113">管理适用于 SAP 的 Azure 增强型监视扩展</span><span class="sxs-lookup"><span data-stu-id="5ac59-113">Manage Azure Enhanced Monitoring Extensions for SAP</span></span> |  |
| [<span data-ttu-id="5ac59-114">alias</span><span class="sxs-lookup"><span data-stu-id="5ac59-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-115">0.5.0</span><span class="sxs-lookup"><span data-stu-id="5ac59-115">0.5.0</span></span> | <span data-ttu-id="5ac59-116">支持命令别名</span><span class="sxs-lookup"><span data-stu-id="5ac59-116">Support for command aliases</span></span> | <span data-ttu-id="5ac59-117">是</span><span class="sxs-lookup"><span data-stu-id="5ac59-117">Yes</span></span> |
| [<span data-ttu-id="5ac59-118">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="5ac59-118">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="5ac59-119">2.2.1</span><span class="sxs-lookup"><span data-stu-id="5ac59-119">2.2.1</span></span> | <span data-ttu-id="5ac59-120">用于操作 Azure Batch 服务的其他命令</span><span class="sxs-lookup"><span data-stu-id="5ac59-120">Additional commands for working with Azure Batch service</span></span> |  |
| [<span data-ttu-id="5ac59-121">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="5ac59-121">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="5ac59-122">0.4.3</span><span class="sxs-lookup"><span data-stu-id="5ac59-122">0.4.3</span></span> | <span data-ttu-id="5ac59-123">为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层</span><span class="sxs-lookup"><span data-stu-id="5ac59-123">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service</span></span> |  |
| [<span data-ttu-id="5ac59-124">dns</span><span class="sxs-lookup"><span data-stu-id="5ac59-124">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-125">0.0.2</span><span class="sxs-lookup"><span data-stu-id="5ac59-125">0.0.2</span></span> | <span data-ttu-id="5ac59-126">适用于 DNS 区域的 Azure CLI 扩展</span><span class="sxs-lookup"><span data-stu-id="5ac59-126">An Azure CLI Extension for DNS zones</span></span> |  |
| [<span data-ttu-id="5ac59-127">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="5ac59-127">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-128">0.0.5</span><span class="sxs-lookup"><span data-stu-id="5ac59-128">0.0.5</span></span> | <span data-ttu-id="5ac59-129">用于在不同区域之间复制映像的 Azure CLI 扩展。</span><span class="sxs-lookup"><span data-stu-id="5ac59-129">An Azure CLI Extension that copies images from region to region.</span></span> |  |
| [<span data-ttu-id="5ac59-130">managementgroups</span><span class="sxs-lookup"><span data-stu-id="5ac59-130">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-131">0.1.0</span><span class="sxs-lookup"><span data-stu-id="5ac59-131">0.1.0</span></span> | <span data-ttu-id="5ac59-132">适用于管理组的 Azure CLI 扩展</span><span class="sxs-lookup"><span data-stu-id="5ac59-132">An Azure CLI Extension for Management Groups</span></span> |  |
| [<span data-ttu-id="5ac59-133">managementpartner</span><span class="sxs-lookup"><span data-stu-id="5ac59-133">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-134">0.1.2</span><span class="sxs-lookup"><span data-stu-id="5ac59-134">0.1.2</span></span> | <span data-ttu-id="5ac59-135">支持“管理合作伙伴”预览版</span><span class="sxs-lookup"><span data-stu-id="5ac59-135">Support for Management Partner preview</span></span> |  |
| [<span data-ttu-id="5ac59-136">rdbms</span><span class="sxs-lookup"><span data-stu-id="5ac59-136">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-137">0.0.5</span><span class="sxs-lookup"><span data-stu-id="5ac59-137">0.0.5</span></span> | <span data-ttu-id="5ac59-138">提供 Azure MySQL 和 Azure PostgreSQL 支持的 Azure CLI 扩展。</span><span class="sxs-lookup"><span data-stu-id="5ac59-138">An Azure CLI Extension providing support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="5ac59-139">subscription</span><span class="sxs-lookup"><span data-stu-id="5ac59-139">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-140">0.1.1</span><span class="sxs-lookup"><span data-stu-id="5ac59-140">0.1.1</span></span> | <span data-ttu-id="5ac59-141">支持订阅管理预览版。</span><span class="sxs-lookup"><span data-stu-id="5ac59-141">Support for subscription management preview.</span></span> |  |
| [<span data-ttu-id="5ac59-142">webapp</span><span class="sxs-lookup"><span data-stu-id="5ac59-142">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="5ac59-143">0.2.1</span><span class="sxs-lookup"><span data-stu-id="5ac59-143">0.2.1</span></span> | <span data-ttu-id="5ac59-144">用于管理应用服务资源的 Azure CLI 扩展</span><span class="sxs-lookup"><span data-stu-id="5ac59-144">An Azure CLI Extension to manage appservice resources</span></span> | <span data-ttu-id="5ac59-145">是</span><span class="sxs-lookup"><span data-stu-id="5ac59-145">Yes</span></span> |
