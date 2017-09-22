---
title: Azure CLI 2.0
description: "Azure CLI 2.0 概述。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 80ae9f6c-adb7-483c-bfb4-fbb958e075ba
ms.openlocfilehash: 36a08835b9c4f6e71c5ddadbce8ba946c52a1e9b
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2017
---
# <a name="azure-cli-20"></a>Azure CLI 2.0

Azure CLI 2.0 是 Azure 的新命令行体验，用于管理 Azure 资源。
可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 和 Windows 上，然后从命令行运行它。

Azure CLI 2.0 经过优化，可用于从命令行管理 Azure 资源，以及生成可以针对 Azure Resource Manager 运行的自动化脚本。 使用 Azure CLI 2.0 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

使用 [Cloud Shell](/azure/cloud-shell/overview) 在浏览器中运行 CLI，或者在 macOS、Linux 或 Windows 上[安装](install-azure-cli.md)它。
请阅读[入门](get-started-with-azure-cli.md)一文，开始使用 CLI。
有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

可借助以下示例了解如何使用 Azure CLI 2.0 执行常见方案：
- [Linux 虚拟机](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Windows 虚拟机](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [Web 应用](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [SQL 数据库](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

我们还提供了一篇详细的[参考](/cli/azure/)文章，其中介绍了如何使用每个 Azure CLI 2.0 命令。

立即[开始使用](get-started-with-azure-cli.md) Azure CLI 2.0。


> [!NOTE]
> 如果正在使用旧版 CLI (Azure CLI)，可以继续使用它。
> 如果同时使用这两个版本的 CLI，请记住，`azure` 是旧 CLI (Azure CLI)，`az` 是新 CLI (Azure CLI 2.0)。 