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
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2017
---
# <a name="output-formats-for-azure-cli-20-commands"></a><span data-ttu-id="bde31-104">Azure CLI 2.0 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="bde31-104">Output formats for Azure CLI 2.0 commands</span></span>

<span data-ttu-id="bde31-105">Azure CLI 2.0 使用 json 作为默认输出选项，但允许通过多种方法设置任何命令的输出。</span><span class="sxs-lookup"><span data-stu-id="bde31-105">Azure CLI 2.0 uses json as its default output option, but offers various ways for you to format the output of any command.</span></span>  <span data-ttu-id="bde31-106">使用 `--output`（或者 `--out` 或 `-o`）参数可将命令的输出格式设置为下表中所述的输出类型之一。</span><span class="sxs-lookup"><span data-stu-id="bde31-106">Use the `--output` (or `--out` or `-o`) parameter to format the output of the command into one of the output types noted in the following table.</span></span>

<span data-ttu-id="bde31-107">--output</span><span class="sxs-lookup"><span data-stu-id="bde31-107">--output</span></span> | <span data-ttu-id="bde31-108">说明</span><span class="sxs-lookup"><span data-stu-id="bde31-108">Description</span></span>
---------|-------------------------------
`json`   | <span data-ttu-id="bde31-109">json 字符串。</span><span class="sxs-lookup"><span data-stu-id="bde31-109">json string.</span></span> <span data-ttu-id="bde31-110">`json` 为默认值。</span><span class="sxs-lookup"><span data-stu-id="bde31-110">`json` is the default.</span></span>
`jsonc`  | <span data-ttu-id="bde31-111">彩色 json 字符串。</span><span class="sxs-lookup"><span data-stu-id="bde31-111">colorized json string.</span></span>
`table`  | <span data-ttu-id="bde31-112">包含列标题的表。</span><span class="sxs-lookup"><span data-stu-id="bde31-112">table with column headings.</span></span>
`tsv`    | <span data-ttu-id="bde31-113">制表符分隔值。</span><span class="sxs-lookup"><span data-stu-id="bde31-113">tab-separated values.</span></span>

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

## <a name="using-the-json-option"></a><span data-ttu-id="bde31-114">使用 json 选项</span><span class="sxs-lookup"><span data-stu-id="bde31-114">Using the json option</span></span>

<span data-ttu-id="bde31-115">以下示例以默认 json 格式显示订阅中的虚拟机列表。</span><span class="sxs-lookup"><span data-stu-id="bde31-115">The following example displays the list of virtual machines in your subscriptions in the default json format.</span></span>

```azurecli-interactive
az vm list --output json
```

<span data-ttu-id="bde31-116">结果会采用此格式（为简洁起见，仅显示部分输出）。</span><span class="sxs-lookup"><span data-stu-id="bde31-116">The results are in this form (only showing partial output for sake of brevity).</span></span>

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

## <a name="using-the-table-option"></a><span data-ttu-id="bde31-117">使用 table 选项</span><span class="sxs-lookup"><span data-stu-id="bde31-117">Using the table option</span></span>

<span data-ttu-id="bde31-118">使用 table 选项可以提供易于阅读的输出集，但请注意，与前面的.json 示例不同，使用简单 `--output table` 时，嵌套的对象不会包含在输出中。</span><span class="sxs-lookup"><span data-stu-id="bde31-118">The table option provides an easy to read set of output, but note that nested objects are not included in the output with the simple `--output table`, unlike the preceding .json example.</span></span>  <span data-ttu-id="bde31-119">在同一示例中使用“table”输出格式会组织有序的最常见属性值列表。</span><span class="sxs-lookup"><span data-stu-id="bde31-119">Using the same example with 'table' output format provides a curated list of most common property values.</span></span>

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

<span data-ttu-id="bde31-120">可以使用 `--query` 参数来自定义要在列表输出中显示的属性和列。</span><span class="sxs-lookup"><span data-stu-id="bde31-120">You can use the `--query` parameter to customize the properties and columns you want to show in the list output.</span></span> <span data-ttu-id="bde31-121">以下示例演示如何只在 `list` 命令中选择 VM 名称和资源组名称。</span><span class="sxs-lookup"><span data-stu-id="bde31-121">The following example shows how to select just the VM Name and the Resource Group Name in the `list` command.</span></span>

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

## <a name="using-the-tsv-option"></a><span data-ttu-id="bde31-122">使用 tsv 选项</span><span class="sxs-lookup"><span data-stu-id="bde31-122">Using the tsv option</span></span>

<span data-ttu-id="bde31-123">“tsv”输出格式返回不带标题和短划线的、基于文本的制表符分隔输出。</span><span class="sxs-lookup"><span data-stu-id="bde31-123">'tsv' output format returns a simple text-based and tab-separated output with no headings and dashes.</span></span> <span data-ttu-id="bde31-124">采用这种格式可在需要以某种形式处理文本的其他命令和工具中轻松使用输出。</span><span class="sxs-lookup"><span data-stu-id="bde31-124">This format makes it easy to consume the output into other commands and tools that need to process the text in some form.</span></span> <span data-ttu-id="bde31-125">在前面的示例中使用 `tsv` 选项会输出制表符分隔结果。</span><span class="sxs-lookup"><span data-stu-id="bde31-125">Using the preceding example with the `tsv` option outputs the tab-separated result.</span></span>

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

<span data-ttu-id="bde31-126">下一示例演示如何将 `tsv` 输出传递给 `grep` 和 `cut` 等命令，以进一步分析 `list` 输出中的特定值。</span><span class="sxs-lookup"><span data-stu-id="bde31-126">The next example shows how the `tsv` output can be piped to commands like `grep` and `cut` to further parse specific values out of the `list` output.</span></span> <span data-ttu-id="bde31-127">`grep` 命令仅选择包含文本“RGD”的项，`cut` 命令仅选择在输出中显示第 8 个字符（制表符分隔）。</span><span class="sxs-lookup"><span data-stu-id="bde31-127">The `grep` command selects only items that have text "RGD" in them and then the `cut` command selects only the eighth field (separated by tabs) value to show in the output.</span></span>

```azurecli
az vm list --out tsv | grep RGD | cut -f8
```

```
KBDemo001VM
KBDemo020
```

## <a name="setting-the-default-output-format"></a><span data-ttu-id="bde31-128">设置默认的输出格式</span><span class="sxs-lookup"><span data-stu-id="bde31-128">Setting the default output format</span></span>

<span data-ttu-id="bde31-129">可以使用 `az configure` 命令设置环境或者建立首选项，例如，输出格式的默认设置。</span><span class="sxs-lookup"><span data-stu-id="bde31-129">You can use the `az configure` command to set up your environment or establish preferences such as default settings for output formats.</span></span> <span data-ttu-id="bde31-130">对于一般用途，最方便的默认输出格式为“table”格式 - 系统提示选择输出格式时请选择 **3**。</span><span class="sxs-lookup"><span data-stu-id="bde31-130">For common use, the easiest output format default is the "table" format - select **3** when prompted for output format choices.</span></span>

```
What default output format would you like?
 [1] json - JSON formatted output that most closely matches API responses
 [2] jsonc - Colored JSON formatted output that most closely matches API responses
 [3] table - Human-readable output format
 [4] tsv - Tab and Newline delimited, great for GREP, AWK, etc.
Please enter a choice [3]:
```