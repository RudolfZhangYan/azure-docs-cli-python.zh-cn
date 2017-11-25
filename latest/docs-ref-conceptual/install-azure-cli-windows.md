---
title: "安装适用于 Windows 的 Azure CLI"
description: "如何在 Windows 上安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure 安装 windows, azure cli windows, azure windows"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 96a123575226f281accf125cb5bb29ee7d14ef2a
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-windows"></a><span data-ttu-id="c30f4-104">在 Windows 上安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="c30f4-104">Install Azure CLI 2.0 on Windows</span></span>

<span data-ttu-id="c30f4-105">可以在 Windows 上安装一个源自 MSI 的本机二进制文件，该文件可以通过 Windows 命令提示符或 PowerShell 来使用。</span><span class="sxs-lookup"><span data-stu-id="c30f4-105">On Windows, you can install a native binary from an MSI, which you can use through the Windows Command Prompt or PowerShell.</span></span> <span data-ttu-id="c30f4-106">若要运行适用于 Linux 的 Windows 子系统 (WSL)，则可使用适合所运行发行版的包。</span><span class="sxs-lookup"><span data-stu-id="c30f4-106">If you are running Windows Subsystem for Linux (WSL) there are packages available for the distribution you are running.</span></span> <span data-ttu-id="c30f4-107">请参阅[安装主页](install-azure-cli.md)，获取受支持包管理器的列表，或者了解如何在 WSL 下手动进行安装。</span><span class="sxs-lookup"><span data-stu-id="c30f4-107">See the [main install page](install-azure-cli.md) for the list of supported package managers or how to install manually under WSL.</span></span>

## <a name="install-or-update-with-msi"></a><span data-ttu-id="c30f4-108">使用 MSI 进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="c30f4-108">Install or update with MSI</span></span>

<span data-ttu-id="c30f4-109">MSI 发行版用于在 Windows 上安装、更新和卸载 `az` 命令。</span><span class="sxs-lookup"><span data-stu-id="c30f4-109">The MSI distributable is used for installing, updating, and uninstalling the `az` command on Windows.</span></span> <span data-ttu-id="c30f4-110">可以[下载 MSI 安装程序](https://aka.ms/InstallAzureCliWindows)，在运行后即可进行安装或更新。</span><span class="sxs-lookup"><span data-stu-id="c30f4-110">You can [download the MSI installer](https://aka.ms/InstallAzureCliWindows) and then run it to install or update.</span></span>

<span data-ttu-id="c30f4-111">当安装程序询问是否可以对计算机进行更改时，请单击“是”框。</span><span class="sxs-lookup"><span data-stu-id="c30f4-111">When the installer asks if it can make changes to your computer, click the "Yes" box.</span></span>

<span data-ttu-id="c30f4-112">现在可以通过 Windows 命令提示符或 PowerShell 使用 `az` 命令运行 Azure CLI 了。</span><span class="sxs-lookup"><span data-stu-id="c30f4-112">You can now run the Azure CLI with the `az` command from either Windows Command Prompt or PowerShell.</span></span>

## <a name="uninstall-with-msi"></a><span data-ttu-id="c30f4-113">使用 MSI 卸载</span><span class="sxs-lookup"><span data-stu-id="c30f4-113">Uninstall with MSI</span></span>

<span data-ttu-id="c30f4-114">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="c30f4-114">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="c30f4-115">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="c30f4-115">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="c30f4-116">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="c30f4-116">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="c30f4-117">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="c30f4-117">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="c30f4-118">再次运行 MSI 并选择“卸载”选项即可进行卸载。</span><span class="sxs-lookup"><span data-stu-id="c30f4-118">Uninstalling can be done by running the MSI again, and choosing the "Uninstall" option.</span></span> <span data-ttu-id="c30f4-119">可以[下载 MSI 安装程序](https://aka.ms/InstallAzureCliWindows)（如果在卸载 CLI 后又需要使用）。</span><span class="sxs-lookup"><span data-stu-id="c30f4-119">You can [download the MSI installer](https://aka.ms/InstallAzureCliWindows) if you no longer have it available.</span></span>
