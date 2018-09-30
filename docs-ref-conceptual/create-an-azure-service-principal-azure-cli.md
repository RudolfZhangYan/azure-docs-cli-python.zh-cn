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
# <a name="create-an-azure-service-principal-with-azure-cli"></a><span data-ttu-id="a94d9-103">使用 Azure CLI 创建 Azure 服务主体</span><span class="sxs-lookup"><span data-stu-id="a94d9-103">Create an Azure service principal with Azure CLI</span></span>

<span data-ttu-id="a94d9-104">如果想要创建具有访问限制的单独登录名，可以通过服务主体来执行此操作。</span><span class="sxs-lookup"><span data-stu-id="a94d9-104">If you want to create a separate sign-in with access restrictions, you can do so through a service principal.</span></span> <span data-ttu-id="a94d9-105">服务主体是可与帐户关联的单独标识。</span><span class="sxs-lookup"><span data-stu-id="a94d9-105">Service principals are separate identities that can be associated with an account.</span></span> <span data-ttu-id="a94d9-106">服务主体对于处理必须自动执行的应用程序和任务很有用。</span><span class="sxs-lookup"><span data-stu-id="a94d9-106">Service principals are useful for working with applications and tasks that must be automated.</span></span> <span data-ttu-id="a94d9-107">本文将引导你完成创建服务主体的步骤。</span><span class="sxs-lookup"><span data-stu-id="a94d9-107">This article runs you through the steps for creating a service principal.</span></span>

## <a name="create-the-service-principal"></a><span data-ttu-id="a94d9-108">创建服务主体</span><span class="sxs-lookup"><span data-stu-id="a94d9-108">Create the service principal</span></span>

<span data-ttu-id="a94d9-109">使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) 命令创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="a94d9-109">Use the [az ad sp create-for-rbac](/cli/azure/ad/sp#az-ad-sp-create-for-rbac) command to create a service principal.</span></span> <span data-ttu-id="a94d9-110">服务主体名称不与任何现有应用程序或用户名相关联。</span><span class="sxs-lookup"><span data-stu-id="a94d9-110">The Service Principal's name isn't tied to any existing application or user name.</span></span> <span data-ttu-id="a94d9-111">可以使用所选身份验证类型创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="a94d9-111">You can create a service principal with your choice of authentication type.</span></span>

* <span data-ttu-id="a94d9-112">`--password` 用于基于密码的身份验证。</span><span class="sxs-lookup"><span data-stu-id="a94d9-112">`--password` is used for password-based authentication.</span></span> <span data-ttu-id="a94d9-113">请确保按照 [Azure Active Directory 密码规则和限制](/azure/active-directory/active-directory-passwords-policy)创建强密码。</span><span class="sxs-lookup"><span data-stu-id="a94d9-113">Make sure that you create a strong password by following the [Azure Active Directory password rules and restrictions](/azure/active-directory/active-directory-passwords-policy).</span></span> <span data-ttu-id="a94d9-114">如果未指定密码，系统将为你创建一个。</span><span class="sxs-lookup"><span data-stu-id="a94d9-114">If you don't specify a password, one is created for you.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --password PASSWORD
  ```

* <span data-ttu-id="a94d9-115">`--cert` 用于现有证书的基于证书的身份验证，为 PEM 或 DER 公共字符串，或用于加载文件的 `@{file}`。</span><span class="sxs-lookup"><span data-stu-id="a94d9-115">`--cert` is used for certificate-based authentication for an existing certificate, either as a PEM or DER public string, or `@{file}` to load a file.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert {CertStringOrFile}
  ```

  <span data-ttu-id="a94d9-116">可以添加 `--keyvault` 参数以指示证书存储在 Azure Key Vault 中。</span><span class="sxs-lookup"><span data-stu-id="a94d9-116">The `--keyvault` argument can be added to indicate the cert is stored in Azure Key Vault.</span></span> <span data-ttu-id="a94d9-117">在这种情况下，`--cert` 值引用 Key Vault 中证书的名称。</span><span class="sxs-lookup"><span data-stu-id="a94d9-117">In this case, the `--cert` value refers to the name of the certificate in Key Vault.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --cert CertName --keyvault VaultName
  ```

* <span data-ttu-id="a94d9-118">`--create-cert` 创建用于身份验证的_自签名_证书。</span><span class="sxs-lookup"><span data-stu-id="a94d9-118">`--create-cert` creates a _self-signed_ certificate for authentication.</span></span> <span data-ttu-id="a94d9-119">如果未提供 `--cert` 参数，将会生成随机证书名称。</span><span class="sxs-lookup"><span data-stu-id="a94d9-119">If the `--cert` argument isn't provided, a random certificate name is generated.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert
  ```

  <span data-ttu-id="a94d9-120">可以添加 `--keyvault` 参数以将证书存储在 Azure Key Vault 中。</span><span class="sxs-lookup"><span data-stu-id="a94d9-120">The `--keyvault` argument can be added to store the certificate in Azure Key Vault.</span></span> <span data-ttu-id="a94d9-121">使用 `--keyvault` 时，也必须提供 `--cert` 参数。</span><span class="sxs-lookup"><span data-stu-id="a94d9-121">When using `--keyvault`, the `--cert` argument is also required.</span></span>

  ```azurecli-interactive
  az ad sp create-for-rbac --name ServicePrincipalName --create-cert --cert CertName --keyvault VaultName
  ```

<span data-ttu-id="a94d9-122">如果不包括指示身份验证类型的参数，则默认情况下使用 `--password`。</span><span class="sxs-lookup"><span data-stu-id="a94d9-122">If an argument indicating the authentication type isn't included, `--password` is used by default.</span></span>

<span data-ttu-id="a94d9-123">`create-for-rbac` 命令的输入格式如下：</span><span class="sxs-lookup"><span data-stu-id="a94d9-123">The output of the `create-for-rbac` command is in the following format:</span></span>

```json
{
  "appId": "APP_ID",
  "displayName": "ServicePrincipalName",
  "name": "http://ServicePrincipalName",
  "password": ...,
  "tenant": "XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
}
```

<span data-ttu-id="a94d9-124">`appId`、`tenant` 和 `password` 值用于身份验证。</span><span class="sxs-lookup"><span data-stu-id="a94d9-124">The `appId`, `tenant`, and `password` values are used for authentication.</span></span> <span data-ttu-id="a94d9-125">搜索现有服务主体时使用 `displayName`。</span><span class="sxs-lookup"><span data-stu-id="a94d9-125">The `displayName` is used when searching for an existing service principal.</span></span>

> [!NOTE]
> <span data-ttu-id="a94d9-126">如果帐户没有足够的权限创建服务主体，则将显示一条错误消息指出“权限不足，无法完成该操作”。</span><span class="sxs-lookup"><span data-stu-id="a94d9-126">If your account does not have sufficient permissions to create a service principal, you see an error message containing "Insufficient privileges to complete the operation."</span></span> <span data-ttu-id="a94d9-127">请与 Azure Active Directory 管理员联系以创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="a94d9-127">Contact your Azure Active Directory admin to create a service principal.</span></span>

## <a name="manage-service-principal-roles"></a><span data-ttu-id="a94d9-128">管理服务主体角色</span><span class="sxs-lookup"><span data-stu-id="a94d9-128">Manage service principal roles</span></span>

<span data-ttu-id="a94d9-129">Azure CLI 提供以下命令来管理角色分配。</span><span class="sxs-lookup"><span data-stu-id="a94d9-129">The Azure CLI provides the following commands to manage role assignments.</span></span>

* [<span data-ttu-id="a94d9-130">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="a94d9-130">az role assignment list</span></span>](/cli/azure/role/assignment#az-role-assignment-list)
* [<span data-ttu-id="a94d9-131">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="a94d9-131">az role assignment create</span></span>](/cli/azure/role/assignment#az-role-assignment-create)
* [<span data-ttu-id="a94d9-132">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="a94d9-132">az role assignment delete</span></span>](/cli/azure/role/assignment#az-role-assignment-delete)

<span data-ttu-id="a94d9-133">服务主体的默认角色是“参与者”。</span><span class="sxs-lookup"><span data-stu-id="a94d9-133">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="a94d9-134">此角色具有可读取和写入 Azure 帐户的完全权限，但不适合应用程序。</span><span class="sxs-lookup"><span data-stu-id="a94d9-134">This role has full permissions to read and write to an Azure account, and is not appropriate for applications.</span></span> <span data-ttu-id="a94d9-135">“读者”角色限制性更强，提供只读访问权限。</span><span class="sxs-lookup"><span data-stu-id="a94d9-135">The **Reader** role is more restrictive, providing read-only access.</span></span>  <span data-ttu-id="a94d9-136">有关基于角色的访问控制 (RBAC) 和角色的详细信息，请参阅 [RBAC：内置角色](/azure/active-directory/role-based-access-built-in-roles)。</span><span class="sxs-lookup"><span data-stu-id="a94d9-136">For more information on Role-Based Access Control (RBAC) and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="a94d9-137">此示例将添加“读者”角色并删除“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="a94d9-137">This example adds the **Reader** role and deletes the **Contributor** one.</span></span>

```azurecli-interactive
az role assignment create --assignee APP_ID --role Reader
az role assignment delete --assignee APP_ID --role Contributor
```

<span data-ttu-id="a94d9-138">添加角色并_不_会更改以前分配的任何权限。</span><span class="sxs-lookup"><span data-stu-id="a94d9-138">Adding a role does _not_ change any previously assigned permissions.</span></span> <span data-ttu-id="a94d9-139">要限制服务主体的权限时，应始终删除“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="a94d9-139">When restricting a service principal's permissions, the __Contributor__ role should always be removed.</span></span>

<span data-ttu-id="a94d9-140">可以通过列出分配的角色来验证所做的更改。</span><span class="sxs-lookup"><span data-stu-id="a94d9-140">The changes can be verified by listing the assigned roles.</span></span>

```azurecli-interactive
az role assignment list --assignee APP_ID
```

> [!NOTE]
> <span data-ttu-id="a94d9-141">如果帐户无权分配角色，则将显示错误消息“你的帐户无权在范围 '/subscriptions/{guid}' 内执行操作 'Microsoft.Authorization/roleAssignments/write'”。请与 Azure Active Directory 管理员联系以管理角色。</span><span class="sxs-lookup"><span data-stu-id="a94d9-141">If your account doesn't have the permissions to assign a role, you see an error message that your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'." Contact your Azure Active Directory admin to manage roles.</span></span>

## <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="a94d9-142">使用服务主体登录</span><span class="sxs-lookup"><span data-stu-id="a94d9-142">Sign in using the service principal</span></span>

<span data-ttu-id="a94d9-143">可以通过在 Azure CLI 中采用新服务主体的凭据登录来对其进行测试。</span><span class="sxs-lookup"><span data-stu-id="a94d9-143">You can test the new service principal's credentials and permissions by signing in under it within the Azure CLI.</span></span> <span data-ttu-id="a94d9-144">使用 `appId`、`tenant` 和凭据值以新服务主体身份登录。</span><span class="sxs-lookup"><span data-stu-id="a94d9-144">Sign in as the new service principal using the `appId`, `tenant`, and credentials values.</span></span> <span data-ttu-id="a94d9-145">使用创建服务主体时所用的身份验证类型。</span><span class="sxs-lookup"><span data-stu-id="a94d9-145">Use the authentication type that the service principal was created with.</span></span>

<span data-ttu-id="a94d9-146">若要使用密码登录，请以参数的形式提供密码。</span><span class="sxs-lookup"><span data-stu-id="a94d9-146">To sign in with a password, provide it as an argument parameter.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --password PASSWORD --tenant TENANT_ID
```

<span data-ttu-id="a94d9-147">若要使用证书登录，则证书必须在本地以 PEM 或 DER 文件的形式存在。</span><span class="sxs-lookup"><span data-stu-id="a94d9-147">To sign in with a certificate, it must be available locally as a PEM or DER file.</span></span>

```azurecli-interactive
az login --service-principal --username APP_ID --tenant TENANT_ID --password PATH_TO_CERT
```

## <a name="reset-credentials"></a><span data-ttu-id="a94d9-148">重置凭据</span><span class="sxs-lookup"><span data-stu-id="a94d9-148">Reset credentials</span></span>

<span data-ttu-id="a94d9-149">如果你忘记了服务主体的凭据，可以使用 [az ad sp reset-credentials](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) 命令重置凭据。</span><span class="sxs-lookup"><span data-stu-id="a94d9-149">In the event that you forget the credentials for a service principal, they can be reset with the [az ad sp credential reset](/cli/azure/ad/sp/credential#az-ad-sp-credential-reset) command.</span></span> <span data-ttu-id="a94d9-150">用于创建新服务主体的相同限制和选项在此处同样适用。</span><span class="sxs-lookup"><span data-stu-id="a94d9-150">The same restrictions and options for creating a new service principal also apply here.</span></span>

```azurecli-interactive
az ad sp credential reset --name APP_ID --password NEW_PASSWORD
```
