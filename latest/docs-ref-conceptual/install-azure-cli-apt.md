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
ms.openlocfilehash: 93d947d91973def1c05e2f5b2e7511bc1c5704a2
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="748a9-104">使用 apt 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="748a9-104">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="748a9-105">如果运行的是附带 `apt` 的版本（例如 Ubuntu 或 Debian），则可在系统上安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="748a9-105">If you are running a distirbution that comes with `apt`, such as Ubuntu or Debian, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="748a9-106">必须有 Python 2.7.x 或 Python 3.x 才能使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="748a9-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="748a9-107">如果分发版没有其中任何一个版本的包，请[安装 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="748a9-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="748a9-108">安装</span><span class="sxs-lookup"><span data-stu-id="748a9-108">Install</span></span>

1. <span data-ttu-id="748a9-109">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="748a9-109">Modify your sources list:</span></span>
 
   - <span data-ttu-id="748a9-110">32 位系统</span><span class="sxs-lookup"><span data-stu-id="748a9-110">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="748a9-111">64 位系统</span><span class="sxs-lookup"><span data-stu-id="748a9-111">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="748a9-112">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="748a9-112">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="748a9-113">可以使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="748a9-113">You can run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="748a9-114">更新</span><span class="sxs-lookup"><span data-stu-id="748a9-114">Update</span></span>

<span data-ttu-id="748a9-115">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="748a9-115">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="748a9-116">这会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="748a9-116">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="748a9-117">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="748a9-117">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="uninstall"></a><span data-ttu-id="748a9-118">卸载</span><span class="sxs-lookup"><span data-stu-id="748a9-118">Uninstall</span></span>

<span data-ttu-id="748a9-119">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="748a9-119">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="748a9-120">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="748a9-120">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="748a9-121">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="748a9-121">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="748a9-122">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="748a9-122">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="748a9-123">使用 `apt-get remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="748a9-123">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="748a9-124">如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="748a9-124">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="748a9-125">请删除任何不需要的包。</span><span class="sxs-lookup"><span data-stu-id="748a9-125">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
