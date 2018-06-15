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
ms.openlocfilehash: 72e667d74ff8d55f26ecbf3b3c8845c9c03b56be
ms.sourcegitcommit: 5c80e96e96f9608c92a94fa4a9c4afb25099f3fc
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 06/13/2018
ms.locfileid: "35512897"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="d681e-103">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="d681e-103">Azure CLI 2.0 release notes</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="d681e-104">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d681e-104">June 13, 2018</span></span>

<span data-ttu-id="d681e-105">版本 2.0.36</span><span class="sxs-lookup"><span data-stu-id="d681e-105">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="d681e-106">AKS</span><span class="sxs-lookup"><span data-stu-id="d681e-106">AKS</span></span>

* <span data-ttu-id="d681e-107">为 `aks create` 添加了高级网络选项</span><span class="sxs-lookup"><span data-stu-id="d681e-107">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="d681e-108">为 `aks create` 添加了参数以启用监视和 HTTP 路由</span><span class="sxs-lookup"><span data-stu-id="d681e-108">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span> 
* <span data-ttu-id="d681e-109">为 `aks create` 添加了 `--no-ssh-key` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-109">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="d681e-110">为 `aks create` 添加了 `--enable-rbac` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-110">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="d681e-111">[PREVIEW] 为 `aks create` 添加了对 Azure Active Directory 身份验证的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-111">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-112">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-112">AppService</span></span>

* <span data-ttu-id="d681e-113">修复了不兼容 urllib 版本的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-113">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="d681e-114">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="d681e-114">June 5, 2018</span></span>

<span data-ttu-id="d681e-115">版本 2.0.35</span><span class="sxs-lookup"><span data-stu-id="d681e-115">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-116">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-116">Interactive</span></span>

* <span data-ttu-id="d681e-117">添加了对交互模式的依赖项的限制</span><span class="sxs-lookup"><span data-stu-id="d681e-117">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="d681e-118">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="d681e-118">June 5, 2018</span></span>

<span data-ttu-id="d681e-119">版本 2.0.34</span><span class="sxs-lookup"><span data-stu-id="d681e-119">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="d681e-120">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-120">Core</span></span>

* <span data-ttu-id="d681e-121">增加了对跨租户资源引用的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-121">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="d681e-122">增强了遥测数据上传可靠性</span><span class="sxs-lookup"><span data-stu-id="d681e-122">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-123">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-123">ACR</span></span>

* <span data-ttu-id="d681e-124">增加了对 VSTS 充当远程源位置的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-124">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="d681e-125">添加了 `acr import` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-125">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="d681e-126">AKS</span><span class="sxs-lookup"><span data-stu-id="d681e-126">AKS</span></span>

* <span data-ttu-id="d681e-127">更改了 `aks get-credentials`，可以使用更安全的文件系统权限来创建 kube 配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-127">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="d681e-128">Batch</span><span class="sxs-lookup"><span data-stu-id="d681e-128">Batch</span></span>

* <span data-ttu-id="d681e-129">修复了池列表表格式设置中的 Bug [[问题 #4378](https://github.com/Azure/azure-cli/issues/4378)]</span><span class="sxs-lookup"><span data-stu-id="d681e-129">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="d681e-130">IOT</span><span class="sxs-lookup"><span data-stu-id="d681e-130">IOT</span></span>

* <span data-ttu-id="d681e-131">增加了对创建基本层 IoT 中心的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-131">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="d681e-132">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-132">Network</span></span>

* <span data-ttu-id="d681e-133">改进了 `network vnet peering`</span><span class="sxs-lookup"><span data-stu-id="d681e-133">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="d681e-134">策略见解</span><span class="sxs-lookup"><span data-stu-id="d681e-134">Policy Insights</span></span>

* <span data-ttu-id="d681e-135">初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-135">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="d681e-136">ARM</span><span class="sxs-lookup"><span data-stu-id="d681e-136">ARM</span></span>

* <span data-ttu-id="d681e-137">增加了 `account management-group` 命令。</span><span class="sxs-lookup"><span data-stu-id="d681e-137">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-138">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-138">SQL</span></span>

* <span data-ttu-id="d681e-139">增加了新的托管实例命令：</span><span class="sxs-lookup"><span data-stu-id="d681e-139">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="d681e-140">增加了新的托管数据库命令：</span><span class="sxs-lookup"><span data-stu-id="d681e-140">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="d681e-141">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-141">Storage</span></span>

* <span data-ttu-id="d681e-142">增加了可以从文件扩展名推断且适用于 json 和 javascript 的额外 mimetype</span><span class="sxs-lookup"><span data-stu-id="d681e-142">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-143">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-143">VM</span></span>

* <span data-ttu-id="d681e-144">更改了 `vm list-skus`，可以使用固定列并可添加表明要删除 `Tier` 和 `Size` 的警告</span><span class="sxs-lookup"><span data-stu-id="d681e-144">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="d681e-145">为 `vm create` 添加了 `--accelerated-networking` 选项</span><span class="sxs-lookup"><span data-stu-id="d681e-145">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="d681e-146">为 `identity create` 添加了 `--tags`</span><span class="sxs-lookup"><span data-stu-id="d681e-146">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="d681e-147">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d681e-147">May 22, 2018</span></span>

<span data-ttu-id="d681e-148">版本 2.0.33</span><span class="sxs-lookup"><span data-stu-id="d681e-148">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="d681e-149">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-149">Core</span></span>

* <span data-ttu-id="d681e-150">增加了对在文件名中扩展 `@` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-150">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-151">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-151">ACS</span></span>

* <span data-ttu-id="d681e-152">增加了新的 Dev-Spaces 命令：`aks use-dev-spaces` 和 `aks remove-dev-spaces`</span><span class="sxs-lookup"><span data-stu-id="d681e-152">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="d681e-153">修复了帮助消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="d681e-153">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-154">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-154">AppService</span></span>

* <span data-ttu-id="d681e-155">改进了泛型更新命令</span><span class="sxs-lookup"><span data-stu-id="d681e-155">Improved generic update commands</span></span>
* <span data-ttu-id="d681e-156">增加了对 `webapp deployment source config-zip` 的异步支持</span><span class="sxs-lookup"><span data-stu-id="d681e-156">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="d681e-157">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-157">Container</span></span>

* <span data-ttu-id="d681e-158">增加了对以 yaml 格式导出容器组的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-158">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="d681e-159">增加了对使用 yaml 文件创建/更新容器组的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-159">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-160">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-160">Extension</span></span>

* <span data-ttu-id="d681e-161">改进了扩展的删除方式</span><span class="sxs-lookup"><span data-stu-id="d681e-161">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-162">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-162">Interactive</span></span>

* <span data-ttu-id="d681e-163">更改了日志记录，在完成时将分析器静音</span><span class="sxs-lookup"><span data-stu-id="d681e-163">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="d681e-164">改进了错误的帮助缓存的处理</span><span class="sxs-lookup"><span data-stu-id="d681e-164">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="d681e-165">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d681e-165">KeyVault</span></span>

* <span data-ttu-id="d681e-166">修复了 keyvault 命令，使之可以在 Cloud Shell 或 VM 中与标识一起使用</span><span class="sxs-lookup"><span data-stu-id="d681e-166">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="d681e-167">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-167">Network</span></span>

* <span data-ttu-id="d681e-168">修复了 `network watcher show-topology` 无法与 vnet 和/或子网名称一起使用的问题 [#6326](https://github.com/Azure/azure-cli/issues/6326)</span><span class="sxs-lookup"><span data-stu-id="d681e-168">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="d681e-169">修复了某些 `network watcher` 命令宣称未为区域启用网络观察程序而实际上却已经启用的问题 [#6264](https://github.com/Azure/azure-cli/issues/6264)</span><span class="sxs-lookup"><span data-stu-id="d681e-169">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-170">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-170">SQL</span></span>

* <span data-ttu-id="d681e-171">[重大更改] 更改了从 `db` 和 `dw` 命令返回的响应对象：</span><span class="sxs-lookup"><span data-stu-id="d681e-171">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="d681e-172">已将 `serviceLevelObjective` 属性重命名为 `currentServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="d681e-172">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="d681e-173">删除了 `currentServiceObjectiveId` 和 `requestedServiceObjectiveId` 属性</span><span class="sxs-lookup"><span data-stu-id="d681e-173">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span> 
    * <span data-ttu-id="d681e-174">已将 `maxSizeBytes` 属性更改为整数值而不是字符串</span><span class="sxs-lookup"><span data-stu-id="d681e-174">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="d681e-175">[重大更改] 已将下面的 `db` 和 `dw` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="d681e-175">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="d681e-176">`requestedServiceObjectiveName`。</span><span class="sxs-lookup"><span data-stu-id="d681e-176">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="d681e-177">若要更新，请使用 `--service-objective` 参数或设置 `sku.name` 属性</span><span class="sxs-lookup"><span data-stu-id="d681e-177">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="d681e-178">`edition`。</span><span class="sxs-lookup"><span data-stu-id="d681e-178">`edition`.</span></span> <span data-ttu-id="d681e-179">若要更新，请使用 `--edition` 参数或设置 `sku.tier` 属性</span><span class="sxs-lookup"><span data-stu-id="d681e-179">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="d681e-180">`elasticPoolName`。</span><span class="sxs-lookup"><span data-stu-id="d681e-180">`elasticPoolName`.</span></span> <span data-ttu-id="d681e-181">若要更新，请使用 `--elastic-pool` 参数或设置 `elasticPoolId` 属性</span><span class="sxs-lookup"><span data-stu-id="d681e-181">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="d681e-182">[重大更改] 已将下面的 `elastic-pool` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="d681e-182">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="d681e-183">`edition`。</span><span class="sxs-lookup"><span data-stu-id="d681e-183">`edition`.</span></span> <span data-ttu-id="d681e-184">若要更新，请使用 `--edition` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-184">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="d681e-185">`dtu`。</span><span class="sxs-lookup"><span data-stu-id="d681e-185">`dtu`.</span></span> <span data-ttu-id="d681e-186">若要更新，请使用 `--capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-186">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="d681e-187">`databaseDtuMin`。</span><span class="sxs-lookup"><span data-stu-id="d681e-187">`databaseDtuMin`.</span></span> <span data-ttu-id="d681e-188">若要更新，请使用 `--db-min-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-188">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="d681e-189">`databaseDtuMax`。</span><span class="sxs-lookup"><span data-stu-id="d681e-189">`databaseDtuMax`.</span></span> <span data-ttu-id="d681e-190">若要更新，请使用 `--db-max-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-190">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="d681e-191">为 `db`、`dw` 和 `elastic-pool` 命令增加了 `--family` 和 `--capacity` 参数。</span><span class="sxs-lookup"><span data-stu-id="d681e-191">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="d681e-192">为 `db`、`dw` 和 `elastic-pool` 命令增加了表格式化程序。</span><span class="sxs-lookup"><span data-stu-id="d681e-192">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-193">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-193">Storage</span></span>

* <span data-ttu-id="d681e-194">增加了 `--account-name` 参数的补全选项</span><span class="sxs-lookup"><span data-stu-id="d681e-194">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="d681e-195">修复了 `storage entity query` 的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-195">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-196">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-196">VM</span></span>

* <span data-ttu-id="d681e-197">[重大更改] 从 `vm create` 中删除了 `--write-accelerator`。</span><span class="sxs-lookup"><span data-stu-id="d681e-197">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="d681e-198">可以通过 `vm update` 或 `vm disk attach` 访问同一支持</span><span class="sxs-lookup"><span data-stu-id="d681e-198">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="d681e-199">修复了 `[vm|vmss] extension` 中的扩展映像匹配问题</span><span class="sxs-lookup"><span data-stu-id="d681e-199">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="d681e-200">为 `vm create` 添加了 `--boot-diagnostics-storage`，可以捕获启动日志</span><span class="sxs-lookup"><span data-stu-id="d681e-200">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="d681e-201">为 `[vm|vmss] update` 添加了 `--license-type`</span><span class="sxs-lookup"><span data-stu-id="d681e-201">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="d681e-202">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="d681e-202">May 7, 2018</span></span>

<span data-ttu-id="d681e-203">版本 2.0.32</span><span class="sxs-lookup"><span data-stu-id="d681e-203">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="d681e-204">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-204">Core</span></span>

* <span data-ttu-id="d681e-205">修复了使用证书从服务主体帐户检索机密时引发未处理异常的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-205">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="d681e-206">增加了对位置参数的有限支持</span><span class="sxs-lookup"><span data-stu-id="d681e-206">Added limited support for positional arguments</span></span>
* <span data-ttu-id="d681e-207">修复了 `--query` 无法与 `--ids` 一起使用的问题。</span><span class="sxs-lookup"><span data-stu-id="d681e-207">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="d681e-208">#5591</span><span class="sxs-lookup"><span data-stu-id="d681e-208">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="d681e-209">改进了使用 `--ids` 时通过命令执行的管道方案。</span><span class="sxs-lookup"><span data-stu-id="d681e-209">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="d681e-210">支持在指定查询的情况下使用 `-o tsv`，或者在不指定查询的情况下使用 `-o json`</span><span class="sxs-lookup"><span data-stu-id="d681e-210">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="d681e-211">增加了在用户的命令中存在拼写错误的情况下，针对错误提供命令建议的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-211">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="d681e-212">改进了用户键入 `az ''` 时出现的错误</span><span class="sxs-lookup"><span data-stu-id="d681e-212">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="d681e-213">增加了针对命令模块和扩展自定义资源类型的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-213">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-214">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-214">ACR</span></span>

* <span data-ttu-id="d681e-215">增加了 ACR 生成命令</span><span class="sxs-lookup"><span data-stu-id="d681e-215">Added ACR Build commands</span></span>
* <span data-ttu-id="d681e-216">改进了“找不到资源”类型的错误消息</span><span class="sxs-lookup"><span data-stu-id="d681e-216">Improved resource not found error messages</span></span>
* <span data-ttu-id="d681e-217">改进了资源创建性能和错误处理</span><span class="sxs-lookup"><span data-stu-id="d681e-217">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="d681e-218">改进了 acr 登录非标准控制台和 WSL</span><span class="sxs-lookup"><span data-stu-id="d681e-218">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="d681e-219">改进了存储库命令错误消息</span><span class="sxs-lookup"><span data-stu-id="d681e-219">Improved repository commands error messages</span></span>
* <span data-ttu-id="d681e-220">更新了表列和排序</span><span class="sxs-lookup"><span data-stu-id="d681e-220">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-221">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-221">ACS</span></span>

* <span data-ttu-id="d681e-222">增加了“`az aks` 是预览版服务”警告</span><span class="sxs-lookup"><span data-stu-id="d681e-222">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="d681e-223">修复了未指定 `--aci-resource-group` 时 `aks install-connector` 中的权限问题</span><span class="sxs-lookup"><span data-stu-id="d681e-223">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="d681e-224">AMS</span><span class="sxs-lookup"><span data-stu-id="d681e-224">AMS</span></span>

* <span data-ttu-id="d681e-225">初始版本 - 管理 Azure 媒体服务资源</span><span class="sxs-lookup"><span data-stu-id="d681e-225">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-226">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-226">Appservice</span></span>

* <span data-ttu-id="d681e-227">修复了提供 `--slot` 时 `webapp delete` 中的 Bug</span><span class="sxs-lookup"><span data-stu-id="d681e-227">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="d681e-228">从 `webapp auth update` 删除了 `--runtime-version`</span><span class="sxs-lookup"><span data-stu-id="d681e-228">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="d681e-229">增加了对 min\_tls\_version & https2.0 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-229">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="d681e-230">增加了对多容器的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-230">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="d681e-231">Batch AI</span><span class="sxs-lookup"><span data-stu-id="d681e-231">Batch AI</span></span>

* <span data-ttu-id="d681e-232">更改了 `batchai create cluster`，以便遵循在群集的配置文件中配置的 VM 优先级</span><span class="sxs-lookup"><span data-stu-id="d681e-232">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="d681e-233">认知服务</span><span class="sxs-lookup"><span data-stu-id="d681e-233">Cognitive Services</span></span>

* <span data-ttu-id="d681e-234">修复了在 `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603) 的示例中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="d681e-234">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="d681e-235">消耗</span><span class="sxs-lookup"><span data-stu-id="d681e-235">Consumption</span></span>

* <span data-ttu-id="d681e-236">增加了预算 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="d681e-236">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="d681e-237">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-237">Container</span></span>

* <span data-ttu-id="d681e-238">删除了在映像名称中包括注册表服务器时对 `container create` 命令的 `--registry-server` 参数的要求</span><span class="sxs-lookup"><span data-stu-id="d681e-238">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="d681e-239">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d681e-239">Cosmos DB</span></span>

* <span data-ttu-id="d681e-240">引入针对 Azure CLI 的 VNET 支持 - Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="d681e-240">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="d681e-241">DMS</span><span class="sxs-lookup"><span data-stu-id="d681e-241">DMS</span></span>

* <span data-ttu-id="d681e-242">初始版本 - 为 Azure SQL 迁移方案增加了对 SQL 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-242">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-243">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-243">Extension</span></span>

* <span data-ttu-id="d681e-244">修复了停止显示扩展元数据的 Bug</span><span class="sxs-lookup"><span data-stu-id="d681e-244">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-245">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-245">Interactive</span></span>

* <span data-ttu-id="d681e-246">允许交互式补全选项使用位置参数</span><span class="sxs-lookup"><span data-stu-id="d681e-246">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="d681e-247">增强用户键入 '\' 时的输出的用户友好性</span><span class="sxs-lookup"><span data-stu-id="d681e-247">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="d681e-248">修复了在没有帮助的情况下参数的补全问题</span><span class="sxs-lookup"><span data-stu-id="d681e-248">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="d681e-249">修复了命令组的说明问题</span><span class="sxs-lookup"><span data-stu-id="d681e-249">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="d681e-250">实验室</span><span class="sxs-lookup"><span data-stu-id="d681e-250">Lab</span></span>

* <span data-ttu-id="d681e-251">修复了 Knack 转换的回归问题</span><span class="sxs-lookup"><span data-stu-id="d681e-251">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="d681e-252">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-252">Network</span></span>

* <span data-ttu-id="d681e-253">[重大更改] 删除了以下项的 `--ids` 参数：</span><span class="sxs-lookup"><span data-stu-id="d681e-253">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span> 
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="d681e-254">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-254">Profile</span></span>

* <span data-ttu-id="d681e-255">修复了 `disk create` 源检测问题</span><span class="sxs-lookup"><span data-stu-id="d681e-255">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="d681e-256">[重大更改] 删除了不再使用的 `--msi-port` 和 `--identity-port`</span><span class="sxs-lookup"><span data-stu-id="d681e-256">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="d681e-257">修复了 `account get-access-token` 短摘要中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="d681e-257">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="d681e-258">Redis</span><span class="sxs-lookup"><span data-stu-id="d681e-258">Redis</span></span>

* <span data-ttu-id="d681e-259">弃用 `redis patch-schedule patch-schedule show` 而改用 `redis patch-schedule show`</span><span class="sxs-lookup"><span data-stu-id="d681e-259">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="d681e-260">弃用 `redis list-all`。</span><span class="sxs-lookup"><span data-stu-id="d681e-260">Deprecated `redis list-all`.</span></span> <span data-ttu-id="d681e-261">此功能已加入 `redis list` 中</span><span class="sxs-lookup"><span data-stu-id="d681e-261">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="d681e-262">弃用 `redis import-method` 而改用 `redis import`</span><span class="sxs-lookup"><span data-stu-id="d681e-262">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="d681e-263">为各种命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-263">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="d681e-264">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-264">Role</span></span>

* <span data-ttu-id="d681e-265">[重大更改] 删除了已弃用的 `ad sp reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="d681e-265">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-266">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-266">Storage</span></span>

* <span data-ttu-id="d681e-267">在源 SAS 和帐户密钥未指定的情况下，允许将目标 SAS 令牌应用到源，以便进行 Blob 复制</span><span class="sxs-lookup"><span data-stu-id="d681e-267">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="d681e-268">公开了用于 Blob 上传和下载的 --socket-timeout 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-268">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="d681e-269">将以路径分隔符开头的 Blob 名称视为相对路径</span><span class="sxs-lookup"><span data-stu-id="d681e-269">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="d681e-270">允许 `storage blob copy --source-sas` 以查询字符“?”开头</span><span class="sxs-lookup"><span data-stu-id="d681e-270">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="d681e-271">修复了 `storage entity query --marker` 问题，接受“键=值”列表</span><span class="sxs-lookup"><span data-stu-id="d681e-271">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-272">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-272">VM</span></span>

* <span data-ttu-id="d681e-273">修复了非托管 Blob URI 上的检测逻辑无效的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-273">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="d681e-274">增加了在没有用户提供的服务主体的情况下进行磁盘加密的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-274">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="d681e-275">[重大更改] 请勿使用 VM“ManagedIdentityExtension”来寻求 MSI 支持</span><span class="sxs-lookup"><span data-stu-id="d681e-275">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="d681e-276">增加了对 `vmss` 使用逐出策略的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-276">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="d681e-277">[重大更改] 从以下项删除了 `--ids`：</span><span class="sxs-lookup"><span data-stu-id="d681e-277">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="d681e-278">增加了写入加速器支持</span><span class="sxs-lookup"><span data-stu-id="d681e-278">Added write accelerator support</span></span> 
* <span data-ttu-id="d681e-279">添加了 `vmss perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="d681e-279">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="d681e-280">修复了 `vm diagnostics set` 问题，可以可靠地检测 VM 的 OS 类型</span><span class="sxs-lookup"><span data-stu-id="d681e-280">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="d681e-281">更改了 `vm resize`，系统会检查请求的大小是否不同于当前设置的大小，只在二者有变化时进行更新</span><span class="sxs-lookup"><span data-stu-id="d681e-281">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="d681e-282">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="d681e-282">April 10, 2018</span></span>

<span data-ttu-id="d681e-283">版本 2.0.31</span><span class="sxs-lookup"><span data-stu-id="d681e-283">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-284">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-284">ACR</span></span>

* <span data-ttu-id="d681e-285">改进了 wincred 回退错误处理</span><span class="sxs-lookup"><span data-stu-id="d681e-285">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-286">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-286">ACS</span></span>

* <span data-ttu-id="d681e-287">更改了 aks 创建的 SPN，使其有效期达到 5 年</span><span class="sxs-lookup"><span data-stu-id="d681e-287">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-288">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-288">Appservice</span></span>

* [重大更改]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="d681e-290">修复了 Web 应用计划不存在导致的未捕获异常</span><span class="sxs-lookup"><span data-stu-id="d681e-290">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="d681e-291">BatchAI</span><span class="sxs-lookup"><span data-stu-id="d681e-291">BatchAI</span></span>

* <span data-ttu-id="d681e-292">添加了对 2018-03-01 API 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-292">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="d681e-293">作业级装载</span><span class="sxs-lookup"><span data-stu-id="d681e-293">Job level mounting</span></span>
 - <span data-ttu-id="d681e-294">使用机密值的环境变量</span><span class="sxs-lookup"><span data-stu-id="d681e-294">Environment variables with secret values</span></span>
 - <span data-ttu-id="d681e-295">性能计数器设置</span><span class="sxs-lookup"><span data-stu-id="d681e-295">Performance counters settings</span></span>
 - <span data-ttu-id="d681e-296">报告作业特定的路径段</span><span class="sxs-lookup"><span data-stu-id="d681e-296">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="d681e-297">支持“列出文件”API 中的子文件夹</span><span class="sxs-lookup"><span data-stu-id="d681e-297">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="d681e-298">使用情况和限制报告</span><span class="sxs-lookup"><span data-stu-id="d681e-298">Usage and limits reporting</span></span>
 - <span data-ttu-id="d681e-299">允许为 NFS 服务器指定缓存类型</span><span class="sxs-lookup"><span data-stu-id="d681e-299">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="d681e-300">支持自定义映像</span><span class="sxs-lookup"><span data-stu-id="d681e-300">Support for custom images</span></span>
 - <span data-ttu-id="d681e-301">添加了 pyTorch 工具包支持</span><span class="sxs-lookup"><span data-stu-id="d681e-301">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="d681e-302">添加了 `job wait` 命令，以允许等待作业完成和报告作业退出代码</span><span class="sxs-lookup"><span data-stu-id="d681e-302">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="d681e-303">添加了 `usage show` 命令，用于列出不同区域的当前 Batch AI 资源使用情况和限制</span><span class="sxs-lookup"><span data-stu-id="d681e-303">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="d681e-304">支持国家云</span><span class="sxs-lookup"><span data-stu-id="d681e-304">National clouds are supported</span></span>
* <span data-ttu-id="d681e-305">添加了作业命令行参数，以便除了装载配置文件以外，还能装载作业级别的文件系统</span><span class="sxs-lookup"><span data-stu-id="d681e-305">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="d681e-306">添加了更多选项用于自定义群集 - VM 优先级、子网、自动缩放群集的初始节点计数，以及指定自定义映像</span><span class="sxs-lookup"><span data-stu-id="d681e-306">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="d681e-307">添加了命令行选项用于指定 Batch AI 托管 NFS 的缓存类型</span><span class="sxs-lookup"><span data-stu-id="d681e-307">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="d681e-308">简化了在配置文件中指定装载文件系统的方法。</span><span class="sxs-lookup"><span data-stu-id="d681e-308">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="d681e-309">现在，可以省略 Azure 文件共享和 Azure Blob 容器的凭据 - CLI 将会使用通过命令行参数提供的或通过环境变量指定的存储帐户密钥来填充缺少的凭据，或者从 Azure 存储查询密钥（如果存储帐户属于当前订阅）</span><span class="sxs-lookup"><span data-stu-id="d681e-309">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="d681e-310">作业完成后（成功、失败、已终止或已删除），作业文件流命令现在会自动完成</span><span class="sxs-lookup"><span data-stu-id="d681e-310">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="d681e-311">改进了 `show` 操作的 `table` 输出</span><span class="sxs-lookup"><span data-stu-id="d681e-311">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="d681e-312">添加了 `--use-auto-storage` 选项用于创建群集。</span><span class="sxs-lookup"><span data-stu-id="d681e-312">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="d681e-313">使用此选项可以更方便地管理存储帐户，以及将 Azure 文件共享和 Azure Blob 容器装载到群集</span><span class="sxs-lookup"><span data-stu-id="d681e-313">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="d681e-314">为 `cluster create` 和 `file-server create` 添加了 `--generate-ssh-keys` 选项</span><span class="sxs-lookup"><span data-stu-id="d681e-314">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="d681e-315">添加了通过命令行提供节点设置任务的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-315">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="d681e-316">[重大更改]移动了 `job file` 组下面的 `job stream-file` 和 `job list-files` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-316">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="d681e-317">[重大更改]已将 `file-server create` 命令中的 `--admin-user-name` 重命名为 `--user-name`，使其与 `cluster create` 命令一致</span><span class="sxs-lookup"><span data-stu-id="d681e-317">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="d681e-318">计费</span><span class="sxs-lookup"><span data-stu-id="d681e-318">Billing</span></span>

* <span data-ttu-id="d681e-319">添加了登记帐户命令</span><span class="sxs-lookup"><span data-stu-id="d681e-319">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="d681e-320">消耗</span><span class="sxs-lookup"><span data-stu-id="d681e-320">Consumption</span></span>

* <span data-ttu-id="d681e-321">添加了 `marketplace` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-321">Added `marketplace` commands</span></span>
* <span data-ttu-id="d681e-322">[重大更改] 已将 `reservations summaries` 重命名为 `reservation summary`</span><span class="sxs-lookup"><span data-stu-id="d681e-322">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="d681e-323">[重大更改] 已将 `reservations details` 重命名为 `reservation detail`</span><span class="sxs-lookup"><span data-stu-id="d681e-323">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="d681e-324">[重大更改]删除了 `reservation` 命令的 `--reservation-order-id` 和 `--reservation-id` 短选项</span><span class="sxs-lookup"><span data-stu-id="d681e-324">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="d681e-325">[重大更改]删除了 `reservation summary` 命令的 `--grain` 短选项</span><span class="sxs-lookup"><span data-stu-id="d681e-325">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="d681e-326">[重大更改]删除了 `pricesheet` 命令的 `--include-meter-details` 短选项</span><span class="sxs-lookup"><span data-stu-id="d681e-326">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="d681e-327">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-327">Container</span></span>

* <span data-ttu-id="d681e-328">添加了 git 存储库卷装载参数 `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` 和 `--gitrepo-mount-path`</span><span class="sxs-lookup"><span data-stu-id="d681e-328">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="d681e-329">修复了 [#5926](https://github.com/Azure/azure-cli/issues/5926)：指定 --container-name 时 `az container exec` 失败</span><span class="sxs-lookup"><span data-stu-id="d681e-329">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-330">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-330">Extension</span></span>

* <span data-ttu-id="d681e-331">已将分配检查消息更改为调试级别</span><span class="sxs-lookup"><span data-stu-id="d681e-331">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-332">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-332">Interactive</span></span>

* <span data-ttu-id="d681e-333">更改为在命令不可识别时停止完成</span><span class="sxs-lookup"><span data-stu-id="d681e-333">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="d681e-334">添加了创建命令子树之前和之后所用的事件挂钩</span><span class="sxs-lookup"><span data-stu-id="d681e-334">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="d681e-335">添加了 `--ids` 参数补全</span><span class="sxs-lookup"><span data-stu-id="d681e-335">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="d681e-336">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-336">Network</span></span>

* <span data-ttu-id="d681e-337">修复了 [#5936](https://github.com/Azure/azure-cli/issues/5936)：无法设置 `application-gateway create` 标记</span><span class="sxs-lookup"><span data-stu-id="d681e-337">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="d681e-338">添加了参数 `--auth-certs`，以附加 `application-gateway http-settings [create|update]` 的身份验证证书。</span><span class="sxs-lookup"><span data-stu-id="d681e-338">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="d681e-339">#4910</span><span class="sxs-lookup"><span data-stu-id="d681e-339">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="d681e-340">添加了 `ddos-protection` 命令用于创建 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="d681e-340">Added `ddos-protection` commands to create DDoS protection plans</span></span> 
* <span data-ttu-id="d681e-341">为 `vnet [create|update]` 添加了 `--ddos-protection-plan` 支持，以便将 VNet 关联到 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="d681e-341">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="d681e-342">修复了 `network route-table [create|update]` 中 `--disable-bgp-route-propagation` 标志的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-342">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="d681e-343">删除了 `network lb [create|update]` 的虚拟参数 `--public-ip-address-type` 和 `--subnet-type`</span><span class="sxs-lookup"><span data-stu-id="d681e-343">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="d681e-344">为 `network dns zone [import|export]` 和 `network dns record-set txt add-record` 添加了采用 RFC 1035 转义序列的 TXT 记录支持</span><span class="sxs-lookup"><span data-stu-id="d681e-344">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-345">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-345">Profile</span></span>

* <span data-ttu-id="d681e-346">在 `account list` 中添加了 Azure 经典帐户支持</span><span class="sxs-lookup"><span data-stu-id="d681e-346">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="d681e-347">[重大更改]删除了 `--msi` & `--msi-port` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-347">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="d681e-348">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d681e-348">RDBMS</span></span>

* <span data-ttu-id="d681e-349">添加了 `georestore` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-349">Added `georestore` command</span></span>
* <span data-ttu-id="d681e-350">删除了 `create` 命令的存储大小限制</span><span class="sxs-lookup"><span data-stu-id="d681e-350">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-351">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-351">Resource</span></span>

* <span data-ttu-id="d681e-352">在 `policy definition create` 中添加了对 `--metadata` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-352">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="d681e-353">为 `policy definition update` 添加了对 `--metadata`、`--set`、`--add` 和 `--remove` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-353">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-354">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-354">SQL</span></span>

* <span data-ttu-id="d681e-355">添加了 `sql elastic-pool op list` 和 `sql elastic-pool op cancel`</span><span class="sxs-lookup"><span data-stu-id="d681e-355">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-356">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-356">Storage</span></span>

* <span data-ttu-id="d681e-357">改进了有关连接字符串格式不当的错误消息</span><span class="sxs-lookup"><span data-stu-id="d681e-357">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-358">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-358">VM</span></span>

* <span data-ttu-id="d681e-359">为 `vmss create` 添加了配置平台容错域计数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-359">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="d681e-360">已将 `vmss create` 的默认值更改为区域性、大型或禁用单一位置组的规模集的标准负载均衡器</span><span class="sxs-lookup"><span data-stu-id="d681e-360">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大更改]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="d681e-362">为 `vm create` 添加了对公共 IP SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-362">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="d681e-363">为 `vm secret format` 添加了 `--keyvault` 和 `--resource-group` 参数，以便在命令无法解析保管库 ID 的情况下提供支持。</span><span class="sxs-lookup"><span data-stu-id="d681e-363">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="d681e-364">#5718</span><span class="sxs-lookup"><span data-stu-id="d681e-364">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="d681e-365">改进了当资源组的位置不支持区域时，`[vm|vmss create]` 发生的错误</span><span class="sxs-lookup"><span data-stu-id="d681e-365">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="d681e-366">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d681e-366">March 27, 2018</span></span>

<span data-ttu-id="d681e-367">版本 2.0.30</span><span class="sxs-lookup"><span data-stu-id="d681e-367">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="d681e-368">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-368">Core</span></span>

* <span data-ttu-id="d681e-369">为帮助中标记为预览版的扩展显示消息</span><span class="sxs-lookup"><span data-stu-id="d681e-369">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-370">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-370">ACS</span></span>

* <span data-ttu-id="d681e-371">为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误</span><span class="sxs-lookup"><span data-stu-id="d681e-371">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-372">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-372">Appservice</span></span>

* <span data-ttu-id="d681e-373">为 `webapp update` 添加了仅限 HTTPS 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-373">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="d681e-374">为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-374">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="d681e-375">备份</span><span class="sxs-lookup"><span data-stu-id="d681e-375">Backup</span></span>

* <span data-ttu-id="d681e-376">添加了新命令 `az backup protection isenabled-for-vm`。</span><span class="sxs-lookup"><span data-stu-id="d681e-376">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="d681e-377">此命令可用于检查 VM 是否已由订阅中的任何保管库备份</span><span class="sxs-lookup"><span data-stu-id="d681e-377">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="d681e-378">为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="d681e-378">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="d681e-379">更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="d681e-379">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="d681e-380">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-380">Container</span></span>

* <span data-ttu-id="d681e-381">添加了 `container exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="d681e-381">Added `container exec` command.</span></span> <span data-ttu-id="d681e-382">在正在运行的容器组的容器中执行命令</span><span class="sxs-lookup"><span data-stu-id="d681e-382">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="d681e-383">允许将表输出用于创建和更新容器组</span><span class="sxs-lookup"><span data-stu-id="d681e-383">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-384">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-384">Extension</span></span>

* <span data-ttu-id="d681e-385">为 `extension add` 添加了消息（如果扩展处于预览状态）</span><span class="sxs-lookup"><span data-stu-id="d681e-385">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="d681e-386">更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据</span><span class="sxs-lookup"><span data-stu-id="d681e-386">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="d681e-387">[重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据</span><span class="sxs-lookup"><span data-stu-id="d681e-387">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-388">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-388">Interactive</span></span>

* <span data-ttu-id="d681e-389">已将“完成”更改为在执行命令表加载后立即激活</span><span class="sxs-lookup"><span data-stu-id="d681e-389">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="d681e-390">修复了使用 `--style` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-390">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="d681e-391">交互式词法分析器在命令表转储后实例化（如果缺失）</span><span class="sxs-lookup"><span data-stu-id="d681e-391">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="d681e-392">改进了完成符支持</span><span class="sxs-lookup"><span data-stu-id="d681e-392">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="d681e-393">实验室</span><span class="sxs-lookup"><span data-stu-id="d681e-393">Lab</span></span>

* <span data-ttu-id="d681e-394">修复了 `create environment` 命令的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-394">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-395">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-395">Monitor</span></span>

* <span data-ttu-id="d681e-396">为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="d681e-396">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="d681e-397">修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表</span><span class="sxs-lookup"><span data-stu-id="d681e-397">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="d681e-398">为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="d681e-398">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="d681e-399">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-399">Network</span></span>

* <span data-ttu-id="d681e-400">添加了对专用 DNS 区域的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-400">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-401">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-401">Profile</span></span>

* <span data-ttu-id="d681e-402">为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告</span><span class="sxs-lookup"><span data-stu-id="d681e-402">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="d681e-403">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d681e-403">RDBMS</span></span>

* <span data-ttu-id="d681e-404">添加了业务模型 GA API 版本 2017-12-01</span><span class="sxs-lookup"><span data-stu-id="d681e-404">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-405">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-405">Resource</span></span>

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="d681e-407">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-407">Role</span></span>

* <span data-ttu-id="d681e-408">为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-408">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="d681e-409">更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID</span><span class="sxs-lookup"><span data-stu-id="d681e-409">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="d681e-410">添加了凭据管理命令 `ad sp credential [reset|list|delete]`</span><span class="sxs-lookup"><span data-stu-id="d681e-410">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="d681e-411">[重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”</span><span class="sxs-lookup"><span data-stu-id="d681e-411">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="d681e-412">为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-412">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-413">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-413">Storage</span></span>

* <span data-ttu-id="d681e-414">修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-414">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="d681e-415">修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-415">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-416">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-416">VM</span></span>

* <span data-ttu-id="d681e-417">针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告</span><span class="sxs-lookup"><span data-stu-id="d681e-417">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="d681e-418">为 `vm [snapshot|image]` 添加了区域弹性支持</span><span class="sxs-lookup"><span data-stu-id="d681e-418">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="d681e-419">更改了磁盘实例视图以更好地报告加密状态</span><span class="sxs-lookup"><span data-stu-id="d681e-419">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="d681e-420">[重大更改] 更改了 `vm extension delete` 以不再返回输出</span><span class="sxs-lookup"><span data-stu-id="d681e-420">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="d681e-421">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d681e-421">March 13, 2018</span></span>

<span data-ttu-id="d681e-422">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="d681e-422">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-423">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-423">ACR</span></span>

* <span data-ttu-id="d681e-424">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-424">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="d681e-425">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-425">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="d681e-426">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="d681e-426">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-427">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-427">ACS</span></span>

* <span data-ttu-id="d681e-428">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="d681e-428">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="d681e-429">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="d681e-429">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="d681e-430">顾问</span><span class="sxs-lookup"><span data-stu-id="d681e-430">Advisor</span></span>

* <span data-ttu-id="d681e-431">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="d681e-431">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="d681e-432">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="d681e-432">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="d681e-433">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="d681e-433">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span> 
* <span data-ttu-id="d681e-434">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-434">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="d681e-435">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-435">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-436">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-436">Appservice</span></span>

* <span data-ttu-id="d681e-437">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="d681e-437">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="d681e-438">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="d681e-438">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="d681e-439">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="d681e-439">Eventhubs</span></span>

* <span data-ttu-id="d681e-440">初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-440">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-441">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-441">Extension</span></span>

* <span data-ttu-id="d681e-442">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="d681e-442">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-443">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-443">Interactive</span></span>

* <span data-ttu-id="d681e-444">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="d681e-444">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="d681e-445">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="d681e-445">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="d681e-446">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="d681e-446">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="d681e-447">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="d681e-447">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-448">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-448">Monitor</span></span>

* <span data-ttu-id="d681e-449">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-449">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="d681e-450">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-450">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="d681e-451">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-451">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="d681e-452">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-452">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="d681e-453">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-453">Network</span></span>

* <span data-ttu-id="d681e-454">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-454">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="d681e-455">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="d681e-455">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="d681e-456">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-456">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="d681e-457">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="d681e-457">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-458">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-458">Profile</span></span>

* <span data-ttu-id="d681e-459">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-459">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="d681e-460">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="d681e-460">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="d681e-461">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d681e-461">RDBMS</span></span>

* <span data-ttu-id="d681e-462">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="d681e-462">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="d681e-463">服务总线</span><span class="sxs-lookup"><span data-stu-id="d681e-463">Service Bus</span></span>

* <span data-ttu-id="d681e-464">初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-464">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-465">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-465">Storage</span></span>

* <span data-ttu-id="d681e-466">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云</span><span class="sxs-lookup"><span data-stu-id="d681e-466">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="d681e-467">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="d681e-467">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-468">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-468">VM</span></span>

* <span data-ttu-id="d681e-469">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="d681e-469">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="d681e-470">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="d681e-470">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="d681e-471">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="d681e-471">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="d681e-472">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="d681e-472">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="d681e-473">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d681e-473">February 27, 2018</span></span>

<span data-ttu-id="d681e-474">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="d681e-474">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="d681e-475">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-475">Core</span></span>

* <span data-ttu-id="d681e-476">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="d681e-476">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="d681e-477">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-477">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="d681e-478">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="d681e-478">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-479">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-479">ACS</span></span>

* <span data-ttu-id="d681e-480">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="d681e-480">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="d681e-481">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-481">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="d681e-482">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="d681e-482">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="d681e-483">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="d681e-483">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-484">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-484">Appservice</span></span>

* <span data-ttu-id="d681e-485">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="d681e-485">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="d681e-486">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="d681e-486">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="d681e-487">认知服务</span><span class="sxs-lookup"><span data-stu-id="d681e-487">Cognitive Services</span></span>

* <span data-ttu-id="d681e-488">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="d681e-488">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="d681e-489">消耗</span><span class="sxs-lookup"><span data-stu-id="d681e-489">Consumption</span></span>

* <span data-ttu-id="d681e-490">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="d681e-490">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="d681e-491">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="d681e-491">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="d681e-492">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-492">Container</span></span>

* <span data-ttu-id="d681e-493">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="d681e-493">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="d681e-494">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-494">Network</span></span>

* <span data-ttu-id="d681e-495">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="d681e-495">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-496">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-496">Resource</span></span>

* <span data-ttu-id="d681e-497">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="d681e-497">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="d681e-498">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-498">Role</span></span>

* <span data-ttu-id="d681e-499">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="d681e-499">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-500">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-500">SQL</span></span>

* <span data-ttu-id="d681e-501">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="d681e-501">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-502">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-502">Storage</span></span>

* <span data-ttu-id="d681e-503">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="d681e-503">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-504">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-504">VM</span></span>

* <span data-ttu-id="d681e-505">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-505">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="d681e-506">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="d681e-506">February 13, 2018</span></span>

<span data-ttu-id="d681e-507">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="d681e-507">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="d681e-508">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-508">Core</span></span>

* <span data-ttu-id="d681e-509">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="d681e-509">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-510">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-510">ACS</span></span>

* <span data-ttu-id="d681e-511">[重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="d681e-511">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="d681e-512">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="d681e-512">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="d681e-513">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="d681e-513">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="d681e-514">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="d681e-514">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="d681e-515">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="d681e-515">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="d681e-516">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="d681e-516">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="d681e-517">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="d681e-517">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="d681e-518">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="d681e-518">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-519">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-519">Appservice</span></span>

* <span data-ttu-id="d681e-520">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-520">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="d681e-521">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-521">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="d681e-522">CDN</span><span class="sxs-lookup"><span data-stu-id="d681e-522">CDN</span></span>

* <span data-ttu-id="d681e-523">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-523">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="d681e-524">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-524">Container</span></span>

* <span data-ttu-id="d681e-525">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="d681e-525">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="d681e-526">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="d681e-526">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d681e-527">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d681e-527">CosmosDB</span></span>

* <span data-ttu-id="d681e-528">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-528">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-529">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-529">Extension</span></span>

* <span data-ttu-id="d681e-530">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-530">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="d681e-531">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-531">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="d681e-532">反馈</span><span class="sxs-lookup"><span data-stu-id="d681e-532">Feedback</span></span>

* <span data-ttu-id="d681e-533">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="d681e-533">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-534">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-534">Interactive</span></span>

* <span data-ttu-id="d681e-535">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-535">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="d681e-536">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="d681e-536">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="d681e-537">IoT</span><span class="sxs-lookup"><span data-stu-id="d681e-537">IoT</span></span>

* <span data-ttu-id="d681e-538">修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-538">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="d681e-539">修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-539">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="d681e-540">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="d681e-540">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="d681e-541">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="d681e-541">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-542">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-542">Monitor</span></span>

* <span data-ttu-id="d681e-543">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-543">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="d681e-544">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-544">Network</span></span>

* <span data-ttu-id="d681e-545">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="d681e-545">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="d681e-546">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-546">Profile</span></span>

* <span data-ttu-id="d681e-547">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="d681e-547">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-548">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-548">Resource</span></span>

* <span data-ttu-id="d681e-549">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="d681e-549">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="d681e-550">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-550">Role</span></span>

* <span data-ttu-id="d681e-551">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-551">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-552">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-552">SQL</span></span>

* <span data-ttu-id="d681e-553">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-553">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="d681e-554">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="d681e-554">Added `sql db rename`</span></span>
* <span data-ttu-id="d681e-555">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-555">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-556">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-556">Storage</span></span>

* <span data-ttu-id="d681e-557">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="d681e-557">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-558">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-558">VM</span></span>

* <span data-ttu-id="d681e-559">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="d681e-559">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="d681e-560">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="d681e-560">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="d681e-561">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="d681e-561">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="d681e-562">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="d681e-562">January 31, 2018</span></span>

<span data-ttu-id="d681e-563">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="d681e-563">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="d681e-564">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-564">Core</span></span>

* <span data-ttu-id="d681e-565">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="d681e-565">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="d681e-566">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="d681e-566">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="d681e-567">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="d681e-567">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="d681e-568">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="d681e-568">Use `--verbose` to see</span></span>
* <span data-ttu-id="d681e-569">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="d681e-569">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-570">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-570">ACS</span></span>

* <span data-ttu-id="d681e-571">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-571">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="d681e-572">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="d681e-572">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-573">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-573">Appservice</span></span>

* <span data-ttu-id="d681e-574">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="d681e-574">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="d681e-575">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="d681e-575">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="d681e-576">CDN</span><span class="sxs-lookup"><span data-stu-id="d681e-576">CDN</span></span>

* <span data-ttu-id="d681e-577">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="d681e-577">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d681e-578">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d681e-578">CosmosDB</span></span>

* <span data-ttu-id="d681e-579">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="d681e-579">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-580">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-580">Interactive</span></span>

* <span data-ttu-id="d681e-581">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-581">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="d681e-582">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-582">Network</span></span>

* <span data-ttu-id="d681e-583">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="d681e-583">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="d681e-584">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-584">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="d681e-585">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="d681e-585">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="d681e-586">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="d681e-586">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="d681e-587">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-587">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="d681e-588">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="d681e-588">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="d681e-589">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-589">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="d681e-590">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-590">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="d681e-591">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-591">Fixed issue where certain records were imported twice with `dns zone import`</span></span> 
* <span data-ttu-id="d681e-592">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-592">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-593">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-593">Profile</span></span>

* <span data-ttu-id="d681e-594">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="d681e-594">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-595">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-595">Resource</span></span>

* <span data-ttu-id="d681e-596">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="d681e-596">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-597">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-597">Storage</span></span>

* <span data-ttu-id="d681e-598">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-598">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="d681e-599">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="d681e-599">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="d681e-600">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-600">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>  
* <span data-ttu-id="d681e-601">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="d681e-601">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="d681e-602">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-602">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-603">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-603">VM</span></span>

* <span data-ttu-id="d681e-604">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="d681e-604">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="d681e-605">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="d681e-605">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="d681e-606">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-606">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="d681e-607">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="d681e-607">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="d681e-608">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="d681e-608">January 17, 2018</span></span>

<span data-ttu-id="d681e-609">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="d681e-609">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-610">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-610">ACR</span></span>

* <span data-ttu-id="d681e-611">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-611">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="d681e-612">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="d681e-612">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-613">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-613">ACS</span></span>

* <span data-ttu-id="d681e-614">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-614">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="d681e-615">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="d681e-615">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-616">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-616">Appservice</span></span>

* <span data-ttu-id="d681e-617">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-617">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="d681e-618">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="d681e-618">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="d681e-619">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="d681e-619">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="d681e-620">备份</span><span class="sxs-lookup"><span data-stu-id="d681e-620">Backup</span></span>

* <span data-ttu-id="d681e-621">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="d681e-621">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="d681e-622">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="d681e-622">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="d681e-623">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="d681e-623">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="d681e-624">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-624">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="d681e-625">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="d681e-625">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="d681e-626">Batch</span><span class="sxs-lookup"><span data-stu-id="d681e-626">Batch</span></span>

* <span data-ttu-id="d681e-627">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="d681e-627">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="d681e-628">云</span><span class="sxs-lookup"><span data-stu-id="d681e-628">Cloud</span></span>

* <span data-ttu-id="d681e-629">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="d681e-629">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="d681e-630">消耗</span><span class="sxs-lookup"><span data-stu-id="d681e-630">Consumption</span></span>

* <span data-ttu-id="d681e-631">添加了用于预留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="d681e-631">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="d681e-632">事件网格</span><span class="sxs-lookup"><span data-stu-id="d681e-632">Event Grid</span></span>

* <span data-ttu-id="d681e-633">[重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="d681e-633">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="d681e-634">[重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="d681e-634">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="d681e-635">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="d681e-635">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="d681e-636">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="d681e-636">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="d681e-637">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="d681e-637">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="d681e-638">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="d681e-638">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="d681e-639">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-639">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="d681e-640">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="d681e-640">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-641">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-641">Interactive</span></span>

* <span data-ttu-id="d681e-642">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-642">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="d681e-643">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-643">Fixed errors on startup</span></span>
* <span data-ttu-id="d681e-644">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-644">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="d681e-645">IoT</span><span class="sxs-lookup"><span data-stu-id="d681e-645">IoT</span></span>

* <span data-ttu-id="d681e-646">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-646">Added support for device provisioning service</span></span>
* <span data-ttu-id="d681e-647">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="d681e-647">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="d681e-648">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="d681e-648">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-649">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-649">Monitor</span></span>

* <span data-ttu-id="d681e-650">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="d681e-650">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="d681e-651">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="d681e-651">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="d681e-652">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="d681e-652">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="d681e-653">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-653">Network</span></span>

* <span data-ttu-id="d681e-654">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-654">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="d681e-655">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-655">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-656">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-656">Profile</span></span>

* <span data-ttu-id="d681e-657">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-657">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="d681e-658">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-658">Role</span></span>

* <span data-ttu-id="d681e-659">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="d681e-659">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d681e-660">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d681e-660">Service Fabric</span></span>

* <span data-ttu-id="d681e-661">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="d681e-661">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="d681e-662">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="d681e-662">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-663">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-663">VM</span></span>

* <span data-ttu-id="d681e-664">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="d681e-664">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="d681e-665">[重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="d681e-665">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="d681e-666">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="d681e-666">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="d681e-667">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="d681e-667">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="d681e-668">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-668">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="d681e-669">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-669">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="d681e-670">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="d681e-670">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="d681e-671">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-671">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="d681e-672">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="d681e-672">December 19, 2017</span></span>

<span data-ttu-id="d681e-673">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="d681e-673">Version 2.0.23</span></span>

* <span data-ttu-id="d681e-674">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-674">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="d681e-675">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-675">Container</span></span>

* <span data-ttu-id="d681e-676">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="d681e-676">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="d681e-677">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-677">Network</span></span>

* <span data-ttu-id="d681e-678">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-678">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="d681e-679">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-679">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-680">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-680">Storage</span></span>

* <span data-ttu-id="d681e-681">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-681">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-682">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-682">VM</span></span>

* <span data-ttu-id="d681e-683">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-683">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="d681e-684">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="d681e-684">December 5, 2017</span></span>

<span data-ttu-id="d681e-685">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="d681e-685">Version 2.0.22</span></span>

* <span data-ttu-id="d681e-686">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="d681e-686">Removed `az component` commands.</span></span> <span data-ttu-id="d681e-687">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="d681e-687">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="d681e-688">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-688">Core</span></span>
* <span data-ttu-id="d681e-689">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="d681e-689">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="d681e-690">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-690">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-691">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-691">ACS</span></span>

* <span data-ttu-id="d681e-692">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-692">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="d681e-693">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="d681e-693">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="d681e-694">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="d681e-694">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="d681e-695">顾问</span><span class="sxs-lookup"><span data-stu-id="d681e-695">Advisor</span></span>

* <span data-ttu-id="d681e-696">初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-696">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-697">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-697">Appservice</span></span>

* <span data-ttu-id="d681e-698">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="d681e-698">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="d681e-699">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="d681e-699">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="d681e-700">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="d681e-700">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="d681e-701">消耗</span><span class="sxs-lookup"><span data-stu-id="d681e-701">Consumption</span></span>

* <span data-ttu-id="d681e-702">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-702">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="d681e-703">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-703">Container</span></span>

* <span data-ttu-id="d681e-704">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="d681e-704">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-705">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-705">Monitor</span></span>

* <span data-ttu-id="d681e-706">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="d681e-706">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-707">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-707">Resource</span></span>

* <span data-ttu-id="d681e-708">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-708">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="d681e-709">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-709">Role</span></span>

* <span data-ttu-id="d681e-710">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="d681e-710">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="d681e-711">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="d681e-711">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="d681e-712">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="d681e-712">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-713">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-713">SQL</span></span>

* <span data-ttu-id="d681e-714">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-714">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="d681e-715">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-715">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-716">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-716">VM</span></span>

* <span data-ttu-id="d681e-717">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="d681e-717">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="d681e-718">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="d681e-718">November 14, 2017</span></span>

<span data-ttu-id="d681e-719">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="d681e-719">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-720">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-720">ACR</span></span>

* <span data-ttu-id="d681e-721">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-721">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="d681e-722">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-722">ACS</span></span>

* <span data-ttu-id="d681e-723">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="d681e-723">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="d681e-724">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="d681e-724">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="d681e-725">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="d681e-725">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="d681e-726">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="d681e-726">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="d681e-727">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="d681e-727">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-728">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-728">Appservice</span></span>

* <span data-ttu-id="d681e-729">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="d681e-729">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="d681e-730">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="d681e-730">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="d681e-731">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="d681e-731">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="d681e-732">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="d681e-732">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="d681e-733">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-733">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="d681e-734">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="d681e-734">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="d681e-735">Batch</span><span class="sxs-lookup"><span data-stu-id="d681e-735">Batch</span></span>

* <span data-ttu-id="d681e-736">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-736">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="d681e-737">Batchai</span><span class="sxs-lookup"><span data-stu-id="d681e-737">Batchai</span></span>

* <span data-ttu-id="d681e-738">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="d681e-738">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="d681e-739">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="d681e-739">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="d681e-740">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="d681e-740">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="d681e-741">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="d681e-741">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="d681e-742">云</span><span class="sxs-lookup"><span data-stu-id="d681e-742">Cloud</span></span>

* <span data-ttu-id="d681e-743">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="d681e-743">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="d681e-744">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-744">Container</span></span>

* <span data-ttu-id="d681e-745">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-745">Added support to open multiple ports</span></span>
* <span data-ttu-id="d681e-746">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="d681e-746">Added container group restart policy</span></span>
* <span data-ttu-id="d681e-747">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-747">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="d681e-748">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="d681e-748">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="d681e-749">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d681e-749">Data Lake Analytics</span></span>

* <span data-ttu-id="d681e-750">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="d681e-750">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="d681e-751">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d681e-751">Data Lake Store</span></span>

* <span data-ttu-id="d681e-752">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="d681e-752">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-753">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-753">Extension</span></span>

* <span data-ttu-id="d681e-754">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="d681e-754">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="d681e-755">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="d681e-755">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="d681e-756">IoT</span><span class="sxs-lookup"><span data-stu-id="d681e-756">IoT</span></span>

* <span data-ttu-id="d681e-757">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-757">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-758">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-758">Monitor</span></span>

* <span data-ttu-id="d681e-759">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-759">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="d681e-760">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-760">Network</span></span>

* <span data-ttu-id="d681e-761">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-761">Added support for CAA DNS records</span></span>
* <span data-ttu-id="d681e-762">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-762">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="d681e-763">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-763">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="d681e-764">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-764">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="d681e-765">预留</span><span class="sxs-lookup"><span data-stu-id="d681e-765">Reservations</span></span>

* <span data-ttu-id="d681e-766">初始预览版</span><span class="sxs-lookup"><span data-stu-id="d681e-766">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-767">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-767">Resource</span></span>

* <span data-ttu-id="d681e-768">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-768">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-769">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-769">SQL</span></span>

* <span data-ttu-id="d681e-770">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-770">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-771">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-771">Storage</span></span>

* <span data-ttu-id="d681e-772">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="d681e-772">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="d681e-773">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-773">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="d681e-774">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-774">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="d681e-775">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="d681e-775">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="d681e-776">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-776">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="d681e-777">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-777">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="d681e-778">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-778">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-779">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-779">VM</span></span>

* <span data-ttu-id="d681e-780">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-780">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="d681e-781">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-781">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="d681e-782">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-782">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="d681e-783">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="d681e-783">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="d681e-784">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-784">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="d681e-785">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="d681e-785">October 24, 2017</span></span>

<span data-ttu-id="d681e-786">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="d681e-786">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="d681e-787">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-787">Core</span></span>

* <span data-ttu-id="d681e-788">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="d681e-788">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-789">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-789">ACR</span></span>

* <span data-ttu-id="d681e-790">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="d681e-790">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="d681e-791">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="d681e-791">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="d681e-792">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="d681e-792">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-793">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-793">ACS</span></span>

* <span data-ttu-id="d681e-794">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-794">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="d681e-795">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="d681e-795">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-796">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-796">Appservice</span></span>

* <span data-ttu-id="d681e-797">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-797">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="d681e-798">组件</span><span class="sxs-lookup"><span data-stu-id="d681e-798">Component</span></span>

* <span data-ttu-id="d681e-799">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="d681e-799">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-800">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-800">Monitor</span></span>

* <span data-ttu-id="d681e-801">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-801">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-802">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-802">Resource</span></span>

* <span data-ttu-id="d681e-803">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-803">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="d681e-804">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="d681e-804">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-805">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-805">VM</span></span>

* <span data-ttu-id="d681e-806">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-806">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="d681e-807">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="d681e-807">October 9, 2017</span></span>

<span data-ttu-id="d681e-808">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="d681e-808">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="d681e-809">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-809">Core</span></span>

* <span data-ttu-id="d681e-810">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="d681e-810">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-811">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-811">Appservice</span></span>

* <span data-ttu-id="d681e-812">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="d681e-812">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="d681e-813">Batch</span><span class="sxs-lookup"><span data-stu-id="d681e-813">Batch</span></span>

* <span data-ttu-id="d681e-814">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="d681e-814">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="d681e-815">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="d681e-815">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="d681e-816">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-816">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="d681e-817">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="d681e-817">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="d681e-818">Batchai</span><span class="sxs-lookup"><span data-stu-id="d681e-818">Batchai</span></span>

* <span data-ttu-id="d681e-819">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-819">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="d681e-820">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d681e-820">Keyvault</span></span>

* <span data-ttu-id="d681e-821">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="d681e-821">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="d681e-822">(#4448)</span><span class="sxs-lookup"><span data-stu-id="d681e-822">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="d681e-823">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-823">Network</span></span>

* <span data-ttu-id="d681e-824">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="d681e-824">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="d681e-825">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="d681e-825">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-826">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-826">Resource</span></span>

* <span data-ttu-id="d681e-827">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-827">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="d681e-828">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="d681e-828">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="d681e-829">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="d681e-829">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="d681e-830">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="d681e-830">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-831">Sql</span><span class="sxs-lookup"><span data-stu-id="d681e-831">Sql</span></span>

* <span data-ttu-id="d681e-832">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-832">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="d681e-833">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="d681e-833">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="d681e-834">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="d681e-834">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-835">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-835">Storage</span></span>

* <span data-ttu-id="d681e-836">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-836">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-837">Vm</span><span class="sxs-lookup"><span data-stu-id="d681e-837">Vm</span></span>

* <span data-ttu-id="d681e-838">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="d681e-838">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="d681e-839">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-839">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="d681e-840">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-840">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="d681e-841">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-841">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="d681e-842">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-842">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="d681e-843">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="d681e-843">September 22, 2017</span></span>

<span data-ttu-id="d681e-844">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="d681e-844">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-845">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-845">Resource</span></span>

* <span data-ttu-id="d681e-846">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-846">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="d681e-847">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="d681e-847">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="d681e-848">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-848">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="d681e-849">[重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="d681e-849">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="d681e-850">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-850">Network</span></span>

* <span data-ttu-id="d681e-851">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-851">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="d681e-852">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-852">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="d681e-853">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="d681e-853">Added `asg` application security group commands</span></span>
* <span data-ttu-id="d681e-854">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-854">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="d681e-855">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-855">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="d681e-856">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-856">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="d681e-857">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-857">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-858">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-858">Storage</span></span>

* <span data-ttu-id="d681e-859">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-859">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="d681e-860">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="d681e-860">Eventgrid</span></span>

* <span data-ttu-id="d681e-861">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="d681e-861">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-862">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-862">SQL</span></span>

* <span data-ttu-id="d681e-863">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="d681e-863">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="d681e-864">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="d681e-864">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="d681e-865">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-865">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="d681e-866">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d681e-866">Keyvault</span></span>

* <span data-ttu-id="d681e-867">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-867">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-868">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-868">VM</span></span>

* <span data-ttu-id="d681e-869">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-869">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="d681e-870">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-870">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="d681e-871">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-871">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="d681e-872">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-872">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="d681e-873">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-873">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="d681e-874">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-874">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-875">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-875">ACS</span></span>

* <span data-ttu-id="d681e-876">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-876">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-877">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-877">Appservice</span></span>

* <span data-ttu-id="d681e-878">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-878">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="d681e-879">备份</span><span class="sxs-lookup"><span data-stu-id="d681e-879">Backup</span></span>

* <span data-ttu-id="d681e-880">预览版</span><span class="sxs-lookup"><span data-stu-id="d681e-880">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="d681e-881">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="d681e-881">September 11, 2017</span></span>

<span data-ttu-id="d681e-882">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="d681e-882">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="d681e-883">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-883">Core</span></span>

* <span data-ttu-id="d681e-884">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="d681e-884">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="d681e-885">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="d681e-885">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-886">Acs</span><span class="sxs-lookup"><span data-stu-id="d681e-886">Acs</span></span>

* <span data-ttu-id="d681e-887">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-887">Added `acs list-locations` command</span></span>
* <span data-ttu-id="d681e-888">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="d681e-888">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-889">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-889">Appservice</span></span>

* <span data-ttu-id="d681e-890">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-890">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="d681e-891">CDN</span><span class="sxs-lookup"><span data-stu-id="d681e-891">CDN</span></span>

* <span data-ttu-id="d681e-892">修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug</span><span class="sxs-lookup"><span data-stu-id="d681e-892">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="d681e-893">分机</span><span class="sxs-lookup"><span data-stu-id="d681e-893">Extension</span></span>

* <span data-ttu-id="d681e-894">初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-894">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="d681e-895">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d681e-895">Keyvault</span></span>

* <span data-ttu-id="d681e-896">为 `keyvault set-policy` 修复了权限区分大小写的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-896">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="d681e-897">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-897">Network</span></span>

* <span data-ttu-id="d681e-898">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="d681e-898">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="d681e-899">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="d681e-899">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="d681e-900">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-900">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="d681e-901">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-901">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="d681e-902">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-902">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-903">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-903">Resource</span></span>

* <span data-ttu-id="d681e-904">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="d681e-904">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="d681e-905">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="d681e-905">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="d681e-906">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="d681e-906">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="d681e-907">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="d681e-907">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-908">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-908">SQL</span></span>

* <span data-ttu-id="d681e-909">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-909">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-910">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-910">VM</span></span>

* <span data-ttu-id="d681e-911">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="d681e-911">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="d681e-912">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="d681e-912">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="d681e-913">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="d681e-913">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="d681e-914">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="d681e-914">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="d681e-915">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="d681e-915">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="d681e-916">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="d681e-916">August 31, 2017</span></span>

<span data-ttu-id="d681e-917">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="d681e-917">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="d681e-918">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d681e-918">Keyvault</span></span>

* <span data-ttu-id="d681e-919">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-919">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="d681e-920">Sf</span><span class="sxs-lookup"><span data-stu-id="d681e-920">Sf</span></span>

* <span data-ttu-id="d681e-921">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="d681e-921">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-922">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-922">Storage</span></span>

* <span data-ttu-id="d681e-923">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-923">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="d681e-924">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="d681e-924">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="d681e-925">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="d681e-925">August 28, 2017</span></span>

<span data-ttu-id="d681e-926">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="d681e-926">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="d681e-927">CLI</span><span class="sxs-lookup"><span data-stu-id="d681e-927">CLI</span></span>

* <span data-ttu-id="d681e-928">在 `--version` 中添加了法律说明</span><span class="sxs-lookup"><span data-stu-id="d681e-928">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-929">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-929">ACS</span></span>

* <span data-ttu-id="d681e-930">更正了预览区域</span><span class="sxs-lookup"><span data-stu-id="d681e-930">Corrected preview regions</span></span>
* <span data-ttu-id="d681e-931">正确设置了默认 `dns_name_prefix` 的格式</span><span class="sxs-lookup"><span data-stu-id="d681e-931">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="d681e-932">优化了 acs 命令输出</span><span class="sxs-lookup"><span data-stu-id="d681e-932">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-933">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-933">Appservice</span></span>

* <span data-ttu-id="d681e-934">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致</span><span class="sxs-lookup"><span data-stu-id="d681e-934">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="d681e-935">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="d681e-935">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="d681e-936">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="d681e-936">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="d681e-937">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="d681e-937">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="d681e-938">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="d681e-938">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="d681e-939">IoT</span><span class="sxs-lookup"><span data-stu-id="d681e-939">IoT</span></span>

* <span data-ttu-id="d681e-940">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="d681e-940">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="d681e-941">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-941">Network</span></span>

* <span data-ttu-id="d681e-942">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="d681e-942">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="d681e-943">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="d681e-943">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="d681e-944">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-944">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="d681e-945">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-945">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="d681e-946">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-946">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-947">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-947">Profile</span></span>

* <span data-ttu-id="d681e-948">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="d681e-948">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d681e-949">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d681e-949">Service Fabric</span></span>

* <span data-ttu-id="d681e-950">预览版</span><span class="sxs-lookup"><span data-stu-id="d681e-950">Preview release</span></span>
* <span data-ttu-id="d681e-951">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="d681e-951">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="d681e-952">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-952">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="d681e-953">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-953">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-954">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-954">Storage</span></span>

* <span data-ttu-id="d681e-955">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="d681e-955">Enabled setting blob tier</span></span>
* <span data-ttu-id="d681e-956">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="d681e-956">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="d681e-957">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="d681e-957">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="d681e-958">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-958">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="d681e-959">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="d681e-959">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="d681e-960">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="d681e-960">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-961">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-961">VM</span></span>

* <span data-ttu-id="d681e-962">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-962">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="d681e-963">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="d681e-963">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="d681e-964">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="d681e-964">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="d681e-965">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-965">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="d681e-966">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-966">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="d681e-967">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-967">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="d681e-968">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="d681e-968">August 15, 2017</span></span>

<span data-ttu-id="d681e-969">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="d681e-969">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-970">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-970">ACS</span></span>

* <span data-ttu-id="d681e-971">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="d681e-971">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-972">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-972">Appservice</span></span>

* <span data-ttu-id="d681e-973">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-973">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="d681e-974">事件网格</span><span class="sxs-lookup"><span data-stu-id="d681e-974">Event Grid</span></span>

* <span data-ttu-id="d681e-975">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="d681e-975">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="d681e-976">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="d681e-976">August 11, 2017</span></span>

<span data-ttu-id="d681e-977">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="d681e-977">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-978">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-978">ACS</span></span>

* <span data-ttu-id="d681e-979">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="d681e-979">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="d681e-980">Batch</span><span class="sxs-lookup"><span data-stu-id="d681e-980">Batch</span></span>

* <span data-ttu-id="d681e-981">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="d681e-981">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="d681e-982">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="d681e-982">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="d681e-983">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-983">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="d681e-984">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="d681e-984">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="d681e-985">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="d681e-985">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="d681e-986">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="d681e-986">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="d681e-987">组件</span><span class="sxs-lookup"><span data-stu-id="d681e-987">Component</span></span>

* <span data-ttu-id="d681e-988">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="d681e-988">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="d681e-989">容器</span><span class="sxs-lookup"><span data-stu-id="d681e-989">Container</span></span>

* <span data-ttu-id="d681e-990">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-990">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="d681e-991">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d681e-991">Data Lake Store</span></span>

* <span data-ttu-id="d681e-992">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="d681e-992">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="d681e-993">事件网格</span><span class="sxs-lookup"><span data-stu-id="d681e-993">Event Grid</span></span>

* <span data-ttu-id="d681e-994">初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-994">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="d681e-995">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-995">Network</span></span>

* <span data-ttu-id="d681e-996">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-996">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="d681e-997">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-997">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="d681e-998">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-998">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="d681e-999">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="d681e-999">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-1000">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-1000">Profile</span></span>

* <span data-ttu-id="d681e-1001">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="d681e-1001">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-1002">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-1002">Storage</span></span>

* <span data-ttu-id="d681e-1003">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-1003">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-1004">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-1004">VM</span></span>

* <span data-ttu-id="d681e-1005">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="d681e-1005">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="d681e-1006">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1006">Exposed `list-skus` command</span></span>
* <span data-ttu-id="d681e-1007">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="d681e-1007">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="d681e-1008">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="d681e-1008">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="d681e-1009">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="d681e-1009">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="d681e-1010">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="d681e-1010">July 28, 2017</span></span>

<span data-ttu-id="d681e-1011">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="d681e-1011">Version 2.0.12</span></span>

* <span data-ttu-id="d681e-1012">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1012">Added container commands</span></span>
* <span data-ttu-id="d681e-1013">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="d681e-1013">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="d681e-1014">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-1014">Core</span></span>

* <span data-ttu-id="d681e-1015">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="d681e-1015">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="d681e-1016">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="d681e-1016">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="d681e-1017">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="d681e-1017">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="d681e-1018">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="d681e-1018">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="d681e-1019">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="d681e-1019">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="d681e-1020">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="d681e-1020">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="d681e-1021">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="d681e-1021">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="d681e-1022">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="d681e-1022">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="d681e-1023">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="d681e-1023">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="d681e-1024">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="d681e-1024">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="d681e-1025">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="d681e-1025">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="d681e-1026">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="d681e-1026">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="d681e-1027">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="d681e-1027">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="d681e-1028">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="d681e-1028">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="d681e-1029">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="d681e-1029">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="d681e-1030">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="d681e-1030">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="d681e-1031">ACR</span><span class="sxs-lookup"><span data-stu-id="d681e-1031">ACR</span></span>

* <span data-ttu-id="d681e-1032">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1032">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="d681e-1033">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="d681e-1033">Support SKU update for managed registries</span></span>
* <span data-ttu-id="d681e-1034">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="d681e-1034">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="d681e-1035">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="d681e-1035">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="d681e-1036">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-1036">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="d681e-1037">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1037">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-1038">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-1038">ACS</span></span>

* <span data-ttu-id="d681e-1039">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1039">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-1040">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-1040">Appservice</span></span>

* <span data-ttu-id="d681e-1041">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1041">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="d681e-1042">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="d681e-1042">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="d681e-1043">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1043">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="d681e-1044">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="d681e-1044">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="d681e-1045">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="d681e-1045">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="d681e-1046">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="d681e-1046">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="d681e-1047">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="d681e-1047">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="d681e-1048">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="d681e-1048">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="d681e-1049">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="d681e-1049">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="d681e-1050">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="d681e-1050">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="d681e-1051">Batch</span><span class="sxs-lookup"><span data-stu-id="d681e-1051">Batch</span></span>

* <span data-ttu-id="d681e-1052">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="d681e-1052">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="d681e-1053">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="d681e-1053">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="d681e-1054">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="d681e-1054">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="d681e-1055">CDN</span><span class="sxs-lookup"><span data-stu-id="d681e-1055">CDN</span></span>

* <span data-ttu-id="d681e-1056">当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息</span><span class="sxs-lookup"><span data-stu-id="d681e-1056">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="d681e-1057">云</span><span class="sxs-lookup"><span data-stu-id="d681e-1057">Cloud</span></span>

* <span data-ttu-id="d681e-1058">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="d681e-1058">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="d681e-1059">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="d681e-1059">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="d681e-1060">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="d681e-1060">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="d681e-1061">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-1061">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="d681e-1062">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="d681e-1062">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d681e-1063">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d681e-1063">CosmosDB</span></span>

* <span data-ttu-id="d681e-1064">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1064">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="d681e-1065">添加了对集合默认 TTL 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1065">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="d681e-1066">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d681e-1066">Data Lake Analytics</span></span>

* <span data-ttu-id="d681e-1067">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1067">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="d681e-1068">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="d681e-1068">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="d681e-1069">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="d681e-1069">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="d681e-1070">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d681e-1070">Data Lake Store</span></span>

* <span data-ttu-id="d681e-1071">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1071">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="d681e-1072">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1072">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="d681e-1073">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="d681e-1073">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="d681e-1074">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="d681e-1074">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="d681e-1075">交互</span><span class="sxs-lookup"><span data-stu-id="d681e-1075">Interactive</span></span>

* <span data-ttu-id="d681e-1076">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="d681e-1076">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="d681e-1077">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="d681e-1077">Increased test coverage</span></span>
* <span data-ttu-id="d681e-1078">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1078">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="d681e-1079">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="d681e-1079">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="d681e-1080">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="d681e-1080">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="d681e-1081">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="d681e-1081">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="d681e-1082">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="d681e-1082">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="d681e-1083">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="d681e-1083">Added `--progress` flag</span></span>
* <span data-ttu-id="d681e-1084">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="d681e-1084">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="d681e-1085">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="d681e-1085">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="d681e-1086">IoT</span><span class="sxs-lookup"><span data-stu-id="d681e-1086">IoT</span></span>

* <span data-ttu-id="d681e-1087">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="d681e-1087">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="d681e-1088">(#3934)</span><span class="sxs-lookup"><span data-stu-id="d681e-1088">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="d681e-1089">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="d681e-1089">Key vault</span></span>

* <span data-ttu-id="d681e-1090">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="d681e-1090">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="d681e-1091">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d681e-1091">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="d681e-1092">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d681e-1092">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="d681e-1093">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d681e-1093">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="d681e-1094">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="d681e-1094">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="d681e-1095">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="d681e-1095">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="d681e-1096">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="d681e-1096">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="d681e-1097">(#3307)</span><span class="sxs-lookup"><span data-stu-id="d681e-1097">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="d681e-1098">实验室</span><span class="sxs-lookup"><span data-stu-id="d681e-1098">Lab</span></span>

* <span data-ttu-id="d681e-1099">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1099">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="d681e-1100">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="d681e-1100">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-1101">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-1101">Monitor</span></span>

* <span data-ttu-id="d681e-1102">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="d681e-1102">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="d681e-1103">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="d681e-1103">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="d681e-1104">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="d681e-1104">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="d681e-1105">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="d681e-1105">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="d681e-1106">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="d681e-1106">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="d681e-1107">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="d681e-1107">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="d681e-1108">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="d681e-1108">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="d681e-1109">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="d681e-1109">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="d681e-1110">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="d681e-1110">`location` no longer required</span></span>
  * <span data-ttu-id="d681e-1111">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1111">Add name and ID support for target</span></span>
  * <span data-ttu-id="d681e-1112">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="d681e-1112">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="d681e-1113">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="d681e-1113">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="d681e-1114">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="d681e-1114">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="d681e-1115">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="d681e-1115">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="d681e-1116">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="d681e-1116">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="d681e-1117">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="d681e-1117">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="d681e-1118">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-1118">Network</span></span>

* <span data-ttu-id="d681e-1119">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1119">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="d681e-1120">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1120">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="d681e-1121">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1121">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="d681e-1122">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1122">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="d681e-1123">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1123">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="d681e-1124">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1124">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="d681e-1125">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="d681e-1125">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="d681e-1126">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="d681e-1126">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="d681e-1127">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="d681e-1127">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="d681e-1128">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="d681e-1128">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="d681e-1129">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1129">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="d681e-1130">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1130">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="d681e-1131">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="d681e-1131">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="d681e-1132">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1132">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="d681e-1133">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1133">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="d681e-1134">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1134">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="d681e-1135">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1135">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="d681e-1136">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1136">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="d681e-1137">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1137">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="d681e-1138">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1138">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="d681e-1139">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1139">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="d681e-1140">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1140">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="d681e-1141">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="d681e-1141">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="d681e-1142">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="d681e-1142">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="d681e-1143">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="d681e-1143">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="d681e-1144">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="d681e-1144">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="d681e-1145">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="d681e-1145">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-1146">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-1146">Profile</span></span>

* <span data-ttu-id="d681e-1147">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="d681e-1147">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="d681e-1148">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="d681e-1148">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="d681e-1149">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="d681e-1149">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="d681e-1150">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="d681e-1150">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="d681e-1151">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="d681e-1151">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="d681e-1152">RDBMS</span><span class="sxs-lookup"><span data-stu-id="d681e-1152">RDBMS</span></span>

* <span data-ttu-id="d681e-1153">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="d681e-1153">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="d681e-1154">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="d681e-1154">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="d681e-1155">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="d681e-1155">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="d681e-1156">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="d681e-1156">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-1157">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-1157">Resource</span></span>

* <span data-ttu-id="d681e-1158">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="d681e-1158">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="d681e-1159">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="d681e-1159">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="d681e-1160">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1160">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="d681e-1161">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1161">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="d681e-1162">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="d681e-1162">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="d681e-1163">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="d681e-1163">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="d681e-1164">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="d681e-1164">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="d681e-1165">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1165">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="d681e-1166">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-1166">Role</span></span>

* <span data-ttu-id="d681e-1167">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="d681e-1167">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="d681e-1168">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="d681e-1168">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="d681e-1169">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="d681e-1169">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="d681e-1170">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="d681e-1170">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="d681e-1171">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="d681e-1171">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="d681e-1172">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="d681e-1172">Service Fabric</span></span>
* <span data-ttu-id="d681e-1173">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="d681e-1173">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="d681e-1174">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="d681e-1174">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="d681e-1175">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="d681e-1175">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-1176">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-1176">SQL</span></span>

* <span data-ttu-id="d681e-1177">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1177">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="d681e-1178">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="d681e-1178">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="d681e-1179">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="d681e-1179">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-1180">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-1180">Storage</span></span>

* <span data-ttu-id="d681e-1181">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="d681e-1181">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="d681e-1182">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="d681e-1182">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="d681e-1183">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="d681e-1183">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="d681e-1184">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="d681e-1184">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="d681e-1185">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="d681e-1185">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="d681e-1186">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="d681e-1186">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-1187">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-1187">VM</span></span>

* <span data-ttu-id="d681e-1188">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="d681e-1188">Support configuring nsg</span></span>
* <span data-ttu-id="d681e-1189">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1189">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="d681e-1190">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="d681e-1190">Support managed service identities</span></span>
* <span data-ttu-id="d681e-1191">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1191">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="d681e-1192">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="d681e-1192">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="d681e-1193">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="d681e-1193">May 10, 2017</span></span>

<span data-ttu-id="d681e-1194">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="d681e-1194">Version 2.0.6</span></span>

* <span data-ttu-id="d681e-1195">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="d681e-1195">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="d681e-1196">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="d681e-1196">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="d681e-1197">包括 Data Lake Analytics 和 Data Lake Store 模块</span><span class="sxs-lookup"><span data-stu-id="d681e-1197">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="d681e-1198">包括认知服务模块</span><span class="sxs-lookup"><span data-stu-id="d681e-1198">Include Cognitive Services module</span></span>
* <span data-ttu-id="d681e-1199">包括 Service Fabric 模块</span><span class="sxs-lookup"><span data-stu-id="d681e-1199">Include Service Fabric module</span></span>
* <span data-ttu-id="d681e-1200">包括交互式模块（重命名 az-shell）</span><span class="sxs-lookup"><span data-stu-id="d681e-1200">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="d681e-1201">添加对 CDN 命令的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1201">Add support for CDN commands</span></span>
* <span data-ttu-id="d681e-1202">删除容器模块</span><span class="sxs-lookup"><span data-stu-id="d681e-1202">Remove Container module</span></span>
* <span data-ttu-id="d681e-1203">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="d681e-1203">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="d681e-1204">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="d681e-1204">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="d681e-1205">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-1205">Core</span></span>

* <span data-ttu-id="d681e-1206">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="d681e-1206">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="d681e-1207">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="d681e-1207">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="d681e-1208">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="d681e-1208">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="d681e-1209">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="d681e-1209">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="d681e-1210">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="d681e-1210">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="d681e-1211">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="d681e-1211">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="d681e-1212">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="d681e-1212">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="d681e-1213">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="d681e-1213">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="d681e-1214">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="d681e-1214">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="d681e-1215">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="d681e-1215">core: Improved performance</span></span>
* <span data-ttu-id="d681e-1216">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="d681e-1216">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="d681e-1217">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="d681e-1217">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-1218">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-1218">ACS</span></span>

* <span data-ttu-id="d681e-1219">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="d681e-1219">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="d681e-1220">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="d681e-1220">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="d681e-1221">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="d681e-1221">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="d681e-1222">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="d681e-1222">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-1223">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-1223">AppService</span></span>

* <span data-ttu-id="d681e-1224">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="d681e-1224">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="d681e-1225">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="d681e-1225">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="d681e-1226">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="d681e-1226">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="d681e-1227">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="d681e-1227">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="d681e-1228">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="d681e-1228">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="d681e-1229">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="d681e-1229">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="d681e-1230">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="d681e-1230">support slot swap with preview</span></span>
* <span data-ttu-id="d681e-1231">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="d681e-1231">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="d681e-1232">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="d681e-1232">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="d681e-1233">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="d681e-1233">CosmosDB</span></span>

* <span data-ttu-id="d681e-1234">将 documentdb 模块重命名为 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="d681e-1234">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="d681e-1235">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="d681e-1235">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="d681e-1236">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1236">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="d681e-1237">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1237">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="d681e-1238">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="d681e-1238">Data Lake Analytics</span></span>

* <span data-ttu-id="d681e-1239">修复了在筛选作业结果和状态列表时会引发错误的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1239">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="d681e-1240">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="d681e-1240">Add support for new catalog item type: package.</span></span> <span data-ttu-id="d681e-1241">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="d681e-1241">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="d681e-1242">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="d681e-1242">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="d681e-1243">表</span><span class="sxs-lookup"><span data-stu-id="d681e-1243">Table</span></span>
  * <span data-ttu-id="d681e-1244">表值函数</span><span class="sxs-lookup"><span data-stu-id="d681e-1244">Table valued function</span></span>
  * <span data-ttu-id="d681e-1245">查看</span><span class="sxs-lookup"><span data-stu-id="d681e-1245">View</span></span>
  * <span data-ttu-id="d681e-1246">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="d681e-1246">Table Statistics.</span></span> <span data-ttu-id="d681e-1247">这也可以使用架构（但无需指定表名）列出</span><span class="sxs-lookup"><span data-stu-id="d681e-1247">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="d681e-1248">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="d681e-1248">Data Lake Store</span></span>

* <span data-ttu-id="d681e-1249">更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1249">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="d681e-1250">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="d681e-1250">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="d681e-1251">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="d681e-1251">missed help for access show.</span></span> <span data-ttu-id="d681e-1252">正在添加。</span><span class="sxs-lookup"><span data-stu-id="d681e-1252">adding it.</span></span> <span data-ttu-id="d681e-1253">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="d681e-1253">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="d681e-1254">查找</span><span class="sxs-lookup"><span data-stu-id="d681e-1254">Find</span></span>

* <span data-ttu-id="d681e-1255">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="d681e-1255">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="d681e-1256">KeyVault</span><span class="sxs-lookup"><span data-stu-id="d681e-1256">KeyVault</span></span>

* <span data-ttu-id="d681e-1257">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="d681e-1257">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="d681e-1258">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数</span><span class="sxs-lookup"><span data-stu-id="d681e-1258">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="d681e-1259">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="d681e-1259">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="d681e-1260">修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1260">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="d681e-1261">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="d681e-1261">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="d681e-1262">实验室</span><span class="sxs-lookup"><span data-stu-id="d681e-1262">Lab</span></span>

* <span data-ttu-id="d681e-1263">为实验室中的环境添加 create、show、delete 和 list 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1263">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="d681e-1264">添加 show 和 list 命令以查看实验室中的 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="d681e-1264">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="d681e-1265">在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM</span><span class="sxs-lookup"><span data-stu-id="d681e-1265">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="d681e-1266">添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架</span><span class="sxs-lookup"><span data-stu-id="d681e-1266">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="d681e-1267">添加命令以管理实验室中的机密</span><span class="sxs-lookup"><span data-stu-id="d681e-1267">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="d681e-1268">监视</span><span class="sxs-lookup"><span data-stu-id="d681e-1268">Monitor</span></span>

* <span data-ttu-id="d681e-1269">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="d681e-1269">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="d681e-1270">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="d681e-1270">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="d681e-1271">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-1271">Network</span></span>

* <span data-ttu-id="d681e-1272">添加 `network watcher test-connectivity` 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1272">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="d681e-1273">为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1273">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="d681e-1274">添加对应用程序网关连接排出的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1274">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="d681e-1275">添加对应用程序网关 WAF 规则集配置的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1275">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="d681e-1276">添加对 ExpressRoute 路由筛选器和规则的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1276">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="d681e-1277">添加对 TrafficManager 地理路由的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1277">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="d681e-1278">添加对基于 VPN 连接策略的流量选择器的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1278">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="d681e-1279">添加对 VPN 连接 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1279">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="d681e-1280">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1280">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="d681e-1281">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1281">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="d681e-1282">从 `network vpn-connection list/show` 命令的输出中删除 null 值</span><span class="sxs-lookup"><span data-stu-id="d681e-1282">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="d681e-1283">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1283">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="d681e-1284">修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1284">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="d681e-1285">修复 `dns zone import` 中无法正确导入记录的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1285">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="d681e-1286">修复 `traffic-manager endpoint update` 不起作用的 bug</span><span class="sxs-lookup"><span data-stu-id="d681e-1286">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="d681e-1287">添加“network watcher”预览命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1287">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="d681e-1288">配置文件</span><span class="sxs-lookup"><span data-stu-id="d681e-1288">Profile</span></span>

* <span data-ttu-id="d681e-1289">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="d681e-1289">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="d681e-1290">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="d681e-1290">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="d681e-1291">Redis</span><span class="sxs-lookup"><span data-stu-id="d681e-1291">Redis</span></span>

* <span data-ttu-id="d681e-1292">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="d681e-1292">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="d681e-1293">弃用“update-settings”命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1293">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="d681e-1294">资源</span><span class="sxs-lookup"><span data-stu-id="d681e-1294">Resource</span></span>

* <span data-ttu-id="d681e-1295">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="d681e-1295">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="d681e-1296">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="d681e-1296">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="d681e-1297">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="d681e-1297">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="d681e-1298">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="d681e-1298">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="d681e-1299">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="d681e-1299">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="d681e-1300">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="d681e-1300">Add docs for az lock update.</span></span> <span data-ttu-id="d681e-1301">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="d681e-1301">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="d681e-1302">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="d681e-1302">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="d681e-1303">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="d681e-1303">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="d681e-1304">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="d681e-1304">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="d681e-1305">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="d681e-1305">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="d681e-1306">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="d681e-1306">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="d681e-1307">角色</span><span class="sxs-lookup"><span data-stu-id="d681e-1307">Role</span></span>

* <span data-ttu-id="d681e-1308">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="d681e-1308">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="d681e-1309">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="d681e-1309">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="d681e-1310">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="d681e-1310">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="d681e-1311">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="d681e-1311">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="d681e-1312">SQL</span><span class="sxs-lookup"><span data-stu-id="d681e-1312">SQL</span></span>

* <span data-ttu-id="d681e-1313">添加了 az sql server list-usages 和 az sql db list-usages 命令</span><span class="sxs-lookup"><span data-stu-id="d681e-1313">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="d681e-1314">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="d681e-1314">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="d681e-1315">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-1315">Storage</span></span>

* <span data-ttu-id="d681e-1316">对于 `storage account create`，将位置默认为资源组位置</span><span class="sxs-lookup"><span data-stu-id="d681e-1316">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="d681e-1317">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1317">Add support for incremental blob copy</span></span>
* <span data-ttu-id="d681e-1318">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="d681e-1318">Add support for large block blob upload</span></span>
* <span data-ttu-id="d681e-1319">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="d681e-1319">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-1320">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-1320">VM</span></span>

* <span data-ttu-id="d681e-1321">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="d681e-1321">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="d681e-1322">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="d681e-1322">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="d681e-1323">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="d681e-1323">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="d681e-1324">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="d681e-1324">az vm/vmss disk</span></span>
  3. <span data-ttu-id="d681e-1325">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="d681e-1325">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="d681e-1326">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="d681e-1326">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="d681e-1327">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="d681e-1327">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="d681e-1328">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="d681e-1328">April 3, 2017</span></span>

<span data-ttu-id="d681e-1329">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="d681e-1329">Version 2.0.2</span></span>

<span data-ttu-id="d681e-1330">此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件</span><span class="sxs-lookup"><span data-stu-id="d681e-1330">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="d681e-1331">核心</span><span class="sxs-lookup"><span data-stu-id="d681e-1331">Core</span></span>

* <span data-ttu-id="d681e-1332">在默认列表中添加了 acr、lab、monitor 和 find 模块</span><span class="sxs-lookup"><span data-stu-id="d681e-1332">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="d681e-1333">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="d681e-1333">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="d681e-1334">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="d681e-1334">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="d681e-1335">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="d681e-1335">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="d681e-1336">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="d681e-1336">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="d681e-1337">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="d681e-1337">Add prompting for missing template parameters.</span></span> <span data-ttu-id="d681e-1338">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="d681e-1338">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="d681e-1339">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="d681e-1339">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="d681e-1340">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="d681e-1340">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="d681e-1341">ACS</span><span class="sxs-lookup"><span data-stu-id="d681e-1341">ACS</span></span>

* <span data-ttu-id="d681e-1342">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="d681e-1342">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="d681e-1343">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="d681e-1343">Add support for ssh key password prompting.</span></span> <span data-ttu-id="d681e-1344">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="d681e-1344">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="d681e-1345">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="d681e-1345">Add support for windows clusters.</span></span> <span data-ttu-id="d681e-1346">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="d681e-1346">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="d681e-1347">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="d681e-1347">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="d681e-1348">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="d681e-1348">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="d681e-1349">应用服务</span><span class="sxs-lookup"><span data-stu-id="d681e-1349">AppService</span></span>

* <span data-ttu-id="d681e-1350">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="d681e-1350">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="d681e-1351">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="d681e-1351">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="d681e-1352">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="d681e-1352">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="d681e-1353">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="d681e-1353">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="d681e-1354">DataLake</span><span class="sxs-lookup"><span data-stu-id="d681e-1354">DataLake</span></span>

* <span data-ttu-id="d681e-1355">Data Lake Analytics 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-1355">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="d681e-1356">Data Lake Store 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="d681e-1356">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="d681e-1357">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="d681e-1357">DocuemntDB</span></span>

* <span data-ttu-id="d681e-1358">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="d681e-1358">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="d681e-1359">VM</span><span class="sxs-lookup"><span data-stu-id="d681e-1359">VM</span></span>

* <span data-ttu-id="d681e-1360">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="d681e-1360">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="d681e-1361">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="d681e-1361">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="d681e-1362">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="d681e-1362">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="d681e-1363">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="d681e-1363">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="d681e-1364">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="d681e-1364">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="d681e-1365">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="d681e-1365">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="d681e-1366">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="d681e-1366">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="d681e-1367">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="d681e-1367">February 27, 2017</span></span>

<span data-ttu-id="d681e-1368">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="d681e-1368">Version 2.0.0</span></span>

<span data-ttu-id="d681e-1369">此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="d681e-1369">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="d681e-1370">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="d681e-1370">Container Service (acs)</span></span>
- <span data-ttu-id="d681e-1371">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="d681e-1371">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="d681e-1372">网络</span><span class="sxs-lookup"><span data-stu-id="d681e-1372">Networking</span></span>
- <span data-ttu-id="d681e-1373">存储</span><span class="sxs-lookup"><span data-stu-id="d681e-1373">Storage</span></span>

<span data-ttu-id="d681e-1374">这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="d681e-1374">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="d681e-1375">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="d681e-1375">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="d681e-1376">若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="d681e-1376">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="d681e-1377">其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="d681e-1377">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="d681e-1378">此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="d681e-1378">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="d681e-1379">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="d681e-1379">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="d681e-1380">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="d681e-1380">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="d681e-1381">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队</span><span class="sxs-lookup"><span data-stu-id="d681e-1381">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="d681e-1382">通过命令行使用 `az feedback` 命令提供反馈</span><span class="sxs-lookup"><span data-stu-id="d681e-1382">Provide feedback from the command line with the `az feedback` command</span></span>

