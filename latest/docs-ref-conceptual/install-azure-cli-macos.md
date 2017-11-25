---
title: "安装适用于 macOS 的 Azure CLI"
description: "如何在 macOS 上安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure macos, azure 安装 macos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: e615d2b3ab3b1307e982cb1d4d456633440afdf6
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-macos"></a>在 macOS 上安装 Azure CLI 2.0

对于 macOS 平台，可以通过 [Homebrew 包管理器](http://brew.sh)来安装 Azure CLI，也可以手动安装。 首选安装方法是使用 Homebrew，这样可以在需要时更容易地进行安装、更新获取和卸载操作。

## <a name="use-homebrew-to-install"></a>使用 Homebrew 进行安装

Homebrew 是管理 CLI 安装的最容易的方法。 它可以方便地进行安装、更新和卸载。 它类似于其他包管理器，例如 `apt` 或 `yum`。
如果系统中没有可用的 Homebrew，请先[安装 Homebrew](https://docs.brew.sh/Installation.html)，然后继续。

### <a name="install-with-homebrew"></a>使用 Homebrew 进行安装

安装 CLI 时，可以先更新 brew 存储库信息，然后运行 `install` 命令：

```bash
brew update && brew install azure-cli
```

然后即可使用 `az` 命令来运行 Azure CLI。

### <a name="update-with-homebrew"></a>使用 Homebrew 进行更新

CLI 定期使用 Bug 修复、改进、新功能和预览版功能进行更新。 新版本大约两周发布一次。 需更新本地存储库信息，然后更新 CLI 包。

```bash
brew update && brew upgrade azure-cli
```

### <a name="troubleshooting"></a>故障排除

使用 Homebrew 安装或更新 CLI 时，是否遇到问题？ 下面是一些可能发生的常见错误，以及相应的诊断和解决方法。

#### <a name="unable-to-find-python-or-installed-packages"></a>找不到 Python 或安装的包

如果安装后找不到 Python 或安装的包，则可能是在 Homebrew 安装过程中出现了轻度的版本不匹配问题或其他问题。 CLI 不使用 virtualenv，因此需要能够找到 Homebrew 安装的 Python 的正确版本。 可以通过重新链接 Python 安装来解决这些问题：

```bash
brew link --overwrite python3
```

#### <a name="the-cli-version-is-out-of-date"></a>CLI 版本已过期

如果你认为安装的 CLI 版本可能已过期，则需先运行 `brew update` 命令，然后运行 `brew upgrade azure-cli`。 如果这样无法更新 CLI，需考虑到 Homebrew 包的推出速度可能比常规版本慢。 如果需要安装 CLI 的前沿版本，则应[手动进行安装](#manage-the-cli-manually)。

### <a name="uninstall-with-homebrew"></a>使用 Homebrew 进行卸载

如果你决定卸载 Azure CLI，我们会很遗憾。 在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。 我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。 也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。

如果是使用 Homebrew 安装的，则还应使用它来卸载。

```bash
brew uninstall azure-cli
```

## <a name="install-the-cli-manually"></a>手动安装 CLI

如果不能或者不希望使用 Homebrew 来管理 CLI 安装，则可手动进行安装。

按照 [Linux 手动安装说明](install-azure-cli-linux.md)在 macOS 上手动进行安装。 macOS 10.9 及更高版本应该包括所有必需的依赖项。
