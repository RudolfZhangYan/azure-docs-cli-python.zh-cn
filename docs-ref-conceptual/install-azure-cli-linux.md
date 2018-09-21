---
title: 手动安装适用于 Linux 的 Azure CLI 2.0
description: 如何在 Linux 上手动安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/09/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: be0b21cf0dab0f884b7f2984f2c35314ac157c61
ms.sourcegitcommit: d93b0a2bcfb0d164ef90d6d4618f0552609a8ea6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/20/2018
ms.locfileid: "46469940"
---
# <a name="install-azure-cli-20-on-linux-manually"></a>在 Linux 上手动安装 Azure CLI 2.0

如果没有适用于你的分发版的 Azure CLI 包，请运行一个脚本来手动安装 CLI。

> [!NOTE]
> 强烈建议使用包管理器安装 CLI。 使用包管理器可确保始终获得最新更新，并保证 CLI 组件的稳定性。 在手动安装之前，请检查发行版是否有对应的包。

## <a name="prerequisites"></a>先决条件

CLI 需要以下软件：

* [Python 2.7 或 Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update"></a>安装或更新

安装和更新 CLI 都需要重新运行安装脚本。 运行 `curl` 来安装 CLI。

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

也可以下载并在本地运行该脚本。 可能需要重启 shell 才能使更改生效。

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

## <a name="troubleshooting"></a>故障排除

下面是手动安装过程中可能出现的一些常见问题。 如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。

### <a name="curl-object-moved-error"></a>curl“对象已移动”错误

如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>找不到 `az` 命令

如果在安装后以及在使用 `bash` 或 `zsh` 时无法运行该命令，请清除 shell 的命令哈希缓存。 运行

```bash
hash -r
```

并查看问题是否得到解决。

如果在安装后没有重启 shell，也可能出现此错误。 确保 `az` 命令的位置在 `$PATH` 中。 `az` 命令的位置为

```bash
<install path>/bin
```

## <a name="uninstall"></a>卸载

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

可以通过直接从安装时所选的位置删除文件来卸载 CLI。 默认安装位置是 `$HOME`。

1. 删除安装的 CLI 文件。

  ```bash
  rm -r <install location>/lib/azure-cli
  rm <install location>/bin/az
  ```

2. 修改 `$HOME/.bash_profile` 文件，删除以下行：

  ```text
  <install location>/lib/azure-cli/az.completion
  ```

3. 如果使用 `bash` 或 `zsh`，请重新加载 shell 的命令缓存。

  ```bash
  hash -r
  ```

## <a name="next-steps"></a>后续步骤

现在你已经安装了 Azure CLI，下面简要介绍其功能和常用命令。

> [!div class="nextstepaction"]
> [Azure CLI 入门](get-started-with-azure-cli.md)
