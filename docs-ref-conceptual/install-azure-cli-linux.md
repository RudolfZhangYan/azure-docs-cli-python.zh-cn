---
title: "手动安装适用于 Linux 的 Azure CLI 2.0"
description: "如何在 Linux 上手动安装 Azure CLI 2.0"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 4ab1f70308810e045b9a1d923fd809ad9848f6c6
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="708ba-103">在 Linux 上手动安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="708ba-103">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="708ba-104">如果发行版中没有提供 Azure CLI 包，始终可以通过运行安装脚本来手动安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="708ba-104">If you do not have a package for the Azure CLI available on your distribution, you can always install the CLI manually by running an installation script.</span></span>

> [!NOTE]
> <span data-ttu-id="708ba-105">我们强烈建议使用 CLI 的包管理器。</span><span class="sxs-lookup"><span data-stu-id="708ba-105">It's strongly recommend that you use a package manager for the CLI.</span></span> <span data-ttu-id="708ba-106">使用包管理器可确保始终获得最新更新，并保证 CLI 组件的稳定性。</span><span class="sxs-lookup"><span data-stu-id="708ba-106">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="708ba-107">在手动安装之前，请检查发行版是否有对应的包。</span><span class="sxs-lookup"><span data-stu-id="708ba-107">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="708ba-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="708ba-108">Prerequisites</span></span>

<span data-ttu-id="708ba-109">若要安装 CLI，需确保系统中存在下述软件：</span><span class="sxs-lookup"><span data-stu-id="708ba-109">In order to install the CLI, you need the following software available on your system:</span></span>

* [<span data-ttu-id="708ba-110">Python 2.7 或 Python 3.x</span><span class="sxs-lookup"><span data-stu-id="708ba-110">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="708ba-111">libffi</span><span class="sxs-lookup"><span data-stu-id="708ba-111">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="708ba-112">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="708ba-112">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update"></a><span data-ttu-id="708ba-113">安装或更新</span><span class="sxs-lookup"><span data-stu-id="708ba-113">Install or update</span></span>

<span data-ttu-id="708ba-114">不管是安装还是更新 CLI，都需要执行完整安装。</span><span class="sxs-lookup"><span data-stu-id="708ba-114">Whether you are installing or updating the CLI, you need to perform a full installation.</span></span> <span data-ttu-id="708ba-115">具备先决条件以后，即可通过运行 `curl` 来安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="708ba-115">Once you have the prerequisites, you can install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="708ba-116">也可以下载并在本地运行脚本。</span><span class="sxs-lookup"><span data-stu-id="708ba-116">You can also download the script and run it locally instead.</span></span> <span data-ttu-id="708ba-117">可能需要重启 shell 才能使更改生效。</span><span class="sxs-lookup"><span data-stu-id="708ba-117">You may have to restart your shell in order for changes to take effect.</span></span> <span data-ttu-id="708ba-118">安装后，请使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="708ba-118">After installation, run the CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="708ba-119">故障排除</span><span class="sxs-lookup"><span data-stu-id="708ba-119">Troubleshooting</span></span>

<span data-ttu-id="708ba-120">下面是手动安装过程中可能出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="708ba-120">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="708ba-121">如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="708ba-121">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>
### <a name="curl-object-moved-error"></a><span data-ttu-id="708ba-122">curl“对象已移动”错误</span><span class="sxs-lookup"><span data-stu-id="708ba-122">curl "Object Moved" error</span></span>

<span data-ttu-id="708ba-123">如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：</span><span class="sxs-lookup"><span data-stu-id="708ba-123">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="708ba-124">找不到 `az` 命令</span><span class="sxs-lookup"><span data-stu-id="708ba-124">`az` command not found</span></span>

<span data-ttu-id="708ba-125">如果在安装后以及在使用 `bash` 或 `zsh` 时无法运行该命令，请清除 shell 的命令哈希缓存。</span><span class="sxs-lookup"><span data-stu-id="708ba-125">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="708ba-126">运行</span><span class="sxs-lookup"><span data-stu-id="708ba-126">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="708ba-127">并查看问题是否得到解决。</span><span class="sxs-lookup"><span data-stu-id="708ba-127">and check if the problem is resolved.</span></span>

<span data-ttu-id="708ba-128">如果在安装后没有重启 shell，也可能出现此错误。</span><span class="sxs-lookup"><span data-stu-id="708ba-128">The issue can also occur if you did not restart your shell after installation.</span></span> <span data-ttu-id="708ba-129">确保 `az` 命令的位置在 `$PATH` 中。</span><span class="sxs-lookup"><span data-stu-id="708ba-129">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="708ba-130">`az` 命令的位置为</span><span class="sxs-lookup"><span data-stu-id="708ba-130">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

## <a name="uninstall"></a><span data-ttu-id="708ba-131">卸载</span><span class="sxs-lookup"><span data-stu-id="708ba-131">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="708ba-132">可以通过直接从安装时所选的位置删除文件来卸载 CLI。</span><span class="sxs-lookup"><span data-stu-id="708ba-132">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="708ba-133">默认安装位置是 `$HOME`。</span><span class="sxs-lookup"><span data-stu-id="708ba-133">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="708ba-134">删除安装的 CLI 文件。</span><span class="sxs-lookup"><span data-stu-id="708ba-134">Remove the installed CLI files.</span></span>

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```
2. <span data-ttu-id="708ba-135">修改 `$HOME/.bash_profile` 文件，删除以下行：</span><span class="sxs-lookup"><span data-stu-id="708ba-135">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>

  ```
  <install location>/lib/azure-cli/az.completion
  ```

3. <span data-ttu-id="708ba-136">如果使用 `bash` 或 `zsh`，请重新加载 shell 的命令缓存。</span><span class="sxs-lookup"><span data-stu-id="708ba-136">If using `bash` or `zsh`, reload your shell's command cache.</span></span>

  ```bash
  hash -r
  ```
