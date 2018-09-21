---
title: 使用 Azure CLI 2.0 查询命令结果
description: 了解如何针对 Azure CLI 2.0 命令的输出执行 JMESPath 查询。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 55880b87e1bffc37bbdeaeb84206deb5b9b7b227
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388365"
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a>在 Azure CLI 2.0 中使用 JMESPath 查询

Azure CLI 2.0 使用 `--query` 参数针对命令的结果执行 [JMESPath 查询](http://jmespath.org)。 JMESPath 是用于 JSON 的查询语言，提供从 CLI 输出中选择和显示数据的能力。 先针对 JSON 输出执行这些查询，然后再针对任何显示格式执行。

Azure CLI 中的所有命令均支持 `--query` 参数。 本文中的示例涵盖了常见用例，并演示了如何使用 JMESPath 的功能。

## <a name="work-with-dictionary-output"></a>使用字典输出

返回 JSON 字典的命令可以单独按其键名称查阅。 键路径使用 `.` 字符作为分隔符。 下面的示例拉取允许连接到 Linux VM 的公共 SSH 密钥列表：

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

多个值可放入有序数组。 下面的示例演示如何检索 Azure 映像产品名称和 OS 磁盘大小：

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

如果希望输出中有键，可以使用另一种字典语法。  将元素选择到一个字典时使用格式 `{displayKey:keyPath, ...}` 来针对 `keyPath` JMESPath 表达式进行筛选。 在输出值中，键/值对将更改为 `{displayKey: value}`。 下一个示例采用上一个示例的查询，并通过将键指定到输出来使输出更加清晰：

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

以 `table` 输出格式显示信息时，字典显示允许设置你自己的列标题。 有关输出格式的详细信息，请参阅 [Azure CLI 2.0 命令的输出格式](/cli/azure/format-output-azure-cli)。

> [!NOTE]
> 某些键已筛选掉，未在表视图中输出。 这些键为 `id`、`type` 和 `etag`。 如果需要查看此信息，可以更改键名称并避免筛选。
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a>使用列表输出

可能会返回多个值的 CLI 命令将返回一个数组。 数组元素可按索引访问，不一定每次都按相同的顺序返回。 可以一次性查询所有数组元素，只需使用 `[]` 运算符将其平展即可。 该运算符放在数组的后面，或者用作表达式中的第一个元素。 平展某个数组会针对该数组的每个元素运行该运算符后面的查询。

以下示例输出资源组中每个 VM 的名称以及其上运行的 OS。

```azurecli-interactive
az vm list -g QueryDemo --query '[].{name:name, image:storageProfile.imageReference.offer}'
```

```json
[
  {
    "image": "CentOS",
    "name": "CentBox"
  },
  {
    "image": "openSUSE-Leap",
    "name": "SUSEBox"
  },
  {
    "image": "UbuntuServer",
    "name": "TestVM"
  },
  {
    "image": "UbuntuServer",
    "name": "Test2"
  },
  {
    "image": "WindowsServer",
    "name": "WinServ"
  }
]
```

作为键路径一部分的数组也可以平展。 以下查询获取 VM 连接到的 NIC 的 Azure 对象 ID。

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a>使用谓词筛选数组输出

JMESPath 提供[筛选表达式](http://jmespath.org/specification.html#filterexpressions)以筛选显示的数据。 这些表达式功能强大，尤其是在与 [JMESPath 内置函数](http://jmespath.org/specification.html#built-in-functions)结合使用以执行部分匹配或将数据处理为标准格式时。 筛选表达式只适用于数组数据，在任何其他情况下使用时将返回 `null` 值。 例如，可以采用 `vm list` 等命令的输出，并针对其进行筛选，以查找特定类型的 VM。 以下示例通过筛选 VM 类型以仅捕获 Windows VM 并打印其名称，在前一个示例的基础上进行了扩展。

```azurecli-interactive
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a>以交互方式试验查询

[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python 包提供了用于体验查询的交互式环境，帮助你开始学习 JMESPath。 数据作为输入通过管道传送，然后将编写并编辑程序内部查询以提取数据。

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
