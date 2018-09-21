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
# <a name="use-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="7fb40-103">在 Azure CLI 2.0 中使用 JMESPath 查询</span><span class="sxs-lookup"><span data-stu-id="7fb40-103">Use JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="7fb40-104">Azure CLI 2.0 使用 `--query` 参数针对命令的结果执行 [JMESPath 查询](http://jmespath.org)。</span><span class="sxs-lookup"><span data-stu-id="7fb40-104">The Azure CLI 2.0 uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="7fb40-105">JMESPath 是用于 JSON 的查询语言，提供从 CLI 输出中选择和显示数据的能力。</span><span class="sxs-lookup"><span data-stu-id="7fb40-105">JMESPath is a query language for JSON, giving you the ability to select and present data from CLI output.</span></span> <span data-ttu-id="7fb40-106">先针对 JSON 输出执行这些查询，然后再针对任何显示格式执行。</span><span class="sxs-lookup"><span data-stu-id="7fb40-106">These queries are executed on the JSON output before any display formatting.</span></span>

<span data-ttu-id="7fb40-107">Azure CLI 中的所有命令均支持 `--query` 参数。</span><span class="sxs-lookup"><span data-stu-id="7fb40-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="7fb40-108">本文中的示例涵盖了常见用例，并演示了如何使用 JMESPath 的功能。</span><span class="sxs-lookup"><span data-stu-id="7fb40-108">This article's examples cover common use cases and demonstrate how to use the features of JMESPath.</span></span>

## <a name="work-with-dictionary-output"></a><span data-ttu-id="7fb40-109">使用字典输出</span><span class="sxs-lookup"><span data-stu-id="7fb40-109">Work with dictionary output</span></span>

<span data-ttu-id="7fb40-110">返回 JSON 字典的命令可以单独按其键名称查阅。</span><span class="sxs-lookup"><span data-stu-id="7fb40-110">Commands that return a JSON dictionary can be explored by their key names alone.</span></span> <span data-ttu-id="7fb40-111">键路径使用 `.` 字符作为分隔符。</span><span class="sxs-lookup"><span data-stu-id="7fb40-111">Key paths use the `.` character as a separator.</span></span> <span data-ttu-id="7fb40-112">下面的示例拉取允许连接到 Linux VM 的公共 SSH 密钥列表：</span><span class="sxs-lookup"><span data-stu-id="7fb40-112">The following example pulls a list of the public SSH keys allowed to connect to a Linux VM:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

<span data-ttu-id="7fb40-113">多个值可放入有序数组。</span><span class="sxs-lookup"><span data-stu-id="7fb40-113">Multiple values can be put into an ordered array.</span></span> <span data-ttu-id="7fb40-114">下面的示例演示如何检索 Azure 映像产品名称和 OS 磁盘大小：</span><span class="sxs-lookup"><span data-stu-id="7fb40-114">The following example shows how to retrieve the Azure image offering name and the size of the OS disk:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

<span data-ttu-id="7fb40-115">如果希望输出中有键，可以使用另一种字典语法。</span><span class="sxs-lookup"><span data-stu-id="7fb40-115">If you want keys in your output, you can use an alternate dictionary syntax.</span></span>  <span data-ttu-id="7fb40-116">将元素选择到一个字典时使用格式 `{displayKey:keyPath, ...}` 来针对 `keyPath` JMESPath 表达式进行筛选。</span><span class="sxs-lookup"><span data-stu-id="7fb40-116">Element selection into a dictionary uses the format `{displayKey:keyPath, ...}` to filter on the `keyPath` JMESPath expression.</span></span> <span data-ttu-id="7fb40-117">在输出值中，键/值对将更改为 `{displayKey: value}`。</span><span class="sxs-lookup"><span data-stu-id="7fb40-117">In the output values, the key/value pairs are changed to `{displayKey: value}`.</span></span> <span data-ttu-id="7fb40-118">下一个示例采用上一个示例的查询，并通过将键指定到输出来使输出更加清晰：</span><span class="sxs-lookup"><span data-stu-id="7fb40-118">The next example takes the last example's query, and makes it clearer by assigning keys to the output:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

<span data-ttu-id="7fb40-119">以 `table` 输出格式显示信息时，字典显示允许设置你自己的列标题。</span><span class="sxs-lookup"><span data-stu-id="7fb40-119">When displaying information in the `table` output format, dictionary display allows setting your own column headers.</span></span> <span data-ttu-id="7fb40-120">有关输出格式的详细信息，请参阅 [Azure CLI 2.0 命令的输出格式](/cli/azure/format-output-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="7fb40-120">For more information on output formats, see [Output formats for Azure CLI 2.0 commands](/cli/azure/format-output-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="7fb40-121">某些键已筛选掉，未在表视图中输出。</span><span class="sxs-lookup"><span data-stu-id="7fb40-121">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="7fb40-122">这些键为 `id`、`type` 和 `etag`。</span><span class="sxs-lookup"><span data-stu-id="7fb40-122">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="7fb40-123">如果需要查看此信息，可以更改键名称并避免筛选。</span><span class="sxs-lookup"><span data-stu-id="7fb40-123">If you need to see this information, you can change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a><span data-ttu-id="7fb40-124">使用列表输出</span><span class="sxs-lookup"><span data-stu-id="7fb40-124">Work with list output</span></span>

<span data-ttu-id="7fb40-125">可能会返回多个值的 CLI 命令将返回一个数组。</span><span class="sxs-lookup"><span data-stu-id="7fb40-125">CLI commands that may return  more than one value return an array.</span></span> <span data-ttu-id="7fb40-126">数组元素可按索引访问，不一定每次都按相同的顺序返回。</span><span class="sxs-lookup"><span data-stu-id="7fb40-126">Array elements are accessed by index and may not be returned in the same order every time.</span></span> <span data-ttu-id="7fb40-127">可以一次性查询所有数组元素，只需使用 `[]` 运算符将其平展即可。</span><span class="sxs-lookup"><span data-stu-id="7fb40-127">You can query all array elements at once by flattening them with the `[]` operator.</span></span> <span data-ttu-id="7fb40-128">该运算符放在数组的后面，或者用作表达式中的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="7fb40-128">The operator is put after the array or as the first element in an expression.</span></span> <span data-ttu-id="7fb40-129">平展某个数组会针对该数组的每个元素运行该运算符后面的查询。</span><span class="sxs-lookup"><span data-stu-id="7fb40-129">Flattening an array runs the query after it against each element of the array.</span></span>

<span data-ttu-id="7fb40-130">以下示例输出资源组中每个 VM 的名称以及其上运行的 OS。</span><span class="sxs-lookup"><span data-stu-id="7fb40-130">The following example prints out the name and OS running on each VM in a resource group.</span></span>

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

<span data-ttu-id="7fb40-131">作为键路径一部分的数组也可以平展。</span><span class="sxs-lookup"><span data-stu-id="7fb40-131">Arrays that are part of a key path can be flattened as well.</span></span> <span data-ttu-id="7fb40-132">以下查询获取 VM 连接到的 NIC 的 Azure 对象 ID。</span><span class="sxs-lookup"><span data-stu-id="7fb40-132">The following query gets the Azure object IDs for the NICs a VM is connected to.</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a><span data-ttu-id="7fb40-133">使用谓词筛选数组输出</span><span class="sxs-lookup"><span data-stu-id="7fb40-133">Filter array output with predicates</span></span>

<span data-ttu-id="7fb40-134">JMESPath 提供[筛选表达式](http://jmespath.org/specification.html#filterexpressions)以筛选显示的数据。</span><span class="sxs-lookup"><span data-stu-id="7fb40-134">JMESPath offers [filtering expressions](http://jmespath.org/specification.html#filterexpressions) to filter out the data displayed.</span></span> <span data-ttu-id="7fb40-135">这些表达式功能强大，尤其是在与 [JMESPath 内置函数](http://jmespath.org/specification.html#built-in-functions)结合使用以执行部分匹配或将数据处理为标准格式时。</span><span class="sxs-lookup"><span data-stu-id="7fb40-135">These expressions are powerful, especially when combined with [JMESPath built-in functions](http://jmespath.org/specification.html#built-in-functions) to do partial matches or manipulate data into a standard format.</span></span> <span data-ttu-id="7fb40-136">筛选表达式只适用于数组数据，在任何其他情况下使用时将返回 `null` 值。</span><span class="sxs-lookup"><span data-stu-id="7fb40-136">Filtering expressions only work on array data, and when used in any other situation, return the `null` value.</span></span> <span data-ttu-id="7fb40-137">例如，可以采用 `vm list` 等命令的输出，并针对其进行筛选，以查找特定类型的 VM。</span><span class="sxs-lookup"><span data-stu-id="7fb40-137">For example, you can take the output of commands like `vm list` and filter on it to look for specific types of VMs.</span></span> <span data-ttu-id="7fb40-138">以下示例通过筛选 VM 类型以仅捕获 Windows VM 并打印其名称，在前一个示例的基础上进行了扩展。</span><span class="sxs-lookup"><span data-stu-id="7fb40-138">The following example expands on the previous by filtering out the VM type to capture only Windows VMs and print their name.</span></span>

```azurecli-interactive
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="7fb40-139">以交互方式试验查询</span><span class="sxs-lookup"><span data-stu-id="7fb40-139">Experiment with queries interactively</span></span>

<span data-ttu-id="7fb40-140">[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python 包提供了用于体验查询的交互式环境，帮助你开始学习 JMESPath。</span><span class="sxs-lookup"><span data-stu-id="7fb40-140">To start learning JMESPath, the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package offers an interactive environment to experiment with queries.</span></span> <span data-ttu-id="7fb40-141">数据作为输入通过管道传送，然后将编写并编辑程序内部查询以提取数据。</span><span class="sxs-lookup"><span data-stu-id="7fb40-141">Data is piped as input, and then in-program queries are written and edited to extract the data.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
