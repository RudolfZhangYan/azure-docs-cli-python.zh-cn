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
# <a name="run-azure-cli-in-a-docker-container"></a><span data-ttu-id="1d8b1-103">在 Docker 容器中运行 Azure CLI</span><span class="sxs-lookup"><span data-stu-id="1d8b1-103">Run Azure CLI in a Docker container</span></span>

<span data-ttu-id="1d8b1-104">可以使用 Docker 运行已预装 Azure CLI 的独立 Linux 容器。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-104">You can use Docker to run a standalone Linux container with the Azure CLI pre-installed.</span></span> <span data-ttu-id="1d8b1-105">Docker 可让你快速开始创建一个用于运行 CLI 的隔离环境。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-105">Docker gets you started quickly with an isolated environment to run the CLI in.</span></span> <span data-ttu-id="1d8b1-106">映像也可以用作你自己的部署的基础。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-106">The image can also be used as a base for your own deployments.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="1d8b1-107">在 Docker 容器中运行</span><span class="sxs-lookup"><span data-stu-id="1d8b1-107">Run in a Docker container</span></span>

<span data-ttu-id="1d8b1-108">请使用 `docker run` 安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-108">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="1d8b1-109">若要从用户环境中选取 SSH 密钥，请使用 `-v ${HOME}/.ssh:/root/.ssh` 在环境中装载 SSH 密钥。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-109">If you want to pick up the SSH keys from your user environment, use `-v ${HOME}/.ssh:/root/.ssh` to mount your SSH keys in the environment.</span></span>
>
> ```bash
> docker run -it -v ${HOME}/.ssh:/root/.ssh microsoft/azure-cli
> ```

<span data-ttu-id="1d8b1-110">CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-110">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span> <span data-ttu-id="1d8b1-111">若要登录，请运行 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-111">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="1d8b1-112">若要详细了解不同的身份验证方法，请参阅[使用 Azure CLI 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-112">To learn more about different authentication methods, see [Sign in with the Azure CLI](authenticate-azure-cli.md).</span></span>

## <a name="update-docker-image"></a><span data-ttu-id="1d8b1-113">更新 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="1d8b1-113">Update Docker image</span></span>

<span data-ttu-id="1d8b1-114">使用 Docker 进行更新需要拉取新映像和重新创建任何现有的容器。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-114">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="1d8b1-115">因此，应先行尝试，避免将托管 CLI 的容器用作数据存储。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-115">For this reason, you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="1d8b1-116">使用 `docker pull` 更新本地映像。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-116">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="1d8b1-117">卸载 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="1d8b1-117">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="1d8b1-118">停止运行 CLI 映像的任何容器后，请删除该映像。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-118">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```

## <a name="next-steps"></a><span data-ttu-id="1d8b1-119">后续步骤</span><span class="sxs-lookup"><span data-stu-id="1d8b1-119">Next Steps</span></span>

<span data-ttu-id="1d8b1-120">现在你已准备好使用 Azure CLI，下面简要介绍其功能和常用命令。</span><span class="sxs-lookup"><span data-stu-id="1d8b1-120">Now that you're ready to use the Azure CLI, take a short tour of its features and common commands.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="1d8b1-121">Azure CLI 入门</span><span class="sxs-lookup"><span data-stu-id="1d8b1-121">Get started with the Azure CLI</span></span>](get-started-with-azure-cli.md)
