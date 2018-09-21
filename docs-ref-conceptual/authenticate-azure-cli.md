---
title: 使用 Azure CLI 2.0 登录
description: 使用 Azure CLI 2.0 以交互方式登录或使用本地凭据登录
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/07/2018
ms.topic: conceptual
ms.technology: azure-cli
ms.devlang: azurecli
ms.service: active-directory
ms.component: authentication
ms.openlocfilehash: ef77f407284752ad4f4a1585f8a4036b32b3eb1b
ms.sourcegitcommit: 0e688704889fc88b91588bb6678a933c2d54f020
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/11/2018
ms.locfileid: "44388314"
---
# <a name="sign-in-with-azure-cli-20"></a>使用 Azure CLI 2.0 登录

Azure CLI 有多种身份验证类型。 最简单的入门方法是使用 [Azure Cloud Shell](/azure/cloud-shell/overview)，这样可以自动登录。 在本地，可以通过浏览器使用 `az login` 命令以交互方式登录。 编写脚本时，建议的方法是使用服务主体。 通过授予服务主体所需的最低适当权限，可以确保自动化的安全性。

CLI 不会存储任何登录信息。 身份验证令牌由 Azure 生成并存储。 登录后，如果身份验证令牌未经使用，那么它会在 90 天内保持有效。

登录后，将针对默认订阅运行 CLI 命令。 如果你有多个订阅，可以[更改默认订阅](manage-azure-subscriptions-azure-cli.md)。

## <a name="sign-in-interactively"></a>以交互方式登录

Azure CLI 的默认身份验证方法是使用 Web 浏览器和访问令牌进行登录。

[!INCLUDE [interactive_login](includes/interactive-login.md)]

## <a name="sign-in-with-credentials-on-the-command-line"></a>在命令行中使用凭据登录。

在命令行中提供 Azure 用户凭据。

> [!Note]
> 此方法不适用于 Microsoft 帐户或已启用双重身份验证的帐户。

```azurecli
az login -u <username> -p <password>
```

> [!IMPORTANT]
> 如果想要避免在控制台中显示自己的密码并以交互方式使用 `az login`，请在 `bash` 下面使用 `read -s` 命令。
>
> ```bash
> read -sp "Azure password: " AZ_PASS && echo && az login -u <username> -p $AZ_PASS
> ```
>
> 在 PowerShell 中，使用 `Read-Host -AsSecureString` cmdlet 和安全字符串转换。
>
> ```powershell
> $securePass =  Read-Host "Azure password: " -AsSecureString;
> $AzPass = [Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($securePass));
> az login -u <username> -p $AzPass;
> $AzPass = ""
> ```

## <a name="sign-in-with-a-specific-tenant"></a>使用特定租户登录

可以使用 `--tenant` 参数选择用于登录的租户。 此参数的值可以是 `.onmicrosoft.com` 域或租户的 Azure 对象 ID。 交互式登录方法和命令行登录方法都可以配合 `--tenant` 来使用。

```azurecli
az login --tenant <tenant>
```

## <a name="sign-in-with-a-service-principal"></a>使用服务主体进行登录

服务主体是未绑定到任何特定用户的帐户，这些帐户具有通过预定义角色分配的权限。 使用服务主体进行身份验证是编写安全脚本或程序的最佳方法，因为这样可以同时应用权限限制和本地存储的静态凭据信息。 若要了解有关服务主体的详细信息，请参阅[使用 Azure CLI 创建 Azure 服务主体](create-an-azure-service-principal-azure-cli.md)。

若要使用服务主体登录，需要：

* 与该服务主体关联的 URL 或名称
* 该服务主体的密码，或用于创建该服务主体的 X509 证书（PEM 格式）
* 与该服务主体关联的租户（`.onmicrosoft.com` 域或 Azure 对象 ID）

```azurecli
az login --service-principal -u <app-url> -p <password-or-cert> --tenant <tenant>
```

> [!IMPORTANT]
> 如果想要避免在控制台中显示自己的密码并以交互方式使用 `az login`，请在 `bash` 下面使用 `read -s` 命令。
>
> ```bash
> read -sp "Azure password: " AZ_PASS && echo && az login --service-principal -u <app-url> -p $AZ_PASS --tenant <tenant>
> ```
>
> 在 PowerShell 中，使用 `Read-Host -AsSecureString` cmdlet 和安全字符串转换。
>
> ```powershell
> $securePass =  Read-Host "Azure password: " -AsSecureString;
> $AzPass = [Runtime.InteropServices.Marshal]::PtrToStringAuto([Runtime.InteropServices.Marshal]::SecureStringToBSTR($securePass));
> az login --service-principal -u <app-url> -p $AzPass --tenant <tenant>;
> $AzPass = ""
> ```
