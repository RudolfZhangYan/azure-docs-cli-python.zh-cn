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
# <a name="azure-cli-20"></a><span data-ttu-id="fe389-103">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="fe389-103">Azure CLI 2.0</span></span>

<span data-ttu-id="fe389-104">Azure CLI 2.0 是用于管理 Azure 资源的 Microsoft 跨平台命令行体验。</span><span class="sxs-lookup"><span data-stu-id="fe389-104">The Azure CLI 2.0 is Microsoft's cross-platform command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="fe389-105">可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 或 Windows 上，然后从命令行运行它。</span><span class="sxs-lookup"><span data-stu-id="fe389-105">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or [install](install-azure-cli.md) it on macOS, Linux, or Windows and run it from the command line.</span></span>

<span data-ttu-id="fe389-106">Azure CLI 2.0 易于入门，非常适合用于生成可针对 Azure 资源管理器运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="fe389-106">Azure CLI 2.0 is simple to get started with, and best used for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="fe389-107">使用 Azure CLI 2.0 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：</span><span class="sxs-lookup"><span data-stu-id="fe389-107">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

## <a name="run-or-install"></a><span data-ttu-id="fe389-108">运行或安装</span><span class="sxs-lookup"><span data-stu-id="fe389-108">Run or Install</span></span>

<span data-ttu-id="fe389-109">可在本地安装 CLI，在浏览器中使用 Azure Cloud Shell 运行 CLI，或者在 Docker 容器中运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="fe389-109">You can install the CLI locally, run it in the browser with Azure Cloud Shell, or run in a Docker container.</span></span>

* <span data-ttu-id="fe389-110">若要在浏览器中使用 Azure Cloud Shell 运行 CLI，请参阅 [Azure Cloud Shell 中的 Bash 快速入门](/azure/cloud-shell/quickstart)或 [Azure Cloud Shell 中的 PowerShell 快速入门](/azure/cloud-shell/quickstart-powershell)。</span><span class="sxs-lookup"><span data-stu-id="fe389-110">To run in your browser with Azure Cloud Shell, see [Quickstart for Bash in Azure Cloud Shell](/azure/cloud-shell/quickstart) or [Quickstart for PowerShell in Azure Cloud Shell](/azure/cloud-shell/quickstart-powershell).</span></span>
* <span data-ttu-id="fe389-111">若要安装 CLI，请参阅[安装 Azure CLI 2.0](install-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="fe389-111">To install the CLI, see [Install the Azure CLI 2.0](install-azure-cli.md).</span></span>
* <span data-ttu-id="fe389-112">若要以 Docker 容器的形式运行 CLI，请参阅[在 Docker 容器中运行 Azure CLI 2.0](run-azure-cli-docker.md)</span><span class="sxs-lookup"><span data-stu-id="fe389-112">To run as a Docker container, see [Run Azure CLI 2.0 in a Docker Container](run-azure-cli-docker.md)</span></span>

## <a name="get-started"></a><span data-ttu-id="fe389-113">入门</span><span class="sxs-lookup"><span data-stu-id="fe389-113">Get started</span></span>

<span data-ttu-id="fe389-114">请阅读[入门](get-started-with-azure-cli.md)一文来了解 CLI 基础知识。</span><span class="sxs-lookup"><span data-stu-id="fe389-114">Read the [Get Started](get-started-with-azure-cli.md) article to learn the CLI basics.</span></span> <span data-ttu-id="fe389-115">以下示例演示一些常见用例：</span><span class="sxs-lookup"><span data-stu-id="fe389-115">The following samples demonstrate some common uses cases:</span></span>

- [<span data-ttu-id="fe389-116">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="fe389-116">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="fe389-117">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="fe389-117">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="fe389-118">Web 应用</span><span class="sxs-lookup"><span data-stu-id="fe389-118">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="fe389-119">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="fe389-119">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="fe389-120">我们还提供了一篇详细的[参考](/cli/azure/reference-index)文章，其中介绍了如何使用每个 Azure CLI 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="fe389-120">A detailed [reference](/cli/azure/reference-index) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

> [!NOTE]
> <span data-ttu-id="fe389-121">如果正在使用旧版 CLI (Azure CLI 1.0)，可以继续使用它。</span><span class="sxs-lookup"><span data-stu-id="fe389-121">If you use the previous version of the CLI (Azure CLI 1.0), you can continue to use it.</span></span>
> <span data-ttu-id="fe389-122">但是，我们建议进行更新以使用最新版本的 Azure CLI 2.0 来获得最佳体验。</span><span class="sxs-lookup"><span data-stu-id="fe389-122">However, we recommend updating to use the latest version of Azure CLI 2.0 for the best experience.</span></span>
> <span data-ttu-id="fe389-123">如果同时使用这两个版本的 CLI，请记住，`azure` 是旧 CLI (Azure CLI)，`az` 是新 CLI (Azure CLI 2.0)。</span><span class="sxs-lookup"><span data-stu-id="fe389-123">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span>
