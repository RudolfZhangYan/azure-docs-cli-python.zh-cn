---
title: Azure CLI 扩展
description: 使用 Azure CLI 的扩展
keywords: Azure CLI, 扩展
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 0ba204063c00bf706f6af5a14dc59ba317385f95
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178110"
---
# <a name="use-extensions-with-azure-cli"></a><span data-ttu-id="1ab00-104">使用 Azure CLI 的扩展</span><span class="sxs-lookup"><span data-stu-id="1ab00-104">Use extensions with Azure CLI</span></span> 

<span data-ttu-id="1ab00-105">Azure CLI 提供用于加载扩展的功能。</span><span class="sxs-lookup"><span data-stu-id="1ab00-105">The Azure CLI offers the capability to load extensions.</span></span> <span data-ttu-id="1ab00-106">扩展属于 Python wheel，它们未随附在 CLI 中，而是作为 CLI 命令运行。</span><span class="sxs-lookup"><span data-stu-id="1ab00-106">Extensions are Python wheels that aren't shipped as part of the CLI but run as CLI commands.</span></span>
<span data-ttu-id="1ab00-107">使用扩展可以访问试验性命令和预发行的命令，以及编写自己的 CLI 接口。</span><span class="sxs-lookup"><span data-stu-id="1ab00-107">With extensions, you gain access to experimental and pre-release commands along with the ability to write your own CLI interfaces.</span></span> <span data-ttu-id="1ab00-108">本文介绍如何管理扩展，并解答有关其用法的常见问题。</span><span class="sxs-lookup"><span data-stu-id="1ab00-108">This article covers how to manage extensions and answers common questions about their use.</span></span>

## <a name="find-extensions"></a><span data-ttu-id="1ab00-109">查找扩展</span><span class="sxs-lookup"><span data-stu-id="1ab00-109">Find extensions</span></span>

<span data-ttu-id="1ab00-110">若要查看 Microsoft 提供和维护的扩展，请使用 [az extension list-available](/cli/azure/extension#az-extension-list-available) 命令。</span><span class="sxs-lookup"><span data-stu-id="1ab00-110">To see the extensions provided and maintained by Microsoft, use the [az extension list-available](/cli/azure/extension#az-extension-list-available) command.</span></span>

```azurecli-interactive
az extension list-available --output table
```

<span data-ttu-id="1ab00-111">我们还在文档站点上提供了[扩展列表](azure-cli-extensions-list.md)。</span><span class="sxs-lookup"><span data-stu-id="1ab00-111">We also host a [list of extensions](azure-cli-extensions-list.md) on the documentation site.</span></span>

## <a name="install-extensions"></a><span data-ttu-id="1ab00-112">安装扩展</span><span class="sxs-lookup"><span data-stu-id="1ab00-112">Install extensions</span></span>

<span data-ttu-id="1ab00-113">找到要安装的扩展后，请使用 [az extension add](https://docs.microsoft.com/cli/azure/extension#az-extension-add) 获取它。</span><span class="sxs-lookup"><span data-stu-id="1ab00-113">Once you have found an extension to install, use [az extension add](https://docs.microsoft.com/cli/azure/extension#az-extension-add) to get it.</span></span> <span data-ttu-id="1ab00-114">如果该扩展在 `az extension list-available` 中列出，可以按名称安装该扩展。</span><span class="sxs-lookup"><span data-stu-id="1ab00-114">If the extension is listed in `az extension list-available`, you can install the extension by name.</span></span>

```azurecli-interactive
az extension add --name <extension-name>
```

<span data-ttu-id="1ab00-115">如果此扩展来自外部资源，或者你有指向它的直接链接，则可以提供源 URL 或本地路径。</span><span class="sxs-lookup"><span data-stu-id="1ab00-115">If the extension is from an external resource or you have a direct link to it, provide the source URL or local path.</span></span> <span data-ttu-id="1ab00-116">该扩展必须是已编译的 Python wheel 文件。</span><span class="sxs-lookup"><span data-stu-id="1ab00-116">The extension _must_ be a compiled Python wheel file.</span></span>

```azurecli-interactive
az extension add --source <URL-or-path>
```

<span data-ttu-id="1ab00-117">安装扩展后，可在 `$AZURE_EXTENSION_DIR` shell 变量的值下找到它。</span><span class="sxs-lookup"><span data-stu-id="1ab00-117">Once an extension is installed, it's found under the value of the `$AZURE_EXTENSION_DIR` shell variable.</span></span> <span data-ttu-id="1ab00-118">如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="1ab00-118">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

## <a name="update-extensions"></a><span data-ttu-id="1ab00-119">更新扩展</span><span class="sxs-lookup"><span data-stu-id="1ab00-119">Update extensions</span></span>

<span data-ttu-id="1ab00-120">如果已按名称安装了扩展，可以使用 [az extension update](https://docs.microsoft.com/cli/azure/extension#az-extension-update) 更新该扩展。</span><span class="sxs-lookup"><span data-stu-id="1ab00-120">If an extension was installed by name, update it using [az extension update](https://docs.microsoft.com/cli/azure/extension#az-extension-update).</span></span>

```azurecli-interactive
az extension update --name <extension-name>
```

<span data-ttu-id="1ab00-121">否则，可以按照[安装扩展](#install-extensions)说明，从源更新扩展。</span><span class="sxs-lookup"><span data-stu-id="1ab00-121">Otherwise, an extension can be updated from source by following the [Install extensions](#install-extensions) instructions.</span></span>

<span data-ttu-id="1ab00-122">如果扩展名称无法由 CLI 解析，请卸载该扩展，然后尝试重新安装。</span><span class="sxs-lookup"><span data-stu-id="1ab00-122">If an extension name can't be resolved by the CLI, uninstall it and attempt to reinstall.</span></span> <span data-ttu-id="1ab00-123">该扩展也可能属于基本 CLI。</span><span class="sxs-lookup"><span data-stu-id="1ab00-123">The extension could also have become part of the base CLI.</span></span>
<span data-ttu-id="1ab00-124">请按照[安装 Azure CLI](install-azure-cli.md) 中的说明尝试更新 CLI，并查看扩展的命令是否已添加。</span><span class="sxs-lookup"><span data-stu-id="1ab00-124">Try updating the CLI as described in [Install the Azure CLI](install-azure-cli.md) and see if the extension's commands were added.</span></span>

## <a name="uninstall-extensions"></a><span data-ttu-id="1ab00-125">卸载扩展</span><span class="sxs-lookup"><span data-stu-id="1ab00-125">Uninstall extensions</span></span>

<span data-ttu-id="1ab00-126">如果不再需要某个扩展，请使用 [az extension remove](https://docs.microsoft.com/cli/azure/extension#az-extension-remove) 将其卸载。</span><span class="sxs-lookup"><span data-stu-id="1ab00-126">If you no longer need an extension, remove it with [az extension remove](https://docs.microsoft.com/cli/azure/extension#az-extension-remove).</span></span>

```azurecli-interactive
az extension remove --name <extension-name>
```

<span data-ttu-id="1ab00-127">还可以通过从安装扩展的位置删除它来进行手动删除。</span><span class="sxs-lookup"><span data-stu-id="1ab00-127">You can also remove an extension manually by deleting it from the location where it was installed.</span></span> <span data-ttu-id="1ab00-128">`$AZURE_EXTENSION_DIR` shell 变量定义模块的安装位置。</span><span class="sxs-lookup"><span data-stu-id="1ab00-128">The `$AZURE_EXTENSION_DIR` shell variable defines where modules are installed.</span></span>
<span data-ttu-id="1ab00-129">如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。</span><span class="sxs-lookup"><span data-stu-id="1ab00-129">If this variable is unset, by default the value is `$HOME/.azure/cliextensions` on Linux and macOS, and `%USERPROFILE%\.azure\cliextensions` on Windows.</span></span>

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

## <a name="faq"></a><span data-ttu-id="1ab00-130">常见问题解答</span><span class="sxs-lookup"><span data-stu-id="1ab00-130">FAQ</span></span>

<span data-ttu-id="1ab00-131">以下是一些有关 CLI 扩展的其他常见问题的答案。</span><span class="sxs-lookup"><span data-stu-id="1ab00-131">Here are some answers to other common questions about CLI extensions.</span></span>

### <a name="what-file-formats-are-allowed-for-installation"></a><span data-ttu-id="1ab00-132">安装允许哪些文件格式？</span><span class="sxs-lookup"><span data-stu-id="1ab00-132">What file formats are allowed for installation?</span></span>

<span data-ttu-id="1ab00-133">当前，只有编译的 Python wheel 才能作为扩展进行安装。</span><span class="sxs-lookup"><span data-stu-id="1ab00-133">Currently, only compiled Python wheels can be installed as extensions.</span></span>

### <a name="can-extensions-replace-existing-commands"></a><span data-ttu-id="1ab00-134">扩展是否可以替换现有命令？</span><span class="sxs-lookup"><span data-stu-id="1ab00-134">Can extensions replace existing commands?</span></span>

<span data-ttu-id="1ab00-135">是的。</span><span class="sxs-lookup"><span data-stu-id="1ab00-135">Yes.</span></span> <span data-ttu-id="1ab00-136">扩展可以替换现有命令，但在运行已替换的命令之前，CLI 会发出一个警告。</span><span class="sxs-lookup"><span data-stu-id="1ab00-136">Extensions may replace existing commands, but before running a command that has been replaced the CLI will issue a warning.</span></span>

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a><span data-ttu-id="1ab00-137">如何判断扩展是否处于预发布阶段？</span><span class="sxs-lookup"><span data-stu-id="1ab00-137">How can I tell if an extension is in pre-release?</span></span>

<span data-ttu-id="1ab00-138">扩展的文档和版本将显示该扩展是否是预发行版。</span><span class="sxs-lookup"><span data-stu-id="1ab00-138">An extension's documentation and versioning will show if it's in pre-release.</span></span> <span data-ttu-id="1ab00-139">Microsoft 通常以 CLI 扩展的形式发布预览版命令，以后会提供相应的选项用于将这些命令移到主要 CLI 产品中。</span><span class="sxs-lookup"><span data-stu-id="1ab00-139">Microsoft often releases preview commands as CLI extensions, with the option of moving them into the main CLI product later.</span></span> <span data-ttu-id="1ab00-140">将命令转出扩展后，应卸载旧扩展。</span><span class="sxs-lookup"><span data-stu-id="1ab00-140">When commands are moved out of extensions, the old extension should be uninstalled.</span></span> 

### <a name="can-extensions-depend-upon-each-other"></a><span data-ttu-id="1ab00-141">扩展是否可以彼此依赖？</span><span class="sxs-lookup"><span data-stu-id="1ab00-141">Can extensions depend upon each other?</span></span>

<span data-ttu-id="1ab00-142">不是。</span><span class="sxs-lookup"><span data-stu-id="1ab00-142">No.</span></span> <span data-ttu-id="1ab00-143">由于 CLI 不能保证加载顺序，因此可能无法满足依赖关系方面的要求。</span><span class="sxs-lookup"><span data-stu-id="1ab00-143">Since the CLI doesn't guarantee a load order, dependencies might not be satisfied.</span></span> <span data-ttu-id="1ab00-144">删除一个扩展不会影响其他任何扩展。</span><span class="sxs-lookup"><span data-stu-id="1ab00-144">Removing an extension won't affect any others.</span></span>

### <a name="are-extensions-updated-along-with-the-cli"></a><span data-ttu-id="1ab00-145">扩展是否随 CLI 一起更新？</span><span class="sxs-lookup"><span data-stu-id="1ab00-145">Are extensions updated along with the CLI?</span></span>

<span data-ttu-id="1ab00-146">不是。</span><span class="sxs-lookup"><span data-stu-id="1ab00-146">No.</span></span> <span data-ttu-id="1ab00-147">扩展必须单独更新，如[更新扩展](#update-extensions)所述。</span><span class="sxs-lookup"><span data-stu-id="1ab00-147">Extensions must be updated separately, as described in [Update extensions](#update-extensions).</span></span>
