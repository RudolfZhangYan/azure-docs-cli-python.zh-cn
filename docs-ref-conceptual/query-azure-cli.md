---
title: "使用 Azure CLI 2.0 查询命令结果"
description: "了解如何针对 Azure CLI 2.0 命令的输出执行 JMESPath 查询。"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 98bc35c1e8136231011a2303901f42c68c9a7758
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2018
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="8b917-103">在 Azure CLI 2.0 中使用 JMESPath 查询</span><span class="sxs-lookup"><span data-stu-id="8b917-103">Use JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="8b917-104">Azure CLI 2.0 使用 `--query` 参数针对 `az` 命令的结果执行 [JMESPath 查询](http://jmespath.org)。</span><span class="sxs-lookup"><span data-stu-id="8b917-104">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="8b917-105">JMESPath 是适用于 JSON 输出的强大查询语言。</span><span class="sxs-lookup"><span data-stu-id="8b917-105">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="8b917-106">如果不熟悉 JMESPath 查询，可以在 [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html) 中找到教程。</span><span class="sxs-lookup"><span data-stu-id="8b917-106">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="8b917-107">Azure CLI 2.0 中的每种资源类型（容器服务、Web 应用、VM 等）都支持 `Query` 参数，可将该参数用于各种不同的目的。</span><span class="sxs-lookup"><span data-stu-id="8b917-107">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="8b917-108">下面列出了几个示例。</span><span class="sxs-lookup"><span data-stu-id="8b917-108">We have listed several examples below.</span></span>

## <a name="select-simple-properties"></a><span data-ttu-id="8b917-109">选择简单属性</span><span class="sxs-lookup"><span data-stu-id="8b917-109">Select simple properties</span></span>

<span data-ttu-id="8b917-110">采用 `table` 输出格式的简单 `list` 命令以易于阅读的表格格式返回每种资源类型的一组最常见的、组织有序的简单属性。</span><span class="sxs-lookup"><span data-stu-id="8b917-110">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

```azurecli-interactive
az vm list --out table
```

```
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

<span data-ttu-id="8b917-111">使用 `--query` 参数可以仅显示订阅中所有虚拟机的资源组名称和 VM 名称。</span><span class="sxs-lookup"><span data-stu-id="8b917-111">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

```azurecli-interactive
az vm list \
  --query "[].[name, resourceGroup]" --out table
```

```
Column1     Column2
---------   -----------
DemoVM010   DEMORG1
demovm111   DEMORG1
demovm211   DEMORG1
demovm212   DEMORG1
demovm213   DEMORG1
demovm214   DEMORG1
demovm222   DEMORG1
KBDemo001VM RGDEMO001
KBDemo020   RGDEMO001
```

<span data-ttu-id="8b917-112">在前面的示例中，可以看到列标题为“Column1”和“Column2”。</span><span class="sxs-lookup"><span data-stu-id="8b917-112">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="8b917-113">还可以将友好的标签或名称添加到所选的属性。</span><span class="sxs-lookup"><span data-stu-id="8b917-113">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="8b917-114">在以下示例中，我们已将标签“VMName”和“RGName”添加到所选的属性“name”和“resourceGroup”。</span><span class="sxs-lookup"><span data-stu-id="8b917-114">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


```azurecli-interactive
az vm list \
  --query "[].{RGName:resourceGroup, VMName:name}" --out table
```

```
RGName     VMName
---------  -----------
DEMORG1    DemoVM010
DEMORG1    demovm111
DEMORG1    demovm211
DEMORG1    demovm212
DEMORG1    demovm213
DEMORG1    demovm214
DEMORG1    demovm222
RGDEMO001  KBDemo001VM
RGDEMO001  KBDemo020
```

## <a name="select-complex-nested-properties"></a><span data-ttu-id="8b917-115">选择复杂的嵌套属性</span><span class="sxs-lookup"><span data-stu-id="8b917-115">Select complex nested properties</span></span>

<span data-ttu-id="8b917-116">如果要选择的属性嵌套在 JSON 输出中的深层位置，则需要提供该嵌套属性的完整路径。</span><span class="sxs-lookup"><span data-stu-id="8b917-116">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="8b917-117">以下示例演示如何通过 vm list 命令选择 VM 名称和 OS 类型。</span><span class="sxs-lookup"><span data-stu-id="8b917-117">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

```azurecli-interactive
az vm list \
  --query "[].{VMName:name, OSType:storageProfile.osDisk.osType}" --out table
```

```
VMName       OSType
-----------  --------
DemoVM010    Linux
demovm111    Linux
demovm211    Linux
demovm212    Linux
demovm213    Linux
demovm214    Linux
demovm222    Linux
KBDemo001VM  Linux
KBDemo020    Linux
```

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="8b917-118">使用 contains 函数进行筛选</span><span class="sxs-lookup"><span data-stu-id="8b917-118">Filter with the contains function</span></span>

<span data-ttu-id="8b917-119">可以使用 JMESPath `contains` 函数来细化查询中返回的结果。</span><span class="sxs-lookup"><span data-stu-id="8b917-119">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="8b917-120">在以下示例中，命令仅选择名称中包含文本“RGD”的 VM。</span><span class="sxs-lookup"><span data-stu-id="8b917-120">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>

```azurecli-interactive
az vm list \
  --query "[?contains(resourceGroup, 'RGD')].{ resource: resourceGroup, name: name }" --out table
```

```
Resource    VMName
----------  -----------
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

<span data-ttu-id="8b917-121">在下一个示例中，结果将返回 vmSize 为“Standard_DS1”的 VM。</span><span class="sxs-lookup"><span data-stu-id="8b917-121">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

```azurecli-interactive
az vm list \
  --query "[?contains(hardwareProfile.vmSize, 'Standard_DS1')]" --out table
```

```
ResourceGroup    VMName     VmId                                  Location    ProvisioningState
---------------  ---------  ------------------------------------  ----------  -------------------
DEMORG1          DemoVM010  cbd56d9b-9340-44bc-a722-25f15b578444  westus      Succeeded
DEMORG1          demovm111  c1c024eb-3837-4075-9117-bfbc212fa7da  westus      Succeeded
DEMORG1          demovm211  95eda642-417f-4036-9475-67246ac0f0d0  westus      Succeeded
DEMORG1          demovm212  4bdac85d-c2f7-410f-9907-ca7921d930b4  westus      Succeeded
DEMORG1          demovm213  2131c664-221a-4b7f-9653-f6d542fbfa34  westus      Succeeded
DEMORG1          demovm214  48f419af-d27a-4df0-87f3-9481007c2e5a  westus      Succeeded
DEMORG1          demovm222  e0f59516-1d69-4d54-b8a2-f6c4a5d031de  westus      Succeeded
```

## <a name="filter-with-grep"></a><span data-ttu-id="8b917-122">使用 grep 进行筛选</span><span class="sxs-lookup"><span data-stu-id="8b917-122">Filter with grep</span></span>

<span data-ttu-id="8b917-123">`tsv` 输出格式是不带标题的制表符分隔文本。</span><span class="sxs-lookup"><span data-stu-id="8b917-123">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="8b917-124">可将它传递给 `grep` 和 `cut` 等命令，以进一步分析 `list` 输出中的特定值。</span><span class="sxs-lookup"><span data-stu-id="8b917-124">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="8b917-125">在以下示例中，`grep` 命令仅选择名称中包含文本“RGD”的 VM。</span><span class="sxs-lookup"><span data-stu-id="8b917-125">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="8b917-126">`cut` 命令仅选择在输出中显示第 8 个字段值（制表符分隔）。</span><span class="sxs-lookup"><span data-stu-id="8b917-126">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="8b917-127">使用 jpterm 进行浏览</span><span class="sxs-lookup"><span data-stu-id="8b917-127">Explore with jpterm</span></span>

<span data-ttu-id="8b917-128">还可以将命令输出传递给 [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal)，然后在该位置体验 JMESPath 查询。</span><span class="sxs-lookup"><span data-stu-id="8b917-128">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

