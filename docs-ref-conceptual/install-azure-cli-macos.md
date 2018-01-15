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
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-on-macos"></a><span data-ttu-id="f55bc-104">在 macOS 上安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="f55bc-104">Install Azure CLI 2.0 on macOS</span></span>

<span data-ttu-id="f55bc-105">对于 macOS 平台，可以通过 [Homebrew 包管理器](http://brew.sh)来安装 Azure CLI，也可以手动安装。</span><span class="sxs-lookup"><span data-stu-id="f55bc-105">For the macOS platform, you can install the Azure CLI either through the [homebrew package manager](http://brew.sh) or manually.</span></span> <span data-ttu-id="f55bc-106">首选安装方法是使用 Homebrew，这样可以在需要时更容易地进行安装、更新获取和卸载操作。</span><span class="sxs-lookup"><span data-stu-id="f55bc-106">The preferred installation method is through homebrew, so that it's easier to install, get updates, and uninstall if you need to.</span></span>

## <a name="use-homebrew-to-install"></a><span data-ttu-id="f55bc-107">使用 Homebrew 进行安装</span><span class="sxs-lookup"><span data-stu-id="f55bc-107">Use homebrew to install</span></span>

<span data-ttu-id="f55bc-108">Homebrew 是管理 CLI 安装的最容易的方法。</span><span class="sxs-lookup"><span data-stu-id="f55bc-108">Homebrew is the easiest way to manage your CLI install.</span></span> <span data-ttu-id="f55bc-109">它可以方便地进行安装、更新和卸载。</span><span class="sxs-lookup"><span data-stu-id="f55bc-109">It provides convenient ways to install, update, and uninstall.</span></span> <span data-ttu-id="f55bc-110">它类似于其他包管理器，例如 `apt` 或 `yum`。</span><span class="sxs-lookup"><span data-stu-id="f55bc-110">It's similar to other package managers such as `apt` or `yum`.</span></span>
<span data-ttu-id="f55bc-111">如果系统中没有可用的 Homebrew，请先[安装 Homebrew](https://docs.brew.sh/Installation.html)，然后继续。</span><span class="sxs-lookup"><span data-stu-id="f55bc-111">If you don't have homebrew available on your system, [install homebrew](https://docs.brew.sh/Installation.html) before continuing.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="f55bc-112">使用 Homebrew 进行安装</span><span class="sxs-lookup"><span data-stu-id="f55bc-112">Install with homebrew</span></span>

<span data-ttu-id="f55bc-113">安装 CLI 时，可以先更新 brew 存储库信息，然后运行 `install` 命令：</span><span class="sxs-lookup"><span data-stu-id="f55bc-113">You can install the CLI by updating your brew repository information, and then running the `install` command:</span></span>

```bash
brew update && brew install azure-cli
```

<span data-ttu-id="f55bc-114">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="f55bc-114">You can then run the Azure CLI with the `az` command.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="f55bc-115">使用 Homebrew 进行更新</span><span class="sxs-lookup"><span data-stu-id="f55bc-115">Update with homebrew</span></span>

<span data-ttu-id="f55bc-116">CLI 定期使用 Bug 修复、改进、新功能和预览版功能进行更新。</span><span class="sxs-lookup"><span data-stu-id="f55bc-116">The CLI is regularly updated with bug fixes, improvements, new features, and preview functionality.</span></span> <span data-ttu-id="f55bc-117">新版本大约两周发布一次。</span><span class="sxs-lookup"><span data-stu-id="f55bc-117">A new release is available roughly every two weeks.</span></span> <span data-ttu-id="f55bc-118">需更新本地存储库信息，然后更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="f55bc-118">You will need to update your local repository information, and then update the CLI package.</span></span>

```bash
brew update && brew upgrade azure-cli
```

### <a name="troubleshooting"></a><span data-ttu-id="f55bc-119">故障排除</span><span class="sxs-lookup"><span data-stu-id="f55bc-119">Troubleshooting</span></span>

<span data-ttu-id="f55bc-120">使用 Homebrew 安装或更新 CLI 时，是否遇到问题？</span><span class="sxs-lookup"><span data-stu-id="f55bc-120">Did you encounter a problem when installing or updating the CLI with homebrew?</span></span> <span data-ttu-id="f55bc-121">下面是一些可能发生的常见错误，以及相应的诊断和解决方法。</span><span class="sxs-lookup"><span data-stu-id="f55bc-121">Here are some common errors that might occur, and ways to diagnose and resolve them.</span></span>

#### <a name="unable-to-find-python-or-installed-packages"></a><span data-ttu-id="f55bc-122">找不到 Python 或安装的包</span><span class="sxs-lookup"><span data-stu-id="f55bc-122">Unable to find Python or installed packages</span></span>

<span data-ttu-id="f55bc-123">如果安装后找不到 Python 或安装的包，则可能是在 Homebrew 安装过程中出现了轻度的版本不匹配问题或其他问题。</span><span class="sxs-lookup"><span data-stu-id="f55bc-123">If your install is unable to find Python or installed packages, there may be a minor version mismatch or other issue which occurred during homebrew installation.</span></span> <span data-ttu-id="f55bc-124">CLI 不使用 virtualenv，因此需要能够找到 Homebrew 安装的 Python 的正确版本。</span><span class="sxs-lookup"><span data-stu-id="f55bc-124">Since the CLI does not use a virtualenv, it relies on being able to find correct versions of Python installed by homebrew.</span></span> <span data-ttu-id="f55bc-125">可以通过重新链接 Python 安装来解决这些问题：</span><span class="sxs-lookup"><span data-stu-id="f55bc-125">You may be able to fix these issues by re-linking your Python installation:</span></span>

```bash
brew link --overwrite python3
```

#### <a name="the-cli-version-is-out-of-date"></a><span data-ttu-id="f55bc-126">CLI 版本已过期</span><span class="sxs-lookup"><span data-stu-id="f55bc-126">The CLI version is out of date</span></span>

<span data-ttu-id="f55bc-127">如果你认为安装的 CLI 版本可能已过期，则需先运行 `brew update` 命令，然后运行 `brew upgrade azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="f55bc-127">If you think that your installed CLI version might be out of date, you will need to run a `brew update` command, followed by `brew upgrade azure-cli`.</span></span> <span data-ttu-id="f55bc-128">如果这样无法更新 CLI，需考虑到 Homebrew 包的推出速度可能比常规版本慢。</span><span class="sxs-lookup"><span data-stu-id="f55bc-128">If this does not update the CLI, be aware that homebrew packages may roll out more slowly than general releases.</span></span> <span data-ttu-id="f55bc-129">如果需要安装 CLI 的前沿版本，则应[手动进行安装](#manage-the-cli-manually)。</span><span class="sxs-lookup"><span data-stu-id="f55bc-129">If you require bleeding-edge installs of the CLI, then you should [install manually](#manage-the-cli-manually).</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="f55bc-130">使用 Homebrew 进行卸载</span><span class="sxs-lookup"><span data-stu-id="f55bc-130">Uninstall with homebrew</span></span>

<span data-ttu-id="f55bc-131">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="f55bc-131">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="f55bc-132">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="f55bc-132">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="f55bc-133">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="f55bc-133">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="f55bc-134">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="f55bc-134">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="f55bc-135">如果是使用 Homebrew 安装的，则还应使用它来卸载。</span><span class="sxs-lookup"><span data-stu-id="f55bc-135">If you installed with homebrew, you should also use it to uninstall.</span></span>

```bash
brew uninstall azure-cli
```

## <a name="install-the-cli-manually"></a><span data-ttu-id="f55bc-136">手动安装 CLI</span><span class="sxs-lookup"><span data-stu-id="f55bc-136">Install the CLI manually</span></span>

<span data-ttu-id="f55bc-137">如果不能或者不希望使用 Homebrew 来管理 CLI 安装，则可手动进行安装。</span><span class="sxs-lookup"><span data-stu-id="f55bc-137">If you can't or don't want to rely on homebrew to manage the CLI install for you, then you can manually install.</span></span>

<span data-ttu-id="f55bc-138">按照 [Linux 手动安装说明](install-azure-cli-linux.md)在 macOS 上手动进行安装。</span><span class="sxs-lookup"><span data-stu-id="f55bc-138">Follow the [manual Linux installation instructions](install-azure-cli-linux.md) to install manually on macOS.</span></span> <span data-ttu-id="f55bc-139">macOS 10.9 及更高版本应该包括所有必需的依赖项。</span><span class="sxs-lookup"><span data-stu-id="f55bc-139">macOS versions 10.9 and later should include all of the required dependencies.</span></span>
