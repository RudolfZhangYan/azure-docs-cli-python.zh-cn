---
title: "使用 yum 安装 Azure CLI 2.0"
description: "如何使用 yum 安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure yum, azure rhel, azure fedora, azure centos"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: f0d5effcd8315094b30050a35119e41eddf89961
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20-with-yum"></a>使用 yum 安装 Azure CLI 2.0

如果运行的是附带 `yum` 的版本（例如 RHEL、Fedora 或 CentOS），则可在系统上安装适用于 Azure CLI 的包。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>安装

1. 导入 Microsoft 存储库密钥：

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. 创建本地 `azure-cli` 存储库信息：

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. 更新 `yum` 包索引并安装：

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

使用 `az` 命令运行 Azure CLI。

## <a name="update"></a>更新

使用 `yum update` 命令更新 Azure CLI。

```bash
yum check-update
sudo yum update azure-cli
```

## <a name="uninstall"></a>卸载

如果你决定卸载 Azure CLI，我们会很遗憾。 在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。 我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。 也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。

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