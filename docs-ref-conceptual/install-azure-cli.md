---
title: "安装 Azure CLI 2.0"
description: "用于安装 Azure CLI 2.0 的参考文档"
keywords: "Azure CLI 2.0, Azure CLI 2.0 参考, 安装 Azure CLI 2.0, Azure Python CLI, 卸载 Azure CLI 2.0"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 08/17/2017
ms.topic: "articleå"
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ea5c0ee1-c530-4a1e-a83f-e1be71f6d416
ms.openlocfilehash: 432edac070e238a6f1be0ccd76b9b3582b082219
ms.sourcegitcommit: 2ec80224c6b831e31038b710d912c0dbb1ddfef6
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 08/17/2017
---
# <a name="install-azure-cli-20"></a>安装 Azure CLI 2.0

现在就安装新版本的 Azure CLI！
我们已改进并更新了 Azure CLI，以提供用于管理 Azure 资源的卓越本机命令行体验。
它可以在 macOS、Linux 和 Windows 上使用。
有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

> [!NOTE]
> 如果需要早期版本的 Azure CLI，请参阅[如何安装 Azure CLI 1.0](/azure/cli-install-nodejs)。

## <a name="macos"></a>macOS

> [!WARNING]
> 适用于 Azure CLI 的 Homebrew 公式 `azure-cli` 当前已过时，并且它将安装以前的版本。

1. 使用一个 `curl` 命令安装 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 可能需要重新启动命令外壳，某些更改才会生效。

   ```bash
   exec -l $SHELL
   ```
   
3. 在命令提示符下使用 `az` 命令运行 CLI。

> [!Note]
> 使用 InstallAzureCli 进行安装时，[`az component update`](/cli/azure/component#update) 不受支持。
> 若要更新到最新 CLI，请再次运行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要卸载，请参阅[手动卸载说明](#uninstall)。

## <a name="windows"></a>Windows

可使用 MSI 安装 Azure CLI 2.0 并在 Windows 命令行中使用它，或者可以在 Windows 中的 Bash on Ubuntu 上使用 apt-get 来安装 CLI。

### <a name="msi-for-the-windows-command-line"></a>适用于 Windows 命令行的 MSI 

要在 Windows 上安装 CLI 并在 Windows 命令行中使用它，请下载并运行 [msi](https://aka.ms/InstallAzureCliWindows)。

> [!NOTE]
> 使用 msi 进行安装时，[`az component`](/cli/azure/component) 不受支持。
> 要更新到最新 CLI，请再次运行 [msi](https://aka.ms/InstallAzureCliWindows)。
> 
> 要卸载 CLI，请再次运行 [msi](https://aka.ms/InstallAzureCliWindows) 并选择卸载。

### <a name="apt-get-for-bash-on-ubuntu-on-windows"></a>适用于 Windows 中的 Bash on Ubuntu 的 apt-get

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

> [!NOTE]
> 使用 apt-get 进行安装时，[`az component`](/cli/azure/component) 不受支持。
> 若要更新 CLI，请再次运行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要卸载，请运行 `sudo apt-get remove azure-cli`。

## <a name="apt-get-for-debianubuntu"></a>适用于 Debian/Ubuntu 的 apt-get

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

> [!NOTE]
> 使用 apt-get 进行安装时，[`az component`](/cli/azure/component) 不受支持。
> 若要更新 CLI，请再次运行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要卸载，请运行 `sudo apt-get remove azure-cli`。

## <a name="docker"></a>Docker

我们维护预先配置了 Azure CLI 2.0 的 Docker 映像。

请使用 `docker run` 安装 CLI。

```bash
docker run azuresdk/azure-cli-python:<version>
```

请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。

> [!NOTE]
> 如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。

>> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

CLI 作为 `/usr/local/bin` 中的 `az` 命令安装在映像中。

> [!NOTE]
> Docker 映像不支持 [`az component`](/cli/azure/component) 功能。
> 若要更新 Azure CLI 2.0，请使用 `docker run` 安装最新映像或所需的特定映像。

## <a name="linux"></a>Linux

1. 如果尚未安装 [Python](https://www.python.org/downloads)，请安装它。

2. 根据 Linux 发行版，安装必备组件。

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

3. 请使用一个 `curl` 命令安装 CLI。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

4. 可能需要重新启动命令外壳，某些更改才会生效。

   ```bash
   exec -l $SHELL
   ```

5. 在命令提示符下使用 `az` 命令运行 CLI。

> [!Note]
> 使用 InstallAzureCli 进行安装时，[`az component update`](/cli/azure/component#update) 不受支持。
> 若要更新到最新 CLI，请再次运行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要卸载，请参阅[手动卸载说明](#uninstall)。

## <a name="troubleshooting"></a>故障排除

### <a name="errors-with-curl-redirection"></a>有关 curl 重定向的错误

如果从有关 `-L` 参数的 `curl` 命令收到错误，或者收到说明“对象已移动”的错误，请尝试使用完整 url 而不是 aka.ms url：

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

## <a name="uninstall"></a>卸载

如果使用了 https://aka.ms/InstallAzureCli 上的脚本安装 CLI，可以通过这些步骤来卸载它。

1. 删除已安装的文件。

   ```bash
   rm -r <install location>/lib/azure-cli
   rm <install location>/bin/az
   ```

2. 从 `<install location>/.bash_profile` 删除行 `<install location>/lib/azure-cli/az.completion`。

> [!Note]
> 默认安装位置是 `/Users/<username>`。

如果使用了 apt-get、Docker 或 msi 安装 CLI，请使用相同的工具卸载。

## <a name="reporting-issues-and-feedback"></a>报告问题和反馈

如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-cli/issues)部分中提出问题。
若要从命令行提供反馈，请尝试 `az feedback` 命令。
