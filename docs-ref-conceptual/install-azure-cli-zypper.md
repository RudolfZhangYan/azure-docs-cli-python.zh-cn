---
title: 使用 zypper 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 zypper 安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: ed92443b6de4e538eaf5da41376e836aa2c771a0
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388297"
---
# <a name="install-azure-cli-20-with-zypper"></a><span data-ttu-id="beaa0-103">使用 zypper 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="beaa0-103">Install Azure CLI 2.0 with zypper</span></span>

<span data-ttu-id="beaa0-104">对于附带 `zypper` 的 Linux 分发版（例如 openSUSE 或 SLES），可以安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="beaa0-104">For Linux distributions with `zypper`, such as openSUSE or SLES, there's a package available for the Azure CLI.</span></span> <span data-ttu-id="beaa0-105">此包已在 openSUSE 42.2 和 SLES 12 SP 2 中测试。</span><span class="sxs-lookup"><span data-stu-id="beaa0-105">This package has been tested with openSUSE 42.2 and SLES 12 SP 2.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="beaa0-106">安装</span><span class="sxs-lookup"><span data-stu-id="beaa0-106">Install</span></span>

1. <span data-ttu-id="beaa0-107">安装 `curl`：</span><span class="sxs-lookup"><span data-stu-id="beaa0-107">Install `curl`:</span></span>

   ```bash
   sudo zypper install -y curl
   ```

2. <span data-ttu-id="beaa0-108">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="beaa0-108">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. <span data-ttu-id="beaa0-109">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="beaa0-109">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. <span data-ttu-id="beaa0-110">更新 `zypper` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="beaa0-110">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

<span data-ttu-id="beaa0-111">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="beaa0-111">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="beaa0-112">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="beaa0-112">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="beaa0-113">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="beaa0-113">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="beaa0-114">更新</span><span class="sxs-lookup"><span data-stu-id="beaa0-114">Update</span></span>

<span data-ttu-id="beaa0-115">可以使用 `zypper update` 命令来更新包。</span><span class="sxs-lookup"><span data-stu-id="beaa0-115">You can update the package with the `zypper update` command.</span></span>

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="beaa0-116">卸载</span><span class="sxs-lookup"><span data-stu-id="beaa0-116">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="beaa0-117">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="beaa0-117">Remove the package from your system.</span></span>

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. <span data-ttu-id="beaa0-118">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="beaa0-118">If you don't plan to reinstall the CLI, remove the repository information.</span></span>

  ```bash
  sudo zypper removerepo azure-cli
  ```

3. <span data-ttu-id="beaa0-119">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="beaa0-119">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```