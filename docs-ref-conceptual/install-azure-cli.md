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
ms.openlocfilehash: b7c0b7c50794333b28c034de9b41f1e506053e25
ms.sourcegitcommit: 663d4188ccc4be425d3d551fe32613fafd05a764
ms.translationtype: HT
ms.contentlocale: zh-CN
---
# <a name="install-azure-cli-20"></a>安装 Azure CLI 2.0

现在就安装新版本的 Azure CLI！
我们已改进并更新了 Azure CLI，以提供用于管理 Azure 资源的卓越本机命令行体验。
它可以在 macOS、Linux 和 Windows 上使用。
有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

> [!NOTE]
> 如果需要早期版本的 Azure CLI，请参阅此处的如何[安装 Azure 1.0](/azure/cli-install-nodejs)。

## <a name="macos"></a>macOS

1. 使用一个 `curl` 命令安装 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

2. 可能需要重新启动命令外壳，某些更改才会生效。

   ```bash
   exec -l $SHELL
   ```
   
3. 在命令提示符下使用 `az` 命令运行 Azure CLI 2.0。

> [!Note]
> 使用 InstallAzureCli 进行安装时，`az component update` 不受支持。
> 若要更新到最新 CLI，请再次运行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要卸载，请参阅[手动卸载说明](#uninstall)。

## <a name="windows"></a>Windows

Azure CLI 2.0 支持 Bash 命令语法，从而使基于 Windows 的 Ubuntu 上的 Bash 成为使用 CLI 的良好方式。
如果不使用 Bash，可以在 Windows 命令行中安装并使用 CLI。

### <a name="bash-on-ubuntu-on-windows"></a>基于 Windows 的 Ubuntu 上的 Bash

1. 如果你的 Windows 上没有 Bash，请[安装它](https://msdn.microsoft.com/commandline/wsl/install_guide)。

2. 打开 Bash Shell。

3. 如果尚未安装 Python，请安装它。

   ```bash
   sudo apt-get install python3
   ```

   > [!NOTE]
   > 若要查看是否已安装 Python，请运行 `python --version`。

4. 修改源列表。

   ```bash
   echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ wheezy main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
   ```

5. 运行以下 sudo 命令：

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 417A0893
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

> [!NOTE]
> 使用 apt-get 进行安装时，`az component` 不受支持。
> 若要更新 CLI，请再次运行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要卸载，请运行 `sudo apt-get remove azure-cli`。

### <a name="windows-command-line"></a>Windows 命令行 

1. 访问 Python 站点并[下载适用于 Windows 的 Python](https://www.python.org/downloads/)。
   请务必在安装 Python 时安装 Pip 组件。
   在安装完成后，将 Python 添加到 PATH 环境变量（安装程序将提示你）。

2. 在命令提示符下检查 Python 安装。

   ```bash
   python --version
   ```

3. 使用 `pip` 安装 Azure CLI 2.0。

   ```bash
   pip install --user azure-cli
   ```

4. 将包含 az.bat 的文件夹添加到你的路径。
   CLI `az.bat` 可以安装在 `%USERPROFILE%\AppData\Roaming\Python\Scripts` 或 `%USERPROFILE%\AppData\Roaming\Python\PythonXY\Scripts` 中，其中 `XY` 是你的 Python 版本（例如 `%USERPROFILE%\AppData\Roaming\Python\Python27\Scripts`）。
   将包含 `az.bat` 的文件夹添加到你的路径。
   
4. 在命令提示符下使用 `az` 命令运行 Azure CLI 2.0。

> [!NOTE]
> 如果已安装 Azure CLI 2.0，并且希望查看是否安装了最新版本，请使用 `az --version` 查看已安装的是哪个版本。
> 将该版本与 [https://pypi.python.org/pypi/azure-cli](https://pypi.python.org/pypi/azure-cli) 上提供的最新版本进行比较。
> 
> 若要更新到最新 CLI，请运行 `az component update`。
> 
> 若要卸载 CLI，请运行 `pip uninstall azure-cli`。

## <a name="linux"></a>Linux

1. 在 Linux 上，可能需要安装特定的[必备组件](#linux-prerequisites)。

2. 使用一个 `curl` 命令安装 Azure CLI 2.0。

   ```bash
   curl -L https://aka.ms/InstallAzureCli | bash
   ```

3. 可能需要重新启动命令外壳，某些更改才会生效。

   ```bash
   exec -l $SHELL
   ```

4. 在命令提示符下使用 `az` 命令运行 Azure CLI 2.0。

> [!Note]
> 使用 InstallAzureCli 进行安装时，`az component update` 不受支持。
> 若要更新到最新 CLI，请再次运行 `curl -L https://aka.ms/InstallAzureCli | bash`。
> 
> 若要卸载，请参阅[手动卸载说明](#uninstall)。

## <a name="docker"></a>Docker

我们维护预先配置了 Azure CLI 的 Docker 映像。

请使用 `docker run` 安装 Azure CLI。

```bash
docker run azuresdk/azure-cli-python:<version>
```

请参阅我们的 [Docker 标记](https://hub.docker.com/r/azuresdk/azure-cli-python/tags/)来了解可用版本。

> [!NOTE]
> 如果要从用户环境选取 SSH 密钥，可以使用 `-v ${HOME}:/root` 将 $HOME 装载为 `/root`。
>
> ```bash
> docker run -v ${HOME}:/root azuresdk/azure-cli-python:<version>
> ```

> [!NOTE]
> Docker 映像不支持 [`component` 功能](/cli/azure/component)。
> 若要更新 Azure CLI 2.0，请使用 `docker run` 安装最新映像或所需的特定映像。

## <a name="apt-get"></a>apt-get

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

> [!NOTE]
> 使用 apt-get 进行安装时，`az component` 不受支持。
> 若要更新 CLI，请再次运行 `sudo apt-get update && sudo apt-get install azure-cli`。
> 
> 若要卸载，请运行 `sudo apt-get remove azure-cli`。

## <a name="linux-prerequisites"></a>Linux 必备组件

1. 如果尚未安装 [Python](https://www.python.org/downloads)，请安装它。

2. 根据你的 Linux 发行版，安装必备组件。

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

## <a name="troubleshooting"></a>故障排除
-------------------------------

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


### <a name="errors-on-install-with-cffi-or-cryptography"></a>使用 `cffi` 或加密包进行安装时出现的错误

如果在 OS X 上进行安装时出现错误，请升级 `pip`。

```bash
pip install --upgrade --force-reinstall pip
```

如果在 **Debian** 或 **Ubuntu** 上安装时出现错误（如这些示例），请安装 `libssl-dev` 和 `libffi-dev`。

```bash
sudo apt-get update
sudo apt-get install -y libssl-dev libffi-dev
```

另请安装适用于你的 Python 版本的 Python Dev。

Python 2：

```bash
sudo apt-get install -y python-dev
```

Python 3：

```bash
sudo apt-get install -y python3-dev
```

Ubuntu 15 可能还需要 `build-essential`：

```bash
sudo apt-get install -y build-essential
```

### <a name="example-errors"></a>示例错误

```
Downloading cffi-1.5.2.tar.gz (388kB)
    100% |################################| 389kB 3.9MB/s
    Complete output from command python setup.py egg_info:

        No working compiler found, or bogus compiler options
        passed to the compiler from Python's distutils module.
        See the error messages above.
        (If they are about -mno-fused-madd and you are on OS/X 10.8,
        see http://stackoverflow.com/questions/22313407/ .)

    ----------------------------------------
Command "python setup.py egg_info" failed with error code 1 in /tmp/pip-build-77i2fido/cffi/
```

```
#include <openssl/e_os2.h>
                            ^
compilation terminated.
error: command 'x86_64-linux-gnu-gcc' failed with exit status 1

Failed building wheel for cryptography
```

请参阅 Stack Overflow 问题 - [Failed to install Python Cryptography package with PIP and setup.py](http://stackoverflow.com/questions/22073516/failed-to-install-python-cryptography-package-with-pip-and-setup-py)（无法使用 PIP 和 setup.py 安装 Python 加密包）

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

如果使用了 pip、apt-get 或 Docker 安装 CLI，请使用相同的工具卸载它。

## <a name="reporting-issues-and-feedback"></a>报告问题和反馈

如果遇到该工具的任何 bug，请在 GitHub 存储库的[问题](https://github.com/Azure/azure-cli/issues)部分中提出问题。
若要从命令行提供反馈，请尝试 `az feedback` 命令。
