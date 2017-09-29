---
title: "安装 Azure CLI 2.0"
description: "有关安装 Azure CLI 2.0 的参考文档"
keywords: "Azure CLI,安装 Azure CLI,Azure Python CLI,Azure CLI 参考"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 08/17/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 935814d56d0a6be00f626da860dc643adbf14804
ms.sourcegitcommit: 9f38efbb7efd800ee5cab80d6641770d268c5a68
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/22/2017
---
# <a name="install-azure-cli-20"></a><span data-ttu-id="62efc-104">安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="62efc-104">Install Azure CLI 2.0</span></span>

<span data-ttu-id="62efc-105">现在就安装新版本的 Azure CLI！</span><span class="sxs-lookup"><span data-stu-id="62efc-105">Install the new version of the Azure CLI today!</span></span>
<span data-ttu-id="62efc-106">我们已改进并更新了 Azure CLI，以提供用于管理 Azure 资源的卓越本机命令行体验。</span><span class="sxs-lookup"><span data-stu-id="62efc-106">We've improved and updated it to provide a great native command-line experience for managing Azure resources.</span></span>
<span data-ttu-id="62efc-107">它可以在 macOS、Linux 和 Windows 上使用。</span><span class="sxs-lookup"><span data-stu-id="62efc-107">It can be used on macOS, Linux, and Windows.</span></span>
<span data-ttu-id="62efc-108">有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="62efc-108">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

> [!NOTE]
> <span data-ttu-id="62efc-109">如果需要早期版本的 Azure CLI，请参阅[如何安装 Azure CLI 1.0](/azure/cli-install-nodejs)。</span><span class="sxs-lookup"><span data-stu-id="62efc-109">If you need the previous version of the Azure CLI, here's how to [install Azure CLI 1.0](/azure/cli-install-nodejs).</span></span>

## <a name="a-namemacosinstall-on-macos"></a><span data-ttu-id="62efc-110"><a name="macOS"/>在 macOS 上安装</span><span class="sxs-lookup"><span data-stu-id="62efc-110"><a name="macOS"/>Install on macOS</span></span>

<span data-ttu-id="62efc-111">在 macOS 上，将能够使用 [Homebrew](https://brew.sh/) 安装或手动安装。</span><span class="sxs-lookup"><span data-stu-id="62efc-111">On macOS, you are able to install either with [Homebrew](https://brew.sh/) or manually.</span></span>

### <a name="install-with-homebrew"></a><span data-ttu-id="62efc-112">使用 Homebrew 安装</span><span class="sxs-lookup"><span data-stu-id="62efc-112">Install with Homebrew</span></span>

1. <span data-ttu-id="62efc-113">如果尚未安装 Homebrew，请按照 [Homebrew 安装说明](https://docs.brew.sh/Installation.html)进行安装。</span><span class="sxs-lookup"><span data-stu-id="62efc-113">If you don't have it already, install Homebrew by following the [Homebrew installation instructions](https://docs.brew.sh/Installation.html).</span></span>

2. <span data-ttu-id="62efc-114">如果以前手动安装了 CLI，请按照[手动卸载](#UninstallManually)说明执行操作。</span><span class="sxs-lookup"><span data-stu-id="62efc-114">If you have previously installed the CLI manually, follow the [manual uninstall](#UninstallManually) instructions.</span></span>

3. <span data-ttu-id="62efc-115">更新本地 Homebrew 存储库。</span><span class="sxs-lookup"><span data-stu-id="62efc-115">Update your local Homebrew repositories.</span></span>

   ```bash
   brew update
   ```

4. <span data-ttu-id="62efc-116">安装 `azure-cli` 包。</span><span class="sxs-lookup"><span data-stu-id="62efc-116">Install the `azure-cli` package.</span></span>

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> <span data-ttu-id="62efc-117">如果以前使用 Homebrew 安装了 Azure CLI 1.0，而不是安装该包，则可以通过常规 Homebrew 升级过程获取 CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="62efc-117">If you previously installed the Azure CLI 1.0 with Homebrew, instead of installing the package you can get CLI 2.0 through the regular Homebrew upgrade process.</span></span>
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a><span data-ttu-id="62efc-118">手动安装</span><span class="sxs-lookup"><span data-stu-id="62efc-118">Install manually</span></span>

1. <span data-ttu-id="62efc-119">安装包含 `curl` 的 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="62efc-119">Install Azure CLI 2.0 with `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. <span data-ttu-id="62efc-120">可能需要重启 shell，某些更改才会生效。</span><span class="sxs-lookup"><span data-stu-id="62efc-120">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```
   
3. <span data-ttu-id="62efc-121">在命令提示符下使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-121">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-windows"></a><span data-ttu-id="62efc-122">在 Windows 上安装</span><span class="sxs-lookup"><span data-stu-id="62efc-122">Install on Windows</span></span>

### <a name="install-with-msi-for-the-windows-command-line"></a><span data-ttu-id="62efc-123">使用适用于 Windows 命令行的 MSI 安装</span><span class="sxs-lookup"><span data-stu-id="62efc-123">Install with MSI for the Windows command-line</span></span> 

<span data-ttu-id="62efc-124">若要在 Windows 上安装 CLI 并在 Windows 命令行中使用它，请下载并运行 [Azure CLI 安装程序 (MSI)](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="62efc-124">To install the CLI on Windows and use it in the Windows command-line, download and run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows).</span></span>

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a><span data-ttu-id="62efc-125">使用适用于 Windows 中的 Bash on Ubuntu 的 apt-get 安装</span><span class="sxs-lookup"><span data-stu-id="62efc-125">Install with apt-get for Bash on Ubuntu on Windows</span></span>

1. <span data-ttu-id="62efc-126">如果 Windows 上没有 Bash，请[安装它](https://msdn.microsoft.com/commandline/wsl/install_guide)。</span><span class="sxs-lookup"><span data-stu-id="62efc-126">If you don't have Bash on Windows, [install it](https://msdn.microsoft.com/commandline/wsl/install_guide).</span></span>

2. <span data-ttu-id="62efc-127">打开 Bash Shell。</span><span class="sxs-lookup"><span data-stu-id="62efc-127">Open the Bash shell.</span></span>

3. <span data-ttu-id="62efc-128">修改源列表。</span><span class="sxs-lookup"><span data-stu-id="62efc-128">Modify your sources list.</span></span>

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. <span data-ttu-id="62efc-129">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="62efc-129">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  <span data-ttu-id="62efc-130">在命令提示符下使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-130">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-debianubuntu-with-apt-get"></a><span data-ttu-id="62efc-131">使用 apt-get 在 Debian/Ubuntu 上安装</span><span class="sxs-lookup"><span data-stu-id="62efc-131">Install on Debian/Ubuntu with apt-get</span></span>

<span data-ttu-id="62efc-132">对于基于 Debian/Ubuntu 的系统，可以通过 `apt-get` 安装 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="62efc-132">For Debian/Ubuntu based systems, you can install Azure CLI 2.0 via `apt-get`.</span></span>

1. <span data-ttu-id="62efc-133">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="62efc-133">Modify your sources list:</span></span>
 
   - <span data-ttu-id="62efc-134">32 位系统</span><span class="sxs-lookup"><span data-stu-id="62efc-134">32-bit system</span></span>

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - <span data-ttu-id="62efc-135">64 位系统</span><span class="sxs-lookup"><span data-stu-id="62efc-135">64-bit system</span></span>

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="62efc-136">运行以下 sudo 命令：</span><span class="sxs-lookup"><span data-stu-id="62efc-136">Run the following sudo commands:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  <span data-ttu-id="62efc-137">在命令提示符下使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-137">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-rhel-fedora-and-centos-with-yum"></a><span data-ttu-id="62efc-138">使用 yum 在 RHEL、Fedora 和 CentOS 上安装</span><span class="sxs-lookup"><span data-stu-id="62efc-138">Install on RHEL, Fedora, and CentOS with yum</span></span>

<span data-ttu-id="62efc-139">对于任何基于 RedHat 且包含 `yum` 包管理器的分发版，可以通过 `yum` 安装 Azure CLI 2.0。</span><span class="sxs-lookup"><span data-stu-id="62efc-139">For any distribution which is based off of RedHat and contains the `yum` package manager, you can install Azure CLI 2.0 via `yum`.</span></span>

1. <span data-ttu-id="62efc-140">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="62efc-140">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="62efc-141">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="62efc-141">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="62efc-142">更新 `yum` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="62efc-142">Update the `yum` package index and install:</span></span>

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. <span data-ttu-id="62efc-143">在命令提示符下使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-143">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-on-opensuse-and-sle-with-zypper"></a><span data-ttu-id="62efc-144">在 openSUSE 和 SLE 上使用 zypper 安装</span><span class="sxs-lookup"><span data-stu-id="62efc-144">Install on openSUSE and SLE with zypper</span></span>

1. <span data-ttu-id="62efc-145">导入 Microsoft 存储库密钥：</span><span class="sxs-lookup"><span data-stu-id="62efc-145">Import the Microsoft repository key:</span></span>

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. <span data-ttu-id="62efc-146">创建本地 `azure-cli` 存储库信息：</span><span class="sxs-lookup"><span data-stu-id="62efc-146">Create local `azure-cli` repository information:</span></span>

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. <span data-ttu-id="62efc-147">更新 `zypper` 包索引并安装：</span><span class="sxs-lookup"><span data-stu-id="62efc-147">Update the `zypper` package index and install:</span></span>

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. <span data-ttu-id="62efc-148">在命令提示符下使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-148">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="install-with-docker"></a><span data-ttu-id="62efc-149">使用 Docker 安装</span><span class="sxs-lookup"><span data-stu-id="62efc-149">Install with Docker</span></span>

<span data-ttu-id="62efc-150">我们维护预先配置了 Azure CLI 2.0 的 Docker 映像。</span><span class="sxs-lookup"><span data-stu-id="62efc-150">We maintain a Docker image preconfigured with the Azure CLI 2.0.</span></span>

<span data-ttu-id="62efc-151">请使用 `docker run` 安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-151">Install the CLI using `docker run`.</span></span>

   ```bash
   docker run azuresdk/azure-cli-python:<version>
   ```

<span data-ttu-id="62efc-152">请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。</span><span class="sxs-lookup"><span data-stu-id="62efc-152">See our [Docker tags](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/) for available versions.</span></span>

<span data-ttu-id="62efc-153">CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。</span><span class="sxs-lookup"><span data-stu-id="62efc-153">The CLI is installed on the image as the `az` command in `/usr/local/bin`.</span></span>

> [!NOTE]
> <span data-ttu-id="62efc-154">如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。</span><span class="sxs-lookup"><span data-stu-id="62efc-154">If you want to pick up the SSH keys from your user environment, you can use `-v ${HOME}:/root` to mount $HOME as `/root`.</span></span>

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><span data-ttu-id="62efc-155"><a name="Linux"/>不使用 apt-get 在 Linux 上安装</span><span class="sxs-lookup"><span data-stu-id="62efc-155"><a name="Linux"/>Install on Linux without apt-get</span></span>

<span data-ttu-id="62efc-156">建议在可能的情况下使用包管理器安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-156">It is recommended that you install the CLI with a package manager if you are able to.</span></span> <span data-ttu-id="62efc-157">对于未提供包的分发版，可以手动安装。</span><span class="sxs-lookup"><span data-stu-id="62efc-157">For distributions which do not have a package provided for them, you can manually install.</span></span>

1. <span data-ttu-id="62efc-158">根据 Linux 分发版安装必备组件。</span><span class="sxs-lookup"><span data-stu-id="62efc-158">Install the prerequisites based on your Linux distribution.</span></span>

   ```
   Platform              | Prerequisites
   ----------------------|---------------------------------------------
   Ubuntu 15.10 or 16.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Ubuntu 12.04 or 14.04 | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   Debian 8              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev build-essential
   Debian 7              | sudo apt-get update && sudo apt-get install -y python libssl-dev libffi-dev python-dev
   CentOS 7.1 or 7.2     | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   RedHat 7.2            | sudo yum check-update; sudo yum install -y gcc python libffi-devel python-devel openssl-devel
   SUSE OpenSUSE 13.2    | sudo zypper refresh && sudo zypper --non-interactive install curl gcc python python-xml libffi-devel python-devel openssl-devel
   ```

<span data-ttu-id="62efc-159">如果上面未列出你的分发版，则需要安装 [Python](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL](https://www.openssl.org/source/)。</span><span class="sxs-lookup"><span data-stu-id="62efc-159">If your distribution is not listed above, you will need to install [Python](https://www.python.org/downloads/), [libffi](https://sourceware.org/libffi/), and [OpenSSL](https://www.openssl.org/source/).</span></span>

2. <span data-ttu-id="62efc-160">请使用 `curl` 安装 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-160">Install the CLI with  `curl`.</span></span>

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. <span data-ttu-id="62efc-161">可能需要重启 shell，某些更改才会生效。</span><span class="sxs-lookup"><span data-stu-id="62efc-161">You may have to restart your shell for some changes to take effect.</span></span>

   ```bash
   exec -l $SHELL
   ```

4. <span data-ttu-id="62efc-162">在命令提示符下使用 `az` 命令运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-162">Run the CLI from the command prompt with the `az` command.</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="62efc-163">故障排除</span><span class="sxs-lookup"><span data-stu-id="62efc-163">Troubleshooting</span></span>

<span data-ttu-id="62efc-164">如果在安装 CLI 过程中遇到问题，请查看本部分是否包括具体的问题。</span><span class="sxs-lookup"><span data-stu-id="62efc-164">If you encounter an issue during CLI install, check this section to see if your particular case is covered.</span></span> <span data-ttu-id="62efc-165">如果本部分未列出该问题，请[提出 Github 问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="62efc-165">If your issue is not here, please [file a Github issue](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="curl-object-moved-error"></a><span data-ttu-id="62efc-166">curl“对象已移动”错误</span><span class="sxs-lookup"><span data-stu-id="62efc-166">curl "Object Moved" error</span></span>

<span data-ttu-id="62efc-167">如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：</span><span class="sxs-lookup"><span data-stu-id="62efc-167">If you get an error from `curl` related to the `-L` parameter, or an error message including the text "Object Moved", try using the full URL instead of the `aka.ms` redirect:</span></span>

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="az-command-not-found"></a><span data-ttu-id="62efc-168">找不到 `az` 命令</span><span class="sxs-lookup"><span data-stu-id="62efc-168">`az` command not found</span></span>

<span data-ttu-id="62efc-169">可能需要清除 shell 的命令哈希缓存。</span><span class="sxs-lookup"><span data-stu-id="62efc-169">You may need to clear your shell's command hash cache.</span></span> <span data-ttu-id="62efc-170">运行</span><span class="sxs-lookup"><span data-stu-id="62efc-170">Run</span></span>

```bash
hash -r
```

<span data-ttu-id="62efc-171">并查看问题是否得以解决。</span><span class="sxs-lookup"><span data-stu-id="62efc-171">and see if the problem is resolved.</span></span>

## <a name="uninstall-cli-1x-versions"></a><span data-ttu-id="62efc-172">卸载 CLI 1.x 版本</span><span class="sxs-lookup"><span data-stu-id="62efc-172">Uninstall CLI 1.x versions</span></span>

<span data-ttu-id="62efc-173">如果系统上安装了早期的 CLI 1.x 版本，可以根据所用的安装类型卸载它。</span><span class="sxs-lookup"><span data-stu-id="62efc-173">If you have an earlier CLI 1.x version available on your system, you can uninstall it based upon the type of install used.</span></span>

### <a name="uninstall-with-npm"></a><span data-ttu-id="62efc-174">使用 npm 卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-174">Uninstall with npm</span></span>

<span data-ttu-id="62efc-175">使用 `npm uninstall` 删除旧版 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-175">Remove the older CLI with `npm uninstall`.</span></span>

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a><span data-ttu-id="62efc-176">使用分发版卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-176">Uninstall with distributable</span></span>

<span data-ttu-id="62efc-177">如果是通过 [Azure CLI 安装程序 (MSI)](http://aka.ms/webpi-azure-cli) 或 [macOS 包](http://aka.ms/mac-azure-cli)安装的，请使用相同的工具删除安装。</span><span class="sxs-lookup"><span data-stu-id="62efc-177">If you installed via the [Azure CLI Installer (MSI)](http://aka.ms/webpi-azure-cli) or a [macOS package](http://aka.ms/mac-azure-cli), use the same tool to remove your install.</span></span>

### <a name="uninstall-with-docker"></a><span data-ttu-id="62efc-178">使用 Docker 卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-178">Uninstall with Docker</span></span>

<span data-ttu-id="62efc-179">如果安装了 Docker 映像来使用早期的 CLI 版本，请删除该映像和所有关联的容器。</span><span class="sxs-lookup"><span data-stu-id="62efc-179">If you installed a Docker image to use the earlier CLI version, remove that image and any associated containers.</span></span> <span data-ttu-id="62efc-180">然后，可以根据安装说明中所述，在安装新的 Docker 映像后重新创建容器。</span><span class="sxs-lookup"><span data-stu-id="62efc-180">You can then re-create the containers after installing the new Docker image as described in the install instructions.</span></span>

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a><span data-ttu-id="62efc-181">更新 CLI</span><span class="sxs-lookup"><span data-stu-id="62efc-181">Update the CLI</span></span>

<span data-ttu-id="62efc-182">若要更新 Azure CLI，请使用安装时所用的相同方法。</span><span class="sxs-lookup"><span data-stu-id="62efc-182">To update the Azure CLI, use the same method that you used to install it.</span></span>

### <a name="update-with-homebrew"></a><span data-ttu-id="62efc-183">使用 Homebrew 更新</span><span class="sxs-lookup"><span data-stu-id="62efc-183">Update with Homebrew</span></span>

1. <span data-ttu-id="62efc-184">如果以前手动进行了安装，请按照[使用 Homebrew 安装](#macOS)说明执行操作。</span><span class="sxs-lookup"><span data-stu-id="62efc-184">If you previously installed manually, follow the [install with Homebrew](#macOS) instructions.</span></span>

2. <span data-ttu-id="62efc-185">更新本地 Homebrew 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="62efc-185">Update your local Homebrew repository information.</span></span>

   ```bash
   brew update
   ```

3. <span data-ttu-id="62efc-186">升级已安装的包。</span><span class="sxs-lookup"><span data-stu-id="62efc-186">Upgrade your installed packages.</span></span>

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a><span data-ttu-id="62efc-187">使用 MSI 更新</span><span class="sxs-lookup"><span data-stu-id="62efc-187">Update with MSI</span></span>

<span data-ttu-id="62efc-188">再次运行 [Azure CLI 安装程序 (MSI)](https://aka.ms/InstallAzureCliWindows)。</span><span class="sxs-lookup"><span data-stu-id="62efc-188">Run the [Azure CLI Installer (MSI)](https://aka.ms/InstallAzureCliWindows) again.</span></span>

### <a name="update-with-apt-get"></a><span data-ttu-id="62efc-189">使用 apt-get 更新</span><span class="sxs-lookup"><span data-stu-id="62efc-189">Update with apt-get</span></span>

<span data-ttu-id="62efc-190">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="62efc-190">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="62efc-191">这会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="62efc-191">This will upgrade all of the installed packages on your system which have not had a dependency change.</span></span>
> <span data-ttu-id="62efc-192">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="62efc-192">To upgrade only the CLI, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a><span data-ttu-id="62efc-193">使用 Docker 更新</span><span class="sxs-lookup"><span data-stu-id="62efc-193">Update with Docker</span></span>

1. <span data-ttu-id="62efc-194">使用 `docker pull` 更新本地映像。</span><span class="sxs-lookup"><span data-stu-id="62efc-194">Update your local image with `docker pull`.</span></span>

   ```bash
   docker pull azuresdk/azure-cli-python
   ```

2. <span data-ttu-id="62efc-195">获取当前正在使用 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="62efc-195">Get the containers currently using the CLI image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

> [!NOTE]
> <span data-ttu-id="62efc-196">如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。</span><span class="sxs-lookup"><span data-stu-id="62efc-196">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

3. <span data-ttu-id="62efc-197">停止并重新创建容器。</span><span class="sxs-lookup"><span data-stu-id="62efc-197">Halt and recreate the containers.</span></span>

   ```bash
   docker stop inspiring_benz
   docker rm inspiring_benz
   docker run azuresdk/azure-cli-python
   ```

### <a name="update-manually"></a><span data-ttu-id="62efc-198">手动更新</span><span class="sxs-lookup"><span data-stu-id="62efc-198">Update manually</span></span>

<span data-ttu-id="62efc-199">遵照适用于 [macOS](#macOS) 或 [Linux](#Linux) 的手动安装说明进行更新。</span><span class="sxs-lookup"><span data-stu-id="62efc-199">Follow the manual installation instructions for [macOS](#macOS) or [Linux](#Linux) to update.</span></span>

## <a name="uninstall"></a><span data-ttu-id="62efc-200">卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-200">Uninstall</span></span>

<span data-ttu-id="62efc-201">我们会很遗憾看到你卸载 CLI。</span><span class="sxs-lookup"><span data-stu-id="62efc-201">If you decide to uninstall the CLI, we're sorry to see you go.</span></span> <span data-ttu-id="62efc-202">应使用安装 CLI 时所用的相同方法进行卸载。</span><span class="sxs-lookup"><span data-stu-id="62efc-202">You should uninstall using the same method that you used to install the CLI.</span></span>

### <a name="uninstall-with-homebrew"></a><span data-ttu-id="62efc-203">使用 Homebrew 卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-203">Uninstall with Homebrew</span></span>

<span data-ttu-id="62efc-204">卸载 `azure-cli` 包。</span><span class="sxs-lookup"><span data-stu-id="62efc-204">Uninstall the `azure-cli` package.</span></span>

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a><span data-ttu-id="62efc-205">使用 MSI 卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-205">Uninstall with MSI</span></span>

<span data-ttu-id="62efc-206">再次运行 [MSI](https://aka.ms/InstallAzureCliWindows) 并选择“卸载”。</span><span class="sxs-lookup"><span data-stu-id="62efc-206">Run the [MSI](https://aka.ms/InstallAzureCliWindows) again and choose uninstall.</span></span>

### <a name="uninstall-with-apt-get"></a><span data-ttu-id="62efc-207">使用 apt-get 卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-207">Uninstall with apt-get</span></span>

<span data-ttu-id="62efc-208">通过 `apt-get remove` 卸载：</span><span class="sxs-lookup"><span data-stu-id="62efc-208">Uninstall via `apt-get remove`:</span></span>

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a><span data-ttu-id="62efc-209">使用 Docker 卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-209">Uninstall with Docker</span></span>

<span data-ttu-id="62efc-210">如果安装了 Docker 映像，需要删除运行该映像的所有容器，然后删除本地映像。</span><span class="sxs-lookup"><span data-stu-id="62efc-210">If you installed a docker image, you will need to remove any containers running it, and then delete the local image.</span></span>

1. <span data-ttu-id="62efc-211">获取正在运行 azure-cli 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="62efc-211">Get the containers which are running the azure-cli image.</span></span>

   ```bash
   docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
   ```

   ```output
   CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
   34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
   ```

2. <span data-ttu-id="62efc-212">删除所有包含 CLI 映像的容器。</span><span class="sxs-lookup"><span data-stu-id="62efc-212">Delete any containers with the CLI image.</span></span>

   ```bash
   docker rm 34a868beb2ab
   ```

3. <span data-ttu-id="62efc-213">删除本地安装的 CLI 映像。</span><span class="sxs-lookup"><span data-stu-id="62efc-213">Remove the locally installed CLI image.</span></span>

   ```bash
   docker rmi azuresdk/azure-cli-python
   ```

> [!NOTE]
> <span data-ttu-id="62efc-214">如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。</span><span class="sxs-lookup"><span data-stu-id="62efc-214">If you installed a specific version of the image, you will need to add `:<version>` to the end of the image name.</span></span>

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><span data-ttu-id="62efc-215"><a name="UninstallManually"/>手动卸载</span><span class="sxs-lookup"><span data-stu-id="62efc-215"><a name="UninstallManually"/>Uninstall manually</span></span>

<span data-ttu-id="62efc-216">如果使用了 https://aka.ms/InstallAzureCli 上的脚本安装 CLI，可以通过这些步骤来卸载它。</span><span class="sxs-lookup"><span data-stu-id="62efc-216">If you used the script at https://aka.ms/InstallAzureCli to install the CLI, you can uninstall it with these steps.</span></span>

1. <span data-ttu-id="62efc-217">删除已安装的文件。</span><span class="sxs-lookup"><span data-stu-id="62efc-217">Remove the installed files.</span></span>

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. <span data-ttu-id="62efc-218">从 `<install location>/.bash_profile` 删除行 `<install location>/lib/azure-cli/az.completion`。</span><span class="sxs-lookup"><span data-stu-id="62efc-218">Delete the line `<install location>/lib/azure-cli/az.completion` from `<install location>/.bash_profile`.</span></span>

> [!Note]
> <span data-ttu-id="62efc-219">默认安装位置是 `/Users/<username>`。</span><span class="sxs-lookup"><span data-stu-id="62efc-219">The default install location is `/Users/<username>`.</span></span>

## <a name="report-cli-issues-and-feedback"></a><span data-ttu-id="62efc-220">报告 CLI 问题和反馈</span><span class="sxs-lookup"><span data-stu-id="62efc-220">Report CLI issues and feedback</span></span>

<span data-ttu-id="62efc-221">如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-cli/issues)部分中提出问题。</span><span class="sxs-lookup"><span data-stu-id="62efc-221">If you encounter any bugs with the tool, file an issue in the [Issues](https://github.com/Azure/azure-cli/issues) section of our GitHub repository.</span></span>
<span data-ttu-id="62efc-222">若要从命令行提供反馈，请使用 `az feedback` 命令。</span><span class="sxs-lookup"><span data-stu-id="62efc-222">To provide feedback from the command line, use the `az feedback` command.</span></span>
