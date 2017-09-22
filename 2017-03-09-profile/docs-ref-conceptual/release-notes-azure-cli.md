---
title: "Azure CLI 2.0 发行说明"
description: "了解 Azure CLI 2.0 的最新更新"
keywords: "Azure CLI 2.0, 发行说明"
author: sptramer
ms.author: sttramer
manager: douge
ms.date: 04/03/2017
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.assetid: ce0428f7-0a59-4e72-9237-d907b171af51
ms.openlocfilehash: e893b99349bbf2a5eec8af254158eb07001f1da7
ms.sourcegitcommit: f107cf927ea1ef51de181d87fc4bc078e9288e47
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/04/2017
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 发行说明

## <a name="august-28-2017"></a>2017 年 8 月 28 日

版本 2.0.15

### <a name="cli"></a>CLI

* 在 `--version` 中添加了法律说明。

### <a name="acs"></a>ACS

* 更正了预览区域。
* 正确设置了默认 `dns_name_prefix` 的格式。
* 优化了 acs 命令输出。

### <a name="appservice"></a>应用服务

* [重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致问题
* 为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名
* 公开了 `az webapp log show`
* 公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册
* 已修复：正确检测槽位设置

### <a name="iot"></a>IoT

* 修复了 #3934：策略创建操作不再清除现有的策略

### <a name="network"></a>网络

* [重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`
* [重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`
* 在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持
* 在 `lb create` 中添加了对 SKU 的支持
* 在 `public-ip create` 中添加了对 SKU 的支持

### <a name="profile"></a>配置文件

* 公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录

### <a name="service-fabric"></a>Service Fabric

* 预览版
* 简化了命令的注册表用户/密码规则
* 修复了即使在参数中传入了密码，也提示用户输入密码的问题
* 添加了对空 `registry_cred` 的支持

### <a name="storage"></a>存储

* 启用了设置 Blob 层
* 为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道
* 添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令  
* 启用了使用客户管理的密钥进行服务加密的功能
* [重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`
* 修复了 #4220：`az storage account update encryption` - 语法不匹配

### <a name="vm"></a>VM

* 修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题
* 在 `vmss create` 中添加了对 `--lb-sku` 的支持： 
* 从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称 
* 修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题
* 修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题
* 修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题


## <a name="august-15-2017"></a>2017 年 8 月 15 日

版本 2.0.14

### <a name="acs"></a>ACS

* 更正了 kubernetes 的 sshMaster0 端口号

### <a name="appservice"></a>应用服务

* 修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题

### <a name="event-grid"></a>事件网格

* 添加了 SDK 依赖项

## <a name="august-11-2017"></a>2017 年 8 月 11 日

版本 2.0.13

### <a name="acs"></a>ACS

* 添加了更多预览区域

### <a name="batch"></a>批处理

* 已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0
* 添加了新命令用于显示作业的任务计数
* 修复了处理资源文件 SAS URL 时的 bug
* Batch 帐户终结点现在支持可选的“https://”前缀
* 支持将包含 100 多个任务的列表添加到作业
* 添加了加载扩展命令模块的调试日志记录

### <a name="component"></a>组件

* 为“az component”命令添加了弃用警告

### <a name="container"></a>容器

* `create`：修复了某个环境变量中不允许等于号的问题


### <a name="data-lake-store"></a>Data Lake Store

* 启用了进度控件

### <a name="event-grid"></a>事件网格

* 初始版本

### <a name="network"></a>网络

* `lb`：修复了某些子资源名称在省略时无法正确解析的问题
* `application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题
* `application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题
* 修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误

### <a name="profile"></a>配置文件

* `account list`：添加了 `--refresh` 用于从服务器同步最新订阅

### <a name="storage"></a>存储

* 启用了使用系统分配的标识更新存储帐户的功能

### <a name="vm"></a>VM

* `availability-set`：公开了转换时的容错域计数
* 公开了 `list-skus` 命令
* 支持在不创建角色分配的情况下分配标识
* 附加数据磁盘时应用存储 SKU
* 删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU


## <a name="july-28-2017"></a>2017 年 7 月 28 日

版本 2.0.12

* 添加了容器命令
* 添加了计费和消耗模块

```
azure-cli (2.0.12)  

acr (2.0.9)  
acs (2.0.11)  
appservice (0.1.11)  
batch (3.0.3)  
billing (0.1.3)  
cdn (0.0.6)  
cloud (2.0.7)  
cognitiveservices (0.1.6)  
command-modules-nspkg (2.0.1)  
component (2.0.6)  
configure (2.0.10)  
consumption (0.1.3)  
container (0.1.7)  
core (2.0.12)  
cosmosdb (0.1.11)  
dla (0.0.10)  
dls (0.0.11)  
feedback (2.0.6)  
find (0.2.6)  
interactive (0.3.7)  
iot (0.1.10)  
keyvault (2.0.8)  
lab (0.0.9)  
monitor (0.0.8)  
network (2.0.11)  
nspkg (3.0.1)  
profile (2.0.9)  
rdbms (0.0.5)  
redis (0.2.7)  
resource (2.0.11)  
role (2.0.9)  
sf (1.0.5)  
sql (2.0.8)  
storage (2.0.11)  
vm (2.0.11) 
```

### <a name="core"></a>核心

* 输出包含证书的服务主体的 SDK 身份验证信息
* 修复了部署进度异常
* 使用当前云中的 arm 终结点创建订阅客户端
* 改进了 clouds.config 文件的并发处理 (#3636)
* 刷新每个命令执行进程的客户端请求 ID
* 使用适当的 SDK 配置文件创建订阅客户端 (#3635)
* 模板部署的进度报告 (#3510)
* 添加了通过 jmespath 查询选择表输出字段的支持 (#3581)
* 改进了分析参数的静默和包含手势的追加历史记录 (#3434)
* 使用适当的 SDK 配置文件创建订阅客户端
* 将所有现有记录文件移到最新的文件夹
* 修复了 VM/VMSS 创建操作的幂等性 (#3586)
* 命令路径不再区分大小写
* 某些布尔类型的参数不再区分大小写
* 支持登录到 Azure Stack 等本地服务器上的 ADFS
* 修复了并发写入 clouds.config 的问题 (#3255)

### <a name="acr"></a>ACR

* 针对托管注册表添加了 `show-usage` 命令
* 支持托管注册表的 SKU 更新
* 添加了包含托管 SKU 的托管注册表
* 通过 ACR Webhook 命令模块添加了托管注册表的 Webhook
* 添加了使用 acr login 命令进行 AAD 身份验证的功能
* 添加了 Docker 存储库、清单和标记的 delete 命令

### <a name="acs"></a>ACS

* API 版本 2017-07-01 的支持

### <a name="appservice"></a>应用服务

* 修复了列出 Linux Web 应用时不返回任何内容的 bug
* 支持从 ACR 检索凭据
* 删除 `appservice web` 下的所有命令
* 将命令输出中的 Docker 注册表密码掩码 (#3656)
* 确保在 macOS 上使用默认浏览器且不出错 (#3623)
* 改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)
* 公开了 `traffic-routing` 命令用于配置静态路由 (#3566)
* 添加了用于配置源代码管理的可靠性修复 (#3245)
* 从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。 需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。

### <a name="batch"></a>批处理

* 已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM
* 已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`
* 添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`

### <a name="cdn"></a>CDN

* 当 `--profile-name` 指定的配置文件不存在时，针对 `cdn endpoint list` 提供更完善的错误消息。

### <a name="cloud"></a>云

* 已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式
* 不需要库终结点
* 支持只将云注册到 ARM 资源管理器终结点
* 提供 `cloud set` 的选项用于在选择当前云时选择配置文件
* 公开了 `endpoint_vm_image_alias_doc`

### <a name="cosmosdb"></a>CosmosDB

* 修复了允许使用自定义分区键创建集合的问题
* 添加了对集合默认 TTL 的支持。

### <a name="data-lake-analytics"></a>数据湖分析

* 在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令
* 添加了 `dla job pipeline show`
* 添加了 `dla job recurrence list`

### <a name="data-lake-store"></a>Data Lake Store

* 在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持
* 更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题
* 添加了命令 `dls enable-key-vault`。 此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据

### <a name="interactive"></a>交互

* 使用缓存的命令改进启动时间
* 增大了测试覆盖率
* 增强了“?”手势，使之也可注入到下一条命令
* 修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)
* 允许使用 `--version` 作为交互模式的参数 (#3645)
* 阻止交互模式在验证填写内容中引发错误 (#3570)
* 模板部署的进度报告 (#3510)
* 添加了 `--progress` 标志
* 从填写内容中删除了 `--debug` 和 `--verbose`
* 从填写内容中删除了 `interactive` (#3324)

### <a name="iot"></a>IoT

* 修复了策略创建操作不再清除现有策略的问题。 (#3934)

### <a name="key-vault"></a>密钥保管库

* 添加了 Key Vault 恢复功能的命令：
  * `keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`
  * `keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`
  * `keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`
  * `keyvault key` 子命令 `purge`、`recover`、`list-deleted`
* 添加了服务主体的 Key Vault 集成 (#3133)
* 已将 Key Vault 数据平面更新到 0.3.2。 (#3307)

### <a name="lab"></a>实验室

* 添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持
* 为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序

### <a name="monitor"></a>监视

* 修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)
* 已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`
* 已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`
* 已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`
* 已将 `monitor alert-rules` 重命名为 `monitor alert`
* 更改了 `monitor alert create`：
  * `condition` 和 `action` 子命令不再接受 JSON
  * 添加了大量的参数来简化规则创建过程
  * `location` 不再是必需的
  * 添加了目标的名称和 ID 支持
  * 删除了 `--alert-rule-resource-name`
  * `is-enabled` 重命名为 `enabled`，不再是必需的
  * `description` 默认值现在基于提供的条件
  *  添加了示例用于帮助澄清新格式
* 支持在 `monitor metric` 命令中使用名称或 ID
* 为 `monitor alert rule update` 添加了方便的参数和示例

### <a name="network"></a>网络

* 添加了 `list-private-access-services` 命令
* 为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数
* 修复了 `application-gateway redirect-config create` 失败的问题
* 修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题
* 修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug
* 添加了 `application-gateway redirect-config` 命令
* 添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`
* 添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`
* 添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`
* 添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`
* 为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数
* 在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持
* 添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`
* 为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数
* 在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持
* 从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数
* 在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持
* 修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug
* 在 `vnet update` 中添加了对 `--dns-servers` 的支持
* 修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug
* 修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug
* 修复了 `network watcher show-topology` 默认逻辑的 bug
* 改进了 `network list-usages` 的输出格式
* 如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP
* 如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器
* 如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池
* 如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP

### <a name="profile"></a>配置文件

* 支持使用托管标识在 VM 内部登录
* 支持采用 SDK 身份验证文件格式的 `account show` 输出
* 使用 '--expanded-view' 时显示弃用警告
* 添加了 `get-access-token` 命令来提供原始 AAD 令牌
* 支持使用不包含关联订阅的用户帐户登录

### <a name="rdbms"></a>RDBMS

* 支持跨订阅列出服务器 (#3417)
* 修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)
* 修复了文档源映射并添加了 CI 任务用于验证 (#3361)
* 修复了 MySQL 和 PostgreSQL 帮助 (#3369)

### <a name="resource"></a>资源

* 改进了有关 `group deployment create` 缺少参数的提示
* 改进了 `--parameters KEY=VALUE` 语法分析
* 修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题
* 支持 `resource` 和 `managedapp` 命令的 `--ids` 参数
* 修复了一些分析和错误消息 (#3584)
* 修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`
* 添加了模板链接模板的参数检查 (#3629)
* 添加了使用 `KEY=VALUE` 语法指定部署参数的支持

### <a name="role"></a>角色

* 支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出
* 删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)
* 在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式
* 使用 `--expanded-view` 时显示弃用警告
* 在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成

### <a name="service-fabric"></a>Service Fabric
* 修复了上传时截断应用程序中的大型文件的问题 (#3666)
* 添加了 Service Fabric 命令的测试 (#3424)
* 添加了大量的 Service Fabric 命令 (#3234)

### <a name="sql"></a>SQL

* 删除了无效的 `sql server create` `--identity` 参数
* 从 `sql server create` 和 `sql server update` 命令输出中删除了密码值
* 添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`

### <a name="storage"></a>存储

* 从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)
* 启用了创建仅限 https 的存储帐户
* 更新了存储指标、日志记录和 CORS 命令 (#3495)
* 重新编写了 CORS add 命令的异常消息 (#3638) (#3362)  
* 已在下载批处理命令试运行模式下将生成器转换为列表 (#3592) 
* 修复了 Blob 下载批处理试运行问题 (#3640) (#3592)

### <a name="vm"></a>VM

* 支持配置 NSG
* 修复了无法正确配置 DNS 服务器的 bug
* 支持托管服务标识
* 修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题。
* 要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头


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
* 创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）
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
可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。可以通过命令行使用 `az feedback` 命令提供反馈。

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
