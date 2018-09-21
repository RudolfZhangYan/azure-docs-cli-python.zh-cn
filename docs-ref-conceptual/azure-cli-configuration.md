---
title: Azure CLI 配置选项
description: 如何配置 Azure CLI 2.0
keywords: Azure CLI, 配置, 设置, Azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 75ea347b0d4d018142a26bf985ee3639f2b79924
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388586"
---
# <a name="azure-cli-20-configuration"></a><span data-ttu-id="c5129-104">Azure CLI 2.0 配置</span><span class="sxs-lookup"><span data-stu-id="c5129-104">Azure CLI 2.0 configuration</span></span>

<span data-ttu-id="c5129-105">Azure CLI 2.0 允许用户配置日志记录、数据收集和默认参数值等设置。</span><span class="sxs-lookup"><span data-stu-id="c5129-105">The Azure CLI 2.0 allows for user configuration for settings such as logging, data collection, and default argument values.</span></span>
<span data-ttu-id="c5129-106">CLI 提供便捷命令 `az configure` 用于管理某些默认设置。</span><span class="sxs-lookup"><span data-stu-id="c5129-106">The CLI offers a convenience command for managing some defaults, `az configure`.</span></span> <span data-ttu-id="c5129-107">可在配置文件中或使用环境变量设置其他值。</span><span class="sxs-lookup"><span data-stu-id="c5129-107">Other values can be set in a configuration file or with environment variables.</span></span>

<span data-ttu-id="c5129-108">CLI 使用的配置值按以下优先顺序计算，列表中位于较高位置的项优先。</span><span class="sxs-lookup"><span data-stu-id="c5129-108">Configuration values used by the CLI are evaluated in the following precedence, with items higher on the list taking priority.</span></span>

1. <span data-ttu-id="c5129-109">命令行参数</span><span class="sxs-lookup"><span data-stu-id="c5129-109">Command-line parameters</span></span>
2. <span data-ttu-id="c5129-110">环境变量</span><span class="sxs-lookup"><span data-stu-id="c5129-110">Environment variables</span></span>
3. <span data-ttu-id="c5129-111">配置文件中的值，或使用 `az configure` 进行设置</span><span class="sxs-lookup"><span data-stu-id="c5129-111">Values in the configuration file or set with `az configure`</span></span>

## <a name="cli-configuration-with-az-configure"></a><span data-ttu-id="c5129-112">使用 az configure 进行 CLI 配置</span><span class="sxs-lookup"><span data-stu-id="c5129-112">CLI configuration with az configure</span></span>

<span data-ttu-id="c5129-113">使用 [az configure](/cli/azure/reference-index#az-configure) 命令设置 CLI 的默认值。</span><span class="sxs-lookup"><span data-stu-id="c5129-113">You set defaults for the CLI with the [az configure](/cli/azure/reference-index#az-configure) command.</span></span>
<span data-ttu-id="c5129-114">此命令采用一个参数 `--defaults`，即 `key=value` 对的空格分隔列表。</span><span class="sxs-lookup"><span data-stu-id="c5129-114">This command takes one argument, `--defaults`, which is a space-separated list of `key=value` pairs.</span></span> <span data-ttu-id="c5129-115">CLI 使用提供的值来取代所需的参数。</span><span class="sxs-lookup"><span data-stu-id="c5129-115">The provided values are used by the CLI in place of required arguments.</span></span>

<span data-ttu-id="c5129-116">下表列出了可用的配置键。</span><span class="sxs-lookup"><span data-stu-id="c5129-116">The following table contains a list of available configuration keys.</span></span>

| <span data-ttu-id="c5129-117">名称</span><span class="sxs-lookup"><span data-stu-id="c5129-117">Name</span></span> | <span data-ttu-id="c5129-118">Description</span><span class="sxs-lookup"><span data-stu-id="c5129-118">Description</span></span> |
|------|-------------|
| <span data-ttu-id="c5129-119">group</span><span class="sxs-lookup"><span data-stu-id="c5129-119">group</span></span> | <span data-ttu-id="c5129-120">所有命令使用的默认资源组。</span><span class="sxs-lookup"><span data-stu-id="c5129-120">The default resource group to use for all commands.</span></span> |
| <span data-ttu-id="c5129-121">location</span><span class="sxs-lookup"><span data-stu-id="c5129-121">location</span></span> | <span data-ttu-id="c5129-122">所有命令使用的默认位置。</span><span class="sxs-lookup"><span data-stu-id="c5129-122">The default location to use for all commands.</span></span> |
| <span data-ttu-id="c5129-123">Web</span><span class="sxs-lookup"><span data-stu-id="c5129-123">web</span></span> | <span data-ttu-id="c5129-124">`az webapp` 命令使用的默认应用名称。</span><span class="sxs-lookup"><span data-stu-id="c5129-124">The default app name to use for `az webapp` commands.</span></span> |
| <span data-ttu-id="c5129-125">vm</span><span class="sxs-lookup"><span data-stu-id="c5129-125">vm</span></span> | <span data-ttu-id="c5129-126">`az vm` 命令使用的默认 VM 名称。</span><span class="sxs-lookup"><span data-stu-id="c5129-126">The default VM name to use for `az vm` commands.</span></span> |
| <span data-ttu-id="c5129-127">vmss</span><span class="sxs-lookup"><span data-stu-id="c5129-127">vmss</span></span> | <span data-ttu-id="c5129-128">用于 `az vmss` 命令的默认虚拟机规模集 (VMSS) 名称。</span><span class="sxs-lookup"><span data-stu-id="c5129-128">The default virtual machine scale set (VMSS) name to use for  `az vmss` commands.</span></span> |
| <span data-ttu-id="c5129-129">acr</span><span class="sxs-lookup"><span data-stu-id="c5129-129">acr</span></span> | <span data-ttu-id="c5129-130">`az acr` 命令使用的默认容器注册表名称。</span><span class="sxs-lookup"><span data-stu-id="c5129-130">The default container registry name to use for `az acr` commands.</span></span> |

<span data-ttu-id="c5129-131">例如，可按如下所示设置所有命令的默认资源组和位置。</span><span class="sxs-lookup"><span data-stu-id="c5129-131">As an example, here's how you would set the default resource group and location for all commands.</span></span>

```azurecli-interactive
az configure --defaults location=westus2 group=MyResourceGroup
```

## <a name="cli-configuration-file"></a><span data-ttu-id="c5129-132">CLI 配置文件</span><span class="sxs-lookup"><span data-stu-id="c5129-132">CLI configuration file</span></span>

<span data-ttu-id="c5129-133">CLI 配置文件包含用于管理 CLI 行为的其他设置。</span><span class="sxs-lookup"><span data-stu-id="c5129-133">The CLI configuration file contains other settings that are used for managing CLI behavior.</span></span> <span data-ttu-id="c5129-134">配置文件本身位于 `$AZURE_CONFIG_DIR/config`。</span><span class="sxs-lookup"><span data-stu-id="c5129-134">The configuration file itself is located at `$AZURE_CONFIG_DIR/config`.</span></span> <span data-ttu-id="c5129-135">`AZURE_CONFIG_DIR` 的默认值为 `$HOME/.azure`（在 Linux 与 macOS 上）和 `%USERPROFILE%\.azure`（在 Windows 上）。</span><span class="sxs-lookup"><span data-stu-id="c5129-135">The default value of `AZURE_CONFIG_DIR` is `$HOME/.azure` on Linux and macOS, and `%USERPROFILE%\.azure` on Windows.</span></span>

<span data-ttu-id="c5129-136">配置文件是以 INI 文件格式编写的。</span><span class="sxs-lookup"><span data-stu-id="c5129-136">Configuration files are written in the INI file format.</span></span> <span data-ttu-id="c5129-137">此文件格式定义为节标头后接键-值项的列表。</span><span class="sxs-lookup"><span data-stu-id="c5129-137">This file format is defined by section headers, followed by a list of key-value entries.</span></span>

* <span data-ttu-id="c5129-138">节标头以 `[section-name]` 的形式写入。</span><span class="sxs-lookup"><span data-stu-id="c5129-138">Section headers are written as `[section-name]`.</span></span> <span data-ttu-id="c5129-139">节名称区分大小写。</span><span class="sxs-lookup"><span data-stu-id="c5129-139">Section names are case-sensitive.</span></span>
* <span data-ttu-id="c5129-140">项以 `key=value` 的形式写入。</span><span class="sxs-lookup"><span data-stu-id="c5129-140">Entries are written as `key=value`.</span></span> <span data-ttu-id="c5129-141">键名称不区分大小写。</span><span class="sxs-lookup"><span data-stu-id="c5129-141">Key names are not case-sensitive.</span></span>
* <span data-ttu-id="c5129-142">注释是以 `#` 或 `;` 开头的任何行。</span><span class="sxs-lookup"><span data-stu-id="c5129-142">Comments are any line that begins with a `#` or `;`.</span></span> <span data-ttu-id="c5129-143">不允许内联注释。</span><span class="sxs-lookup"><span data-stu-id="c5129-143">Inline comments are not allowed.</span></span>

<span data-ttu-id="c5129-144">布尔值不区分大小写，由以下值表示。</span><span class="sxs-lookup"><span data-stu-id="c5129-144">Booleans are case-insensitive, and are represented by the following values.</span></span>

* <span data-ttu-id="c5129-145">__True__：1、yes、true、on</span><span class="sxs-lookup"><span data-stu-id="c5129-145">__True__: 1, yes, true, on</span></span>
* <span data-ttu-id="c5129-146">__False__：0、no、false、off</span><span class="sxs-lookup"><span data-stu-id="c5129-146">__False__: 0, no, false, off</span></span>

<span data-ttu-id="c5129-147">以下示例 CLI 配置文件禁用任何确认提示，并设置在 `/var/log/azure` 目录中进行日志记录。</span><span class="sxs-lookup"><span data-stu-id="c5129-147">Here's an example of a CLI configuration file that disables any confirmation prompts and sets up logging to the `/var/log/azure` directory.</span></span>

```ini
[core]
disable_confirm_prompt=Yes

[logging]
enable_log_file=yes
log_dir=/var/log/azure
```

<span data-ttu-id="c5129-148">有关所有可用配置值及其含义的详细信息，请参阅下一部分。</span><span class="sxs-lookup"><span data-stu-id="c5129-148">See the next section for details on all of the available configuration values and what they mean.</span></span> <span data-ttu-id="c5129-149">有关 INI 文件格式的完整详细信息，请参阅 [INI 上的 Python 文档](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure)。</span><span class="sxs-lookup"><span data-stu-id="c5129-149">For the full details on the INI file format, see the [Python documentation on INI](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure).</span></span>

## <a name="cli-configuration-values-and-environment-variables"></a><span data-ttu-id="c5129-150">CLI 配置值和环境变量</span><span class="sxs-lookup"><span data-stu-id="c5129-150">CLI configuration values and environment variables</span></span>

<span data-ttu-id="c5129-151">下表包含可在配置文件中放置的所有节和选项名称。</span><span class="sxs-lookup"><span data-stu-id="c5129-151">The following table contains all of the sections and option names that can be placed in a configuration file.</span></span> <span data-ttu-id="c5129-152">将其相应环境变量设置为 `AZURE_{section}_{name}`（全大写）。</span><span class="sxs-lookup"><span data-stu-id="c5129-152">Their corresponding environment variables are set as `AZURE_{section}_{name}`, in all caps.</span></span> <span data-ttu-id="c5129-153">例如，在 `AZURE_BATCHAI_STORAGE_ACCOUNT` 变量中设置 `batchai` 的 `storage_account` 默认值。</span><span class="sxs-lookup"><span data-stu-id="c5129-153">For example, the `storage_account` default for `batchai` is set in the `AZURE_BATCHAI_STORAGE_ACCOUNT` variable.</span></span>

<span data-ttu-id="c5129-154">如果提供了默认值，则任何命令都不再需要该参数，</span><span class="sxs-lookup"><span data-stu-id="c5129-154">When you provide a default value, that argument is no longer required by any command.</span></span> <span data-ttu-id="c5129-155">而是改用默认值。</span><span class="sxs-lookup"><span data-stu-id="c5129-155">Instead, the default value is used.</span></span>

| <span data-ttu-id="c5129-156">部分</span><span class="sxs-lookup"><span data-stu-id="c5129-156">Section</span></span> | <span data-ttu-id="c5129-157">名称</span><span class="sxs-lookup"><span data-stu-id="c5129-157">Name</span></span>      | <span data-ttu-id="c5129-158">Type</span><span class="sxs-lookup"><span data-stu-id="c5129-158">Type</span></span> | <span data-ttu-id="c5129-159">Description</span><span class="sxs-lookup"><span data-stu-id="c5129-159">Description</span></span>|
|---------|-----------|------|------------|
| <span data-ttu-id="c5129-160">__core__</span><span class="sxs-lookup"><span data-stu-id="c5129-160">__core__</span></span> | <span data-ttu-id="c5129-161">output</span><span class="sxs-lookup"><span data-stu-id="c5129-161">output</span></span> | <span data-ttu-id="c5129-162">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-162">string</span></span> | <span data-ttu-id="c5129-163">默认输出格式。</span><span class="sxs-lookup"><span data-stu-id="c5129-163">The default output format.</span></span> <span data-ttu-id="c5129-164">可以是 `json`、`jsonc`、`tsv` 或 `table`。</span><span class="sxs-lookup"><span data-stu-id="c5129-164">Can be one of `json`, `jsonc`, `tsv`, or `table`.</span></span> |
| | <span data-ttu-id="c5129-165">disable\_confirm\_prompt</span><span class="sxs-lookup"><span data-stu-id="c5129-165">disable\_confirm\_prompt</span></span> | <span data-ttu-id="c5129-166">布尔值</span><span class="sxs-lookup"><span data-stu-id="c5129-166">boolean</span></span> | <span data-ttu-id="c5129-167">启用/禁用确认提示。</span><span class="sxs-lookup"><span data-stu-id="c5129-167">Turn confirmation prompts on/off.</span></span> |
| | <span data-ttu-id="c5129-168">collect\_telemetry</span><span class="sxs-lookup"><span data-stu-id="c5129-168">collect\_telemetry</span></span> | <span data-ttu-id="c5129-169">布尔值</span><span class="sxs-lookup"><span data-stu-id="c5129-169">boolean</span></span> | <span data-ttu-id="c5129-170">允许 Microsoft 收集有关 CLI 使用情况的匿名数据。</span><span class="sxs-lookup"><span data-stu-id="c5129-170">Allow Microsoft to collect anonymous data on the usage of the CLI.</span></span> <span data-ttu-id="c5129-171">有关隐私信息，请参阅 [Azure CLI 2.0 使用条款](https://aka.ms/AzureCliLegal)。</span><span class="sxs-lookup"><span data-stu-id="c5129-171">For privacy information, see the [Azure CLI 2.0 Terms of Use](https://aka.ms/AzureCliLegal).</span></span> |
| <span data-ttu-id="c5129-172">__logging__</span><span class="sxs-lookup"><span data-stu-id="c5129-172">__logging__</span></span> | <span data-ttu-id="c5129-173">enable\_log\_file</span><span class="sxs-lookup"><span data-stu-id="c5129-173">enable\_log\_file</span></span> | <span data-ttu-id="c5129-174">布尔值</span><span class="sxs-lookup"><span data-stu-id="c5129-174">boolean</span></span> | <span data-ttu-id="c5129-175">启用/关闭日志记录。</span><span class="sxs-lookup"><span data-stu-id="c5129-175">Turn logging on/off.</span></span> |
| | <span data-ttu-id="c5129-176">log\_dir</span><span class="sxs-lookup"><span data-stu-id="c5129-176">log\_dir</span></span> | <span data-ttu-id="c5129-177">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-177">string</span></span> | <span data-ttu-id="c5129-178">要将日志写入到的目录。</span><span class="sxs-lookup"><span data-stu-id="c5129-178">The directory to write logs to.</span></span> <span data-ttu-id="c5129-179">此值默认为 `${AZURE_CONFIG_DIR}/logs`。</span><span class="sxs-lookup"><span data-stu-id="c5129-179">By default this value is `${AZURE_CONFIG_DIR}/logs`.</span></span> |
| <span data-ttu-id="c5129-180">__storage__</span><span class="sxs-lookup"><span data-stu-id="c5129-180">__storage__</span></span> | <span data-ttu-id="c5129-181">connection\_string</span><span class="sxs-lookup"><span data-stu-id="c5129-181">connection\_string</span></span> | <span data-ttu-id="c5129-182">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-182">string</span></span> | <span data-ttu-id="c5129-183">`az storage` 命令使用的默认连接字符串。</span><span class="sxs-lookup"><span data-stu-id="c5129-183">The default connection string to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="c5129-184">帐户</span><span class="sxs-lookup"><span data-stu-id="c5129-184">account</span></span> | <span data-ttu-id="c5129-185">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-185">string</span></span> | <span data-ttu-id="c5129-186">`az storage` 命令使用的默认帐户名。</span><span class="sxs-lookup"><span data-stu-id="c5129-186">The default account name to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="c5129-187">key</span><span class="sxs-lookup"><span data-stu-id="c5129-187">key</span></span> | <span data-ttu-id="c5129-188">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-188">string</span></span> | <span data-ttu-id="c5129-189">`az storage` 命令使用的默认帐户密钥。</span><span class="sxs-lookup"><span data-stu-id="c5129-189">The default account key to use for `az storage` commands.</span></span> |
| | <span data-ttu-id="c5129-190">sas\_token</span><span class="sxs-lookup"><span data-stu-id="c5129-190">sas\_token</span></span> | <span data-ttu-id="c5129-191">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-191">string</span></span> | <span data-ttu-id="c5129-192">`az storage` 命令使用的默认 SAS 令牌。</span><span class="sxs-lookup"><span data-stu-id="c5129-192">The default SAS token to use for `az storage` commands.</span></span> |
| <span data-ttu-id="c5129-193">__batchai__</span><span class="sxs-lookup"><span data-stu-id="c5129-193">__batchai__</span></span> | <span data-ttu-id="c5129-194">storage\_account</span><span class="sxs-lookup"><span data-stu-id="c5129-194">storage\_account</span></span> | <span data-ttu-id="c5129-195">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-195">string</span></span> | <span data-ttu-id="c5129-196">`az batchai` 命令使用的默认存储帐户。</span><span class="sxs-lookup"><span data-stu-id="c5129-196">The default storage account to use for `az batchai` commands.</span></span> |
| | <span data-ttu-id="c5129-197">storage\_key</span><span class="sxs-lookup"><span data-stu-id="c5129-197">storage\_key</span></span> | <span data-ttu-id="c5129-198">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-198">string</span></span> | <span data-ttu-id="c5129-199">`az batchai` 命令使用的默认存储密钥。</span><span class="sxs-lookup"><span data-stu-id="c5129-199">The default storage key to use for `az batchai` commands.</span></span> |
| <span data-ttu-id="c5129-200">__batch__</span><span class="sxs-lookup"><span data-stu-id="c5129-200">__batch__</span></span> | <span data-ttu-id="c5129-201">帐户</span><span class="sxs-lookup"><span data-stu-id="c5129-201">account</span></span> | <span data-ttu-id="c5129-202">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-202">string</span></span> | <span data-ttu-id="c5129-203">`az batch` 命令使用的默认 Azure Batch 帐户名。</span><span class="sxs-lookup"><span data-stu-id="c5129-203">The default Azure Batch account name to use for `az batch` commands.</span></span> |
| | <span data-ttu-id="c5129-204">access\_key</span><span class="sxs-lookup"><span data-stu-id="c5129-204">access\_key</span></span> | <span data-ttu-id="c5129-205">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-205">string</span></span> | <span data-ttu-id="c5129-206">`az batch` 命令使用的默认访问密钥。</span><span class="sxs-lookup"><span data-stu-id="c5129-206">The default access key to use for `az batch` commands.</span></span> <span data-ttu-id="c5129-207">只能与 `aad` 授权配合使用。</span><span class="sxs-lookup"><span data-stu-id="c5129-207">Only used with `aad` authorization.</span></span> |
| | <span data-ttu-id="c5129-208">endpoint</span><span class="sxs-lookup"><span data-stu-id="c5129-208">endpoint</span></span> | <span data-ttu-id="c5129-209">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-209">string</span></span> | <span data-ttu-id="c5129-210">`az batch` 命令要连接到的默认终结点。</span><span class="sxs-lookup"><span data-stu-id="c5129-210">The default endpoint to connect to for `az batch` commands.</span></span> |
| | <span data-ttu-id="c5129-211">auth\_mode</span><span class="sxs-lookup"><span data-stu-id="c5129-211">auth\_mode</span></span> | <span data-ttu-id="c5129-212">字符串</span><span class="sxs-lookup"><span data-stu-id="c5129-212">string</span></span> | <span data-ttu-id="c5129-213">`az batch` 命令使用的授权模式。</span><span class="sxs-lookup"><span data-stu-id="c5129-213">The authorization mode to use for `az batch` commands.</span></span> <span data-ttu-id="c5129-214">可以是 `shared_key` 或 `aad`。</span><span class="sxs-lookup"><span data-stu-id="c5129-214">Can be `shared_key` or `aad`.</span></span> |

> [!NOTE]
> <span data-ttu-id="c5129-215">配置文件中可能包含其他值，但这些值是直接通过 CLI 命令（包括 `az configure`）管理的。</span><span class="sxs-lookup"><span data-stu-id="c5129-215">You may see other values in your configuration file, but these are managed directly through CLI commands, including `az configure`.</span></span> <span data-ttu-id="c5129-216">你只能自行更改上表中列出的值。</span><span class="sxs-lookup"><span data-stu-id="c5129-216">The ones listed in the table above are the only values you should change yourself.</span></span>