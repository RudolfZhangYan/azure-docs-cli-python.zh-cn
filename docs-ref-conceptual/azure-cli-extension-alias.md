---
title: Azure CLI 2.0 别名扩展
description: 如何使用 Azure CLI 2.0 别名扩展
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/14/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: e457d78b1009fe573554df36db18f525516e0b4a
ms.sourcegitcommit: 335c11e6c34f7907e61a43507745ba84ed4e7469
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/05/2018
---
# <a name="the-azure-cli-20-alias-extension"></a><span data-ttu-id="0d46f-103">Azure CLI 2.0 别名扩展</span><span class="sxs-lookup"><span data-stu-id="0d46f-103">The Azure CLI 2.0 alias extension</span></span>

<span data-ttu-id="0d46f-104">使用别名扩展，用户可以通过使用现有命令定义自定义 Azure CLI 命令。</span><span class="sxs-lookup"><span data-stu-id="0d46f-104">The alias extension allows users to define custom commands for the Azure CLI by using existing commands.</span></span> <span data-ttu-id="0d46f-105">通过允许使用快捷方式并提供使用位置参数的能力，别名可帮助工作流保持简洁和简单。</span><span class="sxs-lookup"><span data-stu-id="0d46f-105">Aliases help keep your workflow concise and simple by allowing shortcuts and giving you the ability to use positional arguments.</span></span> <span data-ttu-id="0d46f-106">由于别名由 Jinja2 模板引擎提供支持，它们甚至能够提供高级参数处理。</span><span class="sxs-lookup"><span data-stu-id="0d46f-106">Since aliases are powered by the Jinja2 template engine, they even offer advanced argument processing.</span></span>

> [!NOTE]
> <span data-ttu-id="0d46f-107">别名扩展处于公共预览阶段。</span><span class="sxs-lookup"><span data-stu-id="0d46f-107">The Alias Extension is in public preview.</span></span> <span data-ttu-id="0d46f-108">功能和配置文件格式可能发生变化。</span><span class="sxs-lookup"><span data-stu-id="0d46f-108">The features and configuration file format may change.</span></span>

## <a name="install-the-alias-extension"></a><span data-ttu-id="0d46f-109">安装别名扩展</span><span class="sxs-lookup"><span data-stu-id="0d46f-109">Install the alias extension</span></span>

<span data-ttu-id="0d46f-110">为使用别名扩展而需安装的最低 Azure CLI 版本为 **2.0.28**。</span><span class="sxs-lookup"><span data-stu-id="0d46f-110">The minimum required Azure CLI version to use the alias extension is **2.0.28**.</span></span> <span data-ttu-id="0d46f-111">若要检查 CLI 版本，请运行 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="0d46f-111">To check your CLI version, run `az --version`.</span></span> <span data-ttu-id="0d46f-112">如果需要更新安装，请按照[安装 Azure CLI 2.0](./install-azure-cli.md) 中的说明执行操作。</span><span class="sxs-lookup"><span data-stu-id="0d46f-112">If you need to update your installation,  follow the instructions in [Install the Azure CLI 2.0](./install-azure-cli.md).</span></span>

<span data-ttu-id="0d46f-113">使用 [az extension add](/cli/azure/extension#az-extension-add) 命令安装该扩展。</span><span class="sxs-lookup"><span data-stu-id="0d46f-113">Install the extension with the [az extension add](/cli/azure/extension#az-extension-add) command.</span></span>

```azurecli
az extension add --name alias
```

<span data-ttu-id="0d46f-114">使用 [az extension list](/cli/azure/extension#az-extension-list) 验证扩展安装。</span><span class="sxs-lookup"><span data-stu-id="0d46f-114">Verify the installation of the extension with [az extension list](/cli/azure/extension#az-extension-list).</span></span> <span data-ttu-id="0d46f-115">如果该别名扩展已正确安装，它会列入命令输出。</span><span class="sxs-lookup"><span data-stu-id="0d46f-115">If the alias extension was installed properly, it's listed in the command output.</span></span>

```azurecli
az extension list --output table
```

```output
ExtensionType    Name                       Version
---------------  -------------------------  ---------
whl              alias                      0.2.0
```

## <a name="keep-the-extension-up-to-date"></a><span data-ttu-id="0d46f-116">使扩展保持最新</span><span class="sxs-lookup"><span data-stu-id="0d46f-116">Keep the extension up to date</span></span>

<span data-ttu-id="0d46f-117">该别名扩展处于活跃开发阶段，新版本将定期发布。</span><span class="sxs-lookup"><span data-stu-id="0d46f-117">The alias extension is under active development and new versions are released regularly.</span></span> <span data-ttu-id="0d46f-118">每当更新 CLI 时，新版本不会自动安装。</span><span class="sxs-lookup"><span data-stu-id="0d46f-118">New versions are not automatically installed whenever you update the CLI.</span></span> <span data-ttu-id="0d46f-119">请使用 [az extension update](/cli/azure/extension#az-extension-update) 安装该扩展的更新。</span><span class="sxs-lookup"><span data-stu-id="0d46f-119">Install the updates for the extension with [az extension update](/cli/azure/extension#az-extension-update).</span></span>

```azurecli
az extension update --name alias
```

## <a name="alias-commands-file-format"></a><span data-ttu-id="0d46f-120">别名命令文件格式</span><span class="sxs-lookup"><span data-stu-id="0d46f-120">Alias commands file format</span></span>

<span data-ttu-id="0d46f-121">别名命令定义会写入位于 `$AZURE_USER_CONFIG/alias` 的配置文件中。</span><span class="sxs-lookup"><span data-stu-id="0d46f-121">Alias command definitions are written into a configuration file, located at `$AZURE_USER_CONFIG/alias`.</span></span> <span data-ttu-id="0d46f-122">`AZURE_USER_CONFIG` 的默认值为 `$HOME/.azure`（在 macOS 与 Linux 上）和 `%USERPROFILE%\.azure`（在 Windows 上）。</span><span class="sxs-lookup"><span data-stu-id="0d46f-122">The default value of `AZURE_USER_CONFIG` is `$HOME/.azure` on macOS and Linux, and `%USERPROFILE%\.azure` on Windows.</span></span> <span data-ttu-id="0d46f-123">别名配置文件以 INI 配置文件格式编写。</span><span class="sxs-lookup"><span data-stu-id="0d46f-123">The alias configuration file is written in the INI configuration file format.</span></span> <span data-ttu-id="0d46f-124">别名命令的常规格式是：</span><span class="sxs-lookup"><span data-stu-id="0d46f-124">The general format for alias commands is:</span></span>

```
[command_name]
command = invoked_commands
```

<span data-ttu-id="0d46f-125">请不要将 `az` 包含为命令的一部分。</span><span class="sxs-lookup"><span data-stu-id="0d46f-125">Don't include `az` as part of the command.</span></span>

## <a name="create-simple-alias-commands"></a><span data-ttu-id="0d46f-126">创建简单的别名命令</span><span class="sxs-lookup"><span data-stu-id="0d46f-126">Create simple alias commands</span></span>

<span data-ttu-id="0d46f-127">别名的一个用途是缩短现有命令组或命令名称。</span><span class="sxs-lookup"><span data-stu-id="0d46f-127">One use of aliases is for shortening existing command groups or command names.</span></span> <span data-ttu-id="0d46f-128">例如，可以将 `group` 命令组缩短为 `rg`，将 `list` 命令缩短为 `ls`。</span><span class="sxs-lookup"><span data-stu-id="0d46f-128">For example, you can shorten the `group` command group to `rg` and the `list` command to `ls`.</span></span>

```
[rg]
command = group

[ls]
command = list
```

<span data-ttu-id="0d46f-129">这些新定义的别名现在可在其定义所在的任何位置使用。</span><span class="sxs-lookup"><span data-stu-id="0d46f-129">These newly defined aliases can now be used anywhere that their definition would be.</span></span>

```azurecli
az rg list
az rg ls
az vm ls
```

<span data-ttu-id="0d46f-130">别名也可以是完整命令的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="0d46f-130">Aliases can also be shortcuts for complete commands.</span></span> <span data-ttu-id="0d46f-131">下一个示例在表输出中列出了可用资源组及其位置：</span><span class="sxs-lookup"><span data-stu-id="0d46f-131">The next example lists available resource groups and their locations in table output:</span></span>

```
[ls-groups]
command = group list --query '[].{Name:name, Location:location}' --output table
```

<span data-ttu-id="0d46f-132">现在 `ls-groups` 可以像任何其他 CLI 命令一样运行。</span><span class="sxs-lookup"><span data-stu-id="0d46f-132">Now `ls-groups` can be run like any other CLI command.</span></span>

```azurecli
az ls-groups
```

## <a name="create-an-alias-command-with-arguments"></a><span data-ttu-id="0d46f-133">使用参数创建别名命令</span><span class="sxs-lookup"><span data-stu-id="0d46f-133">Create an alias command with arguments</span></span>

<span data-ttu-id="0d46f-134">还可以将位置参数包含为别名中的 `{{ arg_name }}`，来将其添加到别名命令中。</span><span class="sxs-lookup"><span data-stu-id="0d46f-134">You can also add positional arguments to an alias command by including them as `{{ arg_name }}` in the alias name.</span></span> <span data-ttu-id="0d46f-135">括号内的空格是必需的。</span><span class="sxs-lookup"><span data-stu-id="0d46f-135">The whitespace inside the braces is required.</span></span>

```
[alias_name {{ arg1 }} {{ arg2 }} ...]
command = invoke_including_args
```

<span data-ttu-id="0d46f-136">下一个示例别名演示如何使用位置参数获取 VM 的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="0d46f-136">The next example alias shows how to use positional arguments to get the public IP address for a VM.</span></span>

```
[get-vm-ip {{ resourceGroup }} {{ vmName }}]
command = vm list-ip-addresses --resource-group {{ resourceGroup }} --name {{ vmName }} --query [0].virtualMachine.network.publicIpAddresses[0].ipAddress
```

<span data-ttu-id="0d46f-137">当运行此命令时，需要为位置参数提供值。</span><span class="sxs-lookup"><span data-stu-id="0d46f-137">When running this command, you give values to the positional arguments.</span></span>

```azurecli
az get-vm-ip MyResourceGroup MyVM
```

<span data-ttu-id="0d46f-138">还可以在别名调用的命令中使用环境变量，这些变量在运行时将受到评估。</span><span class="sxs-lookup"><span data-stu-id="0d46f-138">You can also use environment variables in commands invoked by aliases, which are evaluated at runtime.</span></span> <span data-ttu-id="0d46f-139">下一个示例将添加 `create-rg` 别名，该别名在 `eastus` 中创建资源组，并且添加 `owner` 标记。</span><span class="sxs-lookup"><span data-stu-id="0d46f-139">The next example adds the `create-rg` alias, which creates a resource group in `eastus` and adds an `owner` tag.</span></span> <span data-ttu-id="0d46f-140">此标记被分配了本地环境变量 `USER` 的值。</span><span class="sxs-lookup"><span data-stu-id="0d46f-140">This tag is assigned the value of the local environment variable `USER`.</span></span>

```
[create-rg {{ groupName }}]
command = group create --name {{ groupName }} --location eastus --tags owner=$USER
```

## <a name="process-arguments-using-jinja2-templates"></a><span data-ttu-id="0d46f-141">使用 Jinja2 模板处理参数</span><span class="sxs-lookup"><span data-stu-id="0d46f-141">Process arguments using Jinja2 templates</span></span>

<span data-ttu-id="0d46f-142">别名扩展中的参数替换由 [Jinja2](http://jinja.pocoo.org/docs/2.10/) 执行，使你可以完全访问 Jinja2 模板引擎的功能。</span><span class="sxs-lookup"><span data-stu-id="0d46f-142">Argument substitution in the alias extension is performed by [Jinja2](http://jinja.pocoo.org/docs/2.10/), giving you full access to the capabilities of the Jinja2 template engine.</span></span> <span data-ttu-id="0d46f-143">模板可用于执行对字符串进行数据提取和替换之类的操作。</span><span class="sxs-lookup"><span data-stu-id="0d46f-143">Templates allow you to perform actions like data extraction and substitution on strings.</span></span>

<span data-ttu-id="0d46f-144">使用 Jinja2 模板，可以编写接受与基础命令不同类型的参数的别名。</span><span class="sxs-lookup"><span data-stu-id="0d46f-144">With Jinja2 templates, you can write aliases which take different types of arguments than the underlying command.</span></span> <span data-ttu-id="0d46f-145">例如，可以编写接受存储 URL 的别名。</span><span class="sxs-lookup"><span data-stu-id="0d46f-145">For example, you can make an alias which takes a storage URL.</span></span> <span data-ttu-id="0d46f-146">然后，此 URL 将受到分析，以将帐户和容器名称传递给存储命令。</span><span class="sxs-lookup"><span data-stu-id="0d46f-146">Then this URL is parsed to pass the account and container names to the storage command.</span></span>

```
[storage-ls {{ url }}]
command = storage blob list --account-name {{ url.replace('https://', '').split('.')[0] }} --container-name {{ url.replace('https://', '').split('/')[1] }}
```

<span data-ttu-id="0d46f-147">若要了解 Jinja2 模板引擎，请参阅 [Jinja2 文档](http://jinja.pocoo.org/docs/2.10/templates/)。</span><span class="sxs-lookup"><span data-stu-id="0d46f-147">To learn about the Jinja2 template engine, see [the Jinja2 documentation](http://jinja.pocoo.org/docs/2.10/templates/).</span></span>

## <a name="uninstall-the-alias-extension"></a><span data-ttu-id="0d46f-148">卸载别名扩展</span><span class="sxs-lookup"><span data-stu-id="0d46f-148">Uninstall the alias extension</span></span>

<span data-ttu-id="0d46f-149">若要卸载扩展，请使用 [az extension remove](/cli/azure/extension#az-extension-remove)命令。</span><span class="sxs-lookup"><span data-stu-id="0d46f-149">To uninstall the extension, use the [az extension remove](/cli/azure/extension#az-extension-remove) command.</span></span>

```azurecli
az extension remove --name alias
```

<span data-ttu-id="0d46f-150">如果是由于该扩展的 bug 或其他问题而进行了卸载，请[提出 GitHub 问题](https://github.com/Azure/azure-cli-extensions/issues)以便我们可以提供修复。</span><span class="sxs-lookup"><span data-stu-id="0d46f-150">If you uninstalled due to a bug or other problem with the extension, please [file a GitHub issue](https://github.com/Azure/azure-cli-extensions/issues) so that we can provide a fix.</span></span>
