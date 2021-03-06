---
title: 在 Docker 容器中运行 Azure CLI
description: 如何运行托管 Azure CLI 的 Docker 容器
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 01/29/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 40e6865ce07b6ccb8e84a2666f0bcd6df3b5cfcf
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47177753"
---
# <a name="run-azure-cli-in-a-docker-container"></a>在 Docker 容器中运行 Azure CLI

可以使用 Docker 运行已预装 Azure CLI 的独立 Linux 容器。 Docker 可让你快速开始创建一个用于运行 CLI 的隔离环境。 映像也可以用作你自己的部署的基础。

## <a name="run-in-a-docker-container"></a>在 Docker 容器中运行

请使用 `docker run` 安装 CLI。

   ```bash
   docker run -it microsoft/azure-cli
   ```

> [!NOTE]
> 若要从用户环境中选取 SSH 密钥，请使用 `-v ${HOME}/.ssh:/root/.ssh` 在环境中装载 SSH 密钥。
>
> ```bash
> docker run -it -v ${HOME}/.ssh:/root/.ssh microsoft/azure-cli
> ```

CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。 若要登录，请运行 [az login](/cli/azure/reference-index#az-login) 命令。

[!INCLUDE [interactive-login](includes/interactive-login.md)]

若要详细了解不同的身份验证方法，请参阅[使用 Azure CLI 登录](authenticate-azure-cli.md)。

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

## <a name="next-steps"></a>后续步骤

现在你已准备好使用 Azure CLI，下面简要介绍其功能和常用命令。

> [!div class="nextstepaction"]
> [Azure CLI 入门](get-started-with-azure-cli.md)
