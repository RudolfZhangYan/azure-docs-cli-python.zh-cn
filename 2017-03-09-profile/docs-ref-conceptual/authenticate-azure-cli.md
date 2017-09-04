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
ms.openlocfilehash: fea893ebd55811527e0e92375ffc081a52cdbb57
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
ms.translationtype: HT
ms.contentlocale: zh-CN
---
# <a name="log-in-with-azure-cli-20"></a><span data-ttu-id="460c2-104">使用 Azure CLI 2.0 登录</span><span class="sxs-lookup"><span data-stu-id="460c2-104">Log in with Azure CLI 2.0</span></span>

<span data-ttu-id="460c2-105">使用 Azure CLI 可通过多种方式进行登录和身份验证。</span><span class="sxs-lookup"><span data-stu-id="460c2-105">There are several ways to log in and authenticate with the Azure CLI.</span></span> <span data-ttu-id="460c2-106">最简单的初始方法是通过浏览器以交互方式登录，或者通过命令行登录。</span><span class="sxs-lookup"><span data-stu-id="460c2-106">The simplest way to get started is to log in interactively through your browser, or to log in at the command line.</span></span> <span data-ttu-id="460c2-107">建议的方法是使用服务主体，这样能够创建可用于处理资源的非交互式帐户。</span><span class="sxs-lookup"><span data-stu-id="460c2-107">Our recommended approach is to use service principals, which provide a way for you to create non-interactive accounts that you can use to manipulate resources.</span></span> <span data-ttu-id="460c2-108">通过授予服务主体所需的最低适当权限，可以确保自动化脚本更加安全。</span><span class="sxs-lookup"><span data-stu-id="460c2-108">By granting just the appropriate permissions needed to a service principal, you can ensure your automation scripts are even more secure.</span></span>

<span data-ttu-id="460c2-109">使用 CLI 运行的命令可针对默认订阅运行。</span><span class="sxs-lookup"><span data-stu-id="460c2-109">Commands that you run with the CLI are run against your default subscription.</span></span>  <span data-ttu-id="460c2-110">如果你有多个订阅，可能需要[确认默认订阅](manage-azure-subscriptions-azure-cli.md)并相应地进行更改。</span><span class="sxs-lookup"><span data-stu-id="460c2-110">If you have more than one subscription, you may want to [confirm your default subscription](manage-azure-subscriptions-azure-cli.md) and change it appropriately.</span></span>

## <a name="interactive-log-in"></a><span data-ttu-id="460c2-111">交互式登录</span><span class="sxs-lookup"><span data-stu-id="460c2-111">Interactive log-in</span></span>

<span data-ttu-id="460c2-112">通过 Web 浏览器以交互方式登录。</span><span class="sxs-lookup"><span data-stu-id="460c2-112">Log in interactively from your web browser.</span></span>

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="command-line"></a><span data-ttu-id="460c2-113">命令行</span><span class="sxs-lookup"><span data-stu-id="460c2-113">Command line</span></span>

<span data-ttu-id="460c2-114">在命令行中提供凭据。</span><span class="sxs-lookup"><span data-stu-id="460c2-114">Provide your credentials on the command line.</span></span>

> [!Note]
> <span data-ttu-id="460c2-115">此方法不适用于 Microsoft 帐户或已启用双重身份验证的帐户。</span><span class="sxs-lookup"><span data-stu-id="460c2-115">This approach doesn't work with Microsoft accounts or accounts that have two-factor authentication enabled.</span></span>

```azurecli
az login -u <username> -p <password>
```

## <a name="logging-in-with-a-service-principal"></a><span data-ttu-id="460c2-116">使用服务主体登录</span><span class="sxs-lookup"><span data-stu-id="460c2-116">Logging in with a service principal</span></span>

<span data-ttu-id="460c2-117">服务主体类似于可以使用 Azure Active Directory 向其应用规则的用户帐户。</span><span class="sxs-lookup"><span data-stu-id="460c2-117">Service principals are like user accounts to which you can apply rules using Azure Active Directory.</span></span>
<span data-ttu-id="460c2-118">使用服务主体进行身份验证能够最好地保护处理资源的脚本或应用程序对你的 Azure 资源的使用。</span><span class="sxs-lookup"><span data-stu-id="460c2-118">Authenticating with a service principal is the best way to secure the usage of your Azure resources from either your scripts or applications that manipulate resources.</span></span>
<span data-ttu-id="460c2-119">可以通过 `az role` 命令集为用户定义角色。</span><span class="sxs-lookup"><span data-stu-id="460c2-119">You define the roles you want your users to have via the `az role` set of commands.</span></span>
<span data-ttu-id="460c2-120">可以在 [az 角色参考文章](https://docs.microsoft.com/cli/azure/role.md)中详细了解服务主体角色并查看其示例。</span><span class="sxs-lookup"><span data-stu-id="460c2-120">You can learn more and see examples of service principal roles in our [az role reference articles](https://docs.microsoft.com/cli/azure/role.md).</span></span>

1. <span data-ttu-id="460c2-121">如果尚未创建服务主体，请[创建一个](create-an-azure-service-principal-azure-cli.md)。</span><span class="sxs-lookup"><span data-stu-id="460c2-121">If you don't already have a service principal, [create one](create-an-azure-service-principal-azure-cli.md).</span></span>

1. <span data-ttu-id="460c2-122">使用服务主体登录。</span><span class="sxs-lookup"><span data-stu-id="460c2-122">Log in with the service principal.</span></span>

   ```azurecli
   az login --service-principal -u "http://my-app" -p <password> --tenant <tenant>
   ```

   <span data-ttu-id="460c2-123">若要获取租户，请以交互方式登录，然后从订阅中获取 tenantId。</span><span class="sxs-lookup"><span data-stu-id="460c2-123">To get your tenant, log in interactively and then get the tenantId from your subscription.</span></span>

   ```azurecli
   az login
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