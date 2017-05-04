---
title: "Azure CLI 2.0 发行说明"
description: "了解 Azure CLI 2.0 的最新更新"
keywords: "Azure CLI 2.0, 发行说明"
author: rloutlaw
ms.author: routlaw
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: 56190b653ab9765017fffd1699056de7eae2db77
ms.sourcegitcommit: bcf93ad8ed8802072249cd8187cd4420da89b4c6
translationtype: HT
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 发行说明

## <a name="april-3-2017"></a>2017 年 4 月 3 日

版本 2.0.2

此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。

```
azure-cli (2.0.2)
 
acr (2.0.0)
acs (2.0.2)
appservice (0.1.2)
batch (2.0.0)
cloud (2.0.0)
component (2.0.0)
configure (2.0.2)
container (0.1.2)
core (2.0.2)
documentdb (0.1.2)
feedback (2.0.0)
find (0.0.1b1)
iot (0.1.2)
keyvault (2.0.0)
lab (0.0.1)
monitor (0.0.1)
network (2.0.2)
nspkg (2.0.0)
profile (2.0.2)
redis (0.1.1b3)
resource (2.0.2)
role (2.0.1)
sql (2.0.0)
storage (2.0.2)
vm (2.0.2)
```

### <a name="core"></a>核心

* 在默认列表中添加了 acr、实验室、监视和查找模块。
* 登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))
* 登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))
* 添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* 核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))
* 添加了有关缺少模板参数的提示。 ([#2364](https://github.com/Azure/azure-cli/pull/2364))
* 支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值
* 支持登录到特定的租户
 
### <a name="acs"></a>ACS

* [ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))
* 添加了 SSH 密钥密码提示的支持。 ([#2044](https://github.com/Azure/azure-cli/pull/2044))
* 添加了对 Windows 群集的支持。 ([#2211](https://github.com/Azure/azure-cli/pull/2211))
* 从“所有者”角色切换到“参与者”角色。 ([#2321](https://github.com/Azure/azure-cli/pull/2321))
 
### <a name="appservice"></a>应用服务

* 应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))
* 应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))
* 应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))
* 应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))
 
### <a name="datalake"></a>DataLake

* Data Lake Analytics 模块的初始版本。
* Data Lake Store 模块的初始版本。
 
### <a name="docuemntdb"></a>DocuemntDB

* DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))

### <a name="vm"></a>VM

* [计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))
* [VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))
* VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))
* 添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* 虚拟机规模集：支持使用 * 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))
* 添加了适用于 VM 和虚拟机规模集的 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))
* 允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))

## <a name="february-27-2017"></a>2017 年 2 月 27 日

版本 2.0.0

此版 Azure CLI 2.0 是第一个“正式版”。
正式版适用于以下命令模块：
- 容器服务 (ACS)
- 计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）
- 网络
- 存储

这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。
可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues)提出问题。
可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。
可以通过命令行使用 `az feedback` 命令提供反馈。

这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。

若要检查 CLI 版本，请使用 `az --version`。
输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。

```
azure-cli (2.0.0)

acs (2.0.0)
appservice (0.1.1b5)
batch (0.1.1b4)
cloud (2.0.0)
component (2.0.0)
configure (2.0.0)
container (0.1.1b4)
core (2.0.0)
documentdb (0.1.1b2)
feedback (2.0.0)
iot (0.1.1b3)
keyvault (0.1.1b5)
network (2.0.0)
nspkg (2.0.0)
profile (2.0.0)
redis (0.1.1b3)
resource (2.0.0)
role (2.0.0)
sql (0.1.1b5)
storage (2.0.0)
vm (2.0.0)
 
Python (Darwin) 2.7.10 (default, Jul 30 2016, 19:40:32) 
[GCC 4.2.1 Compatible Apple LLVM 8.0.0 (clang-800.0.34)]
```

> [!Note]
> 某些命令模块带有“b*n*”或“rc*n*”后缀。
> 这些命令模块仍以预览版提供，将来会发布正式版。

此外，我们还提供 CLI 夜间预览版。
有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。

可通过以下方式报告夜间预览版的问题：
- 在 [github 问题列表](https://github.com/azure/azure-cli/issues)中报告问题
- 通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。
- 请通过命令行使用 `az feedback` 命令提供反馈。

