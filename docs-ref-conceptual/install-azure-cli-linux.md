---
title: 手动安装适用于 Linux 的 Azure CLI 2.0
description: 如何在 Linux 上手动安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: f62d041d17433b845a89dfa009a74b3d8cf6b3be
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="install-azure-cli-20-on-linux-manually"></a>在 Linux 上手动安装 Azure CLI 2.0

如果发行版中没有提供 Azure CLI 包，始终可以通过运行安装脚本来手动安装 CLI。

> [!NOTE]
> 我们强烈建议使用 CLI 的包管理器。 使用包管理器可确保始终获得最新更新，并保证 CLI 组件的稳定性。 在手动安装之前，请检查发行版是否有对应的包。

## <a name="prerequisites"></a>先决条件

若要安装 CLI，需确保系统中存在下述软件：

* [Python 2.7 或 Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL 1.0.2](https://www.openssl.org/source/)

## <a name="install-or-update"></a>安装或更新

不管是安装还是更新 CLI，都需要执行完整安装。 具备先决条件以后，即可通过运行 `curl` 来安装 CLI。

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

也可以下载并在本地运行脚本。 可能需要重启 shell 才能使更改生效。 

然后即可使用 `az` 命令来运行 Azure CLI。 若要登录，请运行 `az login` 命令。

```azurecli
az login
```

若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

## <a name="troubleshooting"></a>故障排除

下面是手动安装过程中可能出现的一些常见问题。 如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。
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

  ```
  <install location>/lib/azure-cli/az.completion
  ```

3. 如果使用 `bash` 或 `zsh`，请重新加载 shell 的命令缓存。

  ```bash
  hash -r
  ```
