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
ms.openlocfilehash: 3bd4b9c059da3b841fc0757a11bc7ce78ec64b08
ms.sourcegitcommit: 66d997a5afcf32143a4d4817ec1608cbdf58a59f
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 发行说明

## <a name="may-10-2017"></a>2017 年 5 月 10 日

版本 2.0.6

* Documentdb 已重命名为 Cosmosdb
* 添加 rdbms (mysql, postgres)
* 包括 Data Lake Analytics 和 Data Lake Store 模块。
* 包括认知服务模块。
* 包括 Service Fabric 模块。
* 包括交互式模块（重命名 az-shell）。
* 添加对 CDN 命令的支持。
* 删除容器模块。
* 添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))
* 提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))

```
azure-cli (2.0.6)

acr (2.0.4)
acs (2.0.6)
appservice (0.1.6)
batch (2.0.4)
cdn (0.0.2)
cloud (2.0.2)
cognitiveservices (0.1.2)
command-modules-nspkg (2.0.0)
component (2.0.4)
configure (2.0.6)
core (2.0.6)
cosmosdb (0.1.6)
dla (0.0.6)
dls (0.0.6)
feedback (2.0.2)
find (0.2.2)
interactive (0.3.1)
iot (0.1.5)
keyvault (2.0.4)
lab (0.0.4)
monitor (0.0.4)
network (2.0.6)
nspkg (3.0.0)
profile (2.0.4)
rdbms (0.0.1)
redis (0.2.3)
resource (2.0.6)
role (2.0.4)
sf (1.0.1)
sql (2.0.3)
storage (2.0.6)
vm (2.0.6)
```

### <a name="core"></a>核心

* 核心：捕获未注册提供程序引发的异常并自动注册   
* 性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))
* 修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))
* 改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))
* 将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))
* 登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))
* 核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))
* 核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))
* 核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))
* 核心：提高了性能
* 核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量
* 核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点

### <a name="acs"></a>ACS

* 将主计数和代理计数修复为整数而不是字符串
* 公开“az acs create --no-wait”和“az acs wait”用于异步创建
* 公开“az acs create --validate”用于试运行验证
* 在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))

### <a name="appservice"></a>应用服务

* Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等
* 将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”
* 创建“az webapp”以替换“az appservice web”（对于向后兼容，“az appservice web”将保留 2 个版本）
* 公开参数以针对 webapp create 配置部署和“运行时堆栈”
* 公开“webapp list-runtimes”
* 支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))
* 支持与预览版交换槽
* 修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))
* 将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))

### <a name="cosmosdb"></a>CosmosDB

* 将 DocumentDB 模块重命名为 CosmosDB。
* 增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理
* 增加对数据库帐户启用自动故障转移的支持
* 增加对新一致性策略 ConsistentPrefix 的支持

### <a name="data-lake-analytics"></a>数据湖分析

* Bug 修复：在筛选作业结果和状态列表时会引发错误。
* 增加对新目录项类型的支持：包。 访问方法：`az dla catalog package`
* 可从数据库内列出下列目录项（无需架构规范）：

  * 表
  * 表值函数
  * 查看
  * 表统计信息。 也可以使用架构列出，但无需指定表名。

### <a name="data-lake-store"></a>Data Lake Store

* 更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。
* 提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))
* 访问显示帮助丢失。 正在添加。 ([#2743](https://github.com/Azure/azure-cli/issues/2743))

### <a name="find"></a>查找

* 改进搜索结果，允许搜索索引的版本控制

### <a name="keyvault"></a>KeyVault

* BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项
* BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。
* 将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值
* 解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。
* KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))

### <a name="lab"></a>实验室

* 针对实验室环境添加 create、show、delete 和 list 命令。
* 添加 show 和 list 命令，查看实验室中的 ARM 模板。
* 在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。
* 添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。
* 添加命令，管理实验室中的机密。

### <a name="monitor"></a>监视

* Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))
* Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))

### <a name="network"></a>网络

* 添加 `network watcher test-connectivity` 命令。
* 添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。
* 添加对应用程序网关连接排出的支持。
* 添加对应用程序网关 WAF 规则集配置的支持。
* 添加对 ExpressRoute 路由筛选器和规则的支持。
* 添加对 TrafficManager 地理路由的支持。
* 添加对基于 VPN 连接策略的流量选择器的支持。
* 添加对 VPN 连接 IPSec 策略的支持。
* 修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。
* 添加对主动-主动 VNet 网关的支持
* 从 `network vpn-connection list/show` 命令的输出中删除 null 值。
* BC：修复 `vpn-connection create` 输出中的 bug 
* Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。
* 修复 `dns zone import` 中的 Bug：记录未正确导入。
* Bug 修复：`traffic-manager endpoint update` 不起作用。
* 添加“network watcher”预览命令。

### <a name="profile"></a>配置文件

* 支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))
* 支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))

### <a name="redis"></a>Redis

* 添加 update 命令，也增加了对 redis 缓存进行缩放的功能
* 弃用“update-settings”命令。

### <a name="resource"></a>资源

* 添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))
* 支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))
* 支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))
* 修复资源分析和 API 版本查找。 ([#2781](https://github.com/Azure/azure-cli/issues/2781))
* 为 az lock update 添加文档。 ([#2702](https://github.com/Azure/azure-cli/issues/2702))
* 尝试为不存在的组列出资源时出错。 ([#2769](https://github.com/Azure/azure-cli/issues/2769))
* [计算] 修复 VMSS 和 VM 可用性集更新的相关问题。 ([#2773](https://github.com/Azure/azure-cli/issues/2773))
* parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))

### <a name="role"></a>角色

* create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))
* RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))
* role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))
* create-for-rbac：确保已选取用户提供的密码

### <a name="sql"></a>SQL

* 添加了 az sql server list-usages 和 az sql db list-usages 命令。
* SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))

### <a name="storage"></a>存储

* 位置默认为 `storage account create` 的资源组位置。
* 添加对增量 blob 复制的支持
* 添加对大型块 blob 上传的支持
* 如果要上传的文件大于 200GB，则将块大小更改为 100MB

### <a name="vm"></a>VM

* avail-set：将 UD 和 FD 域计数设为可选

  注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：
  1. az disk/snapshot/image
  2. az vm/vmss disk
  3. 在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效
* vm/vmss：改进生成 SSH 密钥对时的警告文本
* vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))


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
可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。
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
> 某些命令模块带有“bn”或“rcn”后缀。
> 这些命令模块仍以预览版提供，将来会发布正式版。

此外，我们还提供 CLI 夜间预览版。
有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。

可通过以下方式报告夜间预览版的问题：
- 在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题
- 通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。
- 请通过命令行使用 `az feedback` 命令提供反馈。

