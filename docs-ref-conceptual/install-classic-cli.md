---
title: 安装 Azure 经典 CLI
description: 安装适用于 Mac、Linux 和 Windows 的 Azure 经典 CLI 即可使用 Azure 服务
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/11/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 68aa728b9b9324a53856008f05d8ce30eb61c76d
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178146"
---
# <a name="install-the-azure-classic-cli"></a><span data-ttu-id="6718a-103">安装 Azure 经典 CLI</span><span class="sxs-lookup"><span data-stu-id="6718a-103">Install the Azure classic CLI</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6718a-104">本主题介绍如何安装 Azure 经典 CLI。</span><span class="sxs-lookup"><span data-stu-id="6718a-104">This topic describes how to install the Azure classic CLI.</span></span> <span data-ttu-id="6718a-105">此经典 CLI 已弃用，只能与经典部署模型配合使用。</span><span class="sxs-lookup"><span data-stu-id="6718a-105">The classic CLI is deprecated and should only be used with the classic deployment model.</span></span>
> <span data-ttu-id="6718a-106">进行所有其他的部署时，请使用 [Azure CLI](/cli/azure)。</span><span class="sxs-lookup"><span data-stu-id="6718a-106">For all other deployments, use [the Azure CLI](/cli/azure).</span></span>

<span data-ttu-id="6718a-107">快速安装 Azure 经典 CLI，以便使用一组基于 shell 的开源命令在 Microsoft Azure 中创建和管理资源。</span><span class="sxs-lookup"><span data-stu-id="6718a-107">Quickly install the Azure classic CLI to use a set of open-source shell-based commands for creating and managing resources in Microsoft Azure.</span></span> <span data-ttu-id="6718a-108">可以通过多个选项在计算机上安装这些跨平台工具：</span><span class="sxs-lookup"><span data-stu-id="6718a-108">You have several options to install these cross-platform tools on your computer:</span></span>

* <span data-ttu-id="6718a-109">**npm 包** - 运行 npm（JavaScript 的包管理器），在 Linux 发行版或 OS 中安装 Azure 经典 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="6718a-109">**npm package** - Run npm (the package manager for JavaScript) to install the Azure classic CLI package on your Linux distribution or OS.</span></span> <span data-ttu-id="6718a-110">需要 node.js 和 npm。</span><span class="sxs-lookup"><span data-stu-id="6718a-110">Requires node.js and npm.</span></span>
* <span data-ttu-id="6718a-111">**安装程序** - 下载安装程序，在 macOS 或 Windows 上轻松地进行安装。</span><span class="sxs-lookup"><span data-stu-id="6718a-111">**Installer** - Download an installer for easy installation on macOS or Windows.</span></span>
* <span data-ttu-id="6718a-112">**Docker 容器** - 开始在做好运行准备的 Docker 容器中使用经典 CLI。</span><span class="sxs-lookup"><span data-stu-id="6718a-112">**Docker container** - Start using the classic CLI in a ready-to-run Docker container.</span></span> <span data-ttu-id="6718a-113">需要 Docker 主机。</span><span class="sxs-lookup"><span data-stu-id="6718a-113">Requires a Docker host.</span></span>

<span data-ttu-id="6718a-114">有关更多选项和背景信息，请参阅 [GitHub](https://github.com/azure/azure-xplat-cli) 上的项目存储库。</span><span class="sxs-lookup"><span data-stu-id="6718a-114">For more options and background, see the project repository on [GitHub](https://github.com/azure/azure-xplat-cli).</span></span>

<span data-ttu-id="6718a-115">安装 Azure 经典 CLI 之后，请使用 `azure login` 进行连接，然后从命令行界面（Bash、终端、命令提示符等）运行 `azure` 命令，以便使用 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="6718a-115">Once the Azure classic CLI is installed, connect with `azure login` and run the `azure` commands from your command-line interface (Bash, Terminal, Command prompt, and so on) to work with your Azure resources.</span></span>

## <a name="option-1-install-an-npm-package"></a><span data-ttu-id="6718a-116">选项 1：安装 npm 包</span><span class="sxs-lookup"><span data-stu-id="6718a-116">Option 1: Install an npm package</span></span>

<span data-ttu-id="6718a-117">若要通过 npm 包安装经典 CLI，请确保已下载并安装[最新 Node.js 和 npm](https://nodejs.org/en/download/package-manager/)。</span><span class="sxs-lookup"><span data-stu-id="6718a-117">To install the classic CLI from an npm package, make sure you have downloaded and installed the [latest Node.js and npm](https://nodejs.org/en/download/package-manager/).</span></span> <span data-ttu-id="6718a-118">然后，运行 `npm install` 以安装 azure-cli 包：</span><span class="sxs-lookup"><span data-stu-id="6718a-118">Then, run `npm install` to install the azure-cli package:</span></span>

```bash
npm install -g azure-cli
```

<span data-ttu-id="6718a-119">在 Linux 发行版中，可能需要使用 `sudo` 才能成功运行 `npm` 命令，如下所示：</span><span class="sxs-lookup"><span data-stu-id="6718a-119">On Linux distributions, you might need to use `sudo` to successfully run the `npm` command, as follows:</span></span>

```bash
sudo npm install -g azure-cli
```

> [!NOTE]
> <span data-ttu-id="6718a-120">如果需要在 OS 中安装或更新 Node.js 和 npm，建议安装 Node.js LTS 4.x 或更高版本。</span><span class="sxs-lookup"><span data-stu-id="6718a-120">If you need to install or update Node.js and npm on your OS, we recommend that you install Node.js LTS version 4.x or later.</span></span> <span data-ttu-id="6718a-121">如果使用旧版本，可能会遇到安装错误。</span><span class="sxs-lookup"><span data-stu-id="6718a-121">If you use an older version, you might get installation errors.</span></span>

<span data-ttu-id="6718a-122">如果你愿意，也可从 [GitHub 发行版](https://github.com/Azure/azure-xplat-cli/releases)下载 tar 文件。</span><span class="sxs-lookup"><span data-stu-id="6718a-122">If you prefer, you may also download a tar file from the [GitHub releases](https://github.com/Azure/azure-xplat-cli/releases).</span></span> <span data-ttu-id="6718a-123">然后，安装所下载的 npm 包，如下所示（在 Linux 发行版中可能需要使用 `sudo`）：</span><span class="sxs-lookup"><span data-stu-id="6718a-123">Then, install the downloaded npm package as follows (on Linux distributions you might need to use `sudo`):</span></span>

```bash
npm install -g <path to downloaded tar file>
```

## <a name="option-2-use-an-installer"></a><span data-ttu-id="6718a-124">选项 2：使用安装程序</span><span class="sxs-lookup"><span data-stu-id="6718a-124">Option 2: Use an installer</span></span>

<span data-ttu-id="6718a-125">如果使用 Mac 或 Windows 计算机，可以从 [GitHub 发行版](https://github.com/Azure/azure-xplat-cli/releases)获取 DMG 和 MSI 安装程序。</span><span class="sxs-lookup"><span data-stu-id="6718a-125">If you use a Mac or Windows computer, DMG and MSI installers are available from [GitHub releases](https://github.com/Azure/azure-xplat-cli/releases).</span></span>

> [!TIP]
> <span data-ttu-id="6718a-126">在 Windows 上，还可以下载 [Web 平台安装程序](https://go.microsoft.com/?linkid=9828653)来安装经典 CLI。</span><span class="sxs-lookup"><span data-stu-id="6718a-126">On Windows, you can also download the [Web Platform Installer](https://go.microsoft.com/?linkid=9828653) to install the classic CLI.</span></span> <span data-ttu-id="6718a-127">此安装程序允许安装附加的 Azure SDK 和命令行工具。</span><span class="sxs-lookup"><span data-stu-id="6718a-127">This installer gives you the option to install additional Azure SDK and command-line tools.</span></span>

## <a name="option-3-use-a-docker-container"></a><span data-ttu-id="6718a-128">选项 3：使用 Docker 容器</span><span class="sxs-lookup"><span data-stu-id="6718a-128">Option 3: Use a Docker container</span></span>

<span data-ttu-id="6718a-129">如果已将计算机设置为 [Docker](https://docs.docker.com/engine/understanding-docker/) 主机，可以在 Docker 容器中运行 Azure 经典 CLI。</span><span class="sxs-lookup"><span data-stu-id="6718a-129">If you have set up your computer as a [Docker](https://docs.docker.com/engine/understanding-docker/) host, you can run the Azure classic CLI in a Docker container.</span></span> <span data-ttu-id="6718a-130">运行以下命令（在 Linux 发行版中，可能需要使用 `sudo`）：</span><span class="sxs-lookup"><span data-stu-id="6718a-130">Run the following command (on Linux distributions you might need to use `sudo`):</span></span>

```bash
docker run -it microsoft/azure-cli:0.10.17
```

## <a name="run-azure-classic-cli-commands"></a><span data-ttu-id="6718a-131">运行 Azure 经典 CLI 命令</span><span class="sxs-lookup"><span data-stu-id="6718a-131">Run Azure classic CLI commands</span></span>

<span data-ttu-id="6718a-132">安装经典 CLI 之后，请从命令行用户界面（Bash、终端、命令提示符等）运行 `azure` 命令。</span><span class="sxs-lookup"><span data-stu-id="6718a-132">After the classic CLI is installed, run the `azure` command from your command-line user interface (Bash, Terminal, Command prompt, and so on).</span></span> <span data-ttu-id="6718a-133">例如，若要运行帮助命令，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="6718a-133">For example, to run the help command, type the following:</span></span>

```azurecli
azure help
```

> [!NOTE]
> <span data-ttu-id="6718a-134">在某些 Linux 分发版中，可能会收到类似于“`/usr/bin/env: ‘node’: No such file or directory`”的错误。</span><span class="sxs-lookup"><span data-stu-id="6718a-134">On some Linux distributions, you may receive an error similar to `/usr/bin/env: ‘node’: No such file or directory`.</span></span> <span data-ttu-id="6718a-135">此错误消息来自最近安装在 /usr/bin/nodejs 中的 Node.js。</span><span class="sxs-lookup"><span data-stu-id="6718a-135">This error comes from recent installations of Node.js being installed at /usr/bin/nodejs.</span></span> <span data-ttu-id="6718a-136">若要解决此错误，请运行以下命令创建 /usr/bin/node 的符号链接：</span><span class="sxs-lookup"><span data-stu-id="6718a-136">To fix it, create a symbolic link to /usr/bin/node by running this command:</span></span>

```bash
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

<span data-ttu-id="6718a-137">若要查看安装的 Azure 经典 CLI 版本，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="6718a-137">To see the version of the Azure classic CLI installed, type the following:</span></span>

```azurecli
azure --version
```

> [!NOTE]
> <span data-ttu-id="6718a-138">首次使用 Azure 经典 CLI 时，会看到一条消息，询问是否允许 Microsoft 收集使用情况信息。</span><span class="sxs-lookup"><span data-stu-id="6718a-138">When you first use Azure classic CLI, you see a message asking if you want to allow Microsoft to collect usage information.</span></span> <span data-ttu-id="6718a-139">参与为自愿性质。</span><span class="sxs-lookup"><span data-stu-id="6718a-139">Participation is voluntary.</span></span> <span data-ttu-id="6718a-140">如果选择参与，通过运行 `azure telemetry --disable` 即可随时停止参与。</span><span class="sxs-lookup"><span data-stu-id="6718a-140">If you choose to participate, you can stop at any time by running `azure telemetry --disable`.</span></span> <span data-ttu-id="6718a-141">若要随时启用参与，请运行 `azure telemetry --enable`。</span><span class="sxs-lookup"><span data-stu-id="6718a-141">To enable participation at any time, run `azure telemetry --enable`.</span></span>

## <a name="update-the-classic-cli"></a><span data-ttu-id="6718a-142">更新经典 CLI</span><span class="sxs-lookup"><span data-stu-id="6718a-142">Update the classic CLI</span></span>

<span data-ttu-id="6718a-143">Microsoft 可能会发布 Azure 经典 CLI 的更新版本。</span><span class="sxs-lookup"><span data-stu-id="6718a-143">Microsoft may release updated versions of the Azure classic CLI.</span></span> <span data-ttu-id="6718a-144">使用适用于操作系统的安装程序来重新安装经典 CLI，或运行最新的 Docker 容器。</span><span class="sxs-lookup"><span data-stu-id="6718a-144">Reinstall the classic CLI using the installer for your operating system, or run the latest Docker container.</span></span> <span data-ttu-id="6718a-145">如果已安装最新的 Node.js 和 npm，请键入以下命令（在 Linux 发行版中可能需要使用 `sudo`）进行更新。</span><span class="sxs-lookup"><span data-stu-id="6718a-145">Or, if you have the latest Node.js and npm installed, update by typing the following (on Linux distributions you might need to use `sudo`).</span></span>

```bash
npm update -g azure-cli
```

## <a name="enable-tab-completion"></a><span data-ttu-id="6718a-146">启用 tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="6718a-146">Enable tab completion</span></span>

<span data-ttu-id="6718a-147">Mac 和 Linux 支持 tab 自动补全经典 CLI 命令。</span><span class="sxs-lookup"><span data-stu-id="6718a-147">Tab completion of classic CLI commands is supported for Mac and Linux.</span></span>

<span data-ttu-id="6718a-148">如要在 zsh 中启用，运行：</span><span class="sxs-lookup"><span data-stu-id="6718a-148">To enable it in zsh, run:</span></span>

```bash
echo '. <(azure --completion)' >> .zshrc
```

<span data-ttu-id="6718a-149">若要在 bash 中启用，运行：</span><span class="sxs-lookup"><span data-stu-id="6718a-149">To enable it in bash, run:</span></span>

```bash
azure --completion >> ~/azure.completion.sh
echo 'source ~/azure.completion.sh' >> ~/.bash_profile
```

## <a name="next-steps"></a><span data-ttu-id="6718a-150">后续步骤</span><span class="sxs-lookup"><span data-stu-id="6718a-150">Next steps</span></span>

* <span data-ttu-id="6718a-151">若要了解有关 Azure 经典CLI、下载源代码、报告问题或贡献项目的详细信息，请访问[适用于 Azure 经典CLI 的 GitHub 存储库](https://github.com/azure/azure-xplat-cli)。</span><span class="sxs-lookup"><span data-stu-id="6718a-151">To learn more about the Azure classic CLI, download source code, report problems, or contribute to the project, visit the [GitHub repository for the Azure classic CLI](https://github.com/azure/azure-xplat-cli).</span></span>
