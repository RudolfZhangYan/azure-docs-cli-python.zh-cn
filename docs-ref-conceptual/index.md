---
title: Azure CLI 2.0
description: Azure CLI 2.0 概述。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 05/16/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: ffa435f8c6ee5aa82d2efe2e09d7bcb1f1dc434b
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967684"
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 是用于管理 Azure 资源的 Microsoft 跨平台命令行体验。
可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 或 Windows 上，然后从命令行运行它。

Azure CLI 2.0 经过优化，可用于从命令行管理 Azure 资源，以及生成可以针对 Azure 资源管理器运行的自动化脚本。 使用 Azure CLI 2.0 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

使用 [Cloud Shell](/azure/cloud-shell/overview) 在浏览器中运行 CLI，或者在 macOS、Linux 或 Windows 上[安装](install-azure-cli.md)它。
请阅读[入门](get-started-with-azure-cli.md)一文，开始使用 CLI。
有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

下面的示例可帮助你开始在 Azure CLI 2.0 中执行常见任务：

- [Linux 虚拟机](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows 虚拟机](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web 应用](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL 数据库](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

我们还提供了一篇详细的[参考](/cli/azure/reference-index)文章，其中介绍了如何使用每个 Azure CLI 2.0 命令。

立即[开始使用](get-started-with-azure-cli.md) Azure CLI 2.0。

> [!NOTE]
> 如果正在使用旧版 CLI (Azure CLI 1.0)，可以继续使用它。
> 但是，我们建议进行更新以使用最新版本的 Azure CLI 2.0 来获得最佳体验。
> 如果同时使用这两个版本的 CLI，请记住，`azure` 是旧 CLI (Azure CLI)，`az` 是新 CLI (Azure CLI 2.0)。
