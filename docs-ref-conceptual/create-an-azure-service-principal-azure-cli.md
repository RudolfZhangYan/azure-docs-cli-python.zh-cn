---
title: 通过 Azure CLI 使用 Azure 服务主体
description: 了解如何通过 Azure CLI 创建和使用服务主体。
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 5ba7d8b0bf313a8d8ea1b20fb861c2ac0086b2be
ms.sourcegitcommit: f7554c00b5d5dca0ec716cbf996eb6654183ec37
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/26/2018
ms.locfileid: "47237606"
---
# <a name="create-an-azure-service-principal-with-azure-cli"></a>使用 Azure CLI 创建 Azure 服务主体

如果想要创建具有访问限制的单独登录名，可以通过服务主体来执行此操作。 服务主体是可与帐户关联的单独标识。 服务主体对于处理必须自动执行的应用程序和任务很有用。 本文将引导你完成创建服务主体的步骤。

## <a name="create-the-service-principal"></a>创建服务主体

使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) 命令创建服务主体。 服务主体名称不与任何现有应用程序或用户名相关联。 可以使用所选身份验证类型创建服务主体。

* `--password` 用于基于密码的身份验证。 请确保按照 [Azure Active Directory 密码规则和限制](/azure/active-directory/active-directory-passwords-policy)创建强密码。 如果未指定密码，系统将为你创建一个。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --password PASSWORD
  ```

* `--cert` 用于现有证书的基于证书的身份验证，为 PEM 或 DER 公共字符串，或用于加载文件的 `@{file}`。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile}
  ```

  可以添加 `--keyvault` 参数以指示证书存储在 Azure Key Vault 中。 在这种情况下，`--cert` 值引用 Key Vault 中证书的名称。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert CertName --keyvault VaultName
  ```

* `--create-cert` 创建用于身份验证的_自签名_证书。 如果未提供 `--cert` 参数，将会生成随机证书名称。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

  可以添加 `--keyvault` 参数以将证书存储在 Azure Key Vault 中。 使用 `--keyvault` 时，也必须提供 `--cert` 参数。

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert --cert CertName --keyvault VaultName
  ```

如果不包括指示身份验证类型的参数，则默认情况下使用 `--password`。

`create-for-rbac` 命令的输入格式如下：

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

`appId`、`tenant` 和 `password` 值用于身份验证。 搜索现有服务主体时使用 `displayName`。

> [!NOTE]
> 如果帐户没有足够的权限创建服务主体，则将显示一条错误消息指出“权限不足，无法完成该操作”。 请与 Azure Active Directory 管理员联系以创建服务主体。

## <a name="manage-service-principal-roles"></a>管理服务主体角色

Azure CLI 提供以下命令来管理角色分配。

* [az role assignment list](/cli/azure/role/assignment#az-role-assignment-list)
* [az role assignment create](/cli/azure/role/assignment#az-role-assignment-create)
* [az role assignment delete](/cli/azure/role/assignment#az-role-assignment-delete)

服务主体的默认角色是“参与者”。 此角色具有可读取和写入 Azure 帐户的完全权限，但不适合应用程序。 “读者”角色限制性更强，提供只读访问权限。  有关基于角色的访问控制 (RBAC) 和角色的详细信息，请参阅 [RBAC：内置角色](/azure/active-directory/role-based-access-built-in-roles)。

此示例将添加“读者”角色并删除“参与者”角色。

```azurecli-interactive
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

添加角色并_不_会更改以前分配的任何权限。 要限制服务主体的权限时，应始终删除“参与者”角色。

可以通过列出分配的角色来验证所做的更改。

```azurecli-interactive
az role assignment list --assignee APP_ID
```

> [!NOTE]
> 如果帐户无权分配角色，则将显示错误消息“你的帐户无权在范围 '/subscriptions/{guid}' 内执行操作 'Microsoft.Authorization/roleAssignments/write'”。请与 Azure Active Directory 管理员联系以管理角色。

## <a name="sign-in-using-the-service-principal"></a>使用服务主体登录

可以通过在 Azure CLI 中采用新服务主体的凭据登录来对其进行测试。 使用 `appId`、`tenant` 和凭据值以新服务主体身份登录。 使用创建服务主体时所用的身份验证类型。

若要使用密码登录，请以参数的形式提供密码。

```azurecli-interactive
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

若要使用证书登录，则证书必须在本地以 PEM 或 DER 文件的形式存在。

```azurecli-interactive
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```

## <a name="reset-credentials"></a>重置凭据

如果你忘记了服务主体的凭据，可以使用 [az ad sp reset-credentials](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) 命令重置凭据。 用于创建新服务主体的相同限制和选项在此处同样适用。

```azurecli-interactive
az ad sp credential reset --name APP_ID --password NEW_PASSWORD
```
