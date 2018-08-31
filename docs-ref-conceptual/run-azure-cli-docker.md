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
ms.openlocfilehash: 7a50682d549f6383e68128f2c2aef02dc2877a8e
ms.sourcegitcommit: 83826ca154c9f32c6091c63ce4b3e480694ba8d1
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/09/2018
ms.locfileid: "43144910"
---
# <a name="run-azure-cli-20-in-a-docker-container"></a><span data-ttu-id="f14c3-103">在 Docker 容器中运行 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="f14c3-103">Run Azure CLI 2.0 in a Docker container</span></span>

<span data-ttu-id="f14c3-104">可以使用 Docker 运行已预装 Azure CLI 2.0 的独立 Linux 容器。</span><span class="sxs-lookup"><span data-stu-id="f14c3-104">You can use Docker to run a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="f14c3-105">借助 Docker 可以从某个环境快速上手，在其中试用 CLI 以确定它是否适合自己；或者将我们的映像用作部署的基础。</span><span class="sxs-lookup"><span data-stu-id="f14c3-105">Docker lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or use our image as a base for your own deployment.</span></span>

## <a name="run-in-a-docker-container"></a><span data-ttu-id="f14c3-106">在 Docker 容器中运行</span><span class="sxs-lookup"><span data-stu-id="f14c3-106">Run in a Docker container</span></span>

<span data-ttu-id="f14c3-107">请使用 `docker run` 安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="f14c3-107">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it microsoft/azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="f14c3-108">若要从用户环境中选取 SSH 密钥，可以使用 `-v ${HOME}/.ssh:/root/.ssh` 在环境中装载 SSH 密钥。</span><span class="sxs-lookup"><span data-stu-id="f14c3-108">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}/.ssh:/root/.ssh` to mount your SSH keys in the environment.</span></span>
>
> ```bash
> docker run -it -v ${HOME}/.ssh:/root/.ssh microsoft/azure-cli
> ```

<span data-ttu-id="f14c3-109">CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。</span><span class="sxs-lookup"><span data-stu-id="f14c3-109">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span> <span data-ttu-id="f14c3-110">若要登录，请运行 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="f14c3-110">To sign in, run the [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="f14c3-111">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="f14c3-111">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="update-docker-image"></a><span data-ttu-id="f14c3-112">更新 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="f14c3-112">Update Docker image</span></span>

<span data-ttu-id="f14c3-113">使用 Docker 进行更新需要拉取新映像和重新创建任何现有的容器。</span><span class="sxs-lookup"><span data-stu-id="f14c3-113">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="f14c3-114">因此，应先行尝试，避免将托管 CLI 的容器用作数据存储。</span><span class="sxs-lookup"><span data-stu-id="f14c3-114">For this reason you should try to avoid using a container that hosts the CLI as a data store.</span></span>

<span data-ttu-id="f14c3-115">使用 `docker pull` 更新本地映像。</span><span class="sxs-lookup"><span data-stu-id="f14c3-115">Update your local image with `docker pull`.</span></span>

```bash
docker pull microsoft/azure-cli
```

## <a name="uninstall-docker-image"></a><span data-ttu-id="f14c3-116">卸载 Docker 映像</span><span class="sxs-lookup"><span data-stu-id="f14c3-116">Uninstall Docker image</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

<span data-ttu-id="f14c3-117">停止运行 CLI 映像的任何容器后，请删除该映像。</span><span class="sxs-lookup"><span data-stu-id="f14c3-117">After halting any containers running the CLI image, remove it.</span></span>

```bash
docker rmi microsoft/azure-cli
```
