---
title: Azure CLI 2.0 概述
description: Azure CLI 2.0 概述。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 55c5ea3ad69df60d211cc076e3570e9f07040af7
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388371"
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 是用于管理 Azure 资源的 Microsoft 跨平台命令行体验。
可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 或 Windows 上，然后从命令行运行它。

Azure CLI 2.0 易于入门，非常适合用于生成可针对 Azure 资源管理器运行的自动化脚本。 使用 Azure CLI 2.0 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

## <a name="run-or-install"></a>运行或安装

可在本地安装 CLI，在浏览器中使用 Azure Cloud Shell 运行 CLI，或者在 Docker 容器中运行 CLI。

* 若要在浏览器中使用 Azure Cloud Shell 运行 CLI，请参阅 [Azure Cloud Shell 中的 Bash 快速入门](/azure/cloud-shell/quickstart)或 [Azure Cloud Shell 中的 PowerShell 快速入门](/azure/cloud-shell/quickstart-powershell)。
* 若要安装 CLI，请参阅[安装 Azure CLI 2.0](install-azure-cli.md)。
* 若要以 Docker 容器的形式运行 CLI，请参阅[在 Docker 容器中运行 Azure CLI 2.0](run-azure-cli-docker.md)

## <a name="get-started"></a>入门

请阅读[入门](get-started-with-azure-cli.md)一文来了解 CLI 基础知识。 以下示例演示一些常见用例：

- [Linux 虚拟机](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows 虚拟机](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web 应用](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL 数据库](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

我们还提供了一篇详细的[参考](/cli/azure/reference-index)文章，其中介绍了如何使用每个 Azure CLI 2.0 命令。

> [!NOTE]
> 如果正在使用旧版 CLI (Azure CLI 1.0)，可以继续使用它。
> 但是，我们建议进行更新以使用最新版本的 Azure CLI 2.0 来获得最佳体验。
> 如果同时使用这两个版本的 CLI，请记住，`azure` 是旧 CLI (Azure CLI)，`az` 是新 CLI (Azure CLI 2.0)。
