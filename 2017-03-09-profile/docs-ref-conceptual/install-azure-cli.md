---
title: "安装 Azure CLI 2.0"
description: "有关安装 Azure CLI 2.0 的参考文档"
keywords: "Azure CLI 2.0, Azure CLI 2.0 参考, 安装 Azure CLI 2.0, Azure Python CLI, 卸载 Azure CLI 2.0, Azure CLI, 安装 Azure CLI, Azure CLI 参考"
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
ms.openlocfilehash: 00d5b555975007d7e57f04ce5d69f4f29e6d0219
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2017
---
# <a name="install-azure-cli-20"></a>安装 Azure CLI 2.0

现在就安装新版本的 Azure CLI！
我们已改进并更新了 Azure CLI，以提供用于管理 Azure 资源的卓越本机命令行体验。
它可以在 macOS、Linux 和 Windows 上使用。
有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

> [!NOTE]
> 如果需要早期版本的 Azure CLI，请参阅[如何安装 Azure CLI 1.0](/azure/cli-install-nodejs)。

## <a name="a-namemacosinstall-on-macos"></a><a name="macOS"/>在 macOS 上安装

1. 安装包含 `curl` 的 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 可能需要重启 shell，某些更改才会生效。

   ```bash
   exec -l $SHELL
   ```
   
3. 在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-on-windows"></a>在 Windows 上安装

可使用 MSI 安装 Azure CLI 2.0 并在 Windows 命令行中使用它，或者可以在 Windows 中的 Bash on Ubuntu 上使用 `apt-get` 来安装 CLI。

### <a name="install-with-msi-for-the-windows-command-line"></a>使用适用于 Windows 命令行的 MSI 安装 

若要在 Windows 上安装 CLI 并在 Windows 命令行中使用它，请下载并运行 [MSI](https://aka.ms/InstallAzureCliWindows)。

### <a name="install-with-apt-get-for-bash-on-ubuntu-on-windows"></a>使用适用于 Windows 中的 Bash on Ubuntu 的 apt-get 安装

1. 如果 Windows 上没有 Bash，请[安装它](https://msdn.microsoft.com/commandline/wsl/install_guide)。

2. 打开 Bash Shell。

3. 修改源列表。

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

4. 运行以下 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-on-debianubuntu-with-apt-get"></a>使用 apt-get 在 Debian/Ubuntu 上安装

对于基于 Debian/Ubuntu 的系统，可以通过 `apt-get` 安装 Azure CLI 2.0。

1. 修改源列表。
 
   - 32 位系统

     ```bash
     echo "deb https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

   - 64 位系统

     ```bash
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. 运行以下 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-with-docker"></a>使用 Docker 安装

我们维护预先配置了 Azure CLI 2.0 的 Docker 映像。

请使用 `docker run` 安装 CLI。

  ```bash
  docker run azuresdk/azure-cli-python:<version>
  ```

请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。

CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。

> [!NOTE]
> 如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。

> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

## <a name="a-namelinuxinstall-on-linux-without-apt-get"></a><a name="Linux"/>不使用 apt-get 在 Linux 上安装

建议在可能的情况下使用 `apt-get` 安装 CLI。 对于不使用 `apt` 包管理器的分发版，可以手动安装。

1. 根据 Linux 分发版安装必备组件。

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

如果上面未列出你的分发版，则需要安装 [Python](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL](https://www.openssl.org/source/)。

2. 请使用 `curl` 安装 CLI。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. 可能需要重启 shell，某些更改才会生效。

   ```bash
   exec -l $SHELL
   ```

4. 在命令提示符下使用 `az` 命令运行 CLI。

## <a name="troubleshooting"></a>故障排除

如果在安装 CLI 过程中遇到问题，请查看本部分是否包括具体的问题。 如果本部分未列出该问题，请[提出 Github 问题](https://github.com/Azure/azure-cli/issues)。

### <a name="curl-object-moved-error"></a>curl“对象已移动”错误

如果从有关 `-L` 参数的 `curl` 收到错误，或者收到包含“对象已移动”的错误消息，请尝试使用完整 URL 而不是 `aka.ms` 重定向：

```bash
curl https://azurecliprod.blob.core.windows.net/install | bash
```

### <a name="homebrew-on-macos-installing-older-version"></a>装有旧版本的 Homebrew on macOS

适用于 macOS 的 Homebrew `azure-cli` 公式目前已过期，将安装 1.x 版 CLI。 可以通过检查 `brew info azure-cli` 了解 CLI 是何时更新的。

然后，可以[卸载旧版本](#uninstall_brew)并遵照 [macOS 安装说明](#macOS)。

## <a name="uninstall-cli-1x-versions"></a>卸载 CLI 1.x 版本

如果系统上安装了早期的 CLI 1.x 版本，可以根据所用的安装类型卸载它。

### <a name="uninstall-with-npm"></a>使用 npm 卸载

使用 `npm uninstall` 删除旧版 CLI。

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="a-nameuninstallbrewuninstall-with-homebrew-on-macos"></a><a name="uninstall_brew"/>使用 Homebrew on macOS 卸载

使用 `brew uninstall` 删除旧版 CLI。

```bash
brew uninstall azure-cli
```

### <a name="uninstall-with-distributable"></a>使用分发版卸载

如果是通过 [MSI](http://aka.ms/webpi-azure-cli) 或 [macOS 包](http://aka.ms/mac-azure-cli)安装的，请使用相同的工具删除安装。

### <a name="uninstall-with-docker"></a>使用 Docker 卸载

如果安装了 Docker 映像来使用早期的 CLI 版本，请删除该映像和所有关联的容器。 然后，可以根据安装说明中所述，在安装新的 Docker 映像后重新创建容器。

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a>更新 CLI

若要更新 Azure CLI，请使用安装时所用的相同方法。

### <a name="update-with-msi"></a>使用 MSI 更新

再次运行 [MSI](https://aka.ms/InstallAzureCliWindows)。

### <a name="update-with-apt-get"></a>使用 apt-get 更新

使用 `apt-get upgrade` 更新 CLI 包。

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> 这会升级系统上所有未发生依赖关系更改的已安装包。
> 若只要升级 CLI，请使用 `apt-get install`。
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

### <a name="update-with-docker"></a>使用 Docker 更新

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

### <a name="update-manually"></a>手动更新

遵照适用于 [macOS](#macOS) 或 [Linux](#Linux) 的手动安装说明进行更新。

## <a name="uninstall"></a>卸载

我们会很遗憾看到你卸载 CLI。 应使用安装 CLI 时所用的相同方法进行卸载。

### <a name="uninstall-with-msi"></a>使用 MSI 卸载

再次运行 [MSI](https://aka.ms/InstallAzureCliWindows) 并选择“卸载”。

### <a name="uninstall-with-apt-get"></a>使用 apt-get 卸载

通过 `apt-get remove` 卸载：

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-docker"></a>使用 Docker 卸载

如果安装了 Docker 映像，需要删除运行该映像的所有容器，然后删除本地映像。

1. 获取正在运行 azure-cli 映像的容器。

  ```bash
  docker container ls -a --filter 'ancestor=azuresdk/azure-cli-python'
  ```

  ```output
  CONTAINER ID        IMAGE                              COMMAND             CREATED             STATUS                        PORTS               NAMES
  34a868beb2ab        azuresdk/azure-cli-python:latest      "/bin/sh -c bash"   8 minutes ago       Exited (0) 8 minutes ago                       inspiring_benz
  ```

2. 删除所有包含 CLI 映像的容器。

  ```bash
  docker rm 34a868beb2ab
  ```

3. 删除本地安装的 CLI 映像。

  ```bash
  docker rmi azuresdk/azure-cli-python
  ```

> [!NOTE]
> 如果安装了特定版本的映像，需在映像名称的末尾添加 `:<version>`。

### <a name="uninstall-manually"></a>手动卸载

如果使用了 https://aka.ms/InstallAzureCli 上的脚本安装 CLI，可以通过这些步骤来卸载它。

1. 删除已安装的文件。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. 从 `<install location>/.bash_profile` 删除行 `<install location>/lib/azure-cli/az.completion`。

> [!Note]
> 默认安装位置是 `/Users/<username>`。

## <a name="report-cli-issues-and-feedback"></a>报告 CLI 问题和反馈

如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-cli/issues)部分中提出问题。
若要从命令行提供反馈，请使用 `az feedback` 命令。