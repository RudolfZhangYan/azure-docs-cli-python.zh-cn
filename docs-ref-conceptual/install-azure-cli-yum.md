---
title: "使用 yum 在 Linux 上安装 Azure CLI 2.0"
description: "如何使用 yum 安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure yum, azure rhel, azure fedora, azure centos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 9d11c3cf5d9e7ba58c3e2edd830e0d12669f5b91
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="6ac19-104">使用 yum 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="6ac19-104">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="6ac19-105">如果运行附带 `yum` 的发行版（例如 RHEL、Fedora 或 CentOS），则可以安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="6ac19-105">If you are running a distribution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="6ac19-106">此包已在 RHEL 7、Fedora 19 和更高版本以及 CentOS 7 中测试。</span><span class="sxs-lookup"><span data-stu-id="6ac19-106">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="6ac19-107">安装</span><span class="sxs-lookup"><span data-stu-id="6ac19-107">Install</span></span>

1. <span data-ttu-id="6ac19-108">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="6ac19-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="6ac19-109">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="6ac19-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="6ac19-110">更新 `yum` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="6ac19-110">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

<span data-ttu-id="6ac19-111">使用 `az` 命令运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="6ac19-111">Run the Azure CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="6ac19-112">更新</span><span class="sxs-lookup"><span data-stu-id="6ac19-112">Update</span></span>

<span data-ttu-id="6ac19-113">使用 `yum update` 命令更新 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="6ac19-113">Update the Azure CLI with the `yum update` command.</span></span>

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="6ac19-114">卸载</span><span class="sxs-lookup"><span data-stu-id="6ac19-114">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="6ac19-115">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="6ac19-115">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="6ac19-116">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="6ac19-116">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="6ac19-117">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="6ac19-117">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
