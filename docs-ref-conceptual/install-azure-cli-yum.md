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
ms.openlocfilehash: f0d5effcd8315094b30050a35119e41eddf89961
ms.sourcegitcommit: 3eef136ae752eb90c67af604d4ddd298d70b1c9d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/06/2018
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="f4757-104">使用 yum 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="f4757-104">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="f4757-105">如果运行的是附带 `yum` 的版本（例如 RHEL、Fedora 或 CentOS），则可在系统上安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="f4757-105">If you are running a distirbution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is an available package for the Azure CLI that you can install on your system.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="f4757-106">安装</span><span class="sxs-lookup"><span data-stu-id="f4757-106">Install</span></span>

1. <span data-ttu-id="f4757-107">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="f4757-107">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="f4757-108">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="f4757-108">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="f4757-109">更新 `yum` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="f4757-109">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

<span data-ttu-id="f4757-110">使用 `az` 命令运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="f4757-110">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="f4757-111">更新</span><span class="sxs-lookup"><span data-stu-id="f4757-111">Update</span></span>

<span data-ttu-id="f4757-112">使用 `yum update` 命令更新 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="f4757-112">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="f4757-113">卸载</span><span class="sxs-lookup"><span data-stu-id="f4757-113">Uninstall</span></span>

<span data-ttu-id="f4757-114">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="f4757-114">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="f4757-115">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="f4757-115">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="f4757-116">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="f4757-116">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="f4757-117">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="f4757-117">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

1. <span data-ttu-id="f4757-118">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="f4757-118">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="f4757-119">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="f4757-119">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="f4757-120">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="f4757-120">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
