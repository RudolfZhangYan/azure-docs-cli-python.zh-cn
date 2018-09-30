---
title: Azure CLI 的输出格式
description: 了解如何将 Azure CLI 命令的输出格式设置为表、列表或 json。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 5b5d962e244037d9c904fc5c75314661130d1910
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178059"
---
# <a name="output-formats-for-azure-cli-commands"></a>Azure CLI 命令的输出格式

Azure CLI 使用 JSON 作为默认输出格式，但提供其他格式。  使用 `--output`（`--out` 或 `-o`）参数设置 CLI 输出的格式。 输出的参数值和类型为：

--output | Description
---------|-------------------------------
`json`   | JSON 字符串。 此设置为默认设置。
`jsonc`  | 彩色 JSON。
`yaml`   | YAML，一种机器可读的 JSON 替代格式。
`table`  | 将键作为列标题的 ASCII 表。
`tsv`    | 制表符分隔值，没有键

## <a name="json-output-format"></a>JSON 输出格式

以下示例以默认 json 格式显示订阅中的虚拟机列表。

```azurecli-interactive
az vm list --output json
```

以下输出有为简便起见而省略的一些字段并替换了标识信息。

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1"
    },
    "id": "/subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus",
    "name": "DemoVM010",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/.../resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
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

## <a name="yaml-output-format"></a>YAML 输出格式

`yaml` 格式将输出打印为 [YAML](http://yaml.org/)（一种纯文本数据序列化格式）。 YAML 往往比 JSON 更容易阅读，并且可以轻松映射到该格式。 某些应用程序和 CLI 命令将 YAML（而不是 JSON）作为配置输入。

```azurecli-interactive
az vm list --out yaml
```

以下输出有为简便起见而省略的一些字段并替换了标识信息。

```yaml
- availabilitySet: null
  diagnosticsProfile: null
  hardwareProfile:
    vmSize: Standard_DS1_v2
  id: /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010
  identity: null
  instanceView: null
  licenseType: null
  location: westus
  name: ExampleVM1
  networkProfile:
    networkInterfaces:
    - id: /subscriptions/.../resourceGroups/DemoRG1/providers/Microsoft.Network/networkInterfaces/DemoVM010Nic
      primary: null
      resourceGroup: DemoRG1
  ...
...
```

## <a name="table-output-format"></a>表输出格式

`table` 格式以 ASCII 表的形式列显输出，因此可以轻松阅读和扫描输出。 嵌套对象不会包含在表输出中，但仍可以作为查询的一部分进行筛选。 某些字段不会包含在表中，因此，当你想要数据的快速、人工可搜索的概述时，此格式最佳。

```azurecli-interactive
az vm list --out table
```

```output
Name         ResourceGroup    Location
-----------  ---------------  ----------
DemoVM010    DEMORG1          westus
demovm212    DEMORG1          westus
demovm213    DEMORG1          westus
KBDemo001VM  RGDEMO001        westus
KBDemo020    RGDEMO001        westus
```

可以使用 `--query` 参数来自定义要在列表输出中显示的属性和列。 以下示例演示如何只在 `list` 命令中选择 VM 名称和资源组名称。

```azurecli
az vm list --query "[].{resource:resourceGroup, name:name}" -o table
```

```output
Resource    Name
----------  -----------
DEMORG1     DemoVM010
DEMORG1     demovm212
DEMORG1     demovm213
RGDEMO001   KBDemo001VM
RGDEMO001   KBDemo020
```

> [!NOTE]
> 默认情况下，某些键不会在表视图中列显。 这些键是 `id`、`type` 和 `etag`。 如果需要在输出中查看这些键，可以使用 JMESPath 重新键入功能更改键名称，并避免筛选。
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

若要详细了解如何使用查询来筛选数据，请参阅[在 Azure CLI 中使用 JMESPath 查询](/cli/azure/query-azure-cli)。

## <a name="tsv-output-format"></a>TSV 输出格式

`tsv` 输出格式返回制表符和换行符分隔的值，而不带附加格式设置、键或其他符号。 采用这种格式可在需要以某种形式处理文本的其他命令和工具中轻松使用输出。 与 `table` 格式一样，`tsv` 不会列显嵌套的对象。

在前面的示例中使用 `tsv` 选项会输出制表符分隔结果。

```azurecli-interactive
az vm list --out tsv
```

```output
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010    None    None    westus    DemoVM010            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    cbd56d9b-9340-44bc-a722-25f15b578444
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm212    None    None    westus    demovm212            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    4bdac85d-c2f7-410f-9907-ca7921d930b4
None    None        /subscriptions/.../resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/demovm213    None    None    westus    demovm213            None    Succeeded    DEMORG1    None            Microsoft.Compute/virtualMachines    2131c664-221a-4b7f-9653-f6d542fbfa34
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo001VM    None    None    westus    KBDemo001VM            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    14e74761-c17e-4530-a7be-9e4ff06ea74b
None    None        /subscriptions/.../resourceGroups/RGDEMO001/providers/Microsoft.Compute/virtualMachines/KBDemo02None    None    westus    KBDemo020            None    Succeeded    RGDEMO001    None            Microsoft.Compute/virtualMachines    36baa9-9b80-48a8-b4a9-854c7a858ece
```

以下示例演示如何通过管道将 `tsv` 输出传送到 bash 中的其他命令。 `grep` 选择包含文本“RGD”的项，然后，`cut` 命令选择第 8 个字段以在输出中显示 VM 的名称。

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

为了处理制表符分隔的字段，值的顺序与它们在输出的 JSON 对象中显示的顺序相同。 需保证此顺序在该命令的多次运行之间保持一致。

## <a name="set-the-default-output-format"></a>设置默认输出格式

使用交互式 `az configure` 命令设置环境并建立输出格式的默认设置。 默认输出格式为 `json`。

```azurecli-interactive
az configure
```

```output
Welcome to the Azure CLI! This command will guide you through logging in and setting some default values.

Your settings can be found at /home/defaultuser/.azure/config
Your current configuration is as follows:

  ...

Do you wish to change your settings? (y/N): y

What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab- and Newline-delimited, great for GREP, AWK, etc.
Please enter a choice [1]:
```

若要详细了解如何配置环境，请参阅 [Azure CLI 配置](/cli/azure/azure-cli-configuration)。
