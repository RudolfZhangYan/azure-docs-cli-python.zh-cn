---
title: "安装 Azure CLI 2.0"
description: "Azure CLI 2.0 的参考文档"
keywords: "Azure CLI 2.0, Azure CLI 2.0 参考, 安装 Azure CLI 2.0, Azure Python CLI, 卸载 Azure CLI 2.0"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/06/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 7065ed5270ef9bfc70beea81d0bc442a7b4df38c
ms.sourcegitcommit: c077bd5cbe07f7225714c41714d3981fa0d9928f
ms.contentlocale: zh-CN
ms.lasthandoff: 05/16/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="4d537-104">安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="4d537-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="4d537-105">现在就安装新版本的 Azure CLI！</span><span class="sxs-lookup"><span data-stu-id="4d537-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="4d537-106">我们已改进并更新了 Azure CLI，以提供用于管理 Azure 资源的卓越本机命令行体验。</span><span class="sxs-lookup"><span data-stu-id="4d537-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="4d537-107">它可以在 macOS、Linux 和 Windows 上使用。</span><span class="sxs-lookup"><span data-stu-id="4d537-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="4d537-108">有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="4d537-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="4d537-109">如果需要早期版本的 Azure CLI，请参阅此处的如何[安装 Azure 1.0](/azure/cli-install-nodejs)。</span><span class="sxs-lookup"><span data-stu-id="4d537-109">If you need the previous version of the Azure CLI, here's how to [install Azure 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="macos"></a><span data-ttu-id="4d537-110">macOS</span><span class="sxs-lookup"><span data-stu-id="4d537-110">macOS</span></span>

1. <span data-ttu-id="4d537-111">使用一个 `curl` 命令安装 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4d537-111">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="4d537-112">可能需要重新启动命令外壳，某些更改才会生效。</span><span class="sxs-lookup"><span data-stu-id="4d537-112">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="4d537-113">在命令提示符下使用 `az` 命令运行 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4d537-113">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="4d537-114">使用 InstallAzureCli 进行安装时，`az component update` 不受支持。</span><span class="sxs-lookup"><span data-stu-id="4d537-114">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="4d537-115">若要更新到最新 CLI，请再次运行 `curl -L https://aka.ms/InstallAzureCli | bash`。</span><span class="sxs-lookup"><span data-stu-id="4d537-115">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="4d537-116">若要卸载，请参阅[手动卸载说明](#uninstall)。</span><span class="sxs-lookup"><span data-stu-id="4d537-116">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="windows"></a><span data-ttu-id="4d537-117">Windows</span><span class="sxs-lookup"><span data-stu-id="4d537-117">Windows</span></span>

<span data-ttu-id="4d537-118">可使用 MSI 安装 CLI 并在 Windows 命令行中使用它，或者可以在 Windows 中的 Bash on Ubuntu 上使用 apt-get 来安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="4d537-118">You can install the CLI with the MSI and use it in the Windows command-line, or you can install the CLI with apt-get on Bash on Ubuntu on Windows.</span></span>

### <a name="msi-for-the-windows-command-line"></a><span data-ttu-id="4d537-119">适用于 Windows 命令行的 MSI</span><span class="sxs-lookup"><span data-stu-id="4d537-119">MSI for the Windows command-line</span></span> 

<span data-ttu-id="4d537-120">要在 Windows 上安装 CLI 并在 Windows 命令行中使用它，请下载并运行 [msi](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="4d537-120">To install the CLI on Windows and use it in the Windows command-line, download and run the [msi](https://aka.ms/InstallAzureCliWindows).</span></span>

> [!NOTE]
> <span data-ttu-id="4d537-121">使用 msi 进行安装时，`az component` 不受支持。</span><span class="sxs-lookup"><span data-stu-id="4d537-121">When you install with the msi, `az component` isn't supported.</span></span>
> <span data-ttu-id="4d537-122">要更新到最新 CLI，请再次运行 [msi](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="4d537-122">To update to the latest CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again.</span></span>
> 
> <span data-ttu-id="4d537-123">要卸载 CLI，请再次运行 [msi](https://aka.ms/InstallAzureCliWindows) 并选择卸载。</span><span class="sxs-lookup"><span data-stu-id="4d537-123">To uninstall the CLI, run the [msi](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="4d537-124">适用于 Windows 中的 Bash on Ubuntu 的 apt-get</span><span class="sxs-lookup"><span data-stu-id="4d537-124">apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="4d537-125">如果你的 Windows 上没有 Bash，请[安装它](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="4d537-125">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="4d537-126">打开 Bash Shell。</span><span class="sxs-lookup"><span data-stu-id="4d537-126">Open the Bash shell.</span></span>

3. <span data-ttu-id="4d537-127">修改源列表。</span><span class="sxs-lookup"><span data-stu-id="4d537-127">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="4d537-128">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="4d537-128">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="4d537-129">使用 apt-get 进行安装时，`az component` 不受支持。</span><span class="sxs-lookup"><span data-stu-id="4d537-129">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="4d537-130">若要更新 CLI，请再次运行 `sudo apt-get update && sudo apt-get install azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4d537-130">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="4d537-131">若要卸载，请运行 `sudo apt-get remove azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4d537-131">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux"></a><span data-ttu-id="4d537-132">Linux</span><span class="sxs-lookup"><span data-stu-id="4d537-132">Linux</span></span>

1. <span data-ttu-id="4d537-133">在 Linux 上，可能需要安装特定的[必备组件](#linux-prerequisites)。</span><span class="sxs-lookup"><span data-stu-id="4d537-133">On Linux, you may need to install specific [prerequisites](#linux-prerequisites).</span></span>

2. <span data-ttu-id="4d537-134">使用一个 `curl` 命令安装 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4d537-134">Install Azure CLI 2.0 with one `curl` command.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="4d537-135">可能需要重新启动命令外壳，某些更改才会生效。</span><span class="sxs-lookup"><span data-stu-id="4d537-135">You may have to restart your command shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="4d537-136">在命令提示符下使用 `az` 命令运行 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4d537-136">Run Azure CLI 2.0 from the command prompt with the `az` command.</span></span>

> [!Note]
> <span data-ttu-id="4d537-137">使用 InstallAzureCli 进行安装时，`az component update` 不受支持。</span><span class="sxs-lookup"><span data-stu-id="4d537-137">When you install with InstallAzureCli, `az component update` isn't supported.</span></span>
> <span data-ttu-id="4d537-138">若要更新到最新 CLI，请再次运行 `curl -L https://aka.ms/InstallAzureCli | bash`。</span><span class="sxs-lookup"><span data-stu-id="4d537-138">To update to the latest CLI, run `curl -L https://aka.ms/InstallAzureCli | bash` again.</span></span>
> 
> <span data-ttu-id="4d537-139">若要卸载，请参阅[手动卸载说明](#uninstall)。</span><span class="sxs-lookup"><span data-stu-id="4d537-139">To uninstall, see the [manual uninstall instructions](#uninstall).</span></span>

## <a name="docker"></a><span data-ttu-id="4d537-140">Docker</span><span class="sxs-lookup"><span data-stu-id="4d537-140">Docker</span></span>

<span data-ttu-id="4d537-141">我们维护预先配置了 Azure CLI 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="4d537-141">We maintain a Docker image preconfigured with the Azure CLI.</span></span>

<span data-ttu-id="4d537-142">请使用 `docker run` 安装 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="4d537-142">Install the Azure CLI using `docker run`.</span></span>

```bash
docker run azuresdk/azure-cli-python:<version>
```

<span data-ttu-id="4d537-143">请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。</span><span class="sxs-lookup"><span data-stu-id="4d537-143">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

> [!NOTE]
> <span data-ttu-id="4d537-144">如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。</span><span class="sxs-lookup"><span data-stu-id="4d537-144">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> <span data-ttu-id="4d537-145">Docker 映像不支持 [`component` 功能](/cli/azure/component)。</span><span class="sxs-lookup"><span data-stu-id="4d537-145">The Docker image does not support the [`component` feature](/cli/azure/component).</span></span>
> <span data-ttu-id="4d537-146">若要更新 Azure CLI 2.0，请使用 `docker run` 安装最新映像或所需的特定映像。</span><span class="sxs-lookup"><span data-stu-id="4d537-146">To update the Azure CLI 2.0, use `docker run` to install the latest image, or the specific image that you want.</span></span>

## <a name="apt-get"></a><span data-ttu-id="4d537-147">apt-get</span><span class="sxs-lookup"><span data-stu-id="4d537-147">apt-get</span></span>

<span data-ttu-id="4d537-148">对于基于 Debian/Ubuntu 的系统，可以通过 `apt-get` 安装 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="4d537-148">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="4d537-149">修改源列表。</span><span class="sxs-lookup"><span data-stu-id="4d537-149">Modify your sources list.</span></span>

   - <span data-ttu-id="4d537-150">32 位系统</span><span class="sxs-lookup"><span data-stu-id="4d537-150">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="4d537-151">64 位系统</span><span class="sxs-lookup"><span data-stu-id="4d537-151">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="4d537-152">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="4d537-152">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> <span data-ttu-id="4d537-153">使用 apt-get 进行安装时，`az component` 不受支持。</span><span class="sxs-lookup"><span data-stu-id="4d537-153">When you install with apt-get, `az component` isn't supported.</span></span>
> <span data-ttu-id="4d537-154">若要更新 CLI，请再次运行 `sudo apt-get update && sudo apt-get install azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4d537-154">To update the CLI, run `sudo apt-get update && sudo apt-get install azure-cli` again.</span></span>
> 
> <span data-ttu-id="4d537-155">若要卸载，请运行 `sudo apt-get remove azure-cli`。</span><span class="sxs-lookup"><span data-stu-id="4d537-155">To uninstall, run `sudo apt-get remove azure-cli`.</span></span>

## <a name="linux-prerequisites"></a><span data-ttu-id="4d537-156">Linux 必备组件</span><span class="sxs-lookup"><span data-stu-id="4d537-156">Linux Prerequisites</span></span>

1. <span data-ttu-id="4d537-157">如果尚未安装 [Python](https://www.python.org/downloads)，请安装它。</span><span class="sxs-lookup"><span data-stu-id="4d537-157">If you don't have it, install [Python](https://www.python.org/downloads).</span></span>

2. <span data-ttu-id="4d537-158">根据你的 Linux 发行版，安装必备组件。</span><span class="sxs-lookup"><span data-stu-id="4d537-158">Depending on your Linux distribution, install the prerequisites.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install gcc libffi-devel python-devel openssl-devel
   ```

## <a name="troubleshooting"></a><span data-ttu-id="4d537-159">故障排除</span><span class="sxs-lookup"><span data-stu-id="4d537-159">Troubleshooting</span></span>

### <a name="errors-with-curl-redirection"></a><span data-ttu-id="4d537-160">有关 curl 重定向的错误</span><span class="sxs-lookup"><span data-stu-id="4d537-160">Errors with curl redirection</span></span>

<span data-ttu-id="4d537-161">如果从有关 `-L` 参数的 `curl` 命令收到错误，或者收到说明“对象已移动”的错误，请尝试使用完整 url 而不是 aka.ms url：</span><span class="sxs-lookup"><span data-stu-id="4d537-161">If you get an error from the `curl` command regarding the `-L` parameter, or an error saying "Object Moved", try using the full url instead of the aka.ms url:</span></span>

```
# If you see this:
curl -L https://aka.ms/InstallAzureCli | bash
  % Total    % Received % Xferd  Average Speed   Time    Time     Time  Current
                                 Dload  Upload   Total   Spent    Left  Speed
100   175  100   175    0     0    562      0 --:--:-- --:--:-- --:--:--   560
bash: line 1: syntax error near unexpected token `<'
'ash: line 1: `<html><head><title>Object moved</title></head><body>

#### Try this instead:
curl https://azurecliprod.blob.core.windows.net/install | bash
```

## <a name="uninstall"></a><span data-ttu-id="4d537-162">卸载</span><span class="sxs-lookup"><span data-stu-id="4d537-162">Uninstall</span></span>

<span data-ttu-id="4d537-163">如果使用了 https://aka.ms/InstallAzureCli 上的脚本安装 CLI，可以通过这些步骤来卸载它。</span><span class="sxs-lookup"><span data-stu-id="4d537-163">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="4d537-164">删除已安装的文件。</span><span class="sxs-lookup"><span data-stu-id="4d537-164">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="4d537-165">从 `<install location>/.bash_profile` 删除行 `<install location>/lib/azure-cli/az.completion`。</span><span class="sxs-lookup"><span data-stu-id="4d537-165">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="4d537-166">默认安装位置是 `/Users/<username>`。</span><span class="sxs-lookup"><span data-stu-id="4d537-166">The default install location is `/Users/<username>`.</span></span>

<span data-ttu-id="4d537-167">如果使用了 apt-get、Docker 或 msi 安装 CLI，请使用相同的工具卸载。</span><span class="sxs-lookup"><span data-stu-id="4d537-167">If you used apt-get, Docker, or the msi to install the CLI, use the same tool to uninstall it.</span></span>

## <a name="reporting-issues-and-feedback"></a><span data-ttu-id="4d537-168">报告问题和反馈</span><span class="sxs-lookup"><span data-stu-id="4d537-168">Reporting issues and feedback</span></span>

<span data-ttu-id="4d537-169">如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-cli/issues)部分中提出问题。</span><span class="sxs-lookup"><span data-stu-id="4d537-169">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repo.</span></span>
<span data-ttu-id="4d537-170">若要从命令行提供反馈，请尝试 `az feedback` 命令。</span><span class="sxs-lookup"><span data-stu-id="4d537-170">To provide feedback from the command line, try the `az feedback` command.</span></span>
