---
title: 使用 Azure CLI 2.0 查询命令结果
description: 了解如何针对 Azure CLI 2.0 命令的输出执行 JMESPath 查询。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: ed8f8ac160dd8225170ffcfff9619d94b92e456a
ms.sourcegitcommit: 8b4629a42ceecf30c1efbc6fdddf512f4dddfab0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2018
---
# <a name="use-jmespath-queries-with-azure-cli-20"></a><span data-ttu-id="aa396-103">在 Azure CLI 2.0 中使用 JMESPath 查询</span><span class="sxs-lookup"><span data-stu-id="aa396-103">Use JMESPath queries with Azure CLI 2.0</span></span>

<span data-ttu-id="aa396-104">Azure CLI 2.0 使用 `--query` 参数针对命令的结果执行 [JMESPath 查询](http://jmespath.org)。</span><span class="sxs-lookup"><span data-stu-id="aa396-104">The Azure CLI 2.0 uses the `--query` argument to execute a [JMESPath query](http://jmespath.org) on the results of commands.</span></span> <span data-ttu-id="aa396-105">JMESPath 是用于 JSON 的查询语言，提供从 CLI 输出中选择和显示数据的能力。</span><span class="sxs-lookup"><span data-stu-id="aa396-105">JMESPath is a query language for JSON, giving you the ability to select and present data from CLI output.</span></span> <span data-ttu-id="aa396-106">这些查询在执行任何其他显示格式设置之前针对 JSON 输出执行。</span><span class="sxs-lookup"><span data-stu-id="aa396-106">These queries are executed on the JSON output, before performing any other display formatting.</span></span>

<span data-ttu-id="aa396-107">Azure CLI 中的所有命令均支持 `--query` 参数。</span><span class="sxs-lookup"><span data-stu-id="aa396-107">The `--query` argument is supported by all commands in the Azure CLI.</span></span> <span data-ttu-id="aa396-108">本文中的示例涵盖了常见用例，并演示了如何使用 JMESPath 的功能。</span><span class="sxs-lookup"><span data-stu-id="aa396-108">This article's examples cover common use cases and demonstrate how to use the features of JMESPath.</span></span>

## <a name="work-with-dictionary-output"></a><span data-ttu-id="aa396-109">使用字典输出</span><span class="sxs-lookup"><span data-stu-id="aa396-109">Work with dictionary output</span></span>

<span data-ttu-id="aa396-110">返回 JSON 字典的命令可以单独按其键名称查阅。</span><span class="sxs-lookup"><span data-stu-id="aa396-110">Commands that return a JSON dictionary can be explored by their key names alone.</span></span> <span data-ttu-id="aa396-111">键路径使用 `.` 字符作为分隔符。</span><span class="sxs-lookup"><span data-stu-id="aa396-111">Key paths use the `.` character as a separator.</span></span> <span data-ttu-id="aa396-112">下面的示例拉取允许连接到 Linux VM 的公共 SSH 密钥列表：</span><span class="sxs-lookup"><span data-stu-id="aa396-112">The following example pulls a list of the public SSH keys allowed to connect to a Linux VM:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query osProfile.linuxConfiguration.ssh.publicKeys
```

<span data-ttu-id="aa396-113">也可以获取多个值，将它们放在一个有序数组中。</span><span class="sxs-lookup"><span data-stu-id="aa396-113">You can also get multiple values, putting them in an ordered array.</span></span> <span data-ttu-id="aa396-114">该数组没有任何键信息，但数组元素的顺序与所查询键的顺序匹配。</span><span class="sxs-lookup"><span data-stu-id="aa396-114">The array doesn't have any key information, but the order of the array's elements matches the order of the queried keys.</span></span> <span data-ttu-id="aa396-115">下面的示例演示如何检索 Azure 映像产品名称和 OS 磁盘大小：</span><span class="sxs-lookup"><span data-stu-id="aa396-115">The following example shows how to retrieve the Azure image offering name and the size of the OS disk:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.[imageReference.offer, osDisk.diskSizeGb]'
```

```json
[
  "UbuntuServer",
  30
]
```

<span data-ttu-id="aa396-116">如果希望输出中有键，可以使用另一种字典语法。</span><span class="sxs-lookup"><span data-stu-id="aa396-116">If you want keys in your output, you can use an alternate dictionary syntax.</span></span> <span data-ttu-id="aa396-117">将多个元素选择到一个字典时使用格式 `{displayKey:keyPath, ...}` 来针对 `keyPath` JMESPath 表达式进行筛选。</span><span class="sxs-lookup"><span data-stu-id="aa396-117">Multiple element selection into a dictionary uses the format `{displayKey:keyPath, ...}` to filter on the `keyPath` JMESPath expression.</span></span> <span data-ttu-id="aa396-118">这在输出中以 `{displayKey: value}` 形式显示。</span><span class="sxs-lookup"><span data-stu-id="aa396-118">This displays in the output as `{displayKey: value}`.</span></span> <span data-ttu-id="aa396-119">下一个示例采用上一个示例的查询，并通过将键指定到输出来使输出更加清晰：</span><span class="sxs-lookup"><span data-stu-id="aa396-119">The next example takes the last example's query, and makes it clearer by assigning keys to the output:</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'storageProfile.{image:imageReference.offer, diskSize:osDisk.diskSizeGb}'
```

```json
{
  "diskSize": 30,
  "image": "UbuntuServer"
}
```

<span data-ttu-id="aa396-120">以 `table` 输出格式显示信息时，字典显示尤其有用。</span><span class="sxs-lookup"><span data-stu-id="aa396-120">When displaying information in the `table` output format, dictionary display is especially useful.</span></span> <span data-ttu-id="aa396-121">它允许设置你自己的列标题，使输出更易于理解。</span><span class="sxs-lookup"><span data-stu-id="aa396-121">This allows for setting your own column headers, making output even easier to read.</span></span> <span data-ttu-id="aa396-122">有关输出格式的详细信息，请参阅 [Azure CLI 2.0 命令的输出格式](/cli/azure/format-output-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="aa396-122">For more information on output formats, see [Output formats for Azure CLI 2.0 commands](/cli/azure/format-output-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="aa396-123">某些键已筛选掉，未在表视图中输出。</span><span class="sxs-lookup"><span data-stu-id="aa396-123">Certain keys are filtered out and not printed in the table view.</span></span> <span data-ttu-id="aa396-124">这些键为 `id`、`type` 和 `etag`。</span><span class="sxs-lookup"><span data-stu-id="aa396-124">These keys are `id`, `type`, and `etag`.</span></span> <span data-ttu-id="aa396-125">如果需要查看此信息，可以更改键名称并避免筛选。</span><span class="sxs-lookup"><span data-stu-id="aa396-125">If you need to see this information, you can change the key name and avoid filtering.</span></span>
>
> ```azurecli
> az vm show -g QueryDemo -n TestVM --query "{objectID:id}" -o table
> ```

## <a name="work-with-list-output"></a><span data-ttu-id="aa396-126">使用列表输出</span><span class="sxs-lookup"><span data-stu-id="aa396-126">Work with list output</span></span>

<span data-ttu-id="aa396-127">可能会返回多个值的 CLI 命令总是会返回一个数组。</span><span class="sxs-lookup"><span data-stu-id="aa396-127">CLI commands that may return more than one value always return an array.</span></span> <span data-ttu-id="aa396-128">数组可以使其元素按索引进行访问，但 CLI 中永远不会有顺序保证。</span><span class="sxs-lookup"><span data-stu-id="aa396-128">Arrays can have their elements accessed by index, but there's never an order guarantee from the CLI.</span></span> <span data-ttu-id="aa396-129">查询数组值的最佳方法是使用 `[]` 运算符平展这些值。</span><span class="sxs-lookup"><span data-stu-id="aa396-129">The best way to query an array of values is to flatten them with the `[]` operator.</span></span> <span data-ttu-id="aa396-130">该运算符写在数组的键后面，或写为表达式中的第一个元素。</span><span class="sxs-lookup"><span data-stu-id="aa396-130">The operator is written after the key for the array, or as the first element in the expression.</span></span> <span data-ttu-id="aa396-131">平展时将针对数组中的每个单独元素运行该运算符后的查询，并将结果值放入一个新数组。</span><span class="sxs-lookup"><span data-stu-id="aa396-131">Flattening runs the query following it against each individual element in the array, and places the resulting values into a new array.</span></span> <span data-ttu-id="aa396-132">以下示例输出资源组中每个 VM 的名称以及其上运行的 OS。</span><span class="sxs-lookup"><span data-stu-id="aa396-132">The following example prints out the name and OS running on each VM in a resource group.</span></span> 

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

<span data-ttu-id="aa396-133">作为键路径一部分的数组也可以平展。</span><span class="sxs-lookup"><span data-stu-id="aa396-133">Arrays that are part of a key path can be flattened as well.</span></span> <span data-ttu-id="aa396-134">此示例演示一个查询，该查询获取 VM 连接到的 NIC 的 Azure 对象 ID。</span><span class="sxs-lookup"><span data-stu-id="aa396-134">This example demonstrates a query that gets the Azure object IDs for the NICs a VM is connected to.</span></span>

```azurecli-interactive
az vm show -g QueryDemo -n TestVM --query 'networkProfile.networkInterfaces[].id'
```

## <a name="filter-array-output-with-predicates"></a><span data-ttu-id="aa396-135">使用谓词筛选数组输出</span><span class="sxs-lookup"><span data-stu-id="aa396-135">Filter array output with predicates</span></span>

<span data-ttu-id="aa396-136">JMESPath 提供[筛选表达式](http://jmespath.org/specification.html#filterexpressions)以筛选显示的数据。</span><span class="sxs-lookup"><span data-stu-id="aa396-136">JMESPath offers [filtering expressions](http://jmespath.org/specification.html#filterexpressions) to filter out the data displayed.</span></span> <span data-ttu-id="aa396-137">这些表达式功能强大，尤其是在与 [JMESPath 内置函数](http://jmespath.org/specification.html#built-in-functions)结合使用以执行部分匹配或将数据处理为标准格式时。</span><span class="sxs-lookup"><span data-stu-id="aa396-137">These expressions are powerful, especially when combined with [JMESPath built-in functions](http://jmespath.org/specification.html#built-in-functions) to perform partial matches or manipulate data into a standard format.</span></span> <span data-ttu-id="aa396-138">筛选表达式只适用于数组数据，在任何其他情况下使用时将返回 `null` 值。</span><span class="sxs-lookup"><span data-stu-id="aa396-138">Filtering expressions only work on array data, and when used in any other situation, return the `null` value.</span></span> <span data-ttu-id="aa396-139">例如，可以采用 `vm list` 等命令的输出，并针对其进行筛选，以查找特定类型的 VM。</span><span class="sxs-lookup"><span data-stu-id="aa396-139">For example, you can take the output of commands like `vm list` and filter on it to look for specific types of VMs.</span></span> <span data-ttu-id="aa396-140">以下示例通过筛选 VM 类型以仅捕获 Windows VM 并打印其名称，在前一个示例的基础上进行了扩展。</span><span class="sxs-lookup"><span data-stu-id="aa396-140">The following example expands on the previous by filtering out the VM type to capture only Windows VMs and print their name.</span></span>

```azurecli-interactive
az vm list --query '[?osProfile.windowsConfiguration!=null].name'
```

```json
[
  "WinServ"
]
```

## <a name="experiment-with-queries-interactively"></a><span data-ttu-id="aa396-141">以交互方式试验查询</span><span class="sxs-lookup"><span data-stu-id="aa396-141">Experiment with queries interactively</span></span>

<span data-ttu-id="aa396-142">为了试验 JMESPath 表达式，你可能希望以一种可以快速编辑查询并检查输出的方式工作。</span><span class="sxs-lookup"><span data-stu-id="aa396-142">To experiment with JMESPath expressions, you might want to work in a way where you can quickly edit queries and inspect the output.</span></span> <span data-ttu-id="aa396-143">[JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python 包提供了一种交互式环境，允许通过管道传输数据作为输入并随后编写程序内查询来提取数据。</span><span class="sxs-lookup"><span data-stu-id="aa396-143">An interactive environment is offered by the [JMESPath-terminal](https://github.com/jmespath/jmespath.terminal) Python package, which allows for piping data as input and then writing in-program queries to extract the data.</span></span>

```bash
pip install jmespath-terminal
az vm list --output json | jpterm
```
