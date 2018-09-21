---
title: 安装适用于 Windows 的 Azure CLI
description: 如何在 Windows 上安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 6e57837313faf0edd95d822132ae282ed416aae7
ms.sourcegitcommit: d93b0a2bcfb0d164ef90d6d4618f0552609a8ea6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2018
ms.locfileid: "46469957"
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="69b2b-103">在 Windows 上安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="69b2b-103">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="69b2b-104">在 Windows 上，Azure CLI 是通过 MSI 安装的，因此，可以通过 Windows 命令提示符 (CMD) 或 PowerShell 访问 CLI。</span><span class="sxs-lookup"><span data-stu-id="69b2b-104">For Windows the Azure CLI is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="69b2b-105">为适用于 Linux 的 Windows 子系统 (WSL) 安装时，可以安装适用于 Linux 分发版的包。</span><span class="sxs-lookup"><span data-stu-id="69b2b-105">When installing for Windows Subsystem for Linux (WSL), packages are available for your Linux distribution.</span></span> <span data-ttu-id="69b2b-106">请参阅[安装主页](install-azure-cli.md)，获取受支持包管理器的列表，或者了解如何在 WSL 下手动进行安装。</span><span class="sxs-lookup"><span data-stu-id="69b2b-106">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="69b2b-107">安装或更新</span><span class="sxs-lookup"><span data-stu-id="69b2b-107">Install or update</span></span>

<span data-ttu-id="69b2b-108">MSI 发行版用于在 Windows 上安装、更新和卸载 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="69b2b-108">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="69b2b-109">下载 MSI 安装程序</span><span class="sxs-lookup"><span data-stu-id="69b2b-109">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

<span data-ttu-id="69b2b-110">当安装程序询问是否可以对计算机进行更改时，请单击“是”框。</span><span class="sxs-lookup"><span data-stu-id="69b2b-110">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="69b2b-111">现在可以通过 Windows 命令提示符或 PowerShell 使用 `az` 命令运行 Azure CLI 了。</span><span class="sxs-lookup"><span data-stu-id="69b2b-111">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="69b2b-112">PowerShell 提供了 Windows 命令提示符所不能提供的一些 Tab 键补全功能。</span><span class="sxs-lookup"><span data-stu-id="69b2b-112">PowerShell offers some tab completion features not available from Windows Command Prompt.</span></span> <span data-ttu-id="69b2b-113">若要登录，请运行 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="69b2b-113">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="69b2b-114">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="69b2b-114">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="uninstall"></a><span data-ttu-id="69b2b-115">卸载</span><span class="sxs-lookup"><span data-stu-id="69b2b-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="69b2b-116">再次运行 MSI 并选择“卸载”选项即可进行卸载。</span><span class="sxs-lookup"><span data-stu-id="69b2b-116">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="69b2b-117">下载 MSI 安装程序</span><span class="sxs-lookup"><span data-stu-id="69b2b-117">Download the MSI installer</span></span>](https://aka.ms/installazurecliwindows)

## <a name="next-steps"></a><span data-ttu-id="69b2b-118">后续步骤</span><span class="sxs-lookup"><span data-stu-id="69b2b-118">Next Steps</span></span>

<span data-ttu-id="69b2b-119">现在你已经安装了 Azure CLI，下面简要介绍其功能和常用命令。</span><span class="sxs-lookup"><span data-stu-id="69b2b-119">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="69b2b-120">Azure CLI 入门</span><span class="sxs-lookup"><span data-stu-id="69b2b-120">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
