---
title: "安装适用于 Windows 的 Azure CLI"
description: "如何在 Windows 上安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure 安装 windows, azure cli windows, azure windows"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: f2745c05c12a4ed5fb5a25e86a5dec1664651066
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="979c0-104">在 Windows 上安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="979c0-104">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="979c0-105">在 Windows 上，Azure CLI 二进制文件是通过 MSI 安装的，因此，可以通过 Windows 命令提示符 (CMD) 或 PowerShell 访问 CLI。</span><span class="sxs-lookup"><span data-stu-id="979c0-105">On Windows the Azure CLI binary is installed via an MSI, which gives you access to the CLI through the Windows Command Prompt (CMD) or PowerShell.</span></span>
<span data-ttu-id="979c0-106">如果运行的是适用于 Linux 的 Windows 子系统 (WSL)，可以安装适用于 Linux 发行版的包。</span><span class="sxs-lookup"><span data-stu-id="979c0-106">If you are running Windows Subsystem for Linux (WSL), there are packages available for your Linux distribution.</span></span> <span data-ttu-id="979c0-107">请参阅[安装主页](install-azure-cli.md)，获取受支持包管理器的列表，或者了解如何在 WSL 下手动进行安装。</span><span class="sxs-lookup"><span data-stu-id="979c0-107">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update"></a><span data-ttu-id="979c0-108">安装或更新</span><span class="sxs-lookup"><span data-stu-id="979c0-108">Install or update</span></span>

<span data-ttu-id="979c0-109">MSI 发行版用于在 Windows 上安装、更新和卸载 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="979c0-109">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="979c0-110">下载 MSI 安装程序</span><span class="sxs-lookup"><span data-stu-id="979c0-110">Download the MSI installer</span></span>](https://aka.ms/InstallAzureCliWindows)

<span data-ttu-id="979c0-111">当安装程序询问是否可以对计算机进行更改时，请单击“是”框。</span><span class="sxs-lookup"><span data-stu-id="979c0-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="979c0-112">现在可以通过 Windows 命令提示符或 PowerShell 使用 `az` 命令运行 Azure CLI 了。</span><span class="sxs-lookup"><span data-stu-id="979c0-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="979c0-113">PowerShell 提供了 CMD 所不能提供的一些 Tab 键补全功能。</span><span class="sxs-lookup"><span data-stu-id="979c0-113">PowerShell offers some tab completion features not available from CMD.</span></span>

## <a name="uninstall"></a><span data-ttu-id="979c0-114">卸载</span><span class="sxs-lookup"><span data-stu-id="979c0-114">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="979c0-115">再次运行 MSI 并选择“卸载”选项即可进行卸载。</span><span class="sxs-lookup"><span data-stu-id="979c0-115">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span> 

> [!div class="nextstepaction"]
> [<span data-ttu-id="979c0-116">下载 MSI 安装程序</span><span class="sxs-lookup"><span data-stu-id="979c0-116">Download the MSI installer</span></span>](https://aka.ms/InstallAzureCliWindows)