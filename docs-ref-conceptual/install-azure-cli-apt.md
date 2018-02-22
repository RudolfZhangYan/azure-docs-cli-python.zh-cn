---
title: "使用 apt 在 Linux 上安装 Azure CLI 2.0"
description: "如何使用 apt 包管理器安装 Azure CLI 2.0"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/06/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 4076fefb902a324f77f97bc042b9f5ba3e787734
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="9f330-103">使用 apt 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="9f330-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="9f330-104">如果运行附带 `apt` 的发行版（例如 Ubuntu 或 Debian），则可以安装适用于 Azure CLI 的 64 位包。</span><span class="sxs-lookup"><span data-stu-id="9f330-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="9f330-105">此包已在以下项中测试：</span><span class="sxs-lookup"><span data-stu-id="9f330-105">This package has been tested with:</span></span>

* <span data-ttu-id="9f330-106">Ubuntu wheezy、xenial 和 artful</span><span class="sxs-lookup"><span data-stu-id="9f330-106">Ubuntu wheezy, xenial, and artful</span></span>
* <span data-ttu-id="9f330-107">Debian wheezy、jessie 和 stretch</span><span class="sxs-lookup"><span data-stu-id="9f330-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="9f330-108">安装</span><span class="sxs-lookup"><span data-stu-id="9f330-108">Install</span></span>

1. <span data-ttu-id="9f330-109">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="9f330-109">Modify your sources list:</span></span>

     ```bash
     AZ_REPO=$(lsb_release -cs)
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="9f330-110">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="9f330-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="9f330-111">可以使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="9f330-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="9f330-112">故障排除</span><span class="sxs-lookup"><span data-stu-id="9f330-112">Troubleshooting</span></span>

<span data-ttu-id="9f330-113">下面是使用 `apt` 安装时出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="9f330-113">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="9f330-114">如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="9f330-114">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="9f330-115">apt-key 失败，出现“没有 dirmngr”</span><span class="sxs-lookup"><span data-stu-id="9f330-115">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="9f330-116">运行 `apt-key` 命令时，可能会看到类似于以下错误的输出：</span><span class="sxs-lookup"><span data-stu-id="9f330-116">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="9f330-117">错误的原因是缺少 `apt-key` 所需的组件。</span><span class="sxs-lookup"><span data-stu-id="9f330-117">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="9f330-118">可以通过安装 `dirmngr` 包解决此错误。</span><span class="sxs-lookup"><span data-stu-id="9f330-118">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="9f330-119">更新</span><span class="sxs-lookup"><span data-stu-id="9f330-119">Update</span></span>

<span data-ttu-id="9f330-120">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="9f330-120">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="9f330-121">此命令将会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="9f330-121">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="9f330-122">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="9f330-122">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="9f330-123">卸载</span><span class="sxs-lookup"><span data-stu-id="9f330-123">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="9f330-124">使用 `apt-get remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="9f330-124">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="9f330-125">如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="9f330-125">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="9f330-126">请删除任何不需要的包。</span><span class="sxs-lookup"><span data-stu-id="9f330-126">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
