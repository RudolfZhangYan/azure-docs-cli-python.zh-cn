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
ms.openlocfilehash: 247ae43813ca9ca7b7b98ebd8e933e02989c6649
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-windows"></a>在 Windows 上安装 Azure CLI 2.0

可以在 Windows 上安装一个源自 MSI 的本机二进制文件，该文件可以通过 Windows 命令提示符或 PowerShell 来使用。 若要运行适用于 Linux 的 Windows 子系统 (WSL)，则可使用适合所运行发行版的包。 请参阅[安装主页](install-azure-cli.md)，获取受支持包管理器的列表，或者了解如何在 WSL 下手动进行安装。

## <a name="install-or-update-with-msi"></a>使用 MSI 进行安装或更新

MSI 发行版用于在 Windows 上安装、更新和卸载 `az` 命令。 可以[下载 MSI 安装程序](https://aka.ms/InstallAzureCliWindows)，在运行后即可进行安装或更新。

当安装程序询问是否可以对计算机进行更改时，请单击“是”框。

现在可以通过 Windows 命令提示符或 PowerShell 使用 `az` 命令运行 Azure CLI 了。

## <a name="uninstall-with-msi"></a>使用 MSI 卸载

如果你决定卸载 Azure CLI，我们会很遗憾。 在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。 我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。 也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。

再次运行 MSI 并选择“卸载”选项即可进行卸载。 可以[下载 MSI 安装程序](https://aka.ms/InstallAzureCliWindows)（如果在卸载 CLI 后又需要使用）。
