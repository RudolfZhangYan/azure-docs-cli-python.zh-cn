---
title: Azure CLI 产品之间的差异
description: 了解如何对 Azure CLI 产品执行命名、版本控制和升级操作。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 07/12/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 4370616459ad4e466128ff26123c10f55bfdd7d8
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178145"
---
# <a name="differences-between-azure-cli-products"></a><span data-ttu-id="811de-103">Azure CLI 产品之间的差异</span><span class="sxs-lookup"><span data-stu-id="811de-103">Differences between Azure CLI products</span></span>

<span data-ttu-id="811de-104">在 2018 年 6 月末，显式版本号已从 Azure CLI 产品名称中去除。</span><span class="sxs-lookup"><span data-stu-id="811de-104">As of the end of June 2018, explicit version numbers have been removed from Azure CLI product names.</span></span> <span data-ttu-id="811de-105">这种更改有助于消除用户有时候在阅读文档时遇到的困惑，具体说来就是，用户在被告知使用“Azure CLI”时，并不清楚这是指哪个版本的产品。</span><span class="sxs-lookup"><span data-stu-id="811de-105">This change helps eliminate confusion that sometimes showed up in documentation where users were told to use "the Azure CLI" but it was unclear what version of the product was being referenced.</span></span> <span data-ttu-id="811de-106">如果熟悉旧的产品名称，则应该容易理解下面列出的具体更改：</span><span class="sxs-lookup"><span data-stu-id="811de-106">If you're familiar with the old product names, here is how they have changed:</span></span>

* <span data-ttu-id="811de-107">Azure CLI 2.0 及更高版本现在直接称为“Azure CLI”。</span><span class="sxs-lookup"><span data-stu-id="811de-107">Azure CLI versions 2.0 and later are now referred to only as "Azure CLI."</span></span>
* <span data-ttu-id="811de-108">更早的 Azure CLI 版本（1.x 及更低版本）现在称为“Azure 经典 CLI”。</span><span class="sxs-lookup"><span data-stu-id="811de-108">Earlier Azure CLI versions (1.x and lower) are now referred to as "Azure classic CLI."</span></span>

<span data-ttu-id="811de-109">将名称更改为“Azure 经典 CLI”清楚地表明，此工具仅适用于经典部署模型。</span><span class="sxs-lookup"><span data-stu-id="811de-109">The name change to Azure classic CLI makes it clear that this tool is meant to be used only with the classic deployment model.</span></span> <span data-ttu-id="811de-110">经典 CLI 也不再进行更新或维护。</span><span class="sxs-lookup"><span data-stu-id="811de-110">The classic CLI is also no longer updated or maintained.</span></span> <span data-ttu-id="811de-111">由于这个原因以及更多其他原因，建议放弃经典部署模型而改用 Azure 资源管理器模型，并迁移到最近提供的 Azure CLI 版本。</span><span class="sxs-lookup"><span data-stu-id="811de-111">For this reason, and many more, it's recommended that you move any classic deployments to use the Azure Resource Manager model and migrate to the latest available version of the Azure CLI.</span></span>

<span data-ttu-id="811de-112">如果仍使用经典 CLI，可通过以下文章了解迁移过程：</span><span class="sxs-lookup"><span data-stu-id="811de-112">If you are still using the classic CLI, you can learn about the process of migrating in the following articles:</span></span>

* [<span data-ttu-id="811de-113">从经典部署迁移到 Azure 资源管理器部署</span><span class="sxs-lookup"><span data-stu-id="811de-113">Migrate from Classic to Azure Resource Manager</span></span>](/azure/virtual-machines/linux/migration-classic-resource-manager-overview)
* [<span data-ttu-id="811de-114">安装 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="811de-114">Install the Azure CLI</span></span>](install-azure-cli.md)
* <span data-ttu-id="811de-115">[Migrating from Azure classic CLI to Azure CLI](https://github.com/Azure/azure-cli/blob/dev/doc/classic_cli_migration.md)（从 Azure 经典 CLI 迁移到 Azure CLI）</span><span class="sxs-lookup"><span data-stu-id="811de-115">[Migrating from Azure classic CLI to Azure CLI](https://github.com/Azure/azure-cli/blob/dev/doc/classic_cli_migration.md)</span></span>
