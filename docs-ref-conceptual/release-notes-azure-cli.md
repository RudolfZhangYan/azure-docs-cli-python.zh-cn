---
title: Azure CLI 发行说明
description: 了解 Azure CLI 的最新更新
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 09/21/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: f0ee84c3f70cf168818de447289d6c7ab5a40c9e
ms.sourcegitcommit: c4462456dfb17993f098d47c37bc19f4d78b8179
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/25/2018
ms.locfileid: "47178076"
---
# <a name="azure-cli-release-notes"></a><span data-ttu-id="25fe6-103">Azure CLI 发行说明</span><span class="sxs-lookup"><span data-stu-id="25fe6-103">Azure CLI release notes</span></span>

## <a name="september-21-2018"></a><span data-ttu-id="25fe6-104">2018 年 9 月 21 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-104">September 21, 2018</span></span>

<span data-ttu-id="25fe6-105">版本 20.46</span><span class="sxs-lookup"><span data-stu-id="25fe6-105">Version 20.46</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-106">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-106">ACR</span></span>
* <span data-ttu-id="25fe6-107">添加了 ACR 任务命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-107">Added ACR Task commands</span></span>
* <span data-ttu-id="25fe6-108">添加了快速运行命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-108">Added quick run command</span></span>
* <span data-ttu-id="25fe6-109">已弃用 `build-task` 命令组</span><span class="sxs-lookup"><span data-stu-id="25fe6-109">Deprecated `build-task` command group</span></span>
* <span data-ttu-id="25fe6-110">添加了 `helm` 命令组，以支持使用 ACR 管理 helm 图表</span><span class="sxs-lookup"><span data-stu-id="25fe6-110">Added `helm` command group to support managing helm charts with ACR</span></span>
* <span data-ttu-id="25fe6-111">添加了幂等创建托管注册表的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-111">Added support for idempotent create for managed registry</span></span>
* <span data-ttu-id="25fe6-112">添加了无格式标志用于显示生成日志</span><span class="sxs-lookup"><span data-stu-id="25fe6-112">Added a no-format flag for displaying build logs</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-113">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-113">ACS</span></span>
* <span data-ttu-id="25fe6-114">更改了 `install-connector` 命令以设置 AKS 主 FQDN</span><span class="sxs-lookup"><span data-stu-id="25fe6-114">Changed the `install-connector` command to set the AKS Master FQDN</span></span>
* <span data-ttu-id="25fe6-115">修复了未指定服务主体和 skip-role-assignemnt 时为 vnet-subnet-id 创建角色分配的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-115">Fixed creating role assignment for vnet-subnet-id when not specifying service principal and skip-role-assignemnt</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-116">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-116">AppService</span></span>

* <span data-ttu-id="25fe6-117">添加了 Webjobs（连续和触发）操作管理的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-117">Added support for webjobs (continuous and triggered) operations management</span></span>
* <span data-ttu-id="25fe6-118">az webapp config set 支持 --fts-state 属性。另外，添加了 az functionapp config set 和 show 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-118">az webapp config set supports --fts-state propertyAlso added support fot az functionapp config set & show</span></span>
* <span data-ttu-id="25fe6-119">添加了为 Web 应用自带存储的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-119">Added support for bring your own storage for webapps</span></span>
* <span data-ttu-id="25fe6-120">添加了列出和还原已删除 Web 应用的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-120">Added support for listing and restoring deleted webapps</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-121">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-121">Batch</span></span>
* <span data-ttu-id="25fe6-122">更改了通过 `--json-file` 添加任务的方法，以支持 AddTaskCollectionParameter 语法</span><span class="sxs-lookup"><span data-stu-id="25fe6-122">Changed adding tasks through `--json-file` to support AddTaskCollectionParameter syntax</span></span>
* <span data-ttu-id="25fe6-123">更新了接受 `--json-file` 格式的文档</span><span class="sxs-lookup"><span data-stu-id="25fe6-123">Updated documentation of accepted `--json-file` formats</span></span>
* <span data-ttu-id="25fe6-124">为 `batch pool create` 添加了 `--max-tasks-per-node-option`</span><span class="sxs-lookup"><span data-stu-id="25fe6-124">Added `--max-tasks-per-node-option` to `batch pool create`</span></span>
* <span data-ttu-id="25fe6-125">更改了 `batch account` 的行为，以便在未指定选项时显示当前已登录的帐户</span><span class="sxs-lookup"><span data-stu-id="25fe6-125">Changed behavior of `batch account` to show currently logged in account if no options are specified</span></span>

### <a name="batch-ai"></a><span data-ttu-id="25fe6-126">Batch AI</span><span class="sxs-lookup"><span data-stu-id="25fe6-126">Batch AI</span></span> 
* <span data-ttu-id="25fe6-127">修复了在 `batchai cluster create` 命令中自动创建存储帐户失败的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-127">Fixed auto storage account creation failure in `batchai cluster create` command</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="25fe6-128">认知服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-128">Cognitive Services</span></span>
* <span data-ttu-id="25fe6-129">为 `--sku`、`--kind` 和 `--location` 参数添加了补全选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-129">Added completer for  `--sku`, `--kind`, `--location` arguments</span></span>
* <span data-ttu-id="25fe6-130">添加了命令 `cognitiveservices account list-usage`</span><span class="sxs-lookup"><span data-stu-id="25fe6-130">Added command `cognitiveservices account list-usage`</span></span>
* <span data-ttu-id="25fe6-131">添加了命令 `cognitiveservices account list-kinds`</span><span class="sxs-lookup"><span data-stu-id="25fe6-131">Added command `cognitiveservices account list-kinds`</span></span>
* <span data-ttu-id="25fe6-132">添加了命令 `cognitiveservices account list`</span><span class="sxs-lookup"><span data-stu-id="25fe6-132">Added command `cognitiveservices account list`</span></span>
* <span data-ttu-id="25fe6-133">弃用了 `cognitiveservices list`</span><span class="sxs-lookup"><span data-stu-id="25fe6-133">Deprecated `cognitiveservices list`</span></span>
* <span data-ttu-id="25fe6-134">已将 `--name` 更改为 `cognitiveservices account list-skus` 的可选参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-134">Changed `--name` to be optional for `cognitiveservices account list-skus`</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-135">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-135">Container</span></span>
* <span data-ttu-id="25fe6-136">添加了重启和停止正在运行的容器组的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-136">Added ability to restart and stop a running container group</span></span>
* <span data-ttu-id="25fe6-137">添加了 `--network-profile` 用于传入网络配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-137">Added `--network-profile` for passing in a network profile</span></span>
* <span data-ttu-id="25fe6-138">添加了 `--subnet` 和 `--vnet_name`，以便在 VNET 中创建容器组</span><span class="sxs-lookup"><span data-stu-id="25fe6-138">Added `--subnet`, `--vnet_name`, to allow creating container groups in a VNET</span></span>
* <span data-ttu-id="25fe6-139">更改了表输出，以显示容器组的状态</span><span class="sxs-lookup"><span data-stu-id="25fe6-139">Changed table output to show the status of the container group</span></span>

### <a name="datalake"></a><span data-ttu-id="25fe6-140">Datalake</span><span class="sxs-lookup"><span data-stu-id="25fe6-140">Datalake</span></span>
* <span data-ttu-id="25fe6-141">添加了针对虚拟网络规则的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-141">Added commands for virtual network rules</span></span>

### <a name="interactive-shell"></a><span data-ttu-id="25fe6-142">交互式 Shell</span><span class="sxs-lookup"><span data-stu-id="25fe6-142">Interactive Shell</span></span>
* <span data-ttu-id="25fe6-143">在 Windows 中修复了当命令无法正常运行时发生的错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-143">Fixed error on Windows where commands fail to run properly</span></span>
* <span data-ttu-id="25fe6-144">修复了交互模式下已弃用对象导致的命令加载问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-144">Fixed command loading problem in interactive that was caused by deprecated objects</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-145">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-145">IoT</span></span>
* <span data-ttu-id="25fe6-146">添加了路由 IoT 中心的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-146">Added support for routing IoT Hubs</span></span>

### <a name="key-vault"></a><span data-ttu-id="25fe6-147">Key Vault</span><span class="sxs-lookup"><span data-stu-id="25fe6-147">Key Vault</span></span>
* <span data-ttu-id="25fe6-148">修复了 RSA 密钥的 Key Vault 密钥导入问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-148">Fixed Key Vault key import for RSA keys</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-149">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-149">Network</span></span>
* <span data-ttu-id="25fe6-150">添加了 `network public-ip prefix` 命令以支持公共 IP 前缀功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-150">Add `network public-ip prefix` commands to support public IP prefixes features</span></span>
* <span data-ttu-id="25fe6-151">添加了 `network service-endpoint` 命令以支持服务终结点策略功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-151">Add `network service-endpoint` commands to support service endpoint policy features</span></span>
* <span data-ttu-id="25fe6-152">添加了 `network lb outbound-rule` 命令以支持创建标准负载均衡器出站规则</span><span class="sxs-lookup"><span data-stu-id="25fe6-152">Add `network lb outbound-rule` commands to support creation of Standard Load Balancer outbound rules</span></span>
* <span data-ttu-id="25fe6-153">为 `network lb frontend-ip create/update` 添加了 `--public-ip-prefix`，以支持使用公共 IP 前缀的前端 IP 配置</span><span class="sxs-lookup"><span data-stu-id="25fe6-153">Add `--public-ip-prefix` to `network lb frontend-ip create/update` to support frontend IP configurations using public IP prefixes</span></span>
* <span data-ttu-id="25fe6-154">为 `network lb rule/inbound-nat-rule/inbound-nat-pool create/update` 添加了 `--enable-tcp-reset`</span><span class="sxs-lookup"><span data-stu-id="25fe6-154">Add `--enable-tcp-reset` to `network lb rule/inbound-nat-rule/inbound-nat-pool create/update`</span></span>
* <span data-ttu-id="25fe6-155">为 `network lb rule create/update` 添加了 `--disable-outbound-snat`</span><span class="sxs-lookup"><span data-stu-id="25fe6-155">Add `--disable-outbound-snat` to `network lb rule create/update`</span></span>
* <span data-ttu-id="25fe6-156">允许对经典 NSG 使用 `network watcher flow-log show/configure`</span><span class="sxs-lookup"><span data-stu-id="25fe6-156">Allow `network watcher flow-log show/configure` to be used with classic NSGs</span></span>
* <span data-ttu-id="25fe6-157">添加 `network watcher run-configuration-diagnostic` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-157">Add `network watcher run-configuration-diagnostic` command</span></span>
* <span data-ttu-id="25fe6-158">修复了`network watcher test-connectivity` 命令，并添加了 `--method`、`--valid-status-codes` 和 `--headers` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-158">Fix `network watcher test-connectivity` command and add `--method`, `--valid-status-codes` and `--headers` properties</span></span>
* <span data-ttu-id="25fe6-159">`network express-route create/update`：添加了 `--allow-global-reach` 标志</span><span class="sxs-lookup"><span data-stu-id="25fe6-159">`network express-route create/update`: Add `--allow-global-reach` flag</span></span>
* <span data-ttu-id="25fe6-160">`network vnet subnet create/update`：添加了 `--delegation` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-160">`network vnet subnet create/update`: Add support for `--delegation`</span></span>
* <span data-ttu-id="25fe6-161">添加了 `network vnet subnet list-available-delegations` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-161">Added `network vnet subnet list-available-delegations` command</span></span>
* <span data-ttu-id="25fe6-162">`network traffic-manager profile create/update`：为 Monitor 配置添加了 `--interval`、`--timeout` 和 `--max-failures` 支持。已弃用选项 `--monitor-path`、`--monitor-port` 和 `--monitor-protocol`，改用 `--path`、`--port` 和 `--protocol`</span><span class="sxs-lookup"><span data-stu-id="25fe6-162">`network traffic-manager profile create/update`: Added support for `--interval`, `--timeout` and `--max-failures` for Monitor configuration Deprecated options `--monitor-path`, `--monitor-port` and `--monitor-protocol` in favor of `--path`, `--port`, `--protocol`</span></span>
* <span data-ttu-id="25fe6-163">`network lb frontend-ip create/update`：修复了用于设置专用 IP 分配方法的逻辑。如果提供了专用 IP 地址，则分配是静态的。如果未提供专用 IP 地址，或者为专用 IP 地址提供了空字符串，则分配是动态的。</span><span class="sxs-lookup"><span data-stu-id="25fe6-163">`network lb frontend-ip create/update`: Fixed the logic for setting private IP allocation methodIf a private IP address is provided, the allocation will be staticIf no private IP address is provided, or empty string is provided for private IP address, allocation is dynamic.</span></span>
* <span data-ttu-id="25fe6-164">`dns record-set * create/update`：添加了 `--target-resource` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-164">`dns record-set * create/update`: Add support for `--target-resource`</span></span>
* <span data-ttu-id="25fe6-165">添加了 `network interface-endpoint` 命令用于查询接口终结点对象</span><span class="sxs-lookup"><span data-stu-id="25fe6-165">Add `network interface-endpoint` commands to query interface endpoint objects</span></span>
* <span data-ttu-id="25fe6-166">添加了 `network profile show/list/delete` 用于对网络配置文件进行部分管理</span><span class="sxs-lookup"><span data-stu-id="25fe6-166">Add `network profile show/list/delete` for partial management of network profiles</span></span>
* <span data-ttu-id="25fe6-167">添加了 `network express-route peering connection` 命令用于管理 ExpressRoute 之间的对等连接</span><span class="sxs-lookup"><span data-stu-id="25fe6-167">Add `network express-route peering connection` commands to manage peering connections between ExpressRoutes</span></span>

### <a name="rdbms"></a><span data-ttu-id="25fe6-168">RDBMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-168">RDBMS</span></span>
* <span data-ttu-id="25fe6-169">添加了 MariaDB 服务的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-169">Added support for MariaDB service</span></span>

### <a name="reservation"></a><span data-ttu-id="25fe6-170">保留</span><span class="sxs-lookup"><span data-stu-id="25fe6-170">Reservation</span></span>
* <span data-ttu-id="25fe6-171">在保留的资源枚举类型中添加了 CosmosDb</span><span class="sxs-lookup"><span data-stu-id="25fe6-171">Added CosmosDb in the reserved resource enum type</span></span>
* <span data-ttu-id="25fe6-172">在修补模型中添加了名称属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-172">Added name property in Patch model</span></span>

### <a name="manage-app"></a><span data-ttu-id="25fe6-173">管理应用</span><span class="sxs-lookup"><span data-stu-id="25fe6-173">Manage App</span></span>
* <span data-ttu-id="25fe6-174">修复了 `managedapp create --kind MarketPlace` 中导致创建市场托管应用的实例时发生崩溃的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-174">Fixed bug in `managedapp create --kind MarketPlace` causing instance creation of a Marketplace managed app to crash</span></span>
* <span data-ttu-id="25fe6-175">更改了 `feature` 命令，使其限制为受支持的配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-175">Changed `feature` commands to be restricted to supported profiles</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-176">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-176">Role</span></span>
* <span data-ttu-id="25fe6-177">添加了列出用户组成员身份的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-177">Added support for listing user's group memberships</span></span>

### <a name="signalr"></a><span data-ttu-id="25fe6-178">SignalR</span><span class="sxs-lookup"><span data-stu-id="25fe6-178">SignalR</span></span>
* <span data-ttu-id="25fe6-179">首次发布</span><span class="sxs-lookup"><span data-stu-id="25fe6-179">First release</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-180">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-180">Storage</span></span>
* <span data-ttu-id="25fe6-181">添加了 `--auth-mode login` 参数，以及使用用户的登录凭据进行 Blob 和队列授权</span><span class="sxs-lookup"><span data-stu-id="25fe6-181">Added `--auth-mode login` parameter for use of user's login credentials for blob and queue authorization</span></span>
* <span data-ttu-id="25fe6-182">添加了 `storage container immutability-policy/legal-hold` 用于管理不可变存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-182">Added `storage container immutability-policy/legal-hold` to manage immutable storage</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-183">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-183">VM</span></span>
* <span data-ttu-id="25fe6-184">修复了当公钥文件缺失时，`vm create --generate-ssh-keys` 覆盖私钥文件的问题（#4725、#6780）</span><span class="sxs-lookup"><span data-stu-id="25fe6-184">Fixed issue where `vm create --generate-ssh-keys` overwrites private key file if public key file is missing (#4725, #6780)</span></span>
* <span data-ttu-id="25fe6-185">通过 `az sig` 添加了对共享映像库的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-185">Added support for shared image gallery through `az sig`</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="25fe6-186">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-186">August 28, 2018</span></span>

<span data-ttu-id="25fe6-187">版本 2.0.45</span><span class="sxs-lookup"><span data-stu-id="25fe6-187">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-188">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-188">Core</span></span>

* <span data-ttu-id="25fe6-189">修复了加载空配置文件的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-189">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="25fe6-190">增加了对 Azure Stack 的 `2018-03-01-hybrid` 配置文件的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-190">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-191">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-191">ACR</span></span>

* <span data-ttu-id="25fe6-192">增加了在没有 ARM 请求的情况下针对运行时操作的解决方法</span><span class="sxs-lookup"><span data-stu-id="25fe6-192">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="25fe6-193">从默认情况下 `build` 命令中上传的 tar 更改为 exclude 版本控制文件（例如，.git、.gitignore）</span><span class="sxs-lookup"><span data-stu-id="25fe6-193">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-194">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-194">ACS</span></span>

* <span data-ttu-id="25fe6-195">将 `aks create` 更改为默认的 `Standard_DS2_v2` VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-195">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="25fe6-196">更改了 `aks get-credentials`，现在可以通过调用新 API 来获取群集凭据</span><span class="sxs-lookup"><span data-stu-id="25fe6-196">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-197">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-197">AppService</span></span>

* <span data-ttu-id="25fe6-198">在 functionapp 和 webapp 中增加了对 CORS 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-198">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="25fe6-199">在 create 命令中增加了 ARM 标记支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-199">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="25fe6-200">更改了 `[webapp|functionapp] identity show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-200">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="25fe6-201">备份</span><span class="sxs-lookup"><span data-stu-id="25fe6-201">Backup</span></span>

* <span data-ttu-id="25fe6-202">更改了 `backup vault backup-properties show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-202">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="25fe6-203">Bot 服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-203">Bot Service</span></span>

* <span data-ttu-id="25fe6-204">初始机器人服务 CLI 版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-204">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="25fe6-205">认知服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-205">Cognitive Services</span></span>

* <span data-ttu-id="25fe6-206">添加了新参数 `--api-properties,`，此参数是创建某些服务所需的</span><span class="sxs-lookup"><span data-stu-id="25fe6-206">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-207">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-207">IoT</span></span>

* <span data-ttu-id="25fe6-208">修复了关联已链接中心的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-208">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-209">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-209">Monitor</span></span>

* <span data-ttu-id="25fe6-210">增加了适用于近实时指标警报的 `monitor metrics alert` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-210">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="25fe6-211">弃用了 `monitor alert` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-211">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-212">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-212">Network</span></span>

* <span data-ttu-id="25fe6-213">更改了 `network application-gateway ssl-policy predefined show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-213">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-214">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-214">Resource</span></span>

* <span data-ttu-id="25fe6-215">更改了 `provider operation show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-215">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-216">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-216">Storage</span></span>

* <span data-ttu-id="25fe6-217">更改了 `storage share policy show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-217">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-218">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-218">VM</span></span>

* <span data-ttu-id="25fe6-219">更改了 `vm/vmss identity show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-219">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="25fe6-220">弃用了适用于 `vm create` 的 `--storage-caching`</span><span class="sxs-lookup"><span data-stu-id="25fe6-220">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="25fe6-221">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-221">Auguest 14, 2018</span></span>

<span data-ttu-id="25fe6-222">版本 2.0.44</span><span class="sxs-lookup"><span data-stu-id="25fe6-222">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-223">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-223">Core</span></span>

* <span data-ttu-id="25fe6-224">修复了 `table` 输出中的数字显示问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-224">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="25fe6-225">增加了 YAML 输出格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-225">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="25fe6-226">遥测</span><span class="sxs-lookup"><span data-stu-id="25fe6-226">Telemetry</span></span>

* <span data-ttu-id="25fe6-227">改进了遥测报告</span><span class="sxs-lookup"><span data-stu-id="25fe6-227">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-228">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-228">ACR</span></span>

* <span data-ttu-id="25fe6-229">添加了 `content-trust policy` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-229">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="25fe6-230">修复了 `.dockerignore` 未正确处置的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-230">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-231">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-231">ACS</span></span>

* <span data-ttu-id="25fe6-232">更改了 `az acs/aks install-cli`，可以在 Windows 的 `%USERPROFILE%\.azure-kubectl` 下安装</span><span class="sxs-lookup"><span data-stu-id="25fe6-232">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="25fe6-233">更改了 `az aks install-connector`，可检测群集是否有 RBAC 并可正确配置 ACI 连接器</span><span class="sxs-lookup"><span data-stu-id="25fe6-233">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="25fe6-234">更改了角色分配方式，可以将提供的角色分配到子网</span><span class="sxs-lookup"><span data-stu-id="25fe6-234">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="25fe6-235">增加了新选项，对于已提供角色的子网，可以“跳过角色分配”</span><span class="sxs-lookup"><span data-stu-id="25fe6-235">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="25fe6-236">更改了角色分配，对于已存在分配的子网，可以跳过角色分配</span><span class="sxs-lookup"><span data-stu-id="25fe6-236">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="25fe6-237">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-237">AppService</span></span>

* <span data-ttu-id="25fe6-238">修复了妨碍在外部资源组中使用存储帐户创建 function-app 的 Bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-238">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="25fe6-239">修复了在进行 zip 部署时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-239">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="25fe6-240">BatchAI</span><span class="sxs-lookup"><span data-stu-id="25fe6-240">BatchAI</span></span>

* <span data-ttu-id="25fe6-241">更改了创建自动存储帐户时的记录器输出，现在会指定“资源组”。</span><span class="sxs-lookup"><span data-stu-id="25fe6-241">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="25fe6-242">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-242">Container</span></span>

* <span data-ttu-id="25fe6-243">增加了 `--secure-environment-variables`，用于将安全的环境变量传递到容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-243">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="25fe6-244">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-244">IoT</span></span>

* <span data-ttu-id="25fe6-245">[重大更改] 删除了弃用的命令，这些命令已移至 IoT 扩展</span><span class="sxs-lookup"><span data-stu-id="25fe6-245">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="25fe6-246">更新了元素，现在不采用 `azure-devices.net` 域</span><span class="sxs-lookup"><span data-stu-id="25fe6-246">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="25fe6-247">IoT 中心</span><span class="sxs-lookup"><span data-stu-id="25fe6-247">Iot Central</span></span>

* <span data-ttu-id="25fe6-248">IoT Central 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-248">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-249">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-249">KeyVault</span></span>


* <span data-ttu-id="25fe6-250">增加了用于管理存储帐户和 SAS 定义的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-250">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="25fe6-251">增加了用于网络规则的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-251">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="25fe6-252">增加了针对机密、密钥和证书操作的 `--id` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-252">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="25fe6-253">增加了对 KV 管理多 API 版本的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-253">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="25fe6-254">增加了对 KV 数据平面多 API 版本的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-254">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="25fe6-255">中继</span><span class="sxs-lookup"><span data-stu-id="25fe6-255">Relay</span></span>

* <span data-ttu-id="25fe6-256">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-256">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-257">Sql</span><span class="sxs-lookup"><span data-stu-id="25fe6-257">Sql</span></span>

* <span data-ttu-id="25fe6-258">添加了 `sql failover-group` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-258">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-259">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-259">Storage</span></span>

* <span data-ttu-id="25fe6-260">[重大更改] 更改了 `storage account show-usage`，现在需要 `--location` 参数并且会按区域列出</span><span class="sxs-lookup"><span data-stu-id="25fe6-260">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="25fe6-261">更改了 `--resource-group` 参数，现在此参数为 `storage account` 命令的可选参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-261">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="25fe6-262">对于适用于单个聚合消息的批处理命令中的单个失败，删除了“前提条件失败”警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-262">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="25fe6-263">更改了 `[blob|file] delete-batch` 命令，不再输出 null 数组</span><span class="sxs-lookup"><span data-stu-id="25fe6-263">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="25fe6-264">更改了 `blob [download|upload|delete-batch]` 命令，现在可以读取容器 URL 中的 SAS 令牌</span><span class="sxs-lookup"><span data-stu-id="25fe6-264">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-265">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-265">VM</span></span>

* <span data-ttu-id="25fe6-266">为 `vm list-skus` 添加了常用筛选器，方便用户使用</span><span class="sxs-lookup"><span data-stu-id="25fe6-266">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="25fe6-267">2018 年 7 月 31 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-267">July 31, 2018</span></span>

<span data-ttu-id="25fe6-268">版本 2.0.43</span><span class="sxs-lookup"><span data-stu-id="25fe6-268">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-269">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-269">ACR</span></span>

* <span data-ttu-id="25fe6-270">在 `acr build-task show` 命令中添加了 `--with-secure-properties` 标志</span><span class="sxs-lookup"><span data-stu-id="25fe6-270">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="25fe6-271">添加了 `acr build-task update-build` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-271">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-272">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-272">ACS</span></span>

* <span data-ttu-id="25fe6-273">更改为按 [Ctrl+C] 结束 `az aks browse` 时返回“0 (成功)”</span><span class="sxs-lookup"><span data-stu-id="25fe6-273">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-274">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-274">Batch</span></span>

* <span data-ttu-id="25fe6-275">修复了在 cloudshell 中显示 AAD 令牌时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-275">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-276">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-276">Container</span></span>

* <span data-ttu-id="25fe6-277">删除了在设置订阅时 `--log-analytics-workspace-key` 对名称或 ID 的要求</span><span class="sxs-lookup"><span data-stu-id="25fe6-277">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-278">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-278">Network</span></span>

* <span data-ttu-id="25fe6-279">为 Azure Stack 添加了对 2017-03-09-profile 的 dns 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-279">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="25fe6-280">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-280">Resource</span></span>

* <span data-ttu-id="25fe6-281">将 `--rollback-on-error` 添加到 `group deployment create` 以在出错时执行已知良好的部署</span><span class="sxs-lookup"><span data-stu-id="25fe6-281">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="25fe6-282">修复了将 `--parameters {}` 用于 `group deployment create` 导致错误的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-282">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-283">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-283">Role</span></span>

* <span data-ttu-id="25fe6-284">添加了对堆栈配置文件 2017-03-09-profile 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-284">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="25fe6-285">修复了 `app update` 的通用更新参数无法正常工作的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-285">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="25fe6-286">搜索</span><span class="sxs-lookup"><span data-stu-id="25fe6-286">Search</span></span>

* <span data-ttu-id="25fe6-287">为 Azure 搜索服务添加了命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-287">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="25fe6-288">服务总线</span><span class="sxs-lookup"><span data-stu-id="25fe6-288">Service Bus</span></span>

* <span data-ttu-id="25fe6-289">添加了迁移命令组，以将命名空间从服务总线标准版迁移到高级版</span><span class="sxs-lookup"><span data-stu-id="25fe6-289">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="25fe6-290">为服务总线队列和订阅添加了新的可选属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-290">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="25fe6-291">`queue` 中的 `--enable-batched-operations` 和 `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="25fe6-291">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="25fe6-292">`subscriptions` 中的 `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="25fe6-292">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-293">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-293">Storage</span></span>

* <span data-ttu-id="25fe6-294">添加了对使用单个连接下载大型文件的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-294">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="25fe6-295">转换了在缺少资源时未能失败并显示退出代码 3 的 `show` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-295">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-296">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-296">VM</span></span>

* <span data-ttu-id="25fe6-297">添加了对按订阅列出可用性集的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-297">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="25fe6-298">添加了对 `StandardSSD_LRS` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-298">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="25fe6-299">添加了在创建 VM 规模集时对应用程序安全组的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-299">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="25fe6-300">[重大更改]更改了`[vm|vmss] create`、`[vm|vmss] identity assign` 和 `[vm|vmss] identity remove`，以便以字典格式输出用户指定的标识</span><span class="sxs-lookup"><span data-stu-id="25fe6-300">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="25fe6-301">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-301">July 18, 2018</span></span>

<span data-ttu-id="25fe6-302">版本 2.0.42</span><span class="sxs-lookup"><span data-stu-id="25fe6-302">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-303">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-303">Core</span></span>

* <span data-ttu-id="25fe6-304">在 WSL bash 窗口中添加了对基于浏览器的登录的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-304">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="25fe6-305">为所有通用更新命令添加了 `--force-string` 标志</span><span class="sxs-lookup"><span data-stu-id="25fe6-305">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="25fe6-306">[重大更改]更改了“show”命令以记录错误消息，并在缺少资源时退出代码为 3</span><span class="sxs-lookup"><span data-stu-id="25fe6-306">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-307">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-307">ACR</span></span>

* <span data-ttu-id="25fe6-308">[重大更改]在“acr build”命令中将“--no-push”更新为纯标志</span><span class="sxs-lookup"><span data-stu-id="25fe6-308">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="25fe6-309">在 `acr repository` 组下添加了 `show` 和 `update` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-309">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="25fe6-310">为 `show-manifests` 和 `show-tags`添加了 `--detail` 标记以显示更详细的信息</span><span class="sxs-lookup"><span data-stu-id="25fe6-310">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="25fe6-311">添加了 `--image` 参数以支持通过图像获取构建详细信息或日志</span><span class="sxs-lookup"><span data-stu-id="25fe6-311">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-312">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-312">ACS</span></span>

* <span data-ttu-id="25fe6-313">如果 `--max-pods` 小于 5，则将 `az aks create` 更改为错误输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-313">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-314">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-314">AppService</span></span>

* <span data-ttu-id="25fe6-315">添加了对 PremiumV2 sku 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-315">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-316">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-316">Batch</span></span>

* <span data-ttu-id="25fe6-317">修复了在 Cloud Shell 模式下使用令牌凭据时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-317">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="25fe6-318">将 JSON 输入更改为不区分大小写</span><span class="sxs-lookup"><span data-stu-id="25fe6-318">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="25fe6-319">Batch AI</span><span class="sxs-lookup"><span data-stu-id="25fe6-319">Batch AI</span></span>

* <span data-ttu-id="25fe6-320">修复了 `az batchai job exec` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-320">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-321">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-321">Container</span></span>

* <span data-ttu-id="25fe6-322">删除了非 dockerhub 注册表的用户名和密码要求</span><span class="sxs-lookup"><span data-stu-id="25fe6-322">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="25fe6-323">修复了从 yaml 文件创建容器组时的错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-323">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-324">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-324">Network</span></span>

* <span data-ttu-id="25fe6-325">为 `network nic [create|update|delete]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-325">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="25fe6-326">添加了 `network nic wait`</span><span class="sxs-lookup"><span data-stu-id="25fe6-326">Added `network nic wait`</span></span>
* <span data-ttu-id="25fe6-327">对 `network vnet [subnet|peering] list` 弃用了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-327">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="25fe6-328">添加了 `--include-default` 标志以在 `network nsg rule list` 的输出中包含默认安全规则</span><span class="sxs-lookup"><span data-stu-id="25fe6-328">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="25fe6-329">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-329">Resource</span></span>

* <span data-ttu-id="25fe6-330">为 `group deployment delete` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-330">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="25fe6-331">为 `deployment delete` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-331">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="25fe6-332">添加了 `deployment wait` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-332">Added `deployment wait` command</span></span>
* <span data-ttu-id="25fe6-333">修复了订阅级别 `az deployment` 命令对于配置文件 2017-03-09-profile 错误显示的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-333">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-334">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-334">SQL</span></span>

* <span data-ttu-id="25fe6-335">修复了为 `sql db copy` 和 `sql db replica create` 命令指定弹性池名称时“提供的资源组名称与 URL 中的名称不匹配”错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-335">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="25fe6-336">允许通过执行 `az configure --defaults sql-server=<name>` 配置默认 SQL Server</span><span class="sxs-lookup"><span data-stu-id="25fe6-336">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="25fe6-337">为 `sql server`、`sql server firewall-rule`、`sql list-usages` 和 `sql show-usage` 命令实现了表格式化程序</span><span class="sxs-lookup"><span data-stu-id="25fe6-337">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-338">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-338">Storage</span></span>

* <span data-ttu-id="25fe6-339">将 `pageRanges` 属性添加到了将为页 blob 填充的 `storage blob show` 输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-339">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-340">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-340">VM</span></span>

* <span data-ttu-id="25fe6-341">[重大更改] 将 `vmss create` 更改为使用 `Standard_DS1_v2` 作为默认实例大小</span><span class="sxs-lookup"><span data-stu-id="25fe6-341">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="25fe6-342">向 `vm extension [set|delete]` 和 `vmss extension [set|delete]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-342">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="25fe6-343">添加了 `vm extension wait`</span><span class="sxs-lookup"><span data-stu-id="25fe6-343">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="25fe6-344">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-344">July 3, 2018</span></span>

<span data-ttu-id="25fe6-345">版本 2.0.41</span><span class="sxs-lookup"><span data-stu-id="25fe6-345">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="25fe6-346">AKS</span><span class="sxs-lookup"><span data-stu-id="25fe6-346">AKS</span></span>

* <span data-ttu-id="25fe6-347">更改了监视以使用订阅 ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-347">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="25fe6-348">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-348">July 3, 2018</span></span>

<span data-ttu-id="25fe6-349">版本 2.0.40</span><span class="sxs-lookup"><span data-stu-id="25fe6-349">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-350">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-350">Core</span></span>

* <span data-ttu-id="25fe6-351">添加了用于交互式登录的新授权代码流</span><span class="sxs-lookup"><span data-stu-id="25fe6-351">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-352">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-352">ACR</span></span>

* <span data-ttu-id="25fe6-353">添加了轮询生成状态</span><span class="sxs-lookup"><span data-stu-id="25fe6-353">Added polling build status</span></span>
* <span data-ttu-id="25fe6-354">添加了对不区分大小写的枚举值的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-354">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="25fe6-355">为 `show-manifests` 添加了 `--top` 和 `--orderby` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-355">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-356">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-356">ACS</span></span>

* <span data-ttu-id="25fe6-357">[重大更改] 默认情况下启用 Kubernetes 基于角色的访问控制</span><span class="sxs-lookup"><span data-stu-id="25fe6-357">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="25fe6-358">添加了 `--disable-rbac` 参数并弃用了 `--enable-rbac`，因为它现在是默认值</span><span class="sxs-lookup"><span data-stu-id="25fe6-358">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="25fe6-359">更新了 `aks browse` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="25fe6-359">Updated options for `aks browse` command.</span></span> <span data-ttu-id="25fe6-360">增加了 `--listen-port` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-360">Added `--listen-port` support</span></span>
* <span data-ttu-id="25fe6-361">为 `aks install-connector` 命令更新了默认 helm chart 包。</span><span class="sxs-lookup"><span data-stu-id="25fe6-361">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="25fe6-362">使用 virtual-kubelet-for-aks-latest.tgz</span><span class="sxs-lookup"><span data-stu-id="25fe6-362">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="25fe6-363">添加了 `aks enable-addons` 和 `aks disable-addons` 命令以更新现有群集</span><span class="sxs-lookup"><span data-stu-id="25fe6-363">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-364">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-364">AppService</span></span>

* <span data-ttu-id="25fe6-365">添加了对通过 `webapp identity remove` 禁用标识的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-365">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="25fe6-366">删除了标识功能的 `preview` 标记</span><span class="sxs-lookup"><span data-stu-id="25fe6-366">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="25fe6-367">备份</span><span class="sxs-lookup"><span data-stu-id="25fe6-367">Backup</span></span>

* <span data-ttu-id="25fe6-368">更新了模块定义</span><span class="sxs-lookup"><span data-stu-id="25fe6-368">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="25fe6-369">BatchAI</span><span class="sxs-lookup"><span data-stu-id="25fe6-369">BatchAI</span></span>

* <span data-ttu-id="25fe6-370">修复了 `batchai cluster node list` 和 `batchai job node list` 命令的表输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-370">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="25fe6-371">云</span><span class="sxs-lookup"><span data-stu-id="25fe6-371">Cloud</span></span>

* <span data-ttu-id="25fe6-372">为云配置添加了 `acr login` 服务器后缀</span><span class="sxs-lookup"><span data-stu-id="25fe6-372">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-373">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-373">Container</span></span>

* <span data-ttu-id="25fe6-374">更改了 `container create` 以将其默认为长时间运行的操作</span><span class="sxs-lookup"><span data-stu-id="25fe6-374">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="25fe6-375">添加了 Log Analytics 参数 `--log-analytics-workspace` 和 `--log-analytics-workspace-key`</span><span class="sxs-lookup"><span data-stu-id="25fe6-375">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="25fe6-376">添加了 `--protocol` 参数来指定要使用哪个网络协议</span><span class="sxs-lookup"><span data-stu-id="25fe6-376">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-377">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-377">Extension</span></span>

* <span data-ttu-id="25fe6-378">更改了 `extension list-available` 以仅显示与 CLI 版本兼容的扩展</span><span class="sxs-lookup"><span data-stu-id="25fe6-378">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-379">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-379">Network</span></span>

* <span data-ttu-id="25fe6-380">修复了记录类型区分大小写的问题 ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span><span class="sxs-lookup"><span data-stu-id="25fe6-380">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="25fe6-381">Rdbms</span><span class="sxs-lookup"><span data-stu-id="25fe6-381">Rdbms</span></span>

* <span data-ttu-id="25fe6-382">添加了 `[postgres|myql] server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-382">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-383">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-383">Resource</span></span>

* <span data-ttu-id="25fe6-384">添加了新操作组 `deployment`</span><span class="sxs-lookup"><span data-stu-id="25fe6-384">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-385">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-385">VM</span></span>

* <span data-ttu-id="25fe6-386">添加了对删除系统分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-386">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="25fe6-387">2018 年 6 月 25日</span><span class="sxs-lookup"><span data-stu-id="25fe6-387">June 25, 2018</span></span>

<span data-ttu-id="25fe6-388">版本 2.0.39</span><span class="sxs-lookup"><span data-stu-id="25fe6-388">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="25fe6-389">CLI</span><span class="sxs-lookup"><span data-stu-id="25fe6-389">CLI</span></span>

* <span data-ttu-id="25fe6-390">更新了 MSI 安装程序中的文件修整以修复扩展安装问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-390">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="25fe6-391">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-391">June 19, 2018</span></span>

<span data-ttu-id="25fe6-392">版本 2.0.38</span><span class="sxs-lookup"><span data-stu-id="25fe6-392">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-393">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-393">Core</span></span>

* <span data-ttu-id="25fe6-394">为大多数命令增加了对 `--subscription` 的全局支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-394">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-395">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-395">ACR</span></span>

* <span data-ttu-id="25fe6-396">增加了 `azure-storage-blob` 作为依赖项</span><span class="sxs-lookup"><span data-stu-id="25fe6-396">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="25fe6-397">更改了 `acr build-task create` 的默认 CPU 配置，允许使用 2 核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-397">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-398">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-398">ACS</span></span>

* <span data-ttu-id="25fe6-399">更新了 `aks use-dev-spaces` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="25fe6-399">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="25fe6-400">增加了 `--update` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-400">Added `--update` support</span></span>
* <span data-ttu-id="25fe6-401">更改了 `aks get-credentials --admin`，不替换 `$HOME/.kube/config` 中的用户上下文</span><span class="sxs-lookup"><span data-stu-id="25fe6-401">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="25fe6-402">公开了托管群集上的只读 `nodeResourceGroup` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-402">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="25fe6-403">修复了 `acs browse` 命令错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-403">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="25fe6-404">将 `--connector-name` 设置为 `aks install-connector`、`aks upgrade-connector` 和 `aks remove-connector` 的可选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-404">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="25fe6-405">为 `aks install-connector` 增加了新的 Azure 容器实例区域</span><span class="sxs-lookup"><span data-stu-id="25fe6-405">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="25fe6-406">为 helm 版本名称增加了规范化位置，并为 `aks install-connector` 增加了节点名称</span><span class="sxs-lookup"><span data-stu-id="25fe6-406">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-407">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-407">AppService</span></span>

* <span data-ttu-id="25fe6-408">增加了对更新版 urllib 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-408">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="25fe6-409">为 `functionapp create` 增加了支持，可以使用外部资源组的应用服务计划</span><span class="sxs-lookup"><span data-stu-id="25fe6-409">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-410">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-410">Batch</span></span>

* <span data-ttu-id="25fe6-411">删除了 `azure-batch-extensions` 依赖项</span><span class="sxs-lookup"><span data-stu-id="25fe6-411">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="25fe6-412">Batch AI</span><span class="sxs-lookup"><span data-stu-id="25fe6-412">Batch AI</span></span>

* <span data-ttu-id="25fe6-413">添加了对工作区的支持。</span><span class="sxs-lookup"><span data-stu-id="25fe6-413">Added support for workspaces.</span></span> <span data-ttu-id="25fe6-414">可以通过工作区将群集、文件服务器和试验按组分组，去除了对可以创建的资源数的限制</span><span class="sxs-lookup"><span data-stu-id="25fe6-414">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="25fe6-415">增加了对试验的支持。</span><span class="sxs-lookup"><span data-stu-id="25fe6-415">Added support for experiments.</span></span> <span data-ttu-id="25fe6-416">可以通过试验将作业按集合分组，去除了对已创建作业的数目限制</span><span class="sxs-lookup"><span data-stu-id="25fe6-416">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="25fe6-417">增加了为 Docker 容器中运行的作业配置 `/dev/shm` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-417">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="25fe6-418">增加了 `batchai cluster node exec` 和 `batchai job node exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="25fe6-418">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="25fe6-419">这些命令允许在节点上直接执行任何命令，提供用于端口转发的功能。</span><span class="sxs-lookup"><span data-stu-id="25fe6-419">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="25fe6-420">为 `batchai` 命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-420">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="25fe6-421">[重大更改] 所有群集和文件服务器必须在工作区创建</span><span class="sxs-lookup"><span data-stu-id="25fe6-421">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="25fe6-422">[重大更改] 作业必须在试验中创建</span><span class="sxs-lookup"><span data-stu-id="25fe6-422">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="25fe6-423">[重大更改] 从 `cluster create` 和 `job create` 命令中删除了 `--nfs-resource-group`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-423">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="25fe6-424">若要装载属于其他工作区/资源组的 NFS，请通过 `--nfs` 选项提供文件服务器的 ARM ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-424">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="25fe6-425">[重大更改] 从 `job create` 命令中删除了 `--cluster-resource-group`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-425">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="25fe6-426">若要在属于其他工作区/资源组的群集上提交作业，请通过 `--cluster` 选项提供群集的 ARM ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-426">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="25fe6-427">[重大更改] 从作业、群集和文件服务器中删除了 `location` 特性。</span><span class="sxs-lookup"><span data-stu-id="25fe6-427">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="25fe6-428">位置现在是工作区的特性。</span><span class="sxs-lookup"><span data-stu-id="25fe6-428">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="25fe6-429">[重大更改] 从 `job create`、`cluster create` 和 `file-server create` 命令中删除了 `--location`</span><span class="sxs-lookup"><span data-stu-id="25fe6-429">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="25fe6-430">[重大更改] 更改了短选项的名称，使接口更一致：</span><span class="sxs-lookup"><span data-stu-id="25fe6-430">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="25fe6-431">[`--config`, `-c`] 已重命名为 [`--config-file`, `-f`]</span><span class="sxs-lookup"><span data-stu-id="25fe6-431">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="25fe6-432">[`--cluster`, `-r`] 已重命名为 [`--cluster`, `-c`]</span><span class="sxs-lookup"><span data-stu-id="25fe6-432">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="25fe6-433">[`--cluster`, `-n`] 已重命名为 [`--cluster`, `-c`]</span><span class="sxs-lookup"><span data-stu-id="25fe6-433">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="25fe6-434">[`--job`, `-n`] 已重命名为 [`--job`, `-j`]</span><span class="sxs-lookup"><span data-stu-id="25fe6-434">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="25fe6-435">地图</span><span class="sxs-lookup"><span data-stu-id="25fe6-435">Maps</span></span>

* <span data-ttu-id="25fe6-436">[重大更改] 更改了 `maps account create`，要求通过交互式提示或 `--accept-tos` 标志接受《服务条款》</span><span class="sxs-lookup"><span data-stu-id="25fe6-436">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-437">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-437">Network</span></span>

* <span data-ttu-id="25fe6-438">为 `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571) 增加了对 `https` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-438">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="25fe6-439">修复了 `--endpoint-status` 区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="25fe6-439">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="25fe6-440">#6502</span><span class="sxs-lookup"><span data-stu-id="25fe6-440">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="25fe6-441">预留</span><span class="sxs-lookup"><span data-stu-id="25fe6-441">Reservations</span></span>

* <span data-ttu-id="25fe6-442">[重大更改] 为 `reservations catalog show` 增加了必需参数 `ReservedResourceType`</span><span class="sxs-lookup"><span data-stu-id="25fe6-442">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="25fe6-443">为 `reservations catalog show` 增加了参数 `Location`</span><span class="sxs-lookup"><span data-stu-id="25fe6-443">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="25fe6-444">[重大更改] 从 `ReservationProperties` 中删除了 `kind`</span><span class="sxs-lookup"><span data-stu-id="25fe6-444">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="25fe6-445">[重大更改] 已在 `Catalog` 中将 `capabilities` 重命名为 `sku_properties`</span><span class="sxs-lookup"><span data-stu-id="25fe6-445">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="25fe6-446">[重大更改] 从 `Catalog` 中删除了 `size` 和 `tier` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-446">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="25fe6-447">为 `reservations reservation update` 增加了参数 `InstanceFlexibility`</span><span class="sxs-lookup"><span data-stu-id="25fe6-447">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-448">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-448">Role</span></span>

* <span data-ttu-id="25fe6-449">改进了错误处理</span><span class="sxs-lookup"><span data-stu-id="25fe6-449">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-450">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-450">SQL</span></span>

* <span data-ttu-id="25fe6-451">修复了针对不可供订阅使用的位置运行 `az sql db list-editions` 时出现的令人困惑的错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-451">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-452">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-452">Storage</span></span>

* <span data-ttu-id="25fe6-453">更改了 `storage blob download` 的表输出，使之更为可读</span><span class="sxs-lookup"><span data-stu-id="25fe6-453">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-454">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-454">VM</span></span>

* <span data-ttu-id="25fe6-455">针对 `vm create` 中的加速网络支持，改进了 refine vm size check</span><span class="sxs-lookup"><span data-stu-id="25fe6-455">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="25fe6-456">增加了针对 `vmss create` 的警告：默认的 VM 大小将从 `Standard_D1_v2` 切换为 `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="25fe6-456">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="25fe6-457">为 `[vm|vmss] extension set` 增加了 `--force-update`，即使在配置未变的情况下也可以更新扩展</span><span class="sxs-lookup"><span data-stu-id="25fe6-457">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="25fe6-458">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-458">June 13, 2018</span></span>

<span data-ttu-id="25fe6-459">版本 2.0.37</span><span class="sxs-lookup"><span data-stu-id="25fe6-459">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-460">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-460">Core</span></span>

* <span data-ttu-id="25fe6-461">改进了交互式遥测</span><span class="sxs-lookup"><span data-stu-id="25fe6-461">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="25fe6-462">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-462">June 13, 2018</span></span>

<span data-ttu-id="25fe6-463">版本 2.0.36</span><span class="sxs-lookup"><span data-stu-id="25fe6-463">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="25fe6-464">AKS</span><span class="sxs-lookup"><span data-stu-id="25fe6-464">AKS</span></span>

* <span data-ttu-id="25fe6-465">为 `aks create` 添加了高级网络选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-465">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="25fe6-466">为 `aks create` 添加了参数以启用监视和 HTTP 路由</span><span class="sxs-lookup"><span data-stu-id="25fe6-466">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="25fe6-467">为 `aks create` 添加了 `--no-ssh-key` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-467">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="25fe6-468">为 `aks create` 添加了 `--enable-rbac` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-468">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="25fe6-469">[PREVIEW] 为 `aks create` 添加了对 Azure Active Directory 身份验证的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-469">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-470">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-470">AppService</span></span>

* <span data-ttu-id="25fe6-471">修复了不兼容 urllib 版本的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-471">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="25fe6-472">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-472">June 5, 2018</span></span>

<span data-ttu-id="25fe6-473">版本 2.0.35</span><span class="sxs-lookup"><span data-stu-id="25fe6-473">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-474">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-474">Interactive</span></span>

* <span data-ttu-id="25fe6-475">添加了对交互模式的依赖项的限制</span><span class="sxs-lookup"><span data-stu-id="25fe6-475">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="25fe6-476">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-476">June 5, 2018</span></span>

<span data-ttu-id="25fe6-477">版本 2.0.34</span><span class="sxs-lookup"><span data-stu-id="25fe6-477">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-478">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-478">Core</span></span>

* <span data-ttu-id="25fe6-479">增加了对跨租户资源引用的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-479">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="25fe6-480">增强了遥测数据上传可靠性</span><span class="sxs-lookup"><span data-stu-id="25fe6-480">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-481">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-481">ACR</span></span>

* <span data-ttu-id="25fe6-482">增加了对 VSTS 充当远程源位置的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-482">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="25fe6-483">添加了 `acr import` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-483">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="25fe6-484">AKS</span><span class="sxs-lookup"><span data-stu-id="25fe6-484">AKS</span></span>

* <span data-ttu-id="25fe6-485">更改了 `aks get-credentials`，可以使用更安全的文件系统权限来创建 kube 配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-485">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-486">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-486">Batch</span></span>

* <span data-ttu-id="25fe6-487">修复了池列表表格式设置中的 Bug [[问题 #4378](https://github.com/Azure/azure-cli/issues/4378)]</span><span class="sxs-lookup"><span data-stu-id="25fe6-487">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-488">IOT</span><span class="sxs-lookup"><span data-stu-id="25fe6-488">IOT</span></span>

* <span data-ttu-id="25fe6-489">增加了对创建基本层 IoT 中心的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-489">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-490">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-490">Network</span></span>

* <span data-ttu-id="25fe6-491">改进了 `network vnet peering`</span><span class="sxs-lookup"><span data-stu-id="25fe6-491">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="25fe6-492">策略见解</span><span class="sxs-lookup"><span data-stu-id="25fe6-492">Policy Insights</span></span>

* <span data-ttu-id="25fe6-493">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-493">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="25fe6-494">ARM</span><span class="sxs-lookup"><span data-stu-id="25fe6-494">ARM</span></span>

* <span data-ttu-id="25fe6-495">增加了 `account management-group` 命令。</span><span class="sxs-lookup"><span data-stu-id="25fe6-495">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-496">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-496">SQL</span></span>

* <span data-ttu-id="25fe6-497">增加了新的托管实例命令：</span><span class="sxs-lookup"><span data-stu-id="25fe6-497">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="25fe6-498">增加了新的托管数据库命令：</span><span class="sxs-lookup"><span data-stu-id="25fe6-498">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="25fe6-499">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-499">Storage</span></span>

* <span data-ttu-id="25fe6-500">增加了可以从文件扩展名推断且适用于 json 和 javascript 的额外 mimetype</span><span class="sxs-lookup"><span data-stu-id="25fe6-500">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-501">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-501">VM</span></span>

* <span data-ttu-id="25fe6-502">更改了 `vm list-skus`，可以使用固定列并可添加表明要删除 `Tier` 和 `Size` 的警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-502">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="25fe6-503">为 `vm create` 添加了 `--accelerated-networking` 选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-503">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="25fe6-504">为 `identity create` 添加了 `--tags`</span><span class="sxs-lookup"><span data-stu-id="25fe6-504">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="25fe6-505">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-505">May 22, 2018</span></span>

<span data-ttu-id="25fe6-506">版本 2.0.33</span><span class="sxs-lookup"><span data-stu-id="25fe6-506">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-507">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-507">Core</span></span>

* <span data-ttu-id="25fe6-508">增加了对在文件名中扩展 `@` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-508">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-509">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-509">ACS</span></span>

* <span data-ttu-id="25fe6-510">增加了新的 Dev-Spaces 命令：`aks use-dev-spaces` 和 `aks remove-dev-spaces`</span><span class="sxs-lookup"><span data-stu-id="25fe6-510">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="25fe6-511">修复了帮助消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-511">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-512">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-512">AppService</span></span>

* <span data-ttu-id="25fe6-513">改进了泛型更新命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-513">Improved generic update commands</span></span>
* <span data-ttu-id="25fe6-514">增加了对 `webapp deployment source config-zip` 的异步支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-514">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-515">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-515">Container</span></span>

* <span data-ttu-id="25fe6-516">增加了对以 yaml 格式导出容器组的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-516">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="25fe6-517">增加了对使用 yaml 文件创建/更新容器组的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-517">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-518">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-518">Extension</span></span>

* <span data-ttu-id="25fe6-519">改进了扩展的删除方式</span><span class="sxs-lookup"><span data-stu-id="25fe6-519">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-520">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-520">Interactive</span></span>

* <span data-ttu-id="25fe6-521">更改了日志记录，在完成时将分析器静音</span><span class="sxs-lookup"><span data-stu-id="25fe6-521">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="25fe6-522">改进了错误的帮助缓存的处理</span><span class="sxs-lookup"><span data-stu-id="25fe6-522">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-523">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-523">KeyVault</span></span>

* <span data-ttu-id="25fe6-524">修复了 keyvault 命令，使之可以在 Cloud Shell 或 VM 中与标识一起使用</span><span class="sxs-lookup"><span data-stu-id="25fe6-524">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-525">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-525">Network</span></span>

* <span data-ttu-id="25fe6-526">修复了 `network watcher show-topology` 无法与 vnet 和/或子网名称一起使用的问题 [#6326](https://github.com/Azure/azure-cli/issues/6326)</span><span class="sxs-lookup"><span data-stu-id="25fe6-526">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="25fe6-527">修复了某些 `network watcher` 命令宣称未为区域启用网络观察程序而实际上却已经启用的问题 [#6264](https://github.com/Azure/azure-cli/issues/6264)</span><span class="sxs-lookup"><span data-stu-id="25fe6-527">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-528">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-528">SQL</span></span>

* <span data-ttu-id="25fe6-529">[重大更改] 更改了从 `db` 和 `dw` 命令返回的响应对象：</span><span class="sxs-lookup"><span data-stu-id="25fe6-529">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="25fe6-530">已将 `serviceLevelObjective` 属性重命名为 `currentServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="25fe6-530">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="25fe6-531">删除了 `currentServiceObjectiveId` 和 `requestedServiceObjectiveId` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-531">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="25fe6-532">已将 `maxSizeBytes` 属性更改为整数值而不是字符串</span><span class="sxs-lookup"><span data-stu-id="25fe6-532">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="25fe6-533">[重大更改] 已将下面的 `db` 和 `dw` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="25fe6-533">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="25fe6-534">`requestedServiceObjectiveName`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-534">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="25fe6-535">若要更新，请使用 `--service-objective` 参数或设置 `sku.name` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-535">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="25fe6-536">`edition`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-536">`edition`.</span></span> <span data-ttu-id="25fe6-537">若要更新，请使用 `--edition` 参数或设置 `sku.tier` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-537">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="25fe6-538">`elasticPoolName`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-538">`elasticPoolName`.</span></span> <span data-ttu-id="25fe6-539">若要更新，请使用 `--elastic-pool` 参数或设置 `elasticPoolId` 属性</span><span class="sxs-lookup"><span data-stu-id="25fe6-539">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="25fe6-540">[重大更改] 已将下面的 `elastic-pool` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="25fe6-540">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="25fe6-541">`edition`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-541">`edition`.</span></span> <span data-ttu-id="25fe6-542">若要更新，请使用 `--edition` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-542">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="25fe6-543">`dtu`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-543">`dtu`.</span></span> <span data-ttu-id="25fe6-544">若要更新，请使用 `--capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-544">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="25fe6-545">`databaseDtuMin`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-545">`databaseDtuMin`.</span></span> <span data-ttu-id="25fe6-546">若要更新，请使用 `--db-min-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-546">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="25fe6-547">`databaseDtuMax`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-547">`databaseDtuMax`.</span></span> <span data-ttu-id="25fe6-548">若要更新，请使用 `--db-max-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-548">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="25fe6-549">为 `db`、`dw` 和 `elastic-pool` 命令增加了 `--family` 和 `--capacity` 参数。</span><span class="sxs-lookup"><span data-stu-id="25fe6-549">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="25fe6-550">为 `db`、`dw` 和 `elastic-pool` 命令增加了表格式化程序。</span><span class="sxs-lookup"><span data-stu-id="25fe6-550">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-551">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-551">Storage</span></span>

* <span data-ttu-id="25fe6-552">增加了 `--account-name` 参数的补全选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-552">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="25fe6-553">修复了 `storage entity query` 的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-553">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-554">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-554">VM</span></span>

* <span data-ttu-id="25fe6-555">[重大更改] 从 `vm create` 中删除了 `--write-accelerator`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-555">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="25fe6-556">可以通过 `vm update` 或 `vm disk attach` 访问同一支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-556">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="25fe6-557">修复了 `[vm|vmss] extension` 中的扩展映像匹配问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-557">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="25fe6-558">为 `vm create` 添加了 `--boot-diagnostics-storage`，可以捕获启动日志</span><span class="sxs-lookup"><span data-stu-id="25fe6-558">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="25fe6-559">为 `[vm|vmss] update` 添加了 `--license-type`</span><span class="sxs-lookup"><span data-stu-id="25fe6-559">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="25fe6-560">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-560">May 7, 2018</span></span>

<span data-ttu-id="25fe6-561">版本 2.0.32</span><span class="sxs-lookup"><span data-stu-id="25fe6-561">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-562">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-562">Core</span></span>

* <span data-ttu-id="25fe6-563">修复了使用证书从服务主体帐户检索机密时引发未处理异常的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-563">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="25fe6-564">增加了对位置参数的有限支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-564">Added limited support for positional arguments</span></span>
* <span data-ttu-id="25fe6-565">修复了 `--query` 无法与 `--ids` 一起使用的问题。</span><span class="sxs-lookup"><span data-stu-id="25fe6-565">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="25fe6-566">#5591</span><span class="sxs-lookup"><span data-stu-id="25fe6-566">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="25fe6-567">改进了使用 `--ids` 时通过命令执行的管道方案。</span><span class="sxs-lookup"><span data-stu-id="25fe6-567">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="25fe6-568">支持在指定查询的情况下使用 `-o tsv`，或者在不指定查询的情况下使用 `-o json`</span><span class="sxs-lookup"><span data-stu-id="25fe6-568">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="25fe6-569">增加了在用户的命令中存在拼写错误的情况下，针对错误提供命令建议的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-569">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="25fe6-570">改进了用户键入 `az ''` 时出现的错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-570">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="25fe6-571">增加了针对命令模块和扩展自定义资源类型的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-571">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-572">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-572">ACR</span></span>

* <span data-ttu-id="25fe6-573">增加了 ACR 生成命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-573">Added ACR Build commands</span></span>
* <span data-ttu-id="25fe6-574">改进了“找不到资源”类型的错误消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-574">Improved resource not found error messages</span></span>
* <span data-ttu-id="25fe6-575">改进了资源创建性能和错误处理</span><span class="sxs-lookup"><span data-stu-id="25fe6-575">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="25fe6-576">改进了 acr 登录非标准控制台和 WSL</span><span class="sxs-lookup"><span data-stu-id="25fe6-576">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="25fe6-577">改进了存储库命令错误消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-577">Improved repository commands error messages</span></span>
* <span data-ttu-id="25fe6-578">更新了表列和排序</span><span class="sxs-lookup"><span data-stu-id="25fe6-578">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-579">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-579">ACS</span></span>

* <span data-ttu-id="25fe6-580">增加了“`az aks` 是预览版服务”警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-580">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="25fe6-581">修复了未指定 `--aci-resource-group` 时 `aks install-connector` 中的权限问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-581">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="25fe6-582">AMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-582">AMS</span></span>

* <span data-ttu-id="25fe6-583">初始版本 - 管理 Azure 媒体服务资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-583">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-584">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-584">Appservice</span></span>

* <span data-ttu-id="25fe6-585">修复了提供 `--slot` 时 `webapp delete` 中的 Bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-585">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="25fe6-586">从 `webapp auth update` 删除了 `--runtime-version`</span><span class="sxs-lookup"><span data-stu-id="25fe6-586">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="25fe6-587">增加了对 min\_tls\_version & https2.0 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-587">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="25fe6-588">增加了对多容器的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-588">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="25fe6-589">Batch AI</span><span class="sxs-lookup"><span data-stu-id="25fe6-589">Batch AI</span></span>

* <span data-ttu-id="25fe6-590">更改了 `batchai create cluster`，以便遵循在群集的配置文件中配置的 VM 优先级</span><span class="sxs-lookup"><span data-stu-id="25fe6-590">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="25fe6-591">认知服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-591">Cognitive Services</span></span>

* <span data-ttu-id="25fe6-592">修复了在 `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603) 的示例中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-592">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="25fe6-593">消耗</span><span class="sxs-lookup"><span data-stu-id="25fe6-593">Consumption</span></span>

* <span data-ttu-id="25fe6-594">增加了预算 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-594">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-595">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-595">Container</span></span>

* <span data-ttu-id="25fe6-596">删除了在映像名称中包括注册表服务器时对 `container create` 命令的 `--registry-server` 参数的要求</span><span class="sxs-lookup"><span data-stu-id="25fe6-596">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="25fe6-597">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="25fe6-597">Cosmos DB</span></span>

* <span data-ttu-id="25fe6-598">引入针对 Azure CLI 的 VNET 支持 - Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="25fe6-598">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="25fe6-599">DMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-599">DMS</span></span>

* <span data-ttu-id="25fe6-600">初始版本 - 为 Azure SQL 迁移方案增加了对 SQL 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-600">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-601">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-601">Extension</span></span>

* <span data-ttu-id="25fe6-602">修复了停止显示扩展元数据的 Bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-602">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-603">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-603">Interactive</span></span>

* <span data-ttu-id="25fe6-604">允许交互式补全选项使用位置参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-604">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="25fe6-605">增强用户键入 '\' 时的输出的用户友好性</span><span class="sxs-lookup"><span data-stu-id="25fe6-605">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="25fe6-606">修复了在没有帮助的情况下参数的补全问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-606">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="25fe6-607">修复了命令组的说明问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-607">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="25fe6-608">实验室</span><span class="sxs-lookup"><span data-stu-id="25fe6-608">Lab</span></span>

* <span data-ttu-id="25fe6-609">修复了 Knack 转换的回归问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-609">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-610">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-610">Network</span></span>

* <span data-ttu-id="25fe6-611">[重大更改] 删除了以下项的 `--ids` 参数：</span><span class="sxs-lookup"><span data-stu-id="25fe6-611">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="25fe6-612">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-612">Profile</span></span>

* <span data-ttu-id="25fe6-613">修复了 `disk create` 源检测问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-613">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="25fe6-614">[重大更改] 删除了不再使用的 `--msi-port` 和 `--identity-port`</span><span class="sxs-lookup"><span data-stu-id="25fe6-614">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="25fe6-615">修复了 `account get-access-token` 短摘要中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-615">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="25fe6-616">Redis</span><span class="sxs-lookup"><span data-stu-id="25fe6-616">Redis</span></span>

* <span data-ttu-id="25fe6-617">弃用 `redis patch-schedule patch-schedule show` 而改用 `redis patch-schedule show`</span><span class="sxs-lookup"><span data-stu-id="25fe6-617">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="25fe6-618">弃用 `redis list-all`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-618">Deprecated `redis list-all`.</span></span> <span data-ttu-id="25fe6-619">此功能已加入 `redis list` 中</span><span class="sxs-lookup"><span data-stu-id="25fe6-619">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="25fe6-620">弃用 `redis import-method` 而改用 `redis import`</span><span class="sxs-lookup"><span data-stu-id="25fe6-620">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="25fe6-621">为各种命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-621">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-622">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-622">Role</span></span>

* <span data-ttu-id="25fe6-623">[重大更改] 删除了已弃用的 `ad sp reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="25fe6-623">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-624">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-624">Storage</span></span>

* <span data-ttu-id="25fe6-625">在源 SAS 和帐户密钥未指定的情况下，允许将目标 SAS 令牌应用到源，以便进行 Blob 复制</span><span class="sxs-lookup"><span data-stu-id="25fe6-625">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="25fe6-626">公开了用于 Blob 上传和下载的 --socket-timeout 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-626">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="25fe6-627">将以路径分隔符开头的 Blob 名称视为相对路径</span><span class="sxs-lookup"><span data-stu-id="25fe6-627">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="25fe6-628">允许 `storage blob copy --source-sas` 以查询字符“?”开头</span><span class="sxs-lookup"><span data-stu-id="25fe6-628">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="25fe6-629">修复了 `storage entity query --marker` 问题，接受“键=值”列表</span><span class="sxs-lookup"><span data-stu-id="25fe6-629">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-630">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-630">VM</span></span>

* <span data-ttu-id="25fe6-631">修复了非托管 Blob URI 上的检测逻辑无效的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-631">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="25fe6-632">增加了在没有用户提供的服务主体的情况下进行磁盘加密的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-632">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="25fe6-633">[重大更改] 请勿使用 VM“ManagedIdentityExtension”来寻求 MSI 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-633">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="25fe6-634">增加了对 `vmss` 使用逐出策略的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-634">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="25fe6-635">[重大更改] 从以下项删除了 `--ids`：</span><span class="sxs-lookup"><span data-stu-id="25fe6-635">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="25fe6-636">增加了写入加速器支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-636">Added write accelerator support</span></span>
* <span data-ttu-id="25fe6-637">添加了 `vmss perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="25fe6-637">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="25fe6-638">修复了 `vm diagnostics set` 问题，可以可靠地检测 VM 的 OS 类型</span><span class="sxs-lookup"><span data-stu-id="25fe6-638">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="25fe6-639">更改了 `vm resize`，系统会检查请求的大小是否不同于当前设置的大小，只在二者有变化时进行更新</span><span class="sxs-lookup"><span data-stu-id="25fe6-639">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="25fe6-640">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-640">April 10, 2018</span></span>

<span data-ttu-id="25fe6-641">版本 2.0.31</span><span class="sxs-lookup"><span data-stu-id="25fe6-641">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-642">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-642">ACR</span></span>

* <span data-ttu-id="25fe6-643">改进了 wincred 回退错误处理</span><span class="sxs-lookup"><span data-stu-id="25fe6-643">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-644">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-644">ACS</span></span>

* <span data-ttu-id="25fe6-645">更改了 aks 创建的 SPN，使其有效期达到 5 年</span><span class="sxs-lookup"><span data-stu-id="25fe6-645">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-646">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-646">Appservice</span></span>

* [重大更改]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="25fe6-648">修复了 Web 应用计划不存在导致的未捕获异常</span><span class="sxs-lookup"><span data-stu-id="25fe6-648">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="25fe6-649">BatchAI</span><span class="sxs-lookup"><span data-stu-id="25fe6-649">BatchAI</span></span>

* <span data-ttu-id="25fe6-650">添加了对 2018-03-01 API 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-650">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="25fe6-651">作业级装载</span><span class="sxs-lookup"><span data-stu-id="25fe6-651">Job level mounting</span></span>
 - <span data-ttu-id="25fe6-652">使用机密值的环境变量</span><span class="sxs-lookup"><span data-stu-id="25fe6-652">Environment variables with secret values</span></span>
 - <span data-ttu-id="25fe6-653">性能计数器设置</span><span class="sxs-lookup"><span data-stu-id="25fe6-653">Performance counters settings</span></span>
 - <span data-ttu-id="25fe6-654">报告作业特定的路径段</span><span class="sxs-lookup"><span data-stu-id="25fe6-654">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="25fe6-655">支持“列出文件”API 中的子文件夹</span><span class="sxs-lookup"><span data-stu-id="25fe6-655">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="25fe6-656">使用情况和限制报告</span><span class="sxs-lookup"><span data-stu-id="25fe6-656">Usage and limits reporting</span></span>
 - <span data-ttu-id="25fe6-657">允许为 NFS 服务器指定缓存类型</span><span class="sxs-lookup"><span data-stu-id="25fe6-657">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="25fe6-658">支持自定义映像</span><span class="sxs-lookup"><span data-stu-id="25fe6-658">Support for custom images</span></span>
 - <span data-ttu-id="25fe6-659">添加了 pyTorch 工具包支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-659">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="25fe6-660">添加了 `job wait` 命令，以允许等待作业完成和报告作业退出代码</span><span class="sxs-lookup"><span data-stu-id="25fe6-660">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="25fe6-661">添加了 `usage show` 命令，用于列出不同区域的当前 Batch AI 资源使用情况和限制</span><span class="sxs-lookup"><span data-stu-id="25fe6-661">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="25fe6-662">支持国家云</span><span class="sxs-lookup"><span data-stu-id="25fe6-662">National clouds are supported</span></span>
* <span data-ttu-id="25fe6-663">添加了作业命令行参数，以便除了装载配置文件以外，还能装载作业级别的文件系统</span><span class="sxs-lookup"><span data-stu-id="25fe6-663">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="25fe6-664">添加了更多选项用于自定义群集 - VM 优先级、子网、自动缩放群集的初始节点计数，以及指定自定义映像</span><span class="sxs-lookup"><span data-stu-id="25fe6-664">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="25fe6-665">添加了命令行选项用于指定 Batch AI 托管 NFS 的缓存类型</span><span class="sxs-lookup"><span data-stu-id="25fe6-665">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="25fe6-666">简化了在配置文件中指定装载文件系统的方法。</span><span class="sxs-lookup"><span data-stu-id="25fe6-666">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="25fe6-667">现在，可以省略 Azure 文件共享和 Azure Blob 容器的凭据 - CLI 将会使用通过命令行参数提供的或通过环境变量指定的存储帐户密钥来填充缺少的凭据，或者从 Azure 存储查询密钥（如果存储帐户属于当前订阅）</span><span class="sxs-lookup"><span data-stu-id="25fe6-667">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="25fe6-668">作业完成后（成功、失败、已终止或已删除），作业文件流命令现在会自动完成</span><span class="sxs-lookup"><span data-stu-id="25fe6-668">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="25fe6-669">改进了 `show` 操作的 `table` 输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-669">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="25fe6-670">添加了 `--use-auto-storage` 选项用于创建群集。</span><span class="sxs-lookup"><span data-stu-id="25fe6-670">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="25fe6-671">使用此选项可以更方便地管理存储帐户，以及将 Azure 文件共享和 Azure Blob 容器装载到群集</span><span class="sxs-lookup"><span data-stu-id="25fe6-671">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="25fe6-672">为 `cluster create` 和 `file-server create` 添加了 `--generate-ssh-keys` 选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-672">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="25fe6-673">添加了通过命令行提供节点设置任务的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-673">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="25fe6-674">[重大更改]移动了 `job file` 组下面的 `job stream-file` 和 `job list-files` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-674">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="25fe6-675">[重大更改]已将 `file-server create` 命令中的 `--admin-user-name` 重命名为 `--user-name`，使其与 `cluster create` 命令一致</span><span class="sxs-lookup"><span data-stu-id="25fe6-675">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="25fe6-676">计费</span><span class="sxs-lookup"><span data-stu-id="25fe6-676">Billing</span></span>

* <span data-ttu-id="25fe6-677">添加了登记帐户命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-677">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="25fe6-678">消耗</span><span class="sxs-lookup"><span data-stu-id="25fe6-678">Consumption</span></span>

* <span data-ttu-id="25fe6-679">添加了 `marketplace` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-679">Added `marketplace` commands</span></span>
* <span data-ttu-id="25fe6-680">[重大更改] 已将 `reservations summaries` 重命名为 `reservation summary`</span><span class="sxs-lookup"><span data-stu-id="25fe6-680">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="25fe6-681">[重大更改] 已将 `reservations details` 重命名为 `reservation detail`</span><span class="sxs-lookup"><span data-stu-id="25fe6-681">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="25fe6-682">[重大更改]删除了 `reservation` 命令的 `--reservation-order-id` 和 `--reservation-id` 短选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-682">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="25fe6-683">[重大更改]删除了 `reservation summary` 命令的 `--grain` 短选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-683">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="25fe6-684">[重大更改]删除了 `pricesheet` 命令的 `--include-meter-details` 短选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-684">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-685">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-685">Container</span></span>

* <span data-ttu-id="25fe6-686">添加了 git 存储库卷装载参数 `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` 和 `--gitrepo-mount-path`</span><span class="sxs-lookup"><span data-stu-id="25fe6-686">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="25fe6-687">修复了 [#5926](https://github.com/Azure/azure-cli/issues/5926)：指定 --container-name 时 `az container exec` 失败</span><span class="sxs-lookup"><span data-stu-id="25fe6-687">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-688">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-688">Extension</span></span>

* <span data-ttu-id="25fe6-689">已将分配检查消息更改为调试级别</span><span class="sxs-lookup"><span data-stu-id="25fe6-689">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-690">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-690">Interactive</span></span>

* <span data-ttu-id="25fe6-691">更改为在命令不可识别时停止完成</span><span class="sxs-lookup"><span data-stu-id="25fe6-691">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="25fe6-692">添加了创建命令子树之前和之后所用的事件挂钩</span><span class="sxs-lookup"><span data-stu-id="25fe6-692">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="25fe6-693">添加了 `--ids` 参数补全</span><span class="sxs-lookup"><span data-stu-id="25fe6-693">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-694">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-694">Network</span></span>

* <span data-ttu-id="25fe6-695">修复了 [#5936](https://github.com/Azure/azure-cli/issues/5936)：无法设置 `application-gateway create` 标记</span><span class="sxs-lookup"><span data-stu-id="25fe6-695">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="25fe6-696">添加了参数 `--auth-certs`，以附加 `application-gateway http-settings [create|update]` 的身份验证证书。</span><span class="sxs-lookup"><span data-stu-id="25fe6-696">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="25fe6-697">#4910</span><span class="sxs-lookup"><span data-stu-id="25fe6-697">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="25fe6-698">添加了 `ddos-protection` 命令用于创建 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="25fe6-698">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="25fe6-699">为 `vnet [create|update]` 添加了 `--ddos-protection-plan` 支持，以便将 VNet 关联到 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="25fe6-699">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="25fe6-700">修复了 `network route-table [create|update]` 中 `--disable-bgp-route-propagation` 标志的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-700">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="25fe6-701">删除了 `network lb [create|update]` 的虚拟参数 `--public-ip-address-type` 和 `--subnet-type`</span><span class="sxs-lookup"><span data-stu-id="25fe6-701">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="25fe6-702">为 `network dns zone [import|export]` 和 `network dns record-set txt add-record` 添加了采用 RFC 1035 转义序列的 TXT 记录支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-702">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-703">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-703">Profile</span></span>

* <span data-ttu-id="25fe6-704">在 `account list` 中添加了 Azure 经典帐户支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-704">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="25fe6-705">[重大更改]删除了 `--msi` & `--msi-port` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-705">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="25fe6-706">RDBMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-706">RDBMS</span></span>

* <span data-ttu-id="25fe6-707">添加了 `georestore` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-707">Added `georestore` command</span></span>
* <span data-ttu-id="25fe6-708">删除了 `create` 命令的存储大小限制</span><span class="sxs-lookup"><span data-stu-id="25fe6-708">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-709">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-709">Resource</span></span>

* <span data-ttu-id="25fe6-710">在 `policy definition create` 中添加了对 `--metadata` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-710">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="25fe6-711">为 `policy definition update` 添加了对 `--metadata`、`--set`、`--add` 和 `--remove` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-711">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-712">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-712">SQL</span></span>

* <span data-ttu-id="25fe6-713">添加了 `sql elastic-pool op list` 和 `sql elastic-pool op cancel`</span><span class="sxs-lookup"><span data-stu-id="25fe6-713">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-714">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-714">Storage</span></span>

* <span data-ttu-id="25fe6-715">改进了有关连接字符串格式不当的错误消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-715">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-716">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-716">VM</span></span>

* <span data-ttu-id="25fe6-717">为 `vmss create` 添加了配置平台容错域计数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-717">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="25fe6-718">已将 `vmss create` 的默认值更改为区域性、大型或禁用单一位置组的规模集的标准负载均衡器</span><span class="sxs-lookup"><span data-stu-id="25fe6-718">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大更改]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="25fe6-720">为 `vm create` 添加了对公共 IP SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-720">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="25fe6-721">为 `vm secret format` 添加了 `--keyvault` 和 `--resource-group` 参数，以便在命令无法解析保管库 ID 的情况下提供支持。</span><span class="sxs-lookup"><span data-stu-id="25fe6-721">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="25fe6-722">#5718</span><span class="sxs-lookup"><span data-stu-id="25fe6-722">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="25fe6-723">改进了当资源组的位置不支持区域时，`[vm|vmss create]` 发生的错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-723">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="25fe6-724">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-724">March 27, 2018</span></span>

<span data-ttu-id="25fe6-725">版本 2.0.30</span><span class="sxs-lookup"><span data-stu-id="25fe6-725">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-726">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-726">Core</span></span>

* <span data-ttu-id="25fe6-727">为帮助中标记为预览版的扩展显示消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-727">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-728">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-728">ACS</span></span>

* <span data-ttu-id="25fe6-729">为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-729">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-730">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-730">Appservice</span></span>

* <span data-ttu-id="25fe6-731">为 `webapp update` 添加了仅限 HTTPS 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-731">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="25fe6-732">为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-732">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="25fe6-733">备份</span><span class="sxs-lookup"><span data-stu-id="25fe6-733">Backup</span></span>

* <span data-ttu-id="25fe6-734">添加了新命令 `az backup protection isenabled-for-vm`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-734">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="25fe6-735">此命令可用于检查 VM 是否已由订阅中的任何保管库备份</span><span class="sxs-lookup"><span data-stu-id="25fe6-735">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="25fe6-736">为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="25fe6-736">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="25fe6-737">更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-737">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-738">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-738">Container</span></span>

* <span data-ttu-id="25fe6-739">添加了 `container exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="25fe6-739">Added `container exec` command.</span></span> <span data-ttu-id="25fe6-740">在正在运行的容器组的容器中执行命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-740">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="25fe6-741">允许将表输出用于创建和更新容器组</span><span class="sxs-lookup"><span data-stu-id="25fe6-741">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-742">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-742">Extension</span></span>

* <span data-ttu-id="25fe6-743">为 `extension add` 添加了消息（如果扩展处于预览状态）</span><span class="sxs-lookup"><span data-stu-id="25fe6-743">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="25fe6-744">更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据</span><span class="sxs-lookup"><span data-stu-id="25fe6-744">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="25fe6-745">[重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据</span><span class="sxs-lookup"><span data-stu-id="25fe6-745">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-746">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-746">Interactive</span></span>

* <span data-ttu-id="25fe6-747">已将“完成”更改为在执行命令表加载后立即激活</span><span class="sxs-lookup"><span data-stu-id="25fe6-747">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="25fe6-748">修复了使用 `--style` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-748">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="25fe6-749">交互式词法分析器在命令表转储后实例化（如果缺失）</span><span class="sxs-lookup"><span data-stu-id="25fe6-749">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="25fe6-750">改进了完成符支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-750">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="25fe6-751">实验室</span><span class="sxs-lookup"><span data-stu-id="25fe6-751">Lab</span></span>

* <span data-ttu-id="25fe6-752">修复了 `create environment` 命令的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-752">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-753">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-753">Monitor</span></span>

* <span data-ttu-id="25fe6-754">为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="25fe6-754">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="25fe6-755">修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表</span><span class="sxs-lookup"><span data-stu-id="25fe6-755">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="25fe6-756">为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="25fe6-756">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-757">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-757">Network</span></span>

* <span data-ttu-id="25fe6-758">添加了对专用 DNS 区域的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-758">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-759">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-759">Profile</span></span>

* <span data-ttu-id="25fe6-760">为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-760">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="25fe6-761">RDBMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-761">RDBMS</span></span>

* <span data-ttu-id="25fe6-762">添加了业务模型 GA API 版本 2017-12-01</span><span class="sxs-lookup"><span data-stu-id="25fe6-762">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-763">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-763">Resource</span></span>

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="25fe6-765">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-765">Role</span></span>

* <span data-ttu-id="25fe6-766">为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-766">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="25fe6-767">更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-767">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="25fe6-768">添加了凭据管理命令 `ad sp credential [reset|list|delete]`</span><span class="sxs-lookup"><span data-stu-id="25fe6-768">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="25fe6-769">[重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”</span><span class="sxs-lookup"><span data-stu-id="25fe6-769">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="25fe6-770">为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-770">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-771">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-771">Storage</span></span>

* <span data-ttu-id="25fe6-772">修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-772">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="25fe6-773">修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-773">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-774">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-774">VM</span></span>

* <span data-ttu-id="25fe6-775">针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-775">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="25fe6-776">为 `vm [snapshot|image]` 添加了区域弹性支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-776">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="25fe6-777">更改了磁盘实例视图以更好地报告加密状态</span><span class="sxs-lookup"><span data-stu-id="25fe6-777">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="25fe6-778">[重大更改] 更改了 `vm extension delete` 以不再返回输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-778">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="25fe6-779">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-779">March 13, 2018</span></span>

<span data-ttu-id="25fe6-780">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="25fe6-780">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-781">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-781">ACR</span></span>

* <span data-ttu-id="25fe6-782">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-782">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="25fe6-783">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-783">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="25fe6-784">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="25fe6-784">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-785">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-785">ACS</span></span>

* <span data-ttu-id="25fe6-786">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="25fe6-786">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="25fe6-787">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="25fe6-787">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="25fe6-788">顾问</span><span class="sxs-lookup"><span data-stu-id="25fe6-788">Advisor</span></span>

* <span data-ttu-id="25fe6-789">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="25fe6-789">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="25fe6-790">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="25fe6-790">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="25fe6-791">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="25fe6-791">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="25fe6-792">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-792">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="25fe6-793">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-793">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-794">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-794">Appservice</span></span>

* <span data-ttu-id="25fe6-795">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="25fe6-795">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="25fe6-796">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="25fe6-796">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="25fe6-797">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="25fe6-797">Eventhubs</span></span>

* <span data-ttu-id="25fe6-798">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-798">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-799">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-799">Extension</span></span>

* <span data-ttu-id="25fe6-800">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-800">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-801">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-801">Interactive</span></span>

* <span data-ttu-id="25fe6-802">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="25fe6-802">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="25fe6-803">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="25fe6-803">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="25fe6-804">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="25fe6-804">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="25fe6-805">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="25fe6-805">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-806">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-806">Monitor</span></span>

* <span data-ttu-id="25fe6-807">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-807">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="25fe6-808">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-808">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="25fe6-809">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-809">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="25fe6-810">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-810">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-811">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-811">Network</span></span>

* <span data-ttu-id="25fe6-812">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-812">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="25fe6-813">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="25fe6-813">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="25fe6-814">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-814">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="25fe6-815">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="25fe6-815">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-816">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-816">Profile</span></span>

* <span data-ttu-id="25fe6-817">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-817">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="25fe6-818">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="25fe6-818">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="25fe6-819">RDBMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-819">RDBMS</span></span>

* <span data-ttu-id="25fe6-820">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="25fe6-820">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="25fe6-821">服务总线</span><span class="sxs-lookup"><span data-stu-id="25fe6-821">Service Bus</span></span>

* <span data-ttu-id="25fe6-822">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-822">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-823">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-823">Storage</span></span>

* <span data-ttu-id="25fe6-824">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云</span><span class="sxs-lookup"><span data-stu-id="25fe6-824">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="25fe6-825">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-825">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-826">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-826">VM</span></span>

* <span data-ttu-id="25fe6-827">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="25fe6-827">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="25fe6-828">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="25fe6-828">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="25fe6-829">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-829">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="25fe6-830">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="25fe6-830">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="25fe6-831">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-831">February 27, 2018</span></span>

<span data-ttu-id="25fe6-832">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="25fe6-832">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-833">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-833">Core</span></span>

* <span data-ttu-id="25fe6-834">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-834">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="25fe6-835">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-835">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="25fe6-836">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="25fe6-836">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-837">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-837">ACS</span></span>

* <span data-ttu-id="25fe6-838">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="25fe6-838">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="25fe6-839">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-839">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="25fe6-840">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="25fe6-840">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="25fe6-841">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="25fe6-841">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-842">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-842">Appservice</span></span>

* <span data-ttu-id="25fe6-843">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="25fe6-843">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="25fe6-844">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="25fe6-844">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="25fe6-845">认知服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-845">Cognitive Services</span></span>

* <span data-ttu-id="25fe6-846">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="25fe6-846">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="25fe6-847">消耗</span><span class="sxs-lookup"><span data-stu-id="25fe6-847">Consumption</span></span>

* <span data-ttu-id="25fe6-848">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-848">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="25fe6-849">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-849">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-850">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-850">Container</span></span>

* <span data-ttu-id="25fe6-851">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="25fe6-851">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-852">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-852">Network</span></span>

* <span data-ttu-id="25fe6-853">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="25fe6-853">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-854">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-854">Resource</span></span>

* <span data-ttu-id="25fe6-855">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-855">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-856">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-856">Role</span></span>

* <span data-ttu-id="25fe6-857">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-857">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-858">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-858">SQL</span></span>

* <span data-ttu-id="25fe6-859">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-859">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-860">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-860">Storage</span></span>

* <span data-ttu-id="25fe6-861">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="25fe6-861">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-862">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-862">VM</span></span>

* <span data-ttu-id="25fe6-863">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-863">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="25fe6-864">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-864">February 13, 2018</span></span>

<span data-ttu-id="25fe6-865">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="25fe6-865">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-866">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-866">Core</span></span>

* <span data-ttu-id="25fe6-867">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="25fe6-867">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-868">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-868">ACS</span></span>

* <span data-ttu-id="25fe6-869">[重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="25fe6-869">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="25fe6-870">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-870">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="25fe6-871">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-871">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="25fe6-872">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-872">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="25fe6-873">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="25fe6-873">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="25fe6-874">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="25fe6-874">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="25fe6-875">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-875">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="25fe6-876">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="25fe6-876">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-877">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-877">Appservice</span></span>

* <span data-ttu-id="25fe6-878">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-878">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="25fe6-879">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-879">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="25fe6-880">CDN</span><span class="sxs-lookup"><span data-stu-id="25fe6-880">CDN</span></span>

* <span data-ttu-id="25fe6-881">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-881">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-882">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-882">Container</span></span>

* <span data-ttu-id="25fe6-883">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="25fe6-883">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="25fe6-884">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-884">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="25fe6-885">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="25fe6-885">CosmosDB</span></span>

* <span data-ttu-id="25fe6-886">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-886">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-887">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-887">Extension</span></span>

* <span data-ttu-id="25fe6-888">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-888">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="25fe6-889">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-889">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="25fe6-890">反馈</span><span class="sxs-lookup"><span data-stu-id="25fe6-890">Feedback</span></span>

* <span data-ttu-id="25fe6-891">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="25fe6-891">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-892">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-892">Interactive</span></span>

* <span data-ttu-id="25fe6-893">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-893">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="25fe6-894">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-894">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-895">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-895">IoT</span></span>

* <span data-ttu-id="25fe6-896">修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-896">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="25fe6-897">修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-897">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="25fe6-898">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-898">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="25fe6-899">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="25fe6-899">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-900">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-900">Monitor</span></span>

* <span data-ttu-id="25fe6-901">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-901">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-902">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-902">Network</span></span>

* <span data-ttu-id="25fe6-903">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="25fe6-903">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="25fe6-904">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-904">Profile</span></span>

* <span data-ttu-id="25fe6-905">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="25fe6-905">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-906">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-906">Resource</span></span>

* <span data-ttu-id="25fe6-907">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="25fe6-907">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-908">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-908">Role</span></span>

* <span data-ttu-id="25fe6-909">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-909">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-910">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-910">SQL</span></span>

* <span data-ttu-id="25fe6-911">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-911">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="25fe6-912">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="25fe6-912">Added `sql db rename`</span></span>
* <span data-ttu-id="25fe6-913">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-913">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-914">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-914">Storage</span></span>

* <span data-ttu-id="25fe6-915">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="25fe6-915">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-916">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-916">VM</span></span>

* <span data-ttu-id="25fe6-917">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="25fe6-917">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="25fe6-918">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-918">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="25fe6-919">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="25fe6-919">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="25fe6-920">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-920">January 31, 2018</span></span>

<span data-ttu-id="25fe6-921">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="25fe6-921">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-922">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-922">Core</span></span>

* <span data-ttu-id="25fe6-923">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="25fe6-923">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="25fe6-924">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="25fe6-924">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="25fe6-925">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="25fe6-925">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="25fe6-926">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="25fe6-926">Use `--verbose` to see</span></span>
* <span data-ttu-id="25fe6-927">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="25fe6-927">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-928">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-928">ACS</span></span>

* <span data-ttu-id="25fe6-929">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-929">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="25fe6-930">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-930">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-931">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-931">Appservice</span></span>

* <span data-ttu-id="25fe6-932">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="25fe6-932">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="25fe6-933">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="25fe6-933">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="25fe6-934">CDN</span><span class="sxs-lookup"><span data-stu-id="25fe6-934">CDN</span></span>

* <span data-ttu-id="25fe6-935">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-935">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="25fe6-936">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="25fe6-936">CosmosDB</span></span>

* <span data-ttu-id="25fe6-937">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="25fe6-937">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-938">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-938">Interactive</span></span>

* <span data-ttu-id="25fe6-939">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-939">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-940">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-940">Network</span></span>

* <span data-ttu-id="25fe6-941">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="25fe6-941">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="25fe6-942">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-942">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="25fe6-943">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="25fe6-943">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="25fe6-944">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-944">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="25fe6-945">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-945">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="25fe6-946">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="25fe6-946">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="25fe6-947">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-947">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="25fe6-948">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-948">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="25fe6-949">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-949">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="25fe6-950">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-950">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-951">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-951">Profile</span></span>

* <span data-ttu-id="25fe6-952">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="25fe6-952">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-953">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-953">Resource</span></span>

* <span data-ttu-id="25fe6-954">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-954">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-955">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-955">Storage</span></span>

* <span data-ttu-id="25fe6-956">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-956">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="25fe6-957">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="25fe6-957">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="25fe6-958">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-958">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="25fe6-959">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="25fe6-959">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="25fe6-960">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-960">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-961">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-961">VM</span></span>

* <span data-ttu-id="25fe6-962">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-962">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="25fe6-963">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-963">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="25fe6-964">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-964">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="25fe6-965">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="25fe6-965">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="25fe6-966">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-966">January 17, 2018</span></span>

<span data-ttu-id="25fe6-967">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="25fe6-967">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-968">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-968">ACR</span></span>

* <span data-ttu-id="25fe6-969">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-969">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="25fe6-970">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="25fe6-970">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-971">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-971">ACS</span></span>

* <span data-ttu-id="25fe6-972">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-972">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="25fe6-973">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="25fe6-973">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-974">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-974">Appservice</span></span>

* <span data-ttu-id="25fe6-975">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-975">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="25fe6-976">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-976">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="25fe6-977">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-977">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="25fe6-978">备份</span><span class="sxs-lookup"><span data-stu-id="25fe6-978">Backup</span></span>

* <span data-ttu-id="25fe6-979">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="25fe6-979">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="25fe6-980">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-980">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="25fe6-981">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="25fe6-981">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="25fe6-982">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-982">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="25fe6-983">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="25fe6-983">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-984">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-984">Batch</span></span>

* <span data-ttu-id="25fe6-985">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="25fe6-985">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="25fe6-986">云</span><span class="sxs-lookup"><span data-stu-id="25fe6-986">Cloud</span></span>

* <span data-ttu-id="25fe6-987">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="25fe6-987">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="25fe6-988">消耗</span><span class="sxs-lookup"><span data-stu-id="25fe6-988">Consumption</span></span>

* <span data-ttu-id="25fe6-989">添加了用于预留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="25fe6-989">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="25fe6-990">事件网格</span><span class="sxs-lookup"><span data-stu-id="25fe6-990">Event Grid</span></span>

* <span data-ttu-id="25fe6-991">[重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="25fe6-991">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="25fe6-992">[重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="25fe6-992">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="25fe6-993">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="25fe6-993">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="25fe6-994">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="25fe6-994">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="25fe6-995">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="25fe6-995">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="25fe6-996">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="25fe6-996">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="25fe6-997">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-997">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="25fe6-998">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-998">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-999">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-999">Interactive</span></span>

* <span data-ttu-id="25fe6-1000">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1000">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="25fe6-1001">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1001">Fixed errors on startup</span></span>
* <span data-ttu-id="25fe6-1002">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1002">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-1003">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-1003">IoT</span></span>

* <span data-ttu-id="25fe6-1004">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1004">Added support for device provisioning service</span></span>
* <span data-ttu-id="25fe6-1005">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1005">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="25fe6-1006">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="25fe6-1006">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-1007">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-1007">Monitor</span></span>

* <span data-ttu-id="25fe6-1008">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1008">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="25fe6-1009">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1009">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="25fe6-1010">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="25fe6-1010">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1011">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1011">Network</span></span>

* <span data-ttu-id="25fe6-1012">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1012">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="25fe6-1013">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1013">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-1014">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1014">Profile</span></span>

* <span data-ttu-id="25fe6-1015">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1015">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-1016">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-1016">Role</span></span>

* <span data-ttu-id="25fe6-1017">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="25fe6-1017">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="25fe6-1018">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="25fe6-1018">Service Fabric</span></span>

* <span data-ttu-id="25fe6-1019">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-1019">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="25fe6-1020">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1020">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1021">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1021">VM</span></span>

* <span data-ttu-id="25fe6-1022">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1022">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="25fe6-1023">[重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1023">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="25fe6-1024">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1024">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="25fe6-1025">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1025">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="25fe6-1026">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1026">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="25fe6-1027">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1027">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="25fe6-1028">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1028">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="25fe6-1029">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1029">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="25fe6-1030">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1030">December 19, 2017</span></span>

<span data-ttu-id="25fe6-1031">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="25fe6-1031">Version 2.0.23</span></span>

* <span data-ttu-id="25fe6-1032">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1032">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-1033">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1033">Container</span></span>

* <span data-ttu-id="25fe6-1034">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="25fe6-1034">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1035">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1035">Network</span></span>

* <span data-ttu-id="25fe6-1036">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1036">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="25fe6-1037">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1037">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1038">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1038">Storage</span></span>

* <span data-ttu-id="25fe6-1039">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1039">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1040">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1040">VM</span></span>

* <span data-ttu-id="25fe6-1041">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1041">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="25fe6-1042">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1042">December 5, 2017</span></span>

<span data-ttu-id="25fe6-1043">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="25fe6-1043">Version 2.0.22</span></span>

* <span data-ttu-id="25fe6-1044">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1044">Removed `az component` commands.</span></span> <span data-ttu-id="25fe6-1045">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1045">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-1046">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1046">Core</span></span>
* <span data-ttu-id="25fe6-1047">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="25fe6-1047">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="25fe6-1048">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1048">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1049">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1049">ACS</span></span>

* <span data-ttu-id="25fe6-1050">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1050">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="25fe6-1051">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="25fe6-1051">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="25fe6-1052">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="25fe6-1052">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="25fe6-1053">顾问</span><span class="sxs-lookup"><span data-stu-id="25fe6-1053">Advisor</span></span>

* <span data-ttu-id="25fe6-1054">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1054">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1055">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1055">Appservice</span></span>

* <span data-ttu-id="25fe6-1056">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1056">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="25fe6-1057">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="25fe6-1057">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="25fe6-1058">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1058">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="25fe6-1059">消耗</span><span class="sxs-lookup"><span data-stu-id="25fe6-1059">Consumption</span></span>

* <span data-ttu-id="25fe6-1060">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1060">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-1061">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1061">Container</span></span>

* <span data-ttu-id="25fe6-1062">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="25fe6-1062">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-1063">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-1063">Monitor</span></span>

* <span data-ttu-id="25fe6-1064">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1064">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1065">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1065">Resource</span></span>

* <span data-ttu-id="25fe6-1066">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1066">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-1067">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-1067">Role</span></span>

* <span data-ttu-id="25fe6-1068">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1068">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="25fe6-1069">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="25fe6-1069">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="25fe6-1070">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="25fe6-1070">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1071">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1071">SQL</span></span>

* <span data-ttu-id="25fe6-1072">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1072">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="25fe6-1073">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1073">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1074">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1074">VM</span></span>

* <span data-ttu-id="25fe6-1075">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1075">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="25fe6-1076">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1076">November 14, 2017</span></span>

<span data-ttu-id="25fe6-1077">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="25fe6-1077">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-1078">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-1078">ACR</span></span>

* <span data-ttu-id="25fe6-1079">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1079">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="25fe6-1080">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1080">ACS</span></span>

* <span data-ttu-id="25fe6-1081">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1081">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="25fe6-1082">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-1082">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="25fe6-1083">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1083">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="25fe6-1084">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1084">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="25fe6-1085">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1085">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1086">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1086">Appservice</span></span>

* <span data-ttu-id="25fe6-1087">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1087">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="25fe6-1088">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-1088">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="25fe6-1089">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-1089">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="25fe6-1090">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1090">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="25fe6-1091">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1091">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="25fe6-1092">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1092">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-1093">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-1093">Batch</span></span>

* <span data-ttu-id="25fe6-1094">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1094">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="25fe6-1095">Batchai</span><span class="sxs-lookup"><span data-stu-id="25fe6-1095">Batchai</span></span>

* <span data-ttu-id="25fe6-1096">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="25fe6-1096">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="25fe6-1097">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="25fe6-1097">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="25fe6-1098">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="25fe6-1098">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="25fe6-1099">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="25fe6-1099">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="25fe6-1100">云</span><span class="sxs-lookup"><span data-stu-id="25fe6-1100">Cloud</span></span>

* <span data-ttu-id="25fe6-1101">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="25fe6-1101">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-1102">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1102">Container</span></span>

* <span data-ttu-id="25fe6-1103">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1103">Added support to open multiple ports</span></span>
* <span data-ttu-id="25fe6-1104">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="25fe6-1104">Added container group restart policy</span></span>
* <span data-ttu-id="25fe6-1105">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1105">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="25fe6-1106">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="25fe6-1106">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="25fe6-1107">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="25fe6-1107">Data Lake Analytics</span></span>

* <span data-ttu-id="25fe6-1108">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1108">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="25fe6-1109">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25fe6-1109">Data Lake Store</span></span>

* <span data-ttu-id="25fe6-1110">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1110">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-1111">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-1111">Extension</span></span>

* <span data-ttu-id="25fe6-1112">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="25fe6-1112">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="25fe6-1113">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="25fe6-1113">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-1114">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-1114">IoT</span></span>

* <span data-ttu-id="25fe6-1115">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1115">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-1116">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-1116">Monitor</span></span>

* <span data-ttu-id="25fe6-1117">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1117">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1118">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1118">Network</span></span>

* <span data-ttu-id="25fe6-1119">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1119">Added support for CAA DNS records</span></span>
* <span data-ttu-id="25fe6-1120">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1120">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="25fe6-1121">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1121">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="25fe6-1122">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1122">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="25fe6-1123">预留</span><span class="sxs-lookup"><span data-stu-id="25fe6-1123">Reservations</span></span>

* <span data-ttu-id="25fe6-1124">初始预览版</span><span class="sxs-lookup"><span data-stu-id="25fe6-1124">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1125">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1125">Resource</span></span>

* <span data-ttu-id="25fe6-1126">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1126">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1127">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1127">SQL</span></span>

* <span data-ttu-id="25fe6-1128">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1128">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1129">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1129">Storage</span></span>

* <span data-ttu-id="25fe6-1130">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1130">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="25fe6-1131">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1131">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="25fe6-1132">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1132">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="25fe6-1133">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1133">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="25fe6-1134">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1134">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="25fe6-1135">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1135">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="25fe6-1136">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1136">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1137">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1137">VM</span></span>

* <span data-ttu-id="25fe6-1138">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1138">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="25fe6-1139">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1139">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="25fe6-1140">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1140">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="25fe6-1141">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1141">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="25fe6-1142">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1142">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="25fe6-1143">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1143">October 24, 2017</span></span>

<span data-ttu-id="25fe6-1144">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="25fe6-1144">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-1145">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1145">Core</span></span>

* <span data-ttu-id="25fe6-1146">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1146">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-1147">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-1147">ACR</span></span>

* <span data-ttu-id="25fe6-1148">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1148">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="25fe6-1149">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1149">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="25fe6-1150">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1150">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1151">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1151">ACS</span></span>

* <span data-ttu-id="25fe6-1152">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1152">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="25fe6-1153">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1153">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1154">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1154">Appservice</span></span>

* <span data-ttu-id="25fe6-1155">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1155">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="25fe6-1156">组件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1156">Component</span></span>

* <span data-ttu-id="25fe6-1157">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="25fe6-1157">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-1158">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-1158">Monitor</span></span>

* <span data-ttu-id="25fe6-1159">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1159">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1160">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1160">Resource</span></span>

* <span data-ttu-id="25fe6-1161">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1161">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="25fe6-1162">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="25fe6-1162">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1163">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1163">VM</span></span>

* <span data-ttu-id="25fe6-1164">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1164">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="25fe6-1165">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1165">October 9, 2017</span></span>

<span data-ttu-id="25fe6-1166">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="25fe6-1166">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-1167">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1167">Core</span></span>

* <span data-ttu-id="25fe6-1168">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1168">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1169">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1169">Appservice</span></span>

* <span data-ttu-id="25fe6-1170">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="25fe6-1170">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-1171">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-1171">Batch</span></span>

* <span data-ttu-id="25fe6-1172">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="25fe6-1172">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="25fe6-1173">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="25fe6-1173">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="25fe6-1174">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1174">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="25fe6-1175">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1175">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="25fe6-1176">Batchai</span><span class="sxs-lookup"><span data-stu-id="25fe6-1176">Batchai</span></span>

* <span data-ttu-id="25fe6-1177">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1177">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-1178">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-1178">Keyvault</span></span>

* <span data-ttu-id="25fe6-1179">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1179">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="25fe6-1180">(#4448)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1180">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="25fe6-1181">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1181">Network</span></span>

* <span data-ttu-id="25fe6-1182">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="25fe6-1182">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="25fe6-1183">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1183">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1184">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1184">Resource</span></span>

* <span data-ttu-id="25fe6-1185">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1185">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="25fe6-1186">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="25fe6-1186">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="25fe6-1187">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="25fe6-1187">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="25fe6-1188">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="25fe6-1188">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1189">Sql</span><span class="sxs-lookup"><span data-stu-id="25fe6-1189">Sql</span></span>

* <span data-ttu-id="25fe6-1190">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1190">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="25fe6-1191">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="25fe6-1191">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="25fe6-1192">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="25fe6-1192">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1193">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1193">Storage</span></span>

* <span data-ttu-id="25fe6-1194">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1194">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1195">Vm</span><span class="sxs-lookup"><span data-stu-id="25fe6-1195">Vm</span></span>

* <span data-ttu-id="25fe6-1196">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="25fe6-1196">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="25fe6-1197">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1197">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="25fe6-1198">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1198">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="25fe6-1199">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1199">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="25fe6-1200">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1200">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="25fe6-1201">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1201">September 22, 2017</span></span>

<span data-ttu-id="25fe6-1202">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="25fe6-1202">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1203">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1203">Resource</span></span>

* <span data-ttu-id="25fe6-1204">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1204">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="25fe6-1205">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1205">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="25fe6-1206">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1206">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="25fe6-1207">[重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1207">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1208">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1208">Network</span></span>

* <span data-ttu-id="25fe6-1209">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1209">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="25fe6-1210">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1210">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="25fe6-1211">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1211">Added `asg` application security group commands</span></span>
* <span data-ttu-id="25fe6-1212">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1212">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="25fe6-1213">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1213">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="25fe6-1214">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1214">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="25fe6-1215">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1215">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1216">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1216">Storage</span></span>

* <span data-ttu-id="25fe6-1217">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1217">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="25fe6-1218">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="25fe6-1218">Eventgrid</span></span>

* <span data-ttu-id="25fe6-1219">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1219">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1220">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1220">SQL</span></span>

* <span data-ttu-id="25fe6-1221">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1221">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="25fe6-1222">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1222">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="25fe6-1223">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1223">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-1224">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-1224">Keyvault</span></span>

* <span data-ttu-id="25fe6-1225">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1225">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1226">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1226">VM</span></span>

* <span data-ttu-id="25fe6-1227">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1227">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="25fe6-1228">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1228">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="25fe6-1229">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1229">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="25fe6-1230">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1230">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="25fe6-1231">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1231">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="25fe6-1232">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1232">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1233">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1233">ACS</span></span>

* <span data-ttu-id="25fe6-1234">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1234">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1235">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1235">Appservice</span></span>

* <span data-ttu-id="25fe6-1236">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1236">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="25fe6-1237">备份</span><span class="sxs-lookup"><span data-stu-id="25fe6-1237">Backup</span></span>

* <span data-ttu-id="25fe6-1238">预览版</span><span class="sxs-lookup"><span data-stu-id="25fe6-1238">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="25fe6-1239">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1239">September 11, 2017</span></span>

<span data-ttu-id="25fe6-1240">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="25fe6-1240">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="25fe6-1241">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1241">Core</span></span>

* <span data-ttu-id="25fe6-1242">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-1242">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="25fe6-1243">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1243">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1244">Acs</span><span class="sxs-lookup"><span data-stu-id="25fe6-1244">Acs</span></span>

* <span data-ttu-id="25fe6-1245">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1245">Added `acs list-locations` command</span></span>
* <span data-ttu-id="25fe6-1246">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1246">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1247">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1247">Appservice</span></span>

* <span data-ttu-id="25fe6-1248">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1248">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="25fe6-1249">CDN</span><span class="sxs-lookup"><span data-stu-id="25fe6-1249">CDN</span></span>

* <span data-ttu-id="25fe6-1250">修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1250">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="25fe6-1251">分机</span><span class="sxs-lookup"><span data-stu-id="25fe6-1251">Extension</span></span>

* <span data-ttu-id="25fe6-1252">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1252">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-1253">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-1253">Keyvault</span></span>

* <span data-ttu-id="25fe6-1254">为 `keyvault set-policy` 修复了权限区分大小写的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1254">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1255">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1255">Network</span></span>

* <span data-ttu-id="25fe6-1256">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1256">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="25fe6-1257">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1257">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="25fe6-1258">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1258">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="25fe6-1259">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1259">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="25fe6-1260">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1260">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1261">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1261">Resource</span></span>

* <span data-ttu-id="25fe6-1262">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="25fe6-1262">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="25fe6-1263">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1263">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="25fe6-1264">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1264">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="25fe6-1265">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1265">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1266">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1266">SQL</span></span>

* <span data-ttu-id="25fe6-1267">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1267">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1268">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1268">VM</span></span>

* <span data-ttu-id="25fe6-1269">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="25fe6-1269">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="25fe6-1270">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="25fe6-1270">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="25fe6-1271">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1271">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="25fe6-1272">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="25fe6-1272">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="25fe6-1273">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-1273">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="25fe6-1274">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1274">August 31, 2017</span></span>

<span data-ttu-id="25fe6-1275">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="25fe6-1275">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-1276">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-1276">Keyvault</span></span>

* <span data-ttu-id="25fe6-1277">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1277">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="25fe6-1278">Sf</span><span class="sxs-lookup"><span data-stu-id="25fe6-1278">Sf</span></span>

* <span data-ttu-id="25fe6-1279">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1279">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1280">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1280">Storage</span></span>

* <span data-ttu-id="25fe6-1281">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1281">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="25fe6-1282">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="25fe6-1282">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="25fe6-1283">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1283">August 28, 2017</span></span>

<span data-ttu-id="25fe6-1284">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="25fe6-1284">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="25fe6-1285">CLI</span><span class="sxs-lookup"><span data-stu-id="25fe6-1285">CLI</span></span>

* <span data-ttu-id="25fe6-1286">在 `--version` 中添加了法律说明</span><span class="sxs-lookup"><span data-stu-id="25fe6-1286">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1287">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1287">ACS</span></span>

* <span data-ttu-id="25fe6-1288">更正了预览区域</span><span class="sxs-lookup"><span data-stu-id="25fe6-1288">Corrected preview regions</span></span>
* <span data-ttu-id="25fe6-1289">正确设置了默认 `dns_name_prefix` 的格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-1289">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="25fe6-1290">优化了 acs 命令输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-1290">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1291">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1291">Appservice</span></span>

* <span data-ttu-id="25fe6-1292">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致</span><span class="sxs-lookup"><span data-stu-id="25fe6-1292">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="25fe6-1293">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="25fe6-1293">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="25fe6-1294">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1294">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="25fe6-1295">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="25fe6-1295">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="25fe6-1296">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="25fe6-1296">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-1297">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-1297">IoT</span></span>

* <span data-ttu-id="25fe6-1298">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="25fe6-1298">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1299">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1299">Network</span></span>

* <span data-ttu-id="25fe6-1300">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1300">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="25fe6-1301">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1301">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="25fe6-1302">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1302">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="25fe6-1303">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1303">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="25fe6-1304">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1304">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-1305">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1305">Profile</span></span>

* <span data-ttu-id="25fe6-1306">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="25fe6-1306">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="25fe6-1307">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="25fe6-1307">Service Fabric</span></span>

* <span data-ttu-id="25fe6-1308">预览版</span><span class="sxs-lookup"><span data-stu-id="25fe6-1308">Preview release</span></span>
* <span data-ttu-id="25fe6-1309">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="25fe6-1309">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="25fe6-1310">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1310">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="25fe6-1311">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1311">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1312">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1312">Storage</span></span>

* <span data-ttu-id="25fe6-1313">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="25fe6-1313">Enabled setting blob tier</span></span>
* <span data-ttu-id="25fe6-1314">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="25fe6-1314">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="25fe6-1315">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1315">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="25fe6-1316">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1316">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="25fe6-1317">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1317">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="25fe6-1318">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="25fe6-1318">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1319">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1319">VM</span></span>

* <span data-ttu-id="25fe6-1320">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1320">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="25fe6-1321">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1321">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="25fe6-1322">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="25fe6-1322">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="25fe6-1323">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1323">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="25fe6-1324">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1324">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="25fe6-1325">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1325">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="25fe6-1326">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1326">August 15, 2017</span></span>

<span data-ttu-id="25fe6-1327">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="25fe6-1327">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1328">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1328">ACS</span></span>

* <span data-ttu-id="25fe6-1329">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="25fe6-1329">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1330">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1330">Appservice</span></span>

* <span data-ttu-id="25fe6-1331">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1331">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="25fe6-1332">事件网格</span><span class="sxs-lookup"><span data-stu-id="25fe6-1332">Event Grid</span></span>

* <span data-ttu-id="25fe6-1333">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="25fe6-1333">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="25fe6-1334">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1334">August 11, 2017</span></span>

<span data-ttu-id="25fe6-1335">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="25fe6-1335">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1336">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1336">ACS</span></span>

* <span data-ttu-id="25fe6-1337">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="25fe6-1337">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-1338">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-1338">Batch</span></span>

* <span data-ttu-id="25fe6-1339">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="25fe6-1339">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="25fe6-1340">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1340">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="25fe6-1341">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1341">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="25fe6-1342">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="25fe6-1342">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="25fe6-1343">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="25fe6-1343">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="25fe6-1344">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="25fe6-1344">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="25fe6-1345">组件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1345">Component</span></span>

* <span data-ttu-id="25fe6-1346">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-1346">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="25fe6-1347">容器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1347">Container</span></span>

* <span data-ttu-id="25fe6-1348">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1348">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="25fe6-1349">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25fe6-1349">Data Lake Store</span></span>

* <span data-ttu-id="25fe6-1350">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1350">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="25fe6-1351">事件网格</span><span class="sxs-lookup"><span data-stu-id="25fe6-1351">Event Grid</span></span>

* <span data-ttu-id="25fe6-1352">初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1352">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1353">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1353">Network</span></span>

* <span data-ttu-id="25fe6-1354">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1354">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="25fe6-1355">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1355">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="25fe6-1356">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1356">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="25fe6-1357">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="25fe6-1357">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-1358">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1358">Profile</span></span>

* <span data-ttu-id="25fe6-1359">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="25fe6-1359">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1360">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1360">Storage</span></span>

* <span data-ttu-id="25fe6-1361">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1361">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1362">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1362">VM</span></span>

* <span data-ttu-id="25fe6-1363">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1363">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="25fe6-1364">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1364">Exposed `list-skus` command</span></span>
* <span data-ttu-id="25fe6-1365">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="25fe6-1365">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="25fe6-1366">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="25fe6-1366">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="25fe6-1367">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="25fe6-1367">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="25fe6-1368">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1368">July 28, 2017</span></span>

<span data-ttu-id="25fe6-1369">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="25fe6-1369">Version 2.0.12</span></span>

* <span data-ttu-id="25fe6-1370">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1370">Added container commands</span></span>
* <span data-ttu-id="25fe6-1371">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="25fe6-1371">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="25fe6-1372">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1372">Core</span></span>

* <span data-ttu-id="25fe6-1373">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1373">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="25fe6-1374">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="25fe6-1374">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="25fe6-1375">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="25fe6-1375">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="25fe6-1376">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1376">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="25fe6-1377">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-1377">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="25fe6-1378">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1378">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="25fe6-1379">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1379">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="25fe6-1380">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1380">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="25fe6-1381">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1381">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="25fe6-1382">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="25fe6-1382">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="25fe6-1383">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="25fe6-1383">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="25fe6-1384">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1384">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="25fe6-1385">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="25fe6-1385">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="25fe6-1386">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="25fe6-1386">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="25fe6-1387">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1387">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="25fe6-1388">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1388">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="25fe6-1389">ACR</span><span class="sxs-lookup"><span data-stu-id="25fe6-1389">ACR</span></span>

* <span data-ttu-id="25fe6-1390">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1390">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="25fe6-1391">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="25fe6-1391">Support SKU update for managed registries</span></span>
* <span data-ttu-id="25fe6-1392">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="25fe6-1392">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="25fe6-1393">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="25fe6-1393">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="25fe6-1394">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1394">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="25fe6-1395">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1395">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1396">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1396">ACS</span></span>

* <span data-ttu-id="25fe6-1397">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1397">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1398">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1398">Appservice</span></span>

* <span data-ttu-id="25fe6-1399">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1399">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="25fe6-1400">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="25fe6-1400">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="25fe6-1401">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1401">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="25fe6-1402">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1402">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="25fe6-1403">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1403">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="25fe6-1404">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1404">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="25fe6-1405">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1405">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="25fe6-1406">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1406">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="25fe6-1407">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1407">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="25fe6-1408">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1408">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="25fe6-1409">Batch</span><span class="sxs-lookup"><span data-stu-id="25fe6-1409">Batch</span></span>

* <span data-ttu-id="25fe6-1410">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1410">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="25fe6-1411">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1411">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="25fe6-1412">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1412">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="25fe6-1413">CDN</span><span class="sxs-lookup"><span data-stu-id="25fe6-1413">CDN</span></span>

* <span data-ttu-id="25fe6-1414">当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息</span><span class="sxs-lookup"><span data-stu-id="25fe6-1414">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="25fe6-1415">云</span><span class="sxs-lookup"><span data-stu-id="25fe6-1415">Cloud</span></span>

* <span data-ttu-id="25fe6-1416">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-1416">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="25fe6-1417">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="25fe6-1417">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="25fe6-1418">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="25fe6-1418">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="25fe6-1419">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1419">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="25fe6-1420">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1420">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="25fe6-1421">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="25fe6-1421">CosmosDB</span></span>

* <span data-ttu-id="25fe6-1422">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1422">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="25fe6-1423">添加了对集合默认 TTL 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1423">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="25fe6-1424">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="25fe6-1424">Data Lake Analytics</span></span>

* <span data-ttu-id="25fe6-1425">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1425">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="25fe6-1426">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1426">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="25fe6-1427">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1427">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="25fe6-1428">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25fe6-1428">Data Lake Store</span></span>

* <span data-ttu-id="25fe6-1429">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1429">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="25fe6-1430">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1430">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="25fe6-1431">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1431">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="25fe6-1432">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="25fe6-1432">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="25fe6-1433">交互</span><span class="sxs-lookup"><span data-stu-id="25fe6-1433">Interactive</span></span>

* <span data-ttu-id="25fe6-1434">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="25fe6-1434">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="25fe6-1435">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="25fe6-1435">Increased test coverage</span></span>
* <span data-ttu-id="25fe6-1436">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1436">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="25fe6-1437">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1437">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="25fe6-1438">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1438">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="25fe6-1439">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1439">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="25fe6-1440">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1440">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="25fe6-1441">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="25fe6-1441">Added `--progress` flag</span></span>
* <span data-ttu-id="25fe6-1442">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1442">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="25fe6-1443">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1443">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="25fe6-1444">IoT</span><span class="sxs-lookup"><span data-stu-id="25fe6-1444">IoT</span></span>

* <span data-ttu-id="25fe6-1445">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1445">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="25fe6-1446">(#3934)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1446">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="25fe6-1447">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="25fe6-1447">Key vault</span></span>

* <span data-ttu-id="25fe6-1448">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1448">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="25fe6-1449">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1449">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="25fe6-1450">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1450">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="25fe6-1451">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1451">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="25fe6-1452">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1452">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="25fe6-1453">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1453">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="25fe6-1454">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1454">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="25fe6-1455">(#3307)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1455">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="25fe6-1456">实验室</span><span class="sxs-lookup"><span data-stu-id="25fe6-1456">Lab</span></span>

* <span data-ttu-id="25fe6-1457">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1457">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="25fe6-1458">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="25fe6-1458">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-1459">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-1459">Monitor</span></span>

* <span data-ttu-id="25fe6-1460">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1460">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="25fe6-1461">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1461">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="25fe6-1462">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1462">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="25fe6-1463">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1463">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="25fe6-1464">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1464">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="25fe6-1465">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1465">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="25fe6-1466">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="25fe6-1466">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="25fe6-1467">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="25fe6-1467">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="25fe6-1468">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="25fe6-1468">`location` no longer required</span></span>
  * <span data-ttu-id="25fe6-1469">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1469">Add name and ID support for target</span></span>
  * <span data-ttu-id="25fe6-1470">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1470">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="25fe6-1471">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="25fe6-1471">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="25fe6-1472">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1472">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="25fe6-1473">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-1473">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="25fe6-1474">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="25fe6-1474">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="25fe6-1475">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="25fe6-1475">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1476">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1476">Network</span></span>

* <span data-ttu-id="25fe6-1477">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1477">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="25fe6-1478">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1478">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="25fe6-1479">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1479">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="25fe6-1480">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1480">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="25fe6-1481">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1481">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="25fe6-1482">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1482">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="25fe6-1483">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1483">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="25fe6-1484">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1484">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="25fe6-1485">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1485">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="25fe6-1486">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1486">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="25fe6-1487">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1487">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="25fe6-1488">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1488">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="25fe6-1489">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1489">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="25fe6-1490">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1490">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="25fe6-1491">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1491">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="25fe6-1492">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1492">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="25fe6-1493">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1493">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="25fe6-1494">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1494">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="25fe6-1495">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1495">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="25fe6-1496">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1496">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="25fe6-1497">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1497">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="25fe6-1498">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1498">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="25fe6-1499">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-1499">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="25fe6-1500">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="25fe6-1500">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="25fe6-1501">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="25fe6-1501">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="25fe6-1502">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="25fe6-1502">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="25fe6-1503">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="25fe6-1503">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-1504">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1504">Profile</span></span>

* <span data-ttu-id="25fe6-1505">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="25fe6-1505">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="25fe6-1506">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-1506">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="25fe6-1507">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-1507">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="25fe6-1508">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="25fe6-1508">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="25fe6-1509">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="25fe6-1509">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="25fe6-1510">RDBMS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1510">RDBMS</span></span>

* <span data-ttu-id="25fe6-1511">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1511">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="25fe6-1512">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1512">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="25fe6-1513">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1513">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="25fe6-1514">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1514">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1515">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1515">Resource</span></span>

* <span data-ttu-id="25fe6-1516">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="25fe6-1516">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="25fe6-1517">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="25fe6-1517">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="25fe6-1518">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1518">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="25fe6-1519">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1519">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="25fe6-1520">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1520">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="25fe6-1521">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1521">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="25fe6-1522">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1522">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="25fe6-1523">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1523">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-1524">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-1524">Role</span></span>

* <span data-ttu-id="25fe6-1525">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="25fe6-1525">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="25fe6-1526">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1526">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="25fe6-1527">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="25fe6-1527">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="25fe6-1528">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="25fe6-1528">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="25fe6-1529">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="25fe6-1529">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="25fe6-1530">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="25fe6-1530">Service Fabric</span></span>
* <span data-ttu-id="25fe6-1531">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1531">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="25fe6-1532">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1532">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="25fe6-1533">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1533">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1534">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1534">SQL</span></span>

* <span data-ttu-id="25fe6-1535">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1535">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="25fe6-1536">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1536">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="25fe6-1537">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1537">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1538">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1538">Storage</span></span>

* <span data-ttu-id="25fe6-1539">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1539">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="25fe6-1540">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="25fe6-1540">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="25fe6-1541">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1541">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="25fe6-1542">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1542">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="25fe6-1543">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1543">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="25fe6-1544">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1544">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1545">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1545">VM</span></span>

* <span data-ttu-id="25fe6-1546">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="25fe6-1546">Support configuring nsg</span></span>
* <span data-ttu-id="25fe6-1547">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1547">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="25fe6-1548">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="25fe6-1548">Support managed service identities</span></span>
* <span data-ttu-id="25fe6-1549">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1549">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="25fe6-1550">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="25fe6-1550">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="25fe6-1551">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1551">May 10, 2017</span></span>

<span data-ttu-id="25fe6-1552">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="25fe6-1552">Version 2.0.6</span></span>

* <span data-ttu-id="25fe6-1553">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="25fe6-1553">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="25fe6-1554">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1554">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="25fe6-1555">包括 Data Lake Analytics 和 Data Lake Store 模块</span><span class="sxs-lookup"><span data-stu-id="25fe6-1555">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="25fe6-1556">包括认知服务模块</span><span class="sxs-lookup"><span data-stu-id="25fe6-1556">Include Cognitive Services module</span></span>
* <span data-ttu-id="25fe6-1557">包括 Service Fabric 模块</span><span class="sxs-lookup"><span data-stu-id="25fe6-1557">Include Service Fabric module</span></span>
* <span data-ttu-id="25fe6-1558">包括交互式模块（重命名 az-shell）</span><span class="sxs-lookup"><span data-stu-id="25fe6-1558">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="25fe6-1559">添加对 CDN 命令的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1559">Add support for CDN commands</span></span>
* <span data-ttu-id="25fe6-1560">删除容器模块</span><span class="sxs-lookup"><span data-stu-id="25fe6-1560">Remove Container module</span></span>
* <span data-ttu-id="25fe6-1561">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1561">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="25fe6-1562">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1562">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="25fe6-1563">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1563">Core</span></span>

* <span data-ttu-id="25fe6-1564">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="25fe6-1564">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="25fe6-1565">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1565">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="25fe6-1566">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1566">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="25fe6-1567">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1567">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="25fe6-1568">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1568">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="25fe6-1569">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1569">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="25fe6-1570">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1570">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="25fe6-1571">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1571">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="25fe6-1572">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1572">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="25fe6-1573">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1573">core: Improved performance</span></span>
* <span data-ttu-id="25fe6-1574">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="25fe6-1574">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="25fe6-1575">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="25fe6-1575">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1576">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1576">ACS</span></span>

* <span data-ttu-id="25fe6-1577">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="25fe6-1577">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="25fe6-1578">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="25fe6-1578">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="25fe6-1579">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="25fe6-1579">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="25fe6-1580">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1580">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1581">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1581">AppService</span></span>

* <span data-ttu-id="25fe6-1582">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="25fe6-1582">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="25fe6-1583">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1583">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="25fe6-1584">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="25fe6-1584">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="25fe6-1585">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1585">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="25fe6-1586">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="25fe6-1586">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="25fe6-1587">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1587">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="25fe6-1588">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="25fe6-1588">support slot swap with preview</span></span>
* <span data-ttu-id="25fe6-1589">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1589">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="25fe6-1590">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1590">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="25fe6-1591">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="25fe6-1591">CosmosDB</span></span>

* <span data-ttu-id="25fe6-1592">将 documentdb 模块重命名为 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="25fe6-1592">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="25fe6-1593">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="25fe6-1593">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="25fe6-1594">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1594">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="25fe6-1595">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1595">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="25fe6-1596">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="25fe6-1596">Data Lake Analytics</span></span>

* <span data-ttu-id="25fe6-1597">修复了在筛选作业结果和状态列表时会引发错误的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1597">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="25fe6-1598">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1598">Add support for new catalog item type: package.</span></span> <span data-ttu-id="25fe6-1599">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="25fe6-1599">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="25fe6-1600">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1600">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="25fe6-1601">表</span><span class="sxs-lookup"><span data-stu-id="25fe6-1601">Table</span></span>
  * <span data-ttu-id="25fe6-1602">表值函数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1602">Table valued function</span></span>
  * <span data-ttu-id="25fe6-1603">查看</span><span class="sxs-lookup"><span data-stu-id="25fe6-1603">View</span></span>
  * <span data-ttu-id="25fe6-1604">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1604">Table Statistics.</span></span> <span data-ttu-id="25fe6-1605">这也可以使用架构（但无需指定表名）列出</span><span class="sxs-lookup"><span data-stu-id="25fe6-1605">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="25fe6-1606">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="25fe6-1606">Data Lake Store</span></span>

* <span data-ttu-id="25fe6-1607">更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1607">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="25fe6-1608">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1608">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="25fe6-1609">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1609">missed help for access show.</span></span> <span data-ttu-id="25fe6-1610">正在添加。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1610">adding it.</span></span> <span data-ttu-id="25fe6-1611">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1611">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="25fe6-1612">查找</span><span class="sxs-lookup"><span data-stu-id="25fe6-1612">Find</span></span>

* <span data-ttu-id="25fe6-1613">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="25fe6-1613">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="25fe6-1614">KeyVault</span><span class="sxs-lookup"><span data-stu-id="25fe6-1614">KeyVault</span></span>

* <span data-ttu-id="25fe6-1615">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="25fe6-1615">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="25fe6-1616">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数</span><span class="sxs-lookup"><span data-stu-id="25fe6-1616">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="25fe6-1617">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1617">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="25fe6-1618">修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1618">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="25fe6-1619">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1619">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="25fe6-1620">实验室</span><span class="sxs-lookup"><span data-stu-id="25fe6-1620">Lab</span></span>

* <span data-ttu-id="25fe6-1621">为实验室中的环境添加 create、show、delete 和 list 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1621">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="25fe6-1622">添加 show 和 list 命令以查看实验室中的 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="25fe6-1622">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="25fe6-1623">在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1623">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="25fe6-1624">添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架</span><span class="sxs-lookup"><span data-stu-id="25fe6-1624">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="25fe6-1625">添加命令以管理实验室中的机密</span><span class="sxs-lookup"><span data-stu-id="25fe6-1625">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="25fe6-1626">监视</span><span class="sxs-lookup"><span data-stu-id="25fe6-1626">Monitor</span></span>

* <span data-ttu-id="25fe6-1627">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1627">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="25fe6-1628">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1628">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="25fe6-1629">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1629">Network</span></span>

* <span data-ttu-id="25fe6-1630">添加 `network watcher test-connectivity` 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1630">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="25fe6-1631">为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1631">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="25fe6-1632">添加对应用程序网关连接排出的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1632">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="25fe6-1633">添加对应用程序网关 WAF 规则集配置的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1633">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="25fe6-1634">添加对 ExpressRoute 路由筛选器和规则的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1634">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="25fe6-1635">添加对 TrafficManager 地理路由的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1635">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="25fe6-1636">添加对基于 VPN 连接策略的流量选择器的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1636">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="25fe6-1637">添加对 VPN 连接 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1637">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="25fe6-1638">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1638">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="25fe6-1639">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1639">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="25fe6-1640">从 `network vpn-connection list/show` 命令的输出中删除 null 值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1640">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="25fe6-1641">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1641">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="25fe6-1642">修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1642">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="25fe6-1643">修复 `dns zone import` 中无法正确导入记录的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1643">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="25fe6-1644">修复 `traffic-manager endpoint update` 不起作用的 bug</span><span class="sxs-lookup"><span data-stu-id="25fe6-1644">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="25fe6-1645">添加“network watcher”预览命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1645">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="25fe6-1646">配置文件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1646">Profile</span></span>

* <span data-ttu-id="25fe6-1647">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1647">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="25fe6-1648">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1648">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="25fe6-1649">Redis</span><span class="sxs-lookup"><span data-stu-id="25fe6-1649">Redis</span></span>

* <span data-ttu-id="25fe6-1650">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="25fe6-1650">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="25fe6-1651">弃用“update-settings”命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1651">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="25fe6-1652">资源</span><span class="sxs-lookup"><span data-stu-id="25fe6-1652">Resource</span></span>

* <span data-ttu-id="25fe6-1653">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1653">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="25fe6-1654">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1654">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="25fe6-1655">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1655">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="25fe6-1656">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1656">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="25fe6-1657">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1657">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="25fe6-1658">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1658">Add docs for az lock update.</span></span> <span data-ttu-id="25fe6-1659">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1659">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="25fe6-1660">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1660">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="25fe6-1661">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1661">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="25fe6-1662">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1662">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="25fe6-1663">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1663">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="25fe6-1664">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1664">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="25fe6-1665">角色</span><span class="sxs-lookup"><span data-stu-id="25fe6-1665">Role</span></span>

* <span data-ttu-id="25fe6-1666">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1666">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="25fe6-1667">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1667">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="25fe6-1668">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1668">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="25fe6-1669">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="25fe6-1669">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="25fe6-1670">SQL</span><span class="sxs-lookup"><span data-stu-id="25fe6-1670">SQL</span></span>

* <span data-ttu-id="25fe6-1671">添加了 az sql server list-usages 和 az sql db list-usages 命令</span><span class="sxs-lookup"><span data-stu-id="25fe6-1671">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="25fe6-1672">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1672">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="25fe6-1673">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1673">Storage</span></span>

* <span data-ttu-id="25fe6-1674">对于 `storage account create`，将位置默认为资源组位置</span><span class="sxs-lookup"><span data-stu-id="25fe6-1674">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="25fe6-1675">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1675">Add support for incremental blob copy</span></span>
* <span data-ttu-id="25fe6-1676">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="25fe6-1676">Add support for large block blob upload</span></span>
* <span data-ttu-id="25fe6-1677">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="25fe6-1677">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1678">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1678">VM</span></span>

* <span data-ttu-id="25fe6-1679">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="25fe6-1679">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="25fe6-1680">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1680">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="25fe6-1681">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="25fe6-1681">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="25fe6-1682">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="25fe6-1682">az vm/vmss disk</span></span>
  3. <span data-ttu-id="25fe6-1683">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="25fe6-1683">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="25fe6-1684">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1684">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="25fe6-1685">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1685">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="25fe6-1686">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1686">April 3, 2017</span></span>

<span data-ttu-id="25fe6-1687">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="25fe6-1687">Version 2.0.2</span></span>

<span data-ttu-id="25fe6-1688">此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件</span><span class="sxs-lookup"><span data-stu-id="25fe6-1688">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="25fe6-1689">核心</span><span class="sxs-lookup"><span data-stu-id="25fe6-1689">Core</span></span>

* <span data-ttu-id="25fe6-1690">在默认列表中添加了 acr、lab、monitor 和 find 模块</span><span class="sxs-lookup"><span data-stu-id="25fe6-1690">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="25fe6-1691">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1691">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="25fe6-1692">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1692">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="25fe6-1693">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1693">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="25fe6-1694">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1694">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="25fe6-1695">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1695">Add prompting for missing template parameters.</span></span> <span data-ttu-id="25fe6-1696">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1696">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="25fe6-1697">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="25fe6-1697">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="25fe6-1698">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="25fe6-1698">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="25fe6-1699">ACS</span><span class="sxs-lookup"><span data-stu-id="25fe6-1699">ACS</span></span>

* <span data-ttu-id="25fe6-1700">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1700">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="25fe6-1701">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1701">Add support for ssh key password prompting.</span></span> <span data-ttu-id="25fe6-1702">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1702">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="25fe6-1703">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1703">Add support for windows clusters.</span></span> <span data-ttu-id="25fe6-1704">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1704">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="25fe6-1705">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1705">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="25fe6-1706">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1706">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="25fe6-1707">应用服务</span><span class="sxs-lookup"><span data-stu-id="25fe6-1707">AppService</span></span>

* <span data-ttu-id="25fe6-1708">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1708">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="25fe6-1709">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1709">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="25fe6-1710">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1710">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="25fe6-1711">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1711">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="25fe6-1712">DataLake</span><span class="sxs-lookup"><span data-stu-id="25fe6-1712">DataLake</span></span>

* <span data-ttu-id="25fe6-1713">Data Lake Analytics 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1713">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="25fe6-1714">Data Lake Store 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="25fe6-1714">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="25fe6-1715">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="25fe6-1715">DocuemntDB</span></span>

* <span data-ttu-id="25fe6-1716">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1716">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="25fe6-1717">VM</span><span class="sxs-lookup"><span data-stu-id="25fe6-1717">VM</span></span>

* <span data-ttu-id="25fe6-1718">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1718">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="25fe6-1719">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1719">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="25fe6-1720">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1720">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="25fe6-1721">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1721">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="25fe6-1722">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1722">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="25fe6-1723">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1723">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="25fe6-1724">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="25fe6-1724">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="25fe6-1725">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="25fe6-1725">February 27, 2017</span></span>

<span data-ttu-id="25fe6-1726">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="25fe6-1726">Version 2.0.0</span></span>

<span data-ttu-id="25fe6-1727">此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1727">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="25fe6-1728">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="25fe6-1728">Container Service (acs)</span></span>
- <span data-ttu-id="25fe6-1729">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="25fe6-1729">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="25fe6-1730">网络</span><span class="sxs-lookup"><span data-stu-id="25fe6-1730">Networking</span></span>
- <span data-ttu-id="25fe6-1731">存储</span><span class="sxs-lookup"><span data-stu-id="25fe6-1731">Storage</span></span>

<span data-ttu-id="25fe6-1732">这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1732">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="25fe6-1733">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1733">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="25fe6-1734">若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1734">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="25fe6-1735">其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1735">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="25fe6-1736">此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="25fe6-1736">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="25fe6-1737">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="25fe6-1737">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="25fe6-1738">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="25fe6-1738">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="25fe6-1739">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队</span><span class="sxs-lookup"><span data-stu-id="25fe6-1739">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="25fe6-1740">通过命令行使用 `az feedback` 命令提供反馈</span><span class="sxs-lookup"><span data-stu-id="25fe6-1740">Provide feedback from the command line with the `az feedback` command</span></span>

