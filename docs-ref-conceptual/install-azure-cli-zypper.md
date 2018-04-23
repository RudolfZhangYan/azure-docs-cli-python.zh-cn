---
title: 使用 zypper 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 zypper 安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 01d293eff229ab8b0eb3a3ff4e23978ea9e00174
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2018
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="dc330-103">使用 zypper 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="dc330-103">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="dc330-104">如果运行附带 `zypper` 的发行版（例如 openSUSE 或 SLES），则可以安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="dc330-104">If you are running a distribution that comes with `zypper`, such as openSUSE or SLES, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="dc330-105">此包已在 openSUSE 42.2 和 SLES 12 SP 2 中测试。</span><span class="sxs-lookup"><span data-stu-id="dc330-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="dc330-106">安装</span><span class="sxs-lookup"><span data-stu-id="dc330-106">Install</span></span>

1. <span data-ttu-id="dc330-107">安装 `curl`：</span><span class="sxs-lookup"><span data-stu-id="dc330-107">Install `curl`:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="dc330-108">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="dc330-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="dc330-109">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="dc330-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. <span data-ttu-id="dc330-110">更新 `zypper` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="dc330-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

<span data-ttu-id="dc330-111">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="dc330-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="dc330-112">若要登录，请运行 `az login` 命令。</span><span class="sxs-lookup"><span data-stu-id="dc330-112">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="dc330-113">若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="dc330-113">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="dc330-114">更新</span><span class="sxs-lookup"><span data-stu-id="dc330-114">Update</span></span>

<span data-ttu-id="dc330-115">可以使用 `zypper update` 命令来更新包。</span><span class="sxs-lookup"><span data-stu-id="dc330-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="dc330-116">卸载</span><span class="sxs-lookup"><span data-stu-id="dc330-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="dc330-117">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="dc330-117">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="dc330-118">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="dc330-118">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. <span data-ttu-id="dc330-119">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="dc330-119">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

