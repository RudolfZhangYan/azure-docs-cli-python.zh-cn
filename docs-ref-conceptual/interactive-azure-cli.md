---
title: Azure CLI 2.0 交互模式
description: 以交互模式使用 Azure CLI 2.0。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 04/06/2017
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 6d7f88101ff20058766afdebf5f589e9c8a89d19
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="interactive-azure-cli-20"></a><span data-ttu-id="464c3-103">交互式 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="464c3-103">Interactive Azure CLI 2.0</span></span>

<span data-ttu-id="464c3-104">通过运行 `az interactive` 命令，能够以交互模式使用 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="464c3-104">You can use Azure CLI 2.0 in interactive mode by running the `az interactive` command.</span></span>
<span data-ttu-id="464c3-105">会进入交互式 shell，其中命令会自动完成，有权访问命令说明、参数说明和命令示例。</span><span class="sxs-lookup"><span data-stu-id="464c3-105">That places you in an interactive shell where your commands are auto-completed and you have access to descriptions of commands and their parameters and command examples.</span></span>

![交互模式](./media/interactive-azure-cli/webapp-create.png)

> [!NOTE]
> <span data-ttu-id="464c3-107">此处并未使用默认样式，也不会在黑色背景下读取。</span><span class="sxs-lookup"><span data-stu-id="464c3-107">We're not using the default style here, which doesn't read as well on a black background.</span></span>

<span data-ttu-id="464c3-108">如果尚未登录帐户，请使用 `login` 命令执行该操作。</span><span class="sxs-lookup"><span data-stu-id="464c3-108">If you're not already logged in to your account, use the `login` command to do that.</span></span>

## <a name="configure"></a><span data-ttu-id="464c3-109">配置</span><span class="sxs-lookup"><span data-stu-id="464c3-109">Configure</span></span>

<span data-ttu-id="464c3-110">交互模式会有选择性地显示命令说明、参数说明和命令示例。</span><span class="sxs-lookup"><span data-stu-id="464c3-110">Interactive mode optionally displays command descriptions, parameter descriptions, and command examples.</span></span>
<span data-ttu-id="464c3-111">使用 `F1` 可打开或关闭说明和示例。</span><span class="sxs-lookup"><span data-stu-id="464c3-111">You can turn descriptions and examples on or off using `F1`.</span></span>

![说明和示例](./media/interactive-azure-cli/descriptions-and-examples.png)

<span data-ttu-id="464c3-113">使用 `F2` 可打开或关闭参数默认值显示。</span><span class="sxs-lookup"><span data-stu-id="464c3-113">You can turn the display of parameter defaults on or off using `F2`.</span></span>

![默认值](./media/interactive-azure-cli/defaults.png)

<span data-ttu-id="464c3-115">使用 `F3` 可切换某些键笔势的显示。</span><span class="sxs-lookup"><span data-stu-id="464c3-115">`F3` toggles the display of some key gestures.</span></span>

![笔势](./media/interactive-azure-cli/gestures.png)

## <a name="scope"></a><span data-ttu-id="464c3-117">范围</span><span class="sxs-lookup"><span data-stu-id="464c3-117">Scope</span></span>

<span data-ttu-id="464c3-118">可将交互模式限定为特定命令组，如 `vm` 或 `vm image`。</span><span class="sxs-lookup"><span data-stu-id="464c3-118">You can scope your interactive mode to a specific command group like `vm` or `vm image`.</span></span>
<span data-ttu-id="464c3-119">执行此操作后，将解释此范围内的所有命令。</span><span class="sxs-lookup"><span data-stu-id="464c3-119">When you do, all commands are interpreted in that scope.</span></span>
<span data-ttu-id="464c3-120">如果完成了该命令组中的所有工作，说明这是很不错的简写形式。</span><span class="sxs-lookup"><span data-stu-id="464c3-120">It's a great shorthand if you're doing all your work in that command group.</span></span>

<span data-ttu-id="464c3-121">因此，不需要键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="464c3-121">Instead of typing these commands:</span></span>

```azurecli
az>> vm create -n myVM -g myRG --image UbuntuLTS
az>> vm list -o table
```

<span data-ttu-id="464c3-122">可将范围限定为 vm 命令组，然后键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="464c3-122">You can scope to the vm command group and type these commands:</span></span>

```azurecli
az>> %%vm
az vm>> create -n myVM -g myRG --image UbuntuLTS
az vm>>list -o table
```

<span data-ttu-id="464c3-123">也可将范围限定为较低级别的命令组。</span><span class="sxs-lookup"><span data-stu-id="464c3-123">You can scope to lower-level command groups as well.</span></span>
<span data-ttu-id="464c3-124">使用 `%%vm image` 可将范围限定为 `vm image`。</span><span class="sxs-lookup"><span data-stu-id="464c3-124">You could scope to `vm image` using `%%vm image`.</span></span>
<span data-ttu-id="464c3-125">在本例中，由于我们已将范围限定为 `vm`，因此使用 `%%image`。</span><span class="sxs-lookup"><span data-stu-id="464c3-125">In this case, since we're already scoped to `vm`, we would use `%%image`.</span></span>

```azurecli
az vm>> %%image
az vm image>>
```

<span data-ttu-id="464c3-126">此时，可使用 `%%..` 将范围限制为 `vm`，或者使用 `%%` 将范围限定到根。</span><span class="sxs-lookup"><span data-stu-id="464c3-126">At that point, we can pop the scope back up to `vm` using `%%..`, or we can scope to the root with just `%%`.</span></span>

```azurecli
az vm image>> %%
az>>
```

## <a name="query"></a><span data-ttu-id="464c3-127">查询</span><span class="sxs-lookup"><span data-stu-id="464c3-127">Query</span></span>

<span data-ttu-id="464c3-128">可针对上一次执行命令的结果执行 JMESPath 查询。</span><span class="sxs-lookup"><span data-stu-id="464c3-128">You can execute a JMESPath query on the results of the last command that you executed.</span></span>
<span data-ttu-id="464c3-129">例如，创建 VM 后，可确保它已完全设置。</span><span class="sxs-lookup"><span data-stu-id="464c3-129">For example, after you create a VM, you can make sure it has fully provisioned.</span></span>

```azurecli
az>> vm create --name myVM --resource-group myRG --image UbuntuLTS --no-wait
az>> ? [*].provisioningState
```

```
[
  "Creating"
]
```

<span data-ttu-id="464c3-130">若要深入了解如何查询命令结果，请参阅[使用 Azure 2.0 查询命令结果](query-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="464c3-130">To learn more about querying the results of your commands, see [Query command results with Azure 2.0](query-azure-cli.md).</span></span>

## <a name="bash-commands"></a><span data-ttu-id="464c3-131">Bash 命令</span><span class="sxs-lookup"><span data-stu-id="464c3-131">Bash commands</span></span>

<span data-ttu-id="464c3-132">使用 `#[cmd]`，无需退出交互模式即可运行 shell 命令。</span><span class="sxs-lookup"><span data-stu-id="464c3-132">You can run shell commands without leaving interactive mode using `#[cmd]`.</span></span>

```azurecli
az>> #dir
```

## <a name="examples"></a><span data-ttu-id="464c3-133">示例</span><span class="sxs-lookup"><span data-stu-id="464c3-133">Examples</span></span>

<span data-ttu-id="464c3-134">某些命令具有大量示例。</span><span class="sxs-lookup"><span data-stu-id="464c3-134">Some commands have lots of examples.</span></span>
<span data-ttu-id="464c3-135">使用 `CTRL-N` 可滚动到下一页示例，使用 `CTRL-Y` 可滚动到前一页。</span><span class="sxs-lookup"><span data-stu-id="464c3-135">You can scroll to the next page of examples using `CTRL-N` and the previous page using `CTRL-Y`.</span></span>

![示例](./media/interactive-azure-cli/examples.png)

<span data-ttu-id="464c3-137">还可使用 `::#` 查看特定示例。</span><span class="sxs-lookup"><span data-stu-id="464c3-137">You can also look at a specific example using `::#`.</span></span>

```azurecli
az>> vm create ::8
```
