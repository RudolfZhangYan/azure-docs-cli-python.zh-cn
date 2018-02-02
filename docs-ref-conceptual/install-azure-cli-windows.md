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
# <a name="install-azure-cli-20-on-windows"></a>在 Windows 上安装 Azure CLI 2.0

在 Windows 上，Azure CLI 二进制文件是通过 MSI 安装的，因此，可以通过 Windows 命令提示符 (CMD) 或 PowerShell 访问 CLI。
如果运行的是适用于 Linux 的 Windows 子系统 (WSL)，可以安装适用于 Linux 发行版的包。 请参阅[安装主页](install-azure-cli.md)，获取受支持包管理器的列表，或者了解如何在 WSL 下手动进行安装。

## <a name="install-or-update"></a>安装或更新

MSI 发行版用于在 Windows 上安装、更新和卸载 `az` 命令。

> [!div class="nextstepaction"]
> [下载 MSI 安装程序](https://aka.ms/InstallAzureCliWindows)

当安装程序询问是否可以对计算机进行更改时，请单击“是”框。

现在可以通过 Windows 命令提示符或 PowerShell 使用 `az` 命令运行 Azure CLI 了。 PowerShell 提供了 CMD 所不能提供的一些 Tab 键补全功能。

## <a name="uninstall"></a>卸载

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

再次运行 MSI 并选择“卸载”选项即可进行卸载。 

> [!div class="nextstepaction"]
> [下载 MSI 安装程序](https://aka.ms/InstallAzureCliWindows)