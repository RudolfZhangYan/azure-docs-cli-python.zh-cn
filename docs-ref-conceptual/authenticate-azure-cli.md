---
title: "使用 Azure CLI 2.0 登录"
description: "使用 Azure CLI 2.0 以交互方式登录或使用本地凭据登录"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 02/13/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: a140f8f54ad72f7f3b5e2d63e2300d0aa2c061ac
ms.sourcegitcommit: b93a19222e116d5880bbe64c03507c64e190331e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 02/15/2018
---
# <a name="log-in-with-azure-cli-20"></a>使用 Azure CLI 2.0 登录

使用 Azure CLI 可通过多种方式进行登录和身份验证。 入门的最简单方法是通过浏览器使用 Azure Cloud Shell 或 `az login` 命令以交互方式登录。
建议的方法是使用帐户权限受限制的服务主体。 通过授予服务主体所需的最低适当权限，可以确保自动化脚本更加安全。

私有凭据信息均不存储在本地。 身份验证令牌由 Azure 生成并存储。 登录后，如果登录令牌未经使用，那么将它在 14 天内保持有效。 登录令牌失效时，你将需要重新进行身份验证。

登录后，将针对默认订阅运行 CLI 命令。 如果有多个订阅，可以[更改默认订阅](manage-azure-subscriptions-azure-cli.md)。

## <a name="interactive-log-in"></a>交互式登录

通过 Web 浏览器以交互方式登录。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a>命令行

在命令行中提供凭据。

> [!Note]
> 此方法不适用于 Microsoft 帐户或已启用双重身份验证的帐户。

```azurecli
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a>使用服务主体登录

服务主体是未绑定到任何特定用户的帐户，这些帐户具有通过预定义角色分配的权限。 使用服务主体进行身份验证是编写安全脚本或程序的最佳方法，因为这样可以同时应用权限限制和本地存储的静态凭据信息。 若要了解有关服务主体的详细信息，请参阅[使用 Azure CLI 创建 Azure 服务主体](create-an-azure-service-principal-azure-cli.md)。

若要使用服务主体登录，请提供用户名、密码或证书 PEM 文件，以及与服务主体关联的租户：

```azurecli
az login --service-principal -u <user> -p <password-or-cert> --tenant <tenant>
```

租户值是与服务主体关联的 Azure Active Directory 租户。 这可以是 .onmicrosoft.com 域，或租户的 Azure 对象 ID。
可使用以下命令获取当前登录名的租户对象 ID：

```azurecli
az account show --query 'tenantId' -o tsv
```

