---
title: "Azure CLI 2.0 的输出格式"
description: "使用 --output 可将 Azure CLI 2.0 命令的输出格式设置为表、列表或 json。"
keywords: "Azure CLI 2.0, 输出, 格式, 表, 列表, json, Linux, Mac, Windows, OS X"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 74bdb727-481d-45f7-a44e-15d18dc55483
ms.openlocfilehash: 3e99c2533031dc063a50996f26712d4df92f65c9
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2018
---
# <a name="output-formats-for-azure-cli-20-commands"></a>Azure CLI 2.0 命令的输出格式

Azure CLI 2.0 使用 json 作为默认输出选项，但允许通过多种方法设置任何命令的输出。  使用 `--output`（或者 `--out` 或 `-o`）参数可将命令的输出格式设置为下表中所述的输出类型之一。

--output | 说明
---------|-------------------------------
`json`   | json 字符串。 `json` 为默认值。
`jsonc`  | 彩色 json 字符串。
`table`  | 包含列标题的表。
`tsv`    | 制表符分隔值。

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a>使用 json 选项

以下示例以默认 json 格式显示订阅中的虚拟机列表。

```azurecli-interactive
az vm list --output json
```

结果会采用此格式（为简洁起见，仅显示部分输出）。

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "demorg1"
        }
      ]
    },
          ...
          ...
          ...
]
```

## <a name="using-the-table-option"></a>使用 table 选项

使用 table 选项可以提供易于阅读的输出集，但请注意，与前面的.json 示例不同，使用简单 `--output table` 时，嵌套的对象不会包含在输出中。  在同一示例中使用“table”输出格式会组织有序的最常见属性值列表。

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

可以使用 `--query` 参数来自定义要在列表输出中显示的属性和列。 以下示例演示如何只在 `list` 命令中选择 VM 名称和资源组名称。

```azurecli-interactive
az vm list --query "[].{ resource: resourceGroup, name: name }" -o table
```

```
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

## <a name="using-the-tsv-option"></a>使用 tsv 选项

“tsv”输出格式返回不带标题和短划线的、基于文本的制表符分隔输出。 采用这种格式可在需要以某种形式处理文本的其他命令和工具中轻松使用输出。 在前面的示例中使用 `tsv` 选项会输出制表符分隔结果。

```azurecli-interactive
az vm list --out tsv
```

```
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus  DemoVM010           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus  demovm212           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus  demovm213           None    Succeeded   DEMORG1 None            Microsoft.Compute/virtualMachines   2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus  KBDemo001VM         None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachines   14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None   None    westus  KBDemo020           None    Succeeded   RGDEMO001   None            Microsoft.Compute/virtualMachinesed36baa9-9b80-48a8-b4a9-854c7a858ece
```

下一示例演示如何将 `tsv` 输出传递给 `grep` 和 `cut` 等命令，以进一步分析 `list` 输出中的特定值。 `grep` 命令仅选择包含文本“RGD”的项，`cut` 命令仅选择在输出中显示第 8 个字符（制表符分隔）。

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a>设置默认的输出格式

可以使用 `az configure` 命令设置环境或者建立首选项，例如，输出格式的默认设置。 对于一般用途，最方便的默认输出格式为“table”格式 - 系统提示选择输出格式时请选择 **3**。

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]:
```