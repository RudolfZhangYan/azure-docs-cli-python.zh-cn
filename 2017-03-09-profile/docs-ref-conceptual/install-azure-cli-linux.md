---
title: "手动安装适用于 Linux 的 Azure CLI 2.0"
description: "如何在 Linux 上手动安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure linux, azure 安装 linux"
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
ms.openlocfilehash: f792d3fc84eedade52ddfb3f351e48689e474d53
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="c5a96-104">在 Linux 上手动安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="c5a96-104">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="c5a96-105">如果发行版中没有提供 Azure CLI 包，则始终可以通过运行安装脚本来手动安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="c5a96-105">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manualy by running an installation script.</span></span> <span data-ttu-id="c5a96-106">如果提供了包，建议始终使用包来进行安装。</span><span class="sxs-lookup"><span data-stu-id="c5a96-106">If you do have a package available, that is always the recommended installation method.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c5a96-107">先决条件</span><span class="sxs-lookup"><span data-stu-id="c5a96-107">Prerequisites</span></span>

<span data-ttu-id="c5a96-108">若要安装 CLI，需确保系统中存在下述软件：</span><span class="sxs-lookup"><span data-stu-id="c5a96-108">In order to install the CLI, you will need the following software available on your system:</span></span>

* [<span data-ttu-id="c5a96-109">Python 2.7 或 Python 3.x</span><span class="sxs-lookup"><span data-stu-id="c5a96-109">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="c5a96-110">libffi</span><span class="sxs-lookup"><span data-stu-id="c5a96-110">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="c5a96-111">OpenSSL</span><span class="sxs-lookup"><span data-stu-id="c5a96-111">OpenSSL</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update-manually"></a><span data-ttu-id="c5a96-112">手动进行安装或更新</span><span class="sxs-lookup"><span data-stu-id="c5a96-112">Install or update manually</span></span>

<span data-ttu-id="c5a96-113">不管是安装还是更新 CLI，都需要执行完整的安装操作。</span><span class="sxs-lookup"><span data-stu-id="c5a96-113">Whether you are installing or updating the CLI, you will need to perform a full installation.</span></span> <span data-ttu-id="c5a96-114">具备先决条件以后，即可通过运行 `curl` 来安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="c5a96-114">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="c5a96-115">如果你愿意，或者如果系统中没有 `curl`，也可改为下载脚本并在本地运行。</span><span class="sxs-lookup"><span data-stu-id="c5a96-115">If you would prefer, or do not have `curl` on your system, you can download the script and run it locally instead.</span></span> <span data-ttu-id="c5a96-116">可能需要重启 shell 才能使更改生效。</span><span class="sxs-lookup"><span data-stu-id="c5a96-116">You may have to restart your shell in order for changes to take effect.</span></span> <span data-ttu-id="c5a96-117">安装后，请使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="c5a96-117">After installation, run the CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c5a96-118">故障排除</span><span class="sxs-lookup"><span data-stu-id="c5a96-118">Troubleshooting</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="c5a96-119">curl“对象已移动”错误</span><span class="sxs-lookup"><span data-stu-id="c5a96-119">curl "Object Moved" error</span></span>

<span data-ttu-id="c5a96-120">如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：</span><span class="sxs-lookup"><span data-stu-id="c5a96-120">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="c5a96-121">找不到 `az` 命令</span><span class="sxs-lookup"><span data-stu-id="c5a96-121">`az` command not found</span></span>

<span data-ttu-id="c5a96-122">如果在安装后无法运行该命令，则可能需要清除 shell 的命令哈希缓存。</span><span class="sxs-lookup"><span data-stu-id="c5a96-122">After installation if you can't run the command, you may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="c5a96-123">运行</span><span class="sxs-lookup"><span data-stu-id="c5a96-123">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="c5a96-124">并查看问题是否得以解决。</span><span class="sxs-lookup"><span data-stu-id="c5a96-124">and see if the problem is resolved.</span></span> 

<span data-ttu-id="c5a96-125">如果在安装后没有重启 shell，也可能出现此问题。</span><span class="sxs-lookup"><span data-stu-id="c5a96-125">This can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="c5a96-126">确保 `az` 命令的位置在 `$PATH` 中。</span><span class="sxs-lookup"><span data-stu-id="c5a96-126">Make sure that the location of the `az` command is in your `$PATH`.</span></span>

<span data-ttu-id="c5a96-127">如果运行过安装脚本，则该位置为：</span><span class="sxs-lookup"><span data-stu-id="c5a96-127">If you ran the installation script, this will be:</span></span>

```bash
<install path>/bin
```

## <a name="unstinall-manually"></a><span data-ttu-id="c5a96-128">手动卸载</span><span class="sxs-lookup"><span data-stu-id="c5a96-128">Unstinall manually</span></span>

<span data-ttu-id="c5a96-129">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="c5a96-129">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="c5a96-130">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="c5a96-130">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="c5a96-131">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="c5a96-131">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="c5a96-132">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="c5a96-132">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="c5a96-133">可以通过直接从安装位置删除文件的方式卸载 CLI。</span><span class="sxs-lookup"><span data-stu-id="c5a96-133">You can uninstall the CLI by directly deleting the files from the install location.</span></span> <span data-ttu-id="c5a96-134">如果是通过 `https://aka.ms/InstallAzureCLI` 脚本进行的安装，则应已在安装时选定安装位置。</span><span class="sxs-lookup"><span data-stu-id="c5a96-134">Your install location should have been chosen at the time of install, if you installed via the `https://aka.ms/InstallAzureCLI` script.</span></span> <span data-ttu-id="c5a96-135">默认安装位置为 `$HOME`。</span><span class="sxs-lookup"><span data-stu-id="c5a96-135">The default installation location is `$HOME`.</span></span>

<span data-ttu-id="c5a96-136">首先，删除安装的 CLI 文件：</span><span class="sxs-lookup"><span data-stu-id="c5a96-136">First, remove the installed CLI files:</span></span>

```bash
rm -r <install location>/lib/azure-cli
rm <install location>/bin/az
```

<span data-ttu-id="c5a96-137">然后修改 `$HOME/.bash_profile` 文件，删除以下行：</span><span class="sxs-lookup"><span data-stu-id="c5a96-137">Then modify your `$HOME/.bash_profile` file to remove the line:</span></span>

```
<install location>/lib/azure-cli/az.completion
```

<span data-ttu-id="c5a96-138">最后，重载 shell 的命令缓存（如果已启用）。</span><span class="sxs-lookup"><span data-stu-id="c5a96-138">And finally, reload your shell's command cache if it uses one.</span></span> <span data-ttu-id="c5a96-139">`bash` 和 `zsh` 用户需执行以下步骤：</span><span class="sxs-lookup"><span data-stu-id="c5a96-139">`bash` and `zsh` users will need to perform this step:</span></span>

```bash
hash -r
```
