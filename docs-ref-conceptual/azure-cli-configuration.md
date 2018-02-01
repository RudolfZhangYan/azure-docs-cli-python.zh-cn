---
title: "Azure CLI 配置选项"
description: "如何配置 Azure CLI 2.0"
keywords: "Azure CLI, 配置, 设置, Azure"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 12/13/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: d60ede5b971ee2489482fb5a72bde9bf5389d37c
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="azure-cli-20-configuration"></a><span data-ttu-id="d8277-104">Azure CLI 2.0 配置</span><span class="sxs-lookup"><span data-stu-id="d8277-104">Azure CLI 2.0 configuration</span></span>

<span data-ttu-id="d8277-105">在 Azure CLI 2.0 中，可以使用用户配置来替代日志记录和数据收集等内部设置，并为某些必需参数提供默认选项。</span><span class="sxs-lookup"><span data-stu-id="d8277-105">The Azure CLI 2.0 allows for user configuration to override internal settings such as logging and data collection, and provide default options for some required parameters.</span></span> <span data-ttu-id="d8277-106">CLI 提供一个便捷的命令 `az configure` 用于管理其中的某些值；可在配置文件中或使用环境变量设置其他值。</span><span class="sxs-lookup"><span data-stu-id="d8277-106">The CLI offers a convenience command for managing some of these values, `az configure`, and other values can be set in a configuration file or with environment variables.</span></span>

<span data-ttu-id="d8277-107">CLI 使用的配置值按以下优先顺序计算，列表中位于较高顺序的项优先。</span><span class="sxs-lookup"><span data-stu-id="d8277-107">Configuration values used by the CLI are evaluted in the following precedence, with items higher on the list taking priority.</span></span>

1. <span data-ttu-id="d8277-108">命令行参数</span><span class="sxs-lookup"><span data-stu-id="d8277-108">Command-line parameters</span></span>
2. <span data-ttu-id="d8277-109">环境变量</span><span class="sxs-lookup"><span data-stu-id="d8277-109">Environment variables</span></span>
3. <span data-ttu-id="d8277-110">配置文件中的值，或使用 `az configure` 进行设置</span><span class="sxs-lookup"><span data-stu-id="d8277-110">Values in the configuration file or set with `az configure`</span></span>

## <a name="cli-configuration-with-az-configure"></a><span data-ttu-id="d8277-111">使用 az configure 进行 CLI 配置</span><span class="sxs-lookup"><span data-stu-id="d8277-111">CLI configuration with az configure</span></span>

<span data-ttu-id="d8277-112">使用 [az configure](/cli/azure/?view=azure-cli-latest#az_configure) 命令设置 CLI 的默认值。</span><span class="sxs-lookup"><span data-stu-id="d8277-112">You set defaults for the CLI with the [az configure](/cli/azure/?view=azure-cli-latest#az_configure) command.</span></span>
<span data-ttu-id="d8277-113">此命令采用一个参数 `--defaults`，即 `key=value` 对的空格分隔列表。</span><span class="sxs-lookup"><span data-stu-id="d8277-113">This command takes one argument, `--defaults`, which is a space-separated list of `key=value` pairs.</span></span> <span data-ttu-id="d8277-114">CLI 使用提供的值来取代所需的参数。</span><span class="sxs-lookup"><span data-stu-id="d8277-114">The provded values are used by the CLI in place of required arguments.</span></span>

<span data-ttu-id="d8277-115">下面是可以使用的键列表。</span><span class="sxs-lookup"><span data-stu-id="d8277-115">The following is a list of available keys that you can use.</span></span>

| <span data-ttu-id="d8277-116">名称</span><span class="sxs-lookup"><span data-stu-id="d8277-116">Name</span></span> | <span data-ttu-id="d8277-117">说明</span><span class="sxs-lookup"><span data-stu-id="d8277-117">Description</span></span> |
|------|-------------|
| <span data-ttu-id="d8277-118">group</span><span class="sxs-lookup"><span data-stu-id="d8277-118">group</span></span> | <span data-ttu-id="d8277-119">所有命令使用的默认资源组。</span><span class="sxs-lookup"><span data-stu-id="d8277-119">The default resource group to use for all commands.</span></span> |
| <span data-ttu-id="d8277-120">location</span><span class="sxs-lookup"><span data-stu-id="d8277-120">location</span></span> | <span data-ttu-id="d8277-121">所有命令使用的默认位置。</span><span class="sxs-lookup"><span data-stu-id="d8277-121">The default location to use for all commands.</span></span> |
| <span data-ttu-id="d8277-122">Web</span><span class="sxs-lookup"><span data-stu-id="d8277-122">web</span></span> | <span data-ttu-id="d8277-123">`az webapp` 命令使用的默认应用名称。</span><span class="sxs-lookup"><span data-stu-id="d8277-123">The default app name to use for `az webapp` commands.</span></span> |
| <span data-ttu-id="d8277-124">vm</span><span class="sxs-lookup"><span data-stu-id="d8277-124">vm</span></span> | <span data-ttu-id="d8277-125">`az vm` 命令使用的默认 VM 名称。</span><span class="sxs-lookup"><span data-stu-id="d8277-125">The default VM name to use for `az vm` commands.</span></span> |
| <span data-ttu-id="d8277-126">vmss</span><span class="sxs-lookup"><span data-stu-id="d8277-126">vmss</span></span> | <span data-ttu-id="d8277-127">`az vmss` 命令使用的默认 VMSS 名称。</span><span class="sxs-lookup"><span data-stu-id="d8277-127">The default VMSS name to use for  `az vmss` commands.</span></span> |
| <span data-ttu-id="d8277-128">acr</span><span class="sxs-lookup"><span data-stu-id="d8277-128">acr</span></span> | <span data-ttu-id="d8277-129">`az acr` 命令使用的默认容器注册表名称。</span><span class="sxs-lookup"><span data-stu-id="d8277-129">The default container registry name to use for `az acr` commands.</span></span> |
| <span data-ttu-id="d8277-130">acs</span><span class="sxs-lookup"><span data-stu-id="d8277-130">acs</span></span> | <span data-ttu-id="d8277-131">`az acs` 命令使用的默认容器服务名称。</span><span class="sxs-lookup"><span data-stu-id="d8277-131">The default container service name to use for `az acs` commands.</span></span> |

<span data-ttu-id="d8277-132">例如，可按如下所示设置所有命令的默认资源组和位置。</span><span class="sxs-lookup"><span data-stu-id="d8277-132">As an example, here's how you would set the default resource group and location for all commands.</span></span>

```azurecli
az configure --defaults "location=westus2 group=MyResourceGroup"
```

## <a name="cli-configuration-file"></a><span data-ttu-id="d8277-133">CLI 配置文件</span><span class="sxs-lookup"><span data-stu-id="d8277-133">CLI configuration file</span></span>

<span data-ttu-id="d8277-134">CLI 配置文件包含用于管理 CLI 行为的其他设置。</span><span class="sxs-lookup"><span data-stu-id="d8277-134">The CLI configuration file contains other settings that are used for managing CLI behavior.</span></span> <span data-ttu-id="d8277-135">配置文件本身位于 `$AZURE_CONFIG_DIR/config`。</span><span class="sxs-lookup"><span data-stu-id="d8277-135">The configuration file itself is located at `$AZURE_CONFIG_DIR/config`.</span></span> <span data-ttu-id="d8277-136">`AZURE_CONFIG_DIR` 的默认值为 `$HOME/.azure/config`（在 Linux 与 macOS 上）和 `%USERPROFILE%\.azure\config`（在 Windows 上）。</span><span class="sxs-lookup"><span data-stu-id="d8277-136">The default value of `AZURE_CONFIG_DIR` is `$HOME/.azure/config` on Linux and macOS, and `%USERPROFILE%\.azure\config` on Windows.</span></span>

<span data-ttu-id="d8277-137">配置文件是以 INI 文件格式编写的。</span><span class="sxs-lookup"><span data-stu-id="d8277-137">Configuration files are written in the INI file format.</span></span> <span data-ttu-id="d8277-138">这些文件包含以 `[section-name]` 标头开头的节，后接 `key=value` 条目的列表。</span><span class="sxs-lookup"><span data-stu-id="d8277-138">These files are made up of sections which start with a `[section-name]` header, followed by a list of `key=value` entries.</span></span> <span data-ttu-id="d8277-139">节名称区分大小写，而键名称则不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="d8277-139">Section names are case-sensitive and key names are not.</span></span>
<span data-ttu-id="d8277-140">注释是以 `#` 或 `;` 开头的任何行。</span><span class="sxs-lookup"><span data-stu-id="d8277-140">Comments are any line that begins with a `#` or `;`.</span></span> <span data-ttu-id="d8277-141">不允许内联注释。</span><span class="sxs-lookup"><span data-stu-id="d8277-141">Inline comments are not allowed.</span></span> <span data-ttu-id="d8277-142">布尔值不区分大小写，由以下值表示。</span><span class="sxs-lookup"><span data-stu-id="d8277-142">Booleans are case-insensitive, and are represented by the following values.</span></span>

* <span data-ttu-id="d8277-143">__True__：1、yes、true、on</span><span class="sxs-lookup"><span data-stu-id="d8277-143">__True__: 1, yes, true, on</span></span>
* <span data-ttu-id="d8277-144">__False__：0、no、false、off</span><span class="sxs-lookup"><span data-stu-id="d8277-144">__False__: 0, no, false, off</span></span>

<span data-ttu-id="d8277-145">以下示例 CLI 配置文件禁用任何确认提示，并设置在 `/var/log/azure` 目录中进行日志记录。</span><span class="sxs-lookup"><span data-stu-id="d8277-145">Here's an example of a CLI configuration file which disables any confirmation prompts and sets up logging to the `/var/log/azure` directory.</span></span>

```
[core]
disable_confirm_prompt=Yes

[logging]
enable_log_file=yes
log_dir=/var/log/azure
```

<span data-ttu-id="d8277-146">有关所有可用配置值及其含义的详细信息，请参阅下一部分。</span><span class="sxs-lookup"><span data-stu-id="d8277-146">See the next section for details on all of the available configuration values and what they mean.</span></span> <span data-ttu-id="d8277-147">有关 INI 文件格式的完整详细信息，请参阅 [INI 上的 Python 文档](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure)。</span><span class="sxs-lookup"><span data-stu-id="d8277-147">For the full details on the INI file format, see the [Python documentation on INI](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure).</span></span>

## <a name="cli-configuration-values-and-environment-variables"></a><span data-ttu-id="d8277-148">CLI 配置值和环境变量</span><span class="sxs-lookup"><span data-stu-id="d8277-148">CLI configuration values and environment variables</span></span>

<span data-ttu-id="d8277-149">下表包含可在配置文件中放置的所有节和选项名称。</span><span class="sxs-lookup"><span data-stu-id="d8277-149">The following table contains all of the sections and option names that can be placed in a configuration file.</span></span> <span data-ttu-id="d8277-150">可将其相应环境变量设置为 `AZURE_{section}_{name}`（全大写）。</span><span class="sxs-lookup"><span data-stu-id="d8277-150">Their corresponding environment variables can be set as `AZURE_{section}_{name}`, in all caps.</span></span> <span data-ttu-id="d8277-151">例如，可以在 `AZURE_BATCHAI_STORAGE_ACCOUNT` 变量中设置 `batchai` 节的 `storage_account` 默认值。</span><span class="sxs-lookup"><span data-stu-id="d8277-151">For example, you can set the `batchai` section's `storage_account` default in the `AZURE_BATCHAI_STORAGE_ACCOUNT` variable.</span></span>

<span data-ttu-id="d8277-152">具有可用默认值的任何值不一定要在命令行参数中出现，即使该值是必需的。</span><span class="sxs-lookup"><span data-stu-id="d8277-152">Any value with a default available does not have to be present in the command line arguments, even if it is required.</span></span>

| <span data-ttu-id="d8277-153">部分</span><span class="sxs-lookup"><span data-stu-id="d8277-153">Section</span></span> | <span data-ttu-id="d8277-154">名称</span><span class="sxs-lookup"><span data-stu-id="d8277-154">Name</span></span>      | <span data-ttu-id="d8277-155">Type</span><span class="sxs-lookup"><span data-stu-id="d8277-155">Type</span></span> | <span data-ttu-id="d8277-156">说明</span><span class="sxs-lookup"><span data-stu-id="d8277-156">Description</span></span>|
|---------|-----------|------|------------|
| <span data-ttu-id="d8277-157">__core__</span><span class="sxs-lookup"><span data-stu-id="d8277-157">__core__</span></span> | <span data-ttu-id="d8277-158">output</span><span class="sxs-lookup"><span data-stu-id="d8277-158">output</span></span> | <span data-ttu-id="d8277-159">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-159">string</span></span> | <span data-ttu-id="d8277-160">默认输出格式。</span><span class="sxs-lookup"><span data-stu-id="d8277-160">The default output format.</span></span> <span data-ttu-id="d8277-161">可以是 `json`、`jsonc`、`tsv` 或 `table`。</span><span class="sxs-lookup"><span data-stu-id="d8277-161">Can be one of `json`, `jsonc`, `tsv`, or `table`.</span></span> |
| | <span data-ttu-id="d8277-162">disable\_confirm\_prompt</span><span class="sxs-lookup"><span data-stu-id="d8277-162">disable\_confirm\_prompt</span></span> | <span data-ttu-id="d8277-163">布尔值</span><span class="sxs-lookup"><span data-stu-id="d8277-163">boolean</span></span> | <span data-ttu-id="d8277-164">启用/禁用确认提示。</span><span class="sxs-lookup"><span data-stu-id="d8277-164">Turn confirmation prompts on/off.</span></span> |
| | <span data-ttu-id="d8277-165">collect\_telemetry</span><span class="sxs-lookup"><span data-stu-id="d8277-165">collect\_telemetry</span></span> | <span data-ttu-id="d8277-166">布尔值</span><span class="sxs-lookup"><span data-stu-id="d8277-166">boolean</span></span> | <span data-ttu-id="d8277-167">允许 Microsoft 收集有关 CLI 使用情况的匿名数据。</span><span class="sxs-lookup"><span data-stu-id="d8277-167">Allow Microsoft to collect anonymous data on the usage of the CLI.</span></span> <span data-ttu-id="d8277-168">有关隐私信息，请参阅 [Azure CLI 2.0 使用条款](http://aka.ms/AzureCliLegal)。</span><span class="sxs-lookup"><span data-stu-id="d8277-168">For privacy information, see the [Azure CLI 2.0 Terms of Use](http://aka.ms/AzureCliLegal).</span></span> |
| <span data-ttu-id="d8277-169">__logging__</span><span class="sxs-lookup"><span data-stu-id="d8277-169">__logging__</span></span> | <span data-ttu-id="d8277-170">enable\_log\_file</span><span class="sxs-lookup"><span data-stu-id="d8277-170">enable\_log\_file</span></span> | <span data-ttu-id="d8277-171">布尔值</span><span class="sxs-lookup"><span data-stu-id="d8277-171">boolean</span></span> | <span data-ttu-id="d8277-172">启用/关闭日志记录。</span><span class="sxs-lookup"><span data-stu-id="d8277-172">Turn logging on/off.</span></span> |
| | <span data-ttu-id="d8277-173">log\_dir</span><span class="sxs-lookup"><span data-stu-id="d8277-173">log\_dir</span></span> | <span data-ttu-id="d8277-174">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-174">string</span></span> | <span data-ttu-id="d8277-175">要将日志写入到的目录。</span><span class="sxs-lookup"><span data-stu-id="d8277-175">The directory to write logs to.</span></span> <span data-ttu-id="d8277-176">默认为 `${AZURE_CONFIG_DIR}/logs`。</span><span class="sxs-lookup"><span data-stu-id="d8277-176">By default this is `${AZURE_CONFIG_DIR}/logs`.</span></span> |
| <span data-ttu-id="d8277-177">__storage__</span><span class="sxs-lookup"><span data-stu-id="d8277-177">__storage__</span></span> | <span data-ttu-id="d8277-178">connection\_string</span><span class="sxs-lookup"><span data-stu-id="d8277-178">connection\_string</span></span> | <span data-ttu-id="d8277-179">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-179">string</span></span> | <span data-ttu-id="d8277-180">`az storage` 命令使用的默认连接字符串。</span><span class="sxs-lookup"><span data-stu-id="d8277-180">The default connection string to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="d8277-181">帐户</span><span class="sxs-lookup"><span data-stu-id="d8277-181">account</span></span> | <span data-ttu-id="d8277-182">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-182">string</span></span> | <span data-ttu-id="d8277-183">`az storage` 命令使用的默认帐户名。</span><span class="sxs-lookup"><span data-stu-id="d8277-183">The default account name to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="d8277-184">key</span><span class="sxs-lookup"><span data-stu-id="d8277-184">key</span></span> | <span data-ttu-id="d8277-185">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-185">string</span></span> | <span data-ttu-id="d8277-186">`az storage` 命令使用的默认帐户密钥。</span><span class="sxs-lookup"><span data-stu-id="d8277-186">The default account key to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="d8277-187">sas\_token</span><span class="sxs-lookup"><span data-stu-id="d8277-187">sas\_token</span></span> | <span data-ttu-id="d8277-188">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-188">string</span></span> | <span data-ttu-id="d8277-189">`az storage` 命令使用的默认 SAS 令牌。</span><span class="sxs-lookup"><span data-stu-id="d8277-189">The default SAS token to use for `az storage` commands.</span></span> |
| <span data-ttu-id="d8277-190">__batchai__</span><span class="sxs-lookup"><span data-stu-id="d8277-190">__batchai__</span></span> | <span data-ttu-id="d8277-191">storage\_account</span><span class="sxs-lookup"><span data-stu-id="d8277-191">storage\_account</span></span> | <span data-ttu-id="d8277-192">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-192">string</span></span> | <span data-ttu-id="d8277-193">`az batchai` 命令使用的默认存储帐户。</span><span class="sxs-lookup"><span data-stu-id="d8277-193">The default storage account to use for `az batchai` commands.</span></span> |
| | <span data-ttu-id="d8277-194">storage\_key</span><span class="sxs-lookup"><span data-stu-id="d8277-194">storage\_key</span></span> | <span data-ttu-id="d8277-195">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-195">string</span></span> | <span data-ttu-id="d8277-196">`az batchai` 命令使用的默认存储密钥。</span><span class="sxs-lookup"><span data-stu-id="d8277-196">The default storage key to use for `az batchai` commands.</span></span> |
| <span data-ttu-id="d8277-197">__batch__</span><span class="sxs-lookup"><span data-stu-id="d8277-197">__batch__</span></span> | <span data-ttu-id="d8277-198">帐户</span><span class="sxs-lookup"><span data-stu-id="d8277-198">account</span></span> | <span data-ttu-id="d8277-199">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-199">string</span></span> | <span data-ttu-id="d8277-200">`az batch` 命令使用的默认 Azure Batch 帐户名。</span><span class="sxs-lookup"><span data-stu-id="d8277-200">The default Azure Batch account name to use for `az batch` commands.</span></span> |
| | <span data-ttu-id="d8277-201">access\_key</span><span class="sxs-lookup"><span data-stu-id="d8277-201">access\_key</span></span> | <span data-ttu-id="d8277-202">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-202">string</span></span> | <span data-ttu-id="d8277-203">`az batch` 命令使用的默认访问密钥。</span><span class="sxs-lookup"><span data-stu-id="d8277-203">The default access key to use for `az batch` commands.</span></span> <span data-ttu-id="d8277-204">只能与 `aad` 授权配合使用。</span><span class="sxs-lookup"><span data-stu-id="d8277-204">Only used with `aad` authorization.</span></span> |
| | <span data-ttu-id="d8277-205">endpoint</span><span class="sxs-lookup"><span data-stu-id="d8277-205">endpoint</span></span> | <span data-ttu-id="d8277-206">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-206">string</span></span> | <span data-ttu-id="d8277-207">`az batch` 命令要连接到的默认终结点。</span><span class="sxs-lookup"><span data-stu-id="d8277-207">The default endpoint to connect to for `az batch` commands.</span></span> |
| | <span data-ttu-id="d8277-208">auth\_mode</span><span class="sxs-lookup"><span data-stu-id="d8277-208">auth\_mode</span></span> | <span data-ttu-id="d8277-209">字符串</span><span class="sxs-lookup"><span data-stu-id="d8277-209">string</span></span> | <span data-ttu-id="d8277-210">`az batch` 命令使用的授权模式。</span><span class="sxs-lookup"><span data-stu-id="d8277-210">The authorization mode to use for `az batch` commands.</span></span> <span data-ttu-id="d8277-211">可以是 `shared_key` 或 `aad`。</span><span class="sxs-lookup"><span data-stu-id="d8277-211">Can be `shared_key` or `aad`.</span></span> |

> [!NOTE]
> <span data-ttu-id="d8277-212">配置文件中可能包含其他值，但这些值是直接通过 CLI 命令（包括 `az configure`）管理的。</span><span class="sxs-lookup"><span data-stu-id="d8277-212">You may see other values in your configuration file, but these are managed directly through CLI commands, including `az configure`.</span></span> <span data-ttu-id="d8277-213">你只能自行更改上表中列出的值。</span><span class="sxs-lookup"><span data-stu-id="d8277-213">The ones listed in the table above are the only values you should change yourself.</span></span>
