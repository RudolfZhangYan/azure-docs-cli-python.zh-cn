---
title: 使用 yum 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 yum 安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 7729077d9240f09e0ad93ad8ab154d1477d8c3fd
ms.sourcegitcommit: 308f9eb433a05b814999ac404f63d181169fffeb
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/03/2018
ms.locfileid: "37439884"
---
# <a name="install-azure-cli-20-with-yum"></a><span data-ttu-id="73ee2-103">使用 yum 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="73ee2-103">Install Azure CLI 2.0 with yum</span></span>

<span data-ttu-id="73ee2-104">如果运行附带 `yum` 的发行版（例如 RHEL、Fedora 或 CentOS），则可以安装适用于 Azure CLI 的包。</span><span class="sxs-lookup"><span data-stu-id="73ee2-104">If you are running a distribution that comes with `yum`, such as RHEL, Fedora, or CentOS, there is a package available for the Azure CLI.</span></span> <span data-ttu-id="73ee2-105">此包已在 RHEL 7、Fedora 19 和更高版本以及 CentOS 7 中测试。</span><span class="sxs-lookup"><span data-stu-id="73ee2-105">This package has been tested with RHEL 7, Fedora 19 and higher, and CentOS 7.</span></span>

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a><span data-ttu-id="73ee2-106">安装</span><span class="sxs-lookup"><span data-stu-id="73ee2-106">Install</span></span>

1. <span data-ttu-id="73ee2-107">导入 Microsoft 存储库密钥。</span><span class="sxs-lookup"><span data-stu-id="73ee2-107">Import the Microsoft repository key.</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="73ee2-108">创建本地 `azure-cli` 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="73ee2-108">Create local `azure-cli` repository information.</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="73ee2-109">使用 `yum install` 命令安装。</span><span class="sxs-lookup"><span data-stu-id="73ee2-109">Install with the `yum install` command.</span></span> 

   ```bash
   sudo yum install azure-cli
   ```

<span data-ttu-id="73ee2-110">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="73ee2-110">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="73ee2-111">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="73ee2-111">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="73ee2-112">若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="73ee2-112">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update"></a><span data-ttu-id="73ee2-113">更新</span><span class="sxs-lookup"><span data-stu-id="73ee2-113">Update</span></span>

<span data-ttu-id="73ee2-114">使用 `yum update` 命令更新 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="73ee2-114">Update the Azure CLI with the `yum update` command.</span></span>

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a><span data-ttu-id="73ee2-115">卸载</span><span class="sxs-lookup"><span data-stu-id="73ee2-115">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="73ee2-116">从系统中删除包。</span><span class="sxs-lookup"><span data-stu-id="73ee2-116">Remove the package from your system.</span></span>

   ```bash
   sudo yum remove azure-cli
   ```

2. <span data-ttu-id="73ee2-117">如果不打算重新安装 CLI，请删除存储库信息。</span><span class="sxs-lookup"><span data-stu-id="73ee2-117">If you do not plan to reinstall the CLI, remove the repository information.</span></span>

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. <span data-ttu-id="73ee2-118">如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。</span><span class="sxs-lookup"><span data-stu-id="73ee2-118">If you removed the repository information, also remove the Microsoft GPG signature key.</span></span>

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
