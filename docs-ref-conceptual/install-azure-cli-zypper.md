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

可以使用 `az` 命令来运行 CLI。

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

