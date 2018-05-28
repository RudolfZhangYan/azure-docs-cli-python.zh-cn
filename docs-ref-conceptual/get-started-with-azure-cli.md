---
title: Azure CLI 2.0 入门
description: 学习命令基础知识开始使用 Azure CLI 2.0。
keywords: Azure CLI, CLI 帮助, Azure 帮助, 查询, 自动化,
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 0c7746e70125dcc1678ed19f93322efea8a2b01b
ms.sourcegitcommit: 8b4629a42ceecf30c1efbc6fdddf512f4dddfab0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/18/2018
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="a0c1c-104">Azure CLI 2.0 入门</span><span class="sxs-lookup"><span data-stu-id="a0c1c-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="a0c1c-105">欢迎使用 Azure CLI 2.0！</span><span class="sxs-lookup"><span data-stu-id="a0c1c-105">Welcome to the Azure CLI 2.0!</span></span> <span data-ttu-id="a0c1c-106">CLI 是旨在让你快速、高效地使用 Azure 服务且主要侧重于自动化的工具。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-106">The CLI is a tool designed to get you working quickly and efficiently with Azure services, with an emphasis on automation.</span></span> <span data-ttu-id="a0c1c-107">本文介绍 CLI 功能，并提供可帮助你高效工作的外部资源的链接。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-107">This article introduces features of the CLI and links out to resources that help you be productive.</span></span>

## <a name="install-and-log-in"></a><span data-ttu-id="a0c1c-108">安装和登录</span><span class="sxs-lookup"><span data-stu-id="a0c1c-108">Install and log in</span></span>

<span data-ttu-id="a0c1c-109">[安装 CLI](install-azure-cli.md)（如果尚未安装），或试用 [Azure Cloud Shell](/azure/cloud-shell/overview)。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-109">If you haven't already, [install the CLI](install-azure-cli.md) or try out the [Azure Cloud Shell](/azure/cloud-shell/overview).</span></span>

<span data-ttu-id="a0c1c-110">对本地安装使用任何 CLI 命令之前，需要使用 [az login](/cli/azure/reference-index#az-login) 登录。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-110">Before using any CLI commands with a local install, you need to log in with [az login](/cli/azure/reference-index#az-login).</span></span>

```azurecli
az login
```

<span data-ttu-id="a0c1c-111">此命令会提示你通过网站使用身份验证代码登录。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-111">This command prompts you to log in with an authentication code via a website.</span></span> <span data-ttu-id="a0c1c-112">非交互方式登录有很方法，在[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)中详细介绍。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-112">There are ways to log in non-interactively, which are covered in detail in [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="common-commands"></a><span data-ttu-id="a0c1c-113">常用命令</span><span class="sxs-lookup"><span data-stu-id="a0c1c-113">Common commands</span></span>

<span data-ttu-id="a0c1c-114">此表列出了 CLI 中使用的常用命令，并链接到外部参考中的其文档页。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-114">This table lists a few of the common commands used in the CLI links out to their documentation pages in the reference.</span></span>
<span data-ttu-id="a0c1c-115">这些组的所有子命令及其文档可以在联机参考中查找，或使用 `--help` 参数查找。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-115">All subcommands of these groups and their documentation can be looked up in online reference or with the `--help` argument.</span></span>

| <span data-ttu-id="a0c1c-116">资源类型</span><span class="sxs-lookup"><span data-stu-id="a0c1c-116">Resource type</span></span> | <span data-ttu-id="a0c1c-117">Azure CLI 命令组</span><span class="sxs-lookup"><span data-stu-id="a0c1c-117">Azure CLI command group</span></span> |
|---------------|-------------------------|
| [<span data-ttu-id="a0c1c-118">资源组</span><span class="sxs-lookup"><span data-stu-id="a0c1c-118">Resource group</span></span>](/azure/azure-resource-manager/resource-group-overview) | [<span data-ttu-id="a0c1c-119">az group</span><span class="sxs-lookup"><span data-stu-id="a0c1c-119">az group</span></span>](/cli/azure/group) |
| [<span data-ttu-id="a0c1c-120">虚拟机</span><span class="sxs-lookup"><span data-stu-id="a0c1c-120">Virtual machines</span></span>](/azure/virtual-machines) | [<span data-ttu-id="a0c1c-121">az vm</span><span class="sxs-lookup"><span data-stu-id="a0c1c-121">az vm</span></span>](/cli/azure/vm) |
| [<span data-ttu-id="a0c1c-122">存储帐户</span><span class="sxs-lookup"><span data-stu-id="a0c1c-122">Storage accounts</span></span>](/azure/storage/common/storage-introduction) | [<span data-ttu-id="a0c1c-123">az storage account</span><span class="sxs-lookup"><span data-stu-id="a0c1c-123">az storage account</span></span>](/cli/azure/storage/account) |
| [<span data-ttu-id="a0c1c-124">Key Vault</span><span class="sxs-lookup"><span data-stu-id="a0c1c-124">Key Vault</span></span>](/azure/key-vault/key-vault-whatis) | [<span data-ttu-id="a0c1c-125">az keyvault</span><span class="sxs-lookup"><span data-stu-id="a0c1c-125">az keyvault</span></span>](/cli/azure/keyvault) |
| [<span data-ttu-id="a0c1c-126">Web 应用程序</span><span class="sxs-lookup"><span data-stu-id="a0c1c-126">Web applications</span></span>](/azure/ap-service) | [<span data-ttu-id="a0c1c-127">az webapp</span><span class="sxs-lookup"><span data-stu-id="a0c1c-127">az webapp</span></span>](/cli/azure/webapp) |
| [<span data-ttu-id="a0c1c-128">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="a0c1c-128">SQL databases</span></span>](/azure/sql-database) | [<span data-ttu-id="a0c1c-129">az sql server</span><span class="sxs-lookup"><span data-stu-id="a0c1c-129">az sql server</span></span>](/cli/azure/sql/server) |
| [<span data-ttu-id="a0c1c-130">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="a0c1c-130">CosmosDB</span></span>](/azure/cosmos-db) | [<span data-ttu-id="a0c1c-131">az cosmosdb</span><span class="sxs-lookup"><span data-stu-id="a0c1c-131">az cosmosdb</span></span>](/cli/azure/cosmosdb) |

## <a name="finding-commands"></a><span data-ttu-id="a0c1c-132">查找命令</span><span class="sxs-lookup"><span data-stu-id="a0c1c-132">Finding commands</span></span>

<span data-ttu-id="a0c1c-133">CLI 中的命令以_组_的_子命令_形式提供。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-133">Commands in the CLI are provided as _subcommands_ of _groups_.</span></span>
<span data-ttu-id="a0c1c-134">每个组表示由 Azure 提供的一个服务，而子组将这些服务的命令划分为逻辑分组。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-134">Each group represents a service provided by Azure, and the subgroups divide commands for these services into logical groupings.</span></span>

<span data-ttu-id="a0c1c-135">若要搜索命令，请使用 [az find](/cli/azure/reference-index#az-find)。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-135">To search for commands, use [az find](/cli/azure/reference-index#az-find).</span></span> <span data-ttu-id="a0c1c-136">例如，若要搜索包含 `secret` 的命令名称，请使用以下命令：</span><span class="sxs-lookup"><span data-stu-id="a0c1c-136">For example, to search for command names containing `secret`, use the following command:</span></span>

```azurecli-interactive
az find -q secret
```

<span data-ttu-id="a0c1c-137">如果你知道要使用哪组命令，`--help` 参数可能是更好的选择。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-137">If you know which group of commands you want to work with, the `--help` argument may be a better choice.</span></span> <span data-ttu-id="a0c1c-138">此参数不仅显示某个命令的详细信息，而且在用于命令组时，会显示所有可用的子命令。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-138">This displays not just detailed information for a command, but when used with a command group, displays all of the available subcommands.</span></span> <span data-ttu-id="a0c1c-139">例如，用于网络安全组 (NSG) 时，可以查找可用的 NSG 子组和命令。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-139">For example, when working with Network Security Groups (NSGs) you can find the available NSG subgroups and commands.</span></span>

```azurecli-interactive
az network nsg --help
```

<span data-ttu-id="a0c1c-140">CLI 为 bash shell 下的命令提供完整 tab 键补全。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-140">The CLI has full tab completion for commands under the bash shell.</span></span>

## <a name="globally-available-arguments"></a><span data-ttu-id="a0c1c-141">全局可用参数</span><span class="sxs-lookup"><span data-stu-id="a0c1c-141">Globally available arguments</span></span>

<span data-ttu-id="a0c1c-142">有一些参数可用于每条命令。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-142">There are some arguments that are available for every command.</span></span>

* <span data-ttu-id="a0c1c-143">`--help` 会输出有关命令及其参数的 CLI 参考信息并列出可用的子组和命令。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-143">`--help` prints CLI reference information about commands and their arguments and lists available subgroups and commands.</span></span>
* <span data-ttu-id="a0c1c-144">`--output` 可更改输出格式。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-144">`--output` changes the output format.</span></span> <span data-ttu-id="a0c1c-145">可用的输出格式包括 `json`、`jsonc`（彩色 JSON）、`tsv`（制表符分隔值）和 `table`（用户可读 ASCII 表）。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-145">The available output formats are `json`, `jsonc` (colorized JSON), `tsv` (Tab-Separated Values), and `table` (human-readable ASCII tables).</span></span> <span data-ttu-id="a0c1c-146">默认情况下，CLI 输出 `json`。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-146">By default the CLI outputs `json`.</span></span> <span data-ttu-id="a0c1c-147">若要了解有关可用输出格式的详细信息，请参阅 [Azure CLI 2.0 的输出格式](format-output-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-147">To learn more about the available output formats, see [Output formats for Azure CLI 2.0](format-output-azure-cli.md).</span></span>
* <span data-ttu-id="a0c1c-148">`--query` 使用 [JMESPath 查询语言](http://jmespath.org/)筛选从 Azure 服务返回的输出。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-148">`--query` uses the [JMESPath query language](http://jmespath.org/) to filter the output returned from Azure services.</span></span> <span data-ttu-id="a0c1c-149">若要了解有关查询的详细信息，请参阅[使用 Azure CLI 2.0 查询命令结果](query-azure-cli.md)和 [JMESPath 教程](http://jmespath.org/tutorial.html)。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-149">To learn To learn more about queries, see [Query command results with Azure CLI 2.0](query-azure-cli.md) and the [JMESPath tutorial](http://jmespath.org/tutorial.html).</span></span>
* <span data-ttu-id="a0c1c-150">`--verbose` 输出有关操作期间在 Azure 中创建的资源的信息和其他有用信息。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-150">`--verbose` prints information about resources created in Azure during an operation, and other useful information.</span></span>
* <span data-ttu-id="a0c1c-151">`--debug` 输出有关 CLI 操作的更详细信息，用于调试目的。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-151">`--debug` prints even more information about CLI operations, used for debugging purposes.</span></span> <span data-ttu-id="a0c1c-152">如果遇到 bug，在提交 bug 报告时，请提供启用 `--debug` 标志生成的输出。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-152">If you encounter a bug, provide output generated with the `--debug` flag on when submitting a bug report.</span></span>


## <a name="interactive-mode"></a><span data-ttu-id="a0c1c-153">交互模式</span><span class="sxs-lookup"><span data-stu-id="a0c1c-153">Interactive mode</span></span>

<span data-ttu-id="a0c1c-154">CLI 提供一种交互模式，可自动显示帮助信息，并可更轻松地选择子命令。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-154">The CLI offers an interactive mode that automatically displays help information and makes it easier to select subcommands.</span></span> <span data-ttu-id="a0c1c-155">使用 [az interactive](/cli/azure/reference-index#az-interactive) 命令即可进入交互模式。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-155">You enter interactive mode with the [az interactive](/cli/azure/reference-index#az-interactive) command.</span></span>

```azurecli-interactive
az interactive
```

<span data-ttu-id="a0c1c-156">有关交互模式的详细信息，请参阅 [Azure CLI 2.0 交互模式](interactive-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-156">For more information on interactive mode, see [Azure CLI 2.0 Interactive Mode](interactive-azure-cli.md).</span></span>

<span data-ttu-id="a0c1c-157">此外，还有提供交互体验的 [Visual Studio Code 插件](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli)，包括自动完成和鼠标悬停显示的文档。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-157">There is also a [Visual Studio Code plugin](https://marketplace.visualstudio.com/items?itemName=ms-vscode.azurecli) that offers an interactive experience, including autocomplete and mouse-over documentation.</span></span>

## <a name="learn-cli-basics-with-quickstarts-and-tutorials"></a><span data-ttu-id="a0c1c-158">使用快速入门和教程了解 CLI 基础知识</span><span class="sxs-lookup"><span data-stu-id="a0c1c-158">Learn CLI basics with quickstarts and tutorials</span></span>

<span data-ttu-id="a0c1c-159">若要开始使用 Azure CLI 2.0，请试用深入教程以设置虚拟机并利用 CLI 的功能查询 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-159">To get you started with the Azure CLI 2.0, try an in-depth tutorial for setting up virtual machines and using the power of the CLI to query Azure resources.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="a0c1c-160">使用 Azure CLI 2.0 教程创建虚拟机</span><span class="sxs-lookup"><span data-stu-id="a0c1c-160">Create virtual machines with the Azure CLI 2.0 tutorial</span></span>](azure-cli-vm-tutorial.yml)

<span data-ttu-id="a0c1c-161">如果你更关注其他服务，有多种使用 CLI 的 Azure 服务的快速入门。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-161">If you would rather focus on other services, there are a variety of quickstarts for Azure services that use the CLI.</span></span>

* [<span data-ttu-id="a0c1c-162">使用 Azure CLI 创建存储帐户</span><span class="sxs-lookup"><span data-stu-id="a0c1c-162">Create a storage account using the Azure CLI</span></span>](/azure/storage/common/storage-quickstart-create-storage-account-cli)
* [<span data-ttu-id="a0c1c-163">使用 CLI 向/从 Azure Blob 存储转移对象</span><span class="sxs-lookup"><span data-stu-id="a0c1c-163">Transfer objects to/from Azure Blob storage using the CLI</span></span>](/azure/storage/blobs/storage-quickstart-blobs-cli)
* [<span data-ttu-id="a0c1c-164">使用 Azure CLI 创建单一 Azure SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="a0c1c-164">Create a single Azure SQL database using the Azure CLI</span></span>](/azure/sql-database/sql-database-get-started-cli)
* [<span data-ttu-id="a0c1c-165">使用 Azure CLI 创建 Azure Database for MySQL 服务器</span><span class="sxs-lookup"><span data-stu-id="a0c1c-165">Create an Azure Database for MySQL server using the Azure CLI</span></span>](/azure/mysql/quickstart-create-mysql-server-database-using-azure-cli)
* [<span data-ttu-id="a0c1c-166">使用 Azure CLI 创建用于 PostgreSQL 的 Azure 数据库</span><span class="sxs-lookup"><span data-stu-id="a0c1c-166">Create an Azure Database for PostgreSQL using the Azure CLI</span></span>](/azure/postgresql/quickstart-create-server-database-azure-cli)
* [<span data-ttu-id="a0c1c-167">在 Azure 中创建 Python Web 应用</span><span class="sxs-lookup"><span data-stu-id="a0c1c-167">Create a Python web app in Azure</span></span>](/azure/app-service/app-service-web-get-started-python)
* [<span data-ttu-id="a0c1c-168">在用于容器的 Azure Web 应用中运行自定义 Docker 中心映像</span><span class="sxs-lookup"><span data-stu-id="a0c1c-168">Run a custom Docker Hub image in Azure Web Apps for Containers</span></span>](/azure/app-service/containers/quickstart-custom-docker-image)

## <a name="give-feedback"></a><span data-ttu-id="a0c1c-169">提供反馈</span><span class="sxs-lookup"><span data-stu-id="a0c1c-169">Give feedback</span></span>

<span data-ttu-id="a0c1c-170">我们欢迎你提供有关 CLI 的反馈以帮助我们改进和解决 bug。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-170">We welcome your feedback for the CLI to help us make improvements and resolve bugs.</span></span> <span data-ttu-id="a0c1c-171">可以[在 Github 上提出问题](https://github.com/azure/azure-cli/issues)，或利用 CLI 的内置功能来通过 [az feedback](/cli/azure/reference-index#az-feedback) 命令留下常规反馈。</span><span class="sxs-lookup"><span data-stu-id="a0c1c-171">You can [file an issue on Github](https://github.com/azure/azure-cli/issues) or use the built-in features of the CLI to leave general feedback with the [az feedback](/cli/azure/reference-index#az-feedback) command.</span></span>

```azurecli-interactive
az feedback
```
