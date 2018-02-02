---
title: "在 Docker 容器中运行 Azure CLI 2.0"
description: "如何运行托管 Azure CLI 2.0 的 Docker 容器"
keywords: "Azure CLI, 安装 Azure CLI, azure docker, azure docker 映像,"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/29/18
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 819ff0cdb0df6057a5dff8f8ab015796f06c6a9b
ms.sourcegitcommit: 8606f36963e8daa6448d637393d1e4ef2c9859a0
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/01/2018
---
# <a name="run-azure-cli-20-in-a-docker-container"></a><span data-ttu-id="533e3-104">在 Docker 容器中运行 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="533e3-104">Run Azure CLI 2.0 in a Docker container</span></span>

<span data-ttu-id="533e3-105">可以使用 Docker 运行已预装 Azure CLI 2.0 的独立 Linux 容器。</span><span class="sxs-lookup"><span data-stu-id="533e3-105">You can use Docker to run a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="533e3-106">借助 Docker 可以从某个环境快速上手，在其中试用 CLI 以确定它是否适合自己；或者将我们的映像用作部署的基础。</span><span class="sxs-lookup"><span data-stu-id="533e3-106">Docker lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or use our image as a base for your own deployment.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="533e3-107">在 Docker 容器中运行</span><span class="sxs-lookup"><span data-stu-id="533e3-107">Run in a Docker container</span></span>

<span data-ttu-id="533e3-108">请使用 `docker run` 安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="533e3-108">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

<span data-ttu-id="533e3-109">CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。</span><span class="sxs-lookup"><span data-stu-id="533e3-109">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="533e3-110">如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。</span><span class="sxs-lookup"><span data-stu-id="533e3-110">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root microsoft/azure-cli
> ```

## <a name="update-docker-image"></a><span data-ttu-id="533e3-111">更新 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="533e3-111">Update Docker image</span></span>

<span data-ttu-id="533e3-112">使用 Docker 进行更新需要拉取新映像和重新创建任何现有的容器。</span><span class="sxs-lookup"><span data-stu-id="533e3-112">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="533e3-113">因此，应先行尝试，避免将托管 CLI 的容器用作数据存储。</span><span class="sxs-lookup"><span data-stu-id="533e3-113">For this reason you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="533e3-114">使用 `docker pull` 更新本地映像。</span><span class="sxs-lookup"><span data-stu-id="533e3-114">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="533e3-115">卸载 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="533e3-115">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="533e3-116">停止运行 CLI 映像的任何容器后，请删除该映像。</span><span class="sxs-lookup"><span data-stu-id="533e3-116">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```
