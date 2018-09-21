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
ms.openlocfilehash: be0b21cf0dab0f884b7f2984f2c35314ac157c61
ms.sourcegitcommit: d93b0a2bcfb0d164ef90d6d4618f0552609a8ea6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2018
ms.locfileid: "46469940"
---
# <a name="install-azure-cli-20-on-linux-manually"></a><span data-ttu-id="8226e-103">在 Linux 上手动安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="8226e-103">Install Azure CLI 2.0 on Linux manually</span></span>

<span data-ttu-id="8226e-104">如果没有适用于你的分发版的 Azure CLI 包，请运行一个脚本来手动安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="8226e-104">If there's no package for the Azure CLI for you your distribution, install the CLI manually by running a script.</span></span>

> [!NOTE]
> <span data-ttu-id="8226e-105">强烈建议使用包管理器安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="8226e-105">It's strongly recommend to install the CLI with a package manager.</span></span> <span data-ttu-id="8226e-106">使用包管理器可确保始终获得最新更新，并保证 CLI 组件的稳定性。</span><span class="sxs-lookup"><span data-stu-id="8226e-106">A package manager makes sure you always get the latest updates, and guarantees the stability of CLI components.</span></span> <span data-ttu-id="8226e-107">在手动安装之前，请检查发行版是否有对应的包。</span><span class="sxs-lookup"><span data-stu-id="8226e-107">Check and see if there is a package for your distribution before installing manually.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="8226e-108">先决条件</span><span class="sxs-lookup"><span data-stu-id="8226e-108">Prerequisites</span></span>

<span data-ttu-id="8226e-109">CLI 需要以下软件：</span><span class="sxs-lookup"><span data-stu-id="8226e-109">The CLI requires the following software:</span></span>

* [<span data-ttu-id="8226e-110">Python 2.7 或 Python 3.x</span><span class="sxs-lookup"><span data-stu-id="8226e-110">Python 2.7 or Python 3.x</span></span>](https://www.python.org/downloads/)
* [<span data-ttu-id="8226e-111">libffi</span><span class="sxs-lookup"><span data-stu-id="8226e-111">libffi</span></span>](https://sourceware.org/libffi/)
* [<span data-ttu-id="8226e-112">OpenSSL 1.0.2</span><span class="sxs-lookup"><span data-stu-id="8226e-112">OpenSSL 1.0.2</span></span>](https://www.openssl.org/source/)

## <a name="install-or-update"></a><span data-ttu-id="8226e-113">安装或更新</span><span class="sxs-lookup"><span data-stu-id="8226e-113">Install or update</span></span>

<span data-ttu-id="8226e-114">安装和更新 CLI 都需要重新运行安装脚本。</span><span class="sxs-lookup"><span data-stu-id="8226e-114">Both installing and updating the CLI requires re-running the install script.</span></span> <span data-ttu-id="8226e-115">运行 `curl` 来安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="8226e-115">Install the CLI by running `curl`.</span></span>

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

<span data-ttu-id="8226e-116">也可以下载并在本地运行该脚本。</span><span class="sxs-lookup"><span data-stu-id="8226e-116">The script can also be downloaded and run locally.</span></span> <span data-ttu-id="8226e-117">可能需要重启 shell 才能使更改生效。</span><span class="sxs-lookup"><span data-stu-id="8226e-117">You may have to restart your shell in order for changes to take effect.</span></span>

<span data-ttu-id="8226e-118">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="8226e-118">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="8226e-119">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="8226e-119">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="8226e-120">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="8226e-120">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="8226e-121">故障排除</span><span class="sxs-lookup"><span data-stu-id="8226e-121">Troubleshooting</span></span>

<span data-ttu-id="8226e-122">下面是手动安装过程中可能出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="8226e-122">Here are some common problems seen during a manual installation.</span></span> <span data-ttu-id="8226e-123">如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="8226e-123">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="8226e-124">curl“对象已移动”错误</span><span class="sxs-lookup"><span data-stu-id="8226e-124">curl "Object Moved" error</span></span>

<span data-ttu-id="8226e-125">如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：</span><span class="sxs-lookup"><span data-stu-id="8226e-125">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="8226e-126">找不到 `az` 命令</span><span class="sxs-lookup"><span data-stu-id="8226e-126">`az` command not found</span></span>

<span data-ttu-id="8226e-127">如果在安装后以及在使用 `bash` 或 `zsh` 时无法运行该命令，请清除 shell 的命令哈希缓存。</span><span class="sxs-lookup"><span data-stu-id="8226e-127">If you can't run the command after installation and using `bash` or `zsh`, clear your shell's command hash cache.</span></span> <span data-ttu-id="8226e-128">运行</span><span class="sxs-lookup"><span data-stu-id="8226e-128">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="8226e-129">并查看问题是否得到解决。</span><span class="sxs-lookup"><span data-stu-id="8226e-129">and check if the problem is resolved.</span></span>

<span data-ttu-id="8226e-130">如果在安装后没有重启 shell，也可能出现此错误。</span><span class="sxs-lookup"><span data-stu-id="8226e-130">The issue can also occur if you didn't restart your shell after installation.</span></span> <span data-ttu-id="8226e-131">确保 `az` 命令的位置在 `$PATH` 中。</span><span class="sxs-lookup"><span data-stu-id="8226e-131">Make sure that the location of the `az` command is in your `$PATH`.</span></span> <span data-ttu-id="8226e-132">`az` 命令的位置为</span><span class="sxs-lookup"><span data-stu-id="8226e-132">The location of the `az` command is</span></span>

```bash
<install path>/bin
```

## <a name="uninstall"></a><span data-ttu-id="8226e-133">卸载</span><span class="sxs-lookup"><span data-stu-id="8226e-133">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="8226e-134">可以通过直接从安装时所选的位置删除文件来卸载 CLI。</span><span class="sxs-lookup"><span data-stu-id="8226e-134">Uninstall the CLI by directly deleting the files from the location chosen at the time of installation.</span></span> <span data-ttu-id="8226e-135">默认安装位置是 `$HOME`。</span><span class="sxs-lookup"><span data-stu-id="8226e-135">The default install location is `$HOME`.</span></span>

1. <span data-ttu-id="8226e-136">删除安装的 CLI 文件。</span><span class="sxs-lookup"><span data-stu-id="8226e-136">Remove the installed CLI files.</span></span>

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```

2. <span data-ttu-id="8226e-137">修改 `$HOME/.bash_profile` 文件，删除以下行：</span><span class="sxs-lookup"><span data-stu-id="8226e-137">Modify your `$HOME/.bash_profile` file to remove the following line:</span></span>

  ```text
  <install location>/lib/azure-cli/az.completion
  ```

3. <span data-ttu-id="8226e-138">如果使用 `bash` 或 `zsh`，请重新加载 shell 的命令缓存。</span><span class="sxs-lookup"><span data-stu-id="8226e-138">If using `bash` or `zsh`, reload your shell's command cache.</span></span>

  ```bash
  hash -r
  ```

## <a name="next-steps"></a><span data-ttu-id="8226e-139">后续步骤</span><span class="sxs-lookup"><span data-stu-id="8226e-139">Next Steps</span></span>

<span data-ttu-id="8226e-140">现在你已经安装了 Azure CLI，下面简要介绍其功能和常用命令。</span><span class="sxs-lookup"><span data-stu-id="8226e-140">Now that you've installed the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="8226e-141">Azure CLI 入门</span><span class="sxs-lookup"><span data-stu-id="8226e-141">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
