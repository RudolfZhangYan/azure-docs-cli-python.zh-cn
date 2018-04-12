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
ms.openlocfilehash: 794ea005816b33fe78ca6c15b86dcf94ace3eaa8
ms.sourcegitcommit: c9da729f4a42a839f13106f7589deaa0ca19cc4e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2018
---
# <a name="available-extensions-for-the-azure-cli-20"></a><span data-ttu-id="1c89f-103">Azure CLI 2.0 的可用扩展</span><span class="sxs-lookup"><span data-stu-id="1c89f-103">Available extensions for the Azure CLI 2.0</span></span>

<span data-ttu-id="1c89f-104">本文是 Microsoft 提供并支持的 Azure CLI 2.0 可用扩展的完整列表。</span><span class="sxs-lookup"><span data-stu-id="1c89f-104">This article is a complete list of the available extensions for the Azure CLI 2.0 which are offered and supported by Microsoft.</span></span>

<span data-ttu-id="1c89f-105">也可以直接从 CLI 获得该扩展列表。</span><span class="sxs-lookup"><span data-stu-id="1c89f-105">The list of extensions is also available directly from the CLI.</span></span> <span data-ttu-id="1c89f-106">若要获取该列表，请运行 [az extension list-available](/cli/azure/extension#az-extension-list-available)：</span><span class="sxs-lookup"><span data-stu-id="1c89f-106">To get it, run [az extension list-available](/cli/azure/extension#az-extension-list-available):</span></span>

```azurecli
az extension list-available --output table
```

| <span data-ttu-id="1c89f-107">名称</span><span class="sxs-lookup"><span data-stu-id="1c89f-107">Name</span></span> | <span data-ttu-id="1c89f-108">版本</span><span class="sxs-lookup"><span data-stu-id="1c89f-108">Version</span></span> | <span data-ttu-id="1c89f-109">摘要</span><span class="sxs-lookup"><span data-stu-id="1c89f-109">Summary</span></span> | <span data-ttu-id="1c89f-110">预览</span><span class="sxs-lookup"><span data-stu-id="1c89f-110">Preview</span></span> |
|------|---------|---------|---------|
| [<span data-ttu-id="1c89f-111">aem</span><span class="sxs-lookup"><span data-stu-id="1c89f-111">aem</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-112">0.1.1</span><span class="sxs-lookup"><span data-stu-id="1c89f-112">0.1.1</span></span> | <span data-ttu-id="1c89f-113">管理适用于 SAP 的 Azure 增强型监视扩展。</span><span class="sxs-lookup"><span data-stu-id="1c89f-113">Manage Azure Enhanced Monitoring Extensions for SAP.</span></span> |  |
| [<span data-ttu-id="1c89f-114">alias</span><span class="sxs-lookup"><span data-stu-id="1c89f-114">alias</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-115">0.3.0</span><span class="sxs-lookup"><span data-stu-id="1c89f-115">0.3.0</span></span> | <span data-ttu-id="1c89f-116">对命令别名的支持。</span><span class="sxs-lookup"><span data-stu-id="1c89f-116">Support for command aliases.</span></span> | <span data-ttu-id="1c89f-117">是</span><span class="sxs-lookup"><span data-stu-id="1c89f-117">Yes</span></span> |
| [<span data-ttu-id="1c89f-118">azure-batch-cli-extensions</span><span class="sxs-lookup"><span data-stu-id="1c89f-118">azure-batch-cli-extensions</span></span>](https://github.com/Azure/azure-batch-cli-extensions) | <span data-ttu-id="1c89f-119">2.1.0</span><span class="sxs-lookup"><span data-stu-id="1c89f-119">2.1.0</span></span> | <span data-ttu-id="1c89f-120">附加的预览版 Azure Batch 命令。</span><span class="sxs-lookup"><span data-stu-id="1c89f-120">Additional preview Azure Batch commands.</span></span> |  |
| [<span data-ttu-id="1c89f-121">azure-cli-iot-ext</span><span class="sxs-lookup"><span data-stu-id="1c89f-121">azure-cli-iot-ext</span></span>](https://github.com/azure/azure-iot-cli-extension) | <span data-ttu-id="1c89f-122">0.4.1</span><span class="sxs-lookup"><span data-stu-id="1c89f-122">0.4.1</span></span> | <span data-ttu-id="1c89f-123">为 Azure IoT 中心、IoT Edge 和 IoT 设备预配服务提供数据平面命令层。</span><span class="sxs-lookup"><span data-stu-id="1c89f-123">Provides the data plane command layer for Azure IoT Hub, IoT Edge and IoT Device Provisioning Service.</span></span> |  |
| [<span data-ttu-id="1c89f-124">dns</span><span class="sxs-lookup"><span data-stu-id="1c89f-124">dns</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-125">0.0.2</span><span class="sxs-lookup"><span data-stu-id="1c89f-125">0.0.2</span></span> | <span data-ttu-id="1c89f-126">对 Azure 专用 DNS 公共预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="1c89f-126">Support for the Azure Private DNS Public Preview.</span></span> |  |
| [<span data-ttu-id="1c89f-127">image-copy-extension</span><span class="sxs-lookup"><span data-stu-id="1c89f-127">image-copy-extension</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-128">0.0.5</span><span class="sxs-lookup"><span data-stu-id="1c89f-128">0.0.5</span></span> | <span data-ttu-id="1c89f-129">将映像从一个区域复制到另一个区域。</span><span class="sxs-lookup"><span data-stu-id="1c89f-129">Copy images from region to region.</span></span> |  |
| [<span data-ttu-id="1c89f-130">managementgroups</span><span class="sxs-lookup"><span data-stu-id="1c89f-130">managementgroups</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-131">0.1.0</span><span class="sxs-lookup"><span data-stu-id="1c89f-131">0.1.0</span></span> | <span data-ttu-id="1c89f-132">对“管理组”预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="1c89f-132">Support for Management Groups preview.</span></span> | <span data-ttu-id="1c89f-133">是</span><span class="sxs-lookup"><span data-stu-id="1c89f-133">Yes</span></span> |
| [<span data-ttu-id="1c89f-134">managementpartner</span><span class="sxs-lookup"><span data-stu-id="1c89f-134">managementpartner</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-135">0.1.2</span><span class="sxs-lookup"><span data-stu-id="1c89f-135">0.1.2</span></span> | <span data-ttu-id="1c89f-136">对“管理合作伙伴”预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="1c89f-136">Support for Management Partner preview.</span></span> | <span data-ttu-id="1c89f-137">是</span><span class="sxs-lookup"><span data-stu-id="1c89f-137">Yes</span></span> |
| [<span data-ttu-id="1c89f-138">rdbms</span><span class="sxs-lookup"><span data-stu-id="1c89f-138">rdbms</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-139">0.0.5</span><span class="sxs-lookup"><span data-stu-id="1c89f-139">0.0.5</span></span> | <span data-ttu-id="1c89f-140">对 Azure MySQL 和 Azure PostgreSQL 的支持。</span><span class="sxs-lookup"><span data-stu-id="1c89f-140">Support for Azure MySQL and Azure PostgreSQL.</span></span> |  |
| [<span data-ttu-id="1c89f-141">subscription</span><span class="sxs-lookup"><span data-stu-id="1c89f-141">subscription</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-142">0.1.1</span><span class="sxs-lookup"><span data-stu-id="1c89f-142">0.1.1</span></span> | <span data-ttu-id="1c89f-143">对订阅定义预览版的支持。</span><span class="sxs-lookup"><span data-stu-id="1c89f-143">Support for subscription definitions preview.</span></span> | <span data-ttu-id="1c89f-144">是</span><span class="sxs-lookup"><span data-stu-id="1c89f-144">Yes</span></span> |
| [<span data-ttu-id="1c89f-145">webapp</span><span class="sxs-lookup"><span data-stu-id="1c89f-145">webapp</span></span>](https://github.com/Azure/azure-cli-extensions) | <span data-ttu-id="1c89f-146">0.2.0</span><span class="sxs-lookup"><span data-stu-id="1c89f-146">0.2.0</span></span> | <span data-ttu-id="1c89f-147">创建和部署应用服务资源。</span><span class="sxs-lookup"><span data-stu-id="1c89f-147">Create and deploy appservice resources.</span></span> | <span data-ttu-id="1c89f-148">是</span><span class="sxs-lookup"><span data-stu-id="1c89f-148">Yes</span></span> |
