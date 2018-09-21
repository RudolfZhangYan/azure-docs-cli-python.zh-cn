---
title: 使用 yum 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 yum 安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: e76572900113d13feaeaf050a9e7e3cc142cbf72
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388263"
---
# <a name="install-azure-cli-20-with-yum"></a>使用 yum 安装 Azure CLI 2.0

对于附带 `yum` 的 Linux 分发版（例如 RHEL、Fedora 或 CentOS），可以安装适用于 Azure CLI 的包。 此包已在 RHEL 7、Fedora 19 和更高版本以及 CentOS 7 中测试。

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

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

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
