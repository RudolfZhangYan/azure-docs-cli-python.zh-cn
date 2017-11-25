---
title: "手动安装适用于 Linux 的 Azure CLI 2.0"
description: "如何在 Linux 上手动安装 Azure CLI 2.0"
keywords: "Azure CLI, 安装 Azure CLI, azure linux, azure 安装 linux"
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
ms.openlocfilehash: f792d3fc84eedade52ddfb3f351e48689e474d53
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-on-linux-manually"></a>在 Linux 上手动安装 Azure CLI 2.0

如果发行版中没有提供 Azure CLI 包，则始终可以通过运行安装脚本来手动安装 CLI。 如果提供了包，建议始终使用包来进行安装。

## <a name="prerequisites"></a>先决条件

若要安装 CLI，需确保系统中存在下述软件：

* [Python 2.7 或 Python 3.x](https://www.python.org/downloads/)
* [libffi](https://sourceware.org/libffi/)
* [OpenSSL](https://www.openssl.org/source/)

## <a name="install-or-update-manually"></a>手动进行安装或更新

不管是安装还是更新 CLI，都需要执行完整的安装操作。 具备先决条件以后，即可通过运行 `curl` 来安装 CLI。

```bash
curl -L https://aka.ms/InstallAzureCli | bash
```

如果你愿意，或者如果系统中没有 `curl`，也可改为下载脚本并在本地运行。 可能需要重启 shell 才能使更改生效。 安装后，请使用 `az` 命令运行 CLI。

## <a name="troubleshooting"></a>故障排除

### <a name="curl-object-moved-error"></a>curl“对象已移动”错误

如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a>找不到 `az` 命令

如果在安装后无法运行该命令，则可能需要清除 shell 的命令哈希缓存。 运行

```bash
hash -r
```

并查看问题是否得以解决。 

如果在安装后没有重启 shell，也可能出现此问题。 确保 `az` 命令的位置在 `$PATH` 中。

如果运行过安装脚本，则该位置为：

```bash
<install path>/bin
```

## <a name="unstinall-manually"></a>手动卸载

如果你决定卸载 Azure CLI，我们会很遗憾。 在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。 我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。 也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。

可以通过直接从安装位置删除文件的方式卸载 CLI。 如果是通过 `https://aka.ms/InstallAzureCLI` 脚本进行的安装，则应已在安装时选定安装位置。 默认安装位置为 `$HOME`。

首先，删除安装的 CLI 文件：

```bash
rm -r <install location>/lib/azure-cli
rm <install location>/bin/az
```

然后修改 `$HOME/.bash_profile` 文件，删除以下行：

```
<install location>/lib/azure-cli/az.completion
```

最后，重载 shell 的命令缓存（如果已启用）。 `bash` 和 `zsh` 用户需执行以下步骤：

```bash
hash -r
```
