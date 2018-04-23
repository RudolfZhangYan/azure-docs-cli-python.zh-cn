---
title: 使用 apt 在 Linux 上安装 Azure CLI 2.0
description: 如何使用 apt 包管理器安装 Azure CLI 2.0
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/06/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: a2578c79ba961cb12f3f49e77a9eaa73c4fe97a2
ms.sourcegitcommit: 0e9aafa07311526f43661c8bd3a7eba7cbc2caed
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 04/20/2018
---
# <a name="install-azure-cli-20-with-apt"></a><span data-ttu-id="83ba4-103">使用 apt 安装 Azure CLI 2.0</span><span class="sxs-lookup"><span data-stu-id="83ba4-103">Install Azure CLI 2.0 with apt</span></span>

<span data-ttu-id="83ba4-104">如果运行附带 `apt` 的发行版（例如 Ubuntu 或 Debian），则可以安装适用于 Azure CLI 的 64 位包。</span><span class="sxs-lookup"><span data-stu-id="83ba4-104">If you are running a distribution that comes with `apt`, such as Ubuntu or Debian, there is a 64-bit package available for the Azure CLI.</span></span> <span data-ttu-id="83ba4-105">此包已在以下项中测试：</span><span class="sxs-lookup"><span data-stu-id="83ba4-105">This package has been tested with:</span></span>

* <span data-ttu-id="83ba4-106">Ubuntu trusty、xenial 和 artful</span><span class="sxs-lookup"><span data-stu-id="83ba4-106">Ubuntu trusty, xenial, and artful</span></span>
* <span data-ttu-id="83ba4-107">Debian wheezy、jessie 和 stretch</span><span class="sxs-lookup"><span data-stu-id="83ba4-107">Debian wheezy, jessie, and stretch</span></span>

## <a name="install"></a><span data-ttu-id="83ba4-108">安装</span><span class="sxs-lookup"><span data-stu-id="83ba4-108">Install</span></span>

1. <span data-ttu-id="83ba4-109">修改源列表：</span><span class="sxs-lookup"><span data-stu-id="83ba4-109">Modify your sources list:</span></span>

     ```bash
     AZ_REPO=$(lsb_release -cs)
     echo "deb [arch=amd64] https://packages.microsoft.com/repos/azure-cli/ $AZ_REPO main" | \
          sudo tee /etc/apt/sources.list.d/azure-cli.list
     ```

2. <span data-ttu-id="83ba4-110">获取 Microsoft 签名密钥：</span><span class="sxs-lookup"><span data-stu-id="83ba4-110">Get the Microsoft signing key:</span></span>

   ```bash
   sudo apt-key adv --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
   ```

  > [!WARNING]
  > <span data-ttu-id="83ba4-111">此签名密钥已弃用，将在 2018 年 5 月底被替换。</span><span class="sxs-lookup"><span data-stu-id="83ba4-111">This signing key is deprecated, and will be replaced at the end of May 2018.</span></span> <span data-ttu-id="83ba4-112">为了能够通过 `apt` 持续获得更新，另请确保安装新密钥：</span><span class="sxs-lookup"><span data-stu-id="83ba4-112">In order to keep getting updates with `apt`, make sure that you also install the new key:</span></span>
  > 
  > ```bash
  > curl -L https://packages.microsoft.com/keys/microsoft.asc | sudo apt-key add -
  > ``` 

3. <span data-ttu-id="83ba4-113">安装 CLI：</span><span class="sxs-lookup"><span data-stu-id="83ba4-113">Install the CLI:</span></span>

   ```bash
   sudo apt-get install apt-transport-https
   sudo apt-get update && sudo apt-get install azure-cli
   ```

<span data-ttu-id="83ba4-114">然后即可使用 `az` 命令来运行 Azure CLI。</span><span class="sxs-lookup"><span data-stu-id="83ba4-114">You can then run the Azure CLI with the `az` command.</span></span> <span data-ttu-id="83ba4-115">若要登录，请运行 `az login` 命令。</span><span class="sxs-lookup"><span data-stu-id="83ba4-115">To log in, run the `az login` command.</span></span>

```azurecli
az login
```

<span data-ttu-id="83ba4-116">若要了解有关不同登录方法的详细信息，请参阅[使用 Azure CLI 2.0 登录](authenticate-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="83ba4-116">To learn more about different login methods, see [Log in with Azure CLI 2.0](authenticate-azure-cli.md).</span></span>

## <a name="troubleshooting"></a><span data-ttu-id="83ba4-117">故障排除</span><span class="sxs-lookup"><span data-stu-id="83ba4-117">Troubleshooting</span></span>

<span data-ttu-id="83ba4-118">下面是使用 `apt` 安装时出现的一些常见问题。</span><span class="sxs-lookup"><span data-stu-id="83ba4-118">Here are some common problems seen when installing with `apt`.</span></span> <span data-ttu-id="83ba4-119">如果出现的问题未在此处列出，请[在 Github 上提问](https://github.com/Azure/azure-cli/issues)。</span><span class="sxs-lookup"><span data-stu-id="83ba4-119">If your issue is not listed here, please [file an issue on github](https://github.com/Azure/azure-cli/issues).</span></span>

### <a name="apt-key-fails-with-no-dirmngr"></a><span data-ttu-id="83ba4-120">apt-key 失败，出现“没有 dirmngr”</span><span class="sxs-lookup"><span data-stu-id="83ba4-120">apt-key fails with "No dirmngr"</span></span>

<span data-ttu-id="83ba4-121">运行 `apt-key` 命令时，可能会看到类似于以下错误的输出：</span><span class="sxs-lookup"><span data-stu-id="83ba4-121">When running the `apt-key` command, you may see output similar to the following error:</span></span>

```output
gpg: failed to start the dirmngr '/usr/bin/dirmngr': No such file or directory
gpg: connecting dirmngr at '/tmp/apt-key-gpghome.kt5zo27tp1/S.dirmngr' failed: No such file or directory
gpg: keyserver receive failed: No dirmngr
```

<span data-ttu-id="83ba4-122">错误的原因是缺少 `apt-key` 所需的组件。</span><span class="sxs-lookup"><span data-stu-id="83ba4-122">The error is due to a missing component required by `apt-key`.</span></span> <span data-ttu-id="83ba4-123">可以通过安装 `dirmngr` 包解决此错误。</span><span class="sxs-lookup"><span data-stu-id="83ba4-123">You can resolve it by installing the `dirmngr` package.</span></span>

```bash
sudo apt-get install dirmngr
```

### <a name="apt-key-hangs"></a><span data-ttu-id="83ba4-124">apt-key 挂起</span><span class="sxs-lookup"><span data-stu-id="83ba4-124">apt-key hangs</span></span>

<span data-ttu-id="83ba4-125">当位于一个防火墙后并且该防火墙阻止与端口 11371 的传出连接时，`apt-key` 命令可能会无限期挂起。</span><span class="sxs-lookup"><span data-stu-id="83ba4-125">When behind a firewall blocking outgoing connections to port 11371, the `apt-key` command might hang indefinitely.</span></span> <span data-ttu-id="83ba4-126">防火墙可能需要对传出连接使用 HTTP 代理：</span><span class="sxs-lookup"><span data-stu-id="83ba4-126">Your firewall may require the use of an HTTP proxy for outgoing connections:</span></span>

```bash
sudo apt-key adv --keyserver-options http-proxy=http://<USER>:<PASSWORD>@<PROXY-HOST>:<PROXY-PORT>/ --keyserver packages.microsoft.com --recv-keys 52E16F86FEE04B979B07E28DB02C46DF417A0893
```

<span data-ttu-id="83ba4-127">如果不知道是否有代理，请与系统管理员联系。</span><span class="sxs-lookup"><span data-stu-id="83ba4-127">If you do not know if you have a proxy, contact your system administrator.</span></span> <span data-ttu-id="83ba4-128">如果代理不需要登录，则省略用户、密码和 `@` 令牌。</span><span class="sxs-lookup"><span data-stu-id="83ba4-128">If your proxy does not require a login then leave out the user, password, and `@` token.</span></span>

## <a name="update"></a><span data-ttu-id="83ba4-129">更新</span><span class="sxs-lookup"><span data-stu-id="83ba4-129">Update</span></span>

<span data-ttu-id="83ba4-130">使用 `apt-get upgrade` 更新 CLI 包。</span><span class="sxs-lookup"><span data-stu-id="83ba4-130">Use `apt-get upgrade` to update the CLI package.</span></span>

   ```bash
   sudo apt-get update && sudo apt-get upgrade
   ```

> [!NOTE]
> <span data-ttu-id="83ba4-131">此命令将会升级系统上所有未发生依赖关系更改的已安装包。</span><span class="sxs-lookup"><span data-stu-id="83ba4-131">This command upgrades all of the installed packages on your system that have not had a dependency change.</span></span>
> <span data-ttu-id="83ba4-132">若只要升级 CLI，请使用 `apt-get install`。</span><span class="sxs-lookup"><span data-stu-id="83ba4-132">To upgrade the CLI only, use `apt-get install`.</span></span>
> ```bash
> sudo apt-get update && sudo apt-get install --only-upgrade -y azure-cli
> ```

## <a name="uninstall"></a><span data-ttu-id="83ba4-133">卸载</span><span class="sxs-lookup"><span data-stu-id="83ba4-133">Uninstall</span></span>

[!INCLUDE [uninstall-boilerplate.md](includes/uninstall-boilerplate.md)]

1. <span data-ttu-id="83ba4-134">使用 `apt-get remove` 进行卸载。</span><span class="sxs-lookup"><span data-stu-id="83ba4-134">Uninstall with `apt-get remove`.</span></span>

    ```bash
    sudo apt-get remove -y azure-cli
    ```

2. <span data-ttu-id="83ba4-135">如果不打算重新安装 CLI，请删除 Azure CLI 存储库信息。</span><span class="sxs-lookup"><span data-stu-id="83ba4-135">If you do not plan to reinstall the CLI, remove the Azure CLI repository information.</span></span>

   ```bash
   sudo rm /etc/apt/sources.list.d/azure-cli.list
   ```

3. <span data-ttu-id="83ba4-136">请删除任何不需要的包。</span><span class="sxs-lookup"><span data-stu-id="83ba4-136">Remove any unneeded packages.</span></span>

   ```bash
   sudo apt autoremove
   ```
