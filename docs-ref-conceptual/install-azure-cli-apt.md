---
title: "使用 apt 安装 Azure CLI 2.0"
description: "如何使用 apt 包管理器安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure apt, azure debian, azure ubuntu"
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
ms.openlocfilehash: 65e8e78275b0f40a2298934fe8bc9368bbf796a7
ms.sourcegitcommit: 59f0b667f2202bae8914e6fc8dc5c9dc79fef91c
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/25/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="826f2-104">使用 apt 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="826f2-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="826f2-105">如果运行的是附带 `apt` 的版本（例如 Ubuntu 或 Debian），则可在系统上安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="826f2-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="826f2-106">安装</span><span class="sxs-lookup"><span data-stu-id="826f2-106">Install</span></span>

1. <span data-ttu-id="826f2-107">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="826f2-107">Modify your sources list:</span></span>

   - <span data-ttu-id="826f2-108">32 位系统</span><span class="sxs-lookup"><span data-stu-id="826f2-108">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="826f2-109">64 位系统</span><span class="sxs-lookup"><span data-stu-id="826f2-109">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="826f2-110">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="826f2-110">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="826f2-111">可以使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="826f2-111">You can run the Azure CLI with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="826f2-112">故障排除</span><span class="sxs-lookup"><span data-stu-id="826f2-112">Troubleshooting</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="826f2-113">apt-key 失败，出现“没有 dirmngr”</span><span class="sxs-lookup"><span data-stu-id="826f2-113">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="826f2-114">运行 `apt-key` 命令时，可能会看到类似于以下错误的输出。</span><span class="sxs-lookup"><span data-stu-id="826f2-114">When running the `apt-key` command, you may see output similar to the following error.</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="826f2-115">这是因为缺少 `apt-key` 所需的组件。</span><span class="sxs-lookup"><span data-stu-id="826f2-115">This is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="826f2-116">可以通过安装 `dirmngr` 包解决此问题。</span><span class="sxs-lookup"><span data-stu-id="826f2-116">You can resolve this by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a><span data-ttu-id="826f2-117">更新</span><span class="sxs-lookup"><span data-stu-id="826f2-117">Update</span></span>

<span data-ttu-id="826f2-118">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="826f2-118">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="826f2-119">这会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="826f2-119">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="826f2-120">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="826f2-120">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="826f2-121">卸载</span><span class="sxs-lookup"><span data-stu-id="826f2-121">Uninstall</span></span>

<span data-ttu-id="826f2-122">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="826f2-122">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="826f2-123">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="826f2-123">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="826f2-124">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="826f2-124">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="826f2-125">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="826f2-125">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="826f2-126">使用 `apt-get remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="826f2-126">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="826f2-127">如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="826f2-127">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="826f2-128">请删除任何不需要的包。</span><span class="sxs-lookup"><span data-stu-id="826f2-128">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
