---
title: 使用 apt 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 apt 包管理器安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 13cc995e099cee47534a46097b2e1afd8e96e8b4
ms.sourcegitcommit: d93b0a2bcfb0d164ef90d6d4618f0552609a8ea6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2018
ms.locfileid: "46469974"
---
# <a name="install-azure-cli-20-with-apt"></a>使用 apt 安装 Azure CLI 2.0

如果运行附带 `apt` 的发行版（例如 Ubuntu 或 Debian），则可以安装适用于 Azure CLI 的 64 位包。 此包已在以下项中测试：

* Ubuntu trusty、xenial、artful 和 bionic
* Debian wheezy、jessie 和 stretch

## <a name="install"></a>安装

1. <div id="install-step-1"/>修改源列表：

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

2. <div id="signingKey"/>获取 Microsoft 签名密钥：

   ```bash
   curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
   ```

3. 安装 CLI：

   ```bash
   sudo apt-get update
   sudo apt-get install apt-transport-https azure-cli
   ```

   > [!WARNING]
   > 签名密钥已在 2018 年 5 月更新，并已被替换。 如果收到签名密钥错误，请确保已[获得最新的签名密钥](#signingKey)。

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

## <a name="troubleshooting"></a>故障排除

下面是使用 `apt` 安装时出现的一些常见问题。 如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。

### <a name="lsbrelease-fails-with-command-not-found"></a>lsb_release 失败，出现“找不到命令”错误

运行 `lsb_release` 命令时，可能会看到类似于以下错误的输出：

```output
-bash: lsb_release: command not found
```

发生该错误的原因是未安装 `lsb_release` 命令。 可以通过安装 `lsb-release` 包解决此错误。

```bash
sudo apt-get install lsb-release
```

### <a name="lsbrelease-does-not-return-the-base-distribution-version"></a>lsb_release 没有返回基础发行版本

某些 Ubuntu 或 Debian 派生的版本（例如 Linux Mint）不会通过 `lsb_release` 返回正确的版本名称。 此值在安装过程中用于确定要安装的包。 如果知道自己的发行版派生自的版本的名称，则可在[安装步骤 1](#install-step-1) 中手动设置 `AZ_REPO` 值。 否则，请查看发行版的信息，了解如何确定基础发行版名称，然后将 `AZ_REPO` 设置为正确值。

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

### <a name="apt-key-hangs"></a>apt-key 挂起

当位于一个防火墙后并且该防火墙阻止与端口 11371 的传出连接时，`apt-key` 命令可能会无限期挂起。 防火墙可能需要对传出连接使用 HTTP 代理：

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

若要确定是否有代理，请与系统管理员联系。 如果代理不需要登录，请省略用户、密码和 `@` 令牌。

## <a name="update"></a>更新

使用 `apt-get upgrade` 更新 CLI 包。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> 签名密钥已在 2018 年 5 月更新，并已被替换。 如果收到签名密钥错误，请确保已[获得最新的签名密钥](#signingKey)。
>
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

## <a name="next-steps"></a>后续步骤

现在你已经安装了 Azure CLI，下面简要介绍其功能和常用命令。

> [!div class="nextstepaction"]
> [Azure CLI 入门](get-started-with-azure-cli.md)