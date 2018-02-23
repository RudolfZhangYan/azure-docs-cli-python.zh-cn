---
title: "使用 yum 在 Linux 上安装 Azure CLI 2.0"
description: "如何使用 yum 安装 Azure CLI 2.0"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 5b7afe999d1afe5be40c4957d9cd0f832b680099
ms.sourcegitcommit: f82774a6f92598c41da9956284f563757f402774
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/19/2018
---
# <a name="install-azure-cli-20-with-yum"></a>使用 yum 安装 Azure CLI 2.0

如果运行附带 `yum` 的发行版（例如 RHEL、Fedora 或 CentOS），则可以安装适用于 Azure CLI 的包。 此包已在 RHEL 7、Fedora 19 和更高版本以及 CentOS 7 中测试。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>安装

1. 导入 Microsoft 存储库密钥。

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. 创建本地 `azure-cli` 存储库信息。

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. 使用 `yum install` 命令安装。 

   ```bash
   sudo yum install azure-cli
   ```

使用 `az` 命令运行 Azure CLI。

## <a name="update"></a>更新

使用 `yum update` 命令更新 Azure CLI。

```bash
sudo yum update azure-cli
```

## <a name="uninstall"></a>卸载

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. 从系统中删除包。

   ```bash
   sudo yum remove azure-cli
   ```

2. 如果不打算重新安装 CLI，请删除存储库信息。

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. 如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  sudo rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```
