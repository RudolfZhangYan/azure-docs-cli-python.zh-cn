---
title: Azure CLI 2.0 扩展
description: 将扩展与 Azure CLI 2.0 配合使用
keywords: Azure CLI, 扩展
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/15/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 5695d1df42689b315dd9d8783232ce35205a0a0e
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/28/2018
---
# <a name="using-extensions-with-the-azure-cli-20"></a><span data-ttu-id="840cd-104">将扩展与 Azure CLI 2.0 配合使用</span><span class="sxs-lookup"><span data-stu-id="840cd-104">Using extensions with the Azure CLI 2.0</span></span>

<span data-ttu-id="840cd-105">扩展是未随 Azure CLI 本身一起提供的单个模块，用于通过新命令添加功能。</span><span class="sxs-lookup"><span data-stu-id="840cd-105">Extensions are individual modules not shipped with the Azure CLI itself that add functionality through new commands.</span></span> <span data-ttu-id="840cd-106">这些扩展可能是实验性产品或预发布产品、Microsoft 提供的专用工具或你自己编写的自定义功能。</span><span class="sxs-lookup"><span data-stu-id="840cd-106">These might be experimental or pre-release offerings, specialized tools from Microsoft, or custom features you write yourself.</span></span> <span data-ttu-id="840cd-107">扩展使 CLI 可以有一定程度的灵活性，让你可以按自己的需求修改它，而无需随附许多不被视为核心功能集的一部分的其他包。</span><span class="sxs-lookup"><span data-stu-id="840cd-107">Extensions allow for a degree of flexibility with the CLI that let you modify it to your own needs, without having to ship a lot of additional packages that aren't considered part of the core feature set.</span></span>

<span data-ttu-id="840cd-108">本文将帮助了解如何安装、更新和删除 CLI 的扩展。</span><span class="sxs-lookup"><span data-stu-id="840cd-108">This article helps you understand how to install, update, and remove extensions for the CLI.</span></span> <span data-ttu-id="840cd-109">此外，还回答了有关扩展行为的常见问题。</span><span class="sxs-lookup"><span data-stu-id="840cd-109">It also answers common questions about extension behavior.</span></span>

## <a name="find-extensions"></a><span data-ttu-id="840cd-110">查找扩展</span><span class="sxs-lookup"><span data-stu-id="840cd-110">Find extensions</span></span>

<span data-ttu-id="840cd-111">若要了解有哪些扩展可用，可以使用 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available)。</span><span class="sxs-lookup"><span data-stu-id="840cd-111">In order to know what extensions are available, you can use [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az-extension-list-available).</span></span> <span data-ttu-id="840cd-112">此命令列出由 Microsoft 提供并维护的正式扩展。</span><span class="sxs-lookup"><span data-stu-id="840cd-112">This command lists the official extensions provided and maintained by Microsoft.</span></span>

```azurecli
az extension list-available --output table
```

<span data-ttu-id="840cd-113">我们还在文档站点上承载了 [Microsoft 扩展的列表](azure-cli-extensions-list.md)。</span><span class="sxs-lookup"><span data-stu-id="840cd-113">We also host a [list of Microsoft extensions](azure-cli-extensions-list.md) on the documentation site.</span></span>

## <a name="install-extensions"></a><span data-ttu-id="840cd-114">安装扩展</span><span class="sxs-lookup"><span data-stu-id="840cd-114">Install extensions</span></span>

<span data-ttu-id="840cd-115">找到要安装的扩展后，请使用 [az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-add) 获取它。</span><span class="sxs-lookup"><span data-stu-id="840cd-115">Once you have found an extension to install, use [az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-add) to get it.</span></span> <span data-ttu-id="840cd-116">如果该扩展在 `az extension list-available` 中列出，可以按名称安装该扩展。</span><span class="sxs-lookup"><span data-stu-id="840cd-116">If the extension is listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli
az extension add --name <extension-name>
```

<span data-ttu-id="840cd-117">如果此扩展来自外部资源，或者你有指向它的直接链接，则可以提供源 URL 或本地路径。</span><span class="sxs-lookup"><span data-stu-id="840cd-117">If the extension is from an external resource or you have a direct link to it, you can provide the source URL or local path.</span></span> <span data-ttu-id="840cd-118">这_必须_是已编译的 Python wheel 文件。</span><span class="sxs-lookup"><span data-stu-id="840cd-118">This _must_ be a compiled Python wheel file.</span></span>

```azurecli
az extension add --source <URL-or-path>
```

<span data-ttu-id="840cd-119">安装扩展后，可在 `$AZURE_EXTENSION_DIR` shell 变量的值下找到它。</span><span class="sxs-lookup"><span data-stu-id="840cd-119">Once an extension is installed, it can be found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="840cd-120">如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="840cd-120">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="update-extensions"></a><span data-ttu-id="840cd-121">更新扩展</span><span class="sxs-lookup"><span data-stu-id="840cd-121">Update extensions</span></span>

<span data-ttu-id="840cd-122">如果已按名称安装了扩展，可以使用 [az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-update) 更新该扩展。</span><span class="sxs-lookup"><span data-stu-id="840cd-122">If an extension was installed by name, it can be updated using [az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-update).</span></span>

```azurecli
az extension update --name <extension-name>
```

<span data-ttu-id="840cd-123">否则，可以按照[安装扩展](#install-extensions)说明，从源更新扩展。</span><span class="sxs-lookup"><span data-stu-id="840cd-123">Otherwise, an extension can be updated from source by following the [Install extensions](#install-extensions) instructions.</span></span>

<span data-ttu-id="840cd-124">如果扩展名无法由 CLI 解析，请将该扩展卸载，然后尝试重新安装。</span><span class="sxs-lookup"><span data-stu-id="840cd-124">If an extension name cannot be resolved by the CLI, uninstall it and attempt to reinstall.</span></span> <span data-ttu-id="840cd-125">此外，还存在扩展已脱离预览阶段并成为 CLI 内置命令的可能性。</span><span class="sxs-lookup"><span data-stu-id="840cd-125">There's also the possibility that the extension was moved out of preview and became a built-in command for the CLI.</span></span> <span data-ttu-id="840cd-126">请按照[安装 Azure CLI 2.0](install-azure-cli.md) 中的说明尝试更新 CLI，查看扩展的命令是否已添加。</span><span class="sxs-lookup"><span data-stu-id="840cd-126">Try updating the CLI as described in [Install the Azure CLI 2.0](install-azure-cli.md) and see if the extension's commands were added.</span></span> 

## <a name="uninstall-extensions"></a><span data-ttu-id="840cd-127">卸载扩展</span><span class="sxs-lookup"><span data-stu-id="840cd-127">Uninstall extensions</span></span>

<span data-ttu-id="840cd-128">如果不再需要某个扩展，可以使用 [az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-remove) 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="840cd-128">If you no longer need an extension, it can be removed with [az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az-extension-remove).</span></span>

```azurecli
az extension remove --name <extension-name>
```

<span data-ttu-id="840cd-129">还可以通过从安装扩展的位置删除它来进行手动删除。</span><span class="sxs-lookup"><span data-stu-id="840cd-129">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="840cd-130">这将是 `$AZURE_EXTENSION_DIR` shell 变量的值。</span><span class="sxs-lookup"><span data-stu-id="840cd-130">This will be the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="840cd-131">如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="840cd-131">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

<span data-ttu-id="840cd-132">建议使用 `az extension remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="840cd-132">It is recommended that you uninstall using `az extension remove`.</span></span>

## <a name="faq"></a><span data-ttu-id="840cd-133">常见问题</span><span class="sxs-lookup"><span data-stu-id="840cd-133">FAQ</span></span>

<span data-ttu-id="840cd-134">以下是一些有关 CLI 扩展的其他常见问题的答案。</span><span class="sxs-lookup"><span data-stu-id="840cd-134">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="840cd-135">安装允许哪些文件格式？</span><span class="sxs-lookup"><span data-stu-id="840cd-135">What file formats are allowed for installation?</span></span>

<span data-ttu-id="840cd-136">当前，只有编译的 Python wheel 才能作为扩展进行安装。</span><span class="sxs-lookup"><span data-stu-id="840cd-136">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="840cd-137">扩展是否可以替换现有命令？</span><span class="sxs-lookup"><span data-stu-id="840cd-137">Can extensions replace existing commands?</span></span>

<span data-ttu-id="840cd-138">是的。</span><span class="sxs-lookup"><span data-stu-id="840cd-138">Yes.</span></span> <span data-ttu-id="840cd-139">扩展可以替换现有命令，但在运行已替换的命令之前，CLI 会发出一个警告。</span><span class="sxs-lookup"><span data-stu-id="840cd-139">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="840cd-140">如何判断扩展是否处于预发布阶段？</span><span class="sxs-lookup"><span data-stu-id="840cd-140">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="840cd-141">如果处于预发布阶段，扩展应通过其自己的文档和版本控制进行指示。</span><span class="sxs-lookup"><span data-stu-id="840cd-141">An extension should indicate through its own documentation and versioning if it is in pre-release.</span></span> <span data-ttu-id="840cd-142">Microsoft 发布 CLI 的预览版命令作为扩展，计划在产品脱离预览阶段后将这些命令移到主 CLI 接口，也十分常见。</span><span class="sxs-lookup"><span data-stu-id="840cd-142">It is also common for Microsoft to release preview commands for the CLI as extensions, with plans to move them into the main CLI interface once the product is out of preview.</span></span>

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="840cd-143">扩展是否可以彼此依赖？</span><span class="sxs-lookup"><span data-stu-id="840cd-143">Can extensions depend upon each other?</span></span>

<span data-ttu-id="840cd-144">不会。</span><span class="sxs-lookup"><span data-stu-id="840cd-144">No.</span></span> <span data-ttu-id="840cd-145">扩展必须是不依赖于其他扩展的单个包。</span><span class="sxs-lookup"><span data-stu-id="840cd-145">Extensions must be individual packages which do not rely on one another.</span></span> <span data-ttu-id="840cd-146">这是因为 CLI 不能保证何时加载扩展，因此不能保证依赖关系使人满意。</span><span class="sxs-lookup"><span data-stu-id="840cd-146">This is because the CLI gives no guarantee about when extensions are loaded, so dependencies could not be guaranteed to be satisfied.</span></span> <span data-ttu-id="840cd-147">安装扩展将仅安装该扩展，并且它应继续工作，即使你删除其他扩展也是如此。</span><span class="sxs-lookup"><span data-stu-id="840cd-147">Installing an extension installs that extension only, and it should continue to work even if you remove other extensions.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="840cd-148">扩展是否随 CLI 一起更新？</span><span class="sxs-lookup"><span data-stu-id="840cd-148">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="840cd-149">不会。</span><span class="sxs-lookup"><span data-stu-id="840cd-149">No.</span></span> <span data-ttu-id="840cd-150">扩展必须单独更新，如[更新扩展](#update-extensions)所述。</span><span class="sxs-lookup"><span data-stu-id="840cd-150">Extensions must be updated separately, as described in [Update extensions](#update-extensions).</span></span>
