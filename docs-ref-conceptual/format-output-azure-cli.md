---
title: Azure CLI 2.0 的输出格式
description: 了解如何将 Azure CLI 2.0 命令的输出格式设置为表、列表或 json。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: b402ce89cbf51adb3d521a604e992dd1fb5a42fa
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967599"
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="91672-103">Azure CLI 2.0 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="91672-103">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="91672-104">Azure CLI 2.0 使用 json 作为默认输出选项，但允许通过多种方法设置任何命令的输出。</span><span class="sxs-lookup"><span data-stu-id="91672-104">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="91672-105">使用 `--output`（或者 `--out` 或 `-o`）参数可将命令的输出格式设置为下表中所述的输出类型之一：</span><span class="sxs-lookup"><span data-stu-id="91672-105">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table:</span></span>

<span data-ttu-id="91672-106">--output</span><span class="sxs-lookup"><span data-stu-id="91672-106">--output</span></span> | <span data-ttu-id="91672-107">说明</span><span class="sxs-lookup"><span data-stu-id="91672-107">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="91672-108">JSON 字符串。</span><span class="sxs-lookup"><span data-stu-id="91672-108">JSON string.</span></span> <span data-ttu-id="91672-109">此设置为默认设置。</span><span class="sxs-lookup"><span data-stu-id="91672-109">This setting is the default.</span></span>
`jsonc`  | <span data-ttu-id="91672-110">彩色 JSON。</span><span class="sxs-lookup"><span data-stu-id="91672-110">Colorized JSON.</span></span>
`table`  | <span data-ttu-id="91672-111">将键作为列标题的 ASCII 表。</span><span class="sxs-lookup"><span data-stu-id="91672-111">ASCII table with keys as column headings.</span></span>
`tsv`    | <span data-ttu-id="91672-112">制表符分隔值，没有键</span><span class="sxs-lookup"><span data-stu-id="91672-112">Tab-separated values, with no keys</span></span>

## <a name="json-output-format"></a><span data-ttu-id="91672-113">JSON 输出格式</span><span class="sxs-lookup"><span data-stu-id="91672-113">JSON output format</span></span>

<span data-ttu-id="91672-114">以下示例以默认 json 格式显示订阅中的虚拟机列表。</span><span class="sxs-lookup"><span data-stu-id="91672-114">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="91672-115">以下输出有为简便起见而省略的一些字段并替换了标识信息。</span><span class="sxs-lookup"><span data-stu-id="91672-115">The following output has some fields omitted for brevity, and identifying information replaced.</span></span>

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

## <a name="table-output-format"></a><span data-ttu-id="91672-116">表输出格式</span><span class="sxs-lookup"><span data-stu-id="91672-116">Table output format</span></span>

<span data-ttu-id="91672-117">`table` 输出格式提供格式化为排序规则数据的行和列的无格式输出，以便更轻松地读取和扫描。</span><span class="sxs-lookup"><span data-stu-id="91672-117">The `table` output format provides plain output formatted as rows and columns of collated data, making it easy to read and scan.</span></span> <span data-ttu-id="91672-118">嵌套对象不包含在表输出中，但仍可以作为查询的一部分进行筛选。</span><span class="sxs-lookup"><span data-stu-id="91672-118">Nested objects are not included in table output, but can still be filtered as part of a query.</span></span> <span data-ttu-id="91672-119">还从表数据中省略了一些字段，因此当你想要数据的快速、人工可搜索的概述时，此格式最佳。</span><span class="sxs-lookup"><span data-stu-id="91672-119">Some fields are also omitted from the table data, so this format is best when you want a quick, human-searchable overview of data.</span></span>

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

<span data-ttu-id="91672-120">可以使用 `--query` 参数来自定义要在列表输出中显示的属性和列。</span><span class="sxs-lookup"><span data-stu-id="91672-120">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="91672-121">以下示例演示如何只在 `list` 命令中选择 VM 名称和资源组名称。</span><span class="sxs-lookup"><span data-stu-id="91672-121">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

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
> <span data-ttu-id="91672-122">某些键已筛选掉，未在表视图中输出。</span><span class="sxs-lookup"><span data-stu-id="91672-122">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="91672-123">这些键是 `id`、`type` 和 `etag`。</span><span class="sxs-lookup"><span data-stu-id="91672-123">These are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="91672-124">如果需要在输出中查看这些键，可以使用 JMESPath 重新键入功能更改键名称，并避免筛选。</span><span class="sxs-lookup"><span data-stu-id="91672-124">If you need to see these in your output, you can use the JMESPath re-keying feature to change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm list --query "[].{objectID:id}" -o table
> ```

<span data-ttu-id="91672-125">有关使用查询筛选数据的详细信息，请参阅[在 Azure CLI 2.0 中使用 JMESPath 查询](/cli/azure/query-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="91672-125">For more about using queries to filter data, see [Use JMESPath queries with Azure CLI 2.0](/cli/azure/query-azure-cli).</span></span>

## <a name="tsv-output-format"></a><span data-ttu-id="91672-126">TSV 输出格式</span><span class="sxs-lookup"><span data-stu-id="91672-126">TSV output format</span></span>

<span data-ttu-id="91672-127">`tsv` 输出格式返回制表符和换行符分隔的值，而不带附加格式设置、键或其他符号。</span><span class="sxs-lookup"><span data-stu-id="91672-127">The `tsv` output format returns tab- and newline-separated values without additional formatting, keys, or other symbols.</span></span> <span data-ttu-id="91672-128">采用这种格式可在需要以某种形式处理文本的其他命令和工具中轻松使用输出。</span><span class="sxs-lookup"><span data-stu-id="91672-128">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="91672-129">与 `table` 格式一样，`tsv` 输出选项不输出嵌套对象。</span><span class="sxs-lookup"><span data-stu-id="91672-129">Like the `table` format, the `tsv` output option does not print nested objects.</span></span>

<span data-ttu-id="91672-130">在前面的示例中使用 `tsv` 选项会输出制表符分隔结果。</span><span class="sxs-lookup"><span data-stu-id="91672-130">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

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

<span data-ttu-id="91672-131">下面的示例说明如何将 `tsv` 输出通过管道传递给 UNIX 系统上的其他命令以提取更具体的数据。</span><span class="sxs-lookup"><span data-stu-id="91672-131">The next example shows how the `tsv` output can be piped to other commands on UNIX systems to extract more specific data.</span></span> <span data-ttu-id="91672-132">`grep` 命令选择包含文本“RGD”的项，然后 `cut` 命令选择第 8 个字符（由制表符分隔）以在输出中显示 VM 的名称。</span><span class="sxs-lookup"><span data-stu-id="91672-132">The `grep` command selects items that have text "RGD" in them, and then the `cut` command selects the eighth field (separated by tabs) to show the name of the VM in output.</span></span>

```bash
az vm list --out tsv | grep RGD | cut -f8
```

```output
KBDemo001VM
KBDemo020
```

<span data-ttu-id="91672-133">为了处理制表符分隔的字段，值的顺序与它们在输出的 JSON 对象中显示的顺序相同。</span><span class="sxs-lookup"><span data-stu-id="91672-133">For the purposes of processing tab-separated fields, the values are in the same order that they appear in the printed JSON object.</span></span> <span data-ttu-id="91672-134">需保证此顺序在该命令的多次运行之间保持一致。</span><span class="sxs-lookup"><span data-stu-id="91672-134">This order is guaranteed to be consistent between runs of the command.</span></span>

## <a name="set-the-default-output-format"></a><span data-ttu-id="91672-135">设置默认输出格式</span><span class="sxs-lookup"><span data-stu-id="91672-135">Set the default output format</span></span>

<span data-ttu-id="91672-136">使用交互式 `az configure` 命令设置环境并建立输出格式的默认设置。</span><span class="sxs-lookup"><span data-stu-id="91672-136">Use the interactive `az configure` command to set up your environment and establish default settings for output formats.</span></span> <span data-ttu-id="91672-137">默认输出格式为 `json`。</span><span class="sxs-lookup"><span data-stu-id="91672-137">The default output format is `json`.</span></span>

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

<span data-ttu-id="91672-138">若要了解有关配置环境的详细信息，请参阅 [Azure CLI 2.0 配置](/cli/azure/azure-cli-configuration)。</span><span class="sxs-lookup"><span data-stu-id="91672-138">To learn more about configuring your environment, see [Azure CLI 2.0 configuration](/cli/azure/azure-cli-configuration).</span></span>