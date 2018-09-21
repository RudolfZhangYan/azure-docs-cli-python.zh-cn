---
title: Azure CLI 2.0 的输出格式
description: 了解如何将 Azure CLI 2.0 命令的输出格式设置为表、列表或 json。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 1430d817a7e6c10a8f8021cf9d763f62d560ba71
ms.sourcegitcommit: 8318ce761c279afa4cd45a81a58d83fc38c616bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/13/2018
ms.locfileid: "45561552"
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="81e3f-103">Azure CLI 2.0 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="81e3f-103">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="81e3f-104">Azure CLI 2.0 使用 JSON 作为默认输出格式，但提供其他格式。</span><span class="sxs-lookup"><span data-stu-id="81e3f-104">Azure CLI 2.0 uses JSON as its default output format, but offers other formats.</span></span>  <span data-ttu-id="81e3f-105">使用 `--output`（`--out` 或 `-o`）参数设置 CLI 输出的格式。</span><span class="sxs-lookup"><span data-stu-id="81e3f-105">Use the `--output` (`--out` or `-o`) parameter to format CLI output.</span></span> <span data-ttu-id="81e3f-106">输出的参数值和类型为：</span><span class="sxs-lookup"><span data-stu-id="81e3f-106">The argument values and types of output are:</span></span>

<span data-ttu-id="81e3f-107">--output</span><span class="sxs-lookup"><span data-stu-id="81e3f-107">--output</span></span> | <span data-ttu-id="81e3f-108">Description</span><span class="sxs-lookup"><span data-stu-id="81e3f-108">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="81e3f-109">JSON 字符串。</span><span class="sxs-lookup"><span data-stu-id="81e3f-109">JSON string.</span></span> <span data-ttu-id="81e3f-110">此设置为默认设置。</span><span class="sxs-lookup"><span data-stu-id="81e3f-110">This setting is the default.</span></span>
`jsonc`  | <span data-ttu-id="81e3f-111">彩色 JSON。</span><span class="sxs-lookup"><span data-stu-id="81e3f-111">Colorized JSON.</span></span>
`yaml`   | <span data-ttu-id="81e3f-112">YAML，一种机器可读的 JSON 替代格式。</span><span class="sxs-lookup"><span data-stu-id="81e3f-112">YAML, a machine-readable alternative to JSON.</span></span>
`table`  | <span data-ttu-id="81e3f-113">将键作为列标题的 ASCII 表。</span><span class="sxs-lookup"><span data-stu-id="81e3f-113">ASCII table with keys as column headings.</span></span>
`tsv`    | <span data-ttu-id="81e3f-114">制表符分隔值，没有键</span><span class="sxs-lookup"><span data-stu-id="81e3f-114">Tab-separated values, with no keys</span></span>

## <a name="json-output-format"></a><span data-ttu-id="81e3f-115">JSON 输出格式</span><span class="sxs-lookup"><span data-stu-id="81e3f-115">JSON output format</span></span>

<span data-ttu-id="81e3f-116">以下示例以默认 json 格式显示订阅中的虚拟机列表。</span><span class="sxs-lookup"><span data-stu-id="81e3f-116">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="81e3f-117">以下输出有为简便起见而省略的一些字段并替换了标识信息。</span><span class="sxs-lookup"><span data-stu-id="81e3f-117">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

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

## <a name="yaml-output-format"></a><span data-ttu-id="81e3f-118">YAML 输出格式</span><span class="sxs-lookup"><span data-stu-id="81e3f-118">YAML output format</span></span>

<span data-ttu-id="81e3f-119">`yaml` 格式将输出打印为 [YAML](http://yaml.org/)（一种纯文本数据序列化格式）。</span><span class="sxs-lookup"><span data-stu-id="81e3f-119">The `yaml` format prints output as [YAML](http://yaml.org/), a plain-text data serialization format.</span></span> <span data-ttu-id="81e3f-120">YAML 往往比 JSON 更容易阅读，并且可以轻松映射到该格式。</span><span class="sxs-lookup"><span data-stu-id="81e3f-120">YAML tends to be easier to read than JSON, and easily maps to that format.</span></span> <span data-ttu-id="81e3f-121">某些应用程序和 CLI 命令将 YAML（而不是 JSON）作为配置输入。</span><span class="sxs-lookup"><span data-stu-id="81e3f-121">Some applications and CLI commands take YAML as configuration input, instead of JSON.</span></span>

```azurecli-interactive
az vm list --out yaml
```

<span data-ttu-id="81e3f-122">以下输出有为简便起见而省略的一些字段并替换了标识信息。</span><span class="sxs-lookup"><span data-stu-id="81e3f-122">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

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

## <a name="table-output-format"></a><span data-ttu-id="81e3f-123">表输出格式</span><span class="sxs-lookup"><span data-stu-id="81e3f-123">Table output format</span></span>

<span data-ttu-id="81e3f-124">`table` 格式以 ASCII 表的形式列显输出，因此可以轻松阅读和扫描输出。</span><span class="sxs-lookup"><span data-stu-id="81e3f-124">The `table` format prints output as an ASCII table, making it easy to read and scan.</span></span> <span data-ttu-id="81e3f-125">嵌套对象不会包含在表输出中，但仍可以作为查询的一部分进行筛选。</span><span class="sxs-lookup"><span data-stu-id="81e3f-125">Nested objects aren't included in table output, but can still be filtered as part of a query.</span></span> <span data-ttu-id="81e3f-126">某些字段不会包含在表中，因此，当你想要数据的快速、人工可搜索的概述时，此格式最佳。</span><span class="sxs-lookup"><span data-stu-id="81e3f-126">Some fields aren't included in the table, so this format is best when you want a quick, human-searchable overview of data.</span></span>

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

<span data-ttu-id="81e3f-127">可以使用 `--query` 参数来自定义要在列表输出中显示的属性和列。</span><span class="sxs-lookup"><span data-stu-id="81e3f-127">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="81e3f-128">以下示例演示如何只在 `list` 命令中选择 VM 名称和资源组名称。</span><span class="sxs-lookup"><span data-stu-id="81e3f-128">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

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
> <span data-ttu-id="81e3f-129">默认情况下，某些键不会在表视图中列显。</span><span class="sxs-lookup"><span data-stu-id="81e3f-129">Some keys are not printed in the table view by default.</span></span> <span data-ttu-id="81e3f-130">这些键是 `id`、`type` 和 `etag`。</span><span class="sxs-lookup"><span data-stu-id="81e3f-130">These are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="81e3f-131">如果需要在输出中查看这些键，可以使用 JMESPath 重新键入功能更改键名称，并避免筛选。</span><span class="sxs-lookup"><span data-stu-id="81e3f-131">If you need to see these in your output, you can use the JMESPath re-keying feature to change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

<span data-ttu-id="81e3f-132">有关使用查询筛选数据的详细信息，请参阅[在 Azure CLI 2.0 中使用 JMESPath 查询](/cli/azure/query-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="81e3f-132">For more about using queries to filter data, see [Use JMESPath queries with Azure CLI 2.0](/cli/azure/query-azure-cli).</span></span>

## <a name="tsv-output-format"></a><span data-ttu-id="81e3f-133">TSV 输出格式</span><span class="sxs-lookup"><span data-stu-id="81e3f-133">TSV output format</span></span>

<span data-ttu-id="81e3f-134">`tsv` 输出格式返回制表符和换行符分隔的值，而不带附加格式设置、键或其他符号。</span><span class="sxs-lookup"><span data-stu-id="81e3f-134">The `tsv` output format returns tab- and newline-separated values without additional formatting, keys, or other symbols.</span></span> <span data-ttu-id="81e3f-135">采用这种格式可在需要以某种形式处理文本的其他命令和工具中轻松使用输出。</span><span class="sxs-lookup"><span data-stu-id="81e3f-135">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="81e3f-136">与 `table` 格式一样，`tsv` 不会列显嵌套的对象。</span><span class="sxs-lookup"><span data-stu-id="81e3f-136">Like the `table` format, `tsv` doesn't print nested objects.</span></span>

<span data-ttu-id="81e3f-137">在前面的示例中使用 `tsv` 选项会输出制表符分隔结果。</span><span class="sxs-lookup"><span data-stu-id="81e3f-137">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

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

<span data-ttu-id="81e3f-138">以下示例演示如何通过管道将 `tsv` 输出传送到 bash 中的其他命令。</span><span class="sxs-lookup"><span data-stu-id="81e3f-138">The next example shows how `tsv` output can be piped to other commands in bash.</span></span> <span data-ttu-id="81e3f-139">`grep` 选择包含文本“RGD”的项，然后，`cut` 命令选择第 8 个字段以在输出中显示 VM 的名称。</span><span class="sxs-lookup"><span data-stu-id="81e3f-139">`grep` selects items that have text "RGD" in them, then the `cut` command selects the eighth field to show the name of the VM in output.</span></span>

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

<span data-ttu-id="81e3f-140">为了处理制表符分隔的字段，值的顺序与它们在输出的 JSON 对象中显示的顺序相同。</span><span class="sxs-lookup"><span data-stu-id="81e3f-140">For the purposes of processing tab-separated fields, the values are in the same order that they appear in the printed JSON object.</span></span> <span data-ttu-id="81e3f-141">需保证此顺序在该命令的多次运行之间保持一致。</span><span class="sxs-lookup"><span data-stu-id="81e3f-141">This order is guaranteed to be consistent between runs of the command.</span></span>

## <a name="set-the-default-output-format"></a><span data-ttu-id="81e3f-142">设置默认输出格式</span><span class="sxs-lookup"><span data-stu-id="81e3f-142">Set the default output format</span></span>

<span data-ttu-id="81e3f-143">使用交互式 `az configure` 命令设置环境并建立输出格式的默认设置。</span><span class="sxs-lookup"><span data-stu-id="81e3f-143">Use the interactive `az configure` command to set up your environment and establish default settings for output formats.</span></span> <span data-ttu-id="81e3f-144">默认输出格式为 `json`。</span><span class="sxs-lookup"><span data-stu-id="81e3f-144">The default output format is `json`.</span></span>

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

<span data-ttu-id="81e3f-145">若要了解有关配置环境的详细信息，请参阅 [Azure CLI 2.0 配置](/cli/azure/azure-cli-configuration)。</span><span class="sxs-lookup"><span data-stu-id="81e3f-145">To learn more about configuring your environment, see [Azure CLI 2.0 configuration](/cli/azure/azure-cli-configuration).</span></span>