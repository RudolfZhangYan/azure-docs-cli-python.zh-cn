---
title: "Azure CLI 2.0 入门"
description: "学习命令基础知识开始使用 Azure CLI 2.0。"
keywords: "Azure CLI, CLI 帮助, Azure 帮助, 查询, 自动化,"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/05/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: c2758922d74080d3a3110b1e3a507ddf0f8d85d1
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2018
---
# <a name="get-started-with-azure-cli-20"></a>Azure CLI 2.0 入门

欢迎使用 Azure CLI 2.0！ CLI 是旨在让你快速、高效地使用 Azure 服务且主要侧重于自动化的工具。 本文介绍 CLI 功能，并提供可帮助你高效工作的外部资源的链接。

## <a name="install-and-log-in"></a>安装和登录

[安装 CLI](install-azure-cli.md)（如果尚未安装），或试用 [Azure Cloud Shell](/azure/cloud-shell/overview)。

对本地安装使用任何 CLI 命令之前，需要使用 [az login](/cli/azure/index#az_login) 登录。

```azurecli
az login
```

此命令会提示你通过网站使用身份验证代码登录。 非交互方式登录有很方法，在[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)中详细介绍。

## <a name="common-commands"></a>常用命令

此表列出了 CLI 中使用的常用命令，并链接到外部参考中的其文档页。
这些组的所有子命令及其文档可以在联机参考中查找，或使用 `--help` 参数查找。

| 资源类型 | Azure CLI 命令组 |
|---------------|-------------------------|
| [资源组](/azure/azure-resource-manager/resource-group-overview) | [az group](/cli/azure/group) |
| [虚拟机](/azure/virtual-machines) | [az vm](/cli/azure/vm) |
| [存储帐户](/azure/storage/common/storage-introduction) | [az storage account](/cli/azure/storage/account) |
| [Key Vault](/azure/key-vault/key-vault-whatis) | [az keyvault](/cli/azure/keyvault) |
| [Web 应用程序](/azure/ap-service) | [az webapp](/cli/azure/webapp) |
| [SQL 数据库](/azure/sql-database) | [az sql server](/cli/azure/sql/server) |
| [CosmosDB](/azure/cosmos-db) | [az cosmosdb](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a>查找命令

CLI 中的命令以_组_的_子命令_形式提供。
每个组表示由 Azure 提供的一个服务，而子组将这些服务的命令划分为逻辑分组。

若要搜索命令，请使用 [az find](/cli/azure/index#az_find)。 例如，若要搜索包含 `secret` 的命令名称，请使用以下命令：

```azurecli
az find -q secret
```

如果你知道要使用哪组命令，`--help` 参数可能是更好的选择。 此参数不仅显示某个命令的详细信息，而且在用于命令组时，会显示所有可用的子命令。 例如，用于网络安全组 (NSG) 时，可以查找可用的 NSG 子组和命令。

```azurecli
az network nsg --help
```

CLI 为 bash shell 下的命令提供完整 tab 键补全。

## <a name="globally-available-arguments"></a>全局可用参数

有一些参数可用于每条命令。

* `--help` 会输出有关命令及其参数的 CLI 参考信息并列出可用的子组和命令。
* `--output` 可更改输出格式。 可用的输出格式包括 `json`、`jsonc`（彩色 JSON）、`tsv`（制表符分隔值）和 `table`（用户可读 ASCII 表）。 默认情况下，CLI 输出 `json`。 若要了解有关可用输出格式的详细信息，请参阅 [Azure CLI 2.0 的输出格式](format-output-azure-cli.md)。
* `--query` 使用 [JMESPath 查询语言](http://jmespath.org/)筛选从 Azure 服务返回的输出。 若要了解有关查询的详细信息，请参阅[使用 Azure CLI 2.0 查询命令结果](query-azure-cli.md)和 [JMESPath 教程](http://jmespath.org/tutorial.html)。
* `--verbose` 输出有关操作期间在 Azure 中创建的资源的信息和其他有用信息。
* `--debug` 输出有关 CLI 操作的更详细信息，用于调试目的。 如果遇到 bug，在提交 bug 报告时，请提供启用 `--debug` 标志生成的输出。


## <a name="interactive-mode"></a>交互模式

CLI 提供一种交互模式，可自动显示帮助信息，并可更轻松地选择子命令。 使用 `az interactive` 命令即可进入交互模式。 有关交互模式以及它如何帮助你了解 CLI 的详细信息，请参阅 [Azure CLI 2.0 交互模式](interactive-azure-cli.md)。

此外，还有提供交互体验的 [Visual Studio Code 插件](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)，包括自动完成和鼠标悬停显示的文档。



## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a>使用快速入门和教程了解 CLI 基础知识

若要开始使用 Azure CLI 2.0，请试用深入教程以设置虚拟机并利用 CLI 的功能查询 Azure 资源。

> [!div class="nextstepaction"]
> [使用 Azure CLI 2.0 教程创建虚拟机](azure-cli-vm-tutorial.yml)

如果你更关注其他服务，有多种使用 CLI 的 Azure 服务的快速入门。

* [使用 Azure CLI 创建存储帐户](/azure/storage/common/storage-quickstart-create-storage-account-cl)
* [使用 CLI 向/从 Azure Blob 存储转移对象](/storage/blobs/storage-quickstart-blobs-cli)
* [使用 Azure CLI 创建单一 Azure SQL 数据库](/azure/sql-database/sql-database-get-started-cli)
* [使用 Azure CLI 创建 Azure Database for MySQL 服务器](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [使用 Azure CLI 创建用于 PostgreSQL 的 Azure 数据库](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [在 Azure 中创建 Python Web 应用](/azure/app-service/app-service-web-get-started-python)
* [在用于容器的 Azure Web 应用中运行自定义 Docker 中心映像](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a>提供反馈

我们欢迎你提供有关 CLI 的反馈以帮助我们改进和解决 bug。 可以[在 Github 上提出问题](https://github.com/azure/azure-cli/issues)或利用 CLI 的内置功能使用 `az feedback` 命令留下常规反馈。

```azurecli
az feedback
```
