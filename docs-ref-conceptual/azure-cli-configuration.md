---
title: Azure CLI 配置选项
description: 如何配置 Azure CLI 2.0
keywords: Azure CLI, 配置, 设置, Azure
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 12/13/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 7ef6175815014ac3f822e8c1038b4f5af8bba9dc
ms.sourcegitcommit: c9da729f4a42a839f13106f7589deaa0ca19cc4e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/06/2018
---
# <a name="azure-cli-20-configuration"></a>Azure CLI 2.0 配置

在 Azure CLI 2.0 中，可以使用用户配置来替代日志记录和数据收集等内部设置，并为某些必需参数提供默认选项。 CLI 提供一个便捷的命令 `az configure` 用于管理其中的某些值；可在配置文件中或使用环境变量设置其他值。

CLI 使用的配置值按以下优先顺序计算，列表中位于较高顺序的项优先。

1. 命令行参数
2. 环境变量
3. 配置文件中的值，或使用 `az configure` 进行设置

## <a name="cli-configuration-with-az-configure"></a>使用 az configure 进行 CLI 配置

使用 [az configure](/cli/azure/reference-index#az-configure) 命令设置 CLI 的默认值。
此命令采用一个参数 `--defaults`，即 `key=value` 对的空格分隔列表。 CLI 使用提供的值来取代所需的参数。

下面是可以使用的键列表。

| 名称 | 说明 |
|------|-------------|
| group | 所有命令使用的默认资源组。 |
| location | 所有命令使用的默认位置。 |
| Web | `az webapp` 命令使用的默认应用名称。 |
| vm | `az vm` 命令使用的默认 VM 名称。 |
| vmss | `az vmss` 命令使用的默认 VMSS 名称。 |
| acr | `az acr` 命令使用的默认容器注册表名称。 |
| acs | `az acs` 命令使用的默认容器服务名称。 |

例如，可按如下所示设置所有命令的默认资源组和位置。

```azurecli
az configure --defaults location=westus2 group=MyResourceGroup
```

## <a name="cli-configuration-file"></a>CLI 配置文件

CLI 配置文件包含用于管理 CLI 行为的其他设置。 配置文件本身位于 `$AZURE_CONFIG_DIR/config`。 `AZURE_CONFIG_DIR` 的默认值为 `$HOME/.azure`（在 Linux 与 macOS 上）和 `%USERPROFILE%\.azure`（在 Windows 上）。

配置文件是以 INI 文件格式编写的。 这些文件包含以 `[section-name]` 标头开头的节，后接 `key=value` 条目的列表。 节名称区分大小写，而键名称则不区分大小写。
注释是以 `#` 或 `;` 开头的任何行。 不允许内联注释。 布尔值不区分大小写，由以下值表示。

* __True__：1、yes、true、on
* __False__：0、no、false、off

以下示例 CLI 配置文件禁用任何确认提示，并设置在 `/var/log/azure` 目录中进行日志记录。

```
[core]
disable_confirm_prompt=Yes

[logging]
enable_log_file=yes
log_dir=/var/log/azure
```

有关所有可用配置值及其含义的详细信息，请参阅下一部分。 有关 INI 文件格式的完整详细信息，请参阅 [INI 上的 Python 文档](https://docs.python.org/3/library/configparser.html#supported-ini-file-structure)。

## <a name="cli-configuration-values-and-environment-variables"></a>CLI 配置值和环境变量

下表包含可在配置文件中放置的所有节和选项名称。 可将其相应环境变量设置为 `AZURE_{section}_{name}`（全大写）。 例如，可以在 `AZURE_BATCHAI_STORAGE_ACCOUNT` 变量中设置 `batchai` 节的 `storage_account` 默认值。

具有可用默认值的任何值不一定要在命令行参数中出现，即使该值是必需的。

| 部分 | 名称      | Type | 说明|
|---------|-----------|------|------------|
| __core__ | output | 字符串 | 默认输出格式。 可以是 `json`、`jsonc`、`tsv` 或 `table`。 |
| | disable\_confirm\_prompt | 布尔值 | 启用/禁用确认提示。 |
| | collect\_telemetry | 布尔值 | 允许 Microsoft 收集有关 CLI 使用情况的匿名数据。 有关隐私信息，请参阅 [Azure CLI 2.0 使用条款](http://aka.ms/AzureCliLegal)。 |
| __logging__ | enable\_log\_file | 布尔值 | 启用/关闭日志记录。 |
| | log\_dir | 字符串 | 要将日志写入到的目录。 默认为 `${AZURE_CONFIG_DIR}/logs`。 |
| __storage__ | connection\_string | 字符串 | `az storage` 命令使用的默认连接字符串。 |
| | 帐户 | 字符串 | `az storage` 命令使用的默认帐户名。 |
| | key | 字符串 | `az storage` 命令使用的默认帐户密钥。 |
| | sas\_token | 字符串 | `az storage` 命令使用的默认 SAS 令牌。 |
| __batchai__ | storage\_account | 字符串 | `az batchai` 命令使用的默认存储帐户。 |
| | storage\_key | 字符串 | `az batchai` 命令使用的默认存储密钥。 |
| __batch__ | 帐户 | 字符串 | `az batch` 命令使用的默认 Azure Batch 帐户名。 |
| | access\_key | 字符串 | `az batch` 命令使用的默认访问密钥。 只能与 `aad` 授权配合使用。 |
| | endpoint | 字符串 | `az batch` 命令要连接到的默认终结点。 |
| | auth\_mode | 字符串 | `az batch` 命令使用的授权模式。 可以是 `shared_key` 或 `aad`。 |

> [!NOTE]
> 配置文件中可能包含其他值，但这些值是直接通过 CLI 命令（包括 `az configure`）管理的。 你只能自行更改上表中列出的值。
