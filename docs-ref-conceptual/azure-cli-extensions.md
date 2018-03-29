---
title: Azure CLI 2.0 扩展
description: 将扩展与 Azure CLI 2.0 配合使用
keywords: Azure CLI, 扩展
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/13/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 548c06c64cc98598a2bd24bcc5959e59bffb4930
ms.sourcegitcommit: f57b5666523ef3642bee644eb0e0fe7085b3194a
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/27/2018
---
# <a name="using-extensions-with-the-azure-cli-20"></a><span data-ttu-id="dbe56-104">将扩展与 Azure CLI 2.0 配合使用</span><span class="sxs-lookup"><span data-stu-id="dbe56-104">Using extensions with the Azure CLI 2.0</span></span>

<span data-ttu-id="dbe56-105">扩展是未随 Azure CLI 本身一起提供的单个模块，用于通过新命令添加功能。</span><span class="sxs-lookup"><span data-stu-id="dbe56-105">Extensions are individual modules not shipped with the Azure CLI itself that add functionality through new commands.</span></span> <span data-ttu-id="dbe56-106">这些扩展可能是实验性产品或预发布产品、Microsoft 提供的专用工具或你自己编写的自定义功能。</span><span class="sxs-lookup"><span data-stu-id="dbe56-106">These might be experimental or pre-release offerings, specialized tools from Microsoft, or custom features you write yourself.</span></span> <span data-ttu-id="dbe56-107">扩展使 CLI 可以有一定程度的灵活性，让你可以按自己的需求修改它，而无需随附许多不被视为核心功能集的一部分的其他包。</span><span class="sxs-lookup"><span data-stu-id="dbe56-107">Extensions allow for a degree of flexibility with the CLI that let you modify it to your own needs, without having to ship a lot of additional packages that aren't considered part of the core feature set.</span></span>

<span data-ttu-id="dbe56-108">本文将帮助了解如何安装、更新和删除 CLI 的扩展。</span><span class="sxs-lookup"><span data-stu-id="dbe56-108">This article helps you understand how to install, update, and remove extensions for the CLI.</span></span> <span data-ttu-id="dbe56-109">它还会回答有关扩展行为的常见问题。</span><span class="sxs-lookup"><span data-stu-id="dbe56-109">It should also answer common questions about extension behavior.</span></span>

## <a name="finding-extensions"></a><span data-ttu-id="dbe56-110">查找扩展</span><span class="sxs-lookup"><span data-stu-id="dbe56-110">Finding extensions</span></span>

<span data-ttu-id="dbe56-111">若要了解有哪些扩展可用，可以使用 [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az_extension_list_available)。</span><span class="sxs-lookup"><span data-stu-id="dbe56-111">In order to know what extensions are available, you can use [az extension list-available](/cli/azure/extension?view=azure-cli-latest#az_extension_list_available).</span></span> <span data-ttu-id="dbe56-112">此命令列出 Microsoft 提供并支持的可用官方扩展。</span><span class="sxs-lookup"><span data-stu-id="dbe56-112">This command lists the available, official extensions which are provided and supported by Microsoft.</span></span>

## <a name="installing-extensions"></a><span data-ttu-id="dbe56-113">安装扩展</span><span class="sxs-lookup"><span data-stu-id="dbe56-113">Installing extensions</span></span>

<span data-ttu-id="dbe56-114">找到要安装的扩展后，请使用 [az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_add) 获取它。</span><span class="sxs-lookup"><span data-stu-id="dbe56-114">Once you have found an extension to install, use [az extension add](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_add) to get it.</span></span> <span data-ttu-id="dbe56-115">如果该扩展在 `az extension list-available` 中列出，可以按名称安装该扩展。</span><span class="sxs-lookup"><span data-stu-id="dbe56-115">If the extension is listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli
az extension add --name <extension-name>
```

<span data-ttu-id="dbe56-116">如果此扩展来自外部资源，或者你有指向它的直接链接，则可以提供源 URL 或本地路径。</span><span class="sxs-lookup"><span data-stu-id="dbe56-116">If the extension is from an external resource or you have a direct link to it, you can provide the source URL or local path.</span></span> <span data-ttu-id="dbe56-117">这_必须_是已编译的 Python wheel 文件。</span><span class="sxs-lookup"><span data-stu-id="dbe56-117">This _must_ be a compiled Python wheel file.</span></span>

```azurecli
az extension add --source <URL-or-path>
```

<span data-ttu-id="dbe56-118">安装扩展后，可在 `$AZURE_EXTENSION_DIR` shell 变量的值下找到它。</span><span class="sxs-lookup"><span data-stu-id="dbe56-118">Once an extension is installed, it can be found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="dbe56-119">如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="dbe56-119">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="updating-extensions"></a><span data-ttu-id="dbe56-120">更新扩展</span><span class="sxs-lookup"><span data-stu-id="dbe56-120">Updating extensions</span></span>

<span data-ttu-id="dbe56-121">扩展只能使用 [az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_update) 按名称更新。</span><span class="sxs-lookup"><span data-stu-id="dbe56-121">Extensions can only be updated by name, using [az extension update](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_update).</span></span>

```azurecli
az extension update --name <extension-name>
```

<span data-ttu-id="dbe56-122">无论什么原因，只要扩展名无法由 CLI 解析，请重新安装该扩展进行更新。</span><span class="sxs-lookup"><span data-stu-id="dbe56-122">If an extension name cannot be resolved by the CLI for whatever reason, reinstall the extension to update it.</span></span> <span data-ttu-id="dbe56-123">此外，还存在扩展已脱离预览阶段并成为 CLI 内置命令的可能性。</span><span class="sxs-lookup"><span data-stu-id="dbe56-123">There is also the possibility that the extension was moved out of preview and became a built-in command for the CLI.</span></span> <span data-ttu-id="dbe56-124">在这种情况下，请更新 CLI 并卸载扩展。</span><span class="sxs-lookup"><span data-stu-id="dbe56-124">In that case, update the CLI and uninstall the extension.</span></span>

## <a name="uninstalling-extensions"></a><span data-ttu-id="dbe56-125">卸载扩展</span><span class="sxs-lookup"><span data-stu-id="dbe56-125">Uninstalling extensions</span></span>

<span data-ttu-id="dbe56-126">如果不再需要某个扩展，可以使用 [az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_remove) 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="dbe56-126">If you no longer need an extension, it can be removed with [az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension?view=azure-cli-latest#az_extension_remove).</span></span>

```azurecli
az extension remove --name <extension-name>
```

<span data-ttu-id="dbe56-127">还可以通过从安装扩展的位置删除它来进行手动删除。</span><span class="sxs-lookup"><span data-stu-id="dbe56-127">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="dbe56-128">这将是 `$AZURE_EXTENSION_DIR` shell 变量的值。</span><span class="sxs-lookup"><span data-stu-id="dbe56-128">This will be the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="dbe56-129">如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="dbe56-129">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

<span data-ttu-id="dbe56-130">建议使用 `az extension remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="dbe56-130">It is recommended that you uninstall using `az extension remove`.</span></span>

## <a name="faq"></a><span data-ttu-id="dbe56-131">常见问题</span><span class="sxs-lookup"><span data-stu-id="dbe56-131">FAQ</span></span>

<span data-ttu-id="dbe56-132">以下是一些有关 CLI 扩展的其他常见问题的答案。</span><span class="sxs-lookup"><span data-stu-id="dbe56-132">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="dbe56-133">安装允许哪些文件格式？</span><span class="sxs-lookup"><span data-stu-id="dbe56-133">What file formats are allowed for installation?</span></span>

<span data-ttu-id="dbe56-134">当前，只有编译的 Python wheel 才能作为扩展进行安装。</span><span class="sxs-lookup"><span data-stu-id="dbe56-134">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="dbe56-135">扩展是否可以替换现有命令？</span><span class="sxs-lookup"><span data-stu-id="dbe56-135">Can extensions replace existing commands?</span></span>

<span data-ttu-id="dbe56-136">是的。</span><span class="sxs-lookup"><span data-stu-id="dbe56-136">Yes.</span></span> <span data-ttu-id="dbe56-137">扩展可以替换现有命令，但在运行已替换的命令之前，CLI 会发出一个警告。</span><span class="sxs-lookup"><span data-stu-id="dbe56-137">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="dbe56-138">如何判断扩展是否处于预发布阶段？</span><span class="sxs-lookup"><span data-stu-id="dbe56-138">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="dbe56-139">如果处于预发布阶段，扩展应通过其自己的文档和版本控制进行指示。</span><span class="sxs-lookup"><span data-stu-id="dbe56-139">An extension should indicate through its own documentation and versioning if it is in pre-release.</span></span> <span data-ttu-id="dbe56-140">Microsoft 发布 CLI 的预览版命令作为扩展，计划在产品脱离预览阶段后将这些命令移到主 CLI 接口，也十分常见。</span><span class="sxs-lookup"><span data-stu-id="dbe56-140">It is also common for Microsoft to release preview commands for the CLI as extensions, with plans to move them into the main CLI interface once the product is out of preview.</span></span>

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="dbe56-141">扩展是否可以彼此依赖？</span><span class="sxs-lookup"><span data-stu-id="dbe56-141">Can extensions depend upon each other?</span></span>

<span data-ttu-id="dbe56-142">不会。</span><span class="sxs-lookup"><span data-stu-id="dbe56-142">No.</span></span> <span data-ttu-id="dbe56-143">扩展必须是不依赖于其他扩展的单个包。</span><span class="sxs-lookup"><span data-stu-id="dbe56-143">Extensions must be individual packages which do not rely on one another.</span></span> <span data-ttu-id="dbe56-144">这是因为 CLI 不能保证何时加载扩展，因此不能保证依赖关系使人满意。</span><span class="sxs-lookup"><span data-stu-id="dbe56-144">This is because the CLI gives no guarantee about when extensions are loaded, so dependencies could not be guaranteed to be satisfied.</span></span> <span data-ttu-id="dbe56-145">安装扩展将仅安装该扩展，并且它应继续工作，即使你删除其他扩展也是如此。</span><span class="sxs-lookup"><span data-stu-id="dbe56-145">Installing an extension installs that extension only, and it should continue to work even if you remove other extensions.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="dbe56-146">扩展是否随 CLI 一起更新？</span><span class="sxs-lookup"><span data-stu-id="dbe56-146">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="dbe56-147">不会。</span><span class="sxs-lookup"><span data-stu-id="dbe56-147">No.</span></span> <span data-ttu-id="dbe56-148">扩展必须单独更新，如[更新扩展](#updating-extensions)部分所述。</span><span class="sxs-lookup"><span data-stu-id="dbe56-148">Extensions must be updated separately, as described in the [Updating extensions](#updating-extensions) section.</span></span>
