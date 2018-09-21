---
title: 安装适用于 macOS 的 Azure CLI
description: 如何在 macOS 上安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: fd829c6ff9162b660a889d3e08615a76f42aeb97
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388467"
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="e22dd-103">在 macOS 上安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="e22dd-103">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="e22dd-104">对于 macOS 平台，可以通过 [homebrew 包管理器](https://brew.sh)安装 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="e22dd-104">For the macOS platform, you can install the Azure CLI with [homebrew package manager](https://brew.sh).</span></span> <span data-ttu-id="e22dd-105">使用 Homebrew 可以轻松保持 CLI 的最新安装状态。</span><span class="sxs-lookup"><span data-stu-id="e22dd-105">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="e22dd-106">该 CLI 包已在 macOS 10.9 和更高版本中测试。</span><span class="sxs-lookup"><span data-stu-id="e22dd-106">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

## <a name="install"></a><span data-ttu-id="e22dd-107">安装</span><span class="sxs-lookup"><span data-stu-id="e22dd-107">Install</span></span>

<span data-ttu-id="e22dd-108">Homebrew 是管理 CLI 安装的最容易的方法。</span><span class="sxs-lookup"><span data-stu-id="e22dd-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="e22dd-109">它可以方便地进行安装、更新和卸载。</span><span class="sxs-lookup"><span data-stu-id="e22dd-109">It provides convenient ways to install, update, and uninstall.</span></span>
<span data-ttu-id="e22dd-110">如果系统中没有可用的 Homebrew，请先[安装 Homebrew](https://docs.brew.sh/Installation.html)，然后继续。</span><span class="sxs-lookup"><span data-stu-id="e22dd-110">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="e22dd-111">安装 CLI 时，可以先更新 brew 存储库信息，然后运行 `install` 命令：</span><span class="sxs-lookup"><span data-stu-id="e22dd-111">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="e22dd-112">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="e22dd-112">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="e22dd-113">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="e22dd-113">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="e22dd-114">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="e22dd-114">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="e22dd-115">故障排除</span><span class="sxs-lookup"><span data-stu-id="e22dd-115">Troubleshooting</span></span>

<span data-ttu-id="e22dd-116">如果在通过 Homebrew 安装 CLI 时遇到问题，会显示以下常见错误。</span><span class="sxs-lookup"><span data-stu-id="e22dd-116">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="e22dd-117">如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="e22dd-117">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="e22dd-118">找不到 Python 或安装的包</span><span class="sxs-lookup"><span data-stu-id="e22dd-118">Unable to find Python or installed packages</span></span>

<span data-ttu-id="e22dd-119">在执行 Homebrew 安装期间，可能会出现次要版本不匹配或其他问题。</span><span class="sxs-lookup"><span data-stu-id="e22dd-119">There may be a minor version mismatch or other issue during homebrew installation.</span></span> <span data-ttu-id="e22dd-120">CLI 不会使用 Python 虚拟环境，因此，它只能查找已安装的 Python 版本。</span><span class="sxs-lookup"><span data-stu-id="e22dd-120">The CLI doesn't use a Python virtual environment, so it relies on finding the installed Python version.</span></span> <span data-ttu-id="e22dd-121">可行的解决方法之一是从 Homebrew 安装并重新链接 `python3` 依赖项。</span><span class="sxs-lookup"><span data-stu-id="e22dd-121">A possible fix is to install and relink the `python3` dependency from Homebrew.</span></span>

```bash
brew update && brew install python3 && brew upgrade python3
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="e22dd-122">已安装 CLI 安装 1.x</span><span class="sxs-lookup"><span data-stu-id="e22dd-122">CLI version 1.x is installed</span></span>

<span data-ttu-id="e22dd-123">如果安装了过时的版本，则陈旧的 Homebrew 缓存可能导致此问题。</span><span class="sxs-lookup"><span data-stu-id="e22dd-123">If an out-of-date version was installed, it could be because of a stale homebrew cache.</span></span> <span data-ttu-id="e22dd-124">请遵照[更新](#Update)说明操作。</span><span class="sxs-lookup"><span data-stu-id="e22dd-124">Follow the [update](#Update) instructions.</span></span>

## <a name="update"></a><span data-ttu-id="e22dd-125">更新</span><span class="sxs-lookup"><span data-stu-id="e22dd-125">Update</span></span>

<span data-ttu-id="e22dd-126">CLI 定期使用 Bug 修复、改进、新功能和预览版功能进行更新。</span><span class="sxs-lookup"><span data-stu-id="e22dd-126">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="e22dd-127">新版本大约两周发布一次。</span><span class="sxs-lookup"><span data-stu-id="e22dd-127">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="e22dd-128">更新本地存储库信息，然后升级 `azure-cli` 包。</span><span class="sxs-lookup"><span data-stu-id="e22dd-128">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="e22dd-129">卸载</span><span class="sxs-lookup"><span data-stu-id="e22dd-129">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="e22dd-130">使用 Homebrew 卸载 `azure-cli` 包。</span><span class="sxs-lookup"><span data-stu-id="e22dd-130">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```
