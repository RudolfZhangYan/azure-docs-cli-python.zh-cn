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
ms.openlocfilehash: 23c743210ccc506935f6e78489ca0df2b99d46a1
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/05/2017
---
# <a name="using-jmespath-queries-with-azure-cli-20"></a>在 Azure CLI 2.0 中使用 JMESPath 查询

Azure CLI 2.0 使用 `--query` 参数针对 `az` 命令的结果执行 [JMESPath 查询](http://jmespath.org)。 JMESPath 是适用于 JSON 输出的强大查询语言。  如果你不熟悉 JMESPath 查询，可以在 [JMESPath.org/tutorial](http:/JMESPath.org/tutorial.html) 中找到教程。

Azure CLI 2.0 中的每种资源类型（容器服务、Web 应用、VM 等）都支持 `Query` 参数，可将该参数用于各种不同的目的。  下面列出了几个示例。

## <a name="selecting-simple-properties"></a>选择简单属性

采用 `table` 输出格式的简单 `list` 命令以易于阅读的表格格式返回每种资源类型的一组最常见的、组织有序的简单属性。

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

使用 `--query` 参数可以仅显示订阅中所有虚拟机的资源组名称和 VM 名称。

```azurecli-interactive
az vm list \
  --query [*].[name,resourceGroup] --out table
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

在前面的示例中，可以看到列标题为“Column1”和“Column2”。  还可以将友好的标签或名称添加到所选的属性。  在以下示例中，我们已将标签“VMName”和“RGName”添加到所选的属性“name”和“resourceGroup”。


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

## <a name="selecting-complex-nested-properties"></a>选择复杂的嵌套属性

如果要选择的属性嵌套在 JSON 输出中的深层位置，则你需要提供该嵌套属性的完整路径。 以下示例演示如何通过 vm list 命令选择 VM 名称和 OS 类型。

```azurecli-interactive
az vm list \
  --query "[].{VMName:name,OSType:storageProfile.osDisk.osType}" --out table
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

## <a name="filter-with-the-contains-function"></a>使用 contains 函数进行筛选

可以使用 JMESPath `contains` 函数来细化查询中返回的结果。
在以下示例中，命令仅选择名称中包含文本“RGD”的 VM。  

```azurecli-interactive
az vm list \
  --query "[?contains(resourceGroup,'RGD')].{ resource: resourceGroup, name: name }" --out table
```

```
Resource    VMName
----------  -----------
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

在下一个示例中，结果将返回 vmSize 为“Standard_DS1”的 VM。

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

## <a name="filter-with-grep"></a>使用 grep 进行筛选

`tsv` 输出格式是不带标题的制表符分隔文本。 可将它传递给 `grep` 和 `cut` 等命令，以进一步分析 `list` 输出中的特定值。 在以下示例中，`grep` 命令仅选择名称中包含文本“RGD”的 VM。  `cut` 命令仅选择在输出中显示第 8 个字段值（制表符分隔）。

```azurecli-interactive
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="explore-with-jpterm"></a>使用 jpterm 进行浏览

还可以将命令输出传递给 [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal)，然后在该位置体验 JMESPath 查询。

```bash
pip install jmespath-terminal
az vm list | jpterm
```

