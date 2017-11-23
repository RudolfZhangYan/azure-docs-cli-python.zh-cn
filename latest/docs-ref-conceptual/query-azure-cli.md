---
title: "使用 Azure CLI 2.0 查询命令结果"
description: "使用 --query 针对 Azure CLI 2.0 命令的输出执行 JMESPath 查询。"
keywords: "Azure CLI 2.0, JMESPath, 查询, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 5979acc5-21a5-41e2-a4b6-3183bfe6aa22
ms.openlocfilehash: 8ab4a5e38f06199c5f044b8526c581828ba61927
ms.sourcegitcommit: 0149f195a0d9f0ea9b7ff5c6e00ad4242223a1a8
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/18/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="b40c8-104">在 Azure CLI 2.0 中使用 JMESPath 查询</span><span class="sxs-lookup"><span data-stu-id="b40c8-104">Using JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="b40c8-105">Azure CLI 2.0 使用 `--query` 参数针对 `az` 命令的结果执行 [JMESPath 查询](http://jmespath.org)。</span><span class="sxs-lookup"><span data-stu-id="b40c8-105">The Azure CLI 2.0 uses the `--query` parameter to execute a [JMESPath query](http://jmespath.org) on the results of your `az` command.</span></span> <span data-ttu-id="b40c8-106">JMESPath 是适用于 JSON 输出的强大查询语言。</span><span class="sxs-lookup"><span data-stu-id="b40c8-106">JMESPath is a powerful query language for JSON outputs.</span></span>  <span data-ttu-id="b40c8-107">如果不熟悉 JMESPath 查询，可以在 [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html) 中找到教程。</span><span class="sxs-lookup"><span data-stu-id="b40c8-107">If you are unfamiliar with JMESPath queries you can find a tutorial at [JMESPath.org/tutorial](http://JMESPath.org/tutorial.html).</span></span>

<span data-ttu-id="b40c8-108">Azure CLI 2.0 中的每种资源类型（容器服务、Web 应用、VM 等）都支持 `Query` 参数，可将该参数用于各种不同的目的。</span><span class="sxs-lookup"><span data-stu-id="b40c8-108">`Query` parameter is supported by every resource type (Container Services, Web Apps, VM, etc.) within Azure CLI 2.0 and can be used for various different purposes.</span></span>  <span data-ttu-id="b40c8-109">下面列出了几个示例。</span><span class="sxs-lookup"><span data-stu-id="b40c8-109">We have listed several examples below.</span></span>

## <a name="selecting-simple-properties"></a><span data-ttu-id="b40c8-110">选择简单属性</span><span class="sxs-lookup"><span data-stu-id="b40c8-110">Selecting simple properties</span></span>

<span data-ttu-id="b40c8-111">采用 `table` 输出格式的简单 `list` 命令以易于阅读的表格格式返回每种资源类型的一组最常见的、组织有序的简单属性。</span><span class="sxs-lookup"><span data-stu-id="b40c8-111">The simple `list` command with `table` output format returns a curated set of most common, simple properties for each resource type in an easy-to-read tabular format.</span></span>

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

<span data-ttu-id="b40c8-112">使用 `--query` 参数可以仅显示订阅中所有虚拟机的资源组名称和 VM 名称。</span><span class="sxs-lookup"><span data-stu-id="b40c8-112">You can use the `--query` parameter to show just the Resource Group name and VM name for all virtual machines in your subscription.</span></span>

```azurecli-interactive
az vm list \
  --query [*].[name, resourceGroup] --out table
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

<span data-ttu-id="b40c8-113">在前面的示例中，可以看到列标题为“Column1”和“Column2”。</span><span class="sxs-lookup"><span data-stu-id="b40c8-113">In the previous example, you notice that the column headings are "Column1" and "Column2".</span></span>  <span data-ttu-id="b40c8-114">还可以将友好的标签或名称添加到所选的属性。</span><span class="sxs-lookup"><span data-stu-id="b40c8-114">You can add friendly labels or names to the properties you select, as well.</span></span>  <span data-ttu-id="b40c8-115">在以下示例中，我们已将标签“VMName”和“RGName”添加到所选的属性“name”和“resourceGroup”。</span><span class="sxs-lookup"><span data-stu-id="b40c8-115">In the following example, we added the labels "VMName" and "RGName" to the selected properties "name" and "resourceGroup".</span></span>


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

## <a name="selecting-complex-nested-properties"></a><span data-ttu-id="b40c8-116">选择复杂的嵌套属性</span><span class="sxs-lookup"><span data-stu-id="b40c8-116">Selecting complex nested properties</span></span>

<span data-ttu-id="b40c8-117">如果要选择的属性嵌套在 JSON 输出中的深层位置，则需要提供该嵌套属性的完整路径。</span><span class="sxs-lookup"><span data-stu-id="b40c8-117">If the property you want to select is nested deep in the JSON output you need to supply the full path to that nested property.</span></span> <span data-ttu-id="b40c8-118">以下示例演示如何通过 vm list 命令选择 VM 名称和 OS 类型。</span><span class="sxs-lookup"><span data-stu-id="b40c8-118">The following example shows how to select the VMName and the OS type from the vm list command.</span></span>

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

## <a name="filter-with-the-contains-function"></a><span data-ttu-id="b40c8-119">使用 contains 函数进行筛选</span><span class="sxs-lookup"><span data-stu-id="b40c8-119">Filter with the contains function</span></span>

<span data-ttu-id="b40c8-120">可以使用 JMESPath `contains` 函数来细化查询中返回的结果。</span><span class="sxs-lookup"><span data-stu-id="b40c8-120">You can use the JMESPath `contains` function to refine your results returned in the query.</span></span>
<span data-ttu-id="b40c8-121">在以下示例中，命令仅选择名称中包含文本“RGD”的 VM。</span><span class="sxs-lookup"><span data-stu-id="b40c8-121">In the following example, the command selects only VMs that have the text "RGD" in their name.</span></span>  

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

<span data-ttu-id="b40c8-122">在下一个示例中，结果将返回 vmSize 为“Standard_DS1”的 VM。</span><span class="sxs-lookup"><span data-stu-id="b40c8-122">With the next example, the results will return the VMs that have the vmSize 'Standard_DS1'.</span></span>

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

## <a name="filter-with-grep"></a><span data-ttu-id="b40c8-123">使用 grep 进行筛选</span><span class="sxs-lookup"><span data-stu-id="b40c8-123">Filter with grep</span></span>

<span data-ttu-id="b40c8-124">`tsv` 输出格式是不带标题的制表符分隔文本。</span><span class="sxs-lookup"><span data-stu-id="b40c8-124">The `tsv` output format is a tab-separated text with no headers.</span></span> <span data-ttu-id="b40c8-125">可将它传递给 `grep` 和 `cut` 等命令，以进一步分析 `list` 输出中的特定值。</span><span class="sxs-lookup"><span data-stu-id="b40c8-125">It can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="b40c8-126">在以下示例中，`grep` 命令仅选择名称中包含文本“RGD”的 VM。</span><span class="sxs-lookup"><span data-stu-id="b40c8-126">In the following example, the `grep` command selects only VMs that have text "RGD" in their name.</span></span>  <span data-ttu-id="b40c8-127">`cut` 命令仅选择在输出中显示第 8 个字段值（制表符分隔）。</span><span class="sxs-lookup"><span data-stu-id="b40c8-127">The `cut` command selects only the 8th field (separated by tabs) value to show in the output.</span></span>

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a><span data-ttu-id="b40c8-128">使用 jpterm 进行浏览</span><span class="sxs-lookup"><span data-stu-id="b40c8-128">Explore with jpterm</span></span>

<span data-ttu-id="b40c8-129">还可以将命令输出传递给 [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal)，然后在该位置体验 JMESPath 查询。</span><span class="sxs-lookup"><span data-stu-id="b40c8-129">You can also pipe the command output to [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) and experiment with your JMESPath query there.</span></span>

```bash
pip install jmespath-terminal
az vm list | jpterm
```

