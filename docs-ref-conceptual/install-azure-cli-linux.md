---
title: 手动安装适用于 Linux 的 Azure CLI 2.0
description: 如何在 Linux 上手动安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: c5c7ea61a35e915760081897e88d8c43b80919e0
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388348"
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="c7ff4-103">在 Linux 上手动安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="c7ff4-103">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="c7ff4-104">如果没有适用于你的分发版的 Azure CLI 包，请运行一个脚本来手动安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-104">If there's no package for the Azure CLI for you your distribution, install the CLI manually by running a script.</span></span>

> [!NOTE]
> <span data-ttu-id="c7ff4-105">强烈建议使用包管理器安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-105">It's strongly recommend to install the CLI with a package manager.</span></span> <span data-ttu-id="c7ff4-106">使用包管理器可确保始终获得最新更新，并保证 CLI 组件的稳定性。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-106">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="c7ff4-107">在手动安装之前，请检查发行版是否有对应的包。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-107">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c7ff4-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="c7ff4-108">Prerequisites</span></span>

<span data-ttu-id="c7ff4-109">CLI 需要以下软件：</span><span class="sxs-lookup"><span data-stu-id="c7ff4-109">The CLI requires the following software:</span></span>

* [<span data-ttu-id="c7ff4-110">Python 2.7 或 Python 3.x</span><span class="sxs-lookup"><span data-stu-id="c7ff4-110">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="c7ff4-111">libffi</span><span class="sxs-lookup"><span data-stu-id="c7ff4-111">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="c7ff4-112">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="c7ff4-112">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update"></a><span data-ttu-id="c7ff4-113">安装或更新</span><span class="sxs-lookup"><span data-stu-id="c7ff4-113">Install or update</span></span>

<span data-ttu-id="c7ff4-114">安装和更新 CLI 都需要重新运行安装脚本。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-114">Both installing and updating the CLI requires re-running the install script.</span></span> <span data-ttu-id="c7ff4-115">运行 `curl` 来安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-115">Install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="c7ff4-116">也可以下载并在本地运行该脚本。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-116">The script can also be downloaded and run locally.</span></span> <span data-ttu-id="c7ff4-117">可能需要重启 shell 才能使更改生效。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-117">You may have to restart your shell in order for changes to take effect.</span></span>

<span data-ttu-id="c7ff4-118">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-118">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="c7ff4-119">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-119">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="c7ff4-120">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-120">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="c7ff4-121">故障排除</span><span class="sxs-lookup"><span data-stu-id="c7ff4-121">Troubleshooting</span></span>

<span data-ttu-id="c7ff4-122">下面是手动安装过程中可能出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-122">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="c7ff4-123">如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-123">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="c7ff4-124">curl“对象已移动”错误</span><span class="sxs-lookup"><span data-stu-id="c7ff4-124">curl "Object Moved" error</span></span>

<span data-ttu-id="c7ff4-125">如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：</span><span class="sxs-lookup"><span data-stu-id="c7ff4-125">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="c7ff4-126">找不到 `az` 命令</span><span class="sxs-lookup"><span data-stu-id="c7ff4-126">`az` command not found</span></span>

<span data-ttu-id="c7ff4-127">如果在安装后以及在使用 `bash` 或 `zsh` 时无法运行该命令，请清除 shell 的命令哈希缓存。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-127">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="c7ff4-128">运行</span><span class="sxs-lookup"><span data-stu-id="c7ff4-128">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="c7ff4-129">并查看问题是否得到解决。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-129">and check if the problem is resolved.</span></span>

<span data-ttu-id="c7ff4-130">如果在安装后没有重启 shell，也可能出现此错误。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-130">The issue can also occur if you didn't restart your shell after installation.</span></span> <span data-ttu-id="c7ff4-131">确保 `az` 命令的位置在 `$PATH` 中。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-131">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="c7ff4-132">`az` 命令的位置为</span><span class="sxs-lookup"><span data-stu-id="c7ff4-132">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

## <a name="uninstall"></a><span data-ttu-id="c7ff4-133">卸载</span><span class="sxs-lookup"><span data-stu-id="c7ff4-133">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="c7ff4-134">可以通过直接从安装时所选的位置删除文件来卸载 CLI。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-134">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="c7ff4-135">默认安装位置是 `$HOME`。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-135">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="c7ff4-136">删除安装的 CLI 文件。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-136">Remove the installed CLI files.</span></span>

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```

2. <span data-ttu-id="c7ff4-137">修改 `$HOME/.bash_profile` 文件，删除以下行：</span><span class="sxs-lookup"><span data-stu-id="c7ff4-137">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>

  ```text
  <install location>/lib/azure-cli/az.completion
  ```

3. <span data-ttu-id="c7ff4-138">如果使用 `bash` 或 `zsh`，请重新加载 shell 的命令缓存。</span><span class="sxs-lookup"><span data-stu-id="c7ff4-138">If using `bash` or `zsh`, reload your shell's command cache.</span></span>

  ```bash
  hash -r
  ```
