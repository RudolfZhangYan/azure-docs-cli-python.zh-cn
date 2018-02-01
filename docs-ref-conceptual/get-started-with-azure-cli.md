---
title: "Azure CLI 2.0 入门"
description: "Linux、Mac 或 Windows 上的 Azure CLI 2.0 入门。"
keywords: Azure CLI 2.0, Linux, Mac, Windows, OS X, Ubuntu, Debian, CentOS, RHEL, SUSE, CoreOS, Docker, Windows, Python, PIP
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 85c418a8-6177-4833-bb8d-ff4ce2233c1a
ms.openlocfilehash: 689b8f4d77af5a6f398c0dd85e922baa398f767a
ms.sourcegitcommit: dd5b2c7b0b56608ef9ea8730c7dc76e6c532d5ea
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/26/2018
---
# <a name="get-started-with-azure-cli-20"></a><span data-ttu-id="4a257-104">Azure CLI 2.0 入门</span><span class="sxs-lookup"><span data-stu-id="4a257-104">Get started with Azure CLI 2.0</span></span>

<span data-ttu-id="4a257-105">Azure CLI 2.0 是 Azure 的新命令行体验，用于管理 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-105">The Azure CLI 2.0 is Azure's new command line experience for managing Azure resources.</span></span>
<span data-ttu-id="4a257-106">可以通过 [Azure Cloud Shell](/azure/cloud-shell/overview) 在浏览器中使用它，也可以将其[安装](install-azure-cli.md)在 macOS、Linux 和 Windows 上，然后从命令行运行它。</span><span class="sxs-lookup"><span data-stu-id="4a257-106">You can use it in your browser with [Azure Cloud Shell](/azure/cloud-shell/overview), or you can [install](install-azure-cli.md) it on macOS, Linux, and Windows and run it from the command line.</span></span>

<span data-ttu-id="4a257-107">Azure CLI 2.0 经过优化，可用于从命令行管理 Azure 资源，以及生成可以针对 Azure 资源管理器运行的自动化脚本。</span><span class="sxs-lookup"><span data-stu-id="4a257-107">Azure CLI 2.0 is optimized for managing and administering Azure resources from the command line, and for building automation scripts that work against the Azure Resource Manager.</span></span>
<span data-ttu-id="4a257-108">本文将帮助你开始使用 Azure PowerShell，并讲解其重要概念。</span><span class="sxs-lookup"><span data-stu-id="4a257-108">This article helps get you started using it, and teaches you the core concepts behind it.</span></span>

<span data-ttu-id="4a257-109">有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="4a257-109">For information about the latest release, see the [release notes](release-notes-azure-cli.md).</span></span>

## <a name="connect"></a><span data-ttu-id="4a257-110">连接</span><span class="sxs-lookup"><span data-stu-id="4a257-110">Connect</span></span>

<span data-ttu-id="4a257-111">最简单的入门方法是[启动 Cloud Shell](/azure/cloud-shell/quickstart)。</span><span class="sxs-lookup"><span data-stu-id="4a257-111">The simplest way to get started is to [launch Cloud Shell](/azure/cloud-shell/quickstart).</span></span>

1. <span data-ttu-id="4a257-112">从 Azure 门户的顶部导航栏启动 Cloud Shell。</span><span class="sxs-lookup"><span data-stu-id="4a257-112">Launch Cloud Shell from the top navigation of the Azure portal.</span></span>

   ![Shell 图标](media/get-started-with-azure-cli/shell-icon.png)

2. <span data-ttu-id="4a257-114">选择要使用的订阅并创建存储帐户。</span><span class="sxs-lookup"><span data-stu-id="4a257-114">Choose the subscription you want to use and create a storage account.</span></span>

   ![创建存储帐户](media/get-started-with-azure-cli/storage-prompt.png)

<span data-ttu-id="4a257-116">还可以[安装](install-azure-cli.md)并在本地通过命令行运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="4a257-116">You can also [install](install-azure-cli.md) the CLI and run it locally from the command line.</span></span> <span data-ttu-id="4a257-117">安装 CLI 后，运行 `az login` 以使用默认订阅进行登录。</span><span class="sxs-lookup"><span data-stu-id="4a257-117">Once you have installed the CLI, run `az login` to log in with your default subscription.</span></span>

## <a name="create-a-resource-group"></a><span data-ttu-id="4a257-118">创建资源组。</span><span class="sxs-lookup"><span data-stu-id="4a257-118">Create a Resource Group</span></span>

<span data-ttu-id="4a257-119">完成所有设置后，让我们使用 Azure CLI 在 Azure 中创建资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-119">Now that we've got everything set up, let's use the Azure CLI to create resources within Azure.</span></span>

<span data-ttu-id="4a257-120">首先，请创建一个资源组。</span><span class="sxs-lookup"><span data-stu-id="4a257-120">First, create a Resource Group.</span></span>  <span data-ttu-id="4a257-121">使用 Azure 中的资源组可以管理希望以逻辑方式分组的多个资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-121">Resource Groups in Azure provide a way to manage multiple resources that you want to logically group.</span></span>  <span data-ttu-id="4a257-122">例如，可为应用程序或项目创建资源组，并在其中添加虚拟机、数据库和 CDN 服务。</span><span class="sxs-lookup"><span data-stu-id="4a257-122">For example, you might create a Resource Group for an application or project and add a virtual machine, a database and a CDN service within it.</span></span>

<span data-ttu-id="4a257-123">让我们在 Azure 的 *westus2* 区域创建一个名为“MyResourceGroup”的资源组。</span><span class="sxs-lookup"><span data-stu-id="4a257-123">Let's create a resource group named "MyResourceGroup" in the *westus2* region of Azure.</span></span>  <span data-ttu-id="4a257-124">为此，请键入以下命令：</span><span class="sxs-lookup"><span data-stu-id="4a257-124">To do so type the following command:</span></span>

```azurecli-interactive
az group create -n MyResourceGroup -l westus2
```

<span data-ttu-id="4a257-125">创建资源组后，`az group create` 命令将输出新建的资源的多个属性：</span><span class="sxs-lookup"><span data-stu-id="4a257-125">Once the resource group has been created, the `az group create` command outputs several properties of the newly created resource:</span></span>

```Output
{
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup",
  "location": "westus2",
  "managedBy": null,
  "name": "MyResourceGroup",
  "properties": {
    "provisioningState": "Succeeded"
  },
  "tags": null
}
```

## <a name="create-a-linux-virtual-machine"></a><span data-ttu-id="4a257-126">创建 Linux 虚拟机</span><span class="sxs-lookup"><span data-stu-id="4a257-126">Create a Linux Virtual Machine</span></span>

<span data-ttu-id="4a257-127">创建资源组后，让我们在其中创建 Linux VM。</span><span class="sxs-lookup"><span data-stu-id="4a257-127">Now that we have our resource group, let's create a Linux VM within it.</span></span>

<span data-ttu-id="4a257-128">可以运行以下命令，使用常用的 UbuntuLTS 映像创建附有两个存储磁盘（大小分别为 10 GB 和 20 GB）的 Linux VM：</span><span class="sxs-lookup"><span data-stu-id="4a257-128">You can create a Linux VM using the popular UbuntuLTS image, with two attached storage disks of 10 GB and 20 GB, with the following command:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

<span data-ttu-id="4a257-129">运行上述命令时，Azure CLI 2.0 将查找存储在 ~/.ssh 目录下的 SSH 密钥对。</span><span class="sxs-lookup"><span data-stu-id="4a257-129">When you run the preceding command, the Azure CLI 2.0 looks for an SSH key pair stored under your ~/.ssh directory.</span></span>  <span data-ttu-id="4a257-130">如果尚未在该位置存储 SSH 密钥对，可让 Azure CLI 绕过 --generate-ssh-keys 参数，自动创建一个密钥对：</span><span class="sxs-lookup"><span data-stu-id="4a257-130">If you don't already have an SSH key pair stored there, you can ask the Azure CLI to automatically create one for you by passing the --generate-ssh-keys parameter:</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20 --generate-ssh-keys
```

<span data-ttu-id="4a257-131">完全创建并已准备好访问和使用 VM 后，`az vm create` 命令将返回输出。</span><span class="sxs-lookup"><span data-stu-id="4a257-131">The `az vm create` command returns output once the VM has been fully created and is ready to be accessed and used.</span></span> <span data-ttu-id="4a257-132">输出包含新建的 VM 的多个属性，包括其公共 IP 地址：</span><span class="sxs-lookup"><span data-stu-id="4a257-132">The output includes several properties of the newly created VM including its public IP address:</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xxx.xx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="4a257-133">创建 VM 后，可以使用创建的 VM 的公共 IP 地址通过 **SSH** 登录到新的 Linux VM：</span><span class="sxs-lookup"><span data-stu-id="4a257-133">Now that the VM has been created, you can log on to your new Linux VM using **SSH** with the public IP address of the VM you created:</span></span>

```azurecli-interactive
ssh xx.xxx.xxx.xxx
```

```Output
Welcome to Ubuntu 14.04.4 LTS (GNU/Linux 3.19.0-65-generic x86_64)

 * Documentation:  https://help.ubuntu.com/

  System information as of Sun Feb 19 00:32:28 UTC 2017

  System load: 0.31              Memory usage: 3%   Processes:       89
  Usage of /:  39.6% of 1.94GB   Swap usage:   0%   Users logged in: 0

  Graph this data and manage this system at:
    https://landscape.canonical.com/

  Get cloud support with Ubuntu Advantage Cloud Guest:
    http://www.ubuntu.com/business/services/cloud

0 packages can be updated.
0 updates are security updates.



The programs included with the Ubuntu system are free software;
the exact distribution terms for each program are described in the
individual files in /usr/share/doc/*/copyright.

Ubuntu comes with ABSOLUTELY NO WARRANTY, to the extent permitted by
applicable law.

my-login@MyLinuxVM:~$
```

## <a name="create-a-windows-server-virtual-machine"></a><span data-ttu-id="4a257-134">创建 Windows Server 虚拟机</span><span class="sxs-lookup"><span data-stu-id="4a257-134">Create a Windows Server Virtual Machine</span></span>

<span data-ttu-id="4a257-135">现在，让我们使用 `az vm create` 命令创建基于 Windows Server 2016 Datacenter 的 VM，并将其添加到用于 Linux VM 的同一个“MyResourceGroup”资源组。</span><span class="sxs-lookup"><span data-stu-id="4a257-135">Let's now create a Windows Server 2016 Datacenter-based VM using the `az vm create` command and add it to the same "MyResourceGroup" resource group that we used for our Linux VM.</span></span>  <span data-ttu-id="4a257-136">与 Linux VM 示例一样，我们还要使用 `--data-disk-sizes-gb` 参数附加两个存储磁盘。</span><span class="sxs-lookup"><span data-stu-id="4a257-136">Like the Linux VM example, we'll also attach two storage disks using the `--data-disk-sizes-gb` parameter.</span></span>

<span data-ttu-id="4a257-137">Azure 要求避免使用很容易猜出的用户名/密码。</span><span class="sxs-lookup"><span data-stu-id="4a257-137">Azure requires that you avoid using easily guessed usernames/passwords.</span></span> <span data-ttu-id="4a257-138">在可以使用哪些字符以及用户名和密码的最小长度方面，都有特定的规则。</span><span class="sxs-lookup"><span data-stu-id="4a257-138">There are specific rules for what characters can be used as well as the minimum length of both username and password.</span></span>

> [!NOTE]
> <span data-ttu-id="4a257-139">运行此命令时，系统会提示输入用户名和密码。</span><span class="sxs-lookup"><span data-stu-id="4a257-139">You will be prompted to enter your username and password when running this command.</span></span>

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

<span data-ttu-id="4a257-140">完全创建并已准备好访问和使用 VM 后，`az vm create` 命令将输出结果。</span><span class="sxs-lookup"><span data-stu-id="4a257-140">The `az vm create` command output results once the VM has been fully created and is ready to be accessed and used.</span></span>

```Output
{
  "fqdns": "",
  "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM",
  "location": "westus2",
  "macAddress": "xx-xx-xx-xx-xx-xx",
  "powerState": "VM running",
  "privateIpAddress": "xx.x.x.x",
  "publicIpAddress": "xx.xxx.xx.xxx",
  "resourceGroup": "MyResourceGroup"
}
```

<span data-ttu-id="4a257-141">现在，请使用远程桌面和 VM 的公共 IP 地址（在 `az vm create` 的输出中返回）登录到新建的 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="4a257-141">Now log on to your newly created Windows Server VM using Remote Desktop and the public IP address of the VM (which is returned in the output from `az vm create`).</span></span>
<span data-ttu-id="4a257-142">如果使用的是基于 Windows 的系统，可以在命令行中使用 `mstsc` 命令来执行此操作：</span><span class="sxs-lookup"><span data-stu-id="4a257-142">If you are on a Windows-based system, you can do this from the command line using the `mstsc` command:</span></span>

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

<span data-ttu-id="4a257-143">提供创建 VM 时所用的同一用户名/密码组合进行登录。</span><span class="sxs-lookup"><span data-stu-id="4a257-143">Supply the same username/password combination you used when creating the VM to log in.</span></span>

## <a name="creating-other-resources-in-azure"></a><span data-ttu-id="4a257-144">在 Azure 中创建其他资源</span><span class="sxs-lookup"><span data-stu-id="4a257-144">Creating other resources in Azure</span></span>

<span data-ttu-id="4a257-145">前面已经逐步讲解了如何创建资源组、Linux VM 和 Windows Server VM。</span><span class="sxs-lookup"><span data-stu-id="4a257-145">We've now walked through how to create a Resource Group, a Linux VM, and a Windows Server VM.</span></span> <span data-ttu-id="4a257-146">还可以创建许多其他类型的 Azure 资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-146">You can create many other types of Azure resources as well.</span></span>

<span data-ttu-id="4a257-147">所有新资源是使用一致的 `az <resource type name> create` 命名模式创建的。</span><span class="sxs-lookup"><span data-stu-id="4a257-147">All new resources are created using a consistent `az <resource type name> create` naming pattern.</span></span>  <span data-ttu-id="4a257-148">例如，若要创建稍后可与新建的 VM 相关联的 Azure 网络负载均衡器，可以使用以下 create 命令：</span><span class="sxs-lookup"><span data-stu-id="4a257-148">For example, to create an Azure Network Load Balancer that we could then associate with our newly created VMs, we can use the following create command:</span></span>

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

<span data-ttu-id="4a257-149">还可以使用以下 create 命令为基础结构创建新的专用虚拟网络（在 Azure 中通常称为“VNet”）：</span><span class="sxs-lookup"><span data-stu-id="4a257-149">We could also create a new private Virtual Network (commonly referred to as a "VNet" within Azure) for our infrastructure using the following create command:</span></span>

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

<span data-ttu-id="4a257-150">Azure 和 Azure CLI 的强大之处在于，我们不仅可以使用它们来获取基于云的基础结构，而且还可以创建托管的平台服务。</span><span class="sxs-lookup"><span data-stu-id="4a257-150">What makes Azure and the Azure CLI powerful is that we can use it not just to get cloud-based infrastructure but also to create managed platform services.</span></span>  <span data-ttu-id="4a257-151">此外，可将托管的平台服务与基础结构结合使用，构建更强大的解决方案。</span><span class="sxs-lookup"><span data-stu-id="4a257-151">The managed platform services can also be combined with infrastructure to build even more powerful solutions.</span></span>

<span data-ttu-id="4a257-152">例如，可以使用 Azure CLI 创建 Azure 应用服务。</span><span class="sxs-lookup"><span data-stu-id="4a257-152">For example, you can use the Azure CLI to create an Azure AppService.</span></span>  <span data-ttu-id="4a257-153">Azure 应用服务是一个托管的平台服务，使用它能够十分方便地托管 Web 应用，而无需考虑基础结构。</span><span class="sxs-lookup"><span data-stu-id="4a257-153">Azure AppService is a managed platform service that provides a great way to host web apps without having to worry about infrastructure.</span></span>  <span data-ttu-id="4a257-154">创建 Azure 应用服务后，可以使用以下 create 命令在应用服务中创建两个新的 Azure Web 应用：</span><span class="sxs-lookup"><span data-stu-id="4a257-154">After creating the Azure AppService, you can create two new Azure Web Apps within the AppService using the following create commands:</span></span>

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan
```

<span data-ttu-id="4a257-155">了解 `az <resource type name> create` 模式的基础知识后，便可以轻松创建任何对象。</span><span class="sxs-lookup"><span data-stu-id="4a257-155">Once you understand the basics of the `az <resource type name> create` pattern, it becomes easy to create anything.</span></span> <span data-ttu-id="4a257-156">下面是一些常见的 Azure 资源类型，以及用于创建这些资源类型的相应 Azure CLI create 命令：</span><span class="sxs-lookup"><span data-stu-id="4a257-156">Following are some popular Azure resource types and the corresponding Azure CLI create commands to create them:</span></span>

```
Resource Type               Azure CLI create command
-------------               ------------------------
Resource Group              az group create
Virtual Machine             az vm create
Virtual Network             az network vnet create
Load Balancer               az network lb create
Managed Disk                az disk create
Storage account             az storage account create
Virtual Machine Scale Set   az vmss create
Azure Container Service     az acs create
Web App                     az webapp create
SQL Database Server         az sql server create
Document DB                 az documentdb create
```

<span data-ttu-id="4a257-157">请访问[参考文档](/cli/azure)，详细了解可传递给上述每个命令的其他特定于资源的参数，以及可创建的资源类型。</span><span class="sxs-lookup"><span data-stu-id="4a257-157">Visit the [Reference documentation](/cli/azure) to learn more about the additional resource-specific parameters that you can pass to each of the preceding commands and the resource types you can create.</span></span>

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a><span data-ttu-id="4a257-158">有用的提示：使用 --no-wait 优化创建操作</span><span class="sxs-lookup"><span data-stu-id="4a257-158">Useful tip: Optimizing create operations using --no-wait</span></span>

<span data-ttu-id="4a257-159">默认情况下，在使用 Azure CLI 2.0 创建资源时，`az <resource type name> create` 命令将等到资源已创建并可供使用为止。</span><span class="sxs-lookup"><span data-stu-id="4a257-159">By default when you create resources using the Azure CLI 2.0, the `az <resource type name> create` command waits until the resource has been created and is ready for you to use.</span></span>  <span data-ttu-id="4a257-160">例如，如果在创建某个 VM，则默认情况下，只有在已创建该 VM 并且可以通过 SSH 或 RDP 连接到该 VM 后，`az vm create` 才会返回。</span><span class="sxs-lookup"><span data-stu-id="4a257-160">For example, if you create a VM, the `az vm create` command will, by default, not return until the VM is created and is ready for you to SSH or RDP into it.</span></span>

<span data-ttu-id="4a257-161">之所以使用这种方案，是因为可以更方便地编写包含多个步骤和依赖项的自动化脚本（需要借助一个前置任务来确保继续下一步之前已成功完成前面的操作）。</span><span class="sxs-lookup"><span data-stu-id="4a257-161">We use this approach because it makes it easier to write automation scripts that contain multiple steps with dependencies (and need a prior task to have completed successfully before continuing).</span></span>

<span data-ttu-id="4a257-162">如果不需要等到创建资源之后才继续下一步，可以使用 `no-wait` 选项在后台启动创建操作。</span><span class="sxs-lookup"><span data-stu-id="4a257-162">If you do not need to wait on creation of a resource before continuing, you can use the `no-wait` option to start a create action in the background.</span></span> <span data-ttu-id="4a257-163">这样，就可以继续使用 CLI 执行其他命令。</span><span class="sxs-lookup"><span data-stu-id="4a257-163">You can continue using the CLI for other commands.</span></span>

<span data-ttu-id="4a257-164">例如，下面使用的 `az vm create` 将启动 VM 部署，然后以快得多的速度返回（在完全启动 VM 之前即可返回）：</span><span class="sxs-lookup"><span data-stu-id="4a257-164">For example, the following usage of the `az vm create` starts a VM deployment and then return much more quickly (and before the VM has fully booted):</span></span>

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

<span data-ttu-id="4a257-165">使用 `--no-wait` 方法有助于明显优化自动化脚本的性能。</span><span class="sxs-lookup"><span data-stu-id="4a257-165">Using the `--no-wait` approach can help you optimize the performance of your automation scripts considerably.</span></span>

## <a name="listing-resources-and-formatting-output"></a><span data-ttu-id="4a257-166">列出资源和设置输出的格式</span><span class="sxs-lookup"><span data-stu-id="4a257-166">Listing resources and formatting output</span></span>

<span data-ttu-id="4a257-167">可以使用 Azure CLI 中的 `list` 命令来查找和列出 Azure 中运行的资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-167">You can use the `list` command within the Azure CLI to find and list the resources running in Azure.</span></span>

<span data-ttu-id="4a257-168">像使用 create 命令一样，可以使用 Azure CLI 2.0 以通用的 `az <resource type name> list` 命名模式（在所有资源类型之间保持一致）列出资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-168">Like with the create command, you can list resources using the Azure CLI 2.0 using a common `az <resource type name> list` naming pattern that is consistent across all resource types.</span></span>  <span data-ttu-id="4a257-169">可以根据偏好的方式，使用各种输出格式和查询选项来筛选资源列表并为其排序。</span><span class="sxs-lookup"><span data-stu-id="4a257-169">There are various output formats and query options available to filter and sort the list of resources in the way you prefer to see them.</span></span>

<span data-ttu-id="4a257-170">例如，`az vm list` 显示所有 VM 的列表。</span><span class="sxs-lookup"><span data-stu-id="4a257-170">For example, `az vm list` shows the list of all VMs you have.</span></span>

```azurecli-interactive
az vm list
```
<span data-ttu-id="4a257-171">返回的值默认采用 JSON 格式（为了简洁起见，仅显示部分输出）。</span><span class="sxs-lookup"><span data-stu-id="4a257-171">The values returned are by default in JSON (only showing partial output for sake of brevity).</span></span>

```json
[
  {
    "availabilitySet": null,
    "diagnosticsProfile": null,
    "hardwareProfile": {
      "vmSize": "Standard_DS1_v2"
    },
    "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/DEMORG1/providers/Microsoft.Compute/virtualMachines/DemoVM010",
    "instanceView": null,
    "licenseType": null,
    "location": "westus2",
    "name": "MyLinuxVM",
    "networkProfile": {
      "networkInterfaces": [
        {
          "id": "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/demorg1/providers/Microsoft.Network/networkInterfaces/DemoVM010VMNic",
          "primary": null,
          "resourceGroup": "MyResourceGroup"
        }
      ]
    },
          ...
          ...
          ...
]
```

<span data-ttu-id="4a257-172">可以根据需要使用 `--output` 选项修改输出格式。</span><span class="sxs-lookup"><span data-stu-id="4a257-172">You can optionally modify the output format using the `--output` option.</span></span>  <span data-ttu-id="4a257-173">运行 `az vm list` 命令可以使用易于阅读的*表*格式选项查看以前创建的 Linux 和 Windows Server VM，以及 VM 的最常见属性：</span><span class="sxs-lookup"><span data-stu-id="4a257-173">Run the `az vm list` command to see both the Linux and Windows Server VMs created earlier, along with the most common properties of a VM, using the easy to read *table* format option:</span></span>

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="4a257-174">*tsv* 输出选项可以用于获取基于文本的、不带任何标头的制表符分隔格式。</span><span class="sxs-lookup"><span data-stu-id="4a257-174">The *tsv* output option can be used to get a text-based, tab-separated format without any headers.</span></span>  <span data-ttu-id="4a257-175">如果想要将输出传递到 grep 等其他基于文本的工具，此格式很有用。</span><span class="sxs-lookup"><span data-stu-id="4a257-175">This format is useful when you want to pipe the output into another text-based tool like grep.</span></span>

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
<span data-ttu-id="4a257-176">请访问有关[输出格式](format-output-azure-cli.md)的文章，详细了解用于列出资源和设置输出格式的其他方法。</span><span class="sxs-lookup"><span data-stu-id="4a257-176">Visit the [output formats](format-output-azure-cli.md) article to learn more about the additional ways to list resources and format the output.</span></span>

## <a name="querying-resources-and-shaping-outputs"></a><span data-ttu-id="4a257-177">查询资源以及为输出塑型</span><span class="sxs-lookup"><span data-stu-id="4a257-177">Querying resources and shaping outputs</span></span>

<span data-ttu-id="4a257-178">通常，我们希望能够只查询符合特定条件的资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-178">Often you want to be able to query for only those resources that meet a specific condition.</span></span>

<span data-ttu-id="4a257-179">`list` 命令提供内置支持，可让用户按资源组名称轻松筛选资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-179">The `list` command has built-in support that makes it easy to filter resources by Resource Group name.</span></span>  <span data-ttu-id="4a257-180">例如，可向 `list` 命令传递 `--ResourceGroup` 或 `-g` 参数，以便只检索特定资源组中的这些资源：</span><span class="sxs-lookup"><span data-stu-id="4a257-180">For example, you can pass either a `--ResourceGroup` or `-g` parameter to a `list` command to only retrieve those resources within a specific resource group:</span></span>


```azurecli-interactive
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

<span data-ttu-id="4a257-181">若要获得更强大的查询支持，可以使用 `--query` 参数针对*任何* `az` 命令的结果执行 JMESPath 查询。</span><span class="sxs-lookup"><span data-stu-id="4a257-181">For even more powerful querying support, you can use the `--query` parameter to execute a JMESPath query on the results of *any* `az` command.</span></span>  <span data-ttu-id="4a257-182">JMESPath 查询既可用于筛选，也可用于对任何返回结果的输出塑型。</span><span class="sxs-lookup"><span data-stu-id="4a257-182">JMESPath queries can be used both to filter as well as shape the output of any returned result.</span></span>

<span data-ttu-id="4a257-183">例如，执行以下命令可以查询任何资源组中包含字母“My”的任何 VM 资源：</span><span class="sxs-lookup"><span data-stu-id="4a257-183">For example, execute the following command to query for any VM resource within any resource group that contains the letters "My":</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup, 'MY')]"
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="4a257-184">然后，我们可以选择使用 JMESPath 查询的塑型功能来细化输出，以便同时输出不同的值。</span><span class="sxs-lookup"><span data-stu-id="4a257-184">We could then choose to further refine the output by using the shaping capability of JMESPath queries to output different values as well.</span></span>  <span data-ttu-id="4a257-185">例如，以下命令检索 VM 使用的 OS 磁盘类型，以确定 OS 是基于 Linux 还是基于 Windows：</span><span class="sxs-lookup"><span data-stu-id="4a257-185">For example, the following command retrieves the type of OS disk the VM is using to determine whether the OS is Linux or Windows based:</span></span>

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup, 'MY')].{ VMName:name, OSType:storageProfile.osDisk.osType }"
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

<span data-ttu-id="4a257-186">Azure CLI 中的 JMESPath 支持非常强大。</span><span class="sxs-lookup"><span data-stu-id="4a257-186">The JMESPath support in Azure CLI is powerful.</span></span>  <span data-ttu-id="4a257-187">请在有关[查询](query-azure-cli.md)的文章中详细了解其用法。</span><span class="sxs-lookup"><span data-stu-id="4a257-187">Learn more about how to use it in our [query](query-azure-cli.md) article.</span></span>

## <a name="deleting-resources"></a><span data-ttu-id="4a257-188">删除资源</span><span class="sxs-lookup"><span data-stu-id="4a257-188">Deleting resources</span></span>

<span data-ttu-id="4a257-189">可以使用 Azure CLI 中的 `delete` 命令删除不再需要的资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-189">You can use the `delete` command within Azure CLI to delete the resources you no longer need.</span></span> <span data-ttu-id="4a257-190">可对任何资源使用 `delete` 命令，就像使用 `create` 命令时一样。</span><span class="sxs-lookup"><span data-stu-id="4a257-190">You can use the `delete` command with any resource just like you can with the `create` command.</span></span>

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

<span data-ttu-id="4a257-191">默认情况下，CLI 会提示确认删除。</span><span class="sxs-lookup"><span data-stu-id="4a257-191">By default the CLI prompts to confirm deletion.</span></span>  <span data-ttu-id="4a257-192">对于自动化脚本，可以禁止显示此提示。</span><span class="sxs-lookup"><span data-stu-id="4a257-192">You can suppress this prompt for automated scripts.</span></span>

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

<span data-ttu-id="4a257-193">还可以使用 `delete` 命令一次性删除多个资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-193">You can also use the `delete` command to delete many resources at a time.</span></span> <span data-ttu-id="4a257-194">例如，以下命令将删除本入门教程中的所有示例使用的“MyResourceGroup”资源组中的所有资源。</span><span class="sxs-lookup"><span data-stu-id="4a257-194">For example, the following command deletes all the resources in the "MyResourceGroup" resource group that we've used for all the samples in this Get Started tutorial.</span></span>

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a><span data-ttu-id="4a257-195">获取示例</span><span class="sxs-lookup"><span data-stu-id="4a257-195">Get samples</span></span>

<span data-ttu-id="4a257-196">若要详细了解 Azure CLI 的用法，请查看适用于 [Linux VM](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Web 应用](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)和 [SQL 数据库](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)的最常用脚本。</span><span class="sxs-lookup"><span data-stu-id="4a257-196">To learn more about ways to use the Azure CLI, check out our most common scripts for [Linux VMs](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Windows VMs](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), [Web apps](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json), and [SQL Database](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json).</span></span>

## <a name="read-the-api-reference-docs"></a><span data-ttu-id="4a257-197">阅读 API 参考文档</span><span class="sxs-lookup"><span data-stu-id="4a257-197">Read the API reference docs</span></span>

[<span data-ttu-id="4a257-198">API 参考</span><span class="sxs-lookup"><span data-stu-id="4a257-198">API reference</span></span>](/cli/azure)

## <a name="get-help"></a><span data-ttu-id="4a257-199">获取帮助</span><span class="sxs-lookup"><span data-stu-id="4a257-199">Get help</span></span>

<span data-ttu-id="4a257-200">Azure CLI 提供内置的帮助文档，其内容与可从命令行运行的 Web 文档相符：</span><span class="sxs-lookup"><span data-stu-id="4a257-200">The Azure CLI has built-in help documentation, which matches our web documentation that you can run from the command line:</span></span>

```azurecli-interactive
az [command-group [command]] -h
```

<span data-ttu-id="4a257-201">例如，若要查看哪些命令和子组适用于 VM，请使用：</span><span class="sxs-lookup"><span data-stu-id="4a257-201">For example, to see what commands and subgroups are available for VMs, use:</span></span>

```azurecli-interactive
az vm -h
```

<span data-ttu-id="4a257-202">若要获取用于创建 VM 的命令的帮助，请使用：</span><span class="sxs-lookup"><span data-stu-id="4a257-202">To get help with the command to create a VM, use:</span></span>

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a><span data-ttu-id="4a257-203">从 Azure CLI 1.0 切换</span><span class="sxs-lookup"><span data-stu-id="4a257-203">Switch from Azure CLI 1.0</span></span>

<span data-ttu-id="4a257-204">如果已了解 Azure CLI 1.0 (azure.js) 的用法，可能会发现，某些命令并不完全相同。</span><span class="sxs-lookup"><span data-stu-id="4a257-204">If you already know how to use Azure CLI 1.0 (azure.js), you'll notice places where the commands aren't quite the same.</span></span>
<span data-ttu-id="4a257-205">有时，用于执行任务的命令有很大的差别。</span><span class="sxs-lookup"><span data-stu-id="4a257-205">Sometimes the commands to perform a task are significantly different.</span></span>
<span data-ttu-id="4a257-206">为了帮助从 Azure CLI 1.0 切换到 Azure CLI 2.0，我们制作了此[命令映射](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst)表。</span><span class="sxs-lookup"><span data-stu-id="4a257-206">To help you make the switch from Azure CLI 1.0 to Azure CLI 2.0, we've started this [command mapping](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst).</span></span>

## <a name="send-us-your-feedback"></a><span data-ttu-id="4a257-207">向我们发送反馈</span><span class="sxs-lookup"><span data-stu-id="4a257-207">Send us your feedback</span></span>

```azurecli-interactive
az feedback
```
