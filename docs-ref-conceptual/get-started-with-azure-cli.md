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
ms.openlocfilehash: 0f8e494ffdd73c666b8361488db0966af01d6876
ms.sourcegitcommit: 66d997a5afcf32143a4d4817ec1608cbdf58a59f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2017
---
# <a name="get-started-with-azure-cli-20"></a>Azure CLI 2.0 入门

Azure CLI 2.0 是 Azure 的新命令行体验，用于管理 Azure 资源。
它可以在 macOS、Linux 和 Windows 上使用。 

Azure CLI 2.0 经过优化，可用于从命令行管理 Azure 资源，以及生成可以针对 Azure Resource Manager 运行的自动化脚本。
本文将帮助你开始使用 Azure PowerShell，并讲解其重要概念。

有关最新版本的信息，请参阅[发行说明](release-notes-azure-cli.md)。

## <a name="install-azure-cli"></a>安装 Azure CLI

首先，请确保已安装最新版本的 Azure CLI：

1. 在所用的任何平台上[安装 Azure CLI 2.0](install-azure-cli.md)。

2. 若要验证安装是否成功，请从命令行运行 `az --version`。 

你应会看到计算机上安装的 Azure CLI 和其他依赖库的版本号。  
  
如果收到错误，原因可能是安装 CLI 时出现问题。 请查看 [Azure CLI 2.0 安装文章](install-azure-cli.md#troubleshooting)的“安装故障排除”部分获得指导，或者在该页面底部的讨论区中发表评论以获得帮助。

## <a name="log-in-to-azure"></a>登录 Azure

安装 Azure CLI 2.0 后，下一步是安全地将它连接到你的 Azure 帐户。 为此，可以使用 `az login` 命令。

1. 从命令行运行以下命令。

   ```azurecli-interactive
   az login
   ```
   
   此命令将输出要在下一步骤中使用的代码。 

2. 使用 Web 浏览器打开页面 [https://aka.ms/devicelogin](https://aka.ms/devicelogin)，然后输入该代码。
  
3. 出现提示时，请使用 Azure 凭据登录。

现在，可以在 Azure CLI 2.0 中针对帐户可用的 Azure 资源和服务运行命令。

## <a name="create-a-resource-group"></a>创建资源组。

完成所有设置后，让我们使用 Azure CLI 在 Azure 中创建资源。

首先，创建一个资源组。  使用 Azure 中的资源组可以管理你想要以逻辑方式分组在一起的多个资源。  例如，可为应用程序或项目创建资源组，并在其中添加虚拟机、数据库和 CDN 服务。

让我们在 Azure 的 *westus2* 区域创建一个名为“MyResourceGroup”的资源组。  为此，请键入以下命令：

```azurecli-interactive
az group create -n MyResourceGroup -l westus2 
```

创建资源组后，`az group create` 命令将输出新建的资源的多个属性：

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

## <a name="create-a-linux-virtual-machine"></a>创建 Linux 虚拟机

创建资源组后，让我们在其中创建 Linux VM。

可以运行以下命令，使用常用的 UbuntuTLS 映像创建附有两个存储磁盘（大小分别为 10GB 和 20GB）的 Linux VM：

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --data-disk-sizes-gb 10 20
```

运行上述命令时，Azure CLI 2.0 将查找存储在 ~/.ssh 目录下的 SSH 密钥对。  如果尚未在该位置存储 SSH 密钥对，可让 Azure CLI 绕过 --generate-ssh-keys 参数，自动创建一个密钥对：

```azurecli-interactive
az vm create -n MyLinuxVM -g MyResourceGroup --image UbuntuLTS --generate-ssh-keys
```

完全创建并已准备好访问和使用 VM 后，`az vm create` 命令将返回输出。 输出包含新建的 VM 的多个属性，包括其公共 IP 地址：

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

创建 VM 后，可以使用创建的 VM 的公共 IP 地址通过 **SSH** 登录到新的 Linux VM：

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

## <a name="create-a-windows-server-virtual-machine"></a>创建 Windows Server 虚拟机

现在，让我们使用 `az vm create` 命令创建基于 Windows Server 2016 Datacenter 的 VM，并将其添加到用于 Linux VM 的同一个“MyResourceGroup”资源组。  与 Linux VM 示例中一样，我们还要使用 `--data-disk-sizes-gb` 参数附加两个存储磁盘。

Azure 要求避免使用很容易猜出的用户名/密码。 在可以使用哪些字符以及用户名和密码的最小长度方面，都有特定的规则。  

> [!NOTE]
> 运行此命令时，系统会提示你输入用户名和密码。

```azurecli-interactive
az vm create -n MyWinVM -g MyResourceGroup --image Win2016Datacenter
```

完全创建并已准备好访问和使用 VM 后，`az vm create` 命令将输出结果。

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

现在，请使用远程桌面和 VM 的公共 IP 地址（在 `az vm create` 的输出中返回）登录到新建的 Windows Server VM。  
如果你使用的是基于 Windows 的系统，可以在命令行中使用 `mstsc` 命令来执行此操作：

```azurecli-interactive
mstsc /v:xx.xxx.xx.xxx
```

提供创建 VM 时所用的同一用户名/密码组合进行登录。

## <a name="creating-other-resources-in-azure"></a>在 Azure 中创建其他资源

前面已经逐步讲解了如何创建资源组、Linux VM 和 Windows Server VM。 还可以创建许多其他类型的 Azure 资源。  

所有新资源是使用一致的 `az <resource type name> create` 命名模式创建的。  例如，若要创建稍后可与新建的 VM 相关联的 Azure 网络负载均衡器，可以使用以下 create 命令：

```azurecli-interactive
az network lb create -n MyLoadBalancer -g MyResourceGroup
```

还可以使用以下 create 命令为基础结构创建新的专用虚拟网络（在 Azure 中通常称为“VNet”）：

```azurecli-interactive
az network vnet create -n MyVirtualNetwork -g MyResourceGroup --address-prefix 10.0.0.0/16
```

Azure 和 Azure CLI 的强大之处在于，我们不仅可以使用它们来获取基于云的基础结构，而且还可以创建托管的平台服务。  此外，可将托管的平台服务与基础结构结合使用，构建更强大的解决方案。

例如，可以使用 Azure CLI 创建 Azure 应用服务。  Azure 应用服务是一个托管的平台服务，使用它能够十分方便地托管 Web 应用，而无需考虑基础结构。  创建 Azure 应用服务后，可以使用以下 create 命令在应用服务中创建两个新的 Azure Web 应用：

```azurecli-interactive
# Create an Azure AppService that we can host any number of web apps within
az appservice plan create -n MyAppServicePlan -g MyResourceGroup

# Create Two Web Apps within the AppService (note: name param must be a unique DNS entry)
az webapp create -n MyWebApp43432 -g MyResourceGroup --plan MyAppServicePlan 
az webapp create -n MyWebApp43433 -g MyResourceGroup --plan MyAppServicePlan 
```

了解 `az <resource type name> create` 模式的基础知识后，便可以轻松创建任何对象。 下面是一些常见的 Azure 资源类型，以及用于创建这些资源类型的相应 Azure CLI create 命令：

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

请访问[参考文档](/azure/doc-ref-autogen)，详细了解可传递给上述每个命令的其他特定于资源的参数，以及可创建的资源类型。 

## <a name="useful-tip-optimizing-create-operations-using---no-wait"></a>有用的提示：使用 --no-wait 优化创建操作

默认情况下，在使用 Azure CLI 2.0 创建资源时，`az <resource type name> create` 命令将等到资源已创建并可供使用为止。  例如，如果你在创建某个 VM，则默认情况下，只有在已创建该 VM 并且可以通过 SSH 或 RDP 连接到该 VM 后，`az vm create` 才会返回。

之所以使用这种方案，是因为可以更方便地编写包含多个步骤和依赖项的自动化脚本（需要借助一个前置任务来确保继续下一步之前已成功完成前面的操作）。

如果你不需要等到创建资源之后才继续下一步，可以使用 `no-wait` 选项在后台启动创建操作。 这样，就可以继续使用 CLI 执行其他命令。

例如，下面使用的 `az vm create` 将启动 VM 部署，然后以快得多的速度返回（在完全启动 VM 之前即可返回）：

```azurecli-interactive
az vm create -n MyLinuxVM2 -g MyResourceGroup --image UbuntuLTS --no-wait
```

使用 `--no-wait` 方法有助于明显优化自动化脚本的性能。

## <a name="listing-resources-and-formatting-output"></a>列出资源和设置输出的格式

可以使用 Azure CLI 中的 `list` 命令来查找和列出 Azure 中运行的资源。 

像使用 create 命令一样，可以使用 Azure CLI 2.0 以通用的 `az <resource type name> list` 命名模式（在所有资源类型之间保持一致）列出资源。  你可以根据偏好的方式，使用各种输出格式和查询选项来筛选资源列表并为其排序。

例如，`az vm list` 显示你的所有 VM 的列表。   

```azurecli-interactive
az vm list 
```
返回的值默认采用 JSON 格式（为了简洁起见，仅显示部分输出）。

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

可以根据需要使用 `--output` 选项修改输出格式。  运行 `az vm list` 命令可以使用易于阅读的*表*格式选项查看以前创建的 Linux 和 Windows Server VM，以及 VM 的最常见属性：

```azurecli-interactive
az vm list --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

*tsv* 输出选项可以用于获取基于文本的、不带任何标头的制表符分隔格式。  如果你想要将输出传递到 grep 等其他基于文本的工具，此格式很有用。 

```azurecli-interactive
az vm list --output tsv
```

```
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyLinuxVM        None    None    westus2 MyLinuxVM                   None        Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
None    None            /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft.Compute/virtualMachines/MyWinVM  None    None    westus2 MyWinVM                 None    Succeeded       MyResourceGroup None                    Microsoft.Compute/virtualMachines       XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```
请访问有关[输出格式](format-output-azure-cli.md)的文章，详细了解用于列出资源和设置输出格式的其他方法。

## <a name="querying-resources-and-shaping-outputs"></a>查询资源以及为输出塑型

通常，我们希望能够只查询符合特定条件的资源。  

`list` 命令提供内置支持，可让用户按资源组名称轻松筛选资源。  例如，可向 `list` 命令传递 `--ResourceGroup` 或 `-g` 参数，以便只检索特定资源组中的这些资源：


```azurecli
az vm list -g MyResourceGroup --output table
```

```Output
Name       ResourceGroup    Location
---------  ---------------  ----------
MyLinuxVM  MyResourceGroup  westus2
MyWinVM    MyResourceGroup  westus2
```

若要获得更强大的查询支持，可以使用 `--query` 参数针对*任何* `az` 命令的结果执行 JMESPath 查询。  JMESPath 查询既可用于筛选，也可用于对任何返回结果的输出塑型。

例如，执行以下命令可以查询任何资源组中包含字母“My”的任何 VM 资源：

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')]" 
```

```Output
ResourceGroup    ProvisioningState    Name       Location    VmId
---------------  -------------------  ---------  ----------  ------------------------------------
MYRESOURCEGROUP  Succeeded            MyLinuxVM  westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
MYRESOURCEGROUP  Succeeded            MyWinVM    westus2     XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

然后，我们可以选择使用 JMESPath 查询的塑型功能来细化输出，以便同时输出不同的值。  例如，以下命令检索 VM 使用的 OS 磁盘类型，以确定 OS 是基于 Linux 还是基于 Windows：

```azurecli-interactive
az vm list --output table --query "[?contains(resourceGroup,'MY')].{ VMName:name,OSType:storageProfile.osDisk.osType }" 
```

```Output
VMName     OSType
---------  --------
MyLinuxVM  Linux
MyWinVM    Windows
```

Azure CLI 中的 JMESPath 支持非常强大。  请在有关[查询](query-azure-cli.md)的文章中详细了解其用法。

## <a name="deleting-resources"></a>删除资源

可以使用 Azure CLI 中的 `delete` 命令删除不再需要的资源。 可对任何资源使用 `delete` 命令，就像使用 `create` 命令时一样。

```azurecli-interactive
az vm delete -n MyLinuxVM -g MyResourceGroup
```

默认情况下，CLI 会提示你确认删除。  对于自动化脚本，可以禁止显示此提示。

```Output
Are you sure you want to perform this operation? (y/n): y
EndTime                           Name                                  StartTime                         Status
--------------------------------  ------------------------------------  --------------------------------  ---------
2017-02-19T02:35:56.678905+00:00  5b74ab80-9b29-4329-b483-52b406583e2f  2017-02-19T02:33:35.372769+00:00  Succeeded
```

还可以使用 `delete` 命令一次性删除多个资源。 例如，以下命令将删除本入门教程中的所有示例使用的“MyResourceGroup”资源组中的所有资源。

```azurecli-interactive
az group delete -n MyResourceGroup
```

```Output
Are you sure you want to perform this operation? (y/n): y
```

## <a name="get-samples"></a>获取示例

若要详细了解 Azure CLI 的用法，请查看适用于 [Linux VM](/azure/virtual-machines/virtual-machines-linux-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Windows VM](/azure/virtual-machines/virtual-machines-windows-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)、[Web 应用](/azure/app-service-web/app-service-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)和 [SQL 数据库](/azure/sql-database/sql-database-cli-samples?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json)的最常用脚本。

## <a name="read-the-api-reference-docs"></a>阅读 API 参考文档

[API 参考](/cli/azure)

## <a name="get-help"></a>获取帮助

Azure CLI 提供内置的帮助文档，其内容与可从命令行运行的 Web 文档相符：

```azurecli-interactive
az [command-group [command]] -h
```

例如，若要查看哪些命令和子组适用于 VM，请使用：

```azurecli-interactive
az vm -h
```

若要获取用于创建 VM 的命令的帮助，请使用：

```azurecli-interactive
az vm create -h
```

## <a name="switch-from-azure-cli-10"></a>从 Azure CLI 1.0 切换

如果你已了解 Azure CLI 1.0 (azure.js) 的用法，可能会发现，某些命令并不完全相同。
有时，用于执行任务的命令有很大的差别。
为了帮助你从 Azure CLI 1.0 切换到 Azure CLI 2.0，我们制作了此[命令映射](https://github.com/Azure/azure-cli/blob/master/doc/azure2az_commands.rst)表。

## <a name="send-us-your-feedback"></a>向我们发送你的反馈

```azurecli-interactive
az feedback
```
