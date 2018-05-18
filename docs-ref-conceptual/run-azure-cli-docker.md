---
title: 在 Docker 容器中运行 Azure CLI 2.0
description: 如何运行托管 Azure CLI 2.0 的 Docker 容器
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: d88dbcec947372aa154bce939edd99f65cd9480f
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="run-azure-cli-20-in-a-docker-container"></a>在 Docker 容器中运行 Azure CLI 2.0

可以使用 Docker 运行已预装 Azure CLI 2.0 的独立 Linux 容器。 借助 Docker 可以从某个环境快速上手，在其中试用 CLI 以确定它是否适合自己；或者将我们的映像用作部署的基础。

## <a name="run-in-a-docker-container"></a>在 Docker 容器中运行

请使用 `docker run` 安装 CLI。

   ```bash
   docker run -it microsoft/azure-cli
   ```

CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。 若要登录，请运行 `az login` 命令。

```azurecli
az login
```

若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。

> [!NOTE]
> 如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli
> ```

## <a name="update-docker-image"></a>更新 Docker 映像

使用 Docker 进行更新需要拉取新映像和重新创建任何现有的容器。 因此，应先行尝试，避免将托管 CLI 的容器用作数据存储。

使用 `docker pull` 更新本地映像。

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a>卸载 Docker 映像

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

停止运行 CLI 映像的任何容器后，请删除该映像。

```bash
docker rmi microsoft/azure-cli
```
