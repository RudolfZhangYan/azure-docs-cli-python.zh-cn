---
title: "使用 zypper 在 Linux 上安装 Azure CLI 2.0"
description: "如何使用 zypper 安装 Azure CLI 2.0"
keywords: "azure cli, azure cli 安装, azure cli zypper, azure cli opensuse, azure cli sle"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: c0b566f96e47d34d20f7bf85db0fae32913ed596
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="39d97-104">使用 zypper 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="39d97-104">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="39d97-105">如果运行附带 `zypper` 的发行版（例如 openSUSE 或 SLES），则可以安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="39d97-105">If you are running a distribution that comes with `zypper`, such as openSUSE or SLES, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="39d97-106">此包已在 openSUSE 42.2 和 SLES 12 SP 2 中测试。</span><span class="sxs-lookup"><span data-stu-id="39d97-106">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="39d97-107">安装</span><span class="sxs-lookup"><span data-stu-id="39d97-107">Install</span></span>

1. <span data-ttu-id="39d97-108">安装 `curl`：</span><span class="sxs-lookup"><span data-stu-id="39d97-108">Install `curl`:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="39d97-109">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="39d97-109">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="39d97-110">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="39d97-110">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. <span data-ttu-id="39d97-111">更新 `zypper` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="39d97-111">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

<span data-ttu-id="39d97-112">可以使用 `az` 命令来运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="39d97-112">You can run the CLI with the `az` command.</span></span>

## <a name="update"></a><span data-ttu-id="39d97-113">更新</span><span class="sxs-lookup"><span data-stu-id="39d97-113">Update</span></span>

<span data-ttu-id="39d97-114">可以使用 `zypper update` 命令来更新包。</span><span class="sxs-lookup"><span data-stu-id="39d97-114">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="39d97-115">卸载</span><span class="sxs-lookup"><span data-stu-id="39d97-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="39d97-116">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="39d97-116">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="39d97-117">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="39d97-117">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="39d97-118">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="39d97-118">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

