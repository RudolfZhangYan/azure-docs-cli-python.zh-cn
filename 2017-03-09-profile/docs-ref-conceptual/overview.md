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
ms.openlocfilehash: 2f4f9950dd663ae85f41bf4efe114b15770ace5d
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: zh-CN
---
# <a name="azure-cli-20"></a><span data-ttu-id="0a5eb-104">Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="0a5eb-104">Azure CLI 2.0</span></span>

<span data-ttu-id="0a5eb-105">Azure CLI 2.0 是 Azure 的新命令行体验，用于管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-105">The Azure CLI 2.0 is Azure's new command-line experience for managing Azure resources.</span></span>  <span data-ttu-id="0a5eb-106">它可以在 macOS、Linux 和 Windows 上使用。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-106">It can be used on macOS, Linux, and Windows.</span></span> 

<span data-ttu-id="0a5eb-107">Azure CLI 2.0 经过优化，可用于从命令行管理 Azure 资源，以及生成可以针对 Azure Resource Manager 运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span> <span data-ttu-id="0a5eb-108">使用 Azure CLI 2.0 时，只需键入以下命令，即可在 Azure 中轻松创建 VM：</span><span class="sxs-lookup"><span data-stu-id="0a5eb-108">Using the Azure CLI 2.0, you can create VMs within Azure as easily as typing the following command:</span></span>

```azurecli
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS
```

<span data-ttu-id="0a5eb-109">请参阅[有关安装的文章](install-azure-cli.md)，了解如何在系统上启动和运行 CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-109">Review the [Install article](install-azure-cli.md) to get Azure CLI 2.0 up and running on your system.</span></span> <span data-ttu-id="0a5eb-110">然后阅读[入门](get-started-with-azure-cli.md)一文开始 Azure PowerShell。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-110">Then read the [Get Started](get-started-with-azure-cli.md) article to begin using it.</span></span>
<span data-ttu-id="0a5eb-111">有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-111">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

<span data-ttu-id="0a5eb-112">以下示例可帮助你了解如何使用 Azure CLI 2.0 执行常见方案：</span><span class="sxs-lookup"><span data-stu-id="0a5eb-112">The following samples can help you learn how to perform common scenarios with Azure CLI 2.0:</span></span>
- [<span data-ttu-id="0a5eb-113">Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="0a5eb-113">Linux Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="0a5eb-114">Windows 虚拟机</span><span class="sxs-lookup"><span data-stu-id="0a5eb-114">Windows Virtual Machines</span></span>](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="0a5eb-115">Web 应用</span><span class="sxs-lookup"><span data-stu-id="0a5eb-115">Web Apps</span></span>](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)
- [<span data-ttu-id="0a5eb-116">SQL 数据库</span><span class="sxs-lookup"><span data-stu-id="0a5eb-116">SQL Database</span></span>](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)

<span data-ttu-id="0a5eb-117">我们还提供了一篇详细的[参考](/cli/azure/)文章，其中介绍了如何使用每个 Azure CLI 2.0 命令。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-117">A detailed [reference](/cli/azure/) is also available that documents how to use each individual Azure CLI 2.0 command.</span></span>

<span data-ttu-id="0a5eb-118">立即[开始使用](get-started-with-azure-cli.md) Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-118">[Get started](get-started-with-azure-cli.md) with Azure CLI 2.0 now.</span></span>


> [!NOTE]
> <span data-ttu-id="0a5eb-119">如果你正在使用旧版 CLI (Azure CLI)，可以继续使用它。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-119">If you use the previous version of the CLI (Azure CLI), you can continue to use it.</span></span>
> <span data-ttu-id="0a5eb-120">如果同时使用这两个版本的 CLI，请记住，`azure` 是旧 CLI (Azure CLI)，`az` 是新 CLI (Azure CLI 2.0)。</span><span class="sxs-lookup"><span data-stu-id="0a5eb-120">If you use both CLIs, remember that `azure` is the old CLI - Azure CLI, and that `az` is the new CLI - Azure CLI 2.0.</span></span> 