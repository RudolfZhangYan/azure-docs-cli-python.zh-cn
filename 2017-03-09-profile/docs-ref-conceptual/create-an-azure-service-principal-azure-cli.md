---
title: "使用 Azure CLI 2.0 创建 Azure 服务主体"
description: "了解如何使用 Azure CLI 2.0 为应用或服务创建服务主体。"
keywords: Azure CLI 2.0, Azure Active Directory, Azure Active Directory, AD, RBAC
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 02/27/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: fab89cb8-dac1-4e21-9d34-5eadd5213c05
ms.openlocfilehash: f37df762a9a605ea649b215f38f2e9866614f4ac
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2017
---
# <a name="create-an-azure-service-principal-with-azure-cli-20"></a><span data-ttu-id="e2a0e-104">使用 Azure CLI 2.0 创建 Azure 服务主体</span><span class="sxs-lookup"><span data-stu-id="e2a0e-104">Create an Azure service principal with Azure CLI 2.0</span></span>

<span data-ttu-id="e2a0e-105">如果打算使用 Azure CLI 2.0 来管理应用或服务，应使用 Azure Active Directory (AAD) 服务主体而不是自己的凭据运行 CLI。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-105">If you plan to manage your app or service with Azure CLI 2.0, you should run it under an Azure Active Directory (AAD) service principal rather than your own credentials.</span></span>
<span data-ttu-id="e2a0e-106">本主题逐步讲解如何使用 Azure CLI 2.0 创建安全主体。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-106">This topic steps you through creating a security principal with Azure CLI 2.0.</span></span>

> [!NOTE]
> <span data-ttu-id="e2a0e-107">也可以通过 Azure 门户创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-107">You can also create a service principal through the Azure portal.</span></span>
> <span data-ttu-id="e2a0e-108">有关详细信息，请参阅[使用门户创建可访问资源的 Active Directory 应用程序和服务主体](/azure/azure-resource-manager/resource-group-create-service-principal-portal)。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-108">Read [Use portal to create Active Directory application and service principal that can access resources](/azure/azure-resource-manager/resource-group-create-service-principal-portal) for more details.</span></span>

## <a name="what-is-a-service-principal"></a><span data-ttu-id="e2a0e-109">什么是“服务主体”？</span><span class="sxs-lookup"><span data-stu-id="e2a0e-109">What is a 'service principal'?</span></span>

<span data-ttu-id="e2a0e-110">Azure 服务主体是用户创建的应用、服务和自动化工具用来访问特定 Azure 资源的安全标识。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-110">An Azure service principal is a security identity used by user-created apps, services, and automation tools to access specific Azure resources.</span></span> <span data-ttu-id="e2a0e-111">可将它视为具有特定角色的“用户标识”（登录名和密码，或者证书），它对资源的访问权限受到严格控制。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-111">Think of it as a 'user identity' (login and password or certificate) with a specific role, and tightly controlled permissions to access your resources.</span></span> <span data-ttu-id="e2a0e-112">与普通的用户标识不同，它只需能够完成特定的任务。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-112">It only needs to be able to do specific things, unlike a general user identity.</span></span> <span data-ttu-id="e2a0e-113">如果只向它授予执行管理任务所需的最低权限级别，则可以提高安全性。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-113">It improves security if you only grant it the minimum permissions level needed to perform its management tasks.</span></span> 

<span data-ttu-id="e2a0e-114">目前，Azure CLI 2.0 仅支持创建基于密码的身份验证凭据。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-114">Right now, Azure CLI 2.0 only supports the creation of password-based authentication credentials.</span></span> <span data-ttu-id="e2a0e-115">本主题介绍如何创建具有特定密码的服务主体，并根据需要向它分配特定的角色。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-115">In this topic, we cover creating a service principal with a specific password, and optionally assigning specific roles to it.</span></span>

## <a name="verify-your-own-permission-level"></a><span data-ttu-id="e2a0e-116">验证自己的权限级别</span><span class="sxs-lookup"><span data-stu-id="e2a0e-116">Verify your own permission level</span></span>

<span data-ttu-id="e2a0e-117">首先，在 Azure Active Directory 和 Azure 订阅中必须拥有足够的权限。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-117">First, you must have sufficient permissions in both your Azure Active Directory and your Azure subscription.</span></span> <span data-ttu-id="e2a0e-118">具体而言，必须能够在 Active Directory 中创建应用并向服务主体分配角色。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-118">Specifically, you must be able to create an app in the Active Directory, and assign a role to the service principal.</span></span> 

<span data-ttu-id="e2a0e-119">检查帐户是否有足够权限的最简方法是使用门户。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-119">The easiest way to check whether your account has adequate permissions is through the portal.</span></span> <span data-ttu-id="e2a0e-120">请参阅[在门户中检查所需的权限](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions)。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-120">See [Check required permission in portal](/azure/azure-resource-manager/resource-group-create-service-principal-portal#required-permissions).</span></span>

## <a name="create-a-service-principal-for-your-application"></a><span data-ttu-id="e2a0e-121">为应用程序创建服务主体</span><span class="sxs-lookup"><span data-stu-id="e2a0e-121">Create a service principal for your application</span></span>

<span data-ttu-id="e2a0e-122">要标识要为其创建服务主体的应用，必须提供下列其中一项：</span><span class="sxs-lookup"><span data-stu-id="e2a0e-122">You must have one of the following to identify the app you want to create a service principal for:</span></span>

  * <span data-ttu-id="e2a0e-123">已部署的应用的唯一名称或 URI（例如示例中的“MyDemoWebApp”），或</span><span class="sxs-lookup"><span data-stu-id="e2a0e-123">The unique name or URI of your deployed app (such as "MyDemoWebApp" in the examples), or</span></span>
  * <span data-ttu-id="e2a0e-124">应用程序 ID，即与已部署的应用、服务或对象关联的唯一 GUID</span><span class="sxs-lookup"><span data-stu-id="e2a0e-124">the Application ID, the unique GUID associated with your deployed app, service, or object</span></span>

<span data-ttu-id="e2a0e-125">创建服务主体时，将使用这些值来标识应用程序。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-125">These values identify your application when creating a service principal.</span></span>

### <a name="get-information-about-your-application"></a><span data-ttu-id="e2a0e-126">获取有关应用程序的信息</span><span class="sxs-lookup"><span data-stu-id="e2a0e-126">Get information about your application</span></span>

<span data-ttu-id="e2a0e-127">使用 `az ad app list` 获取有关应用程序的标识信息。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-127">Get identity information about your application with the `az ad app list`.</span></span>

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

<span data-ttu-id="e2a0e-128">`--display-name` 选项可筛选返回的应用列表，以显示 `displayName` 以 MyDemoWebApp 开头的应用。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-128">The `--display-name` option filters the returned list of apps to show those with `displayName` starting with MyDemoWebApp.</span></span>

### <a name="create-the-service-principal"></a><span data-ttu-id="e2a0e-129">创建服务主体</span><span class="sxs-lookup"><span data-stu-id="e2a0e-129">Create the service principal</span></span>

<span data-ttu-id="e2a0e-130">使用 [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) 创建服务主体。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-130">Use [az ad sp create-for-rbac](/cli/azure/ad/sp#create-for-rbac) to create the service principal.</span></span> 

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
 > <span data-ttu-id="e2a0e-131">请勿创建不安全的密码。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-131">Don't create an insecure password.</span></span>  <span data-ttu-id="e2a0e-132">遵循 [Azure AD 密码规则和限制](/azure/active-directory/active-directory-passwords-policy)指导原则。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-132">Follow the [Azure AD password rules and restrictions](/azure/active-directory/active-directory-passwords-policy) guidance.</span></span>

### <a name="get-information-about-the-service-principal"></a><span data-ttu-id="e2a0e-133">获取有关服务主体的信息</span><span class="sxs-lookup"><span data-stu-id="e2a0e-133">Get information about the service principal</span></span>

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

### <a name="sign-in-using-the-service-principal"></a><span data-ttu-id="e2a0e-134">使用服务主体登录</span><span class="sxs-lookup"><span data-stu-id="e2a0e-134">Sign in using the service principal</span></span>

<span data-ttu-id="e2a0e-135">现在，可以使用 `az ad sp show` 输出的 *appId* 和*密码*，以应用的新服务主体身份登录。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-135">You can now log in as the new service principal for your app using the *appId* and *password* from `az ad sp show`.</span></span>  <span data-ttu-id="e2a0e-136">提供 `az ad sp create-for-rbac` 结果中的*租户*值。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-136">Supply the *tenant* value from the results of `az ad sp create-for-rbac`.</span></span>

```azurecli-interactive
az login --service-principal -u a487e0c1-82af-47d9-9a0b-af184eb87646d --password {password} --tenant {tenant}
``` 

<span data-ttu-id="e2a0e-137">成功登录后，会看到以下输出：</span><span class="sxs-lookup"><span data-stu-id="e2a0e-137">You will see this output after a successful sign-on:</span></span>

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

<span data-ttu-id="e2a0e-138">使用 `id`、`password` 和 `tenant` 值作为凭据来运行应用。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-138">Use the `id`, `password`, and `tenant` values as the credentials for running your app.</span></span> 

## <a name="managing-roles"></a><span data-ttu-id="e2a0e-139">管理角色</span><span class="sxs-lookup"><span data-stu-id="e2a0e-139">Managing roles</span></span> 

> [!NOTE]
> <span data-ttu-id="e2a0e-140">Azure 基于角色的访问控制 (RBAC) 是定义和管理用户及服务主体的角色时使用的模型。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-140">Azure Role-Based Access Control (RBAC) is a model for defining and managing roles for user and service principals.</span></span>
> <span data-ttu-id="e2a0e-141">角色具有关联的权限集，这些权限确定主体可以读取、访问、写入或管理的资源。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-141">Roles have sets of permissions associated with them, which determine the resources a principal can read, access, write, or manage.</span></span>
> <span data-ttu-id="e2a0e-142">有关 RBAC 和角色的详细信息，请参阅 [RBAC：内置角色](/azure/active-directory/role-based-access-built-in-roles)。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-142">For more information on RBAC and roles, see [RBAC: Built-in roles](/azure/active-directory/role-based-access-built-in-roles).</span></span>

<span data-ttu-id="e2a0e-143">Azure CLI 2.0 提供以下命令用于管理角色分配：</span><span class="sxs-lookup"><span data-stu-id="e2a0e-143">The Azure CLI 2.0 provides the following commands to manage role assignments:</span></span>

* [<span data-ttu-id="e2a0e-144">az role assignment list</span><span class="sxs-lookup"><span data-stu-id="e2a0e-144">az role assignment list</span></span>](/cli/azure/role/assignment#list)
* [<span data-ttu-id="e2a0e-145">az role assignment create</span><span class="sxs-lookup"><span data-stu-id="e2a0e-145">az role assignment create</span></span>](/cli/azure/role/assignment#create)
* [<span data-ttu-id="e2a0e-146">az role assignment delete</span><span class="sxs-lookup"><span data-stu-id="e2a0e-146">az role assignment delete</span></span>](/cli/azure/role/assignment#delete)

<span data-ttu-id="e2a0e-147">服务主体的默认角色是“参与者”。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-147">The default role for a service principal is **Contributor**.</span></span> <span data-ttu-id="e2a0e-148">由于该角色的权限比较广泛，对于要与 Azure 服务交互的应用，该角色可能不是最合适的选择。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-148">It may not be the best choice for an app's interactions with Azure services, given its broad permissions.</span></span> <span data-ttu-id="e2a0e-149">“读取者”角色受到严格的限制，非常适合用于只读访问。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-149">The **Reader** role is more restrictive and is a good choice for read-only access.</span></span> <span data-ttu-id="e2a0e-150">可以查看有关角色特定的权限的详细信息，或者如何通过 Azure 门户创建自定义角色。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-150">You can view details on role-specific permissions or create custom ones through the Azure portal.</span></span>

<span data-ttu-id="e2a0e-151">本示例将“读取者”角色添加到前面的示例，并删除“参与者”角色：</span><span class="sxs-lookup"><span data-stu-id="e2a0e-151">In this example, add the **Reader** role to our prior example, and delete the **Contributor** one:</span></span>

```azurecli-interactive
az role assignment create --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Reader
az role assignment delete --assignee a487e0c1-82af-47d9-9a0b-af184eb87646d --role Contributor
```

<span data-ttu-id="e2a0e-152">通过列出当前分配的角色来验证更改：</span><span class="sxs-lookup"><span data-stu-id="e2a0e-152">Verify the changes by listing the currently assigned roles:</span></span>

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
> <span data-ttu-id="e2a0e-153">如果帐户没有足够权限来分配角色，将看到一条错误消息。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-153">If your account does not have sufficient permissions to assign a role, you see an error message.</span></span>
> <span data-ttu-id="e2a0e-154">该消息声明用户的帐户“无权在作用域 '/subscriptions/{guid}' 执行操作 'Microsoft.Authorization/roleAssignments/write'”。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-154">The message states your account "does not have authorization to perform action 'Microsoft.Authorization/roleAssignments/write' over scope '/subscriptions/{guid}'."</span></span>
   
## <a name="change-the-credentials-of-a-security-principal"></a><span data-ttu-id="e2a0e-155">更改安全主体的凭据</span><span class="sxs-lookup"><span data-stu-id="e2a0e-155">Change the credentials of a security principal</span></span>

<span data-ttu-id="e2a0e-156">良好的安全做法是定期审查权限并更新密码。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-156">It's a good security practice to review permissions and update passwords regularly.</span></span> <span data-ttu-id="e2a0e-157">此外，随着应用的变化，可能还需要管理和修改安全凭据。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-157">You may also want to manage and modify the security credentials as your app changes.</span></span>

### <a name="reset-a-service-principal-password"></a><span data-ttu-id="e2a0e-158">重置服务主体密码</span><span class="sxs-lookup"><span data-stu-id="e2a0e-158">Reset a service principal password</span></span>

<span data-ttu-id="e2a0e-159">使用 `az ad sp reset-credentials` 可以重置服务主体的当前密码。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-159">Use `az ad sp reset-credentials` to reset the current password for the service principal.</span></span>

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

<span data-ttu-id="e2a0e-160">如果省略 `--password` 选项，CLI 将生成安全密码。</span><span class="sxs-lookup"><span data-stu-id="e2a0e-160">The CLI generates a secure password if you leave out the `--password` option.</span></span>
