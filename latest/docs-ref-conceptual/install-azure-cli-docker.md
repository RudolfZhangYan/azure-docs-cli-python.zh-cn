---
title: "使用 Docker 安装 Azure CLI"
description: "如何使用 Azure CLI 2.0 安装 Docker 容器"
keywords: "Azure CLI, 安装 Azure CLI, azure docker, azure docker 映像,"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 10/30/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ROBOTS: NOINDEX,NOFOLLOW
ms.openlocfilehash: 76ecf2c9cd0e6e694a31ac160112d1348863f118
ms.sourcegitcommit: 905939cc44764b4d1cc79a9b36c0793f7055a686
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/20/2017
---
# <a name="install-azure-cli-20-with-docker"></a>使用 Docker 安装 Azure CLI 2.0

可以使用 Docker 安装已预安装 Azure CLI 2.0 的独立 Linux 容器。 这样可以通过一个环境来快速启动，在环境中尝试 CLI 以确定其是否适合自己；也可以将此用作基础映像。

## <a name="install-with-docker"></a>使用 Docker 安装

请使用 `docker run` 安装 CLI。

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。

CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。

> [!NOTE]
> 如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

### <a name="update-with-docker"></a>使用 Docker 更新

使用 Docker 进行更新需要拉取新映像和重新创建任何现有的容器。 因此应进行尝试，避免使用将 CLI 作为数据存储来托管的容器。

1. 使用 `docker pull` 更新本地映像。

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. 获取当前正在使用 CLI 映像的容器。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

  > [!NOTE]
  > 如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。

3. 停止并重新创建容器。

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="uninstall-with-docker"></a>使用 Docker 卸载

如果你决定卸载 Azure CLI，我们会很遗憾。 在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。 我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。 也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。

若要正确卸载 CLI Docker 映像，需删除运行该映像的所有容器，然后删除本地映像。

1. 获取运行 azure-cli 映像的容器。

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```
  > [!NOTE]
  > 如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。

2. 删除所有包含 CLI 映像的容器。

   ```bash
   docker rm 34a868beb2ab
   ```

3. 删除本地安装的 CLI 映像。

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

