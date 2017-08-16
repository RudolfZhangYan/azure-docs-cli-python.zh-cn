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
ms.contentlocale: zh-CN
ms.lasthandoff: 05/11/2017
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="336df-104">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="336df-104">Azure CLI 2.0 release notes</span></span>

## <a name="may-10-2017"></a><span data-ttu-id="336df-105">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="336df-105">May 10, 2017</span></span>

<span data-ttu-id="336df-106">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="336df-106">Version 2.0.6</span></span>

* <span data-ttu-id="336df-107">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="336df-107">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="336df-108">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="336df-108">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="336df-109">包括 Data Lake Analytics 和 Data Lake Store 模块。</span><span class="sxs-lookup"><span data-stu-id="336df-109">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="336df-110">包括认知服务模块。</span><span class="sxs-lookup"><span data-stu-id="336df-110">Include Cognitive Services module.</span></span>
* <span data-ttu-id="336df-111">包括 Service Fabric 模块。</span><span class="sxs-lookup"><span data-stu-id="336df-111">Include Service Fabric module.</span></span>
* <span data-ttu-id="336df-112">包括交互式模块（重命名 az-shell）。</span><span class="sxs-lookup"><span data-stu-id="336df-112">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="336df-113">添加对 CDN 命令的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-113">Add support for CDN commands.</span></span>
* <span data-ttu-id="336df-114">删除容器模块。</span><span class="sxs-lookup"><span data-stu-id="336df-114">Remove Container module.</span></span>
* <span data-ttu-id="336df-115">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="336df-115">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="336df-116">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="336df-116">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="336df-117">核心</span><span class="sxs-lookup"><span data-stu-id="336df-117">Core</span></span>

* <span data-ttu-id="336df-118">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="336df-118">core: capture exceptions caused by unregistered provider and auto-register it</span></span>   
* <span data-ttu-id="336df-119">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="336df-119">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="336df-120">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="336df-120">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="336df-121">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="336df-121">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="336df-122">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="336df-122">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="336df-123">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="336df-123">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="336df-124">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="336df-124">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="336df-125">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="336df-125">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="336df-126">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="336df-126">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="336df-127">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="336df-127">core: Improved performance</span></span>
* <span data-ttu-id="336df-128">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="336df-128">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="336df-129">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="336df-129">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="336df-130">ACS</span><span class="sxs-lookup"><span data-stu-id="336df-130">ACS</span></span>

* <span data-ttu-id="336df-131">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="336df-131">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="336df-132">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="336df-132">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="336df-133">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="336df-133">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="336df-134">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="336df-134">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="336df-135">应用服务</span><span class="sxs-lookup"><span data-stu-id="336df-135">AppService</span></span>

* <span data-ttu-id="336df-136">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="336df-136">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="336df-137">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="336df-137">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="336df-138">创建“az webapp”以替换“az appservice web”（对于向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="336df-138">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="336df-139">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="336df-139">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="336df-140">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="336df-140">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="336df-141">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="336df-141">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="336df-142">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="336df-142">support slot swap with preview</span></span>
* <span data-ttu-id="336df-143">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="336df-143">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="336df-144">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="336df-144">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="336df-145">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="336df-145">CosmosDB</span></span>

* <span data-ttu-id="336df-146">将 DocumentDB 模块重命名为 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="336df-146">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="336df-147">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="336df-147">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="336df-148">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="336df-148">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="336df-149">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="336df-149">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="336df-150">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="336df-150">Data Lake Analytics</span></span>

* <span data-ttu-id="336df-151">Bug 修复：在筛选作业结果和状态列表时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="336df-151">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="336df-152">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="336df-152">Add support for new catalog item type: package.</span></span> <span data-ttu-id="336df-153">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="336df-153">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="336df-154">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="336df-154">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="336df-155">表</span><span class="sxs-lookup"><span data-stu-id="336df-155">Table</span></span>
  * <span data-ttu-id="336df-156">表值函数</span><span class="sxs-lookup"><span data-stu-id="336df-156">Table valued function</span></span>
  * <span data-ttu-id="336df-157">查看</span><span class="sxs-lookup"><span data-stu-id="336df-157">View</span></span>
  * <span data-ttu-id="336df-158">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="336df-158">Table Statistics.</span></span> <span data-ttu-id="336df-159">也可以使用架构列出，但无需指定表名。</span><span class="sxs-lookup"><span data-stu-id="336df-159">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="336df-160">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="336df-160">Data Lake Store</span></span>

* <span data-ttu-id="336df-161">更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。</span><span class="sxs-lookup"><span data-stu-id="336df-161">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="336df-162">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="336df-162">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="336df-163">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="336df-163">missed help for access show.</span></span> <span data-ttu-id="336df-164">正在添加。</span><span class="sxs-lookup"><span data-stu-id="336df-164">adding it.</span></span> <span data-ttu-id="336df-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="336df-165">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="336df-166">查找</span><span class="sxs-lookup"><span data-stu-id="336df-166">Find</span></span>

* <span data-ttu-id="336df-167">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="336df-167">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="336df-168">KeyVault</span><span class="sxs-lookup"><span data-stu-id="336df-168">KeyVault</span></span>

* <span data-ttu-id="336df-169">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="336df-169">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="336df-170">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。</span><span class="sxs-lookup"><span data-stu-id="336df-170">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="336df-171">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="336df-171">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="336df-172">解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。</span><span class="sxs-lookup"><span data-stu-id="336df-172">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="336df-173">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="336df-173">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="336df-174">实验室</span><span class="sxs-lookup"><span data-stu-id="336df-174">Lab</span></span>

* <span data-ttu-id="336df-175">针对实验室环境添加 create、show、delete 和 list 命令。</span><span class="sxs-lookup"><span data-stu-id="336df-175">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="336df-176">添加 show 和 list 命令，查看实验室中的 ARM 模板。</span><span class="sxs-lookup"><span data-stu-id="336df-176">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="336df-177">在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。</span><span class="sxs-lookup"><span data-stu-id="336df-177">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="336df-178">添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。</span><span class="sxs-lookup"><span data-stu-id="336df-178">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="336df-179">添加命令，管理实验室中的机密。</span><span class="sxs-lookup"><span data-stu-id="336df-179">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="336df-180">监视</span><span class="sxs-lookup"><span data-stu-id="336df-180">Monitor</span></span>

* <span data-ttu-id="336df-181">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="336df-181">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="336df-182">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="336df-182">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="336df-183">网络</span><span class="sxs-lookup"><span data-stu-id="336df-183">Network</span></span>

* <span data-ttu-id="336df-184">添加 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="336df-184">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="336df-185">添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-185">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="336df-186">添加对应用程序网关连接排出的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-186">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="336df-187">添加对应用程序网关 WAF 规则集配置的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-187">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="336df-188">添加对 ExpressRoute 路由筛选器和规则的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-188">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="336df-189">添加对 TrafficManager 地理路由的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-189">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="336df-190">添加对基于 VPN 连接策略的流量选择器的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-190">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="336df-191">添加对 VPN 连接 IPSec 策略的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-191">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="336df-192">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。</span><span class="sxs-lookup"><span data-stu-id="336df-192">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="336df-193">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="336df-193">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="336df-194">从 `network vpn-connection list/show` 命令的输出中删除 null 值。</span><span class="sxs-lookup"><span data-stu-id="336df-194">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="336df-195">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="336df-195">BC: Fix bug in the output of `vpn-connection create`</span></span> 
* <span data-ttu-id="336df-196">Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。</span><span class="sxs-lookup"><span data-stu-id="336df-196">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="336df-197">修复 `dns zone import` 中的 Bug：记录未正确导入。</span><span class="sxs-lookup"><span data-stu-id="336df-197">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="336df-198">Bug 修复：`traffic-manager endpoint update` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="336df-198">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="336df-199">添加“network watcher”预览命令。</span><span class="sxs-lookup"><span data-stu-id="336df-199">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="336df-200">配置文件</span><span class="sxs-lookup"><span data-stu-id="336df-200">Profile</span></span>

* <span data-ttu-id="336df-201">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="336df-201">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="336df-202">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="336df-202">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="336df-203">Redis</span><span class="sxs-lookup"><span data-stu-id="336df-203">Redis</span></span>

* <span data-ttu-id="336df-204">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="336df-204">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="336df-205">弃用“update-settings”命令。</span><span class="sxs-lookup"><span data-stu-id="336df-205">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="336df-206">资源</span><span class="sxs-lookup"><span data-stu-id="336df-206">Resource</span></span>

* <span data-ttu-id="336df-207">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="336df-207">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="336df-208">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="336df-208">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="336df-209">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="336df-209">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="336df-210">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="336df-210">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="336df-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="336df-211">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="336df-212">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="336df-212">Add docs for az lock update.</span></span> <span data-ttu-id="336df-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="336df-213">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="336df-214">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="336df-214">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="336df-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="336df-215">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="336df-216">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="336df-216">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="336df-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="336df-217">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="336df-218">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="336df-218">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="336df-219">角色</span><span class="sxs-lookup"><span data-stu-id="336df-219">Role</span></span>

* <span data-ttu-id="336df-220">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="336df-220">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="336df-221">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="336df-221">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="336df-222">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="336df-222">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="336df-223">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="336df-223">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="336df-224">SQL</span><span class="sxs-lookup"><span data-stu-id="336df-224">SQL</span></span>

* <span data-ttu-id="336df-225">添加了 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="336df-225">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="336df-226">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="336df-226">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="336df-227">存储</span><span class="sxs-lookup"><span data-stu-id="336df-227">Storage</span></span>

* <span data-ttu-id="336df-228">位置默认为 `storage account create` 的资源组位置。</span><span class="sxs-lookup"><span data-stu-id="336df-228">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="336df-229">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="336df-229">Add support for incremental blob copy</span></span>
* <span data-ttu-id="336df-230">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="336df-230">Add support for large block blob upload</span></span>
* <span data-ttu-id="336df-231">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="336df-231">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="336df-232">VM</span><span class="sxs-lookup"><span data-stu-id="336df-232">VM</span></span>

* <span data-ttu-id="336df-233">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="336df-233">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="336df-234">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="336df-234">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="336df-235">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="336df-235">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="336df-236">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="336df-236">az vm/vmss disk</span></span>
  3. <span data-ttu-id="336df-237">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="336df-237">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="336df-238">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="336df-238">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="336df-239">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="336df-239">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="336df-240">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="336df-240">April 3, 2017</span></span>

<span data-ttu-id="336df-241">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="336df-241">Version 2.0.2</span></span>

<span data-ttu-id="336df-242">此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。</span><span class="sxs-lookup"><span data-stu-id="336df-242">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="336df-243">核心</span><span class="sxs-lookup"><span data-stu-id="336df-243">Core</span></span>

* <span data-ttu-id="336df-244">在默认列表中添加了 acr、实验室、监视和查找模块。</span><span class="sxs-lookup"><span data-stu-id="336df-244">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="336df-245">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="336df-245">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="336df-246">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="336df-246">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="336df-247">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="336df-247">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="336df-248">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="336df-248">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="336df-249">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="336df-249">Add prompting for missing template parameters.</span></span> <span data-ttu-id="336df-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="336df-250">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="336df-251">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="336df-251">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="336df-252">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="336df-252">Support login to specific tenant</span></span>
 
### <a name="acs"></a><span data-ttu-id="336df-253">ACS</span><span class="sxs-lookup"><span data-stu-id="336df-253">ACS</span></span>

* [<span data-ttu-id="336df-254">ACS] 添加了配置默认 ACS 群集的支持 ([#2554</span><span class="sxs-lookup"><span data-stu-id="336df-254">ACS] Adding support for configuring a default ACS cluster ([#2554</span></span>](https://github.com/Azure/azure-cli/pull/2554))
* <span data-ttu-id="336df-255">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-255">Add support for ssh key password prompting.</span></span> <span data-ttu-id="336df-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="336df-256">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="336df-257">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-257">Add support for windows clusters.</span></span> <span data-ttu-id="336df-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="336df-258">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="336df-259">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="336df-259">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="336df-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="336df-260">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>
 
### <a name="appservice"></a><span data-ttu-id="336df-261">应用服务</span><span class="sxs-lookup"><span data-stu-id="336df-261">AppService</span></span>

* <span data-ttu-id="336df-262">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="336df-262">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="336df-263">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="336df-263">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="336df-264">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="336df-264">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="336df-265">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="336df-265">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>
 
### <a name="datalake"></a><span data-ttu-id="336df-266">DataLake</span><span class="sxs-lookup"><span data-stu-id="336df-266">DataLake</span></span>

* <span data-ttu-id="336df-267">Data Lake Analytics 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="336df-267">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="336df-268">Data Lake Store 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="336df-268">Initial release of Data Lake Store module.</span></span>
 
### <a name="docuemntdb"></a><span data-ttu-id="336df-269">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="336df-269">DocuemntDB</span></span>

* <span data-ttu-id="336df-270">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="336df-270">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="336df-271">VM</span><span class="sxs-lookup"><span data-stu-id="336df-271">VM</span></span>

* [<span data-ttu-id="336df-272">计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570</span><span class="sxs-lookup"><span data-stu-id="336df-272">Compute] Add AppGateway support to virtual machine scale set create ([#2570</span></span>](https://github.com/Azure/azure-cli/pull/2570))
* [<span data-ttu-id="336df-273">VM/VMSS] 改进了磁盘缓存支持 ([#2522</span><span class="sxs-lookup"><span data-stu-id="336df-273">VM/VMSS] Improved disk caching support ([#2522</span></span>](https://github.com/Azure/azure-cli/pull/2522))
* <span data-ttu-id="336df-274">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="336df-274">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="336df-275">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="336df-275">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="336df-276">虚拟机规模集：支持使用 * 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="336df-276">Virtual machine scale set: support * to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="336df-277">添加了适用于 VM 和虚拟机规模集的 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="336df-277">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="336df-278">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="336df-278">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="336df-279">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="336df-279">February 27, 2017</span></span>

<span data-ttu-id="336df-280">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="336df-280">Version 2.0.0</span></span>

<span data-ttu-id="336df-281">此版 Azure CLI 2.0 是第一个“正式版”。</span><span class="sxs-lookup"><span data-stu-id="336df-281">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="336df-282">正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="336df-282">General availability applies to these command modules:</span></span>
- <span data-ttu-id="336df-283">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="336df-283">Container Service (acs)</span></span>
- <span data-ttu-id="336df-284">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="336df-284">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="336df-285">网络</span><span class="sxs-lookup"><span data-stu-id="336df-285">Networking</span></span>
- <span data-ttu-id="336df-286">存储</span><span class="sxs-lookup"><span data-stu-id="336df-286">Storage</span></span>

<span data-ttu-id="336df-287">这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。</span><span class="sxs-lookup"><span data-stu-id="336df-287">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="336df-288">可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。</span><span class="sxs-lookup"><span data-stu-id="336df-288">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="336df-289">可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。</span><span class="sxs-lookup"><span data-stu-id="336df-289">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
<span data-ttu-id="336df-290">可以通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="336df-290">You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="336df-291">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="336df-291">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="336df-292">若要检查 CLI 版本，请使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="336df-292">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="336df-293">输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="336df-293">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="336df-294">某些命令模块带有“bn”或“rcn”后缀。</span><span class="sxs-lookup"><span data-stu-id="336df-294">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="336df-295">这些命令模块仍以预览版提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="336df-295">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="336df-296">此外，我们还提供 CLI 夜间预览版。</span><span class="sxs-lookup"><span data-stu-id="336df-296">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="336df-297">有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="336df-297">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="336df-298">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="336df-298">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="336df-299">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="336df-299">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="336df-300">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。</span><span class="sxs-lookup"><span data-stu-id="336df-300">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="336df-301">请通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="336df-301">Provide feedback from the command line with the `az feedback` command.</span></span>

