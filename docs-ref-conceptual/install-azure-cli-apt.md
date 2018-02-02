---
title: "使用 apt 在 Linux 上安装 Azure CLI 2.0"
description: "如何使用 apt 包管理器安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure apt, azure debian, azure ubuntu"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: fdd9f0061d5d38ed5a349b11eb0f5f27786bc1ab
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="install-azure-cli-20-with-apt"></a>使用 apt 安装 Azure CLI 2.0

如果运行附带 `apt` 的发行版（例如 Ubuntu 或 Debian），则可以安装适用于 Azure CLI 的包。 此包已在 Ubuntu Wheezy 和 Ubuntu Xenial 中测试。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

## <a name="install"></a>安装

1. 修改源列表：

   - 32 位系统

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64 位系统

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. 运行以下 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

可以使用 `az` 命令来运行 Azure CLI。

## <a name="troubleshooting"></a>故障排除

下面是使用 `apt` 安装时出现的一些常见问题。 如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。

### <a name="apt-key-fails-with-no-dirmngr"></a>apt-key 失败，出现“没有 dirmngr”

运行 `apt-key` 命令时，可能会看到类似于以下错误的输出：

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

错误的原因是缺少 `apt-key` 所需的组件。 可以通过安装 `dirmngr` 包解决此错误。

```bash
sudo apt-get install dirmngr
```

## <a name="update"></a>更新

使用 `apt-get upgrade` 更新 CLI 包。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> 此命令将会升级系统上所有未发生依赖关系更改的已安装包。
> 若只要升级 CLI，请使用 `apt-get install`。
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a>卸载

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. 使用 `apt-get remove` 进行卸载。

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. 如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. 请删除任何不需要的包。

   ```bash
   sudo apt autoremove
   ```
