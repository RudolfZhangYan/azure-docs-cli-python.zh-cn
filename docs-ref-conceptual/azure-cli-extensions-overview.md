---
title: Azure CLI 2.0 扩展
description: 将扩展与 Azure CLI 2.0 配合使用
keywords: Azure CLI, 扩展
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/15/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 01d7b3d58bf24d5a30386564fb64630d4db055e3
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="using-extensions-with-the-azure-cli-20"></a>将扩展与 Azure CLI 2.0 配合使用

扩展是未随 Azure CLI 本身一起提供的单个模块，用于通过新命令添加功能。 这些扩展可能是实验性产品或预发布产品、Microsoft 提供的专用工具或你自己编写的自定义功能。 扩展使 CLI 可以有一定程度的灵活性，让你可以按自己的需求修改它，而无需随附许多不被视为核心功能集的一部分的其他包。

本文将帮助了解如何安装、更新和删除 CLI 的扩展。 此外，还回答了有关扩展行为的常见问题。

## <a name="find-extensions"></a>查找扩展

若要了解有哪些扩展可用，可以使用 [az extension list-available](/cli/azure/extension#az-extension-list-available)。 此命令列出由 Microsoft 提供并维护的正式扩展。

```azurecli
az extension list-available --output table
```

我们还在文档站点上承载了 [Microsoft 扩展的列表](azure-cli-extensions-list.md)。

## <a name="install-extensions"></a>安装扩展

找到要安装的扩展后，请使用 [az extension add](https://docs.microsoft.com/en-us/cli/azure/extension#az-extension-add) 获取它。 如果该扩展在 `az extension list-available` 中列出，可以按名称安装该扩展。

```azurecli
az extension add --name <extension-name>
```

如果此扩展来自外部资源，或者你有指向它的直接链接，则可以提供源 URL 或本地路径。 这_必须_是已编译的 Python wheel 文件。

```azurecli
az extension add --source <URL-or-path>
```

安装扩展后，可在 `$AZURE_EXTENSION_DIR` shell 变量的值下找到它。 如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。

## <a name="update-extensions"></a>更新扩展

如果已按名称安装了扩展，可以使用 [az extension update](https://docs.microsoft.com/en-us/cli/azure/extension#az-extension-update) 更新该扩展。

```azurecli
az extension update --name <extension-name>
```

否则，可以按照[安装扩展](#install-extensions)说明，从源更新扩展。

如果扩展名无法由 CLI 解析，请将该扩展卸载，然后尝试重新安装。 此外，还存在扩展已脱离预览阶段并成为 CLI 内置命令的可能性。 请按照[安装 Azure CLI 2.0](install-azure-cli.md) 中的说明尝试更新 CLI，查看扩展的命令是否已添加。 

## <a name="uninstall-extensions"></a>卸载扩展

如果不再需要某个扩展，可以使用 [az extension remove](https://docs.microsoft.com/en-us/cli/azure/extension#az-extension-remove) 进行卸载。

```azurecli
az extension remove --name <extension-name>
```

还可以通过从安装扩展的位置删除它来进行手动删除。 这将是 `$AZURE_EXTENSION_DIR` shell 变量的值。 如果此变量未设置，默认情况下在 Linux 和 macOS 上该值为 `$HOME/.azure/cliextensions`，在 Windows 上为 `%USERPROFILE%\.azure\cliextensions`。

```bash
rm -rf $AZURE_EXTENSION_DIR/<extension-name>
```

建议使用 `az extension remove` 进行卸载。

## <a name="faq"></a>常见问题

以下是一些有关 CLI 扩展的其他常见问题的答案。

### <a name="what-file-formats-are-allowed-for-installation"></a>安装允许哪些文件格式？

当前，只有编译的 Python wheel 才能作为扩展进行安装。

### <a name="can-extensions-replace-existing-commands"></a>扩展是否可以替换现有命令？

是的。 扩展可以替换现有命令，但在运行已替换的命令之前，CLI 会发出一个警告。

### <a name="how-can-i-tell-if-an-extension-is-in-pre-release"></a>如何判断扩展是否处于预发布阶段？

如果处于预发布阶段，扩展应通过其自己的文档和版本控制进行指示。 Microsoft 发布 CLI 的预览版命令作为扩展，计划在产品脱离预览阶段后将这些命令移到主 CLI 接口，也十分常见。

### <a name="can-extensions-depend-upon-each-other"></a>扩展是否可以彼此依赖？

不会。 扩展必须是不依赖于其他扩展的单个包。 这是因为 CLI 不能保证何时加载扩展，因此不能保证依赖关系使人满意。 安装扩展将仅安装该扩展，并且它应继续工作，即使你删除其他扩展也是如此。

### <a name="are-extensions-updated-along-with-the-cli"></a>扩展是否随 CLI 一起更新？

不会。 扩展必须单独更新，如[更新扩展](#update-extensions)所述。
