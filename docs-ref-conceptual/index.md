---
title: Azure CLI 概述
description: Azure CLI 概述。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 047a953a0ab8ccaf145d56e4d774d2bf9852ed6f
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177719"
---
# <a name="azure-cli"></a><span data-ttu-id="ba469-103">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="ba469-103">Azure CLI</span></span>

<span data-ttu-id="ba469-104">Azure CLI 是用于管理 Azure 资源的 Microsoft 跨平台命令行体验。</span><span class="sxs-lookup"><span data-stu-id="ba469-104">The Azure CLI is Microsoft's cross-platform command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="ba469-105">可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 或 Windows 上，然后从命令行运行它。</span><span class="sxs-lookup"><span data-stu-id="ba469-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="ba469-106">Azure CLI 易于入门，非常适合用于生成可针对 Azure 资源管理器运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="ba469-106">The Azure CLI is simple to get started with, and best used for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="ba469-107">使用 Azure CLI 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：</span><span class="sxs-lookup"><span data-stu-id="ba469-107">Using the Azure CLI, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

## <a name="run-or-install"></a><span data-ttu-id="ba469-108">运行或安装</span><span class="sxs-lookup"><span data-stu-id="ba469-108">Run or Install</span></span>

<span data-ttu-id="ba469-109">可在本地安装 CLI，在浏览器中使用 Azure Cloud Shell 运行 CLI，或者在 Docker 容器中运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="ba469-109">You can install the CLI locally, run it in the browser with Azure Cloud Shell, or run in a Docker container.</span></span>

* <span data-ttu-id="ba469-110">若要在浏览器中使用 Azure Cloud Shell 运行 CLI，请参阅 [Azure Cloud Shell 中的 Bash 快速入门](/azure/cloud-shell/quickstart)或 [Azure Cloud Shell 中的 PowerShell 快速入门](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="ba469-110">To run in your browser with Azure Cloud Shell, see [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart) or [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="ba469-111">若要安装 CLI，请参阅[安装 Azure CLI](install-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="ba469-111">To install the CLI, see [Install the Azure CLI](install-azure-cli.md).</span></span>
* <span data-ttu-id="ba469-112">若要以 Docker 容器的形式运行 CLI，请参阅[在 Docker 容器中运行 Azure CLI](run-azure-cli-docker.md)</span><span class="sxs-lookup"><span data-stu-id="ba469-112">To run as a Docker container, see [Run Azure CLI in a Docker Container](run-azure-cli-docker.md)</span></span>

## <a name="build-your-skills-with-microsoft-learn"></a><span data-ttu-id="ba469-113">利用 Microsoft Learn 掌握技能</span><span class="sxs-lookup"><span data-stu-id="ba469-113">Build your skills with Microsoft Learn</span></span>

- [<span data-ttu-id="ba469-114">使用 Azure CLI 管理虚拟机</span><span class="sxs-lookup"><span data-stu-id="ba469-114">Manage virtual machines with the Azure CLI</span></span>](/learn/modules/manage-virtual-machines-with-azure-cli/)
- [<span data-ttu-id="ba469-115">使用 CLI 控制 Azure 服务</span><span class="sxs-lookup"><span data-stu-id="ba469-115">Control Azure services with the CLI</span></span>](/learn/modules/control-azure-services-with-cli/)
- [<span data-ttu-id="ba469-116">更多交互式学习...</span><span class="sxs-lookup"><span data-stu-id="ba469-116">More interactive learning...</span></span>](/learn/browse/?products=azure-clis)

## <a name="get-started"></a><span data-ttu-id="ba469-117">入门</span><span class="sxs-lookup"><span data-stu-id="ba469-117">Get started</span></span>

<span data-ttu-id="ba469-118">请阅读[入门](get-started-with-azure-cli.md)一文来了解 CLI 基础知识。</span><span class="sxs-lookup"><span data-stu-id="ba469-118">Read the [Get Started](get-started-with-azure-cli.md) article to learn the CLI basics.</span></span> <span data-ttu-id="ba469-119">以下示例演示一些常见用例：</span><span class="sxs-lookup"><span data-stu-id="ba469-119">The following samples demonstrate some common uses cases:</span></span>

- [<span data-ttu-id="ba469-120">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="ba469-120">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="ba469-121">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="ba469-121">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="ba469-122">Web 应用</span><span class="sxs-lookup"><span data-stu-id="ba469-122">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="ba469-123">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="ba469-123">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="ba469-124">我们还提供了一篇详细的[参考](/cli/azure/reference-index)文章，其中介绍了如何使用每个 Azure CLI 命令。</span><span class="sxs-lookup"><span data-stu-id="ba469-124">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI command.</span></span>

> [!NOTE]
> <span data-ttu-id="ba469-125">如果正在使用旧版 CLI（Azure 经典 CLI），可以继续使用它。</span><span class="sxs-lookup"><span data-stu-id="ba469-125">If you use the previous version of the CLI (Azure classic CLI), you can continue to use it.</span></span>
> <span data-ttu-id="ba469-126">但是，建议进行更新以使用最新版本的 Azure CLI 来获得最佳体验。</span><span class="sxs-lookup"><span data-stu-id="ba469-126">However, we recommend updating to use the latest version of the Azure CLI for the best experience.</span></span>
> <span data-ttu-id="ba469-127">如果同时使用这两个版本的 CLI，请记住，`azure` 是经典 CLI，`az` 是最新 CLI。</span><span class="sxs-lookup"><span data-stu-id="ba469-127">If you use both CLIs, remember that `azure` is the classic CLI and that `az` is the most recent CLI.</span></span>
