---
title: 安装适用于 macOS 的 Azure CLI
description: 如何在 macOS 上安装 Azure CLI
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 9eb816ef68d24d1dbbaaeb5fd4877580edbe87ad
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177651"
---
# <a name="install-azure-cli-on-macos"></a><span data-ttu-id="12d2e-103">在 macOS 上安装 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="12d2e-103">Install Azure CLI on macOS</span></span>

<span data-ttu-id="12d2e-104">对于 macOS 平台，可以通过 [homebrew 包管理器](https://brew.sh)安装 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="12d2e-104">For the macOS platform, you can install the Azure CLI with [homebrew package manager](https://brew.sh).</span></span> <span data-ttu-id="12d2e-105">使用 Homebrew 可以轻松保持 CLI 的最新安装状态。</span><span class="sxs-lookup"><span data-stu-id="12d2e-105">Homebrew makes it easy to keep your installation of the CLI update to date.</span></span> <span data-ttu-id="12d2e-106">该 CLI 包已在 macOS 10.9 和更高版本中测试。</span><span class="sxs-lookup"><span data-stu-id="12d2e-106">The CLI package has been tested on macOS versions 10.9 and later.</span></span>

## <a name="install"></a><span data-ttu-id="12d2e-107">安装</span><span class="sxs-lookup"><span data-stu-id="12d2e-107">Install</span></span>

<span data-ttu-id="12d2e-108">Homebrew 是管理 CLI 安装的最容易的方法。</span><span class="sxs-lookup"><span data-stu-id="12d2e-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="12d2e-109">它可以方便地进行安装、更新和卸载。</span><span class="sxs-lookup"><span data-stu-id="12d2e-109">It provides convenient ways to install, update, and uninstall.</span></span>
<span data-ttu-id="12d2e-110">如果系统中没有可用的 Homebrew，请先[安装 Homebrew](https://docs.brew.sh/Installation.html)，然后继续。</span><span class="sxs-lookup"><span data-stu-id="12d2e-110">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

<span data-ttu-id="12d2e-111">安装 CLI 时，可以先更新 brew 存储库信息，然后运行 `install` 命令：</span><span class="sxs-lookup"><span data-stu-id="12d2e-111">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="12d2e-112">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="12d2e-112">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="12d2e-113">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="12d2e-113">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="12d2e-114">若要详细了解不同的身份验证方法，请参阅[使用 Azure CLI 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="12d2e-114">To learn more about different authentication methods, see [Sign in with Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="12d2e-115">故障排除</span><span class="sxs-lookup"><span data-stu-id="12d2e-115">Troubleshooting</span></span>

<span data-ttu-id="12d2e-116">如果在通过 Homebrew 安装 CLI 时遇到问题，会显示以下常见错误。</span><span class="sxs-lookup"><span data-stu-id="12d2e-116">If you encounter a problem when installing the CLI through Homebrew, here are some common errors.</span></span> <span data-ttu-id="12d2e-117">如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="12d2e-117">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="12d2e-118">找不到 Python 或安装的包</span><span class="sxs-lookup"><span data-stu-id="12d2e-118">Unable to find Python or installed packages</span></span>

<span data-ttu-id="12d2e-119">在执行 Homebrew 安装期间，可能会出现次要版本不匹配或其他问题。</span><span class="sxs-lookup"><span data-stu-id="12d2e-119">There may be a minor version mismatch or other issue during homebrew installation.</span></span> <span data-ttu-id="12d2e-120">CLI 不会使用 Python 虚拟环境，因此，它只能查找已安装的 Python 版本。</span><span class="sxs-lookup"><span data-stu-id="12d2e-120">The CLI doesn't use a Python virtual environment, so it relies on finding the installed Python version.</span></span> <span data-ttu-id="12d2e-121">可行的解决方法之一是从 Homebrew 安装并重新链接 `python3` 依赖项。</span><span class="sxs-lookup"><span data-stu-id="12d2e-121">A possible fix is to install and relink the `python3` dependency from Homebrew.</span></span>

```bash
brew update && brew install python3 && brew upgrade python3
brew link --overwrite python3
```

### <a name="cli-version-1x-is-installed"></a><span data-ttu-id="12d2e-122">已安装 CLI 安装 1.x</span><span class="sxs-lookup"><span data-stu-id="12d2e-122">CLI version 1.x is installed</span></span>

<span data-ttu-id="12d2e-123">如果安装了过时的版本，则陈旧的 Homebrew 缓存可能导致此问题。</span><span class="sxs-lookup"><span data-stu-id="12d2e-123">If an out-of-date version was installed, it could be because of a stale homebrew cache.</span></span> <span data-ttu-id="12d2e-124">请遵照[更新](#Update)说明操作。</span><span class="sxs-lookup"><span data-stu-id="12d2e-124">Follow the [update](#Update) instructions.</span></span>

## <a name="update"></a><span data-ttu-id="12d2e-125">更新</span><span class="sxs-lookup"><span data-stu-id="12d2e-125">Update</span></span>

<span data-ttu-id="12d2e-126">CLI 定期使用 Bug 修复、改进、新功能和预览版功能进行更新。</span><span class="sxs-lookup"><span data-stu-id="12d2e-126">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="12d2e-127">新版本大约两周发布一次。</span><span class="sxs-lookup"><span data-stu-id="12d2e-127">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="12d2e-128">更新本地存储库信息，然后升级 `azure-cli` 包。</span><span class="sxs-lookup"><span data-stu-id="12d2e-128">Update your local repository information and then upgrade the `azure-cli` package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="12d2e-129">卸载</span><span class="sxs-lookup"><span data-stu-id="12d2e-129">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="12d2e-130">使用 Homebrew 卸载 `azure-cli` 包。</span><span class="sxs-lookup"><span data-stu-id="12d2e-130">Use homebrew to uninstall the `azure-cli` package.</span></span>

```bash
brew uninstall azure-cli
```

## <a name="next-steps"></a><span data-ttu-id="12d2e-131">后续步骤</span><span class="sxs-lookup"><span data-stu-id="12d2e-131">Next Steps</span></span>

<span data-ttu-id="12d2e-132">现在你已经安装了 Azure CLI，下面简要介绍其功能和常用命令。</span><span class="sxs-lookup"><span data-stu-id="12d2e-132">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="12d2e-133">Azure CLI 入门</span><span class="sxs-lookup"><span data-stu-id="12d2e-133">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
