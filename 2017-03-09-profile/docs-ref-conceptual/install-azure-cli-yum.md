---
title: "使用 yum 安装 Azure CLI 2.0"
description: "如何使用 yum 安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure yum, azure rhel, azure fedora, azure centos"
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
ms.openlocfilehash: de695454c6f3109679b9eb9f6c0d77348d354518
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="15618-104">使用 yum 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="15618-104">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="15618-105">如果运行的是附带 `yum` 的版本（例如 RHEL、Fedora 或 CentOS），则可在系统上安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="15618-105">If you are running a distirbution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is an available package for the Azure CLI that you can install on your system.</span></span>

> [!NOTE]
> <span data-ttu-id="15618-106">必须有 Python 2.7.x 或 Python 3.x 才能使用 CLI。</span><span class="sxs-lookup"><span data-stu-id="15618-106">You must have Python 2.7.x or Python 3.x in order to use the CLI.</span></span> <span data-ttu-id="15618-107">如果分发版没有其中任何一个版本的包，请[安装 Python](https://www.python.org/downloads/)。</span><span class="sxs-lookup"><span data-stu-id="15618-107">If your distribution does not have a package for either, [install Python](https://www.python.org/downloads/).</span></span>

## <a name="install"></a><span data-ttu-id="15618-108">安装</span><span class="sxs-lookup"><span data-stu-id="15618-108">Install</span></span> 

1. <span data-ttu-id="15618-109">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="15618-109">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="15618-110">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="15618-110">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="15618-111">更新 `yum` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="15618-111">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

<span data-ttu-id="15618-112">使用 `az` 命令运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="15618-112">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="15618-113">更新</span><span class="sxs-lookup"><span data-stu-id="15618-113">Update</span></span>

<span data-ttu-id="15618-114">使用 `yum update` 命令更新 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="15618-114">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="15618-115">卸载</span><span class="sxs-lookup"><span data-stu-id="15618-115">Uninstall</span></span>

<span data-ttu-id="15618-116">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="15618-116">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="15618-117">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="15618-117">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="15618-118">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="15618-118">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="15618-119">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="15618-119">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="15618-120">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="15618-120">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="15618-121">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="15618-121">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="15618-122">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="15618-122">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
