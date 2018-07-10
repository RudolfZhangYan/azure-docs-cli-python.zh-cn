---
title: 使用 zypper 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 zypper 安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 3a63c491b883c5a28e7309145e7a5eeb41e36b46
ms.sourcegitcommit: 308f9eb433a05b814999ac404f63d181169fffeb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2018
ms.locfileid: "37439918"
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="15b83-103">使用 zypper 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="15b83-103">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="15b83-104">如果运行附带 `zypper` 的发行版（例如 openSUSE 或 SLES），则可以安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="15b83-104">If you are running a distribution that comes with `zypper`, such as openSUSE or SLES, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="15b83-105">此包已在 openSUSE 42.2 和 SLES 12 SP 2 中测试。</span><span class="sxs-lookup"><span data-stu-id="15b83-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="15b83-106">安装</span><span class="sxs-lookup"><span data-stu-id="15b83-106">Install</span></span>

1. <span data-ttu-id="15b83-107">安装 `curl`：</span><span class="sxs-lookup"><span data-stu-id="15b83-107">Install `curl`:</span></span>

   ```bash
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="15b83-108">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="15b83-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="15b83-109">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="15b83-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. <span data-ttu-id="15b83-110">更新 `zypper` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="15b83-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

<span data-ttu-id="15b83-111">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="15b83-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="15b83-112">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="15b83-112">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="15b83-113">若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="15b83-113">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="15b83-114">更新</span><span class="sxs-lookup"><span data-stu-id="15b83-114">Update</span></span>

<span data-ttu-id="15b83-115">可以使用 `zypper update` 命令来更新包。</span><span class="sxs-lookup"><span data-stu-id="15b83-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="15b83-116">卸载</span><span class="sxs-lookup"><span data-stu-id="15b83-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="15b83-117">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="15b83-117">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="15b83-118">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="15b83-118">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo zypper removerepo azure-cli
  ```

3. <span data-ttu-id="15b83-119">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="15b83-119">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

