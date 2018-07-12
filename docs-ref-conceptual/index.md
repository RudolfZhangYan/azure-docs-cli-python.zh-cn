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
# <a name="azure-cli-20"></a><span data-ttu-id="4546e-103">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="4546e-103">Azure CLI 2.0</span></span>

<span data-ttu-id="4546e-104">Azure CLI 2.0 是用于管理 Azure 资源的 Microsoft 跨平台命令行体验。</span><span class="sxs-lookup"><span data-stu-id="4546e-104">The Azure CLI 2.0 is Microsoft's cross-platform command line experience for managing Azure resources.</span></span>
<span data-ttu-id="4546e-105">可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 或 Windows 上，然后从命令行运行它。</span><span class="sxs-lookup"><span data-stu-id="4546e-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="4546e-106">Azure CLI 2.0 经过优化，可用于从命令行管理 Azure 资源，以及生成可以针对 Azure 资源管理器运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="4546e-106">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="4546e-107">使用 Azure CLI 2.0 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：</span><span class="sxs-lookup"><span data-stu-id="4546e-107">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="4546e-108">使用 [Cloud Shell](/azure/cloud-shell/overview) 在浏览器中运行 CLI，或者在 macOS、Linux 或 Windows 上[安装](install-azure-cli.md)它。</span><span class="sxs-lookup"><span data-stu-id="4546e-108">Use the [Cloud Shell](/azure/cloud-shell/overview) to run the CLI in your browser, or [install](install-azure-cli.md) it on macOS, Linux, or Windows.</span></span>
<span data-ttu-id="4546e-109">请阅读[入门](get-started-with-azure-cli.md)一文，开始使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="4546e-109">Read the [Get Started](get-started-with-azure-cli.md) article to begin using the CLI.</span></span>
<span data-ttu-id="4546e-110">有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="4546e-110">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="4546e-111">下面的示例可帮助你开始在 Azure CLI 2.0 中执行常见任务：</span><span class="sxs-lookup"><span data-stu-id="4546e-111">The following samples help you get started with common tasks in Azure CLI 2.0:</span></span>

- [<span data-ttu-id="4546e-112">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="4546e-112">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="4546e-113">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="4546e-113">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="4546e-114">Web 应用</span><span class="sxs-lookup"><span data-stu-id="4546e-114">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="4546e-115">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="4546e-115">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="4546e-116">我们还提供了一篇详细的[参考](/cli/azure/reference-index)文章，其中介绍了如何使用每个 Azure CLI 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="4546e-116">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="4546e-117">立即[开始使用](get-started-with-azure-cli.md) Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4546e-117">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>

> [!NOTE]
> <span data-ttu-id="4546e-118">如果正在使用旧版 CLI (Azure CLI 1.0)，可以继续使用它。</span><span class="sxs-lookup"><span data-stu-id="4546e-118">If you use the previous version of the CLI (Azure CLI 1.0), you can continue to use it.</span></span>
> <span data-ttu-id="4546e-119">但是，我们建议进行更新以使用最新版本的 Azure CLI 2.0 来获得最佳体验。</span><span class="sxs-lookup"><span data-stu-id="4546e-119">However, we recommend updating to use the latest version of Azure CLI 2.0 for the best experience.</span></span>
> <span data-ttu-id="4546e-120">如果同时使用这两个版本的 CLI，请记住，`azure` 是旧 CLI (Azure CLI)，`az` 是新 CLI (Azure CLI 2.0)。</span><span class="sxs-lookup"><span data-stu-id="4546e-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>
