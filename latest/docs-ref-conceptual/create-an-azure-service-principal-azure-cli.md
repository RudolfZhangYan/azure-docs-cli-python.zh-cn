---
title: "使用 Azure CLI 2.0 创建 Azure 服务主体"
description: "了解如何使用 Azure CLI 2.0 为应用或服务创建服务主体。"
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active Directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 10/12/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: a6ad5611f3e507b65e160122c87e22ec44546588
ms.sourcegitcommit: e8fe15e4f7725302939d726c75ba0fb3cad430be
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 10/27/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a>使用 Azure CLI 2.0 创建 Azure 服务主体

如果打算使用 Azure CLI 2.0 来管理应用或服务，应使用 Azure Active Directory (AAD) 服务主体而不是自己的凭据运行 CLI。
本主题逐步讲解如何使用 Azure CLI 2.0 创建安全主体。

> [!NOTE]
> 也可以通过 Azure 门户创建服务主体。
> 有关详细信息，请参阅[使用门户创建可访问资源的 Active Directory 应用程序和服务主体](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。

## <a name="what-is-a-service-principal"></a>什么是“服务主体”？

Azure 服务主体是用户创建的应用、服务和自动化工具用来访问特定 Azure 资源的安全标识。 可将它视为具有特定角色的“用户标识”（登录名和密码，或者证书），它对资源的访问权限受到严格控制。 与普通的用户标识不同，它只需能够完成特定的任务。 如果只向它授予执行管理任务所需的最低权限级别，则可以提高安全性。 

Azure CLI 2.0 支持创建基于密码的身份验证凭据和证书凭据。 在本主题中，我们将介绍这两种类型的凭据。

## <a name="verify-your-own-permission-level"></a>验证自己的权限级别

首先，在 Azure Active Directory 和 Azure 订阅中必须拥有足够的权限。 具体而言，必须能够在 Active Directory 中创建应用并向服务主体分配角色。 

检查帐户是否有足够权限的最简方法是使用门户。 请参阅[在门户中检查所需的权限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。

## <a name="create-a-service-principal-for-your-application"></a>为应用程序创建服务主体

要标识要为其创建服务主体的应用，必须提供下列其中一项：

  * 已部署的应用的唯一名称或 URI（例如示例中的“MyDemoWebApp”），或
  * 应用程序 ID，即与已部署的应用、服务或对象关联的唯一 GUID

创建服务主体时，将使用这些值来标识应用程序。

### <a name="get-information-about-your-application"></a>获取有关应用程序的信息

使用 `az ad app list` 获取有关应用程序的标识信息。

[!INCLUDE [cloud-shell-try-it.md](includes/cloud-shell-try-it.md)]

```azurecli-interactive
az ad app list --display-name MyDemoWebApp
```

```json
{
    "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "appPermissions": null,
    "availableToOtherTenants": false,
    "displayName": "MyDemoWebApp",
    "homepage": "http://MyDemoWebApp.azurewebsites.net",
    "identifierUris": [
      "http://MyDemoWebApp"
    ],
    "objectId": "bd07205b-629f-4a2e-945e-1ee5dadf610b9",
    "objectType": "Application",
    "replyUrls": []
  }
```

`--display-name` 选项可筛选返回的应用列表，以显示 `displayName` 以 MyDemoWebApp 开头的应用。

### <a name="create-a-service-principal-with-a-password"></a>创建使用密码的服务主体

使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) 和 `--password` 参数来创建使用密码的服务主体。 如果未提供角色或作用域，那么对于当前已订阅，服务主体将默认为**参与者**角色。 如果在不使用 `--password` 或 `--cert` 参数的情况下创建服务主体，则将使用密码身份验证，并且会生成一个密码。

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --password "{strong password}" 
``` 

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "name": "http://MyDemoWebApp",
  "password": {strong password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

 > [!WARNING] 
 > 请勿创建不安全的密码。  遵循 [Azure AD 密码规则和限制](/azure/active-directory/active-directory-passwords-policy)指导原则。

### <a name="create-a-service-principal-with-a-self-signed-certificate"></a>创建使用自签名证书的服务主体

使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) 和 `--create-cert` 参数来创建自签名证书。

```azurecli-interactive
az ad sp create-for-rbac --name {appId} --create-cert
```

```json
{
  "appId": "c495db57-82e0-4e2e-9369-069dff176858",
  "displayName": "azure-cli-2017-10-12-22-15-38",
  "fileWithCertAndPrivateKey": "<path>/<file-name>.pem",
  "name": "http://MyDemoWebApp",
  "password": null,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

复制 `fileWithCertAndPrivateKey` 响应的值。 这是将用于身份验证的证书文件。

有关使用证书的更多选项，请参阅 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac)。

### <a name="get-information-about-the-service-principal"></a>获取有关服务主体的信息

```azurecli-interactive
az ad sp show --id a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "displayName": "MyDemoWebApp",
  "objectId": "0ceae62e-1a1a-446f-aa56-2300d176659bde",
  "objectType": "ServicePrincipal",
  "servicePrincipalNames": [
    "http://MyDemoWebApp",
    "a487e0c1-82af-47d9-9a0b-af184eb87646d"
  ]
}
```

### <a name="sign-in-using-the-service-principal"></a>使用服务主体登录

现在可以使用来自 `az ad sp show` 的 *appId* 以及密码或已创建证书的路径，作为应用的新服务主体登录。  提供 `az ad sp create-for-rbac` 结果中的*租户*值。

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password-or-path-to-cert} --tenant {tenant}
``` 

成功登录后，会看到以下输出：

```json
[
  {
    "cloudName": "AzureCloud",
    "id": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
    "isDefault": true,
    "state": "Enabled",
    "tenantId": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX",
    "user": {
      "name": "https://MyDemoWebApp",
      "type": "servicePrincipal"
    }
  }
]
```

使用 `id`、`password` 和 `tenant` 值作为凭据来运行应用。 

## <a name="managing-roles"></a>管理角色 

> [!NOTE]
> Azure 基于角色的访问控制 (RBAC) 是定义和管理用户及服务主体的角色时使用的模型。
> 角色具有关联的权限集，这些权限确定主体可以读取、访问、写入或管理的资源。
> 有关 RBAC 和角色的详细信息，请参阅 [RBAC：内置角色](/azure/active-directory/role-based-access-built-in-roles)。

Azure CLI 2.0 提供以下命令用于管理角色分配：

* [az role assignment list](/cli/azure/role/assignment#list)
* [az role assignment create](/cli/azure/role/assignment#create)
* [az role assignment delete](/cli/azure/role/assignment#delete)

服务主体的默认角色是“参与者”。 由于该角色的权限比较广泛，对于要与 Azure 服务交互的应用，该角色可能不是最合适的选择。 “读取者”角色受到严格的限制，非常适合用于只读访问。 可以查看有关角色特定的权限的详细信息，或者如何通过 Azure 门户创建自定义角色。

本示例将“读取者”角色添加到前面的示例，并删除“参与者”角色：

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

通过列出当前分配的角色来验证更改：

```azurecli-interactive
az role assignment list --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d
```

```json
{
    "id": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleAssignments/c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "name": "c27f78a7-9d3b-404b-ab59-47818f9af9ac",
    "properties": {
      "principalId": "790525226-46f9-4051-b439-7079e41dfa31",
      "principalName": "http://MyDemoWebApp",
      "roleDefinitionId": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac/providers/Microsoft.Authorization/roleDefinitions/acdd72a7-3385-48ef-bd42-f606fba81ae7",
      "roleDefinitionName": "Reader",
      "scope": "/subscriptions/34345f33-0398-4a99-a42b-f6613d1664ac"
    },
    "type": "Microsoft.Authorization/roleAssignments"
}
```

> [!NOTE] 
> 如果帐户没有足够权限来分配角色，将看到一条错误消息。
> 该消息声明用户的帐户“无权在作用域 '/subscriptions/{guid}' 执行操作 'Microsoft.Authorization/roleAssignments/write'”。
   
## <a name="change-the-credentials-of-a-security-principal"></a>更改安全主体的凭据

良好的安全做法是定期审查权限并更新密码。 此外，随着应用的变化，可能还需要管理和修改安全凭据。

### <a name="reset-a-service-principal-password"></a>重置服务主体密码

使用 `az ad sp reset-credentials` 可以重置服务主体的当前密码。

```azurecli-interactive
az ad sp reset-credentials --name 20bce7de-3cd7-49f4-ab64-bb5b443838c3 --password {new-password}
```

```json
{
  "appId": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "name": "a487e0c1-82af-47d9-9a0b-af184eb87646d",
  "password": {new-password},
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

如果省略 `--password` 选项，CLI 将生成安全密码。
