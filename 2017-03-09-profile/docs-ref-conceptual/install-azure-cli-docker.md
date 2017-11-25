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
# <a name="install-azure-cli-20-with-docker"></a><span data-ttu-id="6accb-104">使用 Docker 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="6accb-104">Install Azure CLI 2.0 with Docker</span></span>

<span data-ttu-id="6accb-105">可以使用 Docker 安装已预安装 Azure CLI 2.0 的独立 Linux 容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-105">You can use Docker to install a standalone Linux container with the Azure CLI 2.0 pre-installed.</span></span> <span data-ttu-id="6accb-106">这样可以通过一个环境来快速启动，在环境中尝试 CLI 以确定其是否适合自己；也可以将此用作基础映像。</span><span class="sxs-lookup"><span data-stu-id="6accb-106">This lets you get started quickly with an environment where you can try out the CLI to decide if it's right for you, or allows you to use this as a base image.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="6accb-107">使用 Docker 安装</span><span class="sxs-lookup"><span data-stu-id="6accb-107">Install with Docker</span></span>

<span data-ttu-id="6accb-108">请使用 `docker run` 安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="6accb-108">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run -it azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="6accb-109">请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。</span><span class="sxs-lookup"><span data-stu-id="6accb-109">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="6accb-110">CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。</span><span class="sxs-lookup"><span data-stu-id="6accb-110">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="6accb-111">如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。</span><span class="sxs-lookup"><span data-stu-id="6accb-111">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -it -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

### <a name="update-with-docker"></a><span data-ttu-id="6accb-112">使用 Docker 更新</span><span class="sxs-lookup"><span data-stu-id="6accb-112">Update with Docker</span></span>

<span data-ttu-id="6accb-113">使用 Docker 进行更新需要拉取新映像和重新创建任何现有的容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-113">Updating with Docker requires both pulling the new image and re-creating any existing containers.</span></span> <span data-ttu-id="6accb-114">因此应进行尝试，避免使用将 CLI 作为数据存储来托管的容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-114">For this reason you should try and avoid using a container which hosts the CLI as a data store.</span></span>

1. <span data-ttu-id="6accb-115">使用 `docker pull` 更新本地映像。</span><span class="sxs-lookup"><span data-stu-id="6accb-115">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="6accb-116">获取当前正在使用 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-116">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

  > [!NOTE]
  > <span data-ttu-id="6accb-117">如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。</span><span class="sxs-lookup"><span data-stu-id="6accb-117">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="6accb-118">停止并重新创建容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-118">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="6accb-119">使用 Docker 卸载</span><span class="sxs-lookup"><span data-stu-id="6accb-119">Uninstall with Docker</span></span>

<span data-ttu-id="6accb-120">如果你决定卸载 Azure CLI，我们会很遗憾。</span><span class="sxs-lookup"><span data-stu-id="6accb-120">If you ever decide to uninstall the Azure CLI, we're sorry to see you go.</span></span> <span data-ttu-id="6accb-121">在卸载之前，请执行 `az feedback` 命令，说明选择卸载的原因以及希望我们如何改进 CLI 体验。</span><span class="sxs-lookup"><span data-stu-id="6accb-121">Before you uninstall, use the `az feedback` command to give us some reasons why you chose to uninstall and how we could improve the CLI experience.</span></span> <span data-ttu-id="6accb-122">我们希望尽力确保 Azure CLI 没有 Bug，为用户提供美好的体验。</span><span class="sxs-lookup"><span data-stu-id="6accb-122">We want to make sure that the Azure CLI is as bug-free and user-friendly as we can make it.</span></span> <span data-ttu-id="6accb-123">也可[提交 GitHub 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="6accb-123">You can also [file a github issue](https://github.com/Azure/azure-cli/issues).</span></span>

<span data-ttu-id="6accb-124">若要正确卸载 CLI Docker 映像，需删除运行该映像的所有容器，然后删除本地映像。</span><span class="sxs-lookup"><span data-stu-id="6accb-124">To properly uninstall the CLI Docker image you need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="6accb-125">获取运行 azure-cli 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-125">Get the containers running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```
  > [!NOTE]
  > <span data-ttu-id="6accb-126">如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。</span><span class="sxs-lookup"><span data-stu-id="6accb-126">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

2. <span data-ttu-id="6accb-127">删除所有包含 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="6accb-127">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="6accb-128">删除本地安装的 CLI 映像。</span><span class="sxs-lookup"><span data-stu-id="6accb-128">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

