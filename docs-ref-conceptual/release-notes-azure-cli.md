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
ms.openlocfilehash: 116fa95e51399b9b97c1b35c38445f30db7efc94
ms.sourcegitcommit: fefb5bb6a21cab30c44592c0577408a8d1a2ccc7
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 03/17/2018
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="483b0-103">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="483b0-103">Azure CLI 2.0 release notes</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="483b0-104">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="483b0-104">March 13, 2018</span></span>

<span data-ttu-id="483b0-105">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="483b0-105">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="483b0-106">ACR</span><span class="sxs-lookup"><span data-stu-id="483b0-106">ACR</span></span>

* <span data-ttu-id="483b0-107">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-107">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="483b0-108">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-108">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="483b0-109">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="483b0-109">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-110">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-110">ACS</span></span>

* <span data-ttu-id="483b0-111">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="483b0-111">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="483b0-112">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="483b0-112">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="483b0-113">Advisor</span><span class="sxs-lookup"><span data-stu-id="483b0-113">Advisor</span></span>

* <span data-ttu-id="483b0-114">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="483b0-114">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="483b0-115">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="483b0-115">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="483b0-116">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="483b0-116">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="483b0-117">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-117">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="483b0-118">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-118">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-119">Appservice</span><span class="sxs-lookup"><span data-stu-id="483b0-119">Appservice</span></span>

* <span data-ttu-id="483b0-120">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="483b0-120">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="483b0-121">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="483b0-121">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="483b0-122">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="483b0-122">Eventhubs</span></span>

* <span data-ttu-id="483b0-123">初始版本</span><span class="sxs-lookup"><span data-stu-id="483b0-123">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="483b0-124">Extension</span><span class="sxs-lookup"><span data-stu-id="483b0-124">Extension</span></span>

* <span data-ttu-id="483b0-125">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="483b0-125">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="483b0-126">交互</span><span class="sxs-lookup"><span data-stu-id="483b0-126">Interactive</span></span>

* <span data-ttu-id="483b0-127">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="483b0-127">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="483b0-128">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="483b0-128">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="483b0-129">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="483b0-129">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="483b0-130">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="483b0-130">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-131">Monitor</span><span class="sxs-lookup"><span data-stu-id="483b0-131">Monitor</span></span>

* <span data-ttu-id="483b0-132">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-132">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="483b0-133">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-133">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="483b0-134">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-134">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="483b0-135">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-135">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="483b0-136">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-136">Network</span></span>

* <span data-ttu-id="483b0-137">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-137">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="483b0-138">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="483b0-138">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="483b0-139">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-139">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="483b0-140">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="483b0-140">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-141">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-141">Profile</span></span>

* <span data-ttu-id="483b0-142">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-142">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="483b0-143">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="483b0-143">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="483b0-144">RDBMS</span><span class="sxs-lookup"><span data-stu-id="483b0-144">RDBMS</span></span>

* <span data-ttu-id="483b0-145">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="483b0-145">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="483b0-146">服务总线</span><span class="sxs-lookup"><span data-stu-id="483b0-146">Service Bus</span></span>

* <span data-ttu-id="483b0-147">初始版本</span><span class="sxs-lookup"><span data-stu-id="483b0-147">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-148">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-148">Storage</span></span>

* <span data-ttu-id="483b0-149">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云。</span><span class="sxs-lookup"><span data-stu-id="483b0-149">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds.</span></span>
* <span data-ttu-id="483b0-150">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="483b0-150">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-151">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-151">VM</span></span>

* <span data-ttu-id="483b0-152">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="483b0-152">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="483b0-153">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="483b0-153">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="483b0-154">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="483b0-154">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="483b0-155">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="483b0-155">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="483b0-156">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="483b0-156">February 27, 2018</span></span>

<span data-ttu-id="483b0-157">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="483b0-157">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="483b0-158">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-158">Core</span></span>

* <span data-ttu-id="483b0-159">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="483b0-159">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="483b0-160">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-160">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="483b0-161">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="483b0-161">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-162">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-162">ACS</span></span>

* <span data-ttu-id="483b0-163">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="483b0-163">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="483b0-164">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-164">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="483b0-165">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="483b0-165">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="483b0-166">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="483b0-166">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-167">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-167">Appservice</span></span>

* <span data-ttu-id="483b0-168">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="483b0-168">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="483b0-169">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="483b0-169">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="483b0-170">认知服务</span><span class="sxs-lookup"><span data-stu-id="483b0-170">Cognitive Services</span></span>

* <span data-ttu-id="483b0-171">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="483b0-171">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="483b0-172">消耗</span><span class="sxs-lookup"><span data-stu-id="483b0-172">Consumption</span></span>

* <span data-ttu-id="483b0-173">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="483b0-173">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="483b0-174">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="483b0-174">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="483b0-175">容器</span><span class="sxs-lookup"><span data-stu-id="483b0-175">Container</span></span>

* <span data-ttu-id="483b0-176">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="483b0-176">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="483b0-177">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-177">Network</span></span>

* <span data-ttu-id="483b0-178">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="483b0-178">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-179">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-179">Resource</span></span>

* <span data-ttu-id="483b0-180">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="483b0-180">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="483b0-181">角色</span><span class="sxs-lookup"><span data-stu-id="483b0-181">Role</span></span>

* <span data-ttu-id="483b0-182">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="483b0-182">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-183">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-183">SQL</span></span>

* <span data-ttu-id="483b0-184">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="483b0-184">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-185">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-185">Storage</span></span>

* <span data-ttu-id="483b0-186">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="483b0-186">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-187">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-187">VM</span></span>

* <span data-ttu-id="483b0-188">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-188">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="483b0-189">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="483b0-189">February 13, 2018</span></span>

<span data-ttu-id="483b0-190">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="483b0-190">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="483b0-191">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-191">Core</span></span>

* <span data-ttu-id="483b0-192">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="483b0-192">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-193">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-193">ACS</span></span>

* <span data-ttu-id="483b0-194">[重大更改] 为了准确性已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="483b0-194">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="483b0-195">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="483b0-195">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="483b0-196">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="483b0-196">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="483b0-197">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="483b0-197">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="483b0-198">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="483b0-198">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="483b0-199">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="483b0-199">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="483b0-200">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="483b0-200">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="483b0-201">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="483b0-201">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-202">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-202">Appservice</span></span>

* <span data-ttu-id="483b0-203">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-203">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="483b0-204">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-204">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="483b0-205">CDN</span><span class="sxs-lookup"><span data-stu-id="483b0-205">CDN</span></span>

* <span data-ttu-id="483b0-206">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-206">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="483b0-207">容器</span><span class="sxs-lookup"><span data-stu-id="483b0-207">Container</span></span>

* <span data-ttu-id="483b0-208">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="483b0-208">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="483b0-209">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="483b0-209">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="483b0-210">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="483b0-210">CosmosDB</span></span>

* <span data-ttu-id="483b0-211">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-211">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="483b0-212">分机</span><span class="sxs-lookup"><span data-stu-id="483b0-212">Extension</span></span>

* <span data-ttu-id="483b0-213">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-213">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="483b0-214">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-214">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="483b0-215">反馈</span><span class="sxs-lookup"><span data-stu-id="483b0-215">Feedback</span></span>

* <span data-ttu-id="483b0-216">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="483b0-216">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="483b0-217">交互</span><span class="sxs-lookup"><span data-stu-id="483b0-217">Interactive</span></span>

* <span data-ttu-id="483b0-218">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-218">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="483b0-219">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="483b0-219">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="483b0-220">IoT</span><span class="sxs-lookup"><span data-stu-id="483b0-220">IoT</span></span>

* <span data-ttu-id="483b0-221">修复了成功时 `iot dps access policy [create|update]` 返回“未找到”错误的问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-221">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="483b0-222">修复了成功时 `iot dps linked-hub [create|update]` 返回“未找到”错误的问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-222">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success.</span></span>
* <span data-ttu-id="483b0-223">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="483b0-223">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="483b0-224">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="483b0-224">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-225">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-225">Monitor</span></span>

* <span data-ttu-id="483b0-226">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-226">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="483b0-227">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-227">Network</span></span>

* <span data-ttu-id="483b0-228">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="483b0-228">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="483b0-229">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-229">Profile</span></span>

* <span data-ttu-id="483b0-230">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="483b0-230">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-231">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-231">Resource</span></span>

* <span data-ttu-id="483b0-232">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="483b0-232">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="483b0-233">角色</span><span class="sxs-lookup"><span data-stu-id="483b0-233">Role</span></span>

* <span data-ttu-id="483b0-234">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-234">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-235">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-235">SQL</span></span>

* <span data-ttu-id="483b0-236">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-236">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="483b0-237">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="483b0-237">Added `sql db rename`</span></span>
* <span data-ttu-id="483b0-238">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-238">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-239">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-239">Storage</span></span>

* <span data-ttu-id="483b0-240">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="483b0-240">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-241">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-241">VM</span></span>

* <span data-ttu-id="483b0-242">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="483b0-242">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="483b0-243">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="483b0-243">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="483b0-244">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="483b0-244">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="483b0-245">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="483b0-245">January 31, 2018</span></span>

<span data-ttu-id="483b0-246">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="483b0-246">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="483b0-247">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-247">Core</span></span>

* <span data-ttu-id="483b0-248">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="483b0-248">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="483b0-249">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="483b0-249">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="483b0-250">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="483b0-250">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="483b0-251">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="483b0-251">Use `--verbose` to see</span></span>
* <span data-ttu-id="483b0-252">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="483b0-252">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-253">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-253">ACS</span></span>

* <span data-ttu-id="483b0-254">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-254">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="483b0-255">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="483b0-255">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-256">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-256">Appservice</span></span>

* <span data-ttu-id="483b0-257">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="483b0-257">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="483b0-258">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="483b0-258">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="483b0-259">CDN</span><span class="sxs-lookup"><span data-stu-id="483b0-259">CDN</span></span>

* <span data-ttu-id="483b0-260">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="483b0-260">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="483b0-261">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="483b0-261">CosmosDB</span></span>

* <span data-ttu-id="483b0-262">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="483b0-262">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="483b0-263">交互</span><span class="sxs-lookup"><span data-stu-id="483b0-263">Interactive</span></span>

* <span data-ttu-id="483b0-264">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-264">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="483b0-265">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-265">Network</span></span>

* <span data-ttu-id="483b0-266">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="483b0-266">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="483b0-267">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-267">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="483b0-268">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="483b0-268">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="483b0-269">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="483b0-269">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="483b0-270">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-270">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="483b0-271">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="483b0-271">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="483b0-272">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-272">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="483b0-273">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-273">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="483b0-274">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-274">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="483b0-275">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-275">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-276">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-276">Profile</span></span>

* <span data-ttu-id="483b0-277">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="483b0-277">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-278">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-278">Resource</span></span>

* <span data-ttu-id="483b0-279">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="483b0-279">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-280">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-280">Storage</span></span>

* <span data-ttu-id="483b0-281">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-281">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="483b0-282">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="483b0-282">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="483b0-283">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-283">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="483b0-284">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="483b0-284">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="483b0-285">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-285">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-286">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-286">VM</span></span>

* <span data-ttu-id="483b0-287">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="483b0-287">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="483b0-288">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="483b0-288">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="483b0-289">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-289">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="483b0-290">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="483b0-290">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="483b0-291">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="483b0-291">January 17, 2018</span></span>

<span data-ttu-id="483b0-292">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="483b0-292">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="483b0-293">ACR</span><span class="sxs-lookup"><span data-stu-id="483b0-293">ACR</span></span>

* <span data-ttu-id="483b0-294">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-294">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="483b0-295">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="483b0-295">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-296">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-296">ACS</span></span>

* <span data-ttu-id="483b0-297">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-297">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="483b0-298">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="483b0-298">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-299">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-299">Appservice</span></span>

* <span data-ttu-id="483b0-300">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-300">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="483b0-301">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="483b0-301">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="483b0-302">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="483b0-302">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="483b0-303">备份</span><span class="sxs-lookup"><span data-stu-id="483b0-303">Backup</span></span>

* <span data-ttu-id="483b0-304">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="483b0-304">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="483b0-305">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="483b0-305">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="483b0-306">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="483b0-306">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="483b0-307">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-307">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="483b0-308">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="483b0-308">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="483b0-309">Batch</span><span class="sxs-lookup"><span data-stu-id="483b0-309">Batch</span></span>

* <span data-ttu-id="483b0-310">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="483b0-310">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="483b0-311">云</span><span class="sxs-lookup"><span data-stu-id="483b0-311">Cloud</span></span>

* <span data-ttu-id="483b0-312">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="483b0-312">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="483b0-313">消耗</span><span class="sxs-lookup"><span data-stu-id="483b0-313">Consumption</span></span>

* <span data-ttu-id="483b0-314">添加了用于保留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="483b0-314">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="483b0-315">事件网格</span><span class="sxs-lookup"><span data-stu-id="483b0-315">Event Grid</span></span>

* <span data-ttu-id="483b0-316">[重大更改] 已将 `az eventgrid topic event-subscription` 命令移至 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="483b0-316">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="483b0-317">[重大更改] 已将 `az eventgrid resource event-subscription` 命令移至 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="483b0-317">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="483b0-318">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-318">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="483b0-319">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="483b0-319">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="483b0-320">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="483b0-320">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="483b0-321">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="483b0-321">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="483b0-322">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-322">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="483b0-323">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="483b0-323">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="483b0-324">交互</span><span class="sxs-lookup"><span data-stu-id="483b0-324">Interactive</span></span>

* <span data-ttu-id="483b0-325">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-325">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="483b0-326">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-326">Fixed errors on startup</span></span>
* <span data-ttu-id="483b0-327">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-327">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="483b0-328">IoT</span><span class="sxs-lookup"><span data-stu-id="483b0-328">IoT</span></span>

* <span data-ttu-id="483b0-329">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-329">Added support for device provisioning service</span></span>
* <span data-ttu-id="483b0-330">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="483b0-330">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="483b0-331">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="483b0-331">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-332">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-332">Monitor</span></span>

* <span data-ttu-id="483b0-333">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-333">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="483b0-334">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="483b0-334">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="483b0-335">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="483b0-335">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="483b0-336">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-336">Network</span></span>

* <span data-ttu-id="483b0-337">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-337">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="483b0-338">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-338">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-339">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-339">Profile</span></span>

* <span data-ttu-id="483b0-340">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-340">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="483b0-341">角色</span><span class="sxs-lookup"><span data-stu-id="483b0-341">Role</span></span>

* <span data-ttu-id="483b0-342">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="483b0-342">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="483b0-343">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="483b0-343">Service Fabric</span></span>

* <span data-ttu-id="483b0-344">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="483b0-344">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="483b0-345">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="483b0-345">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-346">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-346">VM</span></span>

* <span data-ttu-id="483b0-347">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="483b0-347">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="483b0-348">[重大更改] 已将单区域 `vmss` 默认值更改为“标准”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="483b0-348">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="483b0-349">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="483b0-349">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="483b0-350">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="483b0-350">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="483b0-351">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-351">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="483b0-352">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-352">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="483b0-353">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="483b0-353">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="483b0-354">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-354">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="483b0-355">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="483b0-355">December 19, 2017</span></span>

<span data-ttu-id="483b0-356">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="483b0-356">Version 2.0.23</span></span>

* <span data-ttu-id="483b0-357">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-357">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="483b0-358">容器</span><span class="sxs-lookup"><span data-stu-id="483b0-358">Container</span></span>

* <span data-ttu-id="483b0-359">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="483b0-359">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="483b0-360">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-360">Network</span></span>

* <span data-ttu-id="483b0-361">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-361">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="483b0-362">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-362">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-363">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-363">Storage</span></span>

* <span data-ttu-id="483b0-364">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-364">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-365">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-365">VM</span></span>

* <span data-ttu-id="483b0-366">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-366">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="483b0-367">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="483b0-367">December 5, 2017</span></span>

<span data-ttu-id="483b0-368">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="483b0-368">Version 2.0.22</span></span>

* <span data-ttu-id="483b0-369">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-369">Removed `az component` commands.</span></span> <span data-ttu-id="483b0-370">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="483b0-370">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="483b0-371">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-371">Core</span></span>
* <span data-ttu-id="483b0-372">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="483b0-372">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="483b0-373">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-373">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-374">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-374">ACS</span></span>

* <span data-ttu-id="483b0-375">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-375">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="483b0-376">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="483b0-376">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="483b0-377">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="483b0-377">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="483b0-378">顾问</span><span class="sxs-lookup"><span data-stu-id="483b0-378">Advisor</span></span>

* <span data-ttu-id="483b0-379">初始版本</span><span class="sxs-lookup"><span data-stu-id="483b0-379">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-380">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-380">Appservice</span></span>

* <span data-ttu-id="483b0-381">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="483b0-381">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="483b0-382">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="483b0-382">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="483b0-383">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="483b0-383">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="483b0-384">消耗</span><span class="sxs-lookup"><span data-stu-id="483b0-384">Consumption</span></span>

* <span data-ttu-id="483b0-385">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-385">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="483b0-386">容器</span><span class="sxs-lookup"><span data-stu-id="483b0-386">Container</span></span>

* <span data-ttu-id="483b0-387">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="483b0-387">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-388">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-388">Monitor</span></span>

* <span data-ttu-id="483b0-389">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="483b0-389">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-390">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-390">Resource</span></span>

* <span data-ttu-id="483b0-391">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-391">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="483b0-392">角色</span><span class="sxs-lookup"><span data-stu-id="483b0-392">Role</span></span>

* <span data-ttu-id="483b0-393">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="483b0-393">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="483b0-394">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="483b0-394">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="483b0-395">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="483b0-395">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-396">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-396">SQL</span></span>

* <span data-ttu-id="483b0-397">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-397">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="483b0-398">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-398">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-399">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-399">VM</span></span>

* <span data-ttu-id="483b0-400">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="483b0-400">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="483b0-401">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="483b0-401">November 14, 2017</span></span>

<span data-ttu-id="483b0-402">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="483b0-402">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="483b0-403">ACR</span><span class="sxs-lookup"><span data-stu-id="483b0-403">ACR</span></span>

* <span data-ttu-id="483b0-404">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-404">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="483b0-405">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-405">ACS</span></span>

* <span data-ttu-id="483b0-406">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="483b0-406">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="483b0-407">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="483b0-407">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="483b0-408">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="483b0-408">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="483b0-409">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="483b0-409">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="483b0-410">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="483b0-410">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-411">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-411">Appservice</span></span>

* <span data-ttu-id="483b0-412">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="483b0-412">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="483b0-413">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="483b0-413">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="483b0-414">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="483b0-414">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="483b0-415">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="483b0-415">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="483b0-416">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-416">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="483b0-417">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="483b0-417">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="483b0-418">Batch</span><span class="sxs-lookup"><span data-stu-id="483b0-418">Batch</span></span>

* <span data-ttu-id="483b0-419">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-419">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="483b0-420">Batchai</span><span class="sxs-lookup"><span data-stu-id="483b0-420">Batchai</span></span>

* <span data-ttu-id="483b0-421">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="483b0-421">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="483b0-422">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="483b0-422">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="483b0-423">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="483b0-423">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="483b0-424">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="483b0-424">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="483b0-425">云</span><span class="sxs-lookup"><span data-stu-id="483b0-425">Cloud</span></span>

* <span data-ttu-id="483b0-426">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="483b0-426">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="483b0-427">容器</span><span class="sxs-lookup"><span data-stu-id="483b0-427">Container</span></span>

* <span data-ttu-id="483b0-428">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-428">Added support to open multiple ports</span></span>
* <span data-ttu-id="483b0-429">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="483b0-429">Added container group restart policy</span></span>
* <span data-ttu-id="483b0-430">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-430">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="483b0-431">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="483b0-431">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="483b0-432">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="483b0-432">Data Lake Analytics</span></span>

* <span data-ttu-id="483b0-433">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="483b0-433">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="483b0-434">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="483b0-434">Data Lake Store</span></span>

* <span data-ttu-id="483b0-435">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="483b0-435">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="483b0-436">分机</span><span class="sxs-lookup"><span data-stu-id="483b0-436">Extension</span></span>

* <span data-ttu-id="483b0-437">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="483b0-437">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="483b0-438">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="483b0-438">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="483b0-439">IoT</span><span class="sxs-lookup"><span data-stu-id="483b0-439">IoT</span></span>

* <span data-ttu-id="483b0-440">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-440">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-441">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-441">Monitor</span></span>

* <span data-ttu-id="483b0-442">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-442">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="483b0-443">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-443">Network</span></span>

* <span data-ttu-id="483b0-444">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-444">Added support for CAA DNS records</span></span>
* <span data-ttu-id="483b0-445">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-445">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="483b0-446">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-446">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="483b0-447">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-447">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="483b0-448">保留</span><span class="sxs-lookup"><span data-stu-id="483b0-448">Reservations</span></span>

* <span data-ttu-id="483b0-449">初始预览版</span><span class="sxs-lookup"><span data-stu-id="483b0-449">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-450">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-450">Resource</span></span>

* <span data-ttu-id="483b0-451">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-451">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-452">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-452">SQL</span></span>

* <span data-ttu-id="483b0-453">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-453">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-454">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-454">Storage</span></span>

* <span data-ttu-id="483b0-455">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="483b0-455">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="483b0-456">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-456">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="483b0-457">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-457">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="483b0-458">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="483b0-458">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="483b0-459">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-459">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="483b0-460">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-460">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="483b0-461">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-461">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-462">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-462">VM</span></span>

* <span data-ttu-id="483b0-463">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-463">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="483b0-464">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-464">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="483b0-465">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-465">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="483b0-466">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="483b0-466">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="483b0-467">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-467">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="483b0-468">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="483b0-468">October 24, 2017</span></span>

<span data-ttu-id="483b0-469">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="483b0-469">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="483b0-470">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-470">Core</span></span>

* <span data-ttu-id="483b0-471">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="483b0-471">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="483b0-472">ACR</span><span class="sxs-lookup"><span data-stu-id="483b0-472">ACR</span></span>

* <span data-ttu-id="483b0-473">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="483b0-473">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="483b0-474">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="483b0-474">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="483b0-475">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="483b0-475">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-476">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-476">ACS</span></span>

* <span data-ttu-id="483b0-477">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-477">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="483b0-478">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="483b0-478">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-479">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-479">Appservice</span></span>

* <span data-ttu-id="483b0-480">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-480">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="483b0-481">组件</span><span class="sxs-lookup"><span data-stu-id="483b0-481">Component</span></span>

* <span data-ttu-id="483b0-482">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="483b0-482">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-483">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-483">Monitor</span></span>

* <span data-ttu-id="483b0-484">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-484">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-485">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-485">Resource</span></span>

* <span data-ttu-id="483b0-486">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-486">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="483b0-487">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="483b0-487">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-488">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-488">VM</span></span>

* <span data-ttu-id="483b0-489">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-489">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="483b0-490">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="483b0-490">October 9, 2017</span></span>

<span data-ttu-id="483b0-491">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="483b0-491">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="483b0-492">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-492">Core</span></span>

* <span data-ttu-id="483b0-493">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="483b0-493">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-494">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-494">Appservice</span></span>

* <span data-ttu-id="483b0-495">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="483b0-495">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="483b0-496">Batch</span><span class="sxs-lookup"><span data-stu-id="483b0-496">Batch</span></span>

* <span data-ttu-id="483b0-497">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="483b0-497">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="483b0-498">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="483b0-498">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="483b0-499">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-499">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="483b0-500">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="483b0-500">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="483b0-501">Batchai</span><span class="sxs-lookup"><span data-stu-id="483b0-501">Batchai</span></span>

* <span data-ttu-id="483b0-502">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="483b0-502">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="483b0-503">KeyVault</span><span class="sxs-lookup"><span data-stu-id="483b0-503">Keyvault</span></span>

* <span data-ttu-id="483b0-504">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-504">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="483b0-505">(#4448)</span><span class="sxs-lookup"><span data-stu-id="483b0-505">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="483b0-506">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-506">Network</span></span>

* <span data-ttu-id="483b0-507">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="483b0-507">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="483b0-508">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="483b0-508">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-509">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-509">Resource</span></span>

* <span data-ttu-id="483b0-510">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-510">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="483b0-511">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="483b0-511">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="483b0-512">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="483b0-512">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="483b0-513">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="483b0-513">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-514">Sql</span><span class="sxs-lookup"><span data-stu-id="483b0-514">Sql</span></span>

* <span data-ttu-id="483b0-515">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-515">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="483b0-516">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="483b0-516">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="483b0-517">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="483b0-517">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-518">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-518">Storage</span></span>

* <span data-ttu-id="483b0-519">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-519">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-520">Vm</span><span class="sxs-lookup"><span data-stu-id="483b0-520">Vm</span></span>

* <span data-ttu-id="483b0-521">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="483b0-521">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="483b0-522">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-522">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="483b0-523">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-523">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="483b0-524">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-524">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="483b0-525">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-525">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="483b0-526">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="483b0-526">September 22, 2017</span></span>

<span data-ttu-id="483b0-527">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="483b0-527">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-528">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-528">Resource</span></span>

* <span data-ttu-id="483b0-529">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-529">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="483b0-530">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="483b0-530">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="483b0-531">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-531">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="483b0-532">[重大更改] 将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="483b0-532">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="483b0-533">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-533">Network</span></span>

* <span data-ttu-id="483b0-534">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-534">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="483b0-535">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-535">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="483b0-536">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="483b0-536">Added `asg` application security group commands</span></span>
* <span data-ttu-id="483b0-537">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-537">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="483b0-538">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-538">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="483b0-539">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-539">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="483b0-540">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-540">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-541">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-541">Storage</span></span>

* <span data-ttu-id="483b0-542">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-542">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="483b0-543">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="483b0-543">Eventgrid</span></span>

* <span data-ttu-id="483b0-544">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="483b0-544">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-545">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-545">SQL</span></span>

* <span data-ttu-id="483b0-546">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="483b0-546">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="483b0-547">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="483b0-547">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="483b0-548">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-548">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="483b0-549">KeyVault</span><span class="sxs-lookup"><span data-stu-id="483b0-549">Keyvault</span></span>

* <span data-ttu-id="483b0-550">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-550">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-551">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-551">VM</span></span>

* <span data-ttu-id="483b0-552">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-552">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="483b0-553">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-553">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="483b0-554">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-554">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="483b0-555">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-555">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="483b0-556">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-556">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="483b0-557">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-557">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-558">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-558">ACS</span></span>

* <span data-ttu-id="483b0-559">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-559">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-560">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-560">Appservice</span></span>

* <span data-ttu-id="483b0-561">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-561">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="483b0-562">备份</span><span class="sxs-lookup"><span data-stu-id="483b0-562">Backup</span></span>

* <span data-ttu-id="483b0-563">预览版</span><span class="sxs-lookup"><span data-stu-id="483b0-563">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="483b0-564">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="483b0-564">September 11, 2017</span></span>

<span data-ttu-id="483b0-565">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="483b0-565">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="483b0-566">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-566">Core</span></span>

* <span data-ttu-id="483b0-567">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="483b0-567">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="483b0-568">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="483b0-568">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-569">Acs</span><span class="sxs-lookup"><span data-stu-id="483b0-569">Acs</span></span>

* <span data-ttu-id="483b0-570">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-570">Added `acs list-locations` command</span></span>
* <span data-ttu-id="483b0-571">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="483b0-571">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-572">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-572">Appservice</span></span>

* <span data-ttu-id="483b0-573">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-573">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="483b0-574">CDN</span><span class="sxs-lookup"><span data-stu-id="483b0-574">CDN</span></span>

* <span data-ttu-id="483b0-575">修复了 `cdn custom-domain create` 的“CustomDomain 不可迭代” bug。</span><span class="sxs-lookup"><span data-stu-id="483b0-575">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`.</span></span>

### <a name="extension"></a><span data-ttu-id="483b0-576">分机</span><span class="sxs-lookup"><span data-stu-id="483b0-576">Extension</span></span>

* <span data-ttu-id="483b0-577">初始版本。</span><span class="sxs-lookup"><span data-stu-id="483b0-577">Initial Release.</span></span>

### <a name="keyvault"></a><span data-ttu-id="483b0-578">KeyVault</span><span class="sxs-lookup"><span data-stu-id="483b0-578">Keyvault</span></span>

* <span data-ttu-id="483b0-579">修复了 `keyvault set-policy` 的权限区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-579">Fixed issue where permissions were case sensitive for `keyvault set-policy`.</span></span>

### <a name="network"></a><span data-ttu-id="483b0-580">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-580">Network</span></span>

* <span data-ttu-id="483b0-581">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="483b0-581">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="483b0-582">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="483b0-582">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="483b0-583">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-583">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="483b0-584">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-584">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="483b0-585">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-585">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-586">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-586">Resource</span></span>

* <span data-ttu-id="483b0-587">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="483b0-587">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="483b0-588">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="483b0-588">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="483b0-589">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="483b0-589">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="483b0-590">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="483b0-590">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-591">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-591">SQL</span></span>

* <span data-ttu-id="483b0-592">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-592">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-593">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-593">VM</span></span>

* <span data-ttu-id="483b0-594">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="483b0-594">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="483b0-595">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="483b0-595">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="483b0-596">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="483b0-596">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="483b0-597">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="483b0-597">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="483b0-598">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="483b0-598">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="483b0-599">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="483b0-599">August 31, 2017</span></span>

<span data-ttu-id="483b0-600">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="483b0-600">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="483b0-601">KeyVault</span><span class="sxs-lookup"><span data-stu-id="483b0-601">Keyvault</span></span>

* <span data-ttu-id="483b0-602">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-602">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="483b0-603">Sf</span><span class="sxs-lookup"><span data-stu-id="483b0-603">Sf</span></span>

* <span data-ttu-id="483b0-604">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="483b0-604">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-605">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-605">Storage</span></span>

* <span data-ttu-id="483b0-606">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-606">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="483b0-607">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="483b0-607">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="483b0-608">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="483b0-608">August 28, 2017</span></span>

<span data-ttu-id="483b0-609">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="483b0-609">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="483b0-610">CLI</span><span class="sxs-lookup"><span data-stu-id="483b0-610">CLI</span></span>

* <span data-ttu-id="483b0-611">在 `--version` 中添加了法律说明。</span><span class="sxs-lookup"><span data-stu-id="483b0-611">Added legal note to `--version`.</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-612">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-612">ACS</span></span>

* <span data-ttu-id="483b0-613">更正了预览区域。</span><span class="sxs-lookup"><span data-stu-id="483b0-613">Corrected preview regions.</span></span>
* <span data-ttu-id="483b0-614">正确设置了默认 `dns_name_prefix` 的格式。</span><span class="sxs-lookup"><span data-stu-id="483b0-614">Formatted default `dns_name_prefix` properly.</span></span>
* <span data-ttu-id="483b0-615">优化了 acs 命令输出。</span><span class="sxs-lookup"><span data-stu-id="483b0-615">Optimized acs command output.</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-616">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-616">Appservice</span></span>

* <span data-ttu-id="483b0-617">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致问题</span><span class="sxs-lookup"><span data-stu-id="483b0-617">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="483b0-618">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="483b0-618">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="483b0-619">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="483b0-619">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="483b0-620">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="483b0-620">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="483b0-621">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="483b0-621">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="483b0-622">IoT</span><span class="sxs-lookup"><span data-stu-id="483b0-622">IoT</span></span>

* <span data-ttu-id="483b0-623">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="483b0-623">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="483b0-624">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-624">Network</span></span>

* <span data-ttu-id="483b0-625">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="483b0-625">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="483b0-626">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="483b0-626">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="483b0-627">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-627">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="483b0-628">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-628">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="483b0-629">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-629">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-630">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-630">Profile</span></span>

* <span data-ttu-id="483b0-631">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="483b0-631">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="483b0-632">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="483b0-632">Service Fabric</span></span>

* <span data-ttu-id="483b0-633">预览版</span><span class="sxs-lookup"><span data-stu-id="483b0-633">Preview release</span></span>
* <span data-ttu-id="483b0-634">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="483b0-634">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="483b0-635">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-635">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="483b0-636">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-636">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-637">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-637">Storage</span></span>

* <span data-ttu-id="483b0-638">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="483b0-638">Enabled setting blob tier</span></span>
* <span data-ttu-id="483b0-639">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="483b0-639">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="483b0-640">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="483b0-640">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="483b0-641">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-641">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="483b0-642">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="483b0-642">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="483b0-643">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="483b0-643">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-644">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-644">VM</span></span>

* <span data-ttu-id="483b0-645">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-645">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="483b0-646">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="483b0-646">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="483b0-647">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="483b0-647">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="483b0-648">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-648">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="483b0-649">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-649">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="483b0-650">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-650">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="483b0-651">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="483b0-651">August 15, 2017</span></span>

<span data-ttu-id="483b0-652">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="483b0-652">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-653">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-653">ACS</span></span>

* <span data-ttu-id="483b0-654">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="483b0-654">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-655">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-655">Appservice</span></span>

* <span data-ttu-id="483b0-656">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-656">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="483b0-657">事件网格</span><span class="sxs-lookup"><span data-stu-id="483b0-657">Event Grid</span></span>

* <span data-ttu-id="483b0-658">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="483b0-658">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="483b0-659">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="483b0-659">August 11, 2017</span></span>

<span data-ttu-id="483b0-660">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="483b0-660">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-661">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-661">ACS</span></span>

* <span data-ttu-id="483b0-662">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="483b0-662">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="483b0-663">Batch</span><span class="sxs-lookup"><span data-stu-id="483b0-663">Batch</span></span>

* <span data-ttu-id="483b0-664">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="483b0-664">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="483b0-665">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="483b0-665">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="483b0-666">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-666">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="483b0-667">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="483b0-667">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="483b0-668">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="483b0-668">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="483b0-669">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="483b0-669">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="483b0-670">组件</span><span class="sxs-lookup"><span data-stu-id="483b0-670">Component</span></span>

* <span data-ttu-id="483b0-671">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="483b0-671">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="483b0-672">容器</span><span class="sxs-lookup"><span data-stu-id="483b0-672">Container</span></span>

* <span data-ttu-id="483b0-673">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-673">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="483b0-674">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="483b0-674">Data Lake Store</span></span>

* <span data-ttu-id="483b0-675">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="483b0-675">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="483b0-676">事件网格</span><span class="sxs-lookup"><span data-stu-id="483b0-676">Event Grid</span></span>

* <span data-ttu-id="483b0-677">初始版本</span><span class="sxs-lookup"><span data-stu-id="483b0-677">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="483b0-678">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-678">Network</span></span>

* <span data-ttu-id="483b0-679">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-679">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="483b0-680">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-680">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="483b0-681">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-681">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="483b0-682">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="483b0-682">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-683">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-683">Profile</span></span>

* <span data-ttu-id="483b0-684">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="483b0-684">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-685">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-685">Storage</span></span>

* <span data-ttu-id="483b0-686">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-686">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-687">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-687">VM</span></span>

* <span data-ttu-id="483b0-688">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="483b0-688">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="483b0-689">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-689">Exposed `list-skus` command</span></span>
* <span data-ttu-id="483b0-690">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="483b0-690">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="483b0-691">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="483b0-691">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="483b0-692">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="483b0-692">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="483b0-693">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="483b0-693">July 28, 2017</span></span>

<span data-ttu-id="483b0-694">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="483b0-694">Version 2.0.12</span></span>

* <span data-ttu-id="483b0-695">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="483b0-695">Added container commands</span></span>
* <span data-ttu-id="483b0-696">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="483b0-696">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="483b0-697">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-697">Core</span></span>

* <span data-ttu-id="483b0-698">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="483b0-698">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="483b0-699">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="483b0-699">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="483b0-700">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="483b0-700">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="483b0-701">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="483b0-701">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="483b0-702">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="483b0-702">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="483b0-703">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="483b0-703">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="483b0-704">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="483b0-704">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="483b0-705">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="483b0-705">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="483b0-706">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="483b0-706">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="483b0-707">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="483b0-707">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="483b0-708">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="483b0-708">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="483b0-709">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="483b0-709">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="483b0-710">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="483b0-710">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="483b0-711">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="483b0-711">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="483b0-712">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="483b0-712">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="483b0-713">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="483b0-713">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="483b0-714">ACR</span><span class="sxs-lookup"><span data-stu-id="483b0-714">ACR</span></span>

* <span data-ttu-id="483b0-715">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-715">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="483b0-716">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="483b0-716">Support SKU update for managed registries</span></span>
* <span data-ttu-id="483b0-717">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="483b0-717">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="483b0-718">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="483b0-718">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="483b0-719">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-719">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="483b0-720">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-720">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-721">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-721">ACS</span></span>

* <span data-ttu-id="483b0-722">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-722">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-723">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-723">Appservice</span></span>

* <span data-ttu-id="483b0-724">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-724">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="483b0-725">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="483b0-725">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="483b0-726">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="483b0-726">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="483b0-727">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="483b0-727">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="483b0-728">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="483b0-728">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="483b0-729">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="483b0-729">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="483b0-730">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="483b0-730">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="483b0-731">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="483b0-731">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="483b0-732">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="483b0-732">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="483b0-733">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="483b0-733">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="483b0-734">Batch</span><span class="sxs-lookup"><span data-stu-id="483b0-734">Batch</span></span>

* <span data-ttu-id="483b0-735">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="483b0-735">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="483b0-736">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="483b0-736">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="483b0-737">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="483b0-737">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="483b0-738">CDN</span><span class="sxs-lookup"><span data-stu-id="483b0-738">CDN</span></span>

* <span data-ttu-id="483b0-739">当 `--profile-name` 指定的配置文件不存在时，针对 `cdn endpoint list` 提供更完善的错误消息。</span><span class="sxs-lookup"><span data-stu-id="483b0-739">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist.</span></span>

### <a name="cloud"></a><span data-ttu-id="483b0-740">云</span><span class="sxs-lookup"><span data-stu-id="483b0-740">Cloud</span></span>

* <span data-ttu-id="483b0-741">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="483b0-741">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="483b0-742">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="483b0-742">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="483b0-743">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="483b0-743">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="483b0-744">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-744">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="483b0-745">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="483b0-745">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="483b0-746">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="483b0-746">CosmosDB</span></span>

* <span data-ttu-id="483b0-747">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-747">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="483b0-748">添加了对集合默认 TTL 的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-748">Added support for collection default TTL.</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="483b0-749">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="483b0-749">Data Lake Analytics</span></span>

* <span data-ttu-id="483b0-750">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="483b0-750">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="483b0-751">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="483b0-751">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="483b0-752">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="483b0-752">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="483b0-753">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="483b0-753">Data Lake Store</span></span>

* <span data-ttu-id="483b0-754">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-754">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="483b0-755">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="483b0-755">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="483b0-756">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="483b0-756">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="483b0-757">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="483b0-757">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="483b0-758">交互</span><span class="sxs-lookup"><span data-stu-id="483b0-758">Interactive</span></span>

* <span data-ttu-id="483b0-759">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="483b0-759">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="483b0-760">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="483b0-760">Increased test coverage</span></span>
* <span data-ttu-id="483b0-761">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="483b0-761">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="483b0-762">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="483b0-762">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="483b0-763">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="483b0-763">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="483b0-764">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="483b0-764">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="483b0-765">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="483b0-765">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="483b0-766">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="483b0-766">Added `--progress` flag</span></span>
* <span data-ttu-id="483b0-767">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="483b0-767">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="483b0-768">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="483b0-768">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="483b0-769">IoT</span><span class="sxs-lookup"><span data-stu-id="483b0-769">IoT</span></span>

* <span data-ttu-id="483b0-770">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-770">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="483b0-771">(#3934)</span><span class="sxs-lookup"><span data-stu-id="483b0-771">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="483b0-772">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="483b0-772">Key vault</span></span>

* <span data-ttu-id="483b0-773">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="483b0-773">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="483b0-774">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="483b0-774">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="483b0-775">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="483b0-775">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="483b0-776">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="483b0-776">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="483b0-777">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="483b0-777">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="483b0-778">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="483b0-778">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="483b0-779">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="483b0-779">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="483b0-780">(#3307)</span><span class="sxs-lookup"><span data-stu-id="483b0-780">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="483b0-781">实验室</span><span class="sxs-lookup"><span data-stu-id="483b0-781">Lab</span></span>

* <span data-ttu-id="483b0-782">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-782">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="483b0-783">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="483b0-783">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-784">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-784">Monitor</span></span>

* <span data-ttu-id="483b0-785">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="483b0-785">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="483b0-786">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="483b0-786">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="483b0-787">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="483b0-787">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="483b0-788">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="483b0-788">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="483b0-789">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="483b0-789">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="483b0-790">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="483b0-790">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="483b0-791">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="483b0-791">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="483b0-792">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="483b0-792">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="483b0-793">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="483b0-793">`location` no longer required</span></span>
  * <span data-ttu-id="483b0-794">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="483b0-794">Add name and ID support for target</span></span>
  * <span data-ttu-id="483b0-795">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="483b0-795">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="483b0-796">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="483b0-796">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="483b0-797">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="483b0-797">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="483b0-798">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="483b0-798">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="483b0-799">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="483b0-799">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="483b0-800">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="483b0-800">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="483b0-801">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-801">Network</span></span>

* <span data-ttu-id="483b0-802">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-802">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="483b0-803">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-803">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="483b0-804">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-804">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="483b0-805">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-805">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="483b0-806">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-806">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="483b0-807">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="483b0-807">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="483b0-808">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="483b0-808">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="483b0-809">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="483b0-809">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="483b0-810">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="483b0-810">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="483b0-811">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="483b0-811">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="483b0-812">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-812">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="483b0-813">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-813">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="483b0-814">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="483b0-814">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="483b0-815">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-815">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="483b0-816">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-816">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="483b0-817">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-817">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="483b0-818">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-818">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="483b0-819">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-819">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="483b0-820">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-820">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="483b0-821">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-821">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="483b0-822">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-822">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="483b0-823">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-823">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="483b0-824">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="483b0-824">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="483b0-825">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="483b0-825">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="483b0-826">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="483b0-826">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="483b0-827">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="483b0-827">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="483b0-828">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="483b0-828">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-829">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-829">Profile</span></span>

* <span data-ttu-id="483b0-830">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="483b0-830">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="483b0-831">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="483b0-831">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="483b0-832">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="483b0-832">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="483b0-833">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="483b0-833">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="483b0-834">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="483b0-834">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="483b0-835">RDBMS</span><span class="sxs-lookup"><span data-stu-id="483b0-835">RDBMS</span></span>

* <span data-ttu-id="483b0-836">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="483b0-836">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="483b0-837">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="483b0-837">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="483b0-838">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="483b0-838">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="483b0-839">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="483b0-839">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-840">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-840">Resource</span></span>

* <span data-ttu-id="483b0-841">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="483b0-841">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="483b0-842">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="483b0-842">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="483b0-843">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="483b0-843">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="483b0-844">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-844">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="483b0-845">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="483b0-845">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="483b0-846">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="483b0-846">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="483b0-847">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="483b0-847">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="483b0-848">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-848">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="483b0-849">角色</span><span class="sxs-lookup"><span data-stu-id="483b0-849">Role</span></span>

* <span data-ttu-id="483b0-850">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="483b0-850">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="483b0-851">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="483b0-851">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="483b0-852">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="483b0-852">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="483b0-853">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="483b0-853">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="483b0-854">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="483b0-854">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="483b0-855">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="483b0-855">Service Fabric</span></span>
* <span data-ttu-id="483b0-856">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="483b0-856">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="483b0-857">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="483b0-857">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="483b0-858">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="483b0-858">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-859">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-859">SQL</span></span>

* <span data-ttu-id="483b0-860">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="483b0-860">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="483b0-861">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="483b0-861">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="483b0-862">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="483b0-862">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-863">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-863">Storage</span></span>

* <span data-ttu-id="483b0-864">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="483b0-864">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="483b0-865">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="483b0-865">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="483b0-866">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="483b0-866">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="483b0-867">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="483b0-867">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="483b0-868">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="483b0-868">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="483b0-869">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="483b0-869">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-870">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-870">VM</span></span>

* <span data-ttu-id="483b0-871">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="483b0-871">Support configuring nsg</span></span>
* <span data-ttu-id="483b0-872">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-872">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="483b0-873">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="483b0-873">Support managed service identities</span></span>
* <span data-ttu-id="483b0-874">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-874">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`.</span></span>
* <span data-ttu-id="483b0-875">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="483b0-875">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="483b0-876">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="483b0-876">May 10, 2017</span></span>

<span data-ttu-id="483b0-877">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="483b0-877">Version 2.0.6</span></span>

* <span data-ttu-id="483b0-878">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="483b0-878">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="483b0-879">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="483b0-879">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="483b0-880">包括 Data Lake Analytics 和 Data Lake Store 模块。</span><span class="sxs-lookup"><span data-stu-id="483b0-880">Include Data Lake Analytics and Data Lake Store modules.</span></span>
* <span data-ttu-id="483b0-881">包括认知服务模块。</span><span class="sxs-lookup"><span data-stu-id="483b0-881">Include Cognitive Services module.</span></span>
* <span data-ttu-id="483b0-882">包括 Service Fabric 模块。</span><span class="sxs-lookup"><span data-stu-id="483b0-882">Include Service Fabric module.</span></span>
* <span data-ttu-id="483b0-883">包括交互式模块（重命名 az-shell）。</span><span class="sxs-lookup"><span data-stu-id="483b0-883">Include Interactive module (rename of az-shell).</span></span>
* <span data-ttu-id="483b0-884">添加对 CDN 命令的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-884">Add support for CDN commands.</span></span>
* <span data-ttu-id="483b0-885">删除容器模块。</span><span class="sxs-lookup"><span data-stu-id="483b0-885">Remove Container module.</span></span>
* <span data-ttu-id="483b0-886">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="483b0-886">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="483b0-887">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="483b0-887">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="483b0-888">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-888">Core</span></span>

* <span data-ttu-id="483b0-889">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="483b0-889">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="483b0-890">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="483b0-890">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="483b0-891">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="483b0-891">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="483b0-892">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="483b0-892">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="483b0-893">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="483b0-893">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="483b0-894">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="483b0-894">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="483b0-895">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="483b0-895">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="483b0-896">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="483b0-896">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="483b0-897">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="483b0-897">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="483b0-898">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="483b0-898">core: Improved performance</span></span>
* <span data-ttu-id="483b0-899">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="483b0-899">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="483b0-900">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="483b0-900">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-901">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-901">ACS</span></span>

* <span data-ttu-id="483b0-902">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="483b0-902">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="483b0-903">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="483b0-903">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="483b0-904">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="483b0-904">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="483b0-905">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="483b0-905">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-906">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-906">AppService</span></span>

* <span data-ttu-id="483b0-907">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="483b0-907">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="483b0-908">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="483b0-908">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="483b0-909">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="483b0-909">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="483b0-910">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="483b0-910">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="483b0-911">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="483b0-911">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="483b0-912">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="483b0-912">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="483b0-913">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="483b0-913">support slot swap with preview</span></span>
* <span data-ttu-id="483b0-914">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="483b0-914">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="483b0-915">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="483b0-915">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="483b0-916">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="483b0-916">CosmosDB</span></span>

* <span data-ttu-id="483b0-917">将 DocumentDB 模块重命名为 CosmosDB。</span><span class="sxs-lookup"><span data-stu-id="483b0-917">Rename documentdb module to cosmosdb.</span></span>
* <span data-ttu-id="483b0-918">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="483b0-918">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="483b0-919">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-919">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="483b0-920">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-920">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="483b0-921">数据湖分析</span><span class="sxs-lookup"><span data-stu-id="483b0-921">Data Lake Analytics</span></span>

* <span data-ttu-id="483b0-922">Bug 修复：在筛选作业结果和状态列表时会引发错误。</span><span class="sxs-lookup"><span data-stu-id="483b0-922">Fix a bug where filtering on result and state for job lists would throw an error.</span></span>
* <span data-ttu-id="483b0-923">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="483b0-923">Add support for new catalog item type: package.</span></span> <span data-ttu-id="483b0-924">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="483b0-924">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="483b0-925">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="483b0-925">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="483b0-926">表</span><span class="sxs-lookup"><span data-stu-id="483b0-926">Table</span></span>
  * <span data-ttu-id="483b0-927">表值函数</span><span class="sxs-lookup"><span data-stu-id="483b0-927">Table valued function</span></span>
  * <span data-ttu-id="483b0-928">查看</span><span class="sxs-lookup"><span data-stu-id="483b0-928">View</span></span>
  * <span data-ttu-id="483b0-929">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="483b0-929">Table Statistics.</span></span> <span data-ttu-id="483b0-930">也可以使用架构列出，但无需指定表名。</span><span class="sxs-lookup"><span data-stu-id="483b0-930">This can also be listed with a schema, but without specifying a table name.</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="483b0-931">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="483b0-931">Data Lake Store</span></span>

* <span data-ttu-id="483b0-932">更新基础文件系统 SDK 版本，可更好地支持处理服务器端限制方案。</span><span class="sxs-lookup"><span data-stu-id="483b0-932">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios.</span></span>
* <span data-ttu-id="483b0-933">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="483b0-933">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="483b0-934">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="483b0-934">missed help for access show.</span></span> <span data-ttu-id="483b0-935">正在添加。</span><span class="sxs-lookup"><span data-stu-id="483b0-935">adding it.</span></span> <span data-ttu-id="483b0-936">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="483b0-936">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="483b0-937">查找</span><span class="sxs-lookup"><span data-stu-id="483b0-937">Find</span></span>

* <span data-ttu-id="483b0-938">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="483b0-938">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="483b0-939">KeyVault</span><span class="sxs-lookup"><span data-stu-id="483b0-939">KeyVault</span></span>

* <span data-ttu-id="483b0-940">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="483b0-940">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="483b0-941">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数。</span><span class="sxs-lookup"><span data-stu-id="483b0-941">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service.</span></span>
* <span data-ttu-id="483b0-942">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="483b0-942">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="483b0-943">解决 `keyvault certificate get-default-policy` 中的问题：“expires”和“not_before”已公开，但“validity_in_months”未公开。</span><span class="sxs-lookup"><span data-stu-id="483b0-943">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not.</span></span>
* <span data-ttu-id="483b0-944">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="483b0-944">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="483b0-945">实验室</span><span class="sxs-lookup"><span data-stu-id="483b0-945">Lab</span></span>

* <span data-ttu-id="483b0-946">针对实验室环境添加 create、show、delete 和 list 命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-946">Adding create, show, delete & list commands for environment in the lab.</span></span>
* <span data-ttu-id="483b0-947">添加 show 和 list 命令，查看实验室中的 ARM 模板。</span><span class="sxs-lookup"><span data-stu-id="483b0-947">Adding show & list commands to view ARM templates in the lab.</span></span>
* <span data-ttu-id="483b0-948">在 `az lab vm list` 中添加 --environment 标志，按实验室环境筛选 VM。</span><span class="sxs-lookup"><span data-stu-id="483b0-948">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab.</span></span>
* <span data-ttu-id="483b0-949">添加 convenience 命令 `az lab formula export-artifacts`，导出实验室公式中的项目基架。</span><span class="sxs-lookup"><span data-stu-id="483b0-949">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula.</span></span>
* <span data-ttu-id="483b0-950">添加命令，管理实验室中的机密。</span><span class="sxs-lookup"><span data-stu-id="483b0-950">Add commands to manage secrets within a Lab.</span></span>

### <a name="monitor"></a><span data-ttu-id="483b0-951">监视</span><span class="sxs-lookup"><span data-stu-id="483b0-951">Monitor</span></span>

* <span data-ttu-id="483b0-952">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="483b0-952">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="483b0-953">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="483b0-953">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="483b0-954">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-954">Network</span></span>

* <span data-ttu-id="483b0-955">添加 `network watcher test-connectivity` 命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-955">Add `network watcher test-connectivity` command.</span></span>
* <span data-ttu-id="483b0-956">添加对 `network watcher packet-capture create` 的 `--filters` 参数的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-956">Add support for `--filters` parameter for `network watcher packet-capture create`.</span></span>
* <span data-ttu-id="483b0-957">添加对应用程序网关连接排出的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-957">Add support for Application Gateway connection draining.</span></span>
* <span data-ttu-id="483b0-958">添加对应用程序网关 WAF 规则集配置的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-958">Add support for Application Gateway WAF rule set configuration.</span></span>
* <span data-ttu-id="483b0-959">添加对 ExpressRoute 路由筛选器和规则的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-959">Add support for ExpressRoute route filters and rules.</span></span>
* <span data-ttu-id="483b0-960">添加对 TrafficManager 地理路由的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-960">Add support for TrafficManager geographic routing.</span></span>
* <span data-ttu-id="483b0-961">添加对基于 VPN 连接策略的流量选择器的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-961">Add support for VPN connection policy-based traffic selectors.</span></span>
* <span data-ttu-id="483b0-962">添加对 VPN 连接 IPSec 策略的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-962">Add support for VPN connection IPSec policies.</span></span>
* <span data-ttu-id="483b0-963">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug。</span><span class="sxs-lookup"><span data-stu-id="483b0-963">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters.</span></span>
* <span data-ttu-id="483b0-964">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-964">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="483b0-965">从 `network vpn-connection list/show` 命令的输出中删除 null 值。</span><span class="sxs-lookup"><span data-stu-id="483b0-965">Remove nulls values from output of `network vpn-connection list/show` commands.</span></span>
* <span data-ttu-id="483b0-966">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="483b0-966">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="483b0-967">Bug 修复：“vpn-connection create”的“--key-length”参数未正确分析。</span><span class="sxs-lookup"><span data-stu-id="483b0-967">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly.</span></span>
* <span data-ttu-id="483b0-968">修复 `dns zone import` 中的 Bug：记录未正确导入。</span><span class="sxs-lookup"><span data-stu-id="483b0-968">Fix bug in `dns zone import` where records were not imported correctly.</span></span>
* <span data-ttu-id="483b0-969">Bug 修复：`traffic-manager endpoint update` 不起作用。</span><span class="sxs-lookup"><span data-stu-id="483b0-969">Fix bug where `traffic-manager endpoint update` did not work.</span></span>
* <span data-ttu-id="483b0-970">添加“network watcher”预览命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-970">Add 'network watcher' preview commands.</span></span>

### <a name="profile"></a><span data-ttu-id="483b0-971">配置文件</span><span class="sxs-lookup"><span data-stu-id="483b0-971">Profile</span></span>

* <span data-ttu-id="483b0-972">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="483b0-972">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="483b0-973">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="483b0-973">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="483b0-974">Redis</span><span class="sxs-lookup"><span data-stu-id="483b0-974">Redis</span></span>

* <span data-ttu-id="483b0-975">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="483b0-975">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="483b0-976">弃用“update-settings”命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-976">Deprecates the 'update-settings' command.</span></span>

### <a name="resource"></a><span data-ttu-id="483b0-977">资源</span><span class="sxs-lookup"><span data-stu-id="483b0-977">Resource</span></span>

* <span data-ttu-id="483b0-978">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="483b0-978">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="483b0-979">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="483b0-979">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="483b0-980">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="483b0-980">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="483b0-981">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="483b0-981">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="483b0-982">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="483b0-982">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="483b0-983">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="483b0-983">Add docs for az lock update.</span></span> <span data-ttu-id="483b0-984">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="483b0-984">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="483b0-985">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="483b0-985">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="483b0-986">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="483b0-986">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="483b0-987">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-987">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="483b0-988">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="483b0-988">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="483b0-989">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="483b0-989">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="483b0-990">角色</span><span class="sxs-lookup"><span data-stu-id="483b0-990">Role</span></span>

* <span data-ttu-id="483b0-991">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="483b0-991">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="483b0-992">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="483b0-992">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="483b0-993">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="483b0-993">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="483b0-994">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="483b0-994">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="483b0-995">SQL</span><span class="sxs-lookup"><span data-stu-id="483b0-995">SQL</span></span>

* <span data-ttu-id="483b0-996">添加了 az sql server list-usages 和 az sql db list-usages 命令。</span><span class="sxs-lookup"><span data-stu-id="483b0-996">Added az sql server list-usages and az sql db list-usages commands.</span></span>
* <span data-ttu-id="483b0-997">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="483b0-997">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="483b0-998">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-998">Storage</span></span>

* <span data-ttu-id="483b0-999">位置默认为 `storage account create` 的资源组位置。</span><span class="sxs-lookup"><span data-stu-id="483b0-999">Default location to resource group location for `storage account create`.</span></span>
* <span data-ttu-id="483b0-1000">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-1000">Add support for incremental blob copy</span></span>
* <span data-ttu-id="483b0-1001">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="483b0-1001">Add support for large block blob upload</span></span>
* <span data-ttu-id="483b0-1002">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="483b0-1002">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-1003">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-1003">VM</span></span>

* <span data-ttu-id="483b0-1004">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="483b0-1004">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="483b0-1005">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="483b0-1005">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="483b0-1006">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="483b0-1006">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="483b0-1007">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="483b0-1007">az vm/vmss disk</span></span>
  3. <span data-ttu-id="483b0-1008">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="483b0-1008">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="483b0-1009">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="483b0-1009">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="483b0-1010">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="483b0-1010">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="483b0-1011">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="483b0-1011">April 3, 2017</span></span>

<span data-ttu-id="483b0-1012">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="483b0-1012">Version 2.0.2</span></span>

<span data-ttu-id="483b0-1013">此版本中已发布 ACR、批处理、KeyVault 和 SQL 组件。</span><span class="sxs-lookup"><span data-stu-id="483b0-1013">We released the ACR, Batch, KeyVault, and SQL components in this release.</span></span>

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

### <a name="core"></a><span data-ttu-id="483b0-1014">核心</span><span class="sxs-lookup"><span data-stu-id="483b0-1014">Core</span></span>

* <span data-ttu-id="483b0-1015">在默认列表中添加了 acr、实验室、监视和查找模块。</span><span class="sxs-lookup"><span data-stu-id="483b0-1015">Add acr, lab, monitor, and find modules to default list.</span></span>
* <span data-ttu-id="483b0-1016">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="483b0-1016">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="483b0-1017">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="483b0-1017">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="483b0-1018">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="483b0-1018">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="483b0-1019">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="483b0-1019">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="483b0-1020">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="483b0-1020">Add prompting for missing template parameters.</span></span> <span data-ttu-id="483b0-1021">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="483b0-1021">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="483b0-1022">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="483b0-1022">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="483b0-1023">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="483b0-1023">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="483b0-1024">ACS</span><span class="sxs-lookup"><span data-stu-id="483b0-1024">ACS</span></span>

* <span data-ttu-id="483b0-1025">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="483b0-1025">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="483b0-1026">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-1026">Add support for ssh key password prompting.</span></span> <span data-ttu-id="483b0-1027">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="483b0-1027">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="483b0-1028">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-1028">Add support for windows clusters.</span></span> <span data-ttu-id="483b0-1029">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="483b0-1029">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="483b0-1030">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="483b0-1030">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="483b0-1031">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="483b0-1031">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="483b0-1032">应用服务</span><span class="sxs-lookup"><span data-stu-id="483b0-1032">AppService</span></span>

* <span data-ttu-id="483b0-1033">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="483b0-1033">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="483b0-1034">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="483b0-1034">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="483b0-1035">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="483b0-1035">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="483b0-1036">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="483b0-1036">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="483b0-1037">DataLake</span><span class="sxs-lookup"><span data-stu-id="483b0-1037">DataLake</span></span>

* <span data-ttu-id="483b0-1038">Data Lake Analytics 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="483b0-1038">Initial release of Data Lake Analytics module.</span></span>
* <span data-ttu-id="483b0-1039">Data Lake Store 模块的初始版本。</span><span class="sxs-lookup"><span data-stu-id="483b0-1039">Initial release of Data Lake Store module.</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="483b0-1040">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="483b0-1040">DocuemntDB</span></span>

* <span data-ttu-id="483b0-1041">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="483b0-1041">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="483b0-1042">VM</span><span class="sxs-lookup"><span data-stu-id="483b0-1042">VM</span></span>

* <span data-ttu-id="483b0-1043">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="483b0-1043">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="483b0-1044">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="483b0-1044">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="483b0-1045">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="483b0-1045">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="483b0-1046">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="483b0-1046">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="483b0-1047">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="483b0-1047">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="483b0-1048">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="483b0-1048">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="483b0-1049">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="483b0-1049">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="483b0-1050">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="483b0-1050">February 27, 2017</span></span>

<span data-ttu-id="483b0-1051">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="483b0-1051">Version 2.0.0</span></span>

<span data-ttu-id="483b0-1052">此版 Azure CLI 2.0 是第一个“正式版”。</span><span class="sxs-lookup"><span data-stu-id="483b0-1052">This release of Azure CLI 2.0 is the first "Generally Available" release.</span></span>
<span data-ttu-id="483b0-1053">正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="483b0-1053">General availability applies to these command modules:</span></span>
- <span data-ttu-id="483b0-1054">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="483b0-1054">Container Service (acs)</span></span>
- <span data-ttu-id="483b0-1055">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="483b0-1055">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="483b0-1056">网络</span><span class="sxs-lookup"><span data-stu-id="483b0-1056">Networking</span></span>
- <span data-ttu-id="483b0-1057">存储</span><span class="sxs-lookup"><span data-stu-id="483b0-1057">Storage</span></span>

<span data-ttu-id="483b0-1058">这些命令模块可在生产环境中使用，并受标准 Microsoft SLA 的支持。</span><span class="sxs-lookup"><span data-stu-id="483b0-1058">These command modules can be used in production and are supported by standard Microsoft SLA.</span></span>
<span data-ttu-id="483b0-1059">可以直接向 Microsoft 支持部门或者通过 [github 问题列表](https://github.com/azure/azure-cli/issues/)提出问题。</span><span class="sxs-lookup"><span data-stu-id="483b0-1059">You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/).</span></span>
<span data-ttu-id="483b0-1060">可以[在 StackOverflow 上使用 azure-cli 标记](http://stackoverflow.com/questions/tagged/azure-cli)或者通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队来提出问题。可以通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="483b0-1060">You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com). You can provide feedback from the command line with the `az feedback` command.</span></span>

<span data-ttu-id="483b0-1061">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本的后续发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="483b0-1061">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI.</span></span>

<span data-ttu-id="483b0-1062">若要检查 CLI 版本，请使用 `az --version`。</span><span class="sxs-lookup"><span data-stu-id="483b0-1062">To verify the version of the CLI, use `az --version`.</span></span>
<span data-ttu-id="483b0-1063">输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="483b0-1063">The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using.</span></span>

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
> <span data-ttu-id="483b0-1064">某些命令模块带有“b*n*”或“rc*n*”后缀。</span><span class="sxs-lookup"><span data-stu-id="483b0-1064">Some of the command modules have a "b*n*" or "rc*n*" postfix.</span></span>
> <span data-ttu-id="483b0-1065">这些命令模块仍以预览版提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="483b0-1065">These command modules are still in preview and will become generally available in the future.</span></span>

<span data-ttu-id="483b0-1066">此外，我们还提供 CLI 夜间预览版。</span><span class="sxs-lookup"><span data-stu-id="483b0-1066">We also have nightly preview builds of the CLI.</span></span>
<span data-ttu-id="483b0-1067">有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="483b0-1067">For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup).</span></span>

<span data-ttu-id="483b0-1068">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="483b0-1068">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="483b0-1069">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="483b0-1069">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="483b0-1070">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。</span><span class="sxs-lookup"><span data-stu-id="483b0-1070">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com).</span></span>
- <span data-ttu-id="483b0-1071">请通过命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="483b0-1071">Provide feedback from the command line with the `az feedback` command.</span></span>

