---
title: Azure CLI 2.0 发行说明
description: 了解 Azure CLI 2.0 的最新更新
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 06/01/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 64db2b58ca883518757d8e189bf7263ed818b283
ms.sourcegitcommit: 1a38729d6ae93c49137b3d49b6a9ec8a75eff190
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/19/2018
ms.locfileid: "36262652"
---
# <a name="azure-cli-20-release-notes"></a>Azure CLI 2.0 发行说明

## <a name="june-19-2018"></a>2018 年 6 月 19 日

版本 2.0.38

### <a name="core"></a>核心

* 为大多数命令增加了对 `--subscription` 的全局支持

### <a name="acr"></a>ACR

* 增加了 `azure-storage-blob` 作为依赖项
* 更改了 `acr build-task create` 的默认 CPU 配置，允许使用 2 核心

### <a name="acs"></a>ACS

* 更新了 `aks use-dev-spaces` 命令的选项。 增加了 `--update` 支持
* 更改了 `aks get-credentials --admin`，不替换 `$HOME/.kube/config` 中的用户上下文
* 公开了托管群集上的只读 `nodeResourceGroup` 属性
* 修复了 `acs browse` 命令错误
* 将 `--connector-name` 设置为 `aks install-connector`、`aks upgrade-connector` 和 `aks remove-connector` 的可选项
* 为 `aks install-connector` 增加了新的 Azure 容器实例区域
* 为 helm 版本名称增加了规范化位置，并为 `aks install-connector` 增加了节点名称 

### <a name="appservice"></a>应用服务

* 增加了对更新版 urllib 的支持
* 为 `functionapp create` 增加了支持，可以使用外部资源组的应用服务计划

### <a name="batch"></a>Batch

* 删除了 `azure-batch-extensions` 依赖项

### <a name="batch-ai"></a>Batch AI

* 添加了对工作区的支持。 可以通过工作区将群集、文件服务器和试验按组分组，去除了对可以创建的资源数的限制
* 增加了对试验的支持。 可以通过试验将作业按集合分组，去除了对已创建作业的数目限制
* 增加了为 Docker 容器中运行的作业配置 `/dev/shm` 的支持
* 增加了 `batchai cluster node exec` 和 `batchai job node exec` 命令。 这些命令允许在节点上直接执行任何命令，提供用于端口转发的功能。
* 为 `batchai` 命令增加了对 `--ids` 的支持 
* [重大更改] 所有群集和文件服务器必须在工作区创建
* [重大更改] 作业必须在试验中创建
* [重大更改] 从 `cluster create` 和 `job create` 命令中删除了 `--nfs-resource-group`。 若要装载属于其他工作区/资源组的 NFS，请通过 `--nfs` 选项提供文件服务器的 ARM ID
* [重大更改] 从 `job create` 命令中删除了 `--cluster-resource-group`。 若要在属于其他工作区/资源组的群集上提交作业，请通过 `--cluster` 选项提供群集的 ARM ID
* [重大更改] 从作业、群集和文件服务器中删除了 `location` 特性。 位置现在是工作区的特性。
* [重大更改] 从 `job create`、`cluster create` 和 `file-server create` 命令中删除了 `--location`
* [重大更改] 更改了短选项的名称，使接口更一致：
 - [`--config`, `-c`] 已重命名为 [`--config-file`, `-f`]
 - [`--cluster`, `-r`] 已重命名为 [`--cluster`, `-c`]
 - [`--cluster`, `-n`] 已重命名为 [`--cluster`, `-c`]
 - [`--job`, `-n`] 已重命名为 [`--job`, `-j`]

### <a name="maps"></a>地图

* [重大更改] 更改了 `maps account create`，要求通过交互式提示或 `--accept-tos` 标志接受《服务条款》

### <a name="network"></a>网络

* 为 `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571) 增加了对 `https` 的支持
* 修复了 `--endpoint-status` 区分大小写的问题。 [#6502](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a>预留

* [重大更改] 为 `reservations catalog show` 增加了必需参数 `ReservedResourceType`
* 为 `reservations catalog show` 增加了参数 `Location`
* [重大更改] 从 `ReservationProperties` 中删除了 `kind`
* [重大更改] 已在 `Catalog` 中将 `capabilities` 重命名为 `sku_properties`
* [重大更改] 从 `Catalog` 中删除了 `size` 和 `tier` 属性
* 为 `reservations reservation update` 增加了参数 `InstanceFlexibility`

### <a name="role"></a>角色

* 改进了错误处理

### <a name="sql"></a>SQL

* 修复了针对不可供订阅使用的位置运行 `az sql db list-editions` 时出现的令人困惑的错误

### <a name="storage"></a>存储

* 更改了 `storage blob download` 的表输出，使之更为可读

### <a name="vm"></a>VM

* 针对 `vm create` 中的加速网络支持，改进了 refine vm size check
* 增加了针对 `vmss create` 的警告：默认的 VM 大小将从 `Standard_D1_v2` 切换为 `Standard_DS1_v2`
* 为 `[vm|vmss] extension set` 增加了 `--force-update`，即使在配置未变的情况下也可以更新扩展

## <a name="june-13-2018"></a>2018 年 6 月 13 日

版本 2.0.37

### <a name="core"></a>核心

* 改进了交互式遥测

## <a name="june-13-2018"></a>2018 年 6 月 13 日

版本 2.0.36

### <a name="aks"></a>AKS

* 为 `aks create` 添加了高级网络选项
* 为 `aks create` 添加了参数以启用监视和 HTTP 路由 
* 为 `aks create` 添加了 `--no-ssh-key` 参数
* 为 `aks create` 添加了 `--enable-rbac` 参数
* [PREVIEW] 为 `aks create` 添加了对 Azure Active Directory 身份验证的支持

### <a name="appservice"></a>应用服务

* 修复了不兼容 urllib 版本的问题

## <a name="june-5-2018"></a>2018 年 6 月 5 日

版本 2.0.35

### <a name="interactive"></a>交互

* 添加了对交互模式的依赖项的限制

## <a name="june-5-2018"></a>2018 年 6 月 5 日

版本 2.0.34

### <a name="core"></a>核心

* 增加了对跨租户资源引用的支持
* 增强了遥测数据上传可靠性

### <a name="acr"></a>ACR

* 增加了对 VSTS 充当远程源位置的支持
* 添加了 `acr import` 命令

### <a name="aks"></a>AKS

* 更改了 `aks get-credentials`，可以使用更安全的文件系统权限来创建 kube 配置文件

### <a name="batch"></a>Batch

* 修复了池列表表格式设置中的 Bug [[问题 #4378](https://github.com/Azure/azure-cli/issues/4378)]

### <a name="iot"></a>IOT

* 增加了对创建基本层 IoT 中心的支持

### <a name="network"></a>网络

* 改进了 `network vnet peering`

### <a name="policy-insights"></a>策略见解

* 初始版本

### <a name="arm"></a>ARM

* 增加了 `account management-group` 命令。

### <a name="sql"></a>SQL

* 增加了新的托管实例命令：
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* 增加了新的托管数据库命令：
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a>存储

* 增加了可以从文件扩展名推断且适用于 json 和 javascript 的额外 mimetype

### <a name="vm"></a>VM

* 更改了 `vm list-skus`，可以使用固定列并可添加表明要删除 `Tier` 和 `Size` 的警告
* 为 `vm create` 添加了 `--accelerated-networking` 选项
* 为 `identity create` 添加了 `--tags`

## <a name="may-22-2018"></a>2018 年 5 月 22 日

版本 2.0.33

### <a name="core"></a>核心

* 增加了对在文件名中扩展 `@` 的支持

### <a name="acs"></a>ACS

* 增加了新的 Dev-Spaces 命令：`aks use-dev-spaces` 和 `aks remove-dev-spaces`
* 修复了帮助消息中的拼写错误

### <a name="appservice"></a>应用服务

* 改进了泛型更新命令
* 增加了对 `webapp deployment source config-zip` 的异步支持

### <a name="container"></a>容器

* 增加了对以 yaml 格式导出容器组的支持
* 增加了对使用 yaml 文件创建/更新容器组的支持

### <a name="extension"></a>分机

* 改进了扩展的删除方式

### <a name="interactive"></a>交互

* 更改了日志记录，在完成时将分析器静音
* 改进了错误的帮助缓存的处理

### <a name="keyvault"></a>KeyVault

* 修复了 keyvault 命令，使之可以在 Cloud Shell 或 VM 中与标识一起使用

### <a name="network"></a>网络

* 修复了 `network watcher show-topology` 无法与 vnet 和/或子网名称一起使用的问题 [#6326](https://github.com/Azure/azure-cli/issues/6326)
* 修复了某些 `network watcher` 命令宣称未为区域启用网络观察程序而实际上却已经启用的问题 [#6264](https://github.com/Azure/azure-cli/issues/6264)

### <a name="sql"></a>SQL

* [重大更改] 更改了从 `db` 和 `dw` 命令返回的响应对象：
    * 已将 `serviceLevelObjective` 属性重命名为 `currentServiceObjectiveName`
    * 删除了 `currentServiceObjectiveId` 和 `requestedServiceObjectiveId` 属性 
    * 已将 `maxSizeBytes` 属性更改为整数值而不是字符串
* [重大更改] 已将下面的 `db` 和 `dw` 属性更改为只读：
    * `requestedServiceObjectiveName`。  若要更新，请使用 `--service-objective` 参数或设置 `sku.name` 属性
    * `edition`。 若要更新，请使用 `--edition` 参数或设置 `sku.tier` 属性
    * `elasticPoolName`。 若要更新，请使用 `--elastic-pool` 参数或设置 `elasticPoolId` 属性
* [重大更改] 已将下面的 `elastic-pool` 属性更改为只读：
    * `edition`。 若要更新，请使用 `--edition` 参数
    * `dtu`。 若要更新，请使用 `--capacity` 参数
    *  `databaseDtuMin`。 若要更新，请使用 `--db-min-capacity` 参数
    *  `databaseDtuMax`。 若要更新，请使用 `--db-max-capacity` 参数
* 为 `db`、`dw` 和 `elastic-pool` 命令增加了 `--family` 和 `--capacity` 参数。
* 为 `db`、`dw` 和 `elastic-pool` 命令增加了表格式化程序。

### <a name="storage"></a>存储

* 增加了 `--account-name` 参数的补全选项
* 修复了 `storage entity query` 的问题

### <a name="vm"></a>VM

* [重大更改] 从 `vm create` 中删除了 `--write-accelerator`。 可以通过 `vm update` 或 `vm disk attach` 访问同一支持
* 修复了 `[vm|vmss] extension` 中的扩展映像匹配问题
* 为 `vm create` 添加了 `--boot-diagnostics-storage`，可以捕获启动日志
* 为 `[vm|vmss] update` 添加了 `--license-type`

## <a name="may-7-2018"></a>2018 年 5 月 7 日

版本 2.0.32

### <a name="core"></a>核心

* 修复了使用证书从服务主体帐户检索机密时引发未处理异常的问题
* 增加了对位置参数的有限支持
* 修复了 `--query` 无法与 `--ids` 一起使用的问题。 [#5591](https://github.com/Azure/azure-cli/issues/5591)
* 改进了使用 `--ids` 时通过命令执行的管道方案。 支持在指定查询的情况下使用 `-o tsv`，或者在不指定查询的情况下使用 `-o json`
* 增加了在用户的命令中存在拼写错误的情况下，针对错误提供命令建议的功能
* 改进了用户键入 `az ''` 时出现的错误
* 增加了针对命令模块和扩展自定义资源类型的功能

### <a name="acr"></a>ACR

* 增加了 ACR 生成命令
* 改进了“找不到资源”类型的错误消息
* 改进了资源创建性能和错误处理
* 改进了 acr 登录非标准控制台和 WSL
* 改进了存储库命令错误消息
* 更新了表列和排序

### <a name="acs"></a>ACS

* 增加了“`az aks` 是预览版服务”警告
* 修复了未指定 `--aci-resource-group` 时 `aks install-connector` 中的权限问题

### <a name="ams"></a>AMS

* 初始版本 - 管理 Azure 媒体服务资源

### <a name="appservice"></a>应用服务

* 修复了提供 `--slot` 时 `webapp delete` 中的 Bug
* 从 `webapp auth update` 删除了 `--runtime-version`
* 增加了对 min\_tls\_version & https2.0 的支持
* 增加了对多容器的支持

### <a name="batch-ai"></a>Batch AI

* 更改了 `batchai create cluster`，以便遵循在群集的配置文件中配置的 VM 优先级

### <a name="cognitive-services"></a>认知服务

* 修复了在 `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603) 的示例中的拼写错误

### <a name="consumption"></a>消耗

* 增加了预算 API 的新命令

### <a name="container"></a>容器

* 删除了在映像名称中包括注册表服务器时对 `container create` 命令的 `--registry-server` 参数的要求

### <a name="cosmos-db"></a>Cosmos DB

* 引入针对 Azure CLI 的 VNET 支持 - Cosmos DB

### <a name="dms"></a>DMS

* 初始版本 - 为 Azure SQL 迁移方案增加了对 SQL 的支持

### <a name="extension"></a>分机

* 修复了停止显示扩展元数据的 Bug

### <a name="interactive"></a>交互

* 允许交互式补全选项使用位置参数
* 增强用户键入 '\' 时的输出的用户友好性
* 修复了在没有帮助的情况下参数的补全问题
* 修复了命令组的说明问题

### <a name="lab"></a>实验室

* 修复了 Knack 转换的回归问题

### <a name="network"></a>网络

* [重大更改] 删除了以下项的 `--ids` 参数： 
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a>配置文件

* 修复了 `disk create` 源检测问题
* [重大更改] 删除了不再使用的 `--msi-port` 和 `--identity-port`
* 修复了 `account get-access-token` 短摘要中的拼写错误

### <a name="redis"></a>Redis

* 弃用 `redis patch-schedule patch-schedule show` 而改用 `redis patch-schedule show`
* 弃用 `redis list-all`。 此功能已加入 `redis list` 中
* 弃用 `redis import-method` 而改用 `redis import`
* 为各种命令增加了对 `--ids` 的支持

### <a name="role"></a>角色

* [重大更改] 删除了已弃用的 `ad sp reset-credentials`

### <a name="storage"></a>存储

* 在源 SAS 和帐户密钥未指定的情况下，允许将目标 SAS 令牌应用到源，以便进行 Blob 复制
* 公开了用于 Blob 上传和下载的 --socket-timeout 参数
* 将以路径分隔符开头的 Blob 名称视为相对路径
* 允许 `storage blob copy --source-sas` 以查询字符“?”开头
* 修复了 `storage entity query --marker` 问题，接受“键=值”列表

### <a name="vm"></a>VM

* 修复了非托管 Blob URI 上的检测逻辑无效的问题
* 增加了在没有用户提供的服务主体的情况下进行磁盘加密的功能
* [重大更改] 请勿使用 VM“ManagedIdentityExtension”来寻求 MSI 支持
* 增加了对 `vmss` 使用逐出策略的支持
* [重大更改] 从以下项删除了 `--ids`：
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* 增加了写入加速器支持 
* 添加了 `vmss perform-maintenance`
* 修复了 `vm diagnostics set` 问题，可以可靠地检测 VM 的 OS 类型
* 更改了 `vm resize`，系统会检查请求的大小是否不同于当前设置的大小，只在二者有变化时进行更新


## <a name="april-10-2018"></a>2018 年 4 月 10 日

版本 2.0.31

### <a name="acr"></a>ACR

* 改进了 wincred 回退错误处理

### <a name="acs"></a>ACS

* 更改了 aks 创建的 SPN，使其有效期达到 5 年

### <a name="appservice"></a>应用服务

* [重大更改]: Removed `assign-identity`
* 修复了 Web 应用计划不存在导致的未捕获异常

### <a name="batchai"></a>BatchAI

* 添加了对 2018-03-01 API 的支持

 - 作业级装载
 - 使用机密值的环境变量
 - 性能计数器设置
 - 报告作业特定的路径段
 - 支持“列出文件”API 中的子文件夹
 - 使用情况和限制报告
 - 允许为 NFS 服务器指定缓存类型
 - 支持自定义映像
 - 添加了 pyTorch 工具包支持

* 添加了 `job wait` 命令，以允许等待作业完成和报告作业退出代码
* 添加了 `usage show` 命令，用于列出不同区域的当前 Batch AI 资源使用情况和限制
* 支持国家云
* 添加了作业命令行参数，以便除了装载配置文件以外，还能装载作业级别的文件系统
* 添加了更多选项用于自定义群集 - VM 优先级、子网、自动缩放群集的初始节点计数，以及指定自定义映像
* 添加了命令行选项用于指定 Batch AI 托管 NFS 的缓存类型
* 简化了在配置文件中指定装载文件系统的方法。 现在，可以省略 Azure 文件共享和 Azure Blob 容器的凭据 - CLI 将会使用通过命令行参数提供的或通过环境变量指定的存储帐户密钥来填充缺少的凭据，或者从 Azure 存储查询密钥（如果存储帐户属于当前订阅）
* 作业完成后（成功、失败、已终止或已删除），作业文件流命令现在会自动完成
* 改进了 `show` 操作的 `table` 输出
* 添加了 `--use-auto-storage` 选项用于创建群集。 使用此选项可以更方便地管理存储帐户，以及将 Azure 文件共享和 Azure Blob 容器装载到群集
* 为 `cluster create` 和 `file-server create` 添加了 `--generate-ssh-keys` 选项
* 添加了通过命令行提供节点设置任务的功能
* [重大更改]移动了 `job file` 组下面的 `job stream-file` 和 `job list-files` 命令
* [重大更改]已将 `file-server create` 命令中的 `--admin-user-name` 重命名为 `--user-name`，使其与 `cluster create` 命令一致

### <a name="billing"></a>计费

* 添加了登记帐户命令

### <a name="consumption"></a>消耗

* 添加了 `marketplace` 命令
* [重大更改] 已将 `reservations summaries` 重命名为 `reservation summary`
* [重大更改] 已将 `reservations details` 重命名为 `reservation detail`
* [重大更改]删除了 `reservation` 命令的 `--reservation-order-id` 和 `--reservation-id` 短选项
* [重大更改]删除了 `reservation summary` 命令的 `--grain` 短选项
* [重大更改]删除了 `pricesheet` 命令的 `--include-meter-details` 短选项

### <a name="container"></a>容器

* 添加了 git 存储库卷装载参数 `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` 和 `--gitrepo-mount-path`
* 修复了 [#5926](https://github.com/Azure/azure-cli/issues/5926)：指定 --container-name 时 `az container exec` 失败

### <a name="extension"></a>分机

* 已将分配检查消息更改为调试级别

### <a name="interactive"></a>交互

* 更改为在命令不可识别时停止完成
* 添加了创建命令子树之前和之后所用的事件挂钩
* 添加了 `--ids` 参数补全

### <a name="network"></a>网络

* 修复了 [#5936](https://github.com/Azure/azure-cli/issues/5936)：无法设置 `application-gateway create` 标记
* 添加了参数 `--auth-certs`，以附加 `application-gateway http-settings [create|update]` 的身份验证证书。 [#4910](https://github.com/Azure/azure-cli/issues/4910)
* 添加了 `ddos-protection` 命令用于创建 DDoS 保护计划 
* 为 `vnet [create|update]` 添加了 `--ddos-protection-plan` 支持，以便将 VNet 关联到 DDoS 保护计划
* 修复了 `network route-table [create|update]` 中 `--disable-bgp-route-propagation` 标志的问题
* 删除了 `network lb [create|update]` 的虚拟参数 `--public-ip-address-type` 和 `--subnet-type`
* 为 `network dns zone [import|export]` 和 `network dns record-set txt add-record` 添加了采用 RFC 1035 转义序列的 TXT 记录支持

### <a name="profile"></a>配置文件

* 在 `account list` 中添加了 Azure 经典帐户支持
* [重大更改]删除了 `--msi` & `--msi-port` 参数

### <a name="rdbms"></a>RDBMS

* 添加了 `georestore` 命令
* 删除了 `create` 命令的存储大小限制

### <a name="resource"></a>资源

* 在 `policy definition create` 中添加了对 `--metadata` 的支持
* 为 `policy definition update` 添加了对 `--metadata`、`--set`、`--add` 和 `--remove` 的支持

### <a name="sql"></a>SQL

* 添加了 `sql elastic-pool op list` 和 `sql elastic-pool op cancel`

### <a name="storage"></a>存储

* 改进了有关连接字符串格式不当的错误消息

### <a name="vm"></a>VM

* 为 `vmss create` 添加了配置平台容错域计数的支持
* 已将 `vmss create` 的默认值更改为区域性、大型或禁用单一位置组的规模集的标准负载均衡器
* [重大更改]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret`
* 为 `vm create` 添加了对公共 IP SKU 的支持
* 为 `vm secret format` 添加了 `--keyvault` 和 `--resource-group` 参数，以便在命令无法解析保管库 ID 的情况下提供支持。 [#5718](https://github.com/Azure/azure-cli/issues/5718)
* 改进了当资源组的位置不支持区域时，`[vm|vmss create]` 发生的错误


## <a name="march-27-2018"></a>2018 年 3 月 27 日

版本 2.0.30

### <a name="core"></a>核心

* 为帮助中标记为预览版的扩展显示消息

### <a name="acs"></a>ACS

* 为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误

### <a name="appservice"></a>应用服务

* 为 `webapp update` 添加了仅限 HTTPS 的支持
* 为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持

### <a name="backup"></a>备份

* 添加了新命令 `az backup protection isenabled-for-vm`。 此命令可用于检查 VM 是否已由订阅中的任何保管库备份
* 为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：
  * `backup container show`
  * `backup item set-policy`
  * `backup item show`
  * `backup job show`
  * `backup job stop`
  * `backup job wait`
  * `backup policy delete`
  * `backup policy get-default-for-vm`
  * `backup policy list-associated-items`
  * `backup policy set`
  * `backup policy show`
  * `backup protection backup-now`
  * `backup protection disable`
  * `backup protection enable-for-vm`
  * `backup recoverypoint show`
  * `backup restore files mount-rp`
  * `backup restore files unmount-rp`
  * `backup restore restore-disks`
  * `backup vault delete`
  * `backup vault show`
* 更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式

### <a name="container"></a>容器

* 添加了 `container exec` 命令。 在正在运行的容器组的容器中执行命令
* 允许将表输出用于创建和更新容器组

### <a name="extension"></a>分机

* 为 `extension add` 添加了消息（如果扩展处于预览状态）
* 更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据
* [重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据

### <a name="interactive"></a>交互

* 已将“完成”更改为在执行命令表加载后立即激活
* 修复了使用 `--style` 参数时的 bug
* 交互式词法分析器在命令表转储后实例化（如果缺失）
* 改进了完成符支持

### <a name="lab"></a>实验室

* 修复了 `create environment` 命令的 bug

### <a name="monitor"></a>监视

* 为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)
* 修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表
* 为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)

### <a name="network"></a>网络

* 添加了对专用 DNS 区域的支持

### <a name="profile"></a>配置文件

* 为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告

### <a name="rdbms"></a>RDBMS

* 添加了业务模型 GA API 版本 2017-12-01

### <a name="resource"></a>资源

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a>角色

* 为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持
* 更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID
* 添加了凭据管理命令 `ad sp credential [reset|list|delete]`
* [重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”
* 为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持

### <a name="storage"></a>存储

* 修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题
* 修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题

### <a name="vm"></a>VM

* 针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告
* 为 `vm [snapshot|image]` 添加了区域弹性支持
* 更改了磁盘实例视图以更好地报告加密状态
* [重大更改] 更改了 `vm extension delete` 以不再返回输出

## <a name="march-13-2018"></a>2018 年 3 月 13 日

版本 2.0.29

### <a name="acr"></a>ACR

* 为 `repository delete` 添加了对 `--image` 参数的支持
* 弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数
* 添加了 `repository untag` 命令以在不删除数据的情况下删除标记

### <a name="acs"></a>ACS

* 添加了 `aks upgrade-connector` 命令以升级现有连接器
* 更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML

### <a name="advisor"></a>顾问

* [重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`
* [重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`
* [重大更改] 删除了 `advisor recommendation generate` 
* 为 `advisor recommendation list` 添加了 `--refresh` 参数
* 添加了 `advisor recommendation show` 命令

### <a name="appservice"></a>应用服务

* 弃用了 `[webapp|functionapp] assign-identity`
* 添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`

### <a name="eventhubs"></a>Eventhubs

* 初始版本

### <a name="extension"></a>分机

* 添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误

### <a name="interactive"></a>交互

* 修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录
* 修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录
* 修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”
* 修复了用于长时间运行的操作的进度指示器

### <a name="monitor"></a>监视

* 弃用了 `monitor autoscale-settings` 命令
* 添加了 `monitor autoscale` 命令
* 添加了 `monitor autoscale profile` 命令
* 添加了 `monitor autoscale rule` 命令

### <a name="network"></a>网络

* [重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数
* 删除了以下命令的某些错误默认值：
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* 添加了 `network watcher connection-monitor` 命令
* 为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`

### <a name="profile"></a>配置文件

* 弃用了 `az login` 的 `--msi` 参数
* 为 `az login` 添加了 `--identity` 参数以替换 `--msi`

### <a name="rdbms"></a>RDBMS

* [预览] 已更改为使用 API 2017-12-01-preview

### <a name="service-bus"></a>服务总线

* 初始版本

### <a name="storage"></a>存储

* 修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云
* 修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误

### <a name="vm"></a>VM

* 为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存
* 弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`
* 添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令
* 已将 `vmss create` 中的默认优先级更改为 None

## <a name="february-27-2018"></a>2018 年 2 月 27 日

版本 2.0.28

### <a name="core"></a>核心

* 已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题
* 添加了对具有自定义密钥的扩展遥测的支持
* 为 `--debug` 添加了 HTTP 日志记录

### <a name="acs"></a>ACS

* 已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图
* 已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题
* 已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`
* 从 `aks get-versions` 中删除了弃用通知

### <a name="appservice"></a>应用服务

* 针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新
* 已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU

### <a name="cognitive-services"></a>认知服务

* 更新了创建新的认知服务帐户时的“通知”

### <a name="consumption"></a>消耗

* 为 pricesheet API 添加了新命令
* 更新了现有“使用情况详细信息”和“预订详细信息”格式

### <a name="container"></a>容器

* 为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密

### <a name="network"></a>网络

* 修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端

### <a name="resource"></a>资源

* 更改了 `group deployment export` 以在失败时显示部分模板和错误

### <a name="role"></a>角色

* 添加了 `role assignment list-changelogs` 以允许审核服务主体角色

### <a name="sql"></a>SQL

* 添加了在创建和更新时对数据库和弹性池的区域冗余支持

### <a name="storage"></a>存储

* 已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix

### <a name="vm"></a>VM

* 添加了对在单个 VMSS 实例上附加/分离磁盘的支持


## <a name="february-13-2018"></a>2018 年 2 月 13 日

版本 2.0.27

### <a name="core"></a>核心

* 更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证

### <a name="acs"></a>ACS

* [重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`
* 更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本
* 更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本
* 更新了引用由 AKS 生成的服务主体的帮助消息
* 更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”
* 改进了定位 `az aks browse` 的仪表板 pod 时的可靠性
* 修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误
* 向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`

### <a name="appservice"></a>应用服务

* 修复了由于空引用 `webapp [backup|restore]` 失败的问题
* 通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持

### <a name="cdn"></a>CDN

* 添加了 `cdn custom-domain [enable-https|disable-https]` 命令

### <a name="container"></a>容器

* 向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志
* 添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器

### <a name="cosmosdb"></a>CosmosDB

* 添加了对设置功能的支持

### <a name="extension"></a>分机

* 向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持
* 向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持

### <a name="feedback"></a>反馈

* 将扩展信息添加到了遥测数据

### <a name="interactive"></a>交互

* 修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题
* 修复了缺少参数补全时的回归问题

### <a name="iot"></a>IoT

* 修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题
* 修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题
* 向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持
* 更改了 `iot hub create` 以允许指定分区数

### <a name="monitor"></a>监视

* 修复了 `az monitor log-profiles create` 命令

### <a name="network"></a>网络

* 修复了以下命令的 `--tags` 选项：
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a>配置文件

* 在交互模式中启用了 `az login`

### <a name="resource"></a>资源

* 重新添加了 `feature show`

### <a name="role"></a>角色

* 为 `ad app update` 添加了 `--available-to-other-tenants` 参数

### <a name="sql"></a>SQL

* 添加了 `sql server dns-alias` 命令
* 添加了 `sql db rename`
* 向所有 sql 命令添加了对 `--ids` 参数的支持

### <a name="storage"></a>存储

* 添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除

### <a name="vm"></a>VM

* 修复了无法完全初始化 VM 加密时出现的崩溃
* 添加了启用 MSI 时的主体 ID 输出
* 固定 `vm boot-diagnostics get-boot-log`


## <a name="january-31-2018"></a>2018 年 1 月 31 日

版本 2.0.26

### <a name="core"></a>核心

* 添加了支持在 MSI 上下文中检索原始令牌
* 删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串
* 添加了将使用配置的默认值时显示的警告更改为信息级别条目。 请使用 `--verbose` 查看
* 为等待命令添加了进度指示器

### <a name="acs"></a>ACS

* 说明了 `--disable-browser` 参数
* 改进了 `--vm-size` 参数的 tab 键补全功能

### <a name="appservice"></a>应用服务

* 固定 `webapp log [tail|download]`
* 删除了对 Web 应用和函数的 `kind` 检查

### <a name="cdn"></a>CDN

* 修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题

### <a name="cosmosdb"></a>CosmosDB

* 修复了故障转移策略的参数说明

### <a name="interactive"></a>交互

* 修复了不再显示命令选项补全的问题

### <a name="network"></a>网络

* 向 `application-gateway create` 添加了对 `--cert-password` 的保护
* 修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题
* 向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护
* 修复了运行 `asg create` 时出现的缺少客户端问题
* 向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数
* 修复了 `dns zone export` 存在的以下问题：
  * 修复了未正确导出长 TXT 记录的问题
  * 修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题
* 修复了使用 `dns zone import` 某些记录会导入两次的问题 
* 已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令

### <a name="profile"></a>配置文件

* 修复了 `get-access-token`，使其在 VM 中使用标识正常工作

### <a name="resource"></a>资源

* 修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告

### <a name="storage"></a>存储

* 修复了将存储 V1 帐户迁移到存储 V2 时出现的问题
* 为所有上传/下载命令添加了进度报告
* 修复了 `storage account check-name` 不显示“-n”参数选项的 bug  
* 向 `blob [list|show]` 的表输出添加了“snapshot”列
* 修复了需要作为整数分析的各种参数的 bug

### <a name="vm"></a>VM

* 添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM
* 修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令
* [预览] 向 VMSS 添加了对“低”优先级的支持
* 向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护


## <a name="january-17-2018"></a>2018 年 1 月 17 日

版本 2.0.25

### <a name="acr"></a>ACR

* 添加了发生 Windows 凭据错误时执行 acr 登录回退的功能
* 启用了注册表日志

### <a name="acs"></a>ACS

* 修复了 `get-credentials` 命令
* 删除了 SPN 角色要求

### <a name="appservice"></a>应用服务

* 修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug
* 为 `browse` 添加了自定义 URL 支持
* 修复了 `log tail` 的槽位支持

### <a name="backup"></a>备份

* 将 `backup item list` 的 `--container-name` 选项更改为可选
* 为 `backup restore restore-disks` 添加了存储帐户选项
* 修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写
* 修复了容器名称无效时命令失败的问题
* 已将 `backup item list` 更改为默认包含“Health Status”

### <a name="batch"></a>Batch

* 已将 `batch login` 更改为返回身份验证详细信息

### <a name="cloud"></a>云

* 已更改为在云中设置 `--profile` 时不需要终结点

### <a name="consumption"></a>消耗

* 添加了用于预留的新命令：`consumption reservations summaries` 和 `consumption reservations details`

### <a name="event-grid"></a>事件网格

* [重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`
* [重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`
* [重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。 请改用 `eventgrid event-subscription show --include-full-endpoint-url`
* 添加了命令 `eventgrid topic update`
* 添加了命令 `eventgrid event-subscription update`
* 为 `eventgrid topic` 命令添加了 `--ids` 参数
* 添加了主题名称的 Tab 键补全支持

### <a name="interactive"></a>交互

* 修复了无法在 Python 2.x 中使用交互模式的问题
* 修复了启动时出错的问题
* 修复了无法在交互模式下运行某些命令的问题

### <a name="iot"></a>IoT

* 添加了对设备预配服务的支持
* 在命令和命令帮助中添加了弃用消息
* 添加了 IoT 检查，以告知用户有 IoT 扩展可用

### <a name="monitor"></a>监视

* 添加了多诊断设置支持。 `az monitor diagnostic-settings create` 现在必需 `--name` 参数。
* 添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别

### <a name="network"></a>网络

* 修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题
* 在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持

### <a name="profile"></a>配置文件

* 添加了使用用户分配的标识进行登录的支持

### <a name="role"></a>角色

* 为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询

### <a name="service-fabric"></a>Service Fabric

* 在创建群集时生成的验证响应中添加了详细错误
* 修复了运行多个命令时出现的缺少客户端问题

### <a name="vm"></a>VM

* [预览] `vmss` 的跨区域支持
* [重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器
* [重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`
* [预览] 添加了 OS 磁盘交换支持
* 添加了使用其他订阅中的 VM 映像的支持
* 为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数
* 修复了 `[vm|vmss] create` 出错问题
* 修复了 `vm image list --all` 导致资源使用过度的问题

## <a name="december-19-2017"></a>2017 年 12 月 19 日

版本 2.0.23

* 添加了使用用户分配的标识进行登录的支持

### <a name="container"></a>容器

* 纠正了容器日志参数的错误顺序

### <a name="network"></a>网络

* 为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数
* 为 `public-ip [create|update]` 添加了 `--ip-tags` 参数

### <a name="storage"></a>存储

* 添加了对存储 V2 的支持

### <a name="vm"></a>VM

* [预览] 添加了对 VM 和 VMSS 的用户分配标识的支持


## <a name="december-5-2017"></a>2017 年 12 月 5 日

版本 2.0.22

* 已删除 `az component` 命令。 请改用 `az extension`

### <a name="core"></a>核心
* 已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us
* 已修复持续重新发送遥测数据的问题

### <a name="acs"></a>ACS

* 已添加 `aks install-connector` 和 `aks remove-connector` 命令
* 已改进 `acs create` 的错误报告
* 已修复不带完全限定路径的 `aks get-credentials -f` 的用法

### <a name="advisor"></a>顾问

* 初始版本

### <a name="appservice"></a>应用服务

* 已修复使用 `webapp config ssl upload` 时的证书名称生成问题
* 已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用
* 已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值

### <a name="consumption"></a>消耗

* 已添加对 API 版本 2017-11-30 的支持

### <a name="container"></a>容器

* 已修复默认端口回归

### <a name="monitor"></a>监视

* 已添加对指标命令的多维支持

### <a name="resource"></a>资源

* 为 `resource show` 添加了 `--include-response-body` 参数

### <a name="role"></a>角色

* 已将“经典”管理员的默认分配显示添加到 `role assignment list`
* 已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖
* 已改进 `ad sp create-for-rbac` 的错误报告

### <a name="sql"></a>SQL

* 已添加 `sql db list-usages` 和 `sql db show-usage` 命令
* 已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令

### <a name="vm"></a>VM

* 已对 `az vm list-skus` 添加区域信息


## <a name="november-14-2017"></a>2017 年 11 月 14 日

版本 2.0.21

### <a name="acr"></a>ACR

* 添加了在复制区域中创建 Webhook 的支持


### <a name="acs"></a>ACS

* 已在 AKS 中将所有“代理”一词更改为“节点”
* 弃用了 `acs create` 的 `--orchestrator-release` 选项
* 已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`
* 在 Windows 上修复了 `az aks browse`
* 在 Windows 上修复了 `az aks get-credentials`

### <a name="appservice"></a>应用服务

* 添加了 Web 应用和函数应用的部署源 `config-zip`
* 为 `az webapp log config` 添加了 `--docker-container-logging` 选项
* 从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项
* 完善了 `deployment user set` 的错误消息
* 添加了创建 Linux 函数应用的支持
* 固定 `list-locations`

### <a name="batch"></a>Batch

* 修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug

### <a name="batchai"></a>Batchai

* 在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）
* 为 `cluster create` 参数添加了存储帐户名称和密钥自变量
* 纠正了 `job list-files` 和 `job stream-file` 的文档
* 在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）

### <a name="cloud"></a>云

* 更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云

### <a name="container"></a>容器

* 添加了打开多个端口的支持
* 添加了容器组重启策略
* 添加了将 Azure 文件共享装载为卷的支持
* 更新了帮助器文档

### <a name="data-lake-analytics"></a>Data Lake Analytics

* 更改了 `[job|account] list` 以返回更简洁的信息

### <a name="data-lake-store"></a>Data Lake Store

* 更改了 `account list` 以返回更简洁的信息

### <a name="extension"></a>分机

* 添加了 `extension list-available` 用于列出官方的 Microsoft 扩展
* 为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展

### <a name="iot"></a>IoT

* 添加了对证书颁发机构 (CA) 和证书链的支持

### <a name="monitor"></a>监视

* 添加了 `activity-log alert` 命令

### <a name="network"></a>网络

* 添加了对 CAA DNS 记录的支持
* 修复了无法使用 `traffic-manager profile update` 更新终结点的问题
* 修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题
* 修复了 `dns zone import` 错误导入相对 DNS 名称的问题

### <a name="reservations"></a>预留

* 初始预览版

### <a name="resource"></a>资源

* 添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持

### <a name="sql"></a>SQL

* 为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数

### <a name="storage"></a>存储

* 更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值
* 修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug
* 修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug
* 添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令
* 修复了使用 `storage metrics update` 启用指标时出现的问题
* 修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题
* 修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题

### <a name="vm"></a>VM

* 修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug
* 针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数
* 添加了 `vm secret `[add|remove|list]` 命令
* 已将 `vm format-secret` 重命名为 `vm secret format`
* 为 `vm encryption enable` 添加了 `--encrypt format` 参数

## <a name="october-24-2017"></a>2017 年 10 月 24 日

版本 2.0.20

### <a name="core"></a>核心

* 已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`

### <a name="acr"></a>ACR

* 已更新资源管理以指向 `2017-10-01` API 版本
* 已将“带来你自己的存储”SKU 更改为“经典”
* 已将注册表 SKU 重命名为“基本”、“标准”和“高级”

### <a name="acs"></a>ACS

* [PREVIEW] 添加了 `az aks` 命令
* 已修复 Kubernetes `get-credentials`

### <a name="appservice"></a>应用服务

* 已修复所下载 `webapp` 日志可能无效的问题

### <a name="component"></a>组件

* 为所有安装程序添加了更清晰的弃用消息并添加了确认提示

### <a name="monitor"></a>监视

* 添加了 `action-group` 命令

### <a name="resource"></a>资源

* 修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题
* 修复了 `policy assignment create` 以使用内置策略定义和策略集定义

### <a name="vm"></a>VM

* 为 `vmss create` 添加了 `--accelerated-networking` 参数


## <a name="october-9-2017"></a>2017 年 10 月 9 日

版本 2.0.19

### <a name="core"></a>核心

* 在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL

### <a name="appservice"></a>应用服务

* 添加了新命令 `webapp update` 用于执行常规更新

### <a name="batch"></a>Batch

* 已更新为 Batch SDK 4.0.0
* 更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用
* 添加了对 Batch 扩展命令新 CLI 扩展模型的支持
* 从组件模型中删除了 Batch 支持

### <a name="batchai"></a>Batchai

* Batch AI 模块初始版本

### <a name="keyvault"></a>KeyVault

* 修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。 [(#4448)](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a>网络

* 已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池
* 更新了 `traffic-manager` 以支持最新功能

### <a name="resource"></a>资源

* 在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持
* 为 `account lock` 添加了命令用于处理订阅级锁
* 为 `group lock` 添加了命令用于处理组级锁
* 为 `resource lock` 添加了命令用于处理资源级锁

### <a name="sql"></a>Sql

* 添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持
* 添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库
* 添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作

### <a name="storage"></a>存储

* 添加了对文件共享快照的支持

### <a name="vm"></a>Vm

* 修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃
* [预览] 添加了滚动升级到 `vmss create` 的支持
* 添加了使用 `vm encryption enable` 更新加密设置的支持
* 为 `vm create` 添加了 `--os-disk-size-gb` 参数
* 为 Windows 中的 `vmss create` 添加了 `--license-type` 参数


## <a name="september-22-2017"></a>2017 年 9 月 22 日

版本 2.0.18

### <a name="resource"></a>资源

* 添加了对显示内置策略定义的支持
* 添加了用于创建策略定义的支持模式参数
* 为 `managedapp definition create` 添加了对 UI 定义和模板的支持
* [重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`

### <a name="network"></a>网络

* 为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持
* 为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持
* 添加了 `asg` 应用程序安全组命令
* 为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数
* 为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数
* 为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数
* 添加了 `network [vnet-gateway|vpn-client|show-url]` 命令

### <a name="storage"></a>存储

* 已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题

### <a name="eventgrid"></a>Eventgrid

* 更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”

### <a name="sql"></a>SQL

* 将 `sql server list` 的参数 `--resource-group` 更改为可选。 如果未指定，将返回订阅中的所有 SQL 服务器
* 为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数

### <a name="keyvault"></a>KeyVault

* 添加了对从代理后执行 Keyvault 命令的支持

### <a name="vm"></a>VM

* 为 `[vm|vmss|disk] create` 添加了对可用性区域的支持
* 已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题
* 为 `vm create` 添加了 `--asgs` 参数
* 添加了对使用 `vm run-command` 在 VM 上运行命令的支持
* [预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持
* 添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持

### <a name="acs"></a>ACS

* [预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数

### <a name="appservice"></a>应用服务

* 添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能

### <a name="backup"></a>备份

* 预览版


## <a name="september-11-2017"></a>2017 年 9 月 11 日

版本 2.0.17

### <a name="core"></a>核心

* 启用了命令模块在遥测中设置其自己的相关 ID
* 修复了在遥测设置为诊断模式时的 JSON 转储问题

### <a name="acs"></a>Acs

* 添加了 `acs list-locations` 命令
* 使 `ssh-key-file` 附带预期的默认值

### <a name="appservice"></a>应用服务

* 添加了在未包含活动服务计划的资源组中创建 Web 应用的功能

### <a name="cdn"></a>CDN

* 修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug

### <a name="extension"></a>分机

* 初始版本

### <a name="keyvault"></a>KeyVault

* 为 `keyvault set-policy` 修复了权限区分大小写的问题

### <a name="network"></a>网络

* 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`
* 已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`
* 在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持
* 在 `lb create` 中添加了对 SKU 的支持
* 在 `public-ip create` 中添加了对 SKU 的支持

### <a name="resource"></a>资源

* 允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义
* 允许为 `policy assignment create` 传入参数值
* 允许为所有参数传入 JSON 或文件
* 更新了 API 版本

### <a name="sql"></a>SQL

* 添加了 `sql server vnet-rule` 命令

### <a name="vm"></a>VM

* 已修复：除非提供 `--scope`，否则不分配访问权限
* 已修复：使用与门户相同的扩展命名
* 已从 `[vm|vmss] create` 输出中删除了 `subscription`
* 已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘
* 已修复：`vm format-secret --secrets` 不接受新行分隔的 ID

## <a name="august-31-2017"></a>2017 年 8 月31 日

版本 2.0.16

### <a name="keyvault"></a>KeyVault

* 修复了在尝试使用 `secret download` 自动解析机密编码时的 bug

### <a name="sf"></a>Sf

* 弃用所有支持 Service Fabric CLI (sfctl) 的命令

### <a name="storage"></a>存储

* 修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题
* 在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）

## <a name="august-28-2017"></a>2017 年 8 月 28 日

版本 2.0.15

### <a name="cli"></a>CLI

* 在 `--version` 中添加了法律说明

### <a name="acs"></a>ACS

* 更正了预览区域
* 正确设置了默认 `dns_name_prefix` 的格式
* 优化了 acs 命令输出

### <a name="appservice"></a>应用服务

* [重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致
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

### <a name="batch"></a>Batch

* 已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0
* 添加了新命令用于显示作业的任务计数
* 修复了处理资源文件 SAS URL 时的 bug
* Batch 帐户终结点现在支持可选的“https://” 前缀
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

```text
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

### <a name="batch"></a>Batch

* 已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM
* 已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`
* 添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`

### <a name="cdn"></a>CDN

* 当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息

### <a name="cloud"></a>云

* 已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式
* 不需要库终结点
* 支持只将云注册到 ARM 资源管理器终结点
* 提供 `cloud set` 的选项用于在选择当前云时选择配置文件
* 公开了 `endpoint_vm_image_alias_doc`

### <a name="cosmosdb"></a>CosmosDB

* 修复了允许使用自定义分区键创建集合的问题
* 添加了对集合默认 TTL 的支持

### <a name="data-lake-analytics"></a>Data Lake Analytics

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
* 修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题
* 要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头


## <a name="may-10-2017"></a>2017 年 5 月 10 日

版本 2.0.6

* Documentdb 已重命名为 Cosmosdb
* 添加 rdbms (mysql, postgres)
* 包括 Data Lake Analytics 和 Data Lake Store 模块
* 包括认知服务模块
* 包括 Service Fabric 模块
* 包括交互式模块（重命名 az-shell）
* 添加对 CDN 命令的支持
* 删除容器模块
* 添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))
* 提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))

```text
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

* 将 documentdb 模块重命名为 cosmosdb
* 增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理
* 增加对数据库帐户启用自动故障转移的支持
* 增加对新一致性策略 ConsistentPrefix 的支持

### <a name="data-lake-analytics"></a>Data Lake Analytics

* 修复了在筛选作业结果和状态列表时会引发错误的 bug
* 增加对新目录项类型的支持：包。 访问方法：`az dla catalog package`
* 可从数据库内列出下列目录项（无需架构规范）：

  * 表
  * 表值函数
  * 查看
  * 表统计信息。 这也可以使用架构（但无需指定表名）列出

### <a name="data-lake-store"></a>Data Lake Store

* 更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持
* 提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))
* 访问显示帮助丢失。 正在添加。 ([#2743](https://github.com/Azure/azure-cli/issues/2743))

### <a name="find"></a>查找

* 改进搜索结果，允许搜索索引的版本控制

### <a name="keyvault"></a>KeyVault

* BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项
* BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数
* 将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值
* 修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题
* KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))

### <a name="lab"></a>实验室

* 为实验室中的环境添加 create、show、delete 和 list 命令
* 添加 show 和 list 命令以查看实验室中的 ARM 模板
* 在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM
* 添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架
* 添加命令以管理实验室中的机密

### <a name="monitor"></a>监视

* Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))
* Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))

### <a name="network"></a>网络

* 添加 `network watcher test-connectivity` 命令
* 为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持
* 添加对应用程序网关连接排出的支持
* 添加对应用程序网关 WAF 规则集配置的支持
* 添加对 ExpressRoute 路由筛选器和规则的支持
* 添加对 TrafficManager 地理路由的支持
* 添加对基于 VPN 连接策略的流量选择器的支持
* 添加对 VPN 连接 IPSec 策略的支持
* 修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug
* 添加对主动-主动 VNet 网关的支持
* 从 `network vpn-connection list/show` 命令的输出中删除 null 值
* BC：修复 `vpn-connection create` 输出中的 bug
* 修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug
* 修复 `dns zone import` 中无法正确导入记录的 bug
* 修复 `traffic-manager endpoint update` 不起作用的 bug
* 添加“network watcher”预览命令

### <a name="profile"></a>配置文件

* 支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))
* 支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))

### <a name="redis"></a>Redis

* 添加 update 命令，也增加了对 redis 缓存进行缩放的功能
* 弃用“update-settings”命令

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

* 添加了 az sql server list-usages 和 az sql db list-usages 命令
* SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))

### <a name="storage"></a>存储

* 对于 `storage account create`，将位置默认为资源组位置
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

此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件

```text
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

* 在默认列表中添加了 acr、lab、monitor 和 find 模块
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

* Data Lake Analytics 模块的初始版本
* Data Lake Store 模块的初始版本

### <a name="docuemntdb"></a>DocuemntDB

* DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))

### <a name="vm"></a>VM

* [计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))
* [VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))
* VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))
* 添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))
* 虚拟机规模集：支持使用 * 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))
* 为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))
* 允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))

## <a name="february-27-2017"></a>2017 年 2 月 27 日

版本 2.0.0

此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：
- 容器服务 (ACS)
- 计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）
- 网络
- 存储

这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。

这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。

若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。

```text
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
> 其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。

此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。

可通过以下方式报告夜间预览版的问题：
- 在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题
- 通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队
- 通过命令行使用 `az feedback` 命令提供反馈

