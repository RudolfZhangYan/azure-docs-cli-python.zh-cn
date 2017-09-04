---
title: "使用 Azure CLI 2.0 登录"
description: "在 Linux、Mac 或 Windows 上使用 Azure 2.0 CLI 登录。"
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
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: 4ab4f0de38614eff00f55bad96ea886bb007f3c0
ms.sourcegitcommit: 4fd631a58cf19c494162510d073fbbbdf0524d16
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/05/2017
---
# <a name="log-in-with-azure-cli-20"></a>使用 Azure CLI 2.0 登录

使用 Azure CLI 可通过多种方式进行登录和身份验证。 最简单的初始方法是通过浏览器以交互方式登录，或者通过命令行登录。 建议的方法是使用服务主体，这样能够创建可用于处理资源的非交互式帐户。 通过授予服务主体所需的最低适当权限，可以确保自动化脚本更加安全。

使用 CLI 运行的命令可针对默认订阅运行。  如果你有多个订阅，可能需要[确认默认订阅](manage-azure-subscriptions-azure-cli.md)并相应地进行更改。

## <a name="interactive-log-in"></a>交互式登录

通过 Web 浏览器以交互方式登录。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>命令行

在命令行中提供凭据。

> [!Note]
> 此方法不适用于 Microsoft 帐户或已启用双重身份验证的帐户。

```azurecli-interactive
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>使用服务主体登录

服务主体类似于可以使用 Azure Active Directory 向其应用规则的用户帐户。
使用服务主体进行身份验证能够最好地保护处理资源的脚本或应用程序对你的 Azure 资源的使用。
可以通过 `az role` 命令集为用户定义角色。
可以在 [az 角色参考文章](https://docs.microsoft.com/cli/azure/role.md)中详细了解服务主体角色并查看其示例。

1. 如果尚未创建服务主体，请[创建一个](create-an-azure-service-principal-azure-cli.md)。

1. 使用服务主体登录。

   ```azurecli-interactive
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   若要获取租户，请以交互方式登录，然后从订阅中获取 tenantId。

   ```azurecli
   az account show
   ```

   ```json
   {
       "environmentName": "AzureCloud",
       "id": "********-****-****-****-************",
       "isDefault": true,
       "name": "Pay-As-You-Go",
       "state": "Enabled",
       "tenantId": "********-****-****-****-************",
       "user": {
       "name": "********",
       "type": "user"
       }
   }
   ```