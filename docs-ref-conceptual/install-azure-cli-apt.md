---
title: 使用 apt 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 apt 包管理器安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/06/2018
ms.topic: conceptual
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 7eb04b408f403264f3951bf663d43686601c4ab8
ms.sourcegitcommit: 1d18f667af28b59f5524a3499a4b7dc12af5163d
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/09/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="a6ea7-103">使用 apt 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="a6ea7-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="a6ea7-104">如果运行附带 `apt` 的发行版（例如 Ubuntu 或 Debian），则可以安装适用于 Azure CLI 的 64 位包。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="a6ea7-105">此包已在以下项中测试：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-105">This package has been tested with:</span></span>

* <span data-ttu-id="a6ea7-106">Ubuntu trusty、xenial 和 artful</span><span class="sxs-lookup"><span data-stu-id="a6ea7-106">Ubuntu trusty, xenial, and artful</span></span>
* <span data-ttu-id="a6ea7-107">Debian wheezy、jessie 和 stretch</span><span class="sxs-lookup"><span data-stu-id="a6ea7-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="a6ea7-108">安装</span><span class="sxs-lookup"><span data-stu-id="a6ea7-108">Install</span></span>

1. <span data-ttu-id="a6ea7-109">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-109">Modify your sources list:</span></span>

     ```bash
     AZ_REPO=$(lsb_release -cs)
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="a6ea7-110">获取 Microsoft 签名密钥：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-110">Get the Microsoft signing key:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   ```

  > [!WARNING]
  > <span data-ttu-id="a6ea7-111">此签名密钥已弃用，将在 2018 年 5 月底被替换。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-111">This signing key is deprecated, and will be replaced at the end of May 2018.</span></span> <span data-ttu-id="a6ea7-112">为了能够通过 `apt` 持续获得更新，另请确保安装新密钥：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-112">In order to keep getting updates with `apt`, make sure that you also install the new key:</span></span>
  > 
  > ```bash
  > curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
  > ``` 

3. <span data-ttu-id="a6ea7-113">安装 CLI：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-113">Install the CLI:</span></span>

   ```bash
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="a6ea7-114">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-114">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="a6ea7-115">若要登录，请运行 `az login` 命令。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-115">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="a6ea7-116">若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-116">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="a6ea7-117">故障排除</span><span class="sxs-lookup"><span data-stu-id="a6ea7-117">Troubleshooting</span></span>

<span data-ttu-id="a6ea7-118">下面是使用 `apt` 安装时出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-118">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="a6ea7-119">如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-119">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="lsbrelease-fails-with-command-not-found"></a><span data-ttu-id="a6ea7-120">lsb_release 失败，出现“找不到命令”错误</span><span class="sxs-lookup"><span data-stu-id="a6ea7-120">lsb_release fails with "Command not found"</span></span>

<span data-ttu-id="a6ea7-121">运行 `lsb_release` 命令时，可能会看到类似于以下错误的输出：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-121">When running the `lsb_release` command, you may see output similar to the following error:</span></span>

```output
-bash: lsb_release: command not found
```

<span data-ttu-id="a6ea7-122">此错误是由于未安装 lsb_release。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-122">The error is due to lsb_release not being installed.</span></span> <span data-ttu-id="a6ea7-123">可以通过安装 `lsb-release` 包解决此错误。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-123">You can resolve it by installing the `lsb-release` package.</span></span>

```bash
sudo apt-get install lsb-release
```

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="a6ea7-124">apt-key 失败，出现“没有 dirmngr”</span><span class="sxs-lookup"><span data-stu-id="a6ea7-124">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="a6ea7-125">运行 `apt-key` 命令时，可能会看到类似于以下错误的输出：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-125">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="a6ea7-126">错误的原因是缺少 `apt-key` 所需的组件。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-126">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="a6ea7-127">可以通过安装 `dirmngr` 包解决此错误。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-127">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

### <a name="apt-key-hangs"></a><span data-ttu-id="a6ea7-128">apt-key 挂起</span><span class="sxs-lookup"><span data-stu-id="a6ea7-128">apt-key hangs</span></span>

<span data-ttu-id="a6ea7-129">当位于一个防火墙后并且该防火墙阻止与端口 11371 的传出连接时，`apt-key` 命令可能会无限期挂起。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-129">When behind a firewall blocking outgoing connections to port 11371, the `apt-key` command might hang indefinitely.</span></span> <span data-ttu-id="a6ea7-130">防火墙可能需要对传出连接使用 HTTP 代理：</span><span class="sxs-lookup"><span data-stu-id="a6ea7-130">Your firewall may require the use of an HTTP proxy for outgoing connections:</span></span>

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

<span data-ttu-id="a6ea7-131">如果不知道是否有代理，请与系统管理员联系。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-131">If you do not know if you have a proxy, contact your system administrator.</span></span> <span data-ttu-id="a6ea7-132">如果代理不需要登录，则省略用户、密码和 `@` 令牌。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-132">If your proxy does not require a login then leave out the user, password, and `@` token.</span></span>

## <a name="update"></a><span data-ttu-id="a6ea7-133">更新</span><span class="sxs-lookup"><span data-stu-id="a6ea7-133">Update</span></span>

<span data-ttu-id="a6ea7-134">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-134">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="a6ea7-135">此命令将会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-135">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="a6ea7-136">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-136">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="a6ea7-137">卸载</span><span class="sxs-lookup"><span data-stu-id="a6ea7-137">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="a6ea7-138">使用 `apt-get remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-138">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="a6ea7-139">如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-139">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="a6ea7-140">请删除任何不需要的包。</span><span class="sxs-lookup"><span data-stu-id="a6ea7-140">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
