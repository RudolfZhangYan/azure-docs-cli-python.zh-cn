---
title: "使用 zypper 安装 Azure CLI 2.0"
description: "如何使用 zypper 安装 Azure CLI 2.0"
keywords: "azure cli, azure cli 安装, azure cli zypper, azure cli opensuse, azure cli sle"
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
ms.openlocfilehash: c01679ccb77880f1f628f4e48683d8ff030a568b
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="b6843-104">使用 zypper 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="b6843-104">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="b6843-105">如果运行的是附带 `zypper` 的版本（例如 OpenSUSE 或 SLE），则可在系统上安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="b6843-105">If you are running a distirbution that comes with `zypper`, such as OpenSUSE or SLE, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="b6843-106">必须有 Python 2.7.x 或 Python 3.x 才能使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="b6843-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="b6843-107">如果分发版没有其中任何一个版本的包，请[安装 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="b6843-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="b6843-108">安装</span><span class="sxs-lookup"><span data-stu-id="b6843-108">Install</span></span> 

1. <span data-ttu-id="b6843-109">安装 `curl`：</span><span class="sxs-lookup"><span data-stu-id="b6843-109">Install `curl`:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="b6843-110">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="b6843-110">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="b6843-111">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="b6843-111">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. <span data-ttu-id="b6843-112">更新 `zypper` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="b6843-112">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

<span data-ttu-id="b6843-113">可以使用 `az` 命令来运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="b6843-113">You can run the CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="b6843-114">更新</span><span class="sxs-lookup"><span data-stu-id="b6843-114">Update</span></span>

<span data-ttu-id="b6843-115">可以使用 `zypper update` 命令来更新包。</span><span class="sxs-lookup"><span data-stu-id="b6843-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="b6843-116">卸载</span><span class="sxs-lookup"><span data-stu-id="b6843-116">Uninstall</span></span>

<span data-ttu-id="b6843-117">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="b6843-117">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="b6843-118">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="b6843-118">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="b6843-119">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="b6843-119">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="b6843-120">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="b6843-120">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="b6843-121">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="b6843-121">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="b6843-122">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="b6843-122">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="b6843-123">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="b6843-123">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

