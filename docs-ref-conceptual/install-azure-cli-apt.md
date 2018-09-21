---
title: 使用 apt 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 apt 包管理器安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 88b4570f62858ec1e12898aea51a5dbce6d677b5
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388408"
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="84c40-103">使用 apt 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="84c40-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="84c40-104">如果运行附带 `apt` 的发行版（例如 Ubuntu 或 Debian），则可以安装适用于 Azure CLI 的 64 位包。</span><span class="sxs-lookup"><span data-stu-id="84c40-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there's a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="84c40-105">此包已在以下项中测试：</span><span class="sxs-lookup"><span data-stu-id="84c40-105">This package has been tested with:</span></span>

* <span data-ttu-id="84c40-106">Ubuntu trusty、xenial、artful 和 bionic</span><span class="sxs-lookup"><span data-stu-id="84c40-106">Ubuntu trusty, xenial, artful, and bionic</span></span>
* <span data-ttu-id="84c40-107">Debian wheezy、jessie 和 stretch</span><span class="sxs-lookup"><span data-stu-id="84c40-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="84c40-108">安装</span><span class="sxs-lookup"><span data-stu-id="84c40-108">Install</span></span>

1. <div id="install-step-1"/><span data-ttu-id="84c40-109">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="84c40-109">Modify your sources list:</span></span>

    ```bash
    AZ_REPO=$(lsb_release -cs)
    echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
        sudo tee /etc/apt/sources.list.d/azure-cli.list
    ```

2. <div id="signingKey"/><span data-ttu-id="84c40-110">获取 Microsoft 签名密钥：</span><span class="sxs-lookup"><span data-stu-id="84c40-110">Get the Microsoft signing key:</span></span>

   ```bash
   curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
   ```

3. <span data-ttu-id="84c40-111">安装 CLI：</span><span class="sxs-lookup"><span data-stu-id="84c40-111">Install the CLI:</span></span>

   ```bash
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

   > [!WARNING]
   > <span data-ttu-id="84c40-112">签名密钥已在 2018 年 5 月更新，并已被替换。</span><span class="sxs-lookup"><span data-stu-id="84c40-112">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="84c40-113">如果收到签名密钥错误，请确保已[获得最新的签名密钥](#signingKey)。</span><span class="sxs-lookup"><span data-stu-id="84c40-113">If you receive signing key errors, please ensure that you have [acquired the latest signing key](#signingKey).</span></span>

<span data-ttu-id="84c40-114">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="84c40-114">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="84c40-115">若要登录，请使用 [az login](/cli/azure/reference-index#az-login) 命令。</span><span class="sxs-lookup"><span data-stu-id="84c40-115">To sign in, use [az login](/cli/azure/reference-index#az-login) command.</span></span>

[!INCLUDE [interactive-login](includes/interactive-login.md)]

<span data-ttu-id="84c40-116">若要了解有关不同身份验证方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="84c40-116">To learn more about different authentication methods, see [Sign in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="84c40-117">故障排除</span><span class="sxs-lookup"><span data-stu-id="84c40-117">Troubleshooting</span></span>

<span data-ttu-id="84c40-118">下面是使用 `apt` 安装时出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="84c40-118">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="84c40-119">如果遇到的问题未在本文中列出，请[在 github 上提出问题](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="84c40-119">If you experience a problem not covered here, [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsbrelease-fails-with-command-not-found"></a><span data-ttu-id="84c40-120">lsb_release 失败，出现“找不到命令”错误</span><span class="sxs-lookup"><span data-stu-id="84c40-120">lsb_release fails with "Command not found"</span></span>

<span data-ttu-id="84c40-121">运行 `lsb_release` 命令时，可能会看到类似于以下错误的输出：</span><span class="sxs-lookup"><span data-stu-id="84c40-121">When running the `lsb_release` command, you may see output similar to the following error:</span></span>

```output
-bash: lsb_release: command not found
```

<span data-ttu-id="84c40-122">发生该错误的原因是未安装 `lsb_release` 命令。</span><span class="sxs-lookup"><span data-stu-id="84c40-122">The error is due to the `lsb_release` command not being installed.</span></span> <span data-ttu-id="84c40-123">可以通过安装 `lsb-release` 包解决此错误。</span><span class="sxs-lookup"><span data-stu-id="84c40-123">You can resolve it by installing the `lsb-release` package.</span></span>

```bash
sudo apt-get install lsb-release
```

### <a name="lsbrelease-does-not-return-the-base-distribution-version"></a><span data-ttu-id="84c40-124">lsb_release 没有返回基础发行版本</span><span class="sxs-lookup"><span data-stu-id="84c40-124">lsb_release does not return the base distribution version</span></span>

<span data-ttu-id="84c40-125">某些 Ubuntu 或 Debian 派生的版本（例如 Linux Mint）不会通过 `lsb_release` 返回正确的版本名称。</span><span class="sxs-lookup"><span data-stu-id="84c40-125">Some Ubuntu- or Debian-derived distributions such as Linux Mint may not return the correct version name from `lsb_release`.</span></span> <span data-ttu-id="84c40-126">此值在安装过程中用于确定要安装的包。</span><span class="sxs-lookup"><span data-stu-id="84c40-126">This value is used in the install process to determine the package to install.</span></span> <span data-ttu-id="84c40-127">如果知道自己的发行版派生自的版本的名称，则可在[安装步骤 1](#install-step-1) 中手动设置 `AZ_REPO` 值。</span><span class="sxs-lookup"><span data-stu-id="84c40-127">If you know the name of the version your distribution is derived from, you can set the `AZ_REPO` value manually in [install step 1](#install-step-1).</span></span> <span data-ttu-id="84c40-128">否则，请查看发行版的信息，了解如何确定基础发行版名称，然后将 `AZ_REPO` 设置为正确值。</span><span class="sxs-lookup"><span data-stu-id="84c40-128">Otherwise, look up information for your distribution on how to determine the base distribution name and set `AZ_REPO` to the correct value.</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="84c40-129">apt-key 失败，出现“没有 dirmngr”</span><span class="sxs-lookup"><span data-stu-id="84c40-129">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="84c40-130">运行 `apt-key` 命令时，可能会看到类似于以下错误的输出：</span><span class="sxs-lookup"><span data-stu-id="84c40-130">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="84c40-131">错误的原因是缺少 `apt-key` 所需的组件。</span><span class="sxs-lookup"><span data-stu-id="84c40-131">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="84c40-132">可以通过安装 `dirmngr` 包解决此错误。</span><span class="sxs-lookup"><span data-stu-id="84c40-132">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

### <a name="apt-key-hangs"></a><span data-ttu-id="84c40-133">apt-key 挂起</span><span class="sxs-lookup"><span data-stu-id="84c40-133">apt-key hangs</span></span>

<span data-ttu-id="84c40-134">当位于一个防火墙后并且该防火墙阻止与端口 11371 的传出连接时，`apt-key` 命令可能会无限期挂起。</span><span class="sxs-lookup"><span data-stu-id="84c40-134">When behind a firewall blocking outgoing connections to port 11371, the `apt-key` command might hang indefinitely.</span></span> <span data-ttu-id="84c40-135">防火墙可能需要对传出连接使用 HTTP 代理：</span><span class="sxs-lookup"><span data-stu-id="84c40-135">Your firewall may require the use of an HTTP proxy for outgoing connections:</span></span>

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

<span data-ttu-id="84c40-136">若要确定是否有代理，请与系统管理员联系。</span><span class="sxs-lookup"><span data-stu-id="84c40-136">To determine if you have a proxy, contact your system administrator.</span></span> <span data-ttu-id="84c40-137">如果代理不需要登录，请省略用户、密码和 `@` 令牌。</span><span class="sxs-lookup"><span data-stu-id="84c40-137">If your proxy does not require a login, then leave out the user, password, and `@` token.</span></span>

## <a name="update"></a><span data-ttu-id="84c40-138">更新</span><span class="sxs-lookup"><span data-stu-id="84c40-138">Update</span></span>

<span data-ttu-id="84c40-139">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="84c40-139">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!WARNING]
> <span data-ttu-id="84c40-140">签名密钥已在 2018 年 5 月更新，并已被替换。</span><span class="sxs-lookup"><span data-stu-id="84c40-140">The signing key was updated in May 2018, and has been replaced.</span></span> <span data-ttu-id="84c40-141">如果收到签名密钥错误，请确保已[获得最新的签名密钥](#signingKey)。</span><span class="sxs-lookup"><span data-stu-id="84c40-141">If you receive signing key errors, please ensure that you have [acquired the latest signing key](#signingKey).</span></span>
>
> [!NOTE]
> <span data-ttu-id="84c40-142">此命令将会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="84c40-142">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="84c40-143">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="84c40-143">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="84c40-144">卸载</span><span class="sxs-lookup"><span data-stu-id="84c40-144">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="84c40-145">使用 `apt-get remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="84c40-145">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="84c40-146">如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="84c40-146">If you don't plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="84c40-147">请删除任何不需要的包。</span><span class="sxs-lookup"><span data-stu-id="84c40-147">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
