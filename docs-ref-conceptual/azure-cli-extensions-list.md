---
title: Azure CLI 2.0 的可用扩展
description: 官方支持的 Azure CLI 2.0 扩展的完整列表。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 03/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: ceca7ed92435ab03b196e60dee37195330f6f3c7
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/28/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="fc806-103">Azure CLI 2.0 的可用扩展</span><span class="sxs-lookup"><span data-stu-id="fc806-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="fc806-104">本文是 Microsoft 提供并支持的 Azure CLI 2.0 可用扩展的完整列表。</span><span class="sxs-lookup"><span data-stu-id="fc806-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="fc806-105">也可以直接从 CLI 获得该扩展列表。</span><span class="sxs-lookup"><span data-stu-id="fc806-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="fc806-106">若要获取该列表，请运行 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available)：</span><span class="sxs-lookup"><span data-stu-id="fc806-106">To get it, run [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="fc806-107">名称</span><span class="sxs-lookup"><span data-stu-id="fc806-107">Name</span></span> | <span data-ttu-id="fc806-108">版本</span><span class="sxs-lookup"><span data-stu-id="fc806-108">Version</span></span> | <span data-ttu-id="fc806-109">摘要</span><span class="sxs-lookup"><span data-stu-id="fc806-109">Summary</span></span> | <span data-ttu-id="fc806-110">预览</span><span class="sxs-lookup"><span data-stu-id="fc806-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="fc806-111">aem</span><span class="sxs-lookup"><span data-stu-id="fc806-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-112">0.1.0</span><span class="sxs-lookup"><span data-stu-id="fc806-112">0.1.0</span></span> | <span data-ttu-id="fc806-113">管理适用于 SAP 的 Azure 增强型监视扩展。</span><span class="sxs-lookup"><span data-stu-id="fc806-113">Manage Azure Enhanced Monitoring Extensions for SAP.</span></span> |  |
| [<span data-ttu-id="fc806-114">alias</span><span class="sxs-lookup"><span data-stu-id="fc806-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-115">0.2.0</span><span class="sxs-lookup"><span data-stu-id="fc806-115">0.2.0</span></span> | <span data-ttu-id="fc806-116">对命令别名的支持。</span><span class="sxs-lookup"><span data-stu-id="fc806-116">Support for command aliases.</span></span> |  |
| [<span data-ttu-id="fc806-117">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="fc806-117">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="fc806-118">2.1.0</span><span class="sxs-lookup"><span data-stu-id="fc806-118">2.1.0</span></span> | <span data-ttu-id="fc806-119">附加的预览版 Azure Batch 命令。</span><span class="sxs-lookup"><span data-stu-id="fc806-119">Additional preview Azure Batch commands.</span></span> |  |
| [<span data-ttu-id="fc806-120">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="fc806-120">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="fc806-121">0.4.1</span><span class="sxs-lookup"><span data-stu-id="fc806-121">0.4.1</span></span> | <span data-ttu-id="fc806-122">为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层。</span><span class="sxs-lookup"><span data-stu-id="fc806-122">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service.</span></span> |  |
| [<span data-ttu-id="fc806-123">dns</span><span class="sxs-lookup"><span data-stu-id="fc806-123">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-124">0.0.1</span><span class="sxs-lookup"><span data-stu-id="fc806-124">0.0.1</span></span> | <span data-ttu-id="fc806-125">对 Azure 专用 DNS 公共预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="fc806-125">Support for the Azure Private DNS Public Preview.</span></span> |  |
| [<span data-ttu-id="fc806-126">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="fc806-126">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-127">0.0.5</span><span class="sxs-lookup"><span data-stu-id="fc806-127">0.0.5</span></span> | <span data-ttu-id="fc806-128">将映像从一个区域复制到另一个区域。</span><span class="sxs-lookup"><span data-stu-id="fc806-128">Copy images from region to region.</span></span> |  |
| [<span data-ttu-id="fc806-129">managementgroups</span><span class="sxs-lookup"><span data-stu-id="fc806-129">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-130">0.1.0</span><span class="sxs-lookup"><span data-stu-id="fc806-130">0.1.0</span></span> | <span data-ttu-id="fc806-131">对“管理组”预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="fc806-131">Support for Management Groups preview.</span></span> | <span data-ttu-id="fc806-132">是</span><span class="sxs-lookup"><span data-stu-id="fc806-132">Yes</span></span> |
| [<span data-ttu-id="fc806-133">managementpartner</span><span class="sxs-lookup"><span data-stu-id="fc806-133">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-134">0.1.0</span><span class="sxs-lookup"><span data-stu-id="fc806-134">0.1.0</span></span> | <span data-ttu-id="fc806-135">对“管理合作伙伴”预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="fc806-135">Support for Management Partner preview.</span></span> | <span data-ttu-id="fc806-136">是</span><span class="sxs-lookup"><span data-stu-id="fc806-136">Yes</span></span> |
| [<span data-ttu-id="fc806-137">rdbms</span><span class="sxs-lookup"><span data-stu-id="fc806-137">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-138">0.0.4</span><span class="sxs-lookup"><span data-stu-id="fc806-138">0.0.4</span></span> | <span data-ttu-id="fc806-139">对 Azure MySQL 和 Azure PostgreSQL 的支持。</span><span class="sxs-lookup"><span data-stu-id="fc806-139">Support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="fc806-140">subscription</span><span class="sxs-lookup"><span data-stu-id="fc806-140">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-141">0.1.0</span><span class="sxs-lookup"><span data-stu-id="fc806-141">0.1.0</span></span> | <span data-ttu-id="fc806-142">对订阅定义预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="fc806-142">Support for subscription definitions preview.</span></span> | <span data-ttu-id="fc806-143">是</span><span class="sxs-lookup"><span data-stu-id="fc806-143">Yes</span></span> |
| [<span data-ttu-id="fc806-144">webapp</span><span class="sxs-lookup"><span data-stu-id="fc806-144">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="fc806-145">0.2.0</span><span class="sxs-lookup"><span data-stu-id="fc806-145">0.2.0</span></span> | <span data-ttu-id="fc806-146">创建和部署应用服务资源。</span><span class="sxs-lookup"><span data-stu-id="fc806-146">Create and deploy appservice resources.</span></span> | <span data-ttu-id="fc806-147">是</span><span class="sxs-lookup"><span data-stu-id="fc806-147">Yes</span></span> |
