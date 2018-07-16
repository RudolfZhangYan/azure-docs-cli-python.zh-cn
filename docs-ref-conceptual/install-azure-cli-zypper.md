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
ms.openlocfilehash: a7329784f26edfaeebc3520b63d12faed11fe38f
ms.sourcegitcommit: 64f2c628e83d687d0e172c01f13d71c8c39a8040
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 07/11/2018
ms.locfileid: "38967531"
---
# <a name="install-azure-cli-20-with-zypper"></a>使用 zypper 安装 Azure CLI 2.0

如果运行附带 `zypper` 的发行版（例如 openSUSE 或 SLES），则可以安装适用于 Azure CLI 的包。 此包已在 openSUSE 42.2 和 SLES 12 SP 2 中测试。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>安装

1. 安装 `curl`：

   ```bash
   sudo zypper install -y curl
   ```

2. 导入 Microsoft 存储库密钥：

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

3. 创建本地 `azure-cli` 存储库信息：

   ```bash
   sudo zypper addrepo --name 'Azure CLI' --check https://packages.microsoft.com/yumrepos/azure-cli azure-cli
   ```

4. 更新 `zypper` 包索引并安装：

   ```bash
   sudo zypper install --from azure-cli -y azure-cli
   ```

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

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
  sudo zypper removerepo azure-cli
  ```

3. 如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```