---
title: Azure CLI 2.0 发行说明
description: 了解 Azure CLI 2.0 的最新更新
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 02/27/2018
ms.topic: article
ms.prod: azure
ms.technology: azure
ms.devlang: azurecli
ms.service: multiple
ms.openlocfilehash: 0e81f5723af47242f908b854045deb7d74c50c17
ms.sourcegitcommit: b5a6296c006e3a44f66892729e47d7a967267d3e
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/28/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="0530d-103">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="0530d-103">Azure CLI 2.0 release notes</span></span>

## <a name="march-27-2018"></a><span data-ttu-id="0530d-104">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="0530d-104">March 27, 2018</span></span>

<span data-ttu-id="0530d-105">版本 2.0.30</span><span class="sxs-lookup"><span data-stu-id="0530d-105">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="0530d-106">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-106">Core</span></span>

* <span data-ttu-id="0530d-107">为帮助中标记为预览版的扩展显示消息</span><span class="sxs-lookup"><span data-stu-id="0530d-107">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-108">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-108">ACS</span></span>

* <span data-ttu-id="0530d-109">为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误</span><span class="sxs-lookup"><span data-stu-id="0530d-109">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-110">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-110">Appservice</span></span>

* <span data-ttu-id="0530d-111">为 `webapp update` 添加了仅限 HTTPS 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-111">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="0530d-112">为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-112">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="0530d-113">备份</span><span class="sxs-lookup"><span data-stu-id="0530d-113">Backup</span></span>

* <span data-ttu-id="0530d-114">添加了新命令 `az backup protection isenabled-for-vm`。</span><span class="sxs-lookup"><span data-stu-id="0530d-114">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="0530d-115">此命令可用于检查 VM 是否已由订阅中的任何保管库备份</span><span class="sxs-lookup"><span data-stu-id="0530d-115">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="0530d-116">为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="0530d-116">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="0530d-117">更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="0530d-117">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="0530d-118">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-118">Container</span></span>

* <span data-ttu-id="0530d-119">添加了 `container exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="0530d-119">Added `container exec` command.</span></span> <span data-ttu-id="0530d-120">在正在运行的容器组的容器中执行命令</span><span class="sxs-lookup"><span data-stu-id="0530d-120">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="0530d-121">允许将表输出用于创建和更新容器组</span><span class="sxs-lookup"><span data-stu-id="0530d-121">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="0530d-122">扩展</span><span class="sxs-lookup"><span data-stu-id="0530d-122">Extension</span></span>

* <span data-ttu-id="0530d-123">为 `extension add` 添加了消息（如果扩展处于预览状态）</span><span class="sxs-lookup"><span data-stu-id="0530d-123">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="0530d-124">更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据</span><span class="sxs-lookup"><span data-stu-id="0530d-124">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="0530d-125">[重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据</span><span class="sxs-lookup"><span data-stu-id="0530d-125">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="0530d-126">交互</span><span class="sxs-lookup"><span data-stu-id="0530d-126">Interactive</span></span>

* <span data-ttu-id="0530d-127">已将“完成”更改为在执行命令表加载后立即激活</span><span class="sxs-lookup"><span data-stu-id="0530d-127">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="0530d-128">修复了使用 `--style` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-128">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="0530d-129">交互式词法分析器在命令表转储后实例化（如果缺失）</span><span class="sxs-lookup"><span data-stu-id="0530d-129">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="0530d-130">改进了完成符支持</span><span class="sxs-lookup"><span data-stu-id="0530d-130">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="0530d-131">实验室</span><span class="sxs-lookup"><span data-stu-id="0530d-131">Lab</span></span>

* <span data-ttu-id="0530d-132">修复了 `create environment` 命令的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-132">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-133">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-133">Monitor</span></span>

* <span data-ttu-id="0530d-134">为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="0530d-134">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="0530d-135">修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表</span><span class="sxs-lookup"><span data-stu-id="0530d-135">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="0530d-136">为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="0530d-136">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="0530d-137">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-137">Network</span></span>

* <span data-ttu-id="0530d-138">添加了对专用 DNS 区域的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-138">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-139">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-139">Profile</span></span>

* <span data-ttu-id="0530d-140">为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告</span><span class="sxs-lookup"><span data-stu-id="0530d-140">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="0530d-141">RDBMS</span><span class="sxs-lookup"><span data-stu-id="0530d-141">RDBMS</span></span>

* <span data-ttu-id="0530d-142">添加了业务模型 GA API 版本 2017-12-01</span><span class="sxs-lookup"><span data-stu-id="0530d-142">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-143">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-143">Resource</span></span>

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="0530d-145">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-145">Role</span></span>

* <span data-ttu-id="0530d-146">为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-146">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="0530d-147">更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID</span><span class="sxs-lookup"><span data-stu-id="0530d-147">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="0530d-148">添加了凭据管理命令 `ad sp credential [reset|list|delete]`</span><span class="sxs-lookup"><span data-stu-id="0530d-148">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="0530d-149">[重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”</span><span class="sxs-lookup"><span data-stu-id="0530d-149">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="0530d-150">为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-150">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-151">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-151">Storage</span></span>

* <span data-ttu-id="0530d-152">修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-152">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="0530d-153">修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-153">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-154">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-154">VM</span></span>

* <span data-ttu-id="0530d-155">针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告</span><span class="sxs-lookup"><span data-stu-id="0530d-155">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="0530d-156">为 `vm [snapshot|image]` 添加了区域弹性支持</span><span class="sxs-lookup"><span data-stu-id="0530d-156">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="0530d-157">更改了磁盘实例视图以更好地报告加密状态</span><span class="sxs-lookup"><span data-stu-id="0530d-157">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="0530d-158">[重大更改] 更改了 `vm extension delete` 以不再返回输出</span><span class="sxs-lookup"><span data-stu-id="0530d-158">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="0530d-159">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="0530d-159">March 13, 2018</span></span>

<span data-ttu-id="0530d-160">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="0530d-160">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="0530d-161">ACR</span><span class="sxs-lookup"><span data-stu-id="0530d-161">ACR</span></span>

* <span data-ttu-id="0530d-162">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-162">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="0530d-163">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-163">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="0530d-164">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="0530d-164">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-165">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-165">ACS</span></span>

* <span data-ttu-id="0530d-166">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="0530d-166">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="0530d-167">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="0530d-167">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="0530d-168">顾问</span><span class="sxs-lookup"><span data-stu-id="0530d-168">Advisor</span></span>

* <span data-ttu-id="0530d-169">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="0530d-169">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="0530d-170">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="0530d-170">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="0530d-171">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="0530d-171">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="0530d-172">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-172">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="0530d-173">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-173">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-174">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-174">Appservice</span></span>

* <span data-ttu-id="0530d-175">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="0530d-175">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="0530d-176">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="0530d-176">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="0530d-177">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="0530d-177">Eventhubs</span></span>

* <span data-ttu-id="0530d-178">初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-178">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="0530d-179">分机</span><span class="sxs-lookup"><span data-stu-id="0530d-179">Extension</span></span>

* <span data-ttu-id="0530d-180">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="0530d-180">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="0530d-181">交互</span><span class="sxs-lookup"><span data-stu-id="0530d-181">Interactive</span></span>

* <span data-ttu-id="0530d-182">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="0530d-182">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="0530d-183">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="0530d-183">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="0530d-184">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="0530d-184">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="0530d-185">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="0530d-185">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-186">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-186">Monitor</span></span>

* <span data-ttu-id="0530d-187">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-187">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="0530d-188">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-188">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="0530d-189">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-189">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="0530d-190">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-190">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="0530d-191">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-191">Network</span></span>

* <span data-ttu-id="0530d-192">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-192">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="0530d-193">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="0530d-193">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="0530d-194">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-194">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="0530d-195">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="0530d-195">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-196">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-196">Profile</span></span>

* <span data-ttu-id="0530d-197">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-197">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="0530d-198">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="0530d-198">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="0530d-199">RDBMS</span><span class="sxs-lookup"><span data-stu-id="0530d-199">RDBMS</span></span>

* <span data-ttu-id="0530d-200">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="0530d-200">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="0530d-201">服务总线</span><span class="sxs-lookup"><span data-stu-id="0530d-201">Service Bus</span></span>

* <span data-ttu-id="0530d-202">初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-202">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-203">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-203">Storage</span></span>

* <span data-ttu-id="0530d-204">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云</span><span class="sxs-lookup"><span data-stu-id="0530d-204">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="0530d-205">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="0530d-205">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-206">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-206">VM</span></span>

* <span data-ttu-id="0530d-207">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="0530d-207">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="0530d-208">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="0530d-208">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="0530d-209">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="0530d-209">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="0530d-210">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="0530d-210">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="0530d-211">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="0530d-211">February 27, 2018</span></span>

<span data-ttu-id="0530d-212">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="0530d-212">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="0530d-213">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-213">Core</span></span>

* <span data-ttu-id="0530d-214">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="0530d-214">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="0530d-215">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-215">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="0530d-216">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="0530d-216">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-217">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-217">ACS</span></span>

* <span data-ttu-id="0530d-218">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="0530d-218">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="0530d-219">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-219">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="0530d-220">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="0530d-220">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="0530d-221">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="0530d-221">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-222">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-222">Appservice</span></span>

* <span data-ttu-id="0530d-223">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="0530d-223">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="0530d-224">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="0530d-224">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="0530d-225">认知服务</span><span class="sxs-lookup"><span data-stu-id="0530d-225">Cognitive Services</span></span>

* <span data-ttu-id="0530d-226">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="0530d-226">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="0530d-227">消耗</span><span class="sxs-lookup"><span data-stu-id="0530d-227">Consumption</span></span>

* <span data-ttu-id="0530d-228">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="0530d-228">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="0530d-229">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="0530d-229">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="0530d-230">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-230">Container</span></span>

* <span data-ttu-id="0530d-231">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="0530d-231">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="0530d-232">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-232">Network</span></span>

* <span data-ttu-id="0530d-233">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="0530d-233">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-234">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-234">Resource</span></span>

* <span data-ttu-id="0530d-235">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="0530d-235">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="0530d-236">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-236">Role</span></span>

* <span data-ttu-id="0530d-237">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="0530d-237">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-238">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-238">SQL</span></span>

* <span data-ttu-id="0530d-239">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="0530d-239">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-240">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-240">Storage</span></span>

* <span data-ttu-id="0530d-241">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="0530d-241">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-242">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-242">VM</span></span>

* <span data-ttu-id="0530d-243">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-243">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="0530d-244">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="0530d-244">February 13, 2018</span></span>

<span data-ttu-id="0530d-245">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="0530d-245">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="0530d-246">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-246">Core</span></span>

* <span data-ttu-id="0530d-247">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="0530d-247">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-248">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-248">ACS</span></span>

* <span data-ttu-id="0530d-249">[重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="0530d-249">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="0530d-250">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="0530d-250">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="0530d-251">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="0530d-251">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="0530d-252">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="0530d-252">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="0530d-253">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="0530d-253">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="0530d-254">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="0530d-254">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="0530d-255">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="0530d-255">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="0530d-256">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="0530d-256">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-257">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-257">Appservice</span></span>

* <span data-ttu-id="0530d-258">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-258">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="0530d-259">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-259">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="0530d-260">CDN</span><span class="sxs-lookup"><span data-stu-id="0530d-260">CDN</span></span>

* <span data-ttu-id="0530d-261">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-261">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="0530d-262">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-262">Container</span></span>

* <span data-ttu-id="0530d-263">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="0530d-263">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="0530d-264">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="0530d-264">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0530d-265">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0530d-265">CosmosDB</span></span>

* <span data-ttu-id="0530d-266">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-266">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="0530d-267">分机</span><span class="sxs-lookup"><span data-stu-id="0530d-267">Extension</span></span>

* <span data-ttu-id="0530d-268">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-268">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="0530d-269">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-269">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="0530d-270">反馈</span><span class="sxs-lookup"><span data-stu-id="0530d-270">Feedback</span></span>

* <span data-ttu-id="0530d-271">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="0530d-271">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="0530d-272">交互</span><span class="sxs-lookup"><span data-stu-id="0530d-272">Interactive</span></span>

* <span data-ttu-id="0530d-273">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-273">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="0530d-274">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="0530d-274">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="0530d-275">IoT</span><span class="sxs-lookup"><span data-stu-id="0530d-275">IoT</span></span>

* <span data-ttu-id="0530d-276">修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-276">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="0530d-277">修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-277">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="0530d-278">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="0530d-278">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="0530d-279">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="0530d-279">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-280">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-280">Monitor</span></span>

* <span data-ttu-id="0530d-281">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-281">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="0530d-282">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-282">Network</span></span>

* <span data-ttu-id="0530d-283">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="0530d-283">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="0530d-284">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-284">Profile</span></span>

* <span data-ttu-id="0530d-285">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="0530d-285">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-286">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-286">Resource</span></span>

* <span data-ttu-id="0530d-287">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="0530d-287">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="0530d-288">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-288">Role</span></span>

* <span data-ttu-id="0530d-289">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-289">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-290">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-290">SQL</span></span>

* <span data-ttu-id="0530d-291">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-291">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="0530d-292">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="0530d-292">Added `sql db rename`</span></span>
* <span data-ttu-id="0530d-293">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-293">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-294">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-294">Storage</span></span>

* <span data-ttu-id="0530d-295">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="0530d-295">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-296">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-296">VM</span></span>

* <span data-ttu-id="0530d-297">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="0530d-297">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="0530d-298">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="0530d-298">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="0530d-299">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="0530d-299">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="0530d-300">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="0530d-300">January 31, 2018</span></span>

<span data-ttu-id="0530d-301">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="0530d-301">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="0530d-302">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-302">Core</span></span>

* <span data-ttu-id="0530d-303">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="0530d-303">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="0530d-304">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="0530d-304">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="0530d-305">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="0530d-305">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="0530d-306">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="0530d-306">Use `--verbose` to see</span></span>
* <span data-ttu-id="0530d-307">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="0530d-307">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-308">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-308">ACS</span></span>

* <span data-ttu-id="0530d-309">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-309">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="0530d-310">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="0530d-310">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-311">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-311">Appservice</span></span>

* <span data-ttu-id="0530d-312">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="0530d-312">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="0530d-313">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="0530d-313">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="0530d-314">CDN</span><span class="sxs-lookup"><span data-stu-id="0530d-314">CDN</span></span>

* <span data-ttu-id="0530d-315">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="0530d-315">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0530d-316">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0530d-316">CosmosDB</span></span>

* <span data-ttu-id="0530d-317">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="0530d-317">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="0530d-318">交互</span><span class="sxs-lookup"><span data-stu-id="0530d-318">Interactive</span></span>

* <span data-ttu-id="0530d-319">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-319">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="0530d-320">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-320">Network</span></span>

* <span data-ttu-id="0530d-321">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="0530d-321">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="0530d-322">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-322">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="0530d-323">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="0530d-323">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="0530d-324">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="0530d-324">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="0530d-325">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-325">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="0530d-326">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="0530d-326">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="0530d-327">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-327">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="0530d-328">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-328">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="0530d-329">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-329">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="0530d-330">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-330">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-331">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-331">Profile</span></span>

* <span data-ttu-id="0530d-332">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="0530d-332">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-333">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-333">Resource</span></span>

* <span data-ttu-id="0530d-334">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="0530d-334">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-335">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-335">Storage</span></span>

* <span data-ttu-id="0530d-336">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-336">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="0530d-337">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="0530d-337">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="0530d-338">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-338">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="0530d-339">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="0530d-339">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="0530d-340">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-340">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-341">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-341">VM</span></span>

* <span data-ttu-id="0530d-342">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="0530d-342">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="0530d-343">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="0530d-343">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="0530d-344">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-344">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="0530d-345">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="0530d-345">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="0530d-346">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="0530d-346">January 17, 2018</span></span>

<span data-ttu-id="0530d-347">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="0530d-347">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="0530d-348">ACR</span><span class="sxs-lookup"><span data-stu-id="0530d-348">ACR</span></span>

* <span data-ttu-id="0530d-349">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-349">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="0530d-350">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="0530d-350">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-351">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-351">ACS</span></span>

* <span data-ttu-id="0530d-352">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-352">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="0530d-353">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="0530d-353">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-354">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-354">Appservice</span></span>

* <span data-ttu-id="0530d-355">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-355">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="0530d-356">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="0530d-356">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="0530d-357">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="0530d-357">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="0530d-358">备份</span><span class="sxs-lookup"><span data-stu-id="0530d-358">Backup</span></span>

* <span data-ttu-id="0530d-359">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="0530d-359">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="0530d-360">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="0530d-360">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="0530d-361">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="0530d-361">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="0530d-362">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-362">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="0530d-363">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="0530d-363">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="0530d-364">Batch</span><span class="sxs-lookup"><span data-stu-id="0530d-364">Batch</span></span>

* <span data-ttu-id="0530d-365">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="0530d-365">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="0530d-366">云</span><span class="sxs-lookup"><span data-stu-id="0530d-366">Cloud</span></span>

* <span data-ttu-id="0530d-367">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="0530d-367">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="0530d-368">消耗</span><span class="sxs-lookup"><span data-stu-id="0530d-368">Consumption</span></span>

* <span data-ttu-id="0530d-369">添加了用于保留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="0530d-369">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="0530d-370">事件网格</span><span class="sxs-lookup"><span data-stu-id="0530d-370">Event Grid</span></span>

* <span data-ttu-id="0530d-371">[重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="0530d-371">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="0530d-372">[重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="0530d-372">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="0530d-373">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="0530d-373">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="0530d-374">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="0530d-374">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="0530d-375">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="0530d-375">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="0530d-376">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="0530d-376">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="0530d-377">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-377">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="0530d-378">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="0530d-378">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="0530d-379">交互</span><span class="sxs-lookup"><span data-stu-id="0530d-379">Interactive</span></span>

* <span data-ttu-id="0530d-380">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-380">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="0530d-381">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-381">Fixed errors on startup</span></span>
* <span data-ttu-id="0530d-382">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-382">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="0530d-383">IoT</span><span class="sxs-lookup"><span data-stu-id="0530d-383">IoT</span></span>

* <span data-ttu-id="0530d-384">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-384">Added support for device provisioning service</span></span>
* <span data-ttu-id="0530d-385">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="0530d-385">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="0530d-386">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="0530d-386">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-387">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-387">Monitor</span></span>

* <span data-ttu-id="0530d-388">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="0530d-388">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="0530d-389">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="0530d-389">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="0530d-390">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="0530d-390">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="0530d-391">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-391">Network</span></span>

* <span data-ttu-id="0530d-392">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-392">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="0530d-393">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-393">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-394">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-394">Profile</span></span>

* <span data-ttu-id="0530d-395">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-395">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="0530d-396">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-396">Role</span></span>

* <span data-ttu-id="0530d-397">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="0530d-397">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="0530d-398">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0530d-398">Service Fabric</span></span>

* <span data-ttu-id="0530d-399">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="0530d-399">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="0530d-400">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="0530d-400">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-401">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-401">VM</span></span>

* <span data-ttu-id="0530d-402">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="0530d-402">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="0530d-403">[重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="0530d-403">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="0530d-404">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="0530d-404">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="0530d-405">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="0530d-405">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="0530d-406">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-406">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="0530d-407">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-407">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="0530d-408">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="0530d-408">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="0530d-409">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-409">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="0530d-410">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="0530d-410">December 19, 2017</span></span>

<span data-ttu-id="0530d-411">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="0530d-411">Version 2.0.23</span></span>

* <span data-ttu-id="0530d-412">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-412">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="0530d-413">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-413">Container</span></span>

* <span data-ttu-id="0530d-414">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="0530d-414">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="0530d-415">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-415">Network</span></span>

* <span data-ttu-id="0530d-416">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-416">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="0530d-417">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-417">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-418">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-418">Storage</span></span>

* <span data-ttu-id="0530d-419">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-419">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-420">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-420">VM</span></span>

* <span data-ttu-id="0530d-421">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-421">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="0530d-422">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="0530d-422">December 5, 2017</span></span>

<span data-ttu-id="0530d-423">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="0530d-423">Version 2.0.22</span></span>

* <span data-ttu-id="0530d-424">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="0530d-424">Removed `az component` commands.</span></span> <span data-ttu-id="0530d-425">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="0530d-425">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="0530d-426">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-426">Core</span></span>
* <span data-ttu-id="0530d-427">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="0530d-427">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="0530d-428">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-428">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-429">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-429">ACS</span></span>

* <span data-ttu-id="0530d-430">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-430">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="0530d-431">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="0530d-431">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="0530d-432">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="0530d-432">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="0530d-433">顾问</span><span class="sxs-lookup"><span data-stu-id="0530d-433">Advisor</span></span>

* <span data-ttu-id="0530d-434">初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-434">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-435">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-435">Appservice</span></span>

* <span data-ttu-id="0530d-436">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="0530d-436">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="0530d-437">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="0530d-437">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="0530d-438">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="0530d-438">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="0530d-439">消耗</span><span class="sxs-lookup"><span data-stu-id="0530d-439">Consumption</span></span>

* <span data-ttu-id="0530d-440">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-440">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="0530d-441">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-441">Container</span></span>

* <span data-ttu-id="0530d-442">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="0530d-442">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-443">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-443">Monitor</span></span>

* <span data-ttu-id="0530d-444">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="0530d-444">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-445">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-445">Resource</span></span>

* <span data-ttu-id="0530d-446">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-446">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="0530d-447">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-447">Role</span></span>

* <span data-ttu-id="0530d-448">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="0530d-448">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="0530d-449">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="0530d-449">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="0530d-450">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="0530d-450">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-451">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-451">SQL</span></span>

* <span data-ttu-id="0530d-452">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-452">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="0530d-453">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-453">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-454">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-454">VM</span></span>

* <span data-ttu-id="0530d-455">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="0530d-455">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="0530d-456">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="0530d-456">November 14, 2017</span></span>

<span data-ttu-id="0530d-457">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="0530d-457">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="0530d-458">ACR</span><span class="sxs-lookup"><span data-stu-id="0530d-458">ACR</span></span>

* <span data-ttu-id="0530d-459">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-459">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="0530d-460">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-460">ACS</span></span>

* <span data-ttu-id="0530d-461">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="0530d-461">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="0530d-462">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="0530d-462">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="0530d-463">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="0530d-463">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="0530d-464">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="0530d-464">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="0530d-465">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="0530d-465">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-466">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-466">Appservice</span></span>

* <span data-ttu-id="0530d-467">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="0530d-467">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="0530d-468">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="0530d-468">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="0530d-469">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="0530d-469">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="0530d-470">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="0530d-470">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="0530d-471">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-471">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="0530d-472">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="0530d-472">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="0530d-473">Batch</span><span class="sxs-lookup"><span data-stu-id="0530d-473">Batch</span></span>

* <span data-ttu-id="0530d-474">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-474">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="0530d-475">Batchai</span><span class="sxs-lookup"><span data-stu-id="0530d-475">Batchai</span></span>

* <span data-ttu-id="0530d-476">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="0530d-476">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="0530d-477">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="0530d-477">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="0530d-478">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="0530d-478">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="0530d-479">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="0530d-479">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="0530d-480">云</span><span class="sxs-lookup"><span data-stu-id="0530d-480">Cloud</span></span>

* <span data-ttu-id="0530d-481">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="0530d-481">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="0530d-482">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-482">Container</span></span>

* <span data-ttu-id="0530d-483">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-483">Added support to open multiple ports</span></span>
* <span data-ttu-id="0530d-484">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="0530d-484">Added container group restart policy</span></span>
* <span data-ttu-id="0530d-485">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-485">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="0530d-486">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="0530d-486">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="0530d-487">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="0530d-487">Data Lake Analytics</span></span>

* <span data-ttu-id="0530d-488">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="0530d-488">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="0530d-489">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0530d-489">Data Lake Store</span></span>

* <span data-ttu-id="0530d-490">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="0530d-490">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="0530d-491">分机</span><span class="sxs-lookup"><span data-stu-id="0530d-491">Extension</span></span>

* <span data-ttu-id="0530d-492">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="0530d-492">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="0530d-493">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="0530d-493">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="0530d-494">IoT</span><span class="sxs-lookup"><span data-stu-id="0530d-494">IoT</span></span>

* <span data-ttu-id="0530d-495">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-495">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-496">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-496">Monitor</span></span>

* <span data-ttu-id="0530d-497">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-497">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="0530d-498">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-498">Network</span></span>

* <span data-ttu-id="0530d-499">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-499">Added support for CAA DNS records</span></span>
* <span data-ttu-id="0530d-500">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-500">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="0530d-501">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-501">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="0530d-502">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-502">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="0530d-503">保留</span><span class="sxs-lookup"><span data-stu-id="0530d-503">Reservations</span></span>

* <span data-ttu-id="0530d-504">初始预览版</span><span class="sxs-lookup"><span data-stu-id="0530d-504">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-505">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-505">Resource</span></span>

* <span data-ttu-id="0530d-506">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-506">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-507">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-507">SQL</span></span>

* <span data-ttu-id="0530d-508">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-508">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-509">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-509">Storage</span></span>

* <span data-ttu-id="0530d-510">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="0530d-510">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="0530d-511">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-511">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="0530d-512">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-512">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="0530d-513">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="0530d-513">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="0530d-514">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-514">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="0530d-515">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-515">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="0530d-516">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-516">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-517">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-517">VM</span></span>

* <span data-ttu-id="0530d-518">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-518">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="0530d-519">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-519">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="0530d-520">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-520">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="0530d-521">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="0530d-521">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="0530d-522">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-522">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="0530d-523">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="0530d-523">October 24, 2017</span></span>

<span data-ttu-id="0530d-524">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="0530d-524">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="0530d-525">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-525">Core</span></span>

* <span data-ttu-id="0530d-526">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="0530d-526">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="0530d-527">ACR</span><span class="sxs-lookup"><span data-stu-id="0530d-527">ACR</span></span>

* <span data-ttu-id="0530d-528">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="0530d-528">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="0530d-529">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="0530d-529">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="0530d-530">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="0530d-530">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-531">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-531">ACS</span></span>

* <span data-ttu-id="0530d-532">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-532">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="0530d-533">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="0530d-533">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-534">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-534">Appservice</span></span>

* <span data-ttu-id="0530d-535">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-535">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="0530d-536">组件</span><span class="sxs-lookup"><span data-stu-id="0530d-536">Component</span></span>

* <span data-ttu-id="0530d-537">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="0530d-537">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-538">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-538">Monitor</span></span>

* <span data-ttu-id="0530d-539">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-539">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-540">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-540">Resource</span></span>

* <span data-ttu-id="0530d-541">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-541">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="0530d-542">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="0530d-542">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-543">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-543">VM</span></span>

* <span data-ttu-id="0530d-544">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-544">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="0530d-545">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="0530d-545">October 9, 2017</span></span>

<span data-ttu-id="0530d-546">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="0530d-546">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="0530d-547">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-547">Core</span></span>

* <span data-ttu-id="0530d-548">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="0530d-548">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-549">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-549">Appservice</span></span>

* <span data-ttu-id="0530d-550">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="0530d-550">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="0530d-551">Batch</span><span class="sxs-lookup"><span data-stu-id="0530d-551">Batch</span></span>

* <span data-ttu-id="0530d-552">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="0530d-552">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="0530d-553">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="0530d-553">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="0530d-554">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-554">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="0530d-555">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="0530d-555">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="0530d-556">Batchai</span><span class="sxs-lookup"><span data-stu-id="0530d-556">Batchai</span></span>

* <span data-ttu-id="0530d-557">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-557">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="0530d-558">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0530d-558">Keyvault</span></span>

* <span data-ttu-id="0530d-559">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="0530d-559">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="0530d-560">(#4448)</span><span class="sxs-lookup"><span data-stu-id="0530d-560">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="0530d-561">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-561">Network</span></span>

* <span data-ttu-id="0530d-562">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="0530d-562">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="0530d-563">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="0530d-563">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-564">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-564">Resource</span></span>

* <span data-ttu-id="0530d-565">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-565">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="0530d-566">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="0530d-566">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="0530d-567">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="0530d-567">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="0530d-568">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="0530d-568">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-569">Sql</span><span class="sxs-lookup"><span data-stu-id="0530d-569">Sql</span></span>

* <span data-ttu-id="0530d-570">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-570">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="0530d-571">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="0530d-571">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="0530d-572">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="0530d-572">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-573">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-573">Storage</span></span>

* <span data-ttu-id="0530d-574">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-574">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-575">Vm</span><span class="sxs-lookup"><span data-stu-id="0530d-575">Vm</span></span>

* <span data-ttu-id="0530d-576">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="0530d-576">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="0530d-577">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-577">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="0530d-578">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-578">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="0530d-579">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-579">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="0530d-580">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-580">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="0530d-581">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="0530d-581">September 22, 2017</span></span>

<span data-ttu-id="0530d-582">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="0530d-582">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-583">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-583">Resource</span></span>

* <span data-ttu-id="0530d-584">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-584">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="0530d-585">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="0530d-585">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="0530d-586">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-586">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="0530d-587">[重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="0530d-587">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="0530d-588">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-588">Network</span></span>

* <span data-ttu-id="0530d-589">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-589">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="0530d-590">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-590">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="0530d-591">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="0530d-591">Added `asg` application security group commands</span></span>
* <span data-ttu-id="0530d-592">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-592">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="0530d-593">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-593">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="0530d-594">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-594">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="0530d-595">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-595">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-596">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-596">Storage</span></span>

* <span data-ttu-id="0530d-597">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-597">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="0530d-598">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="0530d-598">Eventgrid</span></span>

* <span data-ttu-id="0530d-599">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="0530d-599">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-600">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-600">SQL</span></span>

* <span data-ttu-id="0530d-601">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="0530d-601">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="0530d-602">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="0530d-602">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="0530d-603">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-603">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="0530d-604">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0530d-604">Keyvault</span></span>

* <span data-ttu-id="0530d-605">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-605">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-606">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-606">VM</span></span>

* <span data-ttu-id="0530d-607">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-607">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="0530d-608">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-608">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="0530d-609">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-609">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="0530d-610">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-610">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="0530d-611">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-611">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="0530d-612">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-612">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-613">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-613">ACS</span></span>

* <span data-ttu-id="0530d-614">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-614">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-615">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-615">Appservice</span></span>

* <span data-ttu-id="0530d-616">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-616">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="0530d-617">备份</span><span class="sxs-lookup"><span data-stu-id="0530d-617">Backup</span></span>

* <span data-ttu-id="0530d-618">预览版</span><span class="sxs-lookup"><span data-stu-id="0530d-618">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="0530d-619">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="0530d-619">September 11, 2017</span></span>

<span data-ttu-id="0530d-620">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="0530d-620">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="0530d-621">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-621">Core</span></span>

* <span data-ttu-id="0530d-622">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="0530d-622">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="0530d-623">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="0530d-623">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-624">Acs</span><span class="sxs-lookup"><span data-stu-id="0530d-624">Acs</span></span>

* <span data-ttu-id="0530d-625">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-625">Added `acs list-locations` command</span></span>
* <span data-ttu-id="0530d-626">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="0530d-626">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-627">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-627">Appservice</span></span>

* <span data-ttu-id="0530d-628">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-628">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="0530d-629">CDN</span><span class="sxs-lookup"><span data-stu-id="0530d-629">CDN</span></span>

* <span data-ttu-id="0530d-630">修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug</span><span class="sxs-lookup"><span data-stu-id="0530d-630">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="0530d-631">Extension</span><span class="sxs-lookup"><span data-stu-id="0530d-631">Extension</span></span>

* <span data-ttu-id="0530d-632">初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-632">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="0530d-633">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0530d-633">Keyvault</span></span>

* <span data-ttu-id="0530d-634">为 `keyvault set-policy` 修复了权限区分大小写的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-634">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="0530d-635">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-635">Network</span></span>

* <span data-ttu-id="0530d-636">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="0530d-636">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="0530d-637">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="0530d-637">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="0530d-638">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-638">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="0530d-639">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-639">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="0530d-640">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-640">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-641">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-641">Resource</span></span>

* <span data-ttu-id="0530d-642">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="0530d-642">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="0530d-643">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="0530d-643">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="0530d-644">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="0530d-644">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="0530d-645">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="0530d-645">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-646">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-646">SQL</span></span>

* <span data-ttu-id="0530d-647">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-647">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-648">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-648">VM</span></span>

* <span data-ttu-id="0530d-649">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="0530d-649">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="0530d-650">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="0530d-650">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="0530d-651">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="0530d-651">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="0530d-652">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="0530d-652">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="0530d-653">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="0530d-653">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="0530d-654">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="0530d-654">August 31, 2017</span></span>

<span data-ttu-id="0530d-655">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="0530d-655">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="0530d-656">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0530d-656">Keyvault</span></span>

* <span data-ttu-id="0530d-657">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-657">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="0530d-658">Sf</span><span class="sxs-lookup"><span data-stu-id="0530d-658">Sf</span></span>

* <span data-ttu-id="0530d-659">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="0530d-659">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-660">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-660">Storage</span></span>

* <span data-ttu-id="0530d-661">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-661">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="0530d-662">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="0530d-662">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="0530d-663">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="0530d-663">August 28, 2017</span></span>

<span data-ttu-id="0530d-664">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="0530d-664">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="0530d-665">CLI</span><span class="sxs-lookup"><span data-stu-id="0530d-665">CLI</span></span>

* <span data-ttu-id="0530d-666">在 `--version` 中添加了法律说明</span><span class="sxs-lookup"><span data-stu-id="0530d-666">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-667">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-667">ACS</span></span>

* <span data-ttu-id="0530d-668">更正了预览区域</span><span class="sxs-lookup"><span data-stu-id="0530d-668">Corrected preview regions</span></span>
* <span data-ttu-id="0530d-669">正确设置了默认 `dns_name_prefix` 的格式</span><span class="sxs-lookup"><span data-stu-id="0530d-669">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="0530d-670">优化了 acs 命令输出</span><span class="sxs-lookup"><span data-stu-id="0530d-670">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-671">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-671">Appservice</span></span>

* <span data-ttu-id="0530d-672">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致</span><span class="sxs-lookup"><span data-stu-id="0530d-672">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="0530d-673">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="0530d-673">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="0530d-674">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="0530d-674">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="0530d-675">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="0530d-675">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="0530d-676">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="0530d-676">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="0530d-677">IoT</span><span class="sxs-lookup"><span data-stu-id="0530d-677">IoT</span></span>

* <span data-ttu-id="0530d-678">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="0530d-678">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="0530d-679">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-679">Network</span></span>

* <span data-ttu-id="0530d-680">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="0530d-680">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="0530d-681">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="0530d-681">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="0530d-682">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-682">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="0530d-683">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-683">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="0530d-684">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-684">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-685">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-685">Profile</span></span>

* <span data-ttu-id="0530d-686">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="0530d-686">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="0530d-687">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0530d-687">Service Fabric</span></span>

* <span data-ttu-id="0530d-688">预览版</span><span class="sxs-lookup"><span data-stu-id="0530d-688">Preview release</span></span>
* <span data-ttu-id="0530d-689">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="0530d-689">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="0530d-690">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-690">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="0530d-691">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-691">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-692">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-692">Storage</span></span>

* <span data-ttu-id="0530d-693">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="0530d-693">Enabled setting blob tier</span></span>
* <span data-ttu-id="0530d-694">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="0530d-694">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="0530d-695">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="0530d-695">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="0530d-696">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-696">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="0530d-697">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="0530d-697">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="0530d-698">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="0530d-698">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-699">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-699">VM</span></span>

* <span data-ttu-id="0530d-700">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-700">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="0530d-701">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="0530d-701">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="0530d-702">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="0530d-702">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="0530d-703">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-703">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="0530d-704">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-704">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="0530d-705">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-705">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="0530d-706">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="0530d-706">August 15, 2017</span></span>

<span data-ttu-id="0530d-707">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="0530d-707">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-708">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-708">ACS</span></span>

* <span data-ttu-id="0530d-709">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="0530d-709">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-710">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-710">Appservice</span></span>

* <span data-ttu-id="0530d-711">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-711">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="0530d-712">事件网格</span><span class="sxs-lookup"><span data-stu-id="0530d-712">Event Grid</span></span>

* <span data-ttu-id="0530d-713">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="0530d-713">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="0530d-714">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="0530d-714">August 11, 2017</span></span>

<span data-ttu-id="0530d-715">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="0530d-715">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-716">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-716">ACS</span></span>

* <span data-ttu-id="0530d-717">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="0530d-717">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="0530d-718">Batch</span><span class="sxs-lookup"><span data-stu-id="0530d-718">Batch</span></span>

* <span data-ttu-id="0530d-719">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="0530d-719">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="0530d-720">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="0530d-720">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="0530d-721">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-721">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="0530d-722">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="0530d-722">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="0530d-723">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="0530d-723">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="0530d-724">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="0530d-724">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="0530d-725">组件</span><span class="sxs-lookup"><span data-stu-id="0530d-725">Component</span></span>

* <span data-ttu-id="0530d-726">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="0530d-726">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="0530d-727">容器</span><span class="sxs-lookup"><span data-stu-id="0530d-727">Container</span></span>

* <span data-ttu-id="0530d-728">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-728">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="0530d-729">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0530d-729">Data Lake Store</span></span>

* <span data-ttu-id="0530d-730">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="0530d-730">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="0530d-731">事件网格</span><span class="sxs-lookup"><span data-stu-id="0530d-731">Event Grid</span></span>

* <span data-ttu-id="0530d-732">初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-732">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="0530d-733">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-733">Network</span></span>

* <span data-ttu-id="0530d-734">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-734">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="0530d-735">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-735">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="0530d-736">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-736">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="0530d-737">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="0530d-737">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-738">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-738">Profile</span></span>

* <span data-ttu-id="0530d-739">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="0530d-739">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-740">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-740">Storage</span></span>

* <span data-ttu-id="0530d-741">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-741">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-742">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-742">VM</span></span>

* <span data-ttu-id="0530d-743">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="0530d-743">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="0530d-744">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-744">Exposed `list-skus` command</span></span>
* <span data-ttu-id="0530d-745">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="0530d-745">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="0530d-746">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="0530d-746">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="0530d-747">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="0530d-747">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="0530d-748">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="0530d-748">July 28, 2017</span></span>

<span data-ttu-id="0530d-749">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="0530d-749">Version 2.0.12</span></span>

* <span data-ttu-id="0530d-750">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="0530d-750">Added container commands</span></span>
* <span data-ttu-id="0530d-751">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="0530d-751">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="0530d-752">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-752">Core</span></span>

* <span data-ttu-id="0530d-753">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="0530d-753">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="0530d-754">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="0530d-754">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="0530d-755">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="0530d-755">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="0530d-756">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="0530d-756">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="0530d-757">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="0530d-757">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="0530d-758">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="0530d-758">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="0530d-759">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="0530d-759">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="0530d-760">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="0530d-760">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="0530d-761">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="0530d-761">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="0530d-762">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="0530d-762">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="0530d-763">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="0530d-763">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="0530d-764">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="0530d-764">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="0530d-765">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="0530d-765">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="0530d-766">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="0530d-766">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="0530d-767">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="0530d-767">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="0530d-768">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="0530d-768">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="0530d-769">ACR</span><span class="sxs-lookup"><span data-stu-id="0530d-769">ACR</span></span>

* <span data-ttu-id="0530d-770">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-770">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="0530d-771">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="0530d-771">Support SKU update for managed registries</span></span>
* <span data-ttu-id="0530d-772">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="0530d-772">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="0530d-773">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="0530d-773">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="0530d-774">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-774">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="0530d-775">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-775">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-776">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-776">ACS</span></span>

* <span data-ttu-id="0530d-777">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-777">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-778">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-778">Appservice</span></span>

* <span data-ttu-id="0530d-779">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-779">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="0530d-780">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="0530d-780">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="0530d-781">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="0530d-781">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="0530d-782">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="0530d-782">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="0530d-783">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="0530d-783">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="0530d-784">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="0530d-784">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="0530d-785">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="0530d-785">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="0530d-786">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="0530d-786">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="0530d-787">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="0530d-787">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="0530d-788">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="0530d-788">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="0530d-789">Batch</span><span class="sxs-lookup"><span data-stu-id="0530d-789">Batch</span></span>

* <span data-ttu-id="0530d-790">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="0530d-790">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="0530d-791">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="0530d-791">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="0530d-792">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="0530d-792">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="0530d-793">CDN</span><span class="sxs-lookup"><span data-stu-id="0530d-793">CDN</span></span>

* <span data-ttu-id="0530d-794">当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息</span><span class="sxs-lookup"><span data-stu-id="0530d-794">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="0530d-795">云</span><span class="sxs-lookup"><span data-stu-id="0530d-795">Cloud</span></span>

* <span data-ttu-id="0530d-796">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="0530d-796">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="0530d-797">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="0530d-797">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="0530d-798">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="0530d-798">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="0530d-799">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-799">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="0530d-800">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="0530d-800">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0530d-801">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0530d-801">CosmosDB</span></span>

* <span data-ttu-id="0530d-802">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-802">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="0530d-803">添加了对集合默认 TTL 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-803">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="0530d-804">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="0530d-804">Data Lake Analytics</span></span>

* <span data-ttu-id="0530d-805">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="0530d-805">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="0530d-806">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="0530d-806">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="0530d-807">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="0530d-807">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="0530d-808">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0530d-808">Data Lake Store</span></span>

* <span data-ttu-id="0530d-809">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-809">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="0530d-810">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="0530d-810">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="0530d-811">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="0530d-811">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="0530d-812">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="0530d-812">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="0530d-813">交互</span><span class="sxs-lookup"><span data-stu-id="0530d-813">Interactive</span></span>

* <span data-ttu-id="0530d-814">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="0530d-814">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="0530d-815">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="0530d-815">Increased test coverage</span></span>
* <span data-ttu-id="0530d-816">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="0530d-816">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="0530d-817">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="0530d-817">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="0530d-818">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="0530d-818">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="0530d-819">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="0530d-819">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="0530d-820">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="0530d-820">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="0530d-821">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="0530d-821">Added `--progress` flag</span></span>
* <span data-ttu-id="0530d-822">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="0530d-822">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="0530d-823">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="0530d-823">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="0530d-824">IoT</span><span class="sxs-lookup"><span data-stu-id="0530d-824">IoT</span></span>

* <span data-ttu-id="0530d-825">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="0530d-825">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="0530d-826">(#3934)</span><span class="sxs-lookup"><span data-stu-id="0530d-826">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="0530d-827">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="0530d-827">Key vault</span></span>

* <span data-ttu-id="0530d-828">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="0530d-828">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="0530d-829">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0530d-829">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="0530d-830">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0530d-830">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="0530d-831">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0530d-831">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="0530d-832">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="0530d-832">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="0530d-833">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="0530d-833">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="0530d-834">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="0530d-834">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="0530d-835">(#3307)</span><span class="sxs-lookup"><span data-stu-id="0530d-835">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="0530d-836">实验室</span><span class="sxs-lookup"><span data-stu-id="0530d-836">Lab</span></span>

* <span data-ttu-id="0530d-837">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-837">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="0530d-838">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="0530d-838">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-839">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-839">Monitor</span></span>

* <span data-ttu-id="0530d-840">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="0530d-840">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="0530d-841">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="0530d-841">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="0530d-842">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="0530d-842">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="0530d-843">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="0530d-843">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="0530d-844">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="0530d-844">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="0530d-845">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="0530d-845">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="0530d-846">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="0530d-846">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="0530d-847">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="0530d-847">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="0530d-848">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="0530d-848">`location` no longer required</span></span>
  * <span data-ttu-id="0530d-849">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="0530d-849">Add name and ID support for target</span></span>
  * <span data-ttu-id="0530d-850">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="0530d-850">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="0530d-851">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="0530d-851">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="0530d-852">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="0530d-852">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="0530d-853">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="0530d-853">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="0530d-854">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="0530d-854">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="0530d-855">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="0530d-855">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="0530d-856">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-856">Network</span></span>

* <span data-ttu-id="0530d-857">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-857">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="0530d-858">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-858">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="0530d-859">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-859">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="0530d-860">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-860">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="0530d-861">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-861">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="0530d-862">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-862">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="0530d-863">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="0530d-863">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="0530d-864">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="0530d-864">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="0530d-865">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="0530d-865">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="0530d-866">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="0530d-866">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="0530d-867">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-867">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="0530d-868">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-868">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="0530d-869">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="0530d-869">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="0530d-870">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-870">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="0530d-871">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-871">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="0530d-872">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-872">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="0530d-873">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-873">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="0530d-874">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-874">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="0530d-875">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-875">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="0530d-876">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-876">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="0530d-877">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-877">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="0530d-878">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-878">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="0530d-879">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="0530d-879">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="0530d-880">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="0530d-880">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="0530d-881">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="0530d-881">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="0530d-882">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="0530d-882">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="0530d-883">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="0530d-883">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-884">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-884">Profile</span></span>

* <span data-ttu-id="0530d-885">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="0530d-885">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="0530d-886">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="0530d-886">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="0530d-887">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="0530d-887">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="0530d-888">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="0530d-888">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="0530d-889">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="0530d-889">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="0530d-890">RDBMS</span><span class="sxs-lookup"><span data-stu-id="0530d-890">RDBMS</span></span>

* <span data-ttu-id="0530d-891">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="0530d-891">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="0530d-892">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="0530d-892">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="0530d-893">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="0530d-893">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="0530d-894">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="0530d-894">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-895">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-895">Resource</span></span>

* <span data-ttu-id="0530d-896">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="0530d-896">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="0530d-897">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="0530d-897">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="0530d-898">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-898">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="0530d-899">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-899">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="0530d-900">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="0530d-900">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="0530d-901">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="0530d-901">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="0530d-902">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="0530d-902">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="0530d-903">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-903">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="0530d-904">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-904">Role</span></span>

* <span data-ttu-id="0530d-905">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="0530d-905">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="0530d-906">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="0530d-906">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="0530d-907">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="0530d-907">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="0530d-908">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="0530d-908">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="0530d-909">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="0530d-909">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="0530d-910">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="0530d-910">Service Fabric</span></span>
* <span data-ttu-id="0530d-911">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="0530d-911">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="0530d-912">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="0530d-912">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="0530d-913">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="0530d-913">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-914">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-914">SQL</span></span>

* <span data-ttu-id="0530d-915">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="0530d-915">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="0530d-916">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="0530d-916">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="0530d-917">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="0530d-917">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-918">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-918">Storage</span></span>

* <span data-ttu-id="0530d-919">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="0530d-919">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="0530d-920">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="0530d-920">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="0530d-921">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="0530d-921">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="0530d-922">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="0530d-922">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="0530d-923">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="0530d-923">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="0530d-924">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="0530d-924">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-925">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-925">VM</span></span>

* <span data-ttu-id="0530d-926">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="0530d-926">Support configuring nsg</span></span>
* <span data-ttu-id="0530d-927">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-927">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="0530d-928">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="0530d-928">Support managed service identities</span></span>
* <span data-ttu-id="0530d-929">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-929">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="0530d-930">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="0530d-930">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="0530d-931">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="0530d-931">May 10, 2017</span></span>

<span data-ttu-id="0530d-932">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="0530d-932">Version 2.0.6</span></span>

* <span data-ttu-id="0530d-933">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="0530d-933">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="0530d-934">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="0530d-934">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="0530d-935">包括 Data Lake Analytics 和 Data Lake Store 模块</span><span class="sxs-lookup"><span data-stu-id="0530d-935">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="0530d-936">包括认知服务模块</span><span class="sxs-lookup"><span data-stu-id="0530d-936">Include Cognitive Services module</span></span>
* <span data-ttu-id="0530d-937">包括 Service Fabric 模块</span><span class="sxs-lookup"><span data-stu-id="0530d-937">Include Service Fabric module</span></span>
* <span data-ttu-id="0530d-938">包括交互式模块（重命名 az-shell）</span><span class="sxs-lookup"><span data-stu-id="0530d-938">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="0530d-939">添加对 CDN 命令的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-939">Add support for CDN commands</span></span>
* <span data-ttu-id="0530d-940">删除容器模块</span><span class="sxs-lookup"><span data-stu-id="0530d-940">Remove Container module</span></span>
* <span data-ttu-id="0530d-941">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="0530d-941">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="0530d-942">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="0530d-942">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="0530d-943">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-943">Core</span></span>

* <span data-ttu-id="0530d-944">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="0530d-944">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="0530d-945">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="0530d-945">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="0530d-946">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="0530d-946">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="0530d-947">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="0530d-947">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="0530d-948">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="0530d-948">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="0530d-949">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="0530d-949">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="0530d-950">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="0530d-950">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="0530d-951">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="0530d-951">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="0530d-952">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="0530d-952">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="0530d-953">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="0530d-953">core: Improved performance</span></span>
* <span data-ttu-id="0530d-954">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="0530d-954">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="0530d-955">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="0530d-955">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-956">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-956">ACS</span></span>

* <span data-ttu-id="0530d-957">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="0530d-957">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="0530d-958">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="0530d-958">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="0530d-959">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="0530d-959">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="0530d-960">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="0530d-960">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-961">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-961">AppService</span></span>

* <span data-ttu-id="0530d-962">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="0530d-962">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="0530d-963">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="0530d-963">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="0530d-964">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="0530d-964">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="0530d-965">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="0530d-965">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="0530d-966">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="0530d-966">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="0530d-967">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="0530d-967">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="0530d-968">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="0530d-968">support slot swap with preview</span></span>
* <span data-ttu-id="0530d-969">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="0530d-969">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="0530d-970">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="0530d-970">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="0530d-971">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="0530d-971">CosmosDB</span></span>

* <span data-ttu-id="0530d-972">将 documentdb 模块重命名为 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="0530d-972">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="0530d-973">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="0530d-973">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="0530d-974">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-974">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="0530d-975">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-975">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="0530d-976">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="0530d-976">Data Lake Analytics</span></span>

* <span data-ttu-id="0530d-977">修复了在筛选作业结果和状态列表时会引发错误的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-977">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="0530d-978">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="0530d-978">Add support for new catalog item type: package.</span></span> <span data-ttu-id="0530d-979">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="0530d-979">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="0530d-980">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="0530d-980">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="0530d-981">表</span><span class="sxs-lookup"><span data-stu-id="0530d-981">Table</span></span>
  * <span data-ttu-id="0530d-982">表值函数</span><span class="sxs-lookup"><span data-stu-id="0530d-982">Table valued function</span></span>
  * <span data-ttu-id="0530d-983">查看</span><span class="sxs-lookup"><span data-stu-id="0530d-983">View</span></span>
  * <span data-ttu-id="0530d-984">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="0530d-984">Table Statistics.</span></span> <span data-ttu-id="0530d-985">这也可以使用架构（但无需指定表名）列出</span><span class="sxs-lookup"><span data-stu-id="0530d-985">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="0530d-986">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="0530d-986">Data Lake Store</span></span>

* <span data-ttu-id="0530d-987">更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-987">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="0530d-988">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="0530d-988">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="0530d-989">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="0530d-989">missed help for access show.</span></span> <span data-ttu-id="0530d-990">正在添加。</span><span class="sxs-lookup"><span data-stu-id="0530d-990">adding it.</span></span> <span data-ttu-id="0530d-991">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="0530d-991">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="0530d-992">查找</span><span class="sxs-lookup"><span data-stu-id="0530d-992">Find</span></span>

* <span data-ttu-id="0530d-993">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="0530d-993">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="0530d-994">KeyVault</span><span class="sxs-lookup"><span data-stu-id="0530d-994">KeyVault</span></span>

* <span data-ttu-id="0530d-995">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="0530d-995">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="0530d-996">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数</span><span class="sxs-lookup"><span data-stu-id="0530d-996">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="0530d-997">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="0530d-997">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="0530d-998">修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题</span><span class="sxs-lookup"><span data-stu-id="0530d-998">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="0530d-999">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="0530d-999">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="0530d-1000">实验室</span><span class="sxs-lookup"><span data-stu-id="0530d-1000">Lab</span></span>

* <span data-ttu-id="0530d-1001">为实验室中的环境添加 create、show、delete 和 list 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-1001">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="0530d-1002">添加 show 和 list 命令以查看实验室中的 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="0530d-1002">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="0530d-1003">在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM</span><span class="sxs-lookup"><span data-stu-id="0530d-1003">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="0530d-1004">添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架</span><span class="sxs-lookup"><span data-stu-id="0530d-1004">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="0530d-1005">添加命令以管理实验室中的机密</span><span class="sxs-lookup"><span data-stu-id="0530d-1005">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="0530d-1006">监视</span><span class="sxs-lookup"><span data-stu-id="0530d-1006">Monitor</span></span>

* <span data-ttu-id="0530d-1007">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="0530d-1007">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="0530d-1008">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="0530d-1008">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="0530d-1009">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-1009">Network</span></span>

* <span data-ttu-id="0530d-1010">添加 `network watcher test-connectivity` 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-1010">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="0530d-1011">为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1011">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="0530d-1012">添加对应用程序网关连接排出的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1012">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="0530d-1013">添加对应用程序网关 WAF 规则集配置的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1013">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="0530d-1014">添加对 ExpressRoute 路由筛选器和规则的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1014">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="0530d-1015">添加对 TrafficManager 地理路由的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1015">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="0530d-1016">添加对基于 VPN 连接策略的流量选择器的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1016">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="0530d-1017">添加对 VPN 连接 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1017">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="0530d-1018">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-1018">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="0530d-1019">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1019">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="0530d-1020">从 `network vpn-connection list/show` 命令的输出中删除 null 值</span><span class="sxs-lookup"><span data-stu-id="0530d-1020">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="0530d-1021">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-1021">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="0530d-1022">修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-1022">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="0530d-1023">修复 `dns zone import` 中无法正确导入记录的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-1023">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="0530d-1024">修复 `traffic-manager endpoint update` 不起作用的 bug</span><span class="sxs-lookup"><span data-stu-id="0530d-1024">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="0530d-1025">添加“network watcher”预览命令</span><span class="sxs-lookup"><span data-stu-id="0530d-1025">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="0530d-1026">配置文件</span><span class="sxs-lookup"><span data-stu-id="0530d-1026">Profile</span></span>

* <span data-ttu-id="0530d-1027">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="0530d-1027">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="0530d-1028">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="0530d-1028">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="0530d-1029">Redis</span><span class="sxs-lookup"><span data-stu-id="0530d-1029">Redis</span></span>

* <span data-ttu-id="0530d-1030">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="0530d-1030">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="0530d-1031">弃用“update-settings”命令</span><span class="sxs-lookup"><span data-stu-id="0530d-1031">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="0530d-1032">资源</span><span class="sxs-lookup"><span data-stu-id="0530d-1032">Resource</span></span>

* <span data-ttu-id="0530d-1033">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="0530d-1033">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="0530d-1034">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="0530d-1034">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="0530d-1035">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="0530d-1035">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="0530d-1036">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="0530d-1036">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="0530d-1037">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="0530d-1037">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="0530d-1038">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="0530d-1038">Add docs for az lock update.</span></span> <span data-ttu-id="0530d-1039">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="0530d-1039">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="0530d-1040">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="0530d-1040">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="0530d-1041">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="0530d-1041">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="0530d-1042">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="0530d-1042">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="0530d-1043">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="0530d-1043">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="0530d-1044">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="0530d-1044">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="0530d-1045">角色</span><span class="sxs-lookup"><span data-stu-id="0530d-1045">Role</span></span>

* <span data-ttu-id="0530d-1046">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="0530d-1046">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="0530d-1047">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="0530d-1047">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="0530d-1048">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="0530d-1048">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="0530d-1049">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="0530d-1049">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="0530d-1050">SQL</span><span class="sxs-lookup"><span data-stu-id="0530d-1050">SQL</span></span>

* <span data-ttu-id="0530d-1051">添加了 az sql server list-usages 和 az sql db list-usages 命令</span><span class="sxs-lookup"><span data-stu-id="0530d-1051">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="0530d-1052">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="0530d-1052">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="0530d-1053">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-1053">Storage</span></span>

* <span data-ttu-id="0530d-1054">对于 `storage account create`，将位置默认为资源组位置</span><span class="sxs-lookup"><span data-stu-id="0530d-1054">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="0530d-1055">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1055">Add support for incremental blob copy</span></span>
* <span data-ttu-id="0530d-1056">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="0530d-1056">Add support for large block blob upload</span></span>
* <span data-ttu-id="0530d-1057">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="0530d-1057">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-1058">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-1058">VM</span></span>

* <span data-ttu-id="0530d-1059">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="0530d-1059">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="0530d-1060">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="0530d-1060">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="0530d-1061">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="0530d-1061">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="0530d-1062">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="0530d-1062">az vm/vmss disk</span></span>
  3. <span data-ttu-id="0530d-1063">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="0530d-1063">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="0530d-1064">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="0530d-1064">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="0530d-1065">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="0530d-1065">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="0530d-1066">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="0530d-1066">April 3, 2017</span></span>

<span data-ttu-id="0530d-1067">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="0530d-1067">Version 2.0.2</span></span>

<span data-ttu-id="0530d-1068">此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件</span><span class="sxs-lookup"><span data-stu-id="0530d-1068">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="0530d-1069">核心</span><span class="sxs-lookup"><span data-stu-id="0530d-1069">Core</span></span>

* <span data-ttu-id="0530d-1070">在默认列表中添加了 acr、lab、monitor 和 find 模块</span><span class="sxs-lookup"><span data-stu-id="0530d-1070">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="0530d-1071">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="0530d-1071">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="0530d-1072">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="0530d-1072">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="0530d-1073">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="0530d-1073">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="0530d-1074">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="0530d-1074">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="0530d-1075">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="0530d-1075">Add prompting for missing template parameters.</span></span> <span data-ttu-id="0530d-1076">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="0530d-1076">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="0530d-1077">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="0530d-1077">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="0530d-1078">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="0530d-1078">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="0530d-1079">ACS</span><span class="sxs-lookup"><span data-stu-id="0530d-1079">ACS</span></span>

* <span data-ttu-id="0530d-1080">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="0530d-1080">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="0530d-1081">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="0530d-1081">Add support for ssh key password prompting.</span></span> <span data-ttu-id="0530d-1082">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="0530d-1082">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="0530d-1083">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="0530d-1083">Add support for windows clusters.</span></span> <span data-ttu-id="0530d-1084">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="0530d-1084">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="0530d-1085">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="0530d-1085">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="0530d-1086">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="0530d-1086">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="0530d-1087">应用服务</span><span class="sxs-lookup"><span data-stu-id="0530d-1087">AppService</span></span>

* <span data-ttu-id="0530d-1088">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="0530d-1088">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="0530d-1089">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="0530d-1089">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="0530d-1090">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="0530d-1090">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="0530d-1091">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="0530d-1091">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="0530d-1092">DataLake</span><span class="sxs-lookup"><span data-stu-id="0530d-1092">DataLake</span></span>

* <span data-ttu-id="0530d-1093">Data Lake Analytics 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-1093">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="0530d-1094">Data Lake Store 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="0530d-1094">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="0530d-1095">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="0530d-1095">DocuemntDB</span></span>

* <span data-ttu-id="0530d-1096">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="0530d-1096">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="0530d-1097">VM</span><span class="sxs-lookup"><span data-stu-id="0530d-1097">VM</span></span>

* <span data-ttu-id="0530d-1098">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="0530d-1098">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="0530d-1099">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="0530d-1099">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="0530d-1100">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="0530d-1100">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="0530d-1101">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="0530d-1101">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="0530d-1102">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="0530d-1102">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="0530d-1103">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="0530d-1103">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="0530d-1104">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="0530d-1104">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="0530d-1105">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="0530d-1105">February 27, 2017</span></span>

<span data-ttu-id="0530d-1106">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="0530d-1106">Version 2.0.0</span></span>

<span data-ttu-id="0530d-1107">此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="0530d-1107">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="0530d-1108">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="0530d-1108">Container Service (acs)</span></span>
- <span data-ttu-id="0530d-1109">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="0530d-1109">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="0530d-1110">网络</span><span class="sxs-lookup"><span data-stu-id="0530d-1110">Networking</span></span>
- <span data-ttu-id="0530d-1111">存储</span><span class="sxs-lookup"><span data-stu-id="0530d-1111">Storage</span></span>

<span data-ttu-id="0530d-1112">这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="0530d-1112">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="0530d-1113">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="0530d-1113">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="0530d-1114">若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="0530d-1114">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="0530d-1115">其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="0530d-1115">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="0530d-1116">此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="0530d-1116">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="0530d-1117">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="0530d-1117">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="0530d-1118">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="0530d-1118">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="0530d-1119">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队</span><span class="sxs-lookup"><span data-stu-id="0530d-1119">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="0530d-1120">通过命令行使用 `az feedback` 命令提供反馈</span><span class="sxs-lookup"><span data-stu-id="0530d-1120">Provide feedback from the command line with the `az feedback` command</span></span>

