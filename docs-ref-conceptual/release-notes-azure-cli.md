---
title: "Azure CLI 2.0 发行说明"
description: "了解 Azure CLI 2.0 的最新更新"
keywords: "Azure CLI 2.0, 发行说明"
author: sptramer
ms.author: sttramer
manager: routlaw
ms.date: 01/17/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 86babea3030ea932de1858a391014e5d0bba7f73
ms.sourcegitcommit: cae66f994cb7b7f829f75ac528093fdb6851f64e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 01/29/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="9262b-104">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="9262b-104">Azure CLI 2.0 release notes</span></span>

## <a name="january-17-2018"></a><span data-ttu-id="9262b-105">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="9262b-105">January 17, 2018</span></span>

<span data-ttu-id="9262b-106">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="9262b-106">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="9262b-107">ACR</span><span class="sxs-lookup"><span data-stu-id="9262b-107">ACR</span></span>

* <span data-ttu-id="9262b-108">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-108">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="9262b-109">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="9262b-109">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-110">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-110">ACS</span></span>

* <span data-ttu-id="9262b-111">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-111">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="9262b-112">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="9262b-112">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-113">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-113">Appservice</span></span>

* <span data-ttu-id="9262b-114">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-114">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="9262b-115">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="9262b-115">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="9262b-116">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="9262b-116">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="9262b-117">备份</span><span class="sxs-lookup"><span data-stu-id="9262b-117">Backup</span></span>

* <span data-ttu-id="9262b-118">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="9262b-118">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="9262b-119">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="9262b-119">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="9262b-120">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="9262b-120">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="9262b-121">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-121">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="9262b-122">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="9262b-122">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="9262b-123">Batch</span><span class="sxs-lookup"><span data-stu-id="9262b-123">Batch</span></span>

* <span data-ttu-id="9262b-124">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="9262b-124">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="9262b-125">云</span><span class="sxs-lookup"><span data-stu-id="9262b-125">Cloud</span></span>

* <span data-ttu-id="9262b-126">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="9262b-126">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="9262b-127">消耗</span><span class="sxs-lookup"><span data-stu-id="9262b-127">Consumption</span></span>

* <span data-ttu-id="9262b-128">添加了用于保留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="9262b-128">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="9262b-129">事件网格</span><span class="sxs-lookup"><span data-stu-id="9262b-129">Event Grid</span></span>

* <span data-ttu-id="9262b-130">[重大更改] 已将 `az eventgrid topic event-subscription` 命令移至 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="9262b-130">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="9262b-131">[重大更改] 已将 `az eventgrid resource event-subscription` 命令移至 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="9262b-131">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="9262b-132">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-132">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="9262b-133">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="9262b-133">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="9262b-134">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="9262b-134">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="9262b-135">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="9262b-135">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="9262b-136">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-136">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="9262b-137">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="9262b-137">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="9262b-138">交互</span><span class="sxs-lookup"><span data-stu-id="9262b-138">Interactive</span></span>

* <span data-ttu-id="9262b-139">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-139">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="9262b-140">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-140">Fixed errors on startup</span></span>
* <span data-ttu-id="9262b-141">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-141">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="9262b-142">IoT</span><span class="sxs-lookup"><span data-stu-id="9262b-142">IoT</span></span>

* <span data-ttu-id="9262b-143">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-143">Added support for device provisioning service</span></span>
* <span data-ttu-id="9262b-144">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="9262b-144">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="9262b-145">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="9262b-145">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="9262b-146">监视</span><span class="sxs-lookup"><span data-stu-id="9262b-146">Monitor</span></span>

* <span data-ttu-id="9262b-147">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-147">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="9262b-148">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="9262b-148">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="9262b-149">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="9262b-149">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span> 

### <a name="network"></a><span data-ttu-id="9262b-150">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-150">Network</span></span>

* <span data-ttu-id="9262b-151">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-151">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="9262b-152">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-152">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="9262b-153">配置文件</span><span class="sxs-lookup"><span data-stu-id="9262b-153">Profile</span></span>

* <span data-ttu-id="9262b-154">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-154">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="9262b-155">角色</span><span class="sxs-lookup"><span data-stu-id="9262b-155">Role</span></span>

* <span data-ttu-id="9262b-156">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="9262b-156">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="9262b-157">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9262b-157">Service Fabric</span></span>

* <span data-ttu-id="9262b-158">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="9262b-158">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="9262b-159">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="9262b-159">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-160">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-160">VM</span></span>

* <span data-ttu-id="9262b-161">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="9262b-161">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="9262b-162">[重大更改] 已将单区域 `vmss` 默认值更改为“标准”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="9262b-162">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="9262b-163">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="9262b-163">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="9262b-164">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="9262b-164">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="9262b-165">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-165">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="9262b-166">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-166">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="9262b-167">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="9262b-167">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="9262b-168">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-168">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="9262b-169">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="9262b-169">December 19, 2017</span></span>

<span data-ttu-id="9262b-170">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="9262b-170">Version 2.0.23</span></span>

* <span data-ttu-id="9262b-171">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-171">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="9262b-172">容器</span><span class="sxs-lookup"><span data-stu-id="9262b-172">Container</span></span>

* <span data-ttu-id="9262b-173">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="9262b-173">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="9262b-174">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-174">Network</span></span>

* <span data-ttu-id="9262b-175">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-175">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="9262b-176">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-176">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-177">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-177">Storage</span></span>

* <span data-ttu-id="9262b-178">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-178">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-179">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-179">VM</span></span>

* <span data-ttu-id="9262b-180">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-180">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="9262b-181">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="9262b-181">December 5, 2017</span></span>

<span data-ttu-id="9262b-182">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="9262b-182">Version 2.0.22</span></span>

* <span data-ttu-id="9262b-183">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-183">Removed `az component` commands.</span></span> <span data-ttu-id="9262b-184">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="9262b-184">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="9262b-185">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-185">Core</span></span>
* <span data-ttu-id="9262b-186">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="9262b-186">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="9262b-187">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-187">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-188">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-188">ACS</span></span>

* <span data-ttu-id="9262b-189">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-189">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="9262b-190">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="9262b-190">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="9262b-191">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="9262b-191">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="9262b-192">顾问</span><span class="sxs-lookup"><span data-stu-id="9262b-192">Advisor</span></span>

* <span data-ttu-id="9262b-193">初始版本</span><span class="sxs-lookup"><span data-stu-id="9262b-193">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-194">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-194">Appservice</span></span>

* <span data-ttu-id="9262b-195">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="9262b-195">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="9262b-196">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="9262b-196">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="9262b-197">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="9262b-197">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="9262b-198">消耗</span><span class="sxs-lookup"><span data-stu-id="9262b-198">Consumption</span></span>

* <span data-ttu-id="9262b-199">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-199">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="9262b-200">容器</span><span class="sxs-lookup"><span data-stu-id="9262b-200">Container</span></span>

* <span data-ttu-id="9262b-201">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="9262b-201">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="9262b-202">监视</span><span class="sxs-lookup"><span data-stu-id="9262b-202">Monitor</span></span>

* <span data-ttu-id="9262b-203">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="9262b-203">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-204">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-204">Resource</span></span>

* <span data-ttu-id="9262b-205">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-205">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="9262b-206">角色</span><span class="sxs-lookup"><span data-stu-id="9262b-206">Role</span></span>

* <span data-ttu-id="9262b-207">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="9262b-207">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="9262b-208">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="9262b-208">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="9262b-209">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="9262b-209">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-210">SQL</span><span class="sxs-lookup"><span data-stu-id="9262b-210">SQL</span></span>

* <span data-ttu-id="9262b-211">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-211">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="9262b-212">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-212">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-213">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-213">VM</span></span>

* <span data-ttu-id="9262b-214">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="9262b-214">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="9262b-215">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="9262b-215">November 14, 2017</span></span>

<span data-ttu-id="9262b-216">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="9262b-216">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="9262b-217">ACR</span><span class="sxs-lookup"><span data-stu-id="9262b-217">ACR</span></span>

* <span data-ttu-id="9262b-218">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-218">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="9262b-219">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-219">ACS</span></span>

* <span data-ttu-id="9262b-220">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="9262b-220">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="9262b-221">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="9262b-221">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="9262b-222">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="9262b-222">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="9262b-223">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="9262b-223">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="9262b-224">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="9262b-224">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-225">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-225">Appservice</span></span>

* <span data-ttu-id="9262b-226">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="9262b-226">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="9262b-227">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="9262b-227">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="9262b-228">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="9262b-228">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="9262b-229">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="9262b-229">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="9262b-230">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-230">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="9262b-231">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="9262b-231">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="9262b-232">Batch</span><span class="sxs-lookup"><span data-stu-id="9262b-232">Batch</span></span>

* <span data-ttu-id="9262b-233">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-233">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="9262b-234">Batchai</span><span class="sxs-lookup"><span data-stu-id="9262b-234">Batchai</span></span>

* <span data-ttu-id="9262b-235">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="9262b-235">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="9262b-236">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="9262b-236">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="9262b-237">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="9262b-237">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="9262b-238">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="9262b-238">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="9262b-239">云</span><span class="sxs-lookup"><span data-stu-id="9262b-239">Cloud</span></span>

* <span data-ttu-id="9262b-240">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="9262b-240">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="9262b-241">容器</span><span class="sxs-lookup"><span data-stu-id="9262b-241">Container</span></span>

* <span data-ttu-id="9262b-242">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-242">Added support to open multiple ports</span></span>
* <span data-ttu-id="9262b-243">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="9262b-243">Added container group restart policy</span></span>
* <span data-ttu-id="9262b-244">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-244">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="9262b-245">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="9262b-245">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="9262b-246">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="9262b-246">Data Lake Analytics</span></span>

* <span data-ttu-id="9262b-247">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="9262b-247">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="9262b-248">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9262b-248">Data Lake Store</span></span>

* <span data-ttu-id="9262b-249">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="9262b-249">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="9262b-250">分机</span><span class="sxs-lookup"><span data-stu-id="9262b-250">Extension</span></span>

* <span data-ttu-id="9262b-251">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="9262b-251">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="9262b-252">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="9262b-252">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="9262b-253">IoT</span><span class="sxs-lookup"><span data-stu-id="9262b-253">IoT</span></span>

* <span data-ttu-id="9262b-254">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-254">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="9262b-255">监视</span><span class="sxs-lookup"><span data-stu-id="9262b-255">Monitor</span></span>

* <span data-ttu-id="9262b-256">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-256">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="9262b-257">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-257">Network</span></span>

* <span data-ttu-id="9262b-258">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-258">Added support for CAA DNS records</span></span>
* <span data-ttu-id="9262b-259">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-259">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="9262b-260">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-260">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="9262b-261">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-261">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="9262b-262">保留</span><span class="sxs-lookup"><span data-stu-id="9262b-262">Reservations</span></span>

* <span data-ttu-id="9262b-263">初始预览版</span><span class="sxs-lookup"><span data-stu-id="9262b-263">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-264">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-264">Resource</span></span>

* <span data-ttu-id="9262b-265">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-265">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-266">SQL</span><span class="sxs-lookup"><span data-stu-id="9262b-266">SQL</span></span>

* <span data-ttu-id="9262b-267">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-267">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-268">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-268">Storage</span></span>

* <span data-ttu-id="9262b-269">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="9262b-269">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="9262b-270">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-270">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="9262b-271">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-271">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="9262b-272">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="9262b-272">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="9262b-273">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-273">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="9262b-274">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-274">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="9262b-275">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-275">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-276">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-276">VM</span></span>

* <span data-ttu-id="9262b-277">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-277">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="9262b-278">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-278">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="9262b-279">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-279">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="9262b-280">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="9262b-280">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="9262b-281">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-281">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="9262b-282">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="9262b-282">October 24, 2017</span></span>

<span data-ttu-id="9262b-283">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="9262b-283">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="9262b-284">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-284">Core</span></span>

* <span data-ttu-id="9262b-285">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="9262b-285">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="9262b-286">ACR</span><span class="sxs-lookup"><span data-stu-id="9262b-286">ACR</span></span>

* <span data-ttu-id="9262b-287">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="9262b-287">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="9262b-288">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="9262b-288">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="9262b-289">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="9262b-289">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-290">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-290">ACS</span></span>

* <span data-ttu-id="9262b-291">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-291">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="9262b-292">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="9262b-292">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-293">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-293">Appservice</span></span>

* <span data-ttu-id="9262b-294">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-294">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="9262b-295">组件</span><span class="sxs-lookup"><span data-stu-id="9262b-295">Component</span></span>

* <span data-ttu-id="9262b-296">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="9262b-296">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="9262b-297">监视</span><span class="sxs-lookup"><span data-stu-id="9262b-297">Monitor</span></span>

* <span data-ttu-id="9262b-298">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-298">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-299">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-299">Resource</span></span>

* <span data-ttu-id="9262b-300">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-300">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="9262b-301">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="9262b-301">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-302">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-302">VM</span></span>

* <span data-ttu-id="9262b-303">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-303">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="9262b-304">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="9262b-304">October 9, 2017</span></span>

<span data-ttu-id="9262b-305">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="9262b-305">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="9262b-306">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-306">Core</span></span>

* <span data-ttu-id="9262b-307">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="9262b-307">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-308">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-308">Appservice</span></span>

* <span data-ttu-id="9262b-309">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="9262b-309">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="9262b-310">Batch</span><span class="sxs-lookup"><span data-stu-id="9262b-310">Batch</span></span>

* <span data-ttu-id="9262b-311">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="9262b-311">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="9262b-312">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="9262b-312">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="9262b-313">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-313">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="9262b-314">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="9262b-314">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="9262b-315">Batchai</span><span class="sxs-lookup"><span data-stu-id="9262b-315">Batchai</span></span>

* <span data-ttu-id="9262b-316">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="9262b-316">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="9262b-317">KeyVault</span><span class="sxs-lookup"><span data-stu-id="9262b-317">Keyvault</span></span>

* <span data-ttu-id="9262b-318">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="9262b-318">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="9262b-319">(#4448)</span><span class="sxs-lookup"><span data-stu-id="9262b-319">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="9262b-320">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-320">Network</span></span>

* <span data-ttu-id="9262b-321">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="9262b-321">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="9262b-322">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="9262b-322">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-323">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-323">Resource</span></span>

* <span data-ttu-id="9262b-324">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-324">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="9262b-325">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="9262b-325">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="9262b-326">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="9262b-326">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="9262b-327">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="9262b-327">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-328">Sql</span><span class="sxs-lookup"><span data-stu-id="9262b-328">Sql</span></span>

* <span data-ttu-id="9262b-329">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-329">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="9262b-330">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="9262b-330">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="9262b-331">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="9262b-331">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-332">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-332">Storage</span></span>

* <span data-ttu-id="9262b-333">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-333">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-334">Vm</span><span class="sxs-lookup"><span data-stu-id="9262b-334">Vm</span></span>

* <span data-ttu-id="9262b-335">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="9262b-335">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="9262b-336">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-336">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="9262b-337">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-337">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="9262b-338">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-338">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="9262b-339">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-339">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="9262b-340">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="9262b-340">September 22, 2017</span></span>

<span data-ttu-id="9262b-341">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="9262b-341">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-342">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-342">Resource</span></span>

* <span data-ttu-id="9262b-343">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-343">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="9262b-344">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="9262b-344">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="9262b-345">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-345">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="9262b-346">[重大更改] 将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="9262b-346">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="9262b-347">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-347">Network</span></span>

* <span data-ttu-id="9262b-348">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-348">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="9262b-349">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-349">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="9262b-350">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="9262b-350">Added `asg` application security group commands</span></span>
* <span data-ttu-id="9262b-351">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-351">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="9262b-352">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-352">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="9262b-353">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-353">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="9262b-354">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-354">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-355">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-355">Storage</span></span>

* <span data-ttu-id="9262b-356">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-356">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="9262b-357">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="9262b-357">Eventgrid</span></span>

* <span data-ttu-id="9262b-358">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="9262b-358">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-359">SQL</span><span class="sxs-lookup"><span data-stu-id="9262b-359">SQL</span></span>

* <span data-ttu-id="9262b-360">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="9262b-360">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="9262b-361">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="9262b-361">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="9262b-362">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-362">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="9262b-363">KeyVault</span><span class="sxs-lookup"><span data-stu-id="9262b-363">Keyvault</span></span>

* <span data-ttu-id="9262b-364">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-364">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-365">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-365">VM</span></span>

* <span data-ttu-id="9262b-366">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-366">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="9262b-367">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-367">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="9262b-368">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-368">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="9262b-369">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-369">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="9262b-370">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-370">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="9262b-371">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-371">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-372">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-372">ACS</span></span>

* <span data-ttu-id="9262b-373">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-373">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-374">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-374">Appservice</span></span>

* <span data-ttu-id="9262b-375">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-375">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="9262b-376">备份</span><span class="sxs-lookup"><span data-stu-id="9262b-376">Backup</span></span>

* <span data-ttu-id="9262b-377">预览版</span><span class="sxs-lookup"><span data-stu-id="9262b-377">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="9262b-378">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="9262b-378">September 11, 2017</span></span>

<span data-ttu-id="9262b-379">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="9262b-379">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="9262b-380">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-380">Core</span></span>

* <span data-ttu-id="9262b-381">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="9262b-381">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="9262b-382">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="9262b-382">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-383">Acs</span><span class="sxs-lookup"><span data-stu-id="9262b-383">Acs</span></span>

* <span data-ttu-id="9262b-384">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-384">Added `acs list-locations` command</span></span>
* <span data-ttu-id="9262b-385">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="9262b-385">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-386">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-386">Appservice</span></span>

* <span data-ttu-id="9262b-387">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-387">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="9262b-388">CDN</span><span class="sxs-lookup"><span data-stu-id="9262b-388">CDN</span></span>

* <span data-ttu-id="9262b-389">修复了 `cdn custom-domain create` 的“CustomDomain 不可迭代” bug。</span><span class="sxs-lookup"><span data-stu-id="9262b-389">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="9262b-390">分机</span><span class="sxs-lookup"><span data-stu-id="9262b-390">Extension</span></span>

* <span data-ttu-id="9262b-391">初始版本。</span><span class="sxs-lookup"><span data-stu-id="9262b-391">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="9262b-392">KeyVault</span><span class="sxs-lookup"><span data-stu-id="9262b-392">Keyvault</span></span>

* <span data-ttu-id="9262b-393">修复了 `keyvault set-policy` 的权限区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="9262b-393">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="9262b-394">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-394">Network</span></span>

* <span data-ttu-id="9262b-395">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="9262b-395">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="9262b-396">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="9262b-396">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="9262b-397">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-397">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="9262b-398">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-398">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="9262b-399">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-399">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-400">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-400">Resource</span></span>

* <span data-ttu-id="9262b-401">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="9262b-401">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="9262b-402">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="9262b-402">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="9262b-403">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="9262b-403">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="9262b-404">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="9262b-404">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-405">SQL</span><span class="sxs-lookup"><span data-stu-id="9262b-405">SQL</span></span>

* <span data-ttu-id="9262b-406">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-406">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-407">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-407">VM</span></span>

* <span data-ttu-id="9262b-408">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="9262b-408">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="9262b-409">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="9262b-409">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="9262b-410">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="9262b-410">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="9262b-411">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="9262b-411">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="9262b-412">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="9262b-412">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="9262b-413">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="9262b-413">August 31, 2017</span></span>

<span data-ttu-id="9262b-414">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="9262b-414">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="9262b-415">KeyVault</span><span class="sxs-lookup"><span data-stu-id="9262b-415">Keyvault</span></span>

* <span data-ttu-id="9262b-416">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-416">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="9262b-417">Sf</span><span class="sxs-lookup"><span data-stu-id="9262b-417">Sf</span></span>

* <span data-ttu-id="9262b-418">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="9262b-418">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-419">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-419">Storage</span></span>

* <span data-ttu-id="9262b-420">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-420">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="9262b-421">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="9262b-421">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="9262b-422">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="9262b-422">August 28, 2017</span></span>

<span data-ttu-id="9262b-423">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="9262b-423">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="9262b-424">CLI</span><span class="sxs-lookup"><span data-stu-id="9262b-424">CLI</span></span>

* <span data-ttu-id="9262b-425">在 `--version` 中添加了法律说明。</span><span class="sxs-lookup"><span data-stu-id="9262b-425">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-426">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-426">ACS</span></span>

* <span data-ttu-id="9262b-427">更正了预览区域。</span><span class="sxs-lookup"><span data-stu-id="9262b-427">Corrected preview regions.</span></span>
* <span data-ttu-id="9262b-428">正确设置了默认 `dns_name_prefix` 的格式。</span><span class="sxs-lookup"><span data-stu-id="9262b-428">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="9262b-429">优化了 acs 命令输出。</span><span class="sxs-lookup"><span data-stu-id="9262b-429">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-430">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-430">Appservice</span></span>

* <span data-ttu-id="9262b-431">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致问题</span><span class="sxs-lookup"><span data-stu-id="9262b-431">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="9262b-432">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="9262b-432">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="9262b-433">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="9262b-433">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="9262b-434">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="9262b-434">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="9262b-435">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="9262b-435">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="9262b-436">IoT</span><span class="sxs-lookup"><span data-stu-id="9262b-436">IoT</span></span>

* <span data-ttu-id="9262b-437">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="9262b-437">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="9262b-438">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-438">Network</span></span>

* <span data-ttu-id="9262b-439">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="9262b-439">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="9262b-440">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="9262b-440">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="9262b-441">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-441">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="9262b-442">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-442">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="9262b-443">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-443">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="9262b-444">配置文件</span><span class="sxs-lookup"><span data-stu-id="9262b-444">Profile</span></span>

* <span data-ttu-id="9262b-445">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="9262b-445">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="9262b-446">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9262b-446">Service Fabric</span></span>

* <span data-ttu-id="9262b-447">预览版</span><span class="sxs-lookup"><span data-stu-id="9262b-447">Preview release</span></span>
* <span data-ttu-id="9262b-448">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="9262b-448">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="9262b-449">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-449">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="9262b-450">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-450">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-451">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-451">Storage</span></span>

* <span data-ttu-id="9262b-452">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="9262b-452">Enabled setting blob tier</span></span>
* <span data-ttu-id="9262b-453">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="9262b-453">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="9262b-454">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="9262b-454">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="9262b-455">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-455">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="9262b-456">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="9262b-456">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="9262b-457">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="9262b-457">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-458">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-458">VM</span></span>

* <span data-ttu-id="9262b-459">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-459">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="9262b-460">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="9262b-460">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="9262b-461">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="9262b-461">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="9262b-462">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-462">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="9262b-463">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-463">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="9262b-464">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-464">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="9262b-465">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="9262b-465">August 15, 2017</span></span>

<span data-ttu-id="9262b-466">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="9262b-466">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-467">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-467">ACS</span></span>

* <span data-ttu-id="9262b-468">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="9262b-468">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-469">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-469">Appservice</span></span>

* <span data-ttu-id="9262b-470">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-470">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="9262b-471">事件网格</span><span class="sxs-lookup"><span data-stu-id="9262b-471">Event Grid</span></span>

* <span data-ttu-id="9262b-472">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="9262b-472">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="9262b-473">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="9262b-473">August 11, 2017</span></span>

<span data-ttu-id="9262b-474">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="9262b-474">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-475">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-475">ACS</span></span>

* <span data-ttu-id="9262b-476">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="9262b-476">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="9262b-477">Batch</span><span class="sxs-lookup"><span data-stu-id="9262b-477">Batch</span></span>

* <span data-ttu-id="9262b-478">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="9262b-478">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="9262b-479">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="9262b-479">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="9262b-480">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-480">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="9262b-481">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="9262b-481">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="9262b-482">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="9262b-482">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="9262b-483">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="9262b-483">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="9262b-484">组件</span><span class="sxs-lookup"><span data-stu-id="9262b-484">Component</span></span>

* <span data-ttu-id="9262b-485">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="9262b-485">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="9262b-486">容器</span><span class="sxs-lookup"><span data-stu-id="9262b-486">Container</span></span>

* <span data-ttu-id="9262b-487">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-487">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="9262b-488">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9262b-488">Data Lake Store</span></span>

* <span data-ttu-id="9262b-489">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="9262b-489">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="9262b-490">事件网格</span><span class="sxs-lookup"><span data-stu-id="9262b-490">Event Grid</span></span>

* <span data-ttu-id="9262b-491">初始版本</span><span class="sxs-lookup"><span data-stu-id="9262b-491">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="9262b-492">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-492">Network</span></span>

* <span data-ttu-id="9262b-493">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-493">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="9262b-494">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-494">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="9262b-495">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-495">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="9262b-496">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="9262b-496">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="9262b-497">配置文件</span><span class="sxs-lookup"><span data-stu-id="9262b-497">Profile</span></span>

* <span data-ttu-id="9262b-498">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="9262b-498">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-499">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-499">Storage</span></span>

* <span data-ttu-id="9262b-500">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-500">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-501">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-501">VM</span></span>

* <span data-ttu-id="9262b-502">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="9262b-502">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="9262b-503">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-503">Exposed `list-skus` command</span></span>
* <span data-ttu-id="9262b-504">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="9262b-504">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="9262b-505">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="9262b-505">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="9262b-506">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="9262b-506">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="9262b-507">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="9262b-507">July 28, 2017</span></span>

<span data-ttu-id="9262b-508">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="9262b-508">Version 2.0.12</span></span>

* <span data-ttu-id="9262b-509">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="9262b-509">Added container commands</span></span>
* <span data-ttu-id="9262b-510">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="9262b-510">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="9262b-511">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-511">Core</span></span>

* <span data-ttu-id="9262b-512">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="9262b-512">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="9262b-513">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="9262b-513">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="9262b-514">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="9262b-514">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="9262b-515">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="9262b-515">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="9262b-516">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="9262b-516">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="9262b-517">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="9262b-517">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="9262b-518">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="9262b-518">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="9262b-519">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="9262b-519">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="9262b-520">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="9262b-520">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="9262b-521">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="9262b-521">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="9262b-522">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="9262b-522">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="9262b-523">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="9262b-523">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="9262b-524">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="9262b-524">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="9262b-525">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="9262b-525">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="9262b-526">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="9262b-526">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="9262b-527">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="9262b-527">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="9262b-528">ACR</span><span class="sxs-lookup"><span data-stu-id="9262b-528">ACR</span></span>

* <span data-ttu-id="9262b-529">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-529">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="9262b-530">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="9262b-530">Support SKU update for managed registries</span></span>
* <span data-ttu-id="9262b-531">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="9262b-531">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="9262b-532">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="9262b-532">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="9262b-533">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-533">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="9262b-534">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-534">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-535">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-535">ACS</span></span>

* <span data-ttu-id="9262b-536">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-536">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-537">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-537">Appservice</span></span>

* <span data-ttu-id="9262b-538">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-538">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="9262b-539">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="9262b-539">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="9262b-540">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="9262b-540">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="9262b-541">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="9262b-541">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="9262b-542">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="9262b-542">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="9262b-543">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="9262b-543">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="9262b-544">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="9262b-544">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="9262b-545">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="9262b-545">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="9262b-546">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="9262b-546">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="9262b-547">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="9262b-547">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="9262b-548">Batch</span><span class="sxs-lookup"><span data-stu-id="9262b-548">Batch</span></span>

* <span data-ttu-id="9262b-549">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="9262b-549">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="9262b-550">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="9262b-550">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="9262b-551">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="9262b-551">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="9262b-552">CDN</span><span class="sxs-lookup"><span data-stu-id="9262b-552">CDN</span></span>

* <span data-ttu-id="9262b-553">当 `--profile-name` 指定的配置文件不存在时，针对 `cdn endpoint list` 提供更完善的错误消息。</span><span class="sxs-lookup"><span data-stu-id="9262b-553">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="9262b-554">云</span><span class="sxs-lookup"><span data-stu-id="9262b-554">Cloud</span></span>

* <span data-ttu-id="9262b-555">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="9262b-555">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="9262b-556">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="9262b-556">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="9262b-557">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="9262b-557">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="9262b-558">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="9262b-558">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="9262b-559">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="9262b-559">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="9262b-560">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9262b-560">CosmosDB</span></span>

* <span data-ttu-id="9262b-561">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-561">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="9262b-562">添加了对集合默认 TTL 的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-562">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="9262b-563">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="9262b-563">Data Lake Analytics</span></span>

* <span data-ttu-id="9262b-564">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="9262b-564">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="9262b-565">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="9262b-565">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="9262b-566">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="9262b-566">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="9262b-567">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9262b-567">Data Lake Store</span></span>

* <span data-ttu-id="9262b-568">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-568">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="9262b-569">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="9262b-569">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="9262b-570">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="9262b-570">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="9262b-571">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="9262b-571">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="9262b-572">交互</span><span class="sxs-lookup"><span data-stu-id="9262b-572">Interactive</span></span>

* <span data-ttu-id="9262b-573">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="9262b-573">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="9262b-574">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="9262b-574">Increased test coverage</span></span>
* <span data-ttu-id="9262b-575">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="9262b-575">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="9262b-576">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="9262b-576">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="9262b-577">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="9262b-577">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="9262b-578">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="9262b-578">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="9262b-579">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="9262b-579">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="9262b-580">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="9262b-580">Added `--progress` flag</span></span>
* <span data-ttu-id="9262b-581">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="9262b-581">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="9262b-582">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="9262b-582">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="9262b-583">IoT</span><span class="sxs-lookup"><span data-stu-id="9262b-583">IoT</span></span>

* <span data-ttu-id="9262b-584">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="9262b-584">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="9262b-585">(#3934)</span><span class="sxs-lookup"><span data-stu-id="9262b-585">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="9262b-586">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="9262b-586">Key vault</span></span>

* <span data-ttu-id="9262b-587">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="9262b-587">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="9262b-588">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="9262b-588">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="9262b-589">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="9262b-589">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="9262b-590">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="9262b-590">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="9262b-591">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="9262b-591">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="9262b-592">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="9262b-592">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="9262b-593">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="9262b-593">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="9262b-594">(#3307)</span><span class="sxs-lookup"><span data-stu-id="9262b-594">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="9262b-595">实验室</span><span class="sxs-lookup"><span data-stu-id="9262b-595">Lab</span></span>

* <span data-ttu-id="9262b-596">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-596">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="9262b-597">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="9262b-597">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="9262b-598">监视</span><span class="sxs-lookup"><span data-stu-id="9262b-598">Monitor</span></span>

* <span data-ttu-id="9262b-599">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="9262b-599">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="9262b-600">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="9262b-600">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="9262b-601">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="9262b-601">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="9262b-602">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="9262b-602">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="9262b-603">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="9262b-603">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="9262b-604">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="9262b-604">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="9262b-605">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="9262b-605">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="9262b-606">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="9262b-606">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="9262b-607">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="9262b-607">`location` no longer required</span></span>
  * <span data-ttu-id="9262b-608">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="9262b-608">Add name and ID support for target</span></span>
  * <span data-ttu-id="9262b-609">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="9262b-609">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="9262b-610">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="9262b-610">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="9262b-611">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="9262b-611">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="9262b-612">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="9262b-612">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="9262b-613">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="9262b-613">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="9262b-614">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="9262b-614">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="9262b-615">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-615">Network</span></span>

* <span data-ttu-id="9262b-616">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-616">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="9262b-617">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-617">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="9262b-618">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-618">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="9262b-619">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-619">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="9262b-620">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-620">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="9262b-621">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="9262b-621">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="9262b-622">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="9262b-622">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="9262b-623">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="9262b-623">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="9262b-624">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="9262b-624">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="9262b-625">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="9262b-625">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="9262b-626">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-626">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="9262b-627">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-627">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="9262b-628">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="9262b-628">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="9262b-629">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-629">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="9262b-630">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-630">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="9262b-631">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-631">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="9262b-632">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-632">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="9262b-633">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-633">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="9262b-634">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-634">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="9262b-635">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-635">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="9262b-636">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-636">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="9262b-637">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-637">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="9262b-638">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="9262b-638">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="9262b-639">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="9262b-639">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="9262b-640">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="9262b-640">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="9262b-641">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="9262b-641">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="9262b-642">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="9262b-642">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="9262b-643">配置文件</span><span class="sxs-lookup"><span data-stu-id="9262b-643">Profile</span></span>

* <span data-ttu-id="9262b-644">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="9262b-644">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="9262b-645">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="9262b-645">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="9262b-646">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="9262b-646">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="9262b-647">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="9262b-647">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="9262b-648">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="9262b-648">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="9262b-649">RDBMS</span><span class="sxs-lookup"><span data-stu-id="9262b-649">RDBMS</span></span>

* <span data-ttu-id="9262b-650">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="9262b-650">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="9262b-651">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="9262b-651">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="9262b-652">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="9262b-652">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="9262b-653">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="9262b-653">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-654">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-654">Resource</span></span>

* <span data-ttu-id="9262b-655">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="9262b-655">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="9262b-656">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="9262b-656">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="9262b-657">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="9262b-657">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="9262b-658">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-658">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="9262b-659">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="9262b-659">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="9262b-660">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="9262b-660">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="9262b-661">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="9262b-661">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="9262b-662">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-662">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="9262b-663">角色</span><span class="sxs-lookup"><span data-stu-id="9262b-663">Role</span></span>

* <span data-ttu-id="9262b-664">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="9262b-664">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="9262b-665">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="9262b-665">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="9262b-666">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="9262b-666">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="9262b-667">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="9262b-667">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="9262b-668">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="9262b-668">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="9262b-669">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="9262b-669">Service Fabric</span></span>
* <span data-ttu-id="9262b-670">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="9262b-670">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="9262b-671">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="9262b-671">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="9262b-672">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="9262b-672">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-673">SQL</span><span class="sxs-lookup"><span data-stu-id="9262b-673">SQL</span></span>

* <span data-ttu-id="9262b-674">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="9262b-674">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="9262b-675">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="9262b-675">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="9262b-676">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="9262b-676">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-677">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-677">Storage</span></span>

* <span data-ttu-id="9262b-678">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="9262b-678">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="9262b-679">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="9262b-679">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="9262b-680">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="9262b-680">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="9262b-681">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="9262b-681">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="9262b-682">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="9262b-682">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="9262b-683">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="9262b-683">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-684">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-684">VM</span></span>

* <span data-ttu-id="9262b-685">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="9262b-685">Support configuring nsg</span></span>
* <span data-ttu-id="9262b-686">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-686">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="9262b-687">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="9262b-687">Support managed service identities</span></span>
* <span data-ttu-id="9262b-688">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题。</span><span class="sxs-lookup"><span data-stu-id="9262b-688">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="9262b-689">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="9262b-689">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="9262b-690">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="9262b-690">May 10, 2017</span></span>

<span data-ttu-id="9262b-691">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="9262b-691">Version 2.0.6</span></span>

* <span data-ttu-id="9262b-692">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="9262b-692">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="9262b-693">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="9262b-693">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="9262b-694">包括 Data Lake Analytics 和 Data Lake Store 模块。</span><span class="sxs-lookup"><span data-stu-id="9262b-694">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="9262b-695">包括认知服务模块。</span><span class="sxs-lookup"><span data-stu-id="9262b-695">Include Cognitive Services module.</span></span>
* <span data-ttu-id="9262b-696">包括 Service Fabric 模块。</span><span class="sxs-lookup"><span data-stu-id="9262b-696">Include Service Fabric module.</span></span>
* <span data-ttu-id="9262b-697">包括交互式模块（重命名 az-shell）。</span><span class="sxs-lookup"><span data-stu-id="9262b-697">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="9262b-698">添加对 CDN 命令的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-698">Add support for CDN commands.</span></span>
* <span data-ttu-id="9262b-699">删除容器模块。</span><span class="sxs-lookup"><span data-stu-id="9262b-699">Remove Container module.</span></span>
* <span data-ttu-id="9262b-700">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="9262b-700">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="9262b-701">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="9262b-701">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="9262b-702">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-702">Core</span></span>

* <span data-ttu-id="9262b-703">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="9262b-703">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="9262b-704">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="9262b-704">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="9262b-705">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="9262b-705">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="9262b-706">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="9262b-706">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="9262b-707">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="9262b-707">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="9262b-708">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="9262b-708">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="9262b-709">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="9262b-709">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="9262b-710">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="9262b-710">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="9262b-711">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="9262b-711">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="9262b-712">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="9262b-712">core: Improved performance</span></span>
* <span data-ttu-id="9262b-713">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="9262b-713">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="9262b-714">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="9262b-714">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-715">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-715">ACS</span></span>

* <span data-ttu-id="9262b-716">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="9262b-716">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="9262b-717">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="9262b-717">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="9262b-718">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="9262b-718">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="9262b-719">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="9262b-719">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-720">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-720">AppService</span></span>

* <span data-ttu-id="9262b-721">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="9262b-721">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="9262b-722">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="9262b-722">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="9262b-723">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="9262b-723">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="9262b-724">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="9262b-724">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="9262b-725">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="9262b-725">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="9262b-726">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="9262b-726">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="9262b-727">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="9262b-727">support slot swap with preview</span></span>
* <span data-ttu-id="9262b-728">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="9262b-728">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="9262b-729">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="9262b-729">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="9262b-730">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="9262b-730">CosmosDB</span></span>

* <span data-ttu-id="9262b-731">将 DocumentDB 模块重命名为 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="9262b-731">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="9262b-732">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="9262b-732">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="9262b-733">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-733">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="9262b-734">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-734">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="9262b-735">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="9262b-735">Data Lake Analytics</span></span>

* <span data-ttu-id="9262b-736">Bug 修复：在筛选作业结果和状态列表时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="9262b-736">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="9262b-737">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="9262b-737">Add support for new catalog item type: package.</span></span> <span data-ttu-id="9262b-738">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="9262b-738">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="9262b-739">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="9262b-739">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="9262b-740">表</span><span class="sxs-lookup"><span data-stu-id="9262b-740">Table</span></span>
  * <span data-ttu-id="9262b-741">表值函数</span><span class="sxs-lookup"><span data-stu-id="9262b-741">Table valued function</span></span>
  * <span data-ttu-id="9262b-742">查看</span><span class="sxs-lookup"><span data-stu-id="9262b-742">View</span></span>
  * <span data-ttu-id="9262b-743">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="9262b-743">Table Statistics.</span></span> <span data-ttu-id="9262b-744">也可以使用架构列出，但无需指定表名。</span><span class="sxs-lookup"><span data-stu-id="9262b-744">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="9262b-745">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="9262b-745">Data Lake Store</span></span>

* <span data-ttu-id="9262b-746">更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。</span><span class="sxs-lookup"><span data-stu-id="9262b-746">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="9262b-747">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="9262b-747">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="9262b-748">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="9262b-748">missed help for access show.</span></span> <span data-ttu-id="9262b-749">正在添加。</span><span class="sxs-lookup"><span data-stu-id="9262b-749">adding it.</span></span> <span data-ttu-id="9262b-750">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="9262b-750">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="9262b-751">查找</span><span class="sxs-lookup"><span data-stu-id="9262b-751">Find</span></span>

* <span data-ttu-id="9262b-752">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="9262b-752">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="9262b-753">KeyVault</span><span class="sxs-lookup"><span data-stu-id="9262b-753">KeyVault</span></span>

* <span data-ttu-id="9262b-754">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="9262b-754">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="9262b-755">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。</span><span class="sxs-lookup"><span data-stu-id="9262b-755">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="9262b-756">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="9262b-756">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="9262b-757">解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。</span><span class="sxs-lookup"><span data-stu-id="9262b-757">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="9262b-758">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="9262b-758">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="9262b-759">实验室</span><span class="sxs-lookup"><span data-stu-id="9262b-759">Lab</span></span>

* <span data-ttu-id="9262b-760">针对实验室环境添加 create、show、delete 和 list 命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-760">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="9262b-761">添加 show 和 list 命令，查看实验室中的 ARM 模板。</span><span class="sxs-lookup"><span data-stu-id="9262b-761">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="9262b-762">在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。</span><span class="sxs-lookup"><span data-stu-id="9262b-762">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="9262b-763">添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。</span><span class="sxs-lookup"><span data-stu-id="9262b-763">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="9262b-764">添加命令，管理实验室中的机密。</span><span class="sxs-lookup"><span data-stu-id="9262b-764">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="9262b-765">监视</span><span class="sxs-lookup"><span data-stu-id="9262b-765">Monitor</span></span>

* <span data-ttu-id="9262b-766">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="9262b-766">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="9262b-767">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="9262b-767">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="9262b-768">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-768">Network</span></span>

* <span data-ttu-id="9262b-769">添加 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-769">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="9262b-770">添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-770">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="9262b-771">添加对应用程序网关连接排出的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-771">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="9262b-772">添加对应用程序网关 WAF 规则集配置的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-772">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="9262b-773">添加对 ExpressRoute 路由筛选器和规则的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-773">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="9262b-774">添加对 TrafficManager 地理路由的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-774">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="9262b-775">添加对基于 VPN 连接策略的流量选择器的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-775">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="9262b-776">添加对 VPN 连接 IPSec 策略的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-776">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="9262b-777">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。</span><span class="sxs-lookup"><span data-stu-id="9262b-777">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="9262b-778">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-778">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="9262b-779">从 `network vpn-connection list/show` 命令的输出中删除 null 值。</span><span class="sxs-lookup"><span data-stu-id="9262b-779">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="9262b-780">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="9262b-780">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="9262b-781">Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。</span><span class="sxs-lookup"><span data-stu-id="9262b-781">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="9262b-782">修复 `dns zone import` 中的 Bug：记录未正确导入。</span><span class="sxs-lookup"><span data-stu-id="9262b-782">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="9262b-783">Bug 修复：`traffic-manager endpoint update` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="9262b-783">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="9262b-784">添加“network watcher”预览命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-784">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="9262b-785">配置文件</span><span class="sxs-lookup"><span data-stu-id="9262b-785">Profile</span></span>

* <span data-ttu-id="9262b-786">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="9262b-786">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="9262b-787">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="9262b-787">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="9262b-788">Redis</span><span class="sxs-lookup"><span data-stu-id="9262b-788">Redis</span></span>

* <span data-ttu-id="9262b-789">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="9262b-789">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="9262b-790">弃用“update-settings”命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-790">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="9262b-791">资源</span><span class="sxs-lookup"><span data-stu-id="9262b-791">Resource</span></span>

* <span data-ttu-id="9262b-792">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="9262b-792">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="9262b-793">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="9262b-793">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="9262b-794">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="9262b-794">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="9262b-795">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="9262b-795">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="9262b-796">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="9262b-796">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="9262b-797">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="9262b-797">Add docs for az lock update.</span></span> <span data-ttu-id="9262b-798">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="9262b-798">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="9262b-799">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="9262b-799">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="9262b-800">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="9262b-800">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="9262b-801">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="9262b-801">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="9262b-802">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="9262b-802">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="9262b-803">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="9262b-803">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="9262b-804">角色</span><span class="sxs-lookup"><span data-stu-id="9262b-804">Role</span></span>

* <span data-ttu-id="9262b-805">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="9262b-805">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="9262b-806">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="9262b-806">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="9262b-807">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="9262b-807">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="9262b-808">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="9262b-808">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="9262b-809">SQL</span><span class="sxs-lookup"><span data-stu-id="9262b-809">SQL</span></span>

* <span data-ttu-id="9262b-810">添加了 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="9262b-810">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="9262b-811">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="9262b-811">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="9262b-812">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-812">Storage</span></span>

* <span data-ttu-id="9262b-813">位置默认为 `storage account create` 的资源组位置。</span><span class="sxs-lookup"><span data-stu-id="9262b-813">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="9262b-814">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-814">Add support for incremental blob copy</span></span>
* <span data-ttu-id="9262b-815">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="9262b-815">Add support for large block blob upload</span></span>
* <span data-ttu-id="9262b-816">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="9262b-816">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-817">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-817">VM</span></span>

* <span data-ttu-id="9262b-818">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="9262b-818">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="9262b-819">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="9262b-819">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="9262b-820">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="9262b-820">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="9262b-821">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="9262b-821">az vm/vmss disk</span></span>
  3. <span data-ttu-id="9262b-822">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="9262b-822">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="9262b-823">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="9262b-823">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="9262b-824">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="9262b-824">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="9262b-825">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="9262b-825">April 3, 2017</span></span>

<span data-ttu-id="9262b-826">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="9262b-826">Version 2.0.2</span></span>

<span data-ttu-id="9262b-827">此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。</span><span class="sxs-lookup"><span data-stu-id="9262b-827">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="9262b-828">核心</span><span class="sxs-lookup"><span data-stu-id="9262b-828">Core</span></span>

* <span data-ttu-id="9262b-829">在默认列表中添加了 acr、实验室、监视和查找模块。</span><span class="sxs-lookup"><span data-stu-id="9262b-829">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="9262b-830">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="9262b-830">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="9262b-831">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="9262b-831">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="9262b-832">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="9262b-832">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="9262b-833">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="9262b-833">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="9262b-834">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="9262b-834">Add prompting for missing template parameters.</span></span> <span data-ttu-id="9262b-835">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="9262b-835">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="9262b-836">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="9262b-836">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="9262b-837">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="9262b-837">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="9262b-838">ACS</span><span class="sxs-lookup"><span data-stu-id="9262b-838">ACS</span></span>

* <span data-ttu-id="9262b-839">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="9262b-839">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="9262b-840">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-840">Add support for ssh key password prompting.</span></span> <span data-ttu-id="9262b-841">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="9262b-841">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="9262b-842">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-842">Add support for windows clusters.</span></span> <span data-ttu-id="9262b-843">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="9262b-843">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="9262b-844">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="9262b-844">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="9262b-845">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="9262b-845">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="9262b-846">应用服务</span><span class="sxs-lookup"><span data-stu-id="9262b-846">AppService</span></span>

* <span data-ttu-id="9262b-847">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="9262b-847">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="9262b-848">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="9262b-848">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="9262b-849">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="9262b-849">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="9262b-850">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="9262b-850">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="9262b-851">DataLake</span><span class="sxs-lookup"><span data-stu-id="9262b-851">DataLake</span></span>

* <span data-ttu-id="9262b-852">Data Lake Analytics 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="9262b-852">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="9262b-853">Data Lake Store 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="9262b-853">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="9262b-854">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="9262b-854">DocuemntDB</span></span>

* <span data-ttu-id="9262b-855">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="9262b-855">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="9262b-856">VM</span><span class="sxs-lookup"><span data-stu-id="9262b-856">VM</span></span>

* <span data-ttu-id="9262b-857">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="9262b-857">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="9262b-858">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="9262b-858">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="9262b-859">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="9262b-859">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="9262b-860">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="9262b-860">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="9262b-861">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="9262b-861">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="9262b-862">添加了适用于 VM 和虚拟机规模集的 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="9262b-862">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="9262b-863">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="9262b-863">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="9262b-864">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="9262b-864">February 27, 2017</span></span>

<span data-ttu-id="9262b-865">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="9262b-865">Version 2.0.0</span></span>

<span data-ttu-id="9262b-866">此版 Azure CLI 2.0 是第一个“正式版”。</span><span class="sxs-lookup"><span data-stu-id="9262b-866">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="9262b-867">正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="9262b-867">General availability applies to these command modules:</span></span>
- <span data-ttu-id="9262b-868">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="9262b-868">Container Service (acs)</span></span>
- <span data-ttu-id="9262b-869">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="9262b-869">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="9262b-870">网络</span><span class="sxs-lookup"><span data-stu-id="9262b-870">Networking</span></span>
- <span data-ttu-id="9262b-871">存储</span><span class="sxs-lookup"><span data-stu-id="9262b-871">Storage</span></span>

<span data-ttu-id="9262b-872">这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。</span><span class="sxs-lookup"><span data-stu-id="9262b-872">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="9262b-873">可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。</span><span class="sxs-lookup"><span data-stu-id="9262b-873">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="9262b-874">可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。可以通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="9262b-874">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="9262b-875">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="9262b-875">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="9262b-876">若要检查 CLI 版本，请使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="9262b-876">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="9262b-877">输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="9262b-877">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="9262b-878">某些命令模块带有“bn”或“rcn”后缀。</span><span class="sxs-lookup"><span data-stu-id="9262b-878">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="9262b-879">这些命令模块仍以预览版提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="9262b-879">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="9262b-880">此外，我们还提供 CLI 夜间预览版。</span><span class="sxs-lookup"><span data-stu-id="9262b-880">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="9262b-881">有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="9262b-881">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="9262b-882">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="9262b-882">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="9262b-883">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="9262b-883">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="9262b-884">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。</span><span class="sxs-lookup"><span data-stu-id="9262b-884">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="9262b-885">请通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="9262b-885">Provide feedback from the command line with the `az feedback` command.</span></span>

