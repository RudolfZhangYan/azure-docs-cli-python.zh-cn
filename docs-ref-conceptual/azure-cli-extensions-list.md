---
title: Azure CLI 2.0 的可用扩展
description: 官方支持的 Azure CLI 2.0 扩展的完整列表。
author: derekbekoe
ms.author: debekoe
manager: routlaw
ms.date: 04/25/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: f22565e4b9bb4fe0656aae90724bf124611ef3c8
ms.sourcegitcommit: 2836d0739f55ba06cbc7c556fdf3e698a3fd1e4e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/26/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="2bc7b-103">Azure CLI 2.0 的可用扩展</span><span class="sxs-lookup"><span data-stu-id="2bc7b-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="2bc7b-104">本文是 Microsoft 提供并支持的 Azure CLI 2.0 可用扩展的完整列表。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="2bc7b-105">也可以直接从 CLI 获得该扩展列表。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="2bc7b-106">若要获取该列表，请运行 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available)：</span><span class="sxs-lookup"><span data-stu-id="2bc7b-106">To get it, run [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="2bc7b-107">名称</span><span class="sxs-lookup"><span data-stu-id="2bc7b-107">Name</span></span> | <span data-ttu-id="2bc7b-108">版本</span><span class="sxs-lookup"><span data-stu-id="2bc7b-108">Version</span></span> | <span data-ttu-id="2bc7b-109">摘要</span><span class="sxs-lookup"><span data-stu-id="2bc7b-109">Summary</span></span> | <span data-ttu-id="2bc7b-110">预览</span><span class="sxs-lookup"><span data-stu-id="2bc7b-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="2bc7b-111">aem</span><span class="sxs-lookup"><span data-stu-id="2bc7b-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-112">0.1.1</span><span class="sxs-lookup"><span data-stu-id="2bc7b-112">0.1.1</span></span> | <span data-ttu-id="2bc7b-113">管理适用于 SAP 的 Azure 增强型监视扩展</span><span class="sxs-lookup"><span data-stu-id="2bc7b-113">Manage Azure Enhanced Monitoring Extensions for SAP</span></span> |  |
| [<span data-ttu-id="2bc7b-114">alias</span><span class="sxs-lookup"><span data-stu-id="2bc7b-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-115">0.5.1</span><span class="sxs-lookup"><span data-stu-id="2bc7b-115">0.5.1</span></span> | <span data-ttu-id="2bc7b-116">支持命令别名</span><span class="sxs-lookup"><span data-stu-id="2bc7b-116">Support for command aliases</span></span> | <span data-ttu-id="2bc7b-117">是</span><span class="sxs-lookup"><span data-stu-id="2bc7b-117">Yes</span></span> |
| [<span data-ttu-id="2bc7b-118">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="2bc7b-118">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="2bc7b-119">2.2.1</span><span class="sxs-lookup"><span data-stu-id="2bc7b-119">2.2.1</span></span> | <span data-ttu-id="2bc7b-120">用于操作 Azure Batch 服务的其他命令</span><span class="sxs-lookup"><span data-stu-id="2bc7b-120">Additional commands for working with Azure Batch service</span></span> |  |
| [<span data-ttu-id="2bc7b-121">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="2bc7b-121">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="2bc7b-122">0.4.3</span><span class="sxs-lookup"><span data-stu-id="2bc7b-122">0.4.3</span></span> | <span data-ttu-id="2bc7b-123">为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层</span><span class="sxs-lookup"><span data-stu-id="2bc7b-123">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service</span></span> |  |
| [<span data-ttu-id="2bc7b-124">dns</span><span class="sxs-lookup"><span data-stu-id="2bc7b-124">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-125">0.0.2</span><span class="sxs-lookup"><span data-stu-id="2bc7b-125">0.0.2</span></span> | <span data-ttu-id="2bc7b-126">适用于 DNS 区域的 Azure CLI 扩展</span><span class="sxs-lookup"><span data-stu-id="2bc7b-126">An Azure CLI Extension for DNS zones</span></span> |  |
| [<span data-ttu-id="2bc7b-127">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="2bc7b-127">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-128">0.0.5</span><span class="sxs-lookup"><span data-stu-id="2bc7b-128">0.0.5</span></span> | <span data-ttu-id="2bc7b-129">用于在不同区域之间复制映像的 Azure CLI 扩展。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-129">An Azure CLI Extension that copies images from region to region.</span></span> |  |
| [<span data-ttu-id="2bc7b-130">managementgroups</span><span class="sxs-lookup"><span data-stu-id="2bc7b-130">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-131">0.1.0</span><span class="sxs-lookup"><span data-stu-id="2bc7b-131">0.1.0</span></span> | <span data-ttu-id="2bc7b-132">适用于管理组的 Azure CLI 扩展</span><span class="sxs-lookup"><span data-stu-id="2bc7b-132">An Azure CLI Extension for Management Groups</span></span> |  |
| [<span data-ttu-id="2bc7b-133">managementpartner</span><span class="sxs-lookup"><span data-stu-id="2bc7b-133">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-134">0.1.2</span><span class="sxs-lookup"><span data-stu-id="2bc7b-134">0.1.2</span></span> | <span data-ttu-id="2bc7b-135">支持“管理合作伙伴”预览版</span><span class="sxs-lookup"><span data-stu-id="2bc7b-135">Support for Management Partner preview</span></span> |  |
| [<span data-ttu-id="2bc7b-136">rdbms</span><span class="sxs-lookup"><span data-stu-id="2bc7b-136">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-137">0.0.5</span><span class="sxs-lookup"><span data-stu-id="2bc7b-137">0.0.5</span></span> | <span data-ttu-id="2bc7b-138">提供 Azure MySQL 和 Azure PostgreSQL 支持的 Azure CLI 扩展。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-138">An Azure CLI Extension providing support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="2bc7b-139">signalr</span><span class="sxs-lookup"><span data-stu-id="2bc7b-139">signalr</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-140">0.1.0</span><span class="sxs-lookup"><span data-stu-id="2bc7b-140">0.1.0</span></span> | <span data-ttu-id="2bc7b-141">支持 signalr 管理预览版。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-141">Support for signalr management preview.</span></span> | <span data-ttu-id="2bc7b-142">是</span><span class="sxs-lookup"><span data-stu-id="2bc7b-142">Yes</span></span> |
| [<span data-ttu-id="2bc7b-143">subscription</span><span class="sxs-lookup"><span data-stu-id="2bc7b-143">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-144">0.1.1</span><span class="sxs-lookup"><span data-stu-id="2bc7b-144">0.1.1</span></span> | <span data-ttu-id="2bc7b-145">支持订阅管理预览版。</span><span class="sxs-lookup"><span data-stu-id="2bc7b-145">Support for subscription management preview.</span></span> |  |
| [<span data-ttu-id="2bc7b-146">webapp</span><span class="sxs-lookup"><span data-stu-id="2bc7b-146">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="2bc7b-147">0.2.1</span><span class="sxs-lookup"><span data-stu-id="2bc7b-147">0.2.1</span></span> | <span data-ttu-id="2bc7b-148">用于管理应用服务资源的 Azure CLI 扩展</span><span class="sxs-lookup"><span data-stu-id="2bc7b-148">An Azure CLI Extension to manage appservice resources</span></span> | <span data-ttu-id="2bc7b-149">是</span><span class="sxs-lookup"><span data-stu-id="2bc7b-149">Yes</span></span> |
