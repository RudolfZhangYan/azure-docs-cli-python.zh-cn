---
title: 安装 Azure CLI 1.0
description: 安装适用于 Mac、Linux 和 Windows 的 Azure CLI 1.0 即可使用 Azure 服务
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 03/20/2017
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 92714f32736e0a1a0ea7c8dd4a615b158c955931
ms.sourcegitcommit: ae72b6c8916aeb372a92188090529037e63930ba
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/28/2018
---
# <a name="install-the-azure-cli-10"></a><span data-ttu-id="cc543-103">安装 Azure CLI 1.0</span><span class="sxs-lookup"><span data-stu-id="cc543-103">Install the Azure CLI 1.0</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cc543-104">本主题介绍如何安装 Azure CLI 1.0。</span><span class="sxs-lookup"><span data-stu-id="cc543-104">This topic describes how to install the Azure CLI 1.0.</span></span> <span data-ttu-id="cc543-105">此 CLI 已弃用，并且仅应当用于支持带有“经典”资源的 Azure 服务管理 (ASM) 模型。</span><span class="sxs-lookup"><span data-stu-id="cc543-105">This CLI is deprecated and should only be used for support with the Azure Service Management (ASM) model with "classic" resources.</span></span>
> <span data-ttu-id="cc543-106">对于 Azure 资源管理器部署，请使用 [Azure CLI 2.0](/cli/azure)。</span><span class="sxs-lookup"><span data-stu-id="cc543-106">For Azure Resource Manager deployments, use [Azure CLI 2.0](/cli/azure).</span></span>

<span data-ttu-id="cc543-107">快速安装 Azure 命令行接口 (Azure CLI 1.0)，以便使用一组基于 shell 的开源命令在 Microsoft Azure 中创建和管理资源。</span><span class="sxs-lookup"><span data-stu-id="cc543-107">Quickly install the Azure Command-Line Interface (Azure CLI 1.0) to use a set of open-source shell-based commands for creating and managing resources in Microsoft Azure.</span></span> <span data-ttu-id="cc543-108">可以通过多个选项在计算机上安装这些跨平台工具：</span><span class="sxs-lookup"><span data-stu-id="cc543-108">You have several options to install these cross-platform tools on your computer:</span></span>

* <span data-ttu-id="cc543-109">**npm 包** - 运行 npm（JavaScript 的包管理器）可在 Linux 分发版或操作系统中安装最新的 Azure CLI 1.0 包。</span><span class="sxs-lookup"><span data-stu-id="cc543-109">**npm package** - Run npm (the package manager for JavaScript) to install the latest Azure CLI 1.0 package on your Linux distribution or OS.</span></span> <span data-ttu-id="cc543-110">计算机上需要存在 node.js 和 npm。</span><span class="sxs-lookup"><span data-stu-id="cc543-110">Requires node.js and npm on your computer.</span></span>
* <span data-ttu-id="cc543-111">**安装程序** - 下载安装程序以轻松在 Mac 或 Windows 上进行安装。</span><span class="sxs-lookup"><span data-stu-id="cc543-111">**Installer** - Download an installer for easy installation on Mac or Windows.</span></span>
* <span data-ttu-id="cc543-112">**Docker 容器** - 在就绪可运行的 Docker 容器中开始使用最新的 CLI。</span><span class="sxs-lookup"><span data-stu-id="cc543-112">**Docker container** - Start using the latest CLI in a ready-to-run Docker container.</span></span> <span data-ttu-id="cc543-113">计算机上需要存在 Docker 主机。</span><span class="sxs-lookup"><span data-stu-id="cc543-113">Requires Docker host on your computer.</span></span>

<span data-ttu-id="cc543-114">有关更多选项和背景信息，请参阅 [GitHub](https://github.com/azure/azure-xplat-cli) 上的项目存储库。</span><span class="sxs-lookup"><span data-stu-id="cc543-114">For more options and background, see the project repository on [GitHub](https://github.com/azure/azure-xplat-cli).</span></span>

<span data-ttu-id="cc543-115">安装 Azure CLI 1.0 后，[将它连接到 Azure 订阅](/cli/azure/authenticate-azure-cli)，并从命令行接口（Bash、终端、命令提示符等）运行 **azure** 命令，从而使用 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="cc543-115">Once the Azure CLI 1.0 is installed, [connect it with your Azure subscription](/cli/azure/authenticate-azure-cli) and run the **azure** commands from your command-line interface (Bash, Terminal, Command prompt, and so on) to work with your Azure resources.</span></span>

## <a name="option-1-install-an-npm-package"></a><span data-ttu-id="cc543-116">选项 1：安装 npm 包</span><span class="sxs-lookup"><span data-stu-id="cc543-116">Option 1: Install an npm package</span></span>
<span data-ttu-id="cc543-117">若要通过 npm 包安装 CLI，请确保已下载并安装了[最新的 Node.js 和 npm](https://nodejs.org/en/download/package-manager/)。</span><span class="sxs-lookup"><span data-stu-id="cc543-117">To install the CLI from an npm package, make sure you have downloaded and installed the [latest Node.js and npm](https://nodejs.org/en/download/package-manager/).</span></span> <span data-ttu-id="cc543-118">然后，运行 npm install，安装 azure-cli 包：</span><span class="sxs-lookup"><span data-stu-id="cc543-118">Then, run **npm install** to install the azure-cli package:</span></span>

```bash
npm install -g azure-cli
```

<span data-ttu-id="cc543-119">在 Linux 分发版中，可能需要使用 **sudo** 才能成功运行 **npm** 命令，如下所示：</span><span class="sxs-lookup"><span data-stu-id="cc543-119">On Linux distributions, you might need to use **sudo** to successfully run the **npm** command, as follows:</span></span>

```bash
sudo npm install -g azure-cli
```

> [!NOTE]
> <span data-ttu-id="cc543-120">如果需要在 Linux 分发版或 OS 中安装或更新 Node.js 和 npm，建议安装最新的 Node.js LTS 版本 (4.x)。</span><span class="sxs-lookup"><span data-stu-id="cc543-120">If you need to install or update Node.js and npm on your Linux distribution or OS, we recommend that you install the most recent Node.js LTS version (4.x).</span></span> <span data-ttu-id="cc543-121">如果使用旧版本，可能会遇到安装错误。</span><span class="sxs-lookup"><span data-stu-id="cc543-121">If you use an older version, you might get installation errors.</span></span>

<span data-ttu-id="cc543-122">如果喜欢，也可以将 npm 包的最新 Linux [tar 文件][linux-installer]下载到本地。</span><span class="sxs-lookup"><span data-stu-id="cc543-122">If you prefer, download the latest Linux [tar file][linux-installer] for the npm package locally.</span></span> <span data-ttu-id="cc543-123">然后，如下所示安装所下载的 npm 包（在 Linux 分发版中可能需要使用 sudo）：</span><span class="sxs-lookup"><span data-stu-id="cc543-123">Then, install the downloaded npm package as follows (on Linux distributions you might need to use **sudo**):</span></span>

```bash
npm install -g <path to downloaded tar file>
```

## <a name="option-2-use-an-installer"></a><span data-ttu-id="cc543-124">选项 2：使用安装程序</span><span class="sxs-lookup"><span data-stu-id="cc543-124">Option 2: Use an installer</span></span>
<span data-ttu-id="cc543-125">如果使用的是 Mac 或 Windows 计算机，可以下载以下 CLI 安装程序：</span><span class="sxs-lookup"><span data-stu-id="cc543-125">If you use a Mac or Windows computer, the following CLI installers are available for download:</span></span>

* <span data-ttu-id="cc543-126">[Mac OS X 安装程序][mac-installer]</span><span class="sxs-lookup"><span data-stu-id="cc543-126">[Mac OS X installer][mac-installer]</span></span>
* <span data-ttu-id="cc543-127">[Windows MSI][windows-installer]</span><span class="sxs-lookup"><span data-stu-id="cc543-127">[Windows MSI][windows-installer]</span></span>

> [!TIP]
> <span data-ttu-id="cc543-128">在 Windows 上，还可以下载 [Web 平台安装程序](https://go.microsoft.com/?linkid=9828653)来安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="cc543-128">On Windows, you can also download the [Web Platform Installer](https://go.microsoft.com/?linkid=9828653) to install the CLI.</span></span> <span data-ttu-id="cc543-129">此安装程序允许在安装 CLI 后安装附加的 Azure SDK 和命令行工具。</span><span class="sxs-lookup"><span data-stu-id="cc543-129">This installer gives you the option to install additional Azure SDK and command-line tools after installing the CLI.</span></span>

## <a name="option-3-use-a-docker-container"></a><span data-ttu-id="cc543-130">选项 3：使用 Docker 容器</span><span class="sxs-lookup"><span data-stu-id="cc543-130">Option 3: Use a Docker container</span></span>
<span data-ttu-id="cc543-131">如果已将计算机设置为 [Docker](https://docs.docker.com/engine/understanding-docker/) 主机，可以在 Docker 容器中运行最新的 Azure CLI 1.0。</span><span class="sxs-lookup"><span data-stu-id="cc543-131">If you have set up your computer as a [Docker](https://docs.docker.com/engine/understanding-docker/) host, you can run the latest Azure CLI 1.0 in a Docker container.</span></span> <span data-ttu-id="cc543-132">运行以下命令（在 Linux 分发版中，可能需要使用 **sudo**）：</span><span class="sxs-lookup"><span data-stu-id="cc543-132">Run the following command (on Linux distributions you might need to use **sudo**):</span></span>

```bash
docker run -it microsoft/azure-cli:0.10.17
```

## <a name="run-azure-cli-10-commands"></a><span data-ttu-id="cc543-133">运行 Azure CLI 1.0 命令</span><span class="sxs-lookup"><span data-stu-id="cc543-133">Run Azure CLI 1.0 commands</span></span>
<span data-ttu-id="cc543-134">安装 Azure CLI 1.0 后，从命令行用户界面（Bash、终端、命令提示符等）运行 **azure** 命令。</span><span class="sxs-lookup"><span data-stu-id="cc543-134">After the Azure CLI 1.0 is installed, run the **azure** command from your command-line user interface (Bash, Terminal, Command prompt, and so on).</span></span> <span data-ttu-id="cc543-135">例如，若要运行帮助命令，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="cc543-135">For example, to run the help command, type the following:</span></span>

```azurecli
azure help
```

> [!NOTE]
> <span data-ttu-id="cc543-136">在某些 Linux 分发版中，可能会收到类似于“`/usr/bin/env: ‘node’: No such file or directory`”的错误。</span><span class="sxs-lookup"><span data-stu-id="cc543-136">On some Linux distributions, you may receive an error similar to `/usr/bin/env: ‘node’: No such file or directory`.</span></span> <span data-ttu-id="cc543-137">此错误消息来自最近安装在 /usr/bin/nodejs 中的 Node.js。</span><span class="sxs-lookup"><span data-stu-id="cc543-137">This error comes from recent installations of Node.js being installed at /usr/bin/nodejs.</span></span> <span data-ttu-id="cc543-138">若要解决此错误，请运行以下命令创建 /usr/bin/node 的符号链接：</span><span class="sxs-lookup"><span data-stu-id="cc543-138">To fix it, create a symbolic link to /usr/bin/node by running this command:</span></span>

```bash
sudo ln -s /usr/bin/nodejs /usr/bin/node
```

<span data-ttu-id="cc543-139">若要查看安装的 Azure CLI 1.0 版本，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="cc543-139">To see the version of the Azure CLI 1.0 you installed, type the following:</span></span>

```azurecli
azure --version
```

<span data-ttu-id="cc543-140">现在已准备就绪！</span><span class="sxs-lookup"><span data-stu-id="cc543-140">Now you are ready!</span></span> <span data-ttu-id="cc543-141">若要访问所有 CLI 命令来使用自己的资源，请[从 Azure CLI 连接到 Azure 订阅](/cli/azure/authenticate-azure-cli)。</span><span class="sxs-lookup"><span data-stu-id="cc543-141">To access all the CLI commands to work with your own resources, [connect to your Azure subscription from the Azure CLI](/cli/azure/authenticate-azure-cli).</span></span>

> [!NOTE]
> <span data-ttu-id="cc543-142">首次使用 Azure CLI 时，会看到一条消息，询问是否允许 Microsoft 收集使用情况信息。</span><span class="sxs-lookup"><span data-stu-id="cc543-142">When you first use Azure CLI, you see a message asking if you want to allow Microsoft to collect usage information.</span></span> <span data-ttu-id="cc543-143">参与为自愿性质。</span><span class="sxs-lookup"><span data-stu-id="cc543-143">Participation is voluntary.</span></span> <span data-ttu-id="cc543-144">如果选择参与，通过运行 `azure telemetry --disable` 即可随时停止参与。</span><span class="sxs-lookup"><span data-stu-id="cc543-144">If you choose to participate, you can stop at any time by running `azure telemetry --disable`.</span></span> <span data-ttu-id="cc543-145">若要随时启用参与，请运行 `azure telemetry --enable`。</span><span class="sxs-lookup"><span data-stu-id="cc543-145">To enable participation at any time, run `azure telemetry --enable`.</span></span>

## <a name="update-the-cli"></a><span data-ttu-id="cc543-146">更新 CLI</span><span class="sxs-lookup"><span data-stu-id="cc543-146">Update the CLI</span></span>
<span data-ttu-id="cc543-147">Microsoft 会频繁发布 Azure CLI 的更新版本。</span><span class="sxs-lookup"><span data-stu-id="cc543-147">Microsoft frequently releases updated versions of the Azure CLI.</span></span> <span data-ttu-id="cc543-148">使用适用于操作系统的安装程序来重新安装 CLI，或运行最新的 Docker 容器。</span><span class="sxs-lookup"><span data-stu-id="cc543-148">Reinstall the CLI using the installer for your operating system, or run the latest Docker container.</span></span> <span data-ttu-id="cc543-149">如果已安装最新的 Node.js 和 npm，请键入以下命令（在 Linux 分发版中可能需要使用 **sudo**）进行更新。</span><span class="sxs-lookup"><span data-stu-id="cc543-149">Or, if you have the latest Node.js and npm installed, update by typing the following (on Linux distributions you might need to use **sudo**).</span></span>

```bash
npm update -g azure-cli
```

## <a name="enable-tab-completion"></a><span data-ttu-id="cc543-150">启用 tab 自动补全</span><span class="sxs-lookup"><span data-stu-id="cc543-150">Enable tab completion</span></span>
<span data-ttu-id="cc543-151">Mac 和 Linux 支持 tab 自动补全 CLI 命令。</span><span class="sxs-lookup"><span data-stu-id="cc543-151">Tab completion of CLI commands is supported for Mac and Linux.</span></span>

<span data-ttu-id="cc543-152">如要在 zsh 中启用，运行：</span><span class="sxs-lookup"><span data-stu-id="cc543-152">To enable it in zsh, run:</span></span>

```bash
echo '. <(azure --completion)' >> .zshrc
```

<span data-ttu-id="cc543-153">若要在 bash 中启用，运行：</span><span class="sxs-lookup"><span data-stu-id="cc543-153">To enable it in bash, run:</span></span>

```bash
azure --completion >> ~/azure.completion.sh
echo 'source ~/azure.completion.sh' >> ~/.bash_profile
```


## <a name="next-steps"></a><span data-ttu-id="cc543-154">后续步骤</span><span class="sxs-lookup"><span data-stu-id="cc543-154">Next steps</span></span>
* <span data-ttu-id="cc543-155">[从 CLI 连接到 Azure 订阅](/cli/azure/authenticate-azure-cli)以创建和管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="cc543-155">[Connect from the CLI to your Azure subscription](/cli/azure/authenticate-azure-cli) to create and manage Azure resources.</span></span>
* <span data-ttu-id="cc543-156">若要了解有关 Azure CLI、下载源代码、报告问题或贡献项目的详细信息，请访问[适用于 Azure CLI 的 GitHub 存储库](https://github.com/azure/azure-xplat-cli)。</span><span class="sxs-lookup"><span data-stu-id="cc543-156">To learn more about the Azure CLI, download source code, report problems, or contribute to the project, visit the [GitHub repository for the Azure CLI](https://github.com/azure/azure-xplat-cli).</span></span>
* <span data-ttu-id="cc543-157">如果在使用 Azure CLI 或 Azure 方面有疑问，请访问 [Azure 论坛](https://social.msdn.microsoft.com/Forums/en-US/home?forum=azurescripting)。</span><span class="sxs-lookup"><span data-stu-id="cc543-157">If you have questions about using the Azure CLI, or Azure, visit the [Azure Forums](https://social.msdn.microsoft.com/Forums/en-US/home?forum=azurescripting).</span></span>


[mac-installer]: http://aka.ms/mac-azure-cli
[windows-installer]: http://aka.ms/webpi-azure-cli
[linux-installer]: http://aka.ms/linux-azure-cli
[cliasm]: /cli/azure/get-started-with-az-cli2
[cliarm]: ./virtual-machines/azure-cli-arm-commands.md
