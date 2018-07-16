---
title: 安装适用于 macOS 的 Azure CLI
description: 如何在 macOS 上安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 76b9afec92aa3da916382b85d2261547b6877e03
ms.sourcegitcommit: fb3fed8701aff6c46af856e8fdc3e56ff9a678bc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2018
ms.locfileid: "38228914"
---
# <a name="install-azure-cli-20-on-macos"></a>在 macOS 上安装 Azure CLI 2.0

对于 macOS 平台，可以通过 [homebrew 包管理器](http://brew.sh)安装 Azure CLI。 使用 Homebrew 可以轻松保持 CLI 的最新安装状态。 该 CLI 包已在 macOS 10.9 和更高版本中测试。

## <a name="install"></a>安装

Homebrew 是管理 CLI 安装的最容易的方法。 它可以方便地进行安装、更新和卸载。
如果系统中没有可用的 Homebrew，请先[安装 Homebrew](https://docs.brew.sh/Installation.html)，然后继续。

安装 CLI 时，可以先更新 brew 存储库信息，然后运行 `install` 命令：

```bash
brew update && brew install azure-cli
```

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

## <a name="troubleshooting"></a>故障排除

如果在通过 Homebrew 安装 CLI 时遇到问题，会显示以下常见错误。 如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。

### <a name="unable-to-find-python-or-installed-packages"></a>找不到 Python 或安装的包

如果安装后找不到 Python 或安装的包，则可能是在 Homebrew 安装过程中出现了轻度的版本不匹配问题或其他问题。 由于 CLI 不使用 Python 虚拟环境，因此它必须能够找到正确的 Python 版本。 可以通过重新链接 Python 安装来解决这些问题。

```bash
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a>已安装 CLI 安装 1.x

如果安装了过时的版本，则陈旧的 Homebrew 缓存可能导致此问题。 请遵照[更新](#Update)说明操作。

## <a name="update"></a>更新

CLI 定期使用 Bug 修复、改进、新功能和预览版功能进行更新。 新版本大约两周发布一次。 更新本地存储库信息，然后升级 `azure-cli` 包。

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a>卸载

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

使用 Homebrew 卸载 `azure-cli` 包。

```bash
brew uninstall azure-cli
```
