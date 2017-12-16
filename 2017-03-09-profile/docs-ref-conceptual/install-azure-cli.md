---
title: "安装 Azure CLI 2.0"
description: "有关安装 Azure CLI 2.0 的参考文档"
keywords: "Azure CLI,安装 Azure CLI,Azure Python CLI,Azure CLI 参考"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 11/01/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 5a667ad8720100b45ff714601225535ef442545c
ms.sourcegitcommit: 2e4d0bdd94c626e061434883032367b5619de4fe
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 12/09/2017
---
# <a name="install-azure-cli-20"></a>安装 Azure CLI 2.0

现在就安装新版本的 Azure CLI！
我们已改进并更新了 Azure CLI，以提供用于管理 Azure 资源的卓越本机命令行体验。
它可以在 macOS、Linux 和 Windows 上使用。
有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

> [!NOTE]
> 如果使用的是 Azure 服务管理 (ASM) 模型，请[安装 Azure CLI 1.0](/azure/cli-install-nodejs)。

## <a name="a-namemacosinstall-on-macos"></a><a name="macOS"/>在 macOS 上安装

在 macOS 上，将能够使用 [Homebrew](https://brew.sh/) 安装或手动安装。

### <a name="install-with-homebrew"></a>使用 Homebrew 安装

1. 如果尚未安装 Homebrew，请按照 [Homebrew 安装说明](https://docs.brew.sh/Installation.html)进行安装。

2. 如果以前手动安装了 CLI，请按照[手动卸载](#UninstallManually)说明执行操作。

3. 更新本地 Homebrew 存储库。

   ```bash
   brew update
   ```

4. 安装 `azure-cli` 包。

  ```bash
  brew install azure-cli
  ```

> [!NOTE]
> 如果以前使用 Homebrew 安装了 Azure CLI 1.0，而不是安装该包，则可以通过常规 Homebrew 升级过程获取 CLI 2.0。
>
> ```bash
> brew upgrade
> ```

### <a name="install-manually"></a>手动安装

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

### <a name="install-with-msi-for-the-windows-command-line"></a>使用适用于 Windows 命令行的 MSI 安装

若要在 Windows 上安装 CLI 并在 Windows 命令行中使用它，请下载并运行 [Azure CLI 安装程序 (MSI)](https://aka.ms/InstallAzureCliWindows)。

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
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

5.  在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-with-apt-package-manager"></a>使用 apt 包管理器进行安装

对于使用 `apt` 包管理器的分发版（如 Ubuntu 或 Debian），可以通过 `apt-get` 安装 Azure CLI 2.0。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. 修改源列表：

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
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

3.  在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-with-yum-package-manager"></a>使用 yum 包管理器进行安装

对于使用 `yum` 包管理器的分发版，如 Red Hat Enterprise Linux (RHEL)、Fedora 或 CentOS，可以通过 `yum` 安装 Azure CLI 2.0。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. 导入 Microsoft 存储库密钥：

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. 创建本地 `azure-cli` 存储库信息：

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/yum.repos.d/azure-cli.repo'
   ```

3. 更新 `yum` 包索引并安装：

   ```bash
   yum check-update
   sudo yum install azure-cli
   ```

4. 在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-with-zypper-package-manager"></a>使用 zypper 包管理器进行安装

对于使用 `zypper` 包管理器的分发版（如 OpenSUSE 或 SLE），可以通过 `zypper` 安装 Azure CLI 2.0。

[!INCLUDE [linux-install-requirements.md](includes/linux-install-requirements.md)]

1. 导入 Microsoft 存储库密钥：

   ```bash
   sudo rpm --import https://packages.microsoft.com/keys/microsoft.asc
   ```

2. 创建本地 `azure-cli` 存储库信息：

   ```bash
   sudo sh -c 'echo -e "[azure-cli]\nname=Azure CLI\nbaseurl=https://packages.microsoft.com/yumrepos/azure-cli\nenabled=1\ntype=rpm-md\ngpgcheck=1\ngpgkey=https://packages.microsoft.com/keys/microsoft.asc" > /etc/zypp/repos.d/azure-cli.repo'
   ```

3. 更新 `zypper` 包索引并安装：

   ```bash
   sudo zypper refresh
   sudo zypper install azure-cli
   ```

4. 在命令提示符下使用 `az` 命令运行 CLI。

## <a name="install-with-docker"></a>使用 Docker 安装

我们维护预先配置了 Azure CLI 2.0 的 Docker 映像。

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

## <a name="a-namelinuxinstall-on-linux-without-a-package-manager"></a><a name="Linux"/>不使用包管理器在 Linux 上安装

建议在可能的情况下使用包管理器安装 CLI。 如果不想要添加 Microsoft 的存储库，或使用的是不包含随附包的分发版，可以手动安装 CLI。

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

如果上面未列出你的分发版，则需要安装 [Python 2.7 或更高版本](https://www.python.org/downloads/)、[libffi](https://sourceware.org/libffi/) 和 [OpenSSL 1.0.2](https://www.openssl.org/source/)。

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

### <a name="az-command-not-found"></a>找不到 `az` 命令

可能需要清除 shell 的命令哈希缓存。 运行

```bash
hash -r
```

并查看问题是否得以解决。 该命令也可能不在 `$PATH` 中。 请确保 `<install path>/bin` 出现在 `$PATH` 中，并重新启动 shell（如有必要）。

## <a name="uninstall-cli-1x-versions"></a>卸载 CLI 1.x 版本

如果系统上安装了早期的 CLI 1.x 版本，可以根据所用的安装类型卸载它。

### <a name="uninstall-with-npm"></a>使用 npm 卸载

使用 `npm uninstall` 删除旧版 CLI。

  ```bash
  npm uninstall -g azure-cli
  ```

### <a name="uninstall-with-distributable"></a>使用分发版卸载

如果是通过 [Azure CLI 安装程序 (MSI)](http://aka.ms/webpi-azure-cli) 或 [macOS 包](http://aka.ms/mac-azure-cli)安装的，请使用相同的工具删除安装。

### <a name="uninstall-with-docker"></a>使用 Docker 卸载

如果安装了 Docker 映像来使用早期的 CLI 版本，请删除该映像和所有关联的容器。 然后，可以根据安装说明中所述，在安装新的 Docker 映像后重新创建容器。

  ```bash
  docker rmi -f microsoft/azure-cli
  ```

## <a name="update-the-cli"></a>更新 CLI

若要更新 Azure CLI，请使用安装时所用的相同方法。

### <a name="update-with-homebrew"></a>使用 Homebrew 更新

1. 如果以前手动进行了安装，请按照[使用 Homebrew 安装](#macOS)说明执行操作。

2. 更新本地 Homebrew 存储库信息。

   ```bash
   brew update
   ```

3. 升级已安装的包。

   ```bash
   brew upgrade
   ```

### <a name="update-with-msi"></a>使用 MSI 更新

再次运行 [Azure CLI 安装程序 (MSI)](https://aka.ms/InstallAzureCliWindows)。

### <a name="update-with-apt"></a>使用 apt 进行更新

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

### <a name="update-with-yum"></a>使用 yum 进行更新

使用 `yum update` 命令更新 Azure CLI。

```bash
yum check-update
sudo yum update azure-cli
```

### <a name="update-with-zypper"></a>使用 zypper 进行更新

可以使用 `zypper update` 命令来更新包。

```bash
sudo zypper refresh
sudo zypper update azure-cli
```

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

### <a name="uninstall-with-homebrew"></a>使用 Homebrew 卸载

卸载 `azure-cli` 包。

   ```bash
   brew uninstall azure-cli
   ```

### <a name="uninstall-with-msi"></a>使用 MSI 卸载

再次运行 [MSI](https://aka.ms/InstallAzureCliWindows) 并选择“卸载”。

### <a name="uninstall-with-apt"></a>使用 apt 进行卸载

通过 `apt-get remove` 卸载：

  ```bash
  sudo apt-get remove -y azure-cli
  ```

### <a name="uninstall-with-yum"></a>使用 yum 进行卸载

1. 从系统中删除包。

   ```bash
   sudo yum remove azure-cli
   ```

2. 如果不打算重新安装 CLI，请删除存储库信息。

   ```bash
   sudo rm /etc/yum.repos.d/azure-cli.repo
   ```

3. 如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
  ```

### <a name="uninstall-with-zypper"></a>使用 zypper 进行卸载

1. 从系统中删除包。

    ```bash
    sudo zypper remove -y azure-cli
    ```

2. 如果不打算重新安装 CLI，请删除存储库信息。

  ```bash
  sudo rm /etc/zypp/repos.d/azure-cli.repo
  ```

3. 如果已删除存储库信息，还需删除 Microsoft GPG 签名密钥。

  ```bash
  MSFT_KEY=`rpm -qa gpg-pubkey /* --qf "%{version}-%{release} %{summary}\n" | grep Microsoft | awk '{print $1}'`
  rpm -e --allmatches gpg-pubkey-$MSFT_KEY
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

###<a name="a-nameuninstallmanuallyuninstall-manually"></a><a name="UninstallManually"/>手动卸载

如果使用了 https://aka.ms/InstallAzureCli 上的脚本安装 CLI，可以通过这些步骤来卸载它。

1. 删除已安装的文件。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. 从 `<install location>/.bash_profile` 删除行 `<install location>/lib/azure-cli/az.completion`。

3. 如果 shell 使用命令缓存，请重新加载它。

   ```bash
   hash -r
   ```

> [!Note]
> macOS 的默认安装位置为 `/Users/<username>`，Linux 的为 `/home/<username>`。

## <a name="report-cli-issues-and-feedback"></a>报告 CLI 问题和反馈

如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-cli/issues)部分中提出问题。
若要从命令行提供反馈，请使用 `az feedback` 命令。
