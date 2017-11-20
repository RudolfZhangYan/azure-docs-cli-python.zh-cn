---
title: "使用 Azure CLI 2.0 登录"
description: "在 Linux、Mac 或 Windows 上使用 Azure 2.0 CLI 登录。"
keywords: "Azure CLI 2.0, 登录, Azure CLI, 身份验证, 授权, 登录"
author: sptramer
ms.author: stttramer
manager: routlaw
ms.date: 11/13/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: 65becd3a-9d69-4415-8a30-777d13a0e7aa
ms.openlocfilehash: dd05868f7378673836f47e743ed4088f2efd3dca
ms.sourcegitcommit: 5db22de971cf3983785cb209d92cbed1bbd69ecf
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 11/14/2017
---
# <a name="log-in-with-azure-cli-20"></a>使用 Azure CLI 2.0 登录

使用 Azure CLI 可通过多种方式进行登录和身份验证。 最简单的初始方法是通过浏览器以交互方式登录，或者通过命令行登录。 建议的方法是使用服务主体，这样能够创建可用于处理资源的非交互式帐户。 通过授予服务主体所需的最低适当权限，可以确保自动化脚本更加安全。 

私有凭据信息均不存储在本地。 身份验证令牌由 Azure 生成并存储。 登录后，如果本地登录令牌未经使用，那么将它在 14 天内保持有效。 本地登录令牌失效时，你将需要重新进行身份验证。

登录后，将针对默认订阅运行 CLI 命令。 如果有多个订阅，可能需要[更改默认订阅](manage-azure-subscriptions-azure-cli.md)。

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
使用服务主体进行身份验证能够最好地保护处理资源的脚本或应用程序对 Azure 资源的使用。 如果没有可用的服务主体并想要创建一个，请参阅[使用 Azure CLI 创建 Azure 服务主体](create-an-azure-service-principal-azure-cli.md)。

若要使用服务主体登录，请提供用户名、密码或证书 PEM 文件，以及与服务主体关联的租户：

```azurecli-interactive
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

租户值是与服务主体关联的 Azure Active Directory 租户。 这可以是 .onmicrosoft.com 域，或租户的 Azure 对象 ID。
可使用以下命令获取当前登录名的租户对象 ID：

```azurecli
az account show --query 'tenanatId' -o tsv
```

