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
ms.openlocfilehash: 3a1e82dc666cd034d0cc4320a8b99dd6a9a14b6d
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="install-azure-cli-20-with-zypper"></a>使用 zypper 安装 Azure CLI 2.0

如果运行附带 `zypper` 的发行版（例如 openSUSE 或 SLES），则可以安装适用于 Azure CLI 的包。 此包已在 openSUSE 42.2 和 SLES 12 SP 2 中测试。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>安装

1. 安装 `curl`：

   ```bash
   sudo zypper refresh
   sudo zypper install -y curl
   ```

2. 导入 Microsoft 存储库密钥：

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. 创建本地 `azure-cli` 存储库信息：

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

4. 更新 `zypper` 包索引并安装：

   ```bash
   sudo zypper refresh
   sudo zypper install -y azure-cli
   ```

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请运行 `az login` 命令。

```azurecli
az login
```

若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

## <a name="update"></a>更新

可以使用 `zypper update` 命令来更新包。

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

## <a name="uninstall"></a>卸载

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. 从系统中删除包。

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. 如果不打算重新安装 CLI，请删除存储库信息。

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. 如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

