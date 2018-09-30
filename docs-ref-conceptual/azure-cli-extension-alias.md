---
title: Azure CLI 别名扩展
description: 如何使用 Azure CLI 别名扩展
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 47afede5cb1954ddd33f03fd4a6a6dc6c5ed7aee
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177923"
---
# <a name="the-azure-cli-alias-extension"></a><span data-ttu-id="fe9b1-103">Azure CLI 别名扩展</span><span class="sxs-lookup"><span data-stu-id="fe9b1-103">The Azure CLI alias extension</span></span>

<span data-ttu-id="fe9b1-104">使用别名扩展，用户可以通过使用现有命令定义自定义 Azure CLI 命令。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-104">The alias extension allows users to define custom commands for the Azure CLI by using existing commands.</span></span> <span data-ttu-id="fe9b1-105">别名允许快捷方式，因此可以简化工作流。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-105">Aliases help keep your workflow simple by allowing shortcuts.</span></span> <span data-ttu-id="fe9b1-106">由于别名由 Jinja2 模板引擎提供支持，它们甚至能够提供高级参数处理。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-106">Since aliases are powered by the Jinja2 template engine, they even offer advanced argument processing.</span></span>

> [!NOTE]
> <span data-ttu-id="fe9b1-107">别名扩展处于公共预览阶段。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-107">The Alias Extension is in public preview.</span></span> <span data-ttu-id="fe9b1-108">功能和配置文件格式可能发生变化。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-108">The features and configuration file format may change.</span></span>

## <a name="install-the-alias-extension"></a><span data-ttu-id="fe9b1-109">安装别名扩展</span><span class="sxs-lookup"><span data-stu-id="fe9b1-109">Install the alias extension</span></span>

<span data-ttu-id="fe9b1-110">为使用别名扩展而需安装的最低 Azure CLI 版本为 **2.0.28**。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-110">The minimum required Azure CLI version to use the alias extension is **2.0.28**.</span></span> <span data-ttu-id="fe9b1-111">若要检查 CLI 版本，请运行 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-111">To check your CLI version, run `az --version`.</span></span> <span data-ttu-id="fe9b1-112">如果需要更新安装，请按照[安装 Azure CLI](./install-azure-cli.md) 中的说明执行操作。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-112">If you need to update your installation,  follow the instructions in [Install the Azure CLI](./install-azure-cli.md).</span></span>

<span data-ttu-id="fe9b1-113">使用 [az extension add](/cli/azure/extension#az-extension-add) 命令安装该扩展。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-113">Install the extension with the [az extension add](/cli/azure/extension#az-extension-add) command.</span></span>

```azurecli-interactive
az extension add --name alias
```

<span data-ttu-id="fe9b1-114">使用 [az extension list](/cli/azure/extension#az-extension-list) 验证扩展安装。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-114">Verify the installation of the extension with [az extension list](/cli/azure/extension#az-extension-list).</span></span> <span data-ttu-id="fe9b1-115">如果该别名扩展已正确安装，它会列入命令输出。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-115">If the alias extension was installed properly, it's listed in the command output.</span></span>

```azurecli-interactive
az extension list --output table --query '[].{Name:name}'
```

```output
Name
------
alias
```

## <a name="keep-the-extension-up-to-date"></a><span data-ttu-id="fe9b1-116">使扩展保持最新</span><span class="sxs-lookup"><span data-stu-id="fe9b1-116">Keep the extension up-to-date</span></span>

<span data-ttu-id="fe9b1-117">该别名扩展处于活跃开发阶段，新版本将定期发布。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-117">The alias extension is under active development and new versions are released regularly.</span></span> <span data-ttu-id="fe9b1-118">更新 CLI 时不会安装新版本。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-118">New versions aren't installed when you update the CLI.</span></span> <span data-ttu-id="fe9b1-119">请使用 [az extension update](/cli/azure/extension#az-extension-update) 安装该扩展的更新。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-119">Install the updates for the extension with [az extension update](/cli/azure/extension#az-extension-update).</span></span>

```azurecli-interactive
az extension update --name alias
```

## <a name="manage-aliases-for-the-azure-cli"></a><span data-ttu-id="fe9b1-120">管理 Azure CLI 的别名</span><span class="sxs-lookup"><span data-stu-id="fe9b1-120">Manage aliases for the Azure CLI</span></span>

<span data-ttu-id="fe9b1-121">使用别名扩展可以创建和管理其他 CLI 命令的别名。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-121">The alias extension lets you create and manage aliases for other CLI commands.</span></span> <span data-ttu-id="fe9b1-122">若要查看所有可用命令和参数详细信息，请结合 `--help` 运行别名命令。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-122">To view all the available commands and parameter details, run the alias command with `--help`.</span></span>

```azurecli-interactive
az alias --help
```

## <a name="create-simple-alias-commands"></a><span data-ttu-id="fe9b1-123">创建简单的别名命令</span><span class="sxs-lookup"><span data-stu-id="fe9b1-123">Create simple alias commands</span></span>

<span data-ttu-id="fe9b1-124">别名的一个用途是缩短现有命令组或命令名称。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-124">One use of aliases is for shortening existing command groups or command names.</span></span> <span data-ttu-id="fe9b1-125">例如，可以将 `group` 命令组缩短为 `rg`，将 `list` 命令缩短为 `ls`。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-125">For example, you can shorten the `group` command group to `rg` and the `list` command to `ls`.</span></span>

```azurecli-interactive
az alias create --name rg --command group
az alias create --name ls --command list
```

<span data-ttu-id="fe9b1-126">这些新定义的别名现在可在其定义所在的任何位置使用。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-126">These newly defined aliases can now be used anywhere that their definition would be.</span></span>

```azurecli-interactive
az rg list
az rg ls
az vm ls
```

<span data-ttu-id="fe9b1-127">请不要将 `az` 包含为命令的一部分。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-127">Do not include `az` as part of the command.</span></span>

<span data-ttu-id="fe9b1-128">别名也可以是完整命令的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-128">Aliases can also be shortcuts for complete commands.</span></span> <span data-ttu-id="fe9b1-129">下一个示例在表输出中列出了可用资源组及其位置：</span><span class="sxs-lookup"><span data-stu-id="fe9b1-129">The next example lists available resource groups and their locations in table output:</span></span>

```azurecli-interactive
az alias create --name ls-groups --command "group list --query '[].{Name:name, Location:location}' --output table"
```

<span data-ttu-id="fe9b1-130">现在 `ls-groups` 可以像任何其他 CLI 命令一样运行。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-130">Now `ls-groups` can be run like any other CLI command.</span></span>

```azurecli-interactive
az ls-groups
```

## <a name="create-an-alias-command-with-arguments"></a><span data-ttu-id="fe9b1-131">使用参数创建别名命令</span><span class="sxs-lookup"><span data-stu-id="fe9b1-131">Create an alias command with arguments</span></span>

<span data-ttu-id="fe9b1-132">还可以将位置参数包含为别名中的 `{{ arg_name }}`，来将其添加到别名命令中。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-132">You can also add positional arguments to an alias command by including them as `{{ arg_name }}` in the alias name.</span></span> <span data-ttu-id="fe9b1-133">括号内的空格是必需的。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-133">The whitespace inside the braces is required.</span></span>

```azurecli-interactive
az alias create --name "alias_name {{ arg1 }} {{ arg2 }} ..." --command "invoke_including_args"
```

<span data-ttu-id="fe9b1-134">下一个示例别名演示如何使用位置参数获取 VM 的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-134">The next example alias shows how to use positional arguments to get the public IP address for a VM.</span></span>

```azurecli-interactive
az alias create \
    --name "get-vm-ip {{ resourceGroup }} {{ vmName }}" \
    --command "vm list-ip-addresses --resource-group {{ resourceGroup }} --name {{ vmName }}
        --query [0].virtualMachine.network.publicIpAddresses[0].ipAddress"
```

<span data-ttu-id="fe9b1-135">当运行此命令时，需要为位置参数提供值。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-135">When running this command, you give values to the positional arguments.</span></span>

```azurecli-interactive
az get-vm-ip MyResourceGroup MyVM
```

<span data-ttu-id="fe9b1-136">还可以在别名命令中使用环境变量，在运行时会评估这些环境变量。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-136">You can also use environment variables in aliased commands, which are evaluated at runtime.</span></span> <span data-ttu-id="fe9b1-137">下一个示例将添加 `create-rg` 别名，该别名在 `eastus` 中创建资源组，并且添加 `owner` 标记。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-137">The next example adds the `create-rg` alias, which creates a resource group in `eastus` and adds an `owner` tag.</span></span> <span data-ttu-id="fe9b1-138">此标记被分配了本地环境变量 `USER` 的值。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-138">This tag is assigned the value of the local environment variable `USER`.</span></span>

```azurecli-interactive
az alias create \
    --name "create-rg {{ groupName }}" \
    --command "group create --name {{ groupName }} --location eastus --tags owner=\$USER"
```

<span data-ttu-id="fe9b1-139">若要在别名命令中注册环境变量，必须转义美元符号 `$`。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-139">To register the environment variables inside the command of the alias, the dollar sign `$` must be escaped.</span></span>

## <a name="process-arguments-using-jinja2-templates"></a><span data-ttu-id="fe9b1-140">使用 Jinja2 模板处理参数</span><span class="sxs-lookup"><span data-stu-id="fe9b1-140">Process arguments using Jinja2 templates</span></span>

<span data-ttu-id="fe9b1-141">别名扩展中的参数替换由 [Jinja2](http://jinja.pocoo.org/docs/2.10/) 执行。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-141">Argument substitution in the alias extension is performed by [Jinja2](http://jinja.pocoo.org/docs/2.10/).</span></span> <span data-ttu-id="fe9b1-142">使用 Jinja2 模板可以操控参数。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-142">Jinja2 templates allow for manipulating the arguments.</span></span>

<span data-ttu-id="fe9b1-143">使用 Jinja2 模板可以编写接受与基础命令不同类型的参数的别名。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-143">With Jinja2 templates, you can write aliases that take different types of arguments than the underlying command.</span></span> <span data-ttu-id="fe9b1-144">例如，可以编写接受存储 URL 的别名。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-144">For example, you can make an alias that takes a storage URL.</span></span> <span data-ttu-id="fe9b1-145">然后，此 URL 将受到分析，以将帐户和容器名称传递给存储命令。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-145">Then this URL is parsed to pass the account and container names to the storage command.</span></span>

```azurecli-interactive
az alias create \
    --name 'storage-ls {{ url }}' \
    --command "storage blob list
        --account-name {{ url.replace('https://', '').split('.')[0] }}
        --container-name {{ url.replace('https://', '').split('/')[1] }}"
```

<span data-ttu-id="fe9b1-146">若要了解 Jinja2 模板引擎，请参阅 [Jinja2 文档](http://jinja.pocoo.org/docs/2.10/templates/)。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-146">To learn about the Jinja2 template engine, see [the Jinja2 documentation](http://jinja.pocoo.org/docs/2.10/templates/).</span></span>

## <a name="alias-configuration-file"></a><span data-ttu-id="fe9b1-147">别名配置文件</span><span class="sxs-lookup"><span data-stu-id="fe9b1-147">Alias configuration file</span></span>

<span data-ttu-id="fe9b1-148">创建和修改别名的另一种方法是更改别名配置文件。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-148">Another way to create and modify aliases is to alter the alias configuration file.</span></span> <span data-ttu-id="fe9b1-149">别名命令定义会写入位于 `$AZURE_USER_CONFIG/alias` 的配置文件中。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-149">Alias command definitions are written into a configuration file, located at `$AZURE_USER_CONFIG/alias`.</span></span> <span data-ttu-id="fe9b1-150">`AZURE_USER_CONFIG` 的默认值为 `$HOME/.azure`（在 macOS 与 Linux 上）和 `%USERPROFILE%\.azure`（在 Windows 上）。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-150">The default value of `AZURE_USER_CONFIG` is `$HOME/.azure` on macOS and Linux, and `%USERPROFILE%\.azure` on Windows.</span></span> <span data-ttu-id="fe9b1-151">别名配置文件以 INI 配置文件格式编写。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-151">The alias configuration file is written in the INI configuration file format.</span></span> <span data-ttu-id="fe9b1-152">别名命令的格式为：</span><span class="sxs-lookup"><span data-stu-id="fe9b1-152">The format for alias commands is:</span></span>

```ini
[alias_name]
command = invoked_commands
```

<span data-ttu-id="fe9b1-153">对于包含位置参数的别名，别名命令的格式为：</span><span class="sxs-lookup"><span data-stu-id="fe9b1-153">For aliases that have positional arguments, the format for alias commands is:</span></span>

```ini
[alias_name {{ arg1 }} {{ arg2 }} ...]
command = invoked_commands_including_args
```

## <a name="create-an-alias-command-with-arguments-via-the-alias-configuration-file"></a><span data-ttu-id="fe9b1-154">通过别名配置文件创建带有参数的别名命令</span><span class="sxs-lookup"><span data-stu-id="fe9b1-154">Create an alias command with arguments via the alias configuration file</span></span>

<span data-ttu-id="fe9b1-155">以下示例演示了包含参数的命令的别名。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-155">The next example shows an alias for a command with arguments.</span></span> <span data-ttu-id="fe9b1-156">此命令获取 VM 的公共 IP 地址。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-156">This command gets the public IP address for a VM.</span></span> <span data-ttu-id="fe9b1-157">别名命令必须在一行中输入，并在别名中使用所有参数。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-157">Aliased commands must all be on a single line, and use all of the arguments in the alias name.</span></span>

```ini
[get-vm-ip {{ resourceGroup }} {{ vmName }}]
command = vm list-ip-addresses --resource-group {{ resourceGroup }} --name {{ vmName }} --query [0].virtualMachine.network.publicIpAddresses[0].ipAddress
```

## <a name="uninstall-the-alias-extension"></a><span data-ttu-id="fe9b1-158">卸载别名扩展</span><span class="sxs-lookup"><span data-stu-id="fe9b1-158">Uninstall the alias extension</span></span>

<span data-ttu-id="fe9b1-159">若要卸载扩展，请使用 [az extension remove](/cli/azure/extension#az-extension-remove)命令。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-159">To uninstall the extension, use the [az extension remove](/cli/azure/extension#az-extension-remove) command.</span></span>

```azurecli-interactive
az extension remove --name alias
```

<span data-ttu-id="fe9b1-160">如果由于出现 bug 或其他扩展问题而卸载了该扩展，请[提出 GitHub 问题](https://github.com/Azure/azure-cli-extensions/issues)，以便我们可以提供修复。</span><span class="sxs-lookup"><span data-stu-id="fe9b1-160">If you uninstalled because a bug or other problem with the extension, [file a GitHub issue](https://github.com/Azure/azure-cli-extensions/issues) so that we can provide a fix.</span></span>
