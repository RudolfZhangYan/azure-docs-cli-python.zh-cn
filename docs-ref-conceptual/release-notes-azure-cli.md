---
title: Azure CLI 2.0 发行说明
description: 了解 Azure CLI 2.0 的最新更新
author: sptramer
ms.author: sttramer
manager: carmonm
ms.date: 08/28/2018
ms.topic: article
ms.prod: azure
ms.technology: azure-cli
ms.devlang: azure-cli
ms.openlocfilehash: 5d179a49ad64201270be7848a72535b871081125
ms.sourcegitcommit: c90bc90c9a2b3adf2836d7cfb84951cd3ab51317
ms.translationtype: HT
ms.contentlocale: zh-CN
ms.lasthandoff: 09/06/2018
ms.locfileid: "43828739"
---
# <a name="azure-cli-20-release-notes"></a><span data-ttu-id="e6e6e-103">Azure CLI 2.0 发行说明</span><span class="sxs-lookup"><span data-stu-id="e6e6e-103">Azure CLI 2.0 release notes</span></span>

## <a name="august-28-2018"></a><span data-ttu-id="e6e6e-104">2018 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-104">August 28, 2018</span></span>

<span data-ttu-id="e6e6e-105">版本 2.0.45</span><span class="sxs-lookup"><span data-stu-id="e6e6e-105">Version 2.0.45</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-106">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-106">Core</span></span>

* <span data-ttu-id="e6e6e-107">修复了加载空配置文件的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-107">Fixed issue of loading empty configuration file</span></span>
* <span data-ttu-id="e6e6e-108">增加了对 Azure Stack 的 `2018-03-01-hybrid` 配置文件的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-108">Added support for profile `2018-03-01-hybrid` for Azure Stack</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-109">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-109">ACR</span></span>

* <span data-ttu-id="e6e6e-110">增加了在没有 ARM 请求的情况下针对运行时操作的解决方法</span><span class="sxs-lookup"><span data-stu-id="e6e6e-110">Added a workaround for runtime operations without ARM requests</span></span>
* <span data-ttu-id="e6e6e-111">从默认情况下 `build` 命令中上传的 tar 更改为 exclude 版本控制文件（例如，.git、.gitignore）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-111">Changed to exclude version control files (eg, .git, .gitignore) from uploaded tar by default in `build` command</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-112">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-112">ACS</span></span>

* <span data-ttu-id="e6e6e-113">将 `aks create` 更改为默认的 `Standard_DS2_v2` VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-113">Changed `aks create` to defaults to `Standard_DS2_v2` VMs</span></span>
* <span data-ttu-id="e6e6e-114">更改了 `aks get-credentials`，现在可以通过调用新 API 来获取群集凭据</span><span class="sxs-lookup"><span data-stu-id="e6e6e-114">Changed `aks get-credentials` to now call new apis to get cluster credential</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-115">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-115">AppService</span></span>

* <span data-ttu-id="e6e6e-116">在 functionapp 和 webapp 中增加了对 CORS 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-116">Added support for CORS on functionapp & webapp</span></span>
* <span data-ttu-id="e6e6e-117">在 create 命令中增加了 ARM 标记支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-117">Added ARM tag support on create commands</span></span>
* <span data-ttu-id="e6e6e-118">更改了 `[webapp|functionapp] identity show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-118">Changed `[webapp|functionapp] identity show` to exit with code 3 upon a missing resource</span></span>

### <a name="backup"></a><span data-ttu-id="e6e6e-119">备份</span><span class="sxs-lookup"><span data-stu-id="e6e6e-119">Backup</span></span>

* <span data-ttu-id="e6e6e-120">更改了 `backup vault backup-properties show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-120">Changed `backup vault backup-properties show` to exit with code 3 upon a missing resource</span></span>

### <a name="bot-service"></a><span data-ttu-id="e6e6e-121">Bot 服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-121">Bot Service</span></span>

* <span data-ttu-id="e6e6e-122">初始机器人服务 CLI 版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-122">Initial Bot Service CLI Release</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="e6e6e-123">认知服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-123">Cognitive Services</span></span>

* <span data-ttu-id="e6e6e-124">添加了新参数 `--api-properties,`，此参数是创建某些服务所需的</span><span class="sxs-lookup"><span data-stu-id="e6e6e-124">Added new parameter `--api-properties,` which is required for creating some of the services</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-125">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-125">IoT</span></span>

* <span data-ttu-id="e6e6e-126">修复了关联已链接中心的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-126">Fixed issue with associating linked hubs</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-127">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-127">Monitor</span></span>

* <span data-ttu-id="e6e6e-128">增加了适用于近实时指标警报的 `monitor metrics alert` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-128">Added `monitor metrics alert` commands for near-realtime metric alerts</span></span>
* <span data-ttu-id="e6e6e-129">弃用了 `monitor alert` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-129">Deprecated `monitor alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-130">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-130">Network</span></span>

* <span data-ttu-id="e6e6e-131">更改了 `network application-gateway ssl-policy predefined show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-131">Changed `network application-gateway ssl-policy predefined show` to exit with code 3 upon a missing resource</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-132">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-132">Resource</span></span>

* <span data-ttu-id="e6e6e-133">更改了 `provider operation show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-133">Changed `provider operation show` to exit with code 3 upon a missing resource</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-134">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-134">Storage</span></span>

* <span data-ttu-id="e6e6e-135">更改了 `storage share policy show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-135">Changed `storage share policy show` to exit with code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-136">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-136">VM</span></span>

* <span data-ttu-id="e6e6e-137">更改了 `vm/vmss identity show`，将会在资源缺失的情况下退出并显示代码 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-137">Changed `vm/vmss identity show` to exit with code 3 upon a missing resource</span></span> 
* <span data-ttu-id="e6e6e-138">弃用了适用于 `vm create` 的 `--storage-caching`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-138">Deprecated `--storage-caching` for `vm create`</span></span>

## <a name="auguest-14-2018"></a><span data-ttu-id="e6e6e-139">2018 年 8 月 14 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-139">Auguest 14, 2018</span></span>

<span data-ttu-id="e6e6e-140">版本 2.0.44</span><span class="sxs-lookup"><span data-stu-id="e6e6e-140">Version 2.0.44</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-141">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-141">Core</span></span>

* <span data-ttu-id="e6e6e-142">修复了 `table` 输出中的数字显示问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-142">Fixed numeric display in `table` output</span></span>
* <span data-ttu-id="e6e6e-143">增加了 YAML 输出格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-143">Added YAML output format</span></span>

### <a name="telemetry"></a><span data-ttu-id="e6e6e-144">遥测</span><span class="sxs-lookup"><span data-stu-id="e6e6e-144">Telemetry</span></span>

* <span data-ttu-id="e6e6e-145">改进了遥测报告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-145">Improved telemetry reporting</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-146">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-146">ACR</span></span>

* <span data-ttu-id="e6e6e-147">添加了 `content-trust policy` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-147">Added `content-trust policy` commands</span></span>
* <span data-ttu-id="e6e6e-148">修复了 `.dockerignore` 未正确处置的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-148">Fixed issue where `.dockerignore` was not handled properly</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-149">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-149">ACS</span></span>

* <span data-ttu-id="e6e6e-150">更改了 `az acs/aks install-cli`，可以在 Windows 的 `%USERPROFILE%\.azure-kubectl` 下安装</span><span class="sxs-lookup"><span data-stu-id="e6e6e-150">Changed `az acs/aks install-cli` to install under `%USERPROFILE%\.azure-kubectl` on Windows</span></span>
* <span data-ttu-id="e6e6e-151">更改了 `az aks install-connector`，可检测群集是否有 RBAC 并可正确配置 ACI 连接器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-151">Changed `az aks install-connector` to detect if the cluster has RBAC and configure ACI Connector appropriately</span></span>
* <span data-ttu-id="e6e6e-152">更改了角色分配方式，可以将提供的角色分配到子网</span><span class="sxs-lookup"><span data-stu-id="e6e6e-152">Changed to role assignment to the subnet when it's provided</span></span>
* <span data-ttu-id="e6e6e-153">增加了新选项，对于已提供角色的子网，可以“跳过角色分配”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-153">Added new option to "skip role assignment" for subnet when it's provided</span></span>                                 
* <span data-ttu-id="e6e6e-154">更改了角色分配，对于已存在分配的子网，可以跳过角色分配</span><span class="sxs-lookup"><span data-stu-id="e6e6e-154">Changed to skip role assignment to subnet when assignment already exists</span></span>                

### <a name="appservice"></a><span data-ttu-id="e6e6e-155">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-155">AppService</span></span>

* <span data-ttu-id="e6e6e-156">修复了妨碍在外部资源组中使用存储帐户创建 function-app 的 Bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-156">Fixed a bug that prevent from creating a function-app using storage accounts in external resource groups</span></span>
* <span data-ttu-id="e6e6e-157">修复了在进行 zip 部署时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-157">Fixed a crash on zip deployment</span></span>

### <a name="batchai"></a><span data-ttu-id="e6e6e-158">BatchAI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-158">BatchAI</span></span>

* <span data-ttu-id="e6e6e-159">更改了创建自动存储帐户时的记录器输出，现在会指定“资源组”。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-159">Changed logger output for auto-storage account creation to specifies "resource *group*".</span></span>        

### <a name="container"></a><span data-ttu-id="e6e6e-160">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-160">Container</span></span>

* <span data-ttu-id="e6e6e-161">增加了 `--secure-environment-variables`，用于将安全的环境变量传递到容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-161">Added `--secure-environment-variables` for passing secure environment variables to a container</span></span>      

### <a name="iot"></a><span data-ttu-id="e6e6e-162">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-162">IoT</span></span>

* <span data-ttu-id="e6e6e-163">[重大更改] 删除了弃用的命令，这些命令已移至 IoT 扩展</span><span class="sxs-lookup"><span data-stu-id="e6e6e-163">[BREAKING CHANGE] Removed deprecated commands which have moved to the iot extension</span></span>
* <span data-ttu-id="e6e6e-164">更新了元素，现在不采用 `azure-devices.net` 域</span><span class="sxs-lookup"><span data-stu-id="e6e6e-164">Updated elements to not assume `azure-devices.net` domain</span></span>

### <a name="iot-central"></a><span data-ttu-id="e6e6e-165">IoT 中心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-165">Iot Central</span></span>

* <span data-ttu-id="e6e6e-166">IoT Central 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-166">Initial release of IoT Central module</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-167">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-167">KeyVault</span></span>


* <span data-ttu-id="e6e6e-168">增加了用于管理存储帐户和 SAS 定义的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-168">Added commands for managing storage accounts and sas-definitions</span></span>
* <span data-ttu-id="e6e6e-169">增加了用于网络规则的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-169">Added commands for network-rules</span></span>                                                           
* <span data-ttu-id="e6e6e-170">增加了针对机密、密钥和证书操作的 `--id` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-170">Added `--id` parameter to secret, key, and certificate operations</span></span>
* <span data-ttu-id="e6e6e-171">增加了对 KV 管理多 API 版本的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-171">Added support for KV mgmt multi-api version</span></span>
* <span data-ttu-id="e6e6e-172">增加了对 KV 数据平面多 API 版本的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-172">Added support for KV data plane multi-api version</span></span>

### <a name="relay"></a><span data-ttu-id="e6e6e-173">中继</span><span class="sxs-lookup"><span data-stu-id="e6e6e-173">Relay</span></span>

* <span data-ttu-id="e6e6e-174">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-174">Initial release</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-175">Sql</span><span class="sxs-lookup"><span data-stu-id="e6e6e-175">Sql</span></span>

* <span data-ttu-id="e6e6e-176">添加了 `sql failover-group` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-176">Added `sql failover-group` commands</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-177">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-177">Storage</span></span>

* <span data-ttu-id="e6e6e-178">[重大更改] 更改了 `storage account show-usage`，现在需要 `--location` 参数并且会按区域列出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-178">[BREAKING CHANGE] Changed `storage account show-usage` to require `--location` parameter and will list by region</span></span>
* <span data-ttu-id="e6e6e-179">更改了 `--resource-group` 参数，现在此参数为 `storage account` 命令的可选参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-179">Changed `--resource-group` parameter to be optional for `storage account` commands</span></span>
* <span data-ttu-id="e6e6e-180">对于适用于单个聚合消息的批处理命令中的单个失败，删除了“前提条件失败”警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-180">Removed 'Failed precondition' warnings for individual failures in batch commands for single aggregated message</span></span>
* <span data-ttu-id="e6e6e-181">更改了 `[blob|file] delete-batch` 命令，不再输出 null 数组</span><span class="sxs-lookup"><span data-stu-id="e6e6e-181">Changed `[blob|file] delete-batch` commands to no longer output array of nulls</span></span>
* <span data-ttu-id="e6e6e-182">更改了 `blob [download|upload|delete-batch]` 命令，现在可以读取容器 URL 中的 SAS 令牌</span><span class="sxs-lookup"><span data-stu-id="e6e6e-182">Changed `blob [download|upload|delete-batch]` commands to read sas-token from container url</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-183">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-183">VM</span></span>

* <span data-ttu-id="e6e6e-184">为 `vm list-skus` 添加了常用筛选器，方便用户使用</span><span class="sxs-lookup"><span data-stu-id="e6e6e-184">Added common filters to `vm list-skus` for ease of use</span></span>

## <a name="july-31-2018"></a><span data-ttu-id="e6e6e-185">2018 年 7 月 31 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-185">July 31, 2018</span></span>

<span data-ttu-id="e6e6e-186">版本 2.0.43</span><span class="sxs-lookup"><span data-stu-id="e6e6e-186">Version 2.0.43</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-187">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-187">ACR</span></span>

* <span data-ttu-id="e6e6e-188">在 `acr build-task show` 命令中添加了 `--with-secure-properties` 标志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-188">Added `--with-secure-properties` flag to `acr build-task show` command</span></span>
* <span data-ttu-id="e6e6e-189">添加了 `acr build-task update-build` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-189">Added `acr build-task update-build` command</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-190">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-190">ACS</span></span>

* <span data-ttu-id="e6e6e-191">更改为按 [Ctrl+C] 结束 `az aks browse` 时返回“0 (成功)”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-191">Changed to return return 0 (success) when ending `az aks browse` by pressing [Ctrl+C]</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-192">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-192">Batch</span></span>

* <span data-ttu-id="e6e6e-193">修复了在 cloudshell 中显示 AAD 令牌时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-193">Fixed bug when showing AAD token in cloudshell</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-194">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-194">Container</span></span>

* <span data-ttu-id="e6e6e-195">删除了在设置订阅时 `--log-analytics-workspace-key` 对名称或 ID 的要求</span><span class="sxs-lookup"><span data-stu-id="e6e6e-195">Removed requirement for `--log-analytics-workspace-key` for name or ID when in set subscription</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-196">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-196">Network</span></span>

* <span data-ttu-id="e6e6e-197">为 Azure Stack 添加了对 2017-03-09-profile 的 dns 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-197">Added dns support to 2017-03-09-profile for Azure Stack</span></span> 

### <a name="resource"></a><span data-ttu-id="e6e6e-198">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-198">Resource</span></span>

* <span data-ttu-id="e6e6e-199">将 `--rollback-on-error` 添加到 `group deployment create` 以在出错时执行已知良好的部署</span><span class="sxs-lookup"><span data-stu-id="e6e6e-199">Added `--rollback-on-error` to `group deployment create` to execute a known-good deployment on error</span></span>
* <span data-ttu-id="e6e6e-200">修复了将 `--parameters {}` 用于 `group deployment create` 导致错误的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-200">Fixed issue where `--parameters {}` with `group deployment create` resulted in an error</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-201">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-201">Role</span></span>

* <span data-ttu-id="e6e6e-202">添加了对堆栈配置文件 2017-03-09-profile 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-202">Added support for stack profile 2017-03-09-profile</span></span>
* <span data-ttu-id="e6e6e-203">修复了 `app update` 的通用更新参数无法正常工作的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-203">Fixed issue where generic update parameters to `app update` would not work correctly</span></span>

### <a name="search"></a><span data-ttu-id="e6e6e-204">搜索</span><span class="sxs-lookup"><span data-stu-id="e6e6e-204">Search</span></span>

* <span data-ttu-id="e6e6e-205">为 Azure 搜索服务添加了命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-205">Added commands for Azure Search service</span></span>

### <a name="service-bus"></a><span data-ttu-id="e6e6e-206">服务总线</span><span class="sxs-lookup"><span data-stu-id="e6e6e-206">Service Bus</span></span>

* <span data-ttu-id="e6e6e-207">添加了迁移命令组，以将命名空间从服务总线标准版迁移到高级版</span><span class="sxs-lookup"><span data-stu-id="e6e6e-207">Added migration command group to migrate a namespace from Service Bus Standard to Premium</span></span>
* <span data-ttu-id="e6e6e-208">为服务总线队列和订阅添加了新的可选属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-208">Added new optional properties to Service Bus queue and Subscription</span></span>
  *  <span data-ttu-id="e6e6e-209">`queue` 中的 `--enable-batched-operations` 和 `--enable-dead-lettering-on-message-expiration`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-209">`--enable-batched-operations` and `--enable-dead-lettering-on-message-expiration` in `queue`</span></span>
  *  <span data-ttu-id="e6e6e-210">`subscriptions` 中的 `--dead-letter-on-filter-exceptions`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-210">`--dead-letter-on-filter-exceptions` in `subscriptions`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-211">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-211">Storage</span></span>

* <span data-ttu-id="e6e6e-212">添加了对使用单个连接下载大型文件的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-212">Added support for download of large files using a single connection</span></span>
* <span data-ttu-id="e6e6e-213">转换了在缺少资源时未能失败并显示退出代码 3 的 `show` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-213">Converted `show` commands that were missed from failing with exit code 3 upon a missing resource</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-214">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-214">VM</span></span>

* <span data-ttu-id="e6e6e-215">添加了对按订阅列出可用性集的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-215">Added support to list availability sets by subscription</span></span>
* <span data-ttu-id="e6e6e-216">添加了对 `StandardSSD_LRS` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-216">Added support for `StandardSSD_LRS`</span></span>
* <span data-ttu-id="e6e6e-217">添加了在创建 VM 规模集时对应用程序安全组的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-217">Added support for application security group on creating VM scale set</span></span>
* <span data-ttu-id="e6e6e-218">[重大更改]更改了`[vm|vmss] create`、`[vm|vmss] identity assign` 和 `[vm|vmss] identity remove`，以便以字典格式输出用户指定的标识</span><span class="sxs-lookup"><span data-stu-id="e6e6e-218">[BREAKING CHANGE] Changed `[vm|vmss] create`, `[vm|vmss] identity assign`, and `[vm|vmss] identity remove` to output user assigned identities in dictionary format</span></span>

## <a name="july-18-2018"></a><span data-ttu-id="e6e6e-219">2018 年 7 月 18 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-219">July 18, 2018</span></span>

<span data-ttu-id="e6e6e-220">版本 2.0.42</span><span class="sxs-lookup"><span data-stu-id="e6e6e-220">Version 2.0.42</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-221">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-221">Core</span></span>

* <span data-ttu-id="e6e6e-222">在 WSL bash 窗口中添加了对基于浏览器的登录的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-222">Added support for browser-based login in WSL bash window</span></span>
* <span data-ttu-id="e6e6e-223">为所有通用更新命令添加了 `--force-string` 标志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-223">Added `--force-string` flag to all generic update commands</span></span>
* <span data-ttu-id="e6e6e-224">[重大更改]更改了“show”命令以记录错误消息，并在缺少资源时退出代码为 3</span><span class="sxs-lookup"><span data-stu-id="e6e6e-224">[BREAKING CHANGE] Changed 'show' commands to log error message and fail with exit code of 3 upon a missing resource</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-225">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-225">ACR</span></span>

* <span data-ttu-id="e6e6e-226">[重大更改]在“acr build”命令中将“--no-push”更新为纯标志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-226">[BREAKING CHANGE] Updated '--no-push' to a pure flag in 'acr build' command</span></span>
* <span data-ttu-id="e6e6e-227">在 `acr repository` 组下添加了 `show` 和 `update` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-227">Added `show` and `update` commands under `acr repository` group</span></span>
* <span data-ttu-id="e6e6e-228">为 `show-manifests` 和 `show-tags`添加了 `--detail` 标记以显示更详细的信息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-228">Added `--detail` flag for `show-manifests` and `show-tags` to show more detailed information</span></span>
* <span data-ttu-id="e6e6e-229">添加了 `--image` 参数以支持通过图像获取构建详细信息或日志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-229">Added `--image` parameter to support get build details or logs by an image</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-230">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-230">ACS</span></span>

* <span data-ttu-id="e6e6e-231">如果 `--max-pods` 小于 5，则将 `az aks create` 更改为错误输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-231">Changed `az aks create` to error out if `--max-pods` is less than 5</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-232">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-232">AppService</span></span>

* <span data-ttu-id="e6e6e-233">添加了对 PremiumV2 sku 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-233">Added support for PremiumV2 skus</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-234">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-234">Batch</span></span>

* <span data-ttu-id="e6e6e-235">修复了在 Cloud Shell 模式下使用令牌凭据时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-235">Fixed bug on using token credential on cloud shell mode</span></span>
* <span data-ttu-id="e6e6e-236">将 JSON 输入更改为不区分大小写</span><span class="sxs-lookup"><span data-stu-id="e6e6e-236">Changed JSON input to be case-insensitive</span></span>

### <a name="batch-ai"></a><span data-ttu-id="e6e6e-237">Batch AI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-237">Batch AI</span></span>

* <span data-ttu-id="e6e6e-238">修复了 `az batchai job exec` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-238">Fixed `az batchai job exec` command</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-239">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-239">Container</span></span>

* <span data-ttu-id="e6e6e-240">删除了非 dockerhub 注册表的用户名和密码要求</span><span class="sxs-lookup"><span data-stu-id="e6e6e-240">Removed the requirement for username and password for non dockerhub registries</span></span>
* <span data-ttu-id="e6e6e-241">修复了从 yaml 文件创建容器组时的错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-241">Fixed error when creating container groups from yaml file</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-242">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-242">Network</span></span>

* <span data-ttu-id="e6e6e-243">为 `network nic [create|update|delete]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-243">Added `--no-wait` support to `network nic [create|update|delete]`</span></span> 
* <span data-ttu-id="e6e6e-244">添加了 `network nic wait`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-244">Added `network nic wait`</span></span>
* <span data-ttu-id="e6e6e-245">对 `network vnet [subnet|peering] list` 弃用了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-245">Deprecated `--ids` argument for `network vnet [subnet|peering] list`</span></span>
* <span data-ttu-id="e6e6e-246">添加了 `--include-default` 标志以在 `network nsg rule list` 的输出中包含默认安全规则</span><span class="sxs-lookup"><span data-stu-id="e6e6e-246">Added `--include-default` flag to include default security rules in the output of `network nsg rule list`</span></span>  

### <a name="resource"></a><span data-ttu-id="e6e6e-247">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-247">Resource</span></span>

* <span data-ttu-id="e6e6e-248">为 `group deployment delete` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-248">Added `--no-wait` support to `group deployment delete`</span></span>
* <span data-ttu-id="e6e6e-249">为 `deployment delete` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-249">Added `--no-wait` support to `deployment delete`</span></span>
* <span data-ttu-id="e6e6e-250">添加了 `deployment wait` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-250">Added `deployment wait` command</span></span>
* <span data-ttu-id="e6e6e-251">修复了订阅级别 `az deployment` 命令对于配置文件 2017-03-09-profile 错误显示的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-251">Fixed issue where the subscription-level `az deployment` commands erroneously appeared for profile 2017-03-09-profile</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-252">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-252">SQL</span></span>

* <span data-ttu-id="e6e6e-253">修复了为 `sql db copy` 和 `sql db replica create` 命令指定弹性池名称时“提供的资源组名称与 URL 中的名称不匹配”错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-253">Fixed 'The provided resource group name ... did not match the name in the Url' error when specifying elastic pool name for `sql db copy` and `sql db replica create` commands</span></span>
* <span data-ttu-id="e6e6e-254">允许通过执行 `az configure --defaults sql-server=<name>` 配置默认 SQL Server</span><span class="sxs-lookup"><span data-stu-id="e6e6e-254">Allow configuring default sql server by executing `az configure --defaults sql-server=<name>`</span></span>
* <span data-ttu-id="e6e6e-255">为 `sql server`、`sql server firewall-rule`、`sql list-usages` 和 `sql show-usage` 命令实现了表格式化程序</span><span class="sxs-lookup"><span data-stu-id="e6e6e-255">Implemented table formatters for `sql server`, `sql server firewall-rule`, `sql list-usages`, and `sql show-usage` commands</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-256">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-256">Storage</span></span>

* <span data-ttu-id="e6e6e-257">将 `pageRanges` 属性添加到了将为页 blob 填充的 `storage blob show` 输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-257">Added `pageRanges` property to `storage blob show` output that will be populated for page blobs</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-258">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-258">VM</span></span>

* <span data-ttu-id="e6e6e-259">[重大更改] 将 `vmss create` 更改为使用 `Standard_DS1_v2` 作为默认实例大小</span><span class="sxs-lookup"><span data-stu-id="e6e6e-259">[BREAKING CHANGE] Changed `vmss create` to use `Standard_DS1_v2` as the default instance size</span></span>
* <span data-ttu-id="e6e6e-260">向 `vm extension [set|delete]` 和 `vmss extension [set|delete]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-260">Added `--no-wait` support to `vm extension [set|delete]` and `vmss extension [set|delete]`</span></span>
* <span data-ttu-id="e6e6e-261">添加了 `vm extension wait`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-261">Added `vm extension wait`</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="e6e6e-262">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-262">July 3, 2018</span></span>

<span data-ttu-id="e6e6e-263">版本 2.0.41</span><span class="sxs-lookup"><span data-stu-id="e6e6e-263">Version 2.0.41</span></span>

### <a name="aks"></a><span data-ttu-id="e6e6e-264">AKS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-264">AKS</span></span>

* <span data-ttu-id="e6e6e-265">更改了监视以使用订阅 ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-265">Changed monitoring to use subscription ID</span></span>

## <a name="july-3-2018"></a><span data-ttu-id="e6e6e-266">2018 年 7 月 3 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-266">July 3, 2018</span></span>

<span data-ttu-id="e6e6e-267">版本 2.0.40</span><span class="sxs-lookup"><span data-stu-id="e6e6e-267">Version 2.0.40</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-268">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-268">Core</span></span>

* <span data-ttu-id="e6e6e-269">添加了用于交互式登录的新授权代码流</span><span class="sxs-lookup"><span data-stu-id="e6e6e-269">Added a new authorization code flow for interactive login</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-270">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-270">ACR</span></span>

* <span data-ttu-id="e6e6e-271">添加了轮询生成状态</span><span class="sxs-lookup"><span data-stu-id="e6e6e-271">Added polling build status</span></span>
* <span data-ttu-id="e6e6e-272">添加了对不区分大小写的枚举值的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-272">Added support for case-insensitive enum values</span></span>
* <span data-ttu-id="e6e6e-273">为 `show-manifests` 添加了 `--top` 和 `--orderby` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-273">Added `--top` and `--orderby` parameters for `show-manifests`</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-274">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-274">ACS</span></span>

* <span data-ttu-id="e6e6e-275">[重大更改] 默认情况下启用 Kubernetes 基于角色的访问控制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-275">[BREAKING CHANGE] Enable Kubernetes role-based access control by default</span></span>
* <span data-ttu-id="e6e6e-276">添加了 `--disable-rbac` 参数并弃用了 `--enable-rbac`，因为它现在是默认值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-276">Added `--disable-rbac` argument and deprecated `--enable-rbac` since it's the default now</span></span>
* <span data-ttu-id="e6e6e-277">更新了 `aks browse` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-277">Updated options for `aks browse` command.</span></span> <span data-ttu-id="e6e6e-278">增加了 `--listen-port` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-278">Added `--listen-port` support</span></span>
* <span data-ttu-id="e6e6e-279">为 `aks install-connector` 命令更新了默认 helm chart 包。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-279">Updated the default helm chart package for `aks install-connector` command.</span></span> <span data-ttu-id="e6e6e-280">使用 virtual-kubelet-for-aks-latest.tgz</span><span class="sxs-lookup"><span data-stu-id="e6e6e-280">Use virtual-kubelet-for-aks-latest.tgz</span></span>
* <span data-ttu-id="e6e6e-281">添加了 `aks enable-addons` 和 `aks disable-addons` 命令以更新现有群集</span><span class="sxs-lookup"><span data-stu-id="e6e6e-281">Added `aks enable-addons` and `aks disable-addons` commands to update an existing cluster</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-282">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-282">AppService</span></span>

* <span data-ttu-id="e6e6e-283">添加了对通过 `webapp identity remove` 禁用标识的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-283">Added support for disabling identity via `webapp identity remove`</span></span>
* <span data-ttu-id="e6e6e-284">删除了标识功能的 `preview` 标记</span><span class="sxs-lookup"><span data-stu-id="e6e6e-284">Removed `preview` tag for Identity feature</span></span>

### <a name="backup"></a><span data-ttu-id="e6e6e-285">备份</span><span class="sxs-lookup"><span data-stu-id="e6e6e-285">Backup</span></span>

* <span data-ttu-id="e6e6e-286">更新了模块定义</span><span class="sxs-lookup"><span data-stu-id="e6e6e-286">Updated module definition</span></span>

### <a name="batchai"></a><span data-ttu-id="e6e6e-287">BatchAI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-287">BatchAI</span></span>

* <span data-ttu-id="e6e6e-288">修复了 `batchai cluster node list` 和 `batchai job node list` 命令的表输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-288">Fixed table output for `batchai cluster node list` and `batchai job node list` commands</span></span>

### <a name="cloud"></a><span data-ttu-id="e6e6e-289">云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-289">Cloud</span></span>

* <span data-ttu-id="e6e6e-290">为云配置添加了 `acr login` 服务器后缀</span><span class="sxs-lookup"><span data-stu-id="e6e6e-290">Added `acr login` server suffix to cloud config</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-291">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-291">Container</span></span>

* <span data-ttu-id="e6e6e-292">更改了 `container create` 以将其默认为长时间运行的操作</span><span class="sxs-lookup"><span data-stu-id="e6e6e-292">Changed `container create` to default to long running operation</span></span>
* <span data-ttu-id="e6e6e-293">添加了 Log Analytics 参数 `--log-analytics-workspace` 和 `--log-analytics-workspace-key`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-293">Added Log Analytics parameters `--log-analytics-workspace` and `--log-analytics-workspace-key`</span></span>
* <span data-ttu-id="e6e6e-294">添加了 `--protocol` 参数来指定要使用哪个网络协议</span><span class="sxs-lookup"><span data-stu-id="e6e6e-294">Added `--protocol` parameter to specify which network protocol to use</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-295">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-295">Extension</span></span>

* <span data-ttu-id="e6e6e-296">更改了 `extension list-available` 以仅显示与 CLI 版本兼容的扩展</span><span class="sxs-lookup"><span data-stu-id="e6e6e-296">Changed `extension list-available` to only show extensions compatible with CLI version</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-297">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-297">Network</span></span>

* <span data-ttu-id="e6e6e-298">修复了记录类型区分大小写的问题 ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-298">Fixed issue where record types were case-sensitive ([#6602](https://github.com/Azure/azure-cli/issues/6602))</span></span>

### <a name="rdbms"></a><span data-ttu-id="e6e6e-299">Rdbms</span><span class="sxs-lookup"><span data-stu-id="e6e6e-299">Rdbms</span></span>

* <span data-ttu-id="e6e6e-300">添加了 `[postgres|myql] server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-300">Added `[postgres|myql] server vnet-rule` commands</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-301">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-301">Resource</span></span>

* <span data-ttu-id="e6e6e-302">添加了新操作组 `deployment`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-302">Added new operation group `deployment`</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-303">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-303">VM</span></span>

* <span data-ttu-id="e6e6e-304">添加了对删除系统分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-304">Added support for removing system assigned identity</span></span>

## <a name="june-25-2018"></a><span data-ttu-id="e6e6e-305">2018 年 6 月 25日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-305">June 25, 2018</span></span>

<span data-ttu-id="e6e6e-306">版本 2.0.39</span><span class="sxs-lookup"><span data-stu-id="e6e6e-306">Version 2.0.39</span></span>

### <a name="cli"></a><span data-ttu-id="e6e6e-307">CLI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-307">CLI</span></span>

* <span data-ttu-id="e6e6e-308">更新了 MSI 安装程序中的文件修整以修复扩展安装问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-308">Updated file trimming in MSI installer to fix extension installation issue</span></span>

## <a name="june-19-2018"></a><span data-ttu-id="e6e6e-309">2018 年 6 月 19 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-309">June 19, 2018</span></span>

<span data-ttu-id="e6e6e-310">版本 2.0.38</span><span class="sxs-lookup"><span data-stu-id="e6e6e-310">Version 2.0.38</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-311">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-311">Core</span></span>

* <span data-ttu-id="e6e6e-312">为大多数命令增加了对 `--subscription` 的全局支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-312">Added global support for `--subscription` to most commands</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-313">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-313">ACR</span></span>

* <span data-ttu-id="e6e6e-314">增加了 `azure-storage-blob` 作为依赖项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-314">Added `azure-storage-blob` as dependency</span></span>
* <span data-ttu-id="e6e6e-315">更改了 `acr build-task create` 的默认 CPU 配置，允许使用 2 核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-315">Changed default CPU configuration with `acr build-task create` to use 2 cores</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-316">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-316">ACS</span></span>

* <span data-ttu-id="e6e6e-317">更新了 `aks use-dev-spaces` 命令的选项。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-317">Updated options of `aks use-dev-spaces` command.</span></span> <span data-ttu-id="e6e6e-318">增加了 `--update` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-318">Added `--update` support</span></span>
* <span data-ttu-id="e6e6e-319">更改了 `aks get-credentials --admin`，不替换 `$HOME/.kube/config` 中的用户上下文</span><span class="sxs-lookup"><span data-stu-id="e6e6e-319">Changed `aks get-credentials --admin` to not eplace the user context in `$HOME/.kube/config`</span></span>
* <span data-ttu-id="e6e6e-320">公开了托管群集上的只读 `nodeResourceGroup` 属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-320">Exposed read-only `nodeResourceGroup` property on managed clusters</span></span>
* <span data-ttu-id="e6e6e-321">修复了 `acs browse` 命令错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-321">Fixed `acs browse` command error</span></span>
* <span data-ttu-id="e6e6e-322">将 `--connector-name` 设置为 `aks install-connector`、`aks upgrade-connector` 和 `aks remove-connector` 的可选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-322">Made `--connector-name` optional for `aks install-connector`, `aks upgrade-connector` and `aks remove-connector`</span></span>
* <span data-ttu-id="e6e6e-323">为 `aks install-connector` 增加了新的 Azure 容器实例区域</span><span class="sxs-lookup"><span data-stu-id="e6e6e-323">Added new Azure Container Instance regions for `aks install-connector`</span></span>
* <span data-ttu-id="e6e6e-324">为 helm 版本名称增加了规范化位置，并为 `aks install-connector` 增加了节点名称</span><span class="sxs-lookup"><span data-stu-id="e6e6e-324">Added the normalized location into the helm release name and node name to `aks install-connector`</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-325">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-325">AppService</span></span>

* <span data-ttu-id="e6e6e-326">增加了对更新版 urllib 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-326">Added support for newer versions of urllib</span></span>
* <span data-ttu-id="e6e6e-327">为 `functionapp create` 增加了支持，可以使用外部资源组的应用服务计划</span><span class="sxs-lookup"><span data-stu-id="e6e6e-327">Added support to `functionapp create` to use appservice plan from external resource groups</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-328">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-328">Batch</span></span>

* <span data-ttu-id="e6e6e-329">删除了 `azure-batch-extensions` 依赖项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-329">Removed `azure-batch-extensions` dependency</span></span>

### <a name="batch-ai"></a><span data-ttu-id="e6e6e-330">Batch AI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-330">Batch AI</span></span>

* <span data-ttu-id="e6e6e-331">添加了对工作区的支持。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-331">Added support for workspaces.</span></span> <span data-ttu-id="e6e6e-332">可以通过工作区将群集、文件服务器和试验按组分组，去除了对可以创建的资源数的限制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-332">Workspaces allow to group clusters, file-servers and experiments in groups removing limitation on number of resources can be created</span></span>
* <span data-ttu-id="e6e6e-333">增加了对试验的支持。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-333">Added support for experiments.</span></span> <span data-ttu-id="e6e6e-334">可以通过试验将作业按集合分组，去除了对已创建作业的数目限制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-334">Experiments allow to group jobs in collections removing limitation on number of created jobs</span></span>
* <span data-ttu-id="e6e6e-335">增加了为 Docker 容器中运行的作业配置 `/dev/shm` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-335">Added support to configure `/dev/shm` for jobs running in a docker container</span></span>
* <span data-ttu-id="e6e6e-336">增加了 `batchai cluster node exec` 和 `batchai job node exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-336">Added `batchai cluster node exec` and `batchai job node exec` commands.</span></span> <span data-ttu-id="e6e6e-337">这些命令允许在节点上直接执行任何命令，提供用于端口转发的功能。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-337">These commands allow to execute any commands directly on nodes and provide functionality for port forwarding.</span></span>
* <span data-ttu-id="e6e6e-338">为 `batchai` 命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-338">Added support for `--ids` to `batchai` commands</span></span>
* <span data-ttu-id="e6e6e-339">[重大更改] 所有群集和文件服务器必须在工作区创建</span><span class="sxs-lookup"><span data-stu-id="e6e6e-339">[BREAKING CHANGE] All clusters and fileservers must be created under workspaces</span></span>
* <span data-ttu-id="e6e6e-340">[重大更改] 作业必须在试验中创建</span><span class="sxs-lookup"><span data-stu-id="e6e6e-340">[BREAKING CHANGE] Jobs must be created under experiments</span></span>
* <span data-ttu-id="e6e6e-341">[重大更改] 从 `cluster create` 和 `job create` 命令中删除了 `--nfs-resource-group`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-341">[BREAKING CHANGE] Removed `--nfs-resource-group` from `cluster create` and `job create` commands.</span></span> <span data-ttu-id="e6e6e-342">若要装载属于其他工作区/资源组的 NFS，请通过 `--nfs` 选项提供文件服务器的 ARM ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-342">To mount an NFS belonging to a different workspace/resource group provide file server's ARM ID via `--nfs` option</span></span>
* <span data-ttu-id="e6e6e-343">[重大更改] 从 `job create` 命令中删除了 `--cluster-resource-group`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-343">[BREAKING CHANGE] Removed `--cluster-resource-group` from `job create` command.</span></span> <span data-ttu-id="e6e6e-344">若要在属于其他工作区/资源组的群集上提交作业，请通过 `--cluster` 选项提供群集的 ARM ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-344">To submit a job on a cluster belonging to a different workspace/resource group provide cluster's ARM ID via `--cluster` option</span></span>
* <span data-ttu-id="e6e6e-345">[重大更改] 从作业、群集和文件服务器中删除了 `location` 特性。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-345">[BREAKING CHANGE] Removed `location` attribute from jobs, cluster and file servers.</span></span> <span data-ttu-id="e6e6e-346">位置现在是工作区的特性。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-346">Location now is an attribute of a workspace.</span></span>
* <span data-ttu-id="e6e6e-347">[重大更改] 从 `job create`、`cluster create` 和 `file-server create` 命令中删除了 `--location`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-347">[BREAKING CHANGE] Removed `--location` from `job create`, `cluster create` and `file-server create` commands</span></span>
* <span data-ttu-id="e6e6e-348">[重大更改] 更改了短选项的名称，使接口更一致：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-348">[BREAKING CHANGE] Changed names of short options to make interface more consistent:</span></span>
 - <span data-ttu-id="e6e6e-349">[`--config`, `-c`] 已重命名为 [`--config-file`, `-f`]</span><span class="sxs-lookup"><span data-stu-id="e6e6e-349">Renamed [`--config`, `-c`] to [`--config-file`, `-f`]</span></span>
 - <span data-ttu-id="e6e6e-350">[`--cluster`, `-r`] 已重命名为 [`--cluster`, `-c`]</span><span class="sxs-lookup"><span data-stu-id="e6e6e-350">Renamed [`--cluster`, `-r`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="e6e6e-351">[`--cluster`, `-n`] 已重命名为 [`--cluster`, `-c`]</span><span class="sxs-lookup"><span data-stu-id="e6e6e-351">Renamed [`--cluster`, `-n`] to [`--cluster`, `-c`]</span></span>
 - <span data-ttu-id="e6e6e-352">[`--job`, `-n`] 已重命名为 [`--job`, `-j`]</span><span class="sxs-lookup"><span data-stu-id="e6e6e-352">Renamed [`--job`, `-n`] to [`--job`, `-j`]</span></span>

### <a name="maps"></a><span data-ttu-id="e6e6e-353">地图</span><span class="sxs-lookup"><span data-stu-id="e6e6e-353">Maps</span></span>

* <span data-ttu-id="e6e6e-354">[重大更改] 更改了 `maps account create`，要求通过交互式提示或 `--accept-tos` 标志接受《服务条款》</span><span class="sxs-lookup"><span data-stu-id="e6e6e-354">[BREAKING CHANGE] Changed `maps account create` to require accepting Terms of Service either by interactive prompt or `--accept-tos` flag</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-355">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-355">Network</span></span>

* <span data-ttu-id="e6e6e-356">为 `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571) 增加了对 `https` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-356">Added support for `https` to `network lb probe create` [#6571](https://github.com/Azure/azure-cli/issues/6571)</span></span>
* <span data-ttu-id="e6e6e-357">修复了 `--endpoint-status` 区分大小写的问题。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-357">Fixed issue where `--endpoint-status` was case sensitive.</span></span> [<span data-ttu-id="e6e6e-358">#6502</span><span class="sxs-lookup"><span data-stu-id="e6e6e-358">#6502</span></span>](https://github.com/Azure/azure-cli/issues/6502)

### <a name="reservations"></a><span data-ttu-id="e6e6e-359">预留</span><span class="sxs-lookup"><span data-stu-id="e6e6e-359">Reservations</span></span>

* <span data-ttu-id="e6e6e-360">[重大更改] 为 `reservations catalog show` 增加了必需参数 `ReservedResourceType`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-360">[BREAKING CHANGE] Added required parameter `ReservedResourceType` to `reservations catalog show`</span></span>
* <span data-ttu-id="e6e6e-361">为 `reservations catalog show` 增加了参数 `Location`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-361">Added parameter `Location`to `reservations catalog show`</span></span>
* <span data-ttu-id="e6e6e-362">[重大更改] 从 `ReservationProperties` 中删除了 `kind`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-362">[BREAKING CHANGE] Removed `kind` from `ReservationProperties`</span></span>
* <span data-ttu-id="e6e6e-363">[重大更改] 已在 `Catalog` 中将 `capabilities` 重命名为 `sku_properties`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-363">[BREAKING CHANGE] Renamed `capabilities` to `sku_properties` in `Catalog`</span></span>
* <span data-ttu-id="e6e6e-364">[重大更改] 从 `Catalog` 中删除了 `size` 和 `tier` 属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-364">[BREAKING CHANGE] Removed `size` and `tier` properties from `Catalog`</span></span>
* <span data-ttu-id="e6e6e-365">为 `reservations reservation update` 增加了参数 `InstanceFlexibility`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-365">Added parameter `InstanceFlexibility` to `reservations reservation update`</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-366">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-366">Role</span></span>

* <span data-ttu-id="e6e6e-367">改进了错误处理</span><span class="sxs-lookup"><span data-stu-id="e6e6e-367">Improved error handling</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-368">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-368">SQL</span></span>

* <span data-ttu-id="e6e6e-369">修复了针对不可供订阅使用的位置运行 `az sql db list-editions` 时出现的令人困惑的错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-369">Fixed confusing error when running `az sql db list-editions` for a location that is not available to your subscription</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-370">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-370">Storage</span></span>

* <span data-ttu-id="e6e6e-371">更改了 `storage blob download` 的表输出，使之更为可读</span><span class="sxs-lookup"><span data-stu-id="e6e6e-371">Changed table output for `storage blob download` to be more readable</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-372">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-372">VM</span></span>

* <span data-ttu-id="e6e6e-373">针对 `vm create` 中的加速网络支持，改进了 refine vm size check</span><span class="sxs-lookup"><span data-stu-id="e6e6e-373">Improved refine vm size check for accelerated networking support in `vm create`</span></span>
* <span data-ttu-id="e6e6e-374">增加了针对 `vmss create` 的警告：默认的 VM 大小将从 `Standard_D1_v2` 切换为 `Standard_DS1_v2`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-374">Added warning for `vmss create` that the default vm size will be switched from `Standard_D1_v2` to `Standard_DS1_v2`</span></span>
* <span data-ttu-id="e6e6e-375">为 `[vm|vmss] extension set` 增加了 `--force-update`，即使在配置未变的情况下也可以更新扩展</span><span class="sxs-lookup"><span data-stu-id="e6e6e-375">Added `--force-update` to `[vm|vmss] extension set` to update the extension even when the configuration has not changed</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="e6e6e-376">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-376">June 13, 2018</span></span>

<span data-ttu-id="e6e6e-377">版本 2.0.37</span><span class="sxs-lookup"><span data-stu-id="e6e6e-377">Version 2.0.37</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-378">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-378">Core</span></span>

* <span data-ttu-id="e6e6e-379">改进了交互式遥测</span><span class="sxs-lookup"><span data-stu-id="e6e6e-379">Improved interactive telemetry</span></span>

## <a name="june-13-2018"></a><span data-ttu-id="e6e6e-380">2018 年 6 月 13 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-380">June 13, 2018</span></span>

<span data-ttu-id="e6e6e-381">版本 2.0.36</span><span class="sxs-lookup"><span data-stu-id="e6e6e-381">Version 2.0.36</span></span>

### <a name="aks"></a><span data-ttu-id="e6e6e-382">AKS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-382">AKS</span></span>

* <span data-ttu-id="e6e6e-383">为 `aks create` 添加了高级网络选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-383">Added advanced networking options to `aks create`</span></span>
* <span data-ttu-id="e6e6e-384">为 `aks create` 添加了参数以启用监视和 HTTP 路由</span><span class="sxs-lookup"><span data-stu-id="e6e6e-384">Added arguments to `aks create` to enable monitoring and HTTP routing</span></span>
* <span data-ttu-id="e6e6e-385">为 `aks create` 添加了 `--no-ssh-key` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-385">Added `--no-ssh-key` argument to `aks create`</span></span>
* <span data-ttu-id="e6e6e-386">为 `aks create` 添加了 `--enable-rbac` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-386">Added `--enable-rbac` argument to `aks create`</span></span>
* <span data-ttu-id="e6e6e-387">[PREVIEW] 为 `aks create` 添加了对 Azure Active Directory 身份验证的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-387">[PREVIEW] Added support for Azure Active Directory authentication to `aks create`</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-388">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-388">AppService</span></span>

* <span data-ttu-id="e6e6e-389">修复了不兼容 urllib 版本的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-389">Fixed an issue with incompatible urllib versions</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="e6e6e-390">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-390">June 5, 2018</span></span>

<span data-ttu-id="e6e6e-391">版本 2.0.35</span><span class="sxs-lookup"><span data-stu-id="e6e6e-391">Version 2.0.35</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-392">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-392">Interactive</span></span>

* <span data-ttu-id="e6e6e-393">添加了对交互模式的依赖项的限制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-393">Added limits to the dependencies of interactive mode</span></span>

## <a name="june-5-2018"></a><span data-ttu-id="e6e6e-394">2018 年 6 月 5 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-394">June 5, 2018</span></span>

<span data-ttu-id="e6e6e-395">版本 2.0.34</span><span class="sxs-lookup"><span data-stu-id="e6e6e-395">Version 2.0.34</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-396">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-396">Core</span></span>

* <span data-ttu-id="e6e6e-397">增加了对跨租户资源引用的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-397">Added support for cross tenant resource referencing</span></span>
* <span data-ttu-id="e6e6e-398">增强了遥测数据上传可靠性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-398">Improved telemetry upload reliability</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-399">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-399">ACR</span></span>

* <span data-ttu-id="e6e6e-400">增加了对 VSTS 充当远程源位置的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-400">Added support for VSTS as a remote source location</span></span>
* <span data-ttu-id="e6e6e-401">添加了 `acr import` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-401">Added `acr import` command</span></span>

### <a name="aks"></a><span data-ttu-id="e6e6e-402">AKS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-402">AKS</span></span>

* <span data-ttu-id="e6e6e-403">更改了 `aks get-credentials`，可以使用更安全的文件系统权限来创建 kube 配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-403">Changed `aks get-credentials` to create the kube config file with more secure filesystem permissions</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-404">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-404">Batch</span></span>

* <span data-ttu-id="e6e6e-405">修复了池列表表格式设置中的 Bug [[问题 #4378](https://github.com/Azure/azure-cli/issues/4378)]</span><span class="sxs-lookup"><span data-stu-id="e6e6e-405">Fixed bug in Pool list table formatting [[Issue #4378](https://github.com/Azure/azure-cli/issues/4378)]</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-406">IOT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-406">IOT</span></span>

* <span data-ttu-id="e6e6e-407">增加了对创建基本层 IoT 中心的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-407">Added support for creating Basic Tier IoT Hubs</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-408">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-408">Network</span></span>

* <span data-ttu-id="e6e6e-409">改进了 `network vnet peering`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-409">Improved `network vnet peering`</span></span>

### <a name="policy-insights"></a><span data-ttu-id="e6e6e-410">策略见解</span><span class="sxs-lookup"><span data-stu-id="e6e6e-410">Policy Insights</span></span>

* <span data-ttu-id="e6e6e-411">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-411">Initial Release</span></span>

### <a name="arm"></a><span data-ttu-id="e6e6e-412">ARM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-412">ARM</span></span>

* <span data-ttu-id="e6e6e-413">增加了 `account management-group` 命令。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-413">Added `account management-group` commands.</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-414">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-414">SQL</span></span>

* <span data-ttu-id="e6e6e-415">增加了新的托管实例命令：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-415">Added new managed instance commands:</span></span>
  * `sql mi create`
  * `sql mi show`
  * `sql mi list`
  * `sql mi update`
  * `sql mi delete`
* <span data-ttu-id="e6e6e-416">增加了新的托管数据库命令：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-416">Added new managed database commands:</span></span>
  * `sql midb create`
  * `sql midb show`
  * `sql midb list`
  * `sql midb restore`
  * `sql midb delete`

### <a name="storage"></a><span data-ttu-id="e6e6e-417">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-417">Storage</span></span>

* <span data-ttu-id="e6e6e-418">增加了可以从文件扩展名推断且适用于 json 和 javascript 的额外 mimetype</span><span class="sxs-lookup"><span data-stu-id="e6e6e-418">Added extra mimetypes for json and javascript to be inferred from file extensions</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-419">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-419">VM</span></span>

* <span data-ttu-id="e6e6e-420">更改了 `vm list-skus`，可以使用固定列并可添加表明要删除 `Tier` 和 `Size` 的警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-420">Changed `vm list-skus` to use fixed columns and add warning that `Tier` and `Size` will be removed</span></span>
* <span data-ttu-id="e6e6e-421">为 `vm create` 添加了 `--accelerated-networking` 选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-421">Added `--accelerated-networking` option to `vm create`</span></span>
* <span data-ttu-id="e6e6e-422">为 `identity create` 添加了 `--tags`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-422">Added `--tags` to `identity create`</span></span>

## <a name="may-22-2018"></a><span data-ttu-id="e6e6e-423">2018 年 5 月 22 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-423">May 22, 2018</span></span>

<span data-ttu-id="e6e6e-424">版本 2.0.33</span><span class="sxs-lookup"><span data-stu-id="e6e6e-424">Version 2.0.33</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-425">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-425">Core</span></span>

* <span data-ttu-id="e6e6e-426">增加了对在文件名中扩展 `@` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-426">Added support for expanding `@` in file names</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-427">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-427">ACS</span></span>

* <span data-ttu-id="e6e6e-428">增加了新的 Dev-Spaces 命令：`aks use-dev-spaces` 和 `aks remove-dev-spaces`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-428">Added new Dev-Spaces commands `aks use-dev-spaces` and `aks remove-dev-spaces`</span></span>
* <span data-ttu-id="e6e6e-429">修复了帮助消息中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-429">Fixed typo in help message</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-430">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-430">AppService</span></span>

* <span data-ttu-id="e6e6e-431">改进了泛型更新命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-431">Improved generic update commands</span></span>
* <span data-ttu-id="e6e6e-432">增加了对 `webapp deployment source config-zip` 的异步支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-432">Added async support for `webapp deployment source config-zip`</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-433">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-433">Container</span></span>

* <span data-ttu-id="e6e6e-434">增加了对以 yaml 格式导出容器组的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-434">Added support for exporting a container group in yaml format</span></span>
* <span data-ttu-id="e6e6e-435">增加了对使用 yaml 文件创建/更新容器组的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-435">Added support for using a yaml file to create / update a container group</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-436">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-436">Extension</span></span>

* <span data-ttu-id="e6e6e-437">改进了扩展的删除方式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-437">Improved removal of extensions</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-438">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-438">Interactive</span></span>

* <span data-ttu-id="e6e6e-439">更改了日志记录，在完成时将分析器静音</span><span class="sxs-lookup"><span data-stu-id="e6e6e-439">Changed logging to mute parser for completions</span></span>
* <span data-ttu-id="e6e6e-440">改进了错误的帮助缓存的处理</span><span class="sxs-lookup"><span data-stu-id="e6e6e-440">Improved handling of bad help caches</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-441">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-441">KeyVault</span></span>

* <span data-ttu-id="e6e6e-442">修复了 keyvault 命令，使之可以在 Cloud Shell 或 VM 中与标识一起使用</span><span class="sxs-lookup"><span data-stu-id="e6e6e-442">Fixed keyvault commands to work in cloud shell or VMs with identity</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-443">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-443">Network</span></span>

* <span data-ttu-id="e6e6e-444">修复了 `network watcher show-topology` 无法与 vnet 和/或子网名称一起使用的问题 [#6326](https://github.com/Azure/azure-cli/issues/6326)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-444">Fix issue where `network watcher show-topology` would not work with vnet and/or subnet name [#6326](https://github.com/Azure/azure-cli/issues/6326)</span></span>
* <span data-ttu-id="e6e6e-445">修复了某些 `network watcher` 命令宣称未为区域启用网络观察程序而实际上却已经启用的问题 [#6264](https://github.com/Azure/azure-cli/issues/6264)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-445">Fix issue where some `network watcher` commands would claim Network Watcher is not enabled for regions when it actually is [#6264](https://github.com/Azure/azure-cli/issues/6264)</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-446">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-446">SQL</span></span>

* <span data-ttu-id="e6e6e-447">[重大更改] 更改了从 `db` 和 `dw` 命令返回的响应对象：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-447">[BREAKING CHANGE] Changed response objects returned from `db` and `dw` commands:</span></span>
    * <span data-ttu-id="e6e6e-448">已将 `serviceLevelObjective` 属性重命名为 `currentServiceObjectiveName`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-448">Renamed `serviceLevelObjective` property to `currentServiceObjectiveName`</span></span>
    * <span data-ttu-id="e6e6e-449">删除了 `currentServiceObjectiveId` 和 `requestedServiceObjectiveId` 属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-449">Removed `currentServiceObjectiveId` and `requestedServiceObjectiveId` properties</span></span>
    * <span data-ttu-id="e6e6e-450">已将 `maxSizeBytes` 属性更改为整数值而不是字符串</span><span class="sxs-lookup"><span data-stu-id="e6e6e-450">Changed `maxSizeBytes` property to be an integer value instead of a string</span></span>
* <span data-ttu-id="e6e6e-451">[重大更改] 已将下面的 `db` 和 `dw` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-451">[BREAKING CHANGE] Changed the following `db` and `dw` properties to be read-only:</span></span>
    * <span data-ttu-id="e6e6e-452">`requestedServiceObjectiveName`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-452">`requestedServiceObjectiveName`.</span></span>  <span data-ttu-id="e6e6e-453">若要更新，请使用 `--service-objective` 参数或设置 `sku.name` 属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-453">To update, use the `--service-objective` parameter or set the `sku.name` property</span></span>
    * <span data-ttu-id="e6e6e-454">`edition`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-454">`edition`.</span></span> <span data-ttu-id="e6e6e-455">若要更新，请使用 `--edition` 参数或设置 `sku.tier` 属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-455">To update, use the `--edition` parameter or set the `sku.tier` property</span></span>
    * <span data-ttu-id="e6e6e-456">`elasticPoolName`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-456">`elasticPoolName`.</span></span> <span data-ttu-id="e6e6e-457">若要更新，请使用 `--elastic-pool` 参数或设置 `elasticPoolId` 属性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-457">To update, use the `--elastic-pool` parameter or set the `elasticPoolId` property</span></span>
* <span data-ttu-id="e6e6e-458">[重大更改] 已将下面的 `elastic-pool` 属性更改为只读：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-458">[BREAKING CHANGE] Changed the following `elastic-pool` properties to be read-only:</span></span>
    * <span data-ttu-id="e6e6e-459">`edition`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-459">`edition`.</span></span> <span data-ttu-id="e6e6e-460">若要更新，请使用 `--edition` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-460">To update, use the `--edition` parameter</span></span>
    * <span data-ttu-id="e6e6e-461">`dtu`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-461">`dtu`.</span></span> <span data-ttu-id="e6e6e-462">若要更新，请使用 `--capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-462">To update, use the `--capacity` parameter</span></span>
    *  <span data-ttu-id="e6e6e-463">`databaseDtuMin`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-463">`databaseDtuMin`.</span></span> <span data-ttu-id="e6e6e-464">若要更新，请使用 `--db-min-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-464">To update, use the `--db-min-capacity` parameter</span></span>
    *  <span data-ttu-id="e6e6e-465">`databaseDtuMax`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-465">`databaseDtuMax`.</span></span> <span data-ttu-id="e6e6e-466">若要更新，请使用 `--db-max-capacity` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-466">To update, use the `--db-max-capacity` parameter</span></span>
* <span data-ttu-id="e6e6e-467">为 `db`、`dw` 和 `elastic-pool` 命令增加了 `--family` 和 `--capacity` 参数。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-467">Added `--family` and `--capacity` parameters to `db`, `dw`, and `elastic-pool` commands.</span></span>
* <span data-ttu-id="e6e6e-468">为 `db`、`dw` 和 `elastic-pool` 命令增加了表格式化程序。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-468">Added table formatters to `db`, `dw`, and `elastic-pool` commands.</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-469">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-469">Storage</span></span>

* <span data-ttu-id="e6e6e-470">增加了 `--account-name` 参数的补全选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-470">Added completer for `--account-name` argument</span></span>
* <span data-ttu-id="e6e6e-471">修复了 `storage entity query` 的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-471">Fixed problem with `storage entity query`</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-472">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-472">VM</span></span>

* <span data-ttu-id="e6e6e-473">[重大更改] 从 `vm create` 中删除了 `--write-accelerator`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-473">[BREAKING CHANGE] Removed `--write-accelerator` from `vm create`.</span></span> <span data-ttu-id="e6e6e-474">可以通过 `vm update` 或 `vm disk attach` 访问同一支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-474">The same support can be accessed through `vm update` or `vm disk attach`</span></span>
* <span data-ttu-id="e6e6e-475">修复了 `[vm|vmss] extension` 中的扩展映像匹配问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-475">Fixed extension image matching in `[vm|vmss] extension`</span></span>
* <span data-ttu-id="e6e6e-476">为 `vm create` 添加了 `--boot-diagnostics-storage`，可以捕获启动日志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-476">Added `--boot-diagnostics-storage` to `vm create` to capture boot log</span></span>
* <span data-ttu-id="e6e6e-477">为 `[vm|vmss] update` 添加了 `--license-type`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-477">Added `--license-type` to `[vm|vmss] update`</span></span>

## <a name="may-7-2018"></a><span data-ttu-id="e6e6e-478">2018 年 5 月 7 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-478">May 7, 2018</span></span>

<span data-ttu-id="e6e6e-479">版本 2.0.32</span><span class="sxs-lookup"><span data-stu-id="e6e6e-479">Version 2.0.32</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-480">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-480">Core</span></span>

* <span data-ttu-id="e6e6e-481">修复了使用证书从服务主体帐户检索机密时引发未处理异常的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-481">Fixed an unhandled exception when retrieving secrets from a service principal account with cert</span></span>
* <span data-ttu-id="e6e6e-482">增加了对位置参数的有限支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-482">Added limited support for positional arguments</span></span>
* <span data-ttu-id="e6e6e-483">修复了 `--query` 无法与 `--ids` 一起使用的问题。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-483">Fix issue where `--query` could not be used with `--ids`.</span></span> [<span data-ttu-id="e6e6e-484">#5591</span><span class="sxs-lookup"><span data-stu-id="e6e6e-484">#5591</span></span>](https://github.com/Azure/azure-cli/issues/5591)
* <span data-ttu-id="e6e6e-485">改进了使用 `--ids` 时通过命令执行的管道方案。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-485">Improved piping scenarios from commands when using `--ids`.</span></span> <span data-ttu-id="e6e6e-486">支持在指定查询的情况下使用 `-o tsv`，或者在不指定查询的情况下使用 `-o json`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-486">Supports `-o tsv` with a query specified or `-o json` without specifying a query</span></span>
* <span data-ttu-id="e6e6e-487">增加了在用户的命令中存在拼写错误的情况下，针对错误提供命令建议的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-487">Added command suggestions on error if users have typo in their commands</span></span>
* <span data-ttu-id="e6e6e-488">改进了用户键入 `az ''` 时出现的错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-488">Improved error when users type `az ''`</span></span>
* <span data-ttu-id="e6e6e-489">增加了针对命令模块和扩展自定义资源类型的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-489">Added support custom resource types for command modules and extensions</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-490">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-490">ACR</span></span>

* <span data-ttu-id="e6e6e-491">增加了 ACR 生成命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-491">Added ACR Build commands</span></span>
* <span data-ttu-id="e6e6e-492">改进了“找不到资源”类型的错误消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-492">Improved resource not found error messages</span></span>
* <span data-ttu-id="e6e6e-493">改进了资源创建性能和错误处理</span><span class="sxs-lookup"><span data-stu-id="e6e6e-493">Improved resource creation performance and error handling</span></span>
* <span data-ttu-id="e6e6e-494">改进了 acr 登录非标准控制台和 WSL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-494">Improved acr login in non-standard consoles and WSL</span></span>
* <span data-ttu-id="e6e6e-495">改进了存储库命令错误消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-495">Improved repository commands error messages</span></span>
* <span data-ttu-id="e6e6e-496">更新了表列和排序</span><span class="sxs-lookup"><span data-stu-id="e6e6e-496">Updated table columns and ordering</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-497">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-497">ACS</span></span>

* <span data-ttu-id="e6e6e-498">增加了“`az aks` 是预览版服务”警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-498">Added warning that `az aks` is a preview service</span></span>
* <span data-ttu-id="e6e6e-499">修复了未指定 `--aci-resource-group` 时 `aks install-connector` 中的权限问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-499">Fixed the permission issue in `aks install-connector` when `--aci-resource-group` is not specified</span></span>

### <a name="ams"></a><span data-ttu-id="e6e6e-500">AMS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-500">AMS</span></span>

* <span data-ttu-id="e6e6e-501">初始版本 - 管理 Azure 媒体服务资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-501">Initial release - Manage Azure Media Services resources</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-502">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-502">Appservice</span></span>

* <span data-ttu-id="e6e6e-503">修复了提供 `--slot` 时 `webapp delete` 中的 Bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-503">Fixed a bug in `webapp delete` when `--slot` is provided</span></span>
* <span data-ttu-id="e6e6e-504">从 `webapp auth update` 删除了 `--runtime-version`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-504">Removed `--runtime-version` from `webapp auth update`</span></span>
* <span data-ttu-id="e6e6e-505">增加了对 min\_tls\_version & https2.0 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-505">Added support for min\_tls\_version & https2.0</span></span>
* <span data-ttu-id="e6e6e-506">增加了对多容器的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-506">Added support for multicontainers</span></span>

### <a name="batch-ai"></a><span data-ttu-id="e6e6e-507">Batch AI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-507">Batch AI</span></span>

* <span data-ttu-id="e6e6e-508">更改了 `batchai create cluster`，以便遵循在群集的配置文件中配置的 VM 优先级</span><span class="sxs-lookup"><span data-stu-id="e6e6e-508">Changed `batchai create cluster` to respect vm priority configured in the cluster's configuration file</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="e6e6e-509">认知服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-509">Cognitive Services</span></span>

* <span data-ttu-id="e6e6e-510">修复了在 `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603) 的示例中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-510">Fixed typo in example for `cognitiveservices account create` [#5603](https://github.com/Azure/azure-cli/issues/5603)</span></span>

### <a name="consumption"></a><span data-ttu-id="e6e6e-511">消耗</span><span class="sxs-lookup"><span data-stu-id="e6e6e-511">Consumption</span></span>

* <span data-ttu-id="e6e6e-512">增加了预算 API 的新命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-512">Added new commands for budget API</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-513">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-513">Container</span></span>

* <span data-ttu-id="e6e6e-514">删除了在映像名称中包括注册表服务器时对 `container create` 命令的 `--registry-server` 参数的要求</span><span class="sxs-lookup"><span data-stu-id="e6e6e-514">Removed requirement for `--registry-server` for `container create` when a registry server is included in the image name</span></span>

### <a name="cosmos-db"></a><span data-ttu-id="e6e6e-515">Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-515">Cosmos DB</span></span>

* <span data-ttu-id="e6e6e-516">引入针对 Azure CLI 的 VNET 支持 - Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-516">Introducing VNET support for Azure CLI - Cosmos DB</span></span>

### <a name="dms"></a><span data-ttu-id="e6e6e-517">DMS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-517">DMS</span></span>

* <span data-ttu-id="e6e6e-518">初始版本 - 为 Azure SQL 迁移方案增加了对 SQL 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-518">Initial release - Adds support for the SQL to Azure SQL migration scenario</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-519">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-519">Extension</span></span>

* <span data-ttu-id="e6e6e-520">修复了停止显示扩展元数据的 Bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-520">Fixed bug where extension metadata stopped being shown</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-521">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-521">Interactive</span></span>

* <span data-ttu-id="e6e6e-522">允许交互式补全选项使用位置参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-522">Allow interactive completers to function with positional arguments</span></span>
* <span data-ttu-id="e6e6e-523">增强用户键入 '\' 时的输出的用户友好性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-523">More user-friendly output when users type '\'</span></span>
* <span data-ttu-id="e6e6e-524">修复了在没有帮助的情况下参数的补全问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-524">Fixed completions for parameters with no help</span></span>
* <span data-ttu-id="e6e6e-525">修复了命令组的说明问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-525">Fixed descriptions for command-groups</span></span>

### <a name="lab"></a><span data-ttu-id="e6e6e-526">实验室</span><span class="sxs-lookup"><span data-stu-id="e6e6e-526">Lab</span></span>

* <span data-ttu-id="e6e6e-527">修复了 Knack 转换的回归问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-527">Fixed regressions from knack conversion</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-528">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-528">Network</span></span>

* <span data-ttu-id="e6e6e-529">[重大更改] 删除了以下项的 `--ids` 参数：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-529">[BREAKING CHANGE] Removed the `--ids` parameter for:</span></span>
  * `express-route auth list`
  * `express-route peering list`
  * `nic ip-config list`
  * `nsg rule list`
  * `route-filter rule list`
  * `route-table route list`
  * `traffic-manager endpoint list`

### <a name="profile"></a><span data-ttu-id="e6e6e-530">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-530">Profile</span></span>

* <span data-ttu-id="e6e6e-531">修复了 `disk create` 源检测问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-531">Fixed `disk create` source detection</span></span>
* <span data-ttu-id="e6e6e-532">[重大更改] 删除了不再使用的 `--msi-port` 和 `--identity-port`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-532">[BREAKING CHANGE] Removed `--msi-port` and `--identity-port` as they are no longer used</span></span>
* <span data-ttu-id="e6e6e-533">修复了 `account get-access-token` 短摘要中的拼写错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-533">Fixed typo in `account get-access-token` short summary</span></span>

### <a name="redis"></a><span data-ttu-id="e6e6e-534">Redis</span><span class="sxs-lookup"><span data-stu-id="e6e6e-534">Redis</span></span>

* <span data-ttu-id="e6e6e-535">弃用 `redis patch-schedule patch-schedule show` 而改用 `redis patch-schedule show`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-535">Deprecated `redis patch-schedule patch-schedule show` in favor of `redis patch-schedule show`</span></span>
* <span data-ttu-id="e6e6e-536">弃用 `redis list-all`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-536">Deprecated `redis list-all`.</span></span> <span data-ttu-id="e6e6e-537">此功能已加入 `redis list` 中</span><span class="sxs-lookup"><span data-stu-id="e6e6e-537">This functionality has been folded into `redis list`</span></span>
* <span data-ttu-id="e6e6e-538">弃用 `redis import-method` 而改用 `redis import`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-538">Deprecated `redis import-method` in favor of `redis import`</span></span>
* <span data-ttu-id="e6e6e-539">为各种命令增加了对 `--ids` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-539">Added support for `--ids` to various commands</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-540">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-540">Role</span></span>

* <span data-ttu-id="e6e6e-541">[重大更改] 删除了已弃用的 `ad sp reset-credentials`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-541">[BREAKING CHANGE] Removed deprecated `ad sp reset-credentials`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-542">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-542">Storage</span></span>

* <span data-ttu-id="e6e6e-543">在源 SAS 和帐户密钥未指定的情况下，允许将目标 SAS 令牌应用到源，以便进行 Blob 复制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-543">Allow destination sas-token to apply to source for blob copy if source sas and account key are unspecified</span></span>
* <span data-ttu-id="e6e6e-544">公开了用于 Blob 上传和下载的 --socket-timeout 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-544">Exposed --socket-timeout for blob uploads and downloads</span></span>
* <span data-ttu-id="e6e6e-545">将以路径分隔符开头的 Blob 名称视为相对路径</span><span class="sxs-lookup"><span data-stu-id="e6e6e-545">Treat blob names that start with path separators as relative paths</span></span>
* <span data-ttu-id="e6e6e-546">允许 `storage blob copy --source-sas` 以查询字符“?”开头</span><span class="sxs-lookup"><span data-stu-id="e6e6e-546">Allow `storage blob copy --source-sas` with starting query char, '?'</span></span>
* <span data-ttu-id="e6e6e-547">修复了 `storage entity query --marker` 问题，接受“键=值”列表</span><span class="sxs-lookup"><span data-stu-id="e6e6e-547">Fixed `storage entity query --marker` to accept list of key=values</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-548">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-548">VM</span></span>

* <span data-ttu-id="e6e6e-549">修复了非托管 Blob URI 上的检测逻辑无效的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-549">Fixed an invalid detection logic on unmanaged blob uri</span></span>
* <span data-ttu-id="e6e6e-550">增加了在没有用户提供的服务主体的情况下进行磁盘加密的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-550">Added support disk encryption w/o user provided service principals</span></span>
* <span data-ttu-id="e6e6e-551">[重大更改] 请勿使用 VM“ManagedIdentityExtension”来寻求 MSI 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-551">[BREAKING CHANGE] Do not use VM 'ManagedIdentityExtension' for MSI support</span></span>
* <span data-ttu-id="e6e6e-552">增加了对 `vmss` 使用逐出策略的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-552">Added support for eviction policy to `vmss`</span></span>
* <span data-ttu-id="e6e6e-553">[重大更改] 从以下项删除了 `--ids`：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-553">[BREAKING CHANGE] Removed `--ids` from:</span></span>
  * `vm extension list`
  * `vm secret list`
  * `vm unmanaged-disk list`
  * `vmss nic list`
* <span data-ttu-id="e6e6e-554">增加了写入加速器支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-554">Added write accelerator support</span></span>
* <span data-ttu-id="e6e6e-555">添加了 `vmss perform-maintenance`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-555">Added `vmss perform-maintenance`</span></span>
* <span data-ttu-id="e6e6e-556">修复了 `vm diagnostics set` 问题，可以可靠地检测 VM 的 OS 类型</span><span class="sxs-lookup"><span data-stu-id="e6e6e-556">Fixed `vm diagnostics set` to detect VM's OS type reliably</span></span>
* <span data-ttu-id="e6e6e-557">更改了 `vm resize`，系统会检查请求的大小是否不同于当前设置的大小，只在二者有变化时进行更新</span><span class="sxs-lookup"><span data-stu-id="e6e6e-557">Changed `vm resize` to check if the requested size is different than currently set and update only on change</span></span>


## <a name="april-10-2018"></a><span data-ttu-id="e6e6e-558">2018 年 4 月 10 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-558">April 10, 2018</span></span>

<span data-ttu-id="e6e6e-559">版本 2.0.31</span><span class="sxs-lookup"><span data-stu-id="e6e6e-559">Version 2.0.31</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-560">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-560">ACR</span></span>

* <span data-ttu-id="e6e6e-561">改进了 wincred 回退错误处理</span><span class="sxs-lookup"><span data-stu-id="e6e6e-561">Improved error handling of wincred fallback</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-562">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-562">ACS</span></span>

* <span data-ttu-id="e6e6e-563">更改了 aks 创建的 SPN，使其有效期达到 5 年</span><span class="sxs-lookup"><span data-stu-id="e6e6e-563">Changed aks created SPNs to be valid for 5 years</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-564">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-564">Appservice</span></span>

* [重大更改]: Removed `assign-identity`
[BREAKING CHANGE]: Removed `assign-identity`
* <span data-ttu-id="e6e6e-566">修复了 Web 应用计划不存在导致的未捕获异常</span><span class="sxs-lookup"><span data-stu-id="e6e6e-566">Fixed uncaught exception for nonexistant webapp plans</span></span>

### <a name="batchai"></a><span data-ttu-id="e6e6e-567">BatchAI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-567">BatchAI</span></span>

* <span data-ttu-id="e6e6e-568">添加了对 2018-03-01 API 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-568">Added support for 2018-03-01 API</span></span>

 - <span data-ttu-id="e6e6e-569">作业级装载</span><span class="sxs-lookup"><span data-stu-id="e6e6e-569">Job level mounting</span></span>
 - <span data-ttu-id="e6e6e-570">使用机密值的环境变量</span><span class="sxs-lookup"><span data-stu-id="e6e6e-570">Environment variables with secret values</span></span>
 - <span data-ttu-id="e6e6e-571">性能计数器设置</span><span class="sxs-lookup"><span data-stu-id="e6e6e-571">Performance counters settings</span></span>
 - <span data-ttu-id="e6e6e-572">报告作业特定的路径段</span><span class="sxs-lookup"><span data-stu-id="e6e6e-572">Reporting of job specific path segment</span></span>
 - <span data-ttu-id="e6e6e-573">支持“列出文件”API 中的子文件夹</span><span class="sxs-lookup"><span data-stu-id="e6e6e-573">Support for subfolders in list files api</span></span>
 - <span data-ttu-id="e6e6e-574">使用情况和限制报告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-574">Usage and limits reporting</span></span>
 - <span data-ttu-id="e6e6e-575">允许为 NFS 服务器指定缓存类型</span><span class="sxs-lookup"><span data-stu-id="e6e6e-575">Allow to specify caching type for NFS servers</span></span>
 - <span data-ttu-id="e6e6e-576">支持自定义映像</span><span class="sxs-lookup"><span data-stu-id="e6e6e-576">Support for custom images</span></span>
 - <span data-ttu-id="e6e6e-577">添加了 pyTorch 工具包支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-577">Added pyTorch toolkit support</span></span>

* <span data-ttu-id="e6e6e-578">添加了 `job wait` 命令，以允许等待作业完成和报告作业退出代码</span><span class="sxs-lookup"><span data-stu-id="e6e6e-578">Added `job wait` command which allows to wait for the job completion and reports job exit code</span></span>
* <span data-ttu-id="e6e6e-579">添加了 `usage show` 命令，用于列出不同区域的当前 Batch AI 资源使用情况和限制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-579">Added `usage show` command to list current Batch AI resources usage and limits for different regions</span></span>
* <span data-ttu-id="e6e6e-580">支持国家云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-580">National clouds are supported</span></span>
* <span data-ttu-id="e6e6e-581">添加了作业命令行参数，以便除了装载配置文件以外，还能装载作业级别的文件系统</span><span class="sxs-lookup"><span data-stu-id="e6e6e-581">Added job command line arguments to mount filesystems on the job level in addition to config files</span></span>
* <span data-ttu-id="e6e6e-582">添加了更多选项用于自定义群集 - VM 优先级、子网、自动缩放群集的初始节点计数，以及指定自定义映像</span><span class="sxs-lookup"><span data-stu-id="e6e6e-582">Added more options to customize clusters - vm priority, subnet, initial nodes count for auto-scale clusters, specifying custom image</span></span>
* <span data-ttu-id="e6e6e-583">添加了命令行选项用于指定 Batch AI 托管 NFS 的缓存类型</span><span class="sxs-lookup"><span data-stu-id="e6e6e-583">Added command line option to specify caching type for Batch AI managed NFS</span></span>
* <span data-ttu-id="e6e6e-584">简化了在配置文件中指定装载文件系统的方法。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-584">Simplified specifying mount filesystem in config files.</span></span> <span data-ttu-id="e6e6e-585">现在，可以省略 Azure 文件共享和 Azure Blob 容器的凭据 - CLI 将会使用通过命令行参数提供的或通过环境变量指定的存储帐户密钥来填充缺少的凭据，或者从 Azure 存储查询密钥（如果存储帐户属于当前订阅）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-585">Now you can omit credentials for Azure File Share and Azure Blob Containers - CLI will populate missing credentials using storage account key provided via command line parameters or specified via environment variable or will query the key from Azure Storage (if the storage account belongs to the current subscription)</span></span>
* <span data-ttu-id="e6e6e-586">作业完成后（成功、失败、已终止或已删除），作业文件流命令现在会自动完成</span><span class="sxs-lookup"><span data-stu-id="e6e6e-586">Job file stream command now auto-completes when the job is completed (succeeded, failed, terminated or deleted)</span></span>
* <span data-ttu-id="e6e6e-587">改进了 `show` 操作的 `table` 输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-587">Improved `table` output for `show` operations</span></span>
* <span data-ttu-id="e6e6e-588">添加了 `--use-auto-storage` 选项用于创建群集。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-588">Added `--use-auto-storage` option for cluster creation.</span></span> <span data-ttu-id="e6e6e-589">使用此选项可以更方便地管理存储帐户，以及将 Azure 文件共享和 Azure Blob 容器装载到群集</span><span class="sxs-lookup"><span data-stu-id="e6e6e-589">This option make it simpler to manage storage accounts and mount Azure File Share and Azure Blob Containers to clusters</span></span>
* <span data-ttu-id="e6e6e-590">为 `cluster create` 和 `file-server create` 添加了 `--generate-ssh-keys` 选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-590">Added `--generate-ssh-keys` option to `cluster create` and `file-server create`</span></span>
* <span data-ttu-id="e6e6e-591">添加了通过命令行提供节点设置任务的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-591">Added ability to provide node setup task via command line</span></span>
* <span data-ttu-id="e6e6e-592">[重大更改]移动了 `job file` 组下面的 `job stream-file` 和 `job list-files` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-592">[BREAKING CHANGE] Moved `job stream-file` and `job list-files` commands under `job file` group</span></span>
* <span data-ttu-id="e6e6e-593">[重大更改]已将 `file-server create` 命令中的 `--admin-user-name` 重命名为 `--user-name`，使其与 `cluster create` 命令一致</span><span class="sxs-lookup"><span data-stu-id="e6e6e-593">[BREAKING CHANGE] Renamed `--admin-user-name` to `--user-name` in `file-server create` command to be consistent with `cluster create` command</span></span>

### <a name="billing"></a><span data-ttu-id="e6e6e-594">计费</span><span class="sxs-lookup"><span data-stu-id="e6e6e-594">Billing</span></span>

* <span data-ttu-id="e6e6e-595">添加了登记帐户命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-595">Added enrollment account commands</span></span>

### <a name="consumption"></a><span data-ttu-id="e6e6e-596">消耗</span><span class="sxs-lookup"><span data-stu-id="e6e6e-596">Consumption</span></span>

* <span data-ttu-id="e6e6e-597">添加了 `marketplace` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-597">Added `marketplace` commands</span></span>
* <span data-ttu-id="e6e6e-598">[重大更改] 已将 `reservations summaries` 重命名为 `reservation summary`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-598">[BREAKING CHANGE] Renamed `reservations summaries` to `reservation summary`</span></span>
* <span data-ttu-id="e6e6e-599">[重大更改] 已将 `reservations details` 重命名为 `reservation detail`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-599">[BREAKING CHANGE] Renamed `reservations details` to `reservation detail`</span></span>
* <span data-ttu-id="e6e6e-600">[重大更改]删除了 `reservation` 命令的 `--reservation-order-id` 和 `--reservation-id` 短选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-600">[BREAKING CHANGE] Removed `--reservation-order-id` and `--reservation-id` short options for `reservation` commands</span></span>
* <span data-ttu-id="e6e6e-601">[重大更改]删除了 `reservation summary` 命令的 `--grain` 短选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-601">[BREAKING CHANGE] Removed `--grain` short options for `reservation summary` commands</span></span>
* <span data-ttu-id="e6e6e-602">[重大更改]删除了 `pricesheet` 命令的 `--include-meter-details` 短选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-602">[BREAKING CHANGE] Removed `--include-meter-details` short options for `pricesheet` commands</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-603">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-603">Container</span></span>

* <span data-ttu-id="e6e6e-604">添加了 git 存储库卷装载参数 `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` 和 `--gitrepo-mount-path`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-604">Added git repo volume mount parameters `--gitrepo-url` `--gitrepo-dir` `--gitrepo-revision` and `--gitrepo-mount-path`</span></span>
* <span data-ttu-id="e6e6e-605">修复了 [#5926](https://github.com/Azure/azure-cli/issues/5926)：指定 --container-name 时 `az container exec` 失败</span><span class="sxs-lookup"><span data-stu-id="e6e6e-605">Fixed [#5926](https://github.com/Azure/azure-cli/issues/5926): `az container exec` failing when --container-name specified</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-606">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-606">Extension</span></span>

* <span data-ttu-id="e6e6e-607">已将分配检查消息更改为调试级别</span><span class="sxs-lookup"><span data-stu-id="e6e6e-607">Changed distribution check message to be debug-level</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-608">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-608">Interactive</span></span>

* <span data-ttu-id="e6e6e-609">更改为在命令不可识别时停止完成</span><span class="sxs-lookup"><span data-stu-id="e6e6e-609">Changed to stop completions upon unrecognized commands</span></span>
* <span data-ttu-id="e6e6e-610">添加了创建命令子树之前和之后所用的事件挂钩</span><span class="sxs-lookup"><span data-stu-id="e6e6e-610">Added event hooks before and after command subtree is created</span></span>
* <span data-ttu-id="e6e6e-611">添加了 `--ids` 参数补全</span><span class="sxs-lookup"><span data-stu-id="e6e6e-611">Added completion for `--ids` parameters</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-612">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-612">Network</span></span>

* <span data-ttu-id="e6e6e-613">修复了 [#5936](https://github.com/Azure/azure-cli/issues/5936)：无法设置 `application-gateway create` 标记</span><span class="sxs-lookup"><span data-stu-id="e6e6e-613">Fixed [#5936](https://github.com/Azure/azure-cli/issues/5936): `application-gateway create` tags could not bet set</span></span>
* <span data-ttu-id="e6e6e-614">添加了参数 `--auth-certs`，以附加 `application-gateway http-settings [create|update]` 的身份验证证书。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-614">Added argument `--auth-certs` to attach authentication certificates for `application-gateway http-settings [create|update]`.</span></span> [<span data-ttu-id="e6e6e-615">#4910</span><span class="sxs-lookup"><span data-stu-id="e6e6e-615">#4910</span></span>](https://github.com/Azure/azure-cli/issues/4910)
* <span data-ttu-id="e6e6e-616">添加了 `ddos-protection` 命令用于创建 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="e6e6e-616">Added `ddos-protection` commands to create DDoS protection plans</span></span>
* <span data-ttu-id="e6e6e-617">为 `vnet [create|update]` 添加了 `--ddos-protection-plan` 支持，以便将 VNet 关联到 DDoS 保护计划</span><span class="sxs-lookup"><span data-stu-id="e6e6e-617">Added support for `--ddos-protection-plan` to `vnet [create|update]` to associate a VNet to a DDoS protection plan</span></span>
* <span data-ttu-id="e6e6e-618">修复了 `network route-table [create|update]` 中 `--disable-bgp-route-propagation` 标志的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-618">Fixed issue with `--disable-bgp-route-propagation` flag in `network route-table [create|update]`</span></span>
* <span data-ttu-id="e6e6e-619">删除了 `network lb [create|update]` 的虚拟参数 `--public-ip-address-type` 和 `--subnet-type`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-619">Removed dummy arguments `--public-ip-address-type` and `--subnet-type` for `network lb [create|update]`</span></span>
* <span data-ttu-id="e6e6e-620">为 `network dns zone [import|export]` 和 `network dns record-set txt add-record` 添加了采用 RFC 1035 转义序列的 TXT 记录支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-620">Added support for TXT records with RFC 1035 escape sequences to `network dns zone [import|export]` and `network dns record-set txt add-record`</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-621">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-621">Profile</span></span>

* <span data-ttu-id="e6e6e-622">在 `account list` 中添加了 Azure 经典帐户支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-622">Added support for Azure Classic accounts in `account list`</span></span>
* <span data-ttu-id="e6e6e-623">[重大更改]删除了 `--msi` & `--msi-port` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-623">[BREAKING CHANGE] Removed `--msi` & `--msi-port` arguments</span></span>

### <a name="rdbms"></a><span data-ttu-id="e6e6e-624">RDBMS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-624">RDBMS</span></span>

* <span data-ttu-id="e6e6e-625">添加了 `georestore` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-625">Added `georestore` command</span></span>
* <span data-ttu-id="e6e6e-626">删除了 `create` 命令的存储大小限制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-626">Removed storage size restriction from `create` command</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-627">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-627">Resource</span></span>

* <span data-ttu-id="e6e6e-628">在 `policy definition create` 中添加了对 `--metadata` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-628">Added support for `--metadata` to `policy definition create`</span></span>
* <span data-ttu-id="e6e6e-629">为 `policy definition update` 添加了对 `--metadata`、`--set`、`--add` 和 `--remove` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-629">Added support for `--metadata`, `--set`, `--add`, `--remove` to `policy definition update`</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-630">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-630">SQL</span></span>

* <span data-ttu-id="e6e6e-631">添加了 `sql elastic-pool op list` 和 `sql elastic-pool op cancel`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-631">Added `sql elastic-pool op list` and `sql elastic-pool op cancel`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-632">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-632">Storage</span></span>

* <span data-ttu-id="e6e6e-633">改进了有关连接字符串格式不当的错误消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-633">Improved error messages for malformed connection strings</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-634">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-634">VM</span></span>

* <span data-ttu-id="e6e6e-635">为 `vmss create` 添加了配置平台容错域计数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-635">Added support to configure platform fault domain count to `vmss create`</span></span>
* <span data-ttu-id="e6e6e-636">已将 `vmss create` 的默认值更改为区域性、大型或禁用单一位置组的规模集的标准负载均衡器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-636">Changed `vmss create` to default to Standard LB for zonal, large or single-placement-group disabled scale-set</span></span>
* [重大更改]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
[BREAKING CHANGE]: Removed `vm assign-identity`, `vm remove-identity and `vm format-secret\`
* <span data-ttu-id="e6e6e-638">为 `vm create` 添加了对公共 IP SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-638">Added support for Public-IP SKU to `vm create`</span></span>
* <span data-ttu-id="e6e6e-639">为 `vm secret format` 添加了 `--keyvault` 和 `--resource-group` 参数，以便在命令无法解析保管库 ID 的情况下提供支持。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-639">Added `--keyvault` and `--resource-group` arguments to `vm secret format` to support scenarios where the command is unable to resolve the vault ID.</span></span> [<span data-ttu-id="e6e6e-640">#5718</span><span class="sxs-lookup"><span data-stu-id="e6e6e-640">#5718</span></span>](https://github.com/Azure/azure-cli/issues/5718)
* <span data-ttu-id="e6e6e-641">改进了当资源组的位置不支持区域时，`[vm|vmss create]` 发生的错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-641">Better errors for `[vm|vmss create]` when a resource group's location has no zone support</span></span>


## <a name="march-27-2018"></a><span data-ttu-id="e6e6e-642">2018 年 3 月 27 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-642">March 27, 2018</span></span>

<span data-ttu-id="e6e6e-643">版本 2.0.30</span><span class="sxs-lookup"><span data-stu-id="e6e6e-643">Version 2.0.30</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-644">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-644">Core</span></span>

* <span data-ttu-id="e6e6e-645">为帮助中标记为预览版的扩展显示消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-645">Show message for extensions marked as preview in help</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-646">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-646">ACS</span></span>

* <span data-ttu-id="e6e6e-647">为 Cloud Shell 中的 `aks install-cli` 修复 SSL 证书验证错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-647">Fix SSL certificate verification error for `aks install-cli` in Cloud Shell</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-648">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-648">Appservice</span></span>

* <span data-ttu-id="e6e6e-649">为 `webapp update` 添加了仅限 HTTPS 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-649">Added HTTPS-only support to `webapp update`</span></span>
* <span data-ttu-id="e6e6e-650">为 `az webapp identity [assign|show]` 和 `az functionapp identity [assign|show]` 添加了对插槽的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-650">Added support for slots to `az webapp identity [assign|show]` and `az functionapp identity [assign|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="e6e6e-651">备份</span><span class="sxs-lookup"><span data-stu-id="e6e6e-651">Backup</span></span>

* <span data-ttu-id="e6e6e-652">添加了新命令 `az backup protection isenabled-for-vm`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-652">Added new command `az backup protection isenabled-for-vm`.</span></span> <span data-ttu-id="e6e6e-653">此命令可用于检查 VM 是否已由订阅中的任何保管库备份</span><span class="sxs-lookup"><span data-stu-id="e6e6e-653">This command can be used to check if a VM is backed up by any vault in the subscription</span></span>
* <span data-ttu-id="e6e6e-654">为下列命令的 `--resource-group` 和 `--vault-name` 参数启用了 Azure 对象 ID：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-654">Enabled Azure object IDs for `--resource-group` and `--vault-name` parameters for the following commands:</span></span>
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
* <span data-ttu-id="e6e6e-655">更改了 `--name` 参数以接受 `backup ... show` 命令的输出格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-655">Changed `--name` parameters to accept the output format from `backup ... show` commands</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-656">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-656">Container</span></span>

* <span data-ttu-id="e6e6e-657">添加了 `container exec` 命令。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-657">Added `container exec` command.</span></span> <span data-ttu-id="e6e6e-658">在正在运行的容器组的容器中执行命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-658">Executes commands in a container for a running container group</span></span>
* <span data-ttu-id="e6e6e-659">允许将表输出用于创建和更新容器组</span><span class="sxs-lookup"><span data-stu-id="e6e6e-659">Allow table output for creating and updating a container group</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-660">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-660">Extension</span></span>

* <span data-ttu-id="e6e6e-661">为 `extension add` 添加了消息（如果扩展处于预览状态）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-661">Added message for `extension add` if extension is in preview</span></span>
* <span data-ttu-id="e6e6e-662">更改了 `extension list-available` 以通过 `--show-details` 显示完整扩展数据</span><span class="sxs-lookup"><span data-stu-id="e6e6e-662">Changed `extension list-available` to show full extension data with `--show-details`</span></span>
* <span data-ttu-id="e6e6e-663">[重大更改] 更改了 `extension list-available` 以在默认情况下显示简化的扩展数据</span><span class="sxs-lookup"><span data-stu-id="e6e6e-663">[BREAKING CHANGE] Changed `extension list-available` to show simplified extension data by default</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-664">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-664">Interactive</span></span>

* <span data-ttu-id="e6e6e-665">已将“完成”更改为在执行命令表加载后立即激活</span><span class="sxs-lookup"><span data-stu-id="e6e6e-665">Changed completions to activate as soon as command table loading is done</span></span>
* <span data-ttu-id="e6e6e-666">修复了使用 `--style` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-666">Fixed bug with using `--style` parameter</span></span>
* <span data-ttu-id="e6e6e-667">交互式词法分析器在命令表转储后实例化（如果缺失）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-667">Interactive lexer instantiated after command table dump if missing</span></span>
* <span data-ttu-id="e6e6e-668">改进了完成符支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-668">Improved completer support</span></span>

### <a name="lab"></a><span data-ttu-id="e6e6e-669">实验室</span><span class="sxs-lookup"><span data-stu-id="e6e6e-669">Lab</span></span>

* <span data-ttu-id="e6e6e-670">修复了 `create environment` 命令的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-670">Fixed bugs with `create environment` command</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-671">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-671">Monitor</span></span>

* <span data-ttu-id="e6e6e-672">为 `metrics list` 添加了对 `--top`、`--orderby` 和 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-672">Added support for `--top`, `--orderby` and `--namespace` to `metrics list` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>
* <span data-ttu-id="e6e6e-673">修复了 [#4529](https://github.com/Azure/azure-cli/issues/5785)：`metrics list`接受要检索的指标的空格分隔列表</span><span class="sxs-lookup"><span data-stu-id="e6e6e-673">Fixed [#4529](https://github.com/Azure/azure-cli/issues/5785): `metrics list` Accepts a space-separated list of metrics to retrieve</span></span>
* <span data-ttu-id="e6e6e-674">为 `metrics list-definitions` 添加了对 `--namespace` 的支持 [#5785](https://github.com/Azure/azure-cli/issues/5785)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-674">Added support for `--namespace` to `metrics list-definitions` [#5785](https://github.com/Azure/azure-cli/issues/5785)</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-675">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-675">Network</span></span>

* <span data-ttu-id="e6e6e-676">添加了对专用 DNS 区域的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-676">Added support for Private DNS zones</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-677">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-677">Profile</span></span>

* <span data-ttu-id="e6e6e-678">为 `login` 添加了针对 `--identity-port` 和 `--msi-port` 的警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-678">Added warning for `--identity-port` and `--msi-port` to `login`</span></span>

### <a name="rdbms"></a><span data-ttu-id="e6e6e-679">RDBMS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-679">RDBMS</span></span>

* <span data-ttu-id="e6e6e-680">添加了业务模型 GA API 版本 2017-12-01</span><span class="sxs-lookup"><span data-stu-id="e6e6e-680">Added business model GA API version 2017-12-01</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-681">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-681">Resource</span></span>

* [重大更改]: Changed `provider operation [list|show]` to not require `--api-version`
[BREAKING CHANGE]: Changed `provider operation [list|show]` to not require `--api-version`

### <a name="role"></a><span data-ttu-id="e6e6e-683">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-683">Role</span></span>

* <span data-ttu-id="e6e6e-684">为 `az ad app create` 添加了对所需访问权限配置和本机客户端的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-684">Added support for required access configurations and native clients to `az ad app create`</span></span>
* <span data-ttu-id="e6e6e-685">更改了 `rbac` 命令以在对象解析时返回少于 1000 个的 ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-685">Changed `rbac` commands to return less than 1000 IDs on object resolution</span></span>
* <span data-ttu-id="e6e6e-686">添加了凭据管理命令 `ad sp credential [reset|list|delete]`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-686">Added credential management commands `ad sp credential [reset|list|delete]`</span></span>
* <span data-ttu-id="e6e6e-687">[重大更改] 从 `az role assignment [list|show]` 输出中删除了“properties”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-687">[BREAKING CHANGE] Removed 'properties' from `az role assignment [list|show]` output</span></span>
* <span data-ttu-id="e6e6e-688">为 `role definition` 添加了对 `dataActions` 和 `notDataActions` 权限的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-688">Added support for `dataActions` and `notDataActions` permissions to `role definition`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-689">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-689">Storage</span></span>

* <span data-ttu-id="e6e6e-690">修复了在上传大小介于 195GB 和 200GB 之间的文件时存在的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-690">Fixed issue when uploading file with size between 195GB and 200GB</span></span>
* <span data-ttu-id="e6e6e-691">修复了 [#4049](https://github.com/Azure/azure-cli/issues/4049)：上传 append 类型的 Blob 时忽略条件参数的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-691">Fixed [#4049](https://github.com/Azure/azure-cli/issues/4049): Problems with append blob uploads ignoring condition parameters</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-692">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-692">VM</span></span>

* <span data-ttu-id="e6e6e-693">针对即将到来的、适用于包含 100 个以上实例的集合的重大更改，为 `vmss create` 添加了警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-693">Added warning to `vmss create` for upcoming breaking changes for sets with 100+ instances</span></span>
* <span data-ttu-id="e6e6e-694">为 `vm [snapshot|image]` 添加了区域弹性支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-694">Added zone resilient support to `vm [snapshot|image]`</span></span>
* <span data-ttu-id="e6e6e-695">更改了磁盘实例视图以更好地报告加密状态</span><span class="sxs-lookup"><span data-stu-id="e6e6e-695">Changed disk instance view to report better encryption status</span></span>
* <span data-ttu-id="e6e6e-696">[重大更改] 更改了 `vm extension delete` 以不再返回输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-696">[BREAKING CHANGE] Changed `vm extension delete` to no longer return output</span></span>

## <a name="march-13-2018"></a><span data-ttu-id="e6e6e-697">2018 年 3 月 13 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-697">March 13, 2018</span></span>

<span data-ttu-id="e6e6e-698">版本 2.0.29</span><span class="sxs-lookup"><span data-stu-id="e6e6e-698">Version 2.0.29</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-699">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-699">ACR</span></span>

* <span data-ttu-id="e6e6e-700">为 `repository delete` 添加了对 `--image` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-700">Added support for `--image` parameter to `repository delete`</span></span>
* <span data-ttu-id="e6e6e-701">弃用了 `repository delete` 命令的 `--manifest` 和 `--tag` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-701">Deprecated `--manifest` and `--tag` parameters of the `repository delete` command</span></span>
* <span data-ttu-id="e6e6e-702">添加了 `repository untag` 命令以在不删除数据的情况下删除标记</span><span class="sxs-lookup"><span data-stu-id="e6e6e-702">Added `repository untag` command to remove a tag without deleting data</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-703">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-703">ACS</span></span>

* <span data-ttu-id="e6e6e-704">添加了 `aks upgrade-connector` 命令以升级现有连接器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-704">Added `aks upgrade-connector` command to upgrade an existing connector</span></span>
* <span data-ttu-id="e6e6e-705">更改了 `kubectl` 配置文件以使用更具可读性的块样式 YAML</span><span class="sxs-lookup"><span data-stu-id="e6e6e-705">Changed `kubectl` config files to use a more readable block-style YAML</span></span>

### <a name="advisor"></a><span data-ttu-id="e6e6e-706">顾问</span><span class="sxs-lookup"><span data-stu-id="e6e6e-706">Advisor</span></span>

* <span data-ttu-id="e6e6e-707">[重大更改] 已将 `advisor configuration get` 重命名为 `advisor configuration list`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-707">[BREAKING CHANGE] Renamed `advisor configuration get` to `advisor configuration list`</span></span>
* <span data-ttu-id="e6e6e-708">[重大更改] 已将 `advisor configuration set` 重命名为 `advisor configuration update`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-708">[BREAKING CHANGE] Renamed `advisor configuration set` to `advisor configuration update`</span></span>
* <span data-ttu-id="e6e6e-709">[重大更改] 删除了 `advisor recommendation generate`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-709">[BREAKING CHANGE] Removed `advisor recommendation generate`</span></span>
* <span data-ttu-id="e6e6e-710">为 `advisor recommendation list` 添加了 `--refresh` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-710">Added `--refresh` parameter to `advisor recommendation list`</span></span>
* <span data-ttu-id="e6e6e-711">添加了 `advisor recommendation show` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-711">Added `advisor recommendation show` command</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-712">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-712">Appservice</span></span>

* <span data-ttu-id="e6e6e-713">弃用了 `[webapp|functionapp] assign-identity`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-713">Deprecated `[webapp|functionapp] assign-identity`</span></span>
* <span data-ttu-id="e6e6e-714">添加了托管标识命令 `webapp identity [assign|show]` 和 `functionapp identity [assign|show]`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-714">Added managed identity commands `webapp identity [assign|show]` and `functionapp identity [assign|show]`</span></span>

### <a name="eventhubs"></a><span data-ttu-id="e6e6e-715">Eventhubs</span><span class="sxs-lookup"><span data-stu-id="e6e6e-715">Eventhubs</span></span>

* <span data-ttu-id="e6e6e-716">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-716">Initial release</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-717">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-717">Extension</span></span>

* <span data-ttu-id="e6e6e-718">添加了检查，以在使用的发行版不是程序包源文件中存储的发行版时提醒用户，因为这可能导致错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-718">Added check to warn user if used distro is different then the one stored in package source file, as this may lead into errors</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-719">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-719">Interactive</span></span>

* <span data-ttu-id="e6e6e-720">修复了 [#5625](https://github.com/Azure/azure-cli/issues/5625)：在不同会话之间永久保留历史记录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-720">Fixed [#5625](https://github.com/Azure/azure-cli/issues/5625): Persist history across different sessions</span></span>
* <span data-ttu-id="e6e6e-721">修复了 [#3016](https://github.com/Azure/azure-cli/issues/3016)：在作用域中时不记录历史记录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-721">Fixed [#3016](https://github.com/Azure/azure-cli/issues/3016): History not recorded while in scope</span></span>
* <span data-ttu-id="e6e6e-722">修复了 [#5688](https://github.com/Azure/azure-cli/issues/5688)：如果命令表加载遇到了异常，不显示“完成”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-722">Fixed [#5688](https://github.com/Azure/azure-cli/issues/5688): Completions did not appear if command table loading encountered an exception</span></span>
* <span data-ttu-id="e6e6e-723">修复了用于长时间运行的操作的进度指示器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-723">Fixed progress meter for long running operations</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-724">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-724">Monitor</span></span>

* <span data-ttu-id="e6e6e-725">弃用了 `monitor autoscale-settings` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-725">Deprecated the `monitor autoscale-settings` commands</span></span>
* <span data-ttu-id="e6e6e-726">添加了 `monitor autoscale` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-726">Added `monitor autoscale` commands</span></span>
* <span data-ttu-id="e6e6e-727">添加了 `monitor autoscale profile` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-727">Added `monitor autoscale profile` commands</span></span>
* <span data-ttu-id="e6e6e-728">添加了 `monitor autoscale rule` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-728">Added `monitor autoscale rule` commands</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-729">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-729">Network</span></span>

* <span data-ttu-id="e6e6e-730">[重大更改] 从 `route-filter rule create` 中删除了 `--tags` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-730">[BREAKING CHANGE] Removed `--tags` parameter from  `route-filter rule create`</span></span>
* <span data-ttu-id="e6e6e-731">删除了以下命令的某些错误默认值：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-731">Removed some erroneous default values for the following commands:</span></span>
  * `network express-route update`
  * `network nsg rule update`
  * `network public-ip update`
  * `traffic-manager profile update`
  * `network vnet-gateway update`
* <span data-ttu-id="e6e6e-732">添加了 `network watcher connection-monitor` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-732">Added `network watcher connection-monitor` commands\`</span></span>
* <span data-ttu-id="e6e6e-733">为 `network watcher show-topology` 添加了 `--vnet` 和 `--subnet`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-733">Added `--vnet` and `--subnet` parameters to `network watcher show-topology`</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-734">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-734">Profile</span></span>

* <span data-ttu-id="e6e6e-735">弃用了 `az login` 的 `--msi` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-735">Deprecated `--msi` parameter for `az login`</span></span>
* <span data-ttu-id="e6e6e-736">为 `az login` 添加了 `--identity` 参数以替换 `--msi`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-736">Added `--identity` parameter for `az login` to replace `--msi`</span></span>

### <a name="rdbms"></a><span data-ttu-id="e6e6e-737">RDBMS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-737">RDBMS</span></span>

* <span data-ttu-id="e6e6e-738">[预览] 已更改为使用 API 2017-12-01-preview</span><span class="sxs-lookup"><span data-stu-id="e6e6e-738">[PREVIEW] Changed to use the API 2017-12-01-preview</span></span>

### <a name="service-bus"></a><span data-ttu-id="e6e6e-739">服务总线</span><span class="sxs-lookup"><span data-stu-id="e6e6e-739">Service Bus</span></span>

* <span data-ttu-id="e6e6e-740">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-740">Initial release</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-741">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-741">Storage</span></span>

* <span data-ttu-id="e6e6e-742">修复了 [#4971](https://github.com/Azure/azure-cli/issues/4971)：`storage blob copy` 现在支持其他 Azure 云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-742">Fixed [#4971](https://github.com/Azure/azure-cli/issues/4971): `storage blob copy` now supports other Azure clouds</span></span>
* <span data-ttu-id="e6e6e-743">修复了 [#5286](https://github.com/Azure/azure-cli/issues/5286)：Batch 命令 `storage blob [delete-batch|download-batch|upload-batch]` 不再在前置条件失败时引发错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-743">Fixed [#5286](https://github.com/Azure/azure-cli/issues/5286): Batch commands `storage blob [delete-batch|download-batch|upload-batch]` no longer throw an error upon precondition failures</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-744">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-744">VM</span></span>

* <span data-ttu-id="e6e6e-745">为 `[vm|vmss] create` 添加了支持，以附加非托管数据磁盘和配置缓存</span><span class="sxs-lookup"><span data-stu-id="e6e6e-745">Added support to `[vm|vmss] create` to attach unmanaged data disks and configure caching</span></span>
* <span data-ttu-id="e6e6e-746">弃用了 `[vm|vmss] assign-identity` 和 `[vm|vmss] remove-identity`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-746">Deprecated `[vm|vmss] assign-identity` and `[vm|vmss] remove-identity`</span></span>
* <span data-ttu-id="e6e6e-747">添加了 `vm identity [assign|remove|show]` 和 `vmss identity [assign|remove|show]` 以替换弃用的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-747">Added `vm identity [assign|remove|show]` and `vmss identity [assign|remove|show]` commands to replace deprecated commands</span></span>
* <span data-ttu-id="e6e6e-748">已将 `vmss create` 中的默认优先级更改为 None</span><span class="sxs-lookup"><span data-stu-id="e6e6e-748">Changed default priority in `vmss create` to None</span></span>

## <a name="february-27-2018"></a><span data-ttu-id="e6e6e-749">2018 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-749">February 27, 2018</span></span>

<span data-ttu-id="e6e6e-750">版本 2.0.28</span><span class="sxs-lookup"><span data-stu-id="e6e6e-750">Version 2.0.28</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-751">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-751">Core</span></span>

* <span data-ttu-id="e6e6e-752">已修复 [#5184](https://github.com/Azure/azure-cli/issues/5184)：Homebrew 安装问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-752">Fixed [#5184](https://github.com/Azure/azure-cli/issues/5184): Homebrew install issue</span></span>
* <span data-ttu-id="e6e6e-753">添加了对具有自定义密钥的扩展遥测的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-753">Added support for extension telemetry with custom keys</span></span>
* <span data-ttu-id="e6e6e-754">为 `--debug` 添加了 HTTP 日志记录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-754">Added HTTP logging to `--debug`</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-755">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-755">ACS</span></span>

* <span data-ttu-id="e6e6e-756">已更改为默认情况下对 `aks install-connector` 使用 `virtual-kubelet-for-aks` Helm 图</span><span class="sxs-lookup"><span data-stu-id="e6e6e-756">Changed to use the the `virtual-kubelet-for-aks` Helm chart for `aks install-connector` by default</span></span>
* <span data-ttu-id="e6e6e-757">已修复问题：服务主体没有足够的权限来创建 ACI 容器组的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-757">Fixed issue: Insuffient permission for service principals to create ACI container group issue</span></span>
* <span data-ttu-id="e6e6e-758">已为 `aks install-connector` 添加了 `--aci-container-group`、`--location` 和 `--image-tag`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-758">Added `--aci-container-group`, `--location`, and `--image-tag` parameters to `aks install-connector`</span></span>
* <span data-ttu-id="e6e6e-759">从 `aks get-versions` 中删除了弃用通知</span><span class="sxs-lookup"><span data-stu-id="e6e6e-759">Removed deprecation notice from `aks get-versions`</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-760">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-760">Appservice</span></span>

* <span data-ttu-id="e6e6e-761">针对新 SDK 版本 (azure-mgmt-web 0.35.0) 的更新</span><span class="sxs-lookup"><span data-stu-id="e6e6e-761">Updates for new SDK version (azure-mgmt-web 0.35.0)</span></span>
* <span data-ttu-id="e6e6e-762">已修复 [#5538](https://github.com/Azure/azure-cli/issues/5538)：`Free` 被报告为无效 SKU</span><span class="sxs-lookup"><span data-stu-id="e6e6e-762">Fixed [#5538](https://github.com/Azure/azure-cli/issues/5538): `Free` reported as invalid SKU</span></span>

### <a name="cognitive-services"></a><span data-ttu-id="e6e6e-763">认知服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-763">Cognitive Services</span></span>

* <span data-ttu-id="e6e6e-764">更新了创建新的认知服务帐户时的“通知”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-764">Updated the 'notice' when creating a new Cognitive Services account</span></span>

### <a name="consumption"></a><span data-ttu-id="e6e6e-765">消耗</span><span class="sxs-lookup"><span data-stu-id="e6e6e-765">Consumption</span></span>

* <span data-ttu-id="e6e6e-766">为 pricesheet API 添加了新命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-766">Added new commands for pricesheet API</span></span>
* <span data-ttu-id="e6e6e-767">更新了现有“使用情况详细信息”和“预订详细信息”格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-767">Updated the existing Usage Details and Reservation Details formats</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-768">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-768">Container</span></span>

* <span data-ttu-id="e6e6e-769">为 `container create` 添加了 `--secrets` 和 `--secrets-mount-path` 参数以在 ACI 中使用机密</span><span class="sxs-lookup"><span data-stu-id="e6e6e-769">Added `--secrets` and `--secrets-mount-path` arguments to `container create` to use secrets in ACI</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-770">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-770">Network</span></span>

* <span data-ttu-id="e6e6e-771">修复了 [#5559](https://github.com/Azure/azure-cli/issues/5559)：`network vnet-gateway vpn-client generate` 中缺少客户端</span><span class="sxs-lookup"><span data-stu-id="e6e6e-771">Fixed [#5559](https://github.com/Azure/azure-cli/issues/5559): Missing client in `network vnet-gateway vpn-client generate`</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-772">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-772">Resource</span></span>

* <span data-ttu-id="e6e6e-773">更改了 `group deployment export` 以在失败时显示部分模板和错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-773">Changed `group deployment export` to display a partial template and errors on failure</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-774">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-774">Role</span></span>

* <span data-ttu-id="e6e6e-775">添加了 `role assignment list-changelogs` 以允许审核服务主体角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-775">Added `role assignment list-changelogs` to allow auditing of service principal roles</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-776">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-776">SQL</span></span>

* <span data-ttu-id="e6e6e-777">添加了在创建和更新时对数据库和弹性池的区域冗余支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-777">Added zone redundancy support for databases and elastic pools on creation and update</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-778">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-778">Storage</span></span>

* <span data-ttu-id="e6e6e-779">已允许为 `storage blob [upload-batch|download-batch]` 指定 destination-path/prefix</span><span class="sxs-lookup"><span data-stu-id="e6e6e-779">Enabled specifying destination-path/prefix for `storage blob [upload-batch|download-batch]`</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-780">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-780">VM</span></span>

* <span data-ttu-id="e6e6e-781">添加了对在单个 VMSS 实例上附加/分离磁盘的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-781">Added suport for attaching/detatching disks on a single VMSS instance</span></span>


## <a name="february-13-2018"></a><span data-ttu-id="e6e6e-782">2018 年 2 月 13 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-782">February 13, 2018</span></span>

<span data-ttu-id="e6e6e-783">版本 2.0.27</span><span class="sxs-lookup"><span data-stu-id="e6e6e-783">Version 2.0.27</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-784">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-784">Core</span></span>

* <span data-ttu-id="e6e6e-785">更改了同时根据订阅 ID 和在 MSI 登录名对密钥进行身份验证</span><span class="sxs-lookup"><span data-stu-id="e6e6e-785">Changed authentication to key on both subscription ID and name on MSI login</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-786">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-786">ACS</span></span>

* <span data-ttu-id="e6e6e-787">[重大更改] 为了提高准确性，已将 `aks get-versions` 重命名为 `aks get-upgrades`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-787">[BREAKING CHANGE] Renamed `aks get-versions` to `aks get-upgrades` in the interest of accuracy</span></span>
* <span data-ttu-id="e6e6e-788">更改了 `aks get-versions` 以显示可用于 `aks create` 的 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-788">Changed `aks get-versions` to show Kubernetes versions available for `aks create`</span></span>
* <span data-ttu-id="e6e6e-789">更改了 `aks create` 默认值以允许服务器选择 Kubernetes 版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-789">Changed `aks create` defaults to letting the server choose the version of Kubernetes</span></span>
* <span data-ttu-id="e6e6e-790">更新了引用由 AKS 生成的服务主体的帮助消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-790">Updated help messages referring to the service principal generated by AKS</span></span>
* <span data-ttu-id="e6e6e-791">更改了 `aks create` 的默认节点大小，从“Standard\_D1\_v2”更改为“Standard\_DS1\_v2”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-791">Changed default node sizes for `aks create` from "Standard\_D1\_v2" to "Standard\_DS1\_v2"</span></span>
* <span data-ttu-id="e6e6e-792">改进了定位 `az aks browse` 的仪表板 pod 时的可靠性</span><span class="sxs-lookup"><span data-stu-id="e6e6e-792">Improved reliability when locating the dashboard pod for `az aks browse`</span></span>
* <span data-ttu-id="e6e6e-793">修复了 `aks get-credentials` 以便在加载 Kubernetes 配置文件时处理 Unicode 错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-793">Fixed `aks get-credentials` to handle Unicode errors when loading Kubernetes configuration files</span></span>
* <span data-ttu-id="e6e6e-794">向 `az aks install-cli` 添加了一条消息，以便帮助在 `$PATH` 中获取 `kubectl`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-794">Added a message to `az aks install-cli` to help get `kubectl` in `$PATH`</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-795">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-795">Appservice</span></span>

* <span data-ttu-id="e6e6e-796">修复了由于空引用 `webapp [backup|restore]` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-796">Fixed issue where `webapp [backup|restore]` failed because of a null reference</span></span>
* <span data-ttu-id="e6e6e-797">通过 `az configure --defaults appserviceplan=my-asp` 添加了对默认应用服务计划的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-797">Added support for default app service plans through `az configure --defaults appserviceplan=my-asp`</span></span>

### <a name="cdn"></a><span data-ttu-id="e6e6e-798">CDN</span><span class="sxs-lookup"><span data-stu-id="e6e6e-798">CDN</span></span>

* <span data-ttu-id="e6e6e-799">添加了 `cdn custom-domain [enable-https|disable-https]` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-799">Added `cdn custom-domain [enable-https|disable-https]` commands</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-800">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-800">Container</span></span>

* <span data-ttu-id="e6e6e-801">向 `az container logs` 添加了 `--follow` 选项，用于流式传输日志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-801">Added `--follow` option to `az container logs` for streaming logs</span></span>
* <span data-ttu-id="e6e6e-802">添加了 `container attach` 命令，用于将本地标准输出和错误流附加到容器组中的容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-802">Added `container attach` command that attaches local standard output and error streams to a container in a container group</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="e6e6e-803">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-803">CosmosDB</span></span>

* <span data-ttu-id="e6e6e-804">添加了对设置功能的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-804">Added support for setting capabilities</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-805">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-805">Extension</span></span>

* <span data-ttu-id="e6e6e-806">向 `az extension [add|update]` 命令添加了对 `--pip-proxy` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-806">Added support for `--pip-proxy` parameter to `az extension [add|update]` commands</span></span>
* <span data-ttu-id="e6e6e-807">向 `az extension [add|update]` 命令添加了对 `--pip-extra-index-urls` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-807">Added support for `--pip-extra-index-urls` argument to `az extension [add|update]` commands</span></span>

### <a name="feedback"></a><span data-ttu-id="e6e6e-808">反馈</span><span class="sxs-lookup"><span data-stu-id="e6e6e-808">Feedback</span></span>

* <span data-ttu-id="e6e6e-809">将扩展信息添加到了遥测数据</span><span class="sxs-lookup"><span data-stu-id="e6e6e-809">Added extension information to telemetry data</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-810">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-810">Interactive</span></span>

* <span data-ttu-id="e6e6e-811">修复了在 Cloud Shell 中使用交互模式时提示用户登录的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-811">Fixed issue where user is prompted to login when using interactive mode in Cloud Shell</span></span>
* <span data-ttu-id="e6e6e-812">修复了缺少参数补全时的回归问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-812">Fixed regression with missing parameter completions</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-813">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-813">IoT</span></span>

* <span data-ttu-id="e6e6e-814">修复了 `iot dps access policy [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-814">Fixed issue where `iot dps access policy [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="e6e6e-815">修复了 `iot dps linked-hub [create|update]` 在成功时返回“not found”错误的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-815">Fixed issue where `iot dps linked-hub [create|update]` would return a 'not found' error on success</span></span>
* <span data-ttu-id="e6e6e-816">向 `iot dps access policy [create|update]` 和 `iot dps linked-hub [create|update]` 添加了 `--no-wait` 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-816">Added `--no-wait` support to `iot dps access policy [create|update]` and `iot dps linked-hub [create|update]`</span></span>
* <span data-ttu-id="e6e6e-817">更改了 `iot hub create` 以允许指定分区数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-817">Changed `iot hub create` to allow specifying the number of partitions</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-818">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-818">Monitor</span></span>

* <span data-ttu-id="e6e6e-819">修复了 `az monitor log-profiles create` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-819">Fixed `az monitor log-profiles create` command</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-820">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-820">Network</span></span>

* <span data-ttu-id="e6e6e-821">修复了以下命令的 `--tags` 选项：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-821">Fixed the `--tags` option for the following commands:</span></span>
  * `network public-ip create`
  * `network lb create`
  * `network local-gateway create`
  * `network nic create`
  * `network vnet-gateway create`
  * `network vpn-connection create`

### <a name="profile"></a><span data-ttu-id="e6e6e-822">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-822">Profile</span></span>

* <span data-ttu-id="e6e6e-823">在交互模式中启用了 `az login`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-823">Enabled `az login` in from interactive mode</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-824">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-824">Resource</span></span>

* <span data-ttu-id="e6e6e-825">重新添加了 `feature show`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-825">Added back `feature show`</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-826">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-826">Role</span></span>

* <span data-ttu-id="e6e6e-827">为 `ad app update` 添加了 `--available-to-other-tenants` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-827">Added `--available-to-other-tenants` argument to `ad app update`</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-828">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-828">SQL</span></span>

* <span data-ttu-id="e6e6e-829">添加了 `sql server dns-alias` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-829">Added `sql server dns-alias` commands</span></span>
* <span data-ttu-id="e6e6e-830">添加了 `sql db rename`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-830">Added `sql db rename`</span></span>
* <span data-ttu-id="e6e6e-831">向所有 sql 命令添加了对 `--ids` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-831">Added support for the `--ids` argument to all sql commands</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-832">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-832">Storage</span></span>

* <span data-ttu-id="e6e6e-833">添加了 `storage blob service-properties delete-policy` 和 `storage blob undelete` 命令以启用软删除</span><span class="sxs-lookup"><span data-stu-id="e6e6e-833">Added `storage blob service-properties delete-policy` and `storage blob undelete` commands to enable soft-delete</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-834">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-834">VM</span></span>

* <span data-ttu-id="e6e6e-835">修复了无法完全初始化 VM 加密时出现的崩溃</span><span class="sxs-lookup"><span data-stu-id="e6e6e-835">Fixed a crash when VM encryption may not be fully initialized</span></span>
* <span data-ttu-id="e6e6e-836">添加了启用 MSI 时的主体 ID 输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-836">Added principal ID output on enabling MSI</span></span>
* <span data-ttu-id="e6e6e-837">固定 `vm boot-diagnostics get-boot-log`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-837">Fixed `vm boot-diagnostics get-boot-log`</span></span>


## <a name="january-31-2018"></a><span data-ttu-id="e6e6e-838">2018 年 1 月 31 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-838">January 31, 2018</span></span>

<span data-ttu-id="e6e6e-839">版本 2.0.26</span><span class="sxs-lookup"><span data-stu-id="e6e6e-839">Version 2.0.26</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-840">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-840">Core</span></span>

* <span data-ttu-id="e6e6e-841">添加了支持在 MSI 上下文中检索原始令牌</span><span class="sxs-lookup"><span data-stu-id="e6e6e-841">Added support raw token retrival in MSI context</span></span>
* <span data-ttu-id="e6e6e-842">删除了完成对 Windows cmd.exe 进行 LRO 操作后轮询指示器字符串</span><span class="sxs-lookup"><span data-stu-id="e6e6e-842">Removed polling indicator string after finishing LRO on Windows cmd.exe</span></span>
* <span data-ttu-id="e6e6e-843">添加了将使用配置的默认值时显示的警告更改为信息级别条目。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-843">Added a warning that appears when using a configured default has been changed to an INFO level entry.</span></span> <span data-ttu-id="e6e6e-844">请使用 `--verbose` 查看</span><span class="sxs-lookup"><span data-stu-id="e6e6e-844">Use `--verbose` to see</span></span>
* <span data-ttu-id="e6e6e-845">为等待命令添加了进度指示器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-845">Add a progress indicator for wait commands</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-846">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-846">ACS</span></span>

* <span data-ttu-id="e6e6e-847">说明了 `--disable-browser` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-847">Clarified `--disable-browser` argument</span></span>
* <span data-ttu-id="e6e6e-848">改进了 `--vm-size` 参数的 tab 键补全功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-848">Improved tab completion for `--vm-size` arguments</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-849">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-849">Appservice</span></span>

* <span data-ttu-id="e6e6e-850">固定 `webapp log [tail|download]`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-850">Fixed `webapp log [tail|download]`</span></span>
* <span data-ttu-id="e6e6e-851">删除了对 Web 应用和函数的 `kind` 检查</span><span class="sxs-lookup"><span data-stu-id="e6e6e-851">Removed the `kind` check on webapps and functions</span></span>

### <a name="cdn"></a><span data-ttu-id="e6e6e-852">CDN</span><span class="sxs-lookup"><span data-stu-id="e6e6e-852">CDN</span></span>

* <span data-ttu-id="e6e6e-853">修复了运行 `cdn custom-domain create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-853">Fixed missing client issue with `cdn custom-domain create`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="e6e6e-854">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-854">CosmosDB</span></span>

* <span data-ttu-id="e6e6e-855">修复了故障转移策略的参数说明</span><span class="sxs-lookup"><span data-stu-id="e6e6e-855">Fixed parameter description for failover policies</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-856">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-856">Interactive</span></span>

* <span data-ttu-id="e6e6e-857">修复了不再显示命令选项补全的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-857">Fixed issue where command option completions no longer appeared</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-858">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-858">Network</span></span>

* <span data-ttu-id="e6e6e-859">向 `application-gateway create` 添加了对 `--cert-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="e6e6e-859">Added protection for `--cert-password` to `application-gateway create`</span></span>
* <span data-ttu-id="e6e6e-860">修复了 `application-gateway update` 出现的 `--sku` 错误应用默认值的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-860">Fixed issue with `application-gateway update` where `--sku` erroneously applied a default value</span></span>
* <span data-ttu-id="e6e6e-861">向 `vpn-connection create` 添加了对 `--shared-key` 和 `--authorization-key` 的保护</span><span class="sxs-lookup"><span data-stu-id="e6e6e-861">Added protection for `--shared-key` and `--authorization-key` to `vpn-connection create`</span></span>
* <span data-ttu-id="e6e6e-862">修复了运行 `asg create` 时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-862">Fixed missing client issue with `asg create`</span></span>
* <span data-ttu-id="e6e6e-863">向 `dns zone export` 添加了用于导出名称的 `--file-name / -f` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-863">Added `--file-name / -f` parameter for exported names to `dns zone export`</span></span>
* <span data-ttu-id="e6e6e-864">修复了 `dns zone export` 存在的以下问题：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-864">Fixed the following issues with `dns zone export`:</span></span>
  * <span data-ttu-id="e6e6e-865">修复了未正确导出长 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-865">Fixed issue where long TXT records were incorrectly exported</span></span>
  * <span data-ttu-id="e6e6e-866">修复了不使用转义引号无法正确导出带引号的 TXT 记录的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-866">Fixed issue where quoted TXT records were incorrectly exported without escaped quotes</span></span>
* <span data-ttu-id="e6e6e-867">修复了使用 `dns zone import` 某些记录会导入两次的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-867">Fixed issue where certain records were imported twice with `dns zone import`</span></span>
* <span data-ttu-id="e6e6e-868">已还原 `vnet-gateway root-cert` 和 `vnet-gateway revoked-cert` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-868">Restored `vnet-gateway root-cert` and `vnet-gateway revoked-cert` commands</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-869">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-869">Profile</span></span>

* <span data-ttu-id="e6e6e-870">修复了 `get-access-token`，使其在 VM 中使用标识正常工作</span><span class="sxs-lookup"><span data-stu-id="e6e6e-870">Fixed `get-access-token` to work inside a VM with identity</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-871">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-871">Resource</span></span>

* <span data-ttu-id="e6e6e-872">修复了 `deployment [create|validate]` 存在的 bug，即当模板的 type 字段包含大写值时错误地显示警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-872">Fixed bug with `deployment [create|validate]` where warning was incorrectly displayed when a template 'type' field contained uppercase values</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-873">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-873">Storage</span></span>

* <span data-ttu-id="e6e6e-874">修复了将存储 V1 帐户迁移到存储 V2 时出现的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-874">Fixed issue with migrating Storage V1 accounts to Storage V2</span></span>
* <span data-ttu-id="e6e6e-875">为所有上传/下载命令添加了进度报告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-875">Added progress reporting for all upload/download commands</span></span>
* <span data-ttu-id="e6e6e-876">修复了 `storage account check-name` 不显示“-n”参数选项的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-876">Fixed bug preventing "-n" arg option with `storage account check-name`</span></span>
* <span data-ttu-id="e6e6e-877">向 `blob [list|show]` 的表输出添加了“snapshot”列</span><span class="sxs-lookup"><span data-stu-id="e6e6e-877">Added 'snapshot' column to table output for `blob [list|show]`</span></span>
* <span data-ttu-id="e6e6e-878">修复了需要作为整数分析的各种参数的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-878">Fixed bugs with various parameters that needed to be parsed as ints</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-879">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-879">VM</span></span>

* <span data-ttu-id="e6e6e-880">添加了 `vm image accept-terms` 命令，以允许使用额外费用从映像创建 VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-880">Added `vm image accept-terms` command to allow creating VMs from images with additional charges</span></span>
* <span data-ttu-id="e6e6e-881">修复了 `[vm|vmss create]`，以确保可以在使用未签名证书的代理下运行命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-881">Fixed `[vm|vmss create]` to ensure commands can run under proxy with unsigned certificates</span></span>
* <span data-ttu-id="e6e6e-882">[预览] 向 VMSS 添加了对“低”优先级的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-882">[PREVIEW] Added support for "low" priority to VMSS</span></span>
* <span data-ttu-id="e6e6e-883">向 `[vm|vmss] create` 添加了对 `--admin-password` 的保护</span><span class="sxs-lookup"><span data-stu-id="e6e6e-883">Added protection for `--admin-password` to `[vm|vmss] create`</span></span>


## <a name="january-17-2018"></a><span data-ttu-id="e6e6e-884">2018 年 1 月 17 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-884">January 17, 2018</span></span>

<span data-ttu-id="e6e6e-885">版本 2.0.25</span><span class="sxs-lookup"><span data-stu-id="e6e6e-885">Version 2.0.25</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-886">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-886">ACR</span></span>

* <span data-ttu-id="e6e6e-887">添加了发生 Windows 凭据错误时执行 acr 登录回退的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-887">Added acr login fallback on Windows credential errors</span></span>
* <span data-ttu-id="e6e6e-888">启用了注册表日志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-888">Enabled registry logs</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-889">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-889">ACS</span></span>

* <span data-ttu-id="e6e6e-890">修复了 `get-credentials` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-890">Fixed `get-credentials` command</span></span>
* <span data-ttu-id="e6e6e-891">删除了 SPN 角色要求</span><span class="sxs-lookup"><span data-stu-id="e6e6e-891">Removed SPN role requirement</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-892">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-892">Appservice</span></span>

* <span data-ttu-id="e6e6e-893">修复了 `hosting_environment_profile` 为 null 时 `config ssl upload` 存在的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-893">Fixed bug with `config ssl upload` where `hosting_environment_profile` was null</span></span>
* <span data-ttu-id="e6e6e-894">为 `browse` 添加了自定义 URL 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-894">Added support for custom URLs to `browse`</span></span>
* <span data-ttu-id="e6e6e-895">修复了 `log tail` 的槽位支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-895">Fixed slot support for `log tail`</span></span>

### <a name="backup"></a><span data-ttu-id="e6e6e-896">备份</span><span class="sxs-lookup"><span data-stu-id="e6e6e-896">Backup</span></span>

* <span data-ttu-id="e6e6e-897">将 `backup item list` 的 `--container-name` 选项更改为可选</span><span class="sxs-lookup"><span data-stu-id="e6e6e-897">Changed `--container-name` option of `backup item list` to be optional</span></span>
* <span data-ttu-id="e6e6e-898">为 `backup restore restore-disks` 添加了存储帐户选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-898">Added storage account options to `backup restore restore-disks`</span></span>
* <span data-ttu-id="e6e6e-899">修复了 `backup protection enable-for-vm` 中的位置检查，使之区分大小写</span><span class="sxs-lookup"><span data-stu-id="e6e6e-899">Fixed location check in `backup protection enable-for-vm` to be case insensitive</span></span>
* <span data-ttu-id="e6e6e-900">修复了容器名称无效时命令失败的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-900">Fixed issue where commands failed with an invalid container name</span></span>
* <span data-ttu-id="e6e6e-901">已将 `backup item list` 更改为默认包含“Health Status”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-901">Changed `backup item list` to include 'Health Status' by default</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-902">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-902">Batch</span></span>

* <span data-ttu-id="e6e6e-903">已将 `batch login` 更改为返回身份验证详细信息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-903">Changed `batch login` to return authentication details</span></span>

### <a name="cloud"></a><span data-ttu-id="e6e6e-904">云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-904">Cloud</span></span>

* <span data-ttu-id="e6e6e-905">已更改为在云中设置 `--profile` 时不需要终结点</span><span class="sxs-lookup"><span data-stu-id="e6e6e-905">Changed to not require endpoints when setting `--profile` on a cloud</span></span>

### <a name="consumption"></a><span data-ttu-id="e6e6e-906">消耗</span><span class="sxs-lookup"><span data-stu-id="e6e6e-906">Consumption</span></span>

* <span data-ttu-id="e6e6e-907">添加了用于预留的新命令：`consumption reservations summaries` 和 `consumption reservations details`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-907">Added new commands for reservations: `consumption reservations summaries` and `consumption reservations details`</span></span>

### <a name="event-grid"></a><span data-ttu-id="e6e6e-908">事件网格</span><span class="sxs-lookup"><span data-stu-id="e6e6e-908">Event Grid</span></span>

* <span data-ttu-id="e6e6e-909">[重大更改] 已将 `az eventgrid topic event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-909">[BREAKING CHANGE] Moved the `az eventgrid topic event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="e6e6e-910">[重大更改] 已将 `az eventgrid resource event-subscription` 命令变动为 `eventgrid event-subscription`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-910">[BREAKING CHANGE] Moved the `az eventgrid resource event-subscription` commands to `eventgrid event-subscription`</span></span>
* <span data-ttu-id="e6e6e-911">[重大更改] 已删除 `eventgrid event-subscription show-endpoint-url` 命令。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-911">[BREAKING CHANGE] Removed the `eventgrid event-subscription show-endpoint-url` command.</span></span> <span data-ttu-id="e6e6e-912">请改用 `eventgrid event-subscription show --include-full-endpoint-url`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-912">Use `eventgrid event-subscription show --include-full-endpoint-url` instead</span></span>
* <span data-ttu-id="e6e6e-913">添加了命令 `eventgrid topic update`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-913">Added command `eventgrid topic update`</span></span>
* <span data-ttu-id="e6e6e-914">添加了命令 `eventgrid event-subscription update`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-914">Added command `eventgrid event-subscription update`</span></span>
* <span data-ttu-id="e6e6e-915">为 `eventgrid topic` 命令添加了 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-915">Added `--ids` parameter for `eventgrid topic` commands</span></span>
* <span data-ttu-id="e6e6e-916">添加了主题名称的 Tab 键补全支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-916">Added tab completion support for topic names</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-917">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-917">Interactive</span></span>

* <span data-ttu-id="e6e6e-918">修复了无法在 Python 2.x 中使用交互模式的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-918">Fixed issue where interactive mode did not work with Python 2.x</span></span>
* <span data-ttu-id="e6e6e-919">修复了启动时出错的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-919">Fixed errors on startup</span></span>
* <span data-ttu-id="e6e6e-920">修复了无法在交互模式下运行某些命令的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-920">Fixed issue with some commands not running in interactive mode</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-921">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-921">IoT</span></span>

* <span data-ttu-id="e6e6e-922">添加了对设备预配服务的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-922">Added support for device provisioning service</span></span>
* <span data-ttu-id="e6e6e-923">在命令和命令帮助中添加了弃用消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-923">Added deprecation messages in commands and command help</span></span>
* <span data-ttu-id="e6e6e-924">添加了 IoT 检查，以告知用户有 IoT 扩展可用</span><span class="sxs-lookup"><span data-stu-id="e6e6e-924">Added IoT check to inform users of the IoT Extension</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-925">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-925">Monitor</span></span>

* <span data-ttu-id="e6e6e-926">添加了多诊断设置支持。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-926">Added multi-diagnostic setting support.</span></span> <span data-ttu-id="e6e6e-927">`az monitor diagnostic-settings create` 现在必需 `--name` 参数。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-927">The `--name` parameter is now required for `az monitor diagnostic-settings create`</span></span>
* <span data-ttu-id="e6e6e-928">添加了命令 `monitor diagnostic-settings categories` 用于获取诊断设置类别</span><span class="sxs-lookup"><span data-stu-id="e6e6e-928">Added command `monitor diagnostic-settings categories` to get diagnostic settings category</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-929">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-929">Network</span></span>

* <span data-ttu-id="e6e6e-930">修复了使用 `vnet-gateway update` 进入/退出主动-待机模式时出现的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-930">Fixed issue when trying to change to/from active-standby mode with `vnet-gateway update`</span></span>
* <span data-ttu-id="e6e6e-931">在 `application-gateway [create|update]` 中添加了对 HTTP2 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-931">Added support for HTTP2 to `application-gateway [create|update]`</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-932">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-932">Profile</span></span>

* <span data-ttu-id="e6e6e-933">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-933">Added support for login with user assigned identities</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-934">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-934">Role</span></span>

* <span data-ttu-id="e6e6e-935">为 `role assignment create` 添加了 `--assignee-object-id` 参数用于绕过图形查询</span><span class="sxs-lookup"><span data-stu-id="e6e6e-935">Added `--assignee-object-id` argument to `role assignment create` to bypass graph query</span></span>

### <a name="service-fabric"></a><span data-ttu-id="e6e6e-936">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e6e6e-936">Service Fabric</span></span>

* <span data-ttu-id="e6e6e-937">在创建群集时生成的验证响应中添加了详细错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-937">Added detailed errors to validation response when creating cluster</span></span>
* <span data-ttu-id="e6e6e-938">修复了运行多个命令时出现的缺少客户端问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-938">Fixed missing client issue with several commands</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-939">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-939">VM</span></span>

* <span data-ttu-id="e6e6e-940">[预览] `vmss` 的跨区域支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-940">[PREVIEW] Cross-zone support for `vmss`</span></span>
* <span data-ttu-id="e6e6e-941">[重大更改] 已将单区域 `vmss` 默认值更改为“Standard”负载均衡器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-941">[BREAKING CHANGE] Changed single-zone `vmss` default to "Standard" load balancer</span></span>
* <span data-ttu-id="e6e6e-942">[重大更改] 已将EMSI 的 `externalIdentities` 更改为 `userAssignedIdentities`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-942">[BREAKING CHANGE] Changed `externalIdentities` to `userAssignedIdentities` for EMSI</span></span>
* <span data-ttu-id="e6e6e-943">[预览] 添加了 OS 磁盘交换支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-943">[PREVIEW] Added support for OS disk swap</span></span>
* <span data-ttu-id="e6e6e-944">添加了使用其他订阅中的 VM 映像的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-944">Added support for using VM images from other subscriptions</span></span>
* <span data-ttu-id="e6e6e-945">为 `[vm|vmss] create` 添加了 `--plan-name`、`--plan-product`、`--plan-promotion-code` 和 `--plan-publisher` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-945">Added `--plan-name`, `--plan-product`, `--plan-promotion-code` and `--plan-publisher` arguments to `[vm|vmss] create`</span></span>
* <span data-ttu-id="e6e6e-946">修复了 `[vm|vmss] create` 出错问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-946">Fixed error issues with `[vm|vmss] create`</span></span>
* <span data-ttu-id="e6e6e-947">修复了 `vm image list --all` 导致资源使用过度的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-947">Fixed excessive resource usage caused by `vm image list --all`</span></span>

## <a name="december-19-2017"></a><span data-ttu-id="e6e6e-948">2017 年 12 月 19 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-948">December 19, 2017</span></span>

<span data-ttu-id="e6e6e-949">版本 2.0.23</span><span class="sxs-lookup"><span data-stu-id="e6e6e-949">Version 2.0.23</span></span>

* <span data-ttu-id="e6e6e-950">添加了使用用户分配的标识进行登录的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-950">Added support for login with user assigned identities</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-951">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-951">Container</span></span>

* <span data-ttu-id="e6e6e-952">纠正了容器日志参数的错误顺序</span><span class="sxs-lookup"><span data-stu-id="e6e6e-952">Fixed incorrect order of parameters for container logs</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-953">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-953">Network</span></span>

* <span data-ttu-id="e6e6e-954">为 `route-table [create|update]` 添加了 `--disable-bgp-route-propagation` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-954">Added `--disable-bgp-route-propagation` argument to `route-table [create|update]`</span></span>
* <span data-ttu-id="e6e6e-955">为 `public-ip [create|update]` 添加了 `--ip-tags` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-955">Added `--ip-tags` argument to `public-ip [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-956">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-956">Storage</span></span>

* <span data-ttu-id="e6e6e-957">添加了对存储 V2 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-957">Added support for storage V2</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-958">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-958">VM</span></span>

* <span data-ttu-id="e6e6e-959">[预览] 添加了对 VM 和 VMSS 的用户分配标识的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-959">[PREVIEW] Added support for user-assigned identities for VMs and VMSSes</span></span>


## <a name="december-5-2017"></a><span data-ttu-id="e6e6e-960">2017 年 12 月 5 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-960">December 5, 2017</span></span>

<span data-ttu-id="e6e6e-961">版本 2.0.22</span><span class="sxs-lookup"><span data-stu-id="e6e6e-961">Version 2.0.22</span></span>

* <span data-ttu-id="e6e6e-962">已删除 `az component` 命令。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-962">Removed `az component` commands.</span></span> <span data-ttu-id="e6e6e-963">请改用 `az extension`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-963">Use `az extension` instead</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-964">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-964">Core</span></span>
* <span data-ttu-id="e6e6e-965">已将 `AZURE_US_GOV_CLOUD` AAD 颁发机构终结点从 login.microsoftonline.com 修改为 login.microsoftonline.us</span><span class="sxs-lookup"><span data-stu-id="e6e6e-965">Modified the `AZURE_US_GOV_CLOUD` AAD authority endpoint from login.microsoftonline.com to login.microsoftonline.us</span></span>
* <span data-ttu-id="e6e6e-966">已修复持续重新发送遥测数据的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-966">Fixed issue where telemetry would continuously resend</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-967">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-967">ACS</span></span>

* <span data-ttu-id="e6e6e-968">已添加 `aks install-connector` 和 `aks remove-connector` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-968">Added `aks install-connector` and `aks remove-connector` commands</span></span>
* <span data-ttu-id="e6e6e-969">已改进 `acs create` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-969">Improved error reporting for `acs create`</span></span>
* <span data-ttu-id="e6e6e-970">已修复不带完全限定路径的 `aks get-credentials -f` 的用法</span><span class="sxs-lookup"><span data-stu-id="e6e6e-970">Fixed usage of `aks get-credentials -f` without fully-qualified path</span></span>

### <a name="advisor"></a><span data-ttu-id="e6e6e-971">顾问</span><span class="sxs-lookup"><span data-stu-id="e6e6e-971">Advisor</span></span>

* <span data-ttu-id="e6e6e-972">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-972">Initial release</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-973">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-973">Appservice</span></span>

* <span data-ttu-id="e6e6e-974">已修复使用 `webapp config ssl upload` 时的证书名称生成问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-974">Fixed cert name generation with `webapp config ssl upload`</span></span>
* <span data-ttu-id="e6e6e-975">已修复 `webapp [list|show]` 和 `functionapp [list|show]` 以显示正确的应用</span><span class="sxs-lookup"><span data-stu-id="e6e6e-975">Fixed `webapp [list|show]` and `functionapp [list|show]` to display correct apps</span></span>
* <span data-ttu-id="e6e6e-976">已为 `WEBSITE_NODE_DEFAULT_VERSION` 添加了默认值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-976">Added default value for `WEBSITE_NODE_DEFAULT_VERSION`</span></span>

### <a name="consumption"></a><span data-ttu-id="e6e6e-977">消耗</span><span class="sxs-lookup"><span data-stu-id="e6e6e-977">Consumption</span></span>

* <span data-ttu-id="e6e6e-978">已添加对 API 版本 2017-11-30 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-978">Aded support for API version 2017-11-30</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-979">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-979">Container</span></span>

* <span data-ttu-id="e6e6e-980">已修复默认端口回归</span><span class="sxs-lookup"><span data-stu-id="e6e6e-980">Fixed default ports regression</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-981">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-981">Monitor</span></span>

* <span data-ttu-id="e6e6e-982">已添加对指标命令的多维支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-982">Added multi-dimension support to metrics command</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-983">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-983">Resource</span></span>

* <span data-ttu-id="e6e6e-984">为 `resource show` 添加了 `--include-response-body` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-984">Added `--include-response-body` argument to `resource show`</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-985">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-985">Role</span></span>

* <span data-ttu-id="e6e6e-986">已将“经典”管理员的默认分配显示添加到 `role assignment list`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-986">Added display of default assignments for "classic" administraors to `role assignment list`</span></span>
* <span data-ttu-id="e6e6e-987">已添加对 `ad sp reset-credentials` 的支持以便添加凭据而不是覆盖</span><span class="sxs-lookup"><span data-stu-id="e6e6e-987">Added suport to `ad sp reset-credentials` for adding credentials instead of overwriting</span></span>
* <span data-ttu-id="e6e6e-988">已改进 `ad sp create-for-rbac` 的错误报告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-988">Improved error reporting for `ad sp create-for-rbac`</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-989">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-989">SQL</span></span>

* <span data-ttu-id="e6e6e-990">已添加 `sql db list-usages` 和 `sql db show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-990">Added `sql db list-usages` and `sql db show-usage` commands</span></span>
* <span data-ttu-id="e6e6e-991">已添加 `sql server conn-policy show` 和 `sql server conn-policy update` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-991">Added `sql server conn-policy show` and `sql server conn-policy update` commands</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-992">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-992">VM</span></span>

* <span data-ttu-id="e6e6e-993">已对 `az vm list-skus` 添加区域信息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-993">Added zone information to `az vm list-skus`</span></span>


## <a name="november-14-2017"></a><span data-ttu-id="e6e6e-994">2017 年 11 月 14 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-994">November 14, 2017</span></span>

<span data-ttu-id="e6e6e-995">版本 2.0.21</span><span class="sxs-lookup"><span data-stu-id="e6e6e-995">Version 2.0.21</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-996">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-996">ACR</span></span>

* <span data-ttu-id="e6e6e-997">添加了在复制区域中创建 Webhook 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-997">Added support for creating webhooks in replication regions</span></span>


### <a name="acs"></a><span data-ttu-id="e6e6e-998">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-998">ACS</span></span>

* <span data-ttu-id="e6e6e-999">已在 AKS 中将所有“代理”一词更改为“节点”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-999">Changed all wording of "agent" to "node" in AKS</span></span>
* <span data-ttu-id="e6e6e-1000">弃用了 `acs create` 的 `--orchestrator-release` 选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1000">Deprecated `--orchestrator-release` option for `acs create`</span></span>
* <span data-ttu-id="e6e6e-1001">已将 AKS 的默认 VM 大小更改为 `Standard_D1_v2`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1001">Changed default VM size for AKS to `Standard_D1_v2`</span></span>
* <span data-ttu-id="e6e6e-1002">在 Windows 上修复了 `az aks browse`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1002">Fixed `az aks browse` on Windows</span></span>
* <span data-ttu-id="e6e6e-1003">在 Windows 上修复了 `az aks get-credentials`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1003">Fixed `az aks get-credentials` on Windows</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1004">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1004">Appservice</span></span>

* <span data-ttu-id="e6e6e-1005">添加了 Web 应用和函数应用的部署源 `config-zip`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1005">Added deployment source `config-zip` for webapps and function apps</span></span>
* <span data-ttu-id="e6e6e-1006">为 `az webapp log config` 添加了 `--docker-container-logging` 选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1006">Added `--docker-container-logging` option to `az webapp log config`</span></span>
* <span data-ttu-id="e6e6e-1007">从 `az webapp log config` 的参数 `--web-server-logging` 中删除了 `storage` 选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1007">Removed the `storage` option from the parameter `--web-server-logging` of `az webapp log config`</span></span>
* <span data-ttu-id="e6e6e-1008">完善了 `deployment user set` 的错误消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1008">Improved error messages for `deployment user set`</span></span>
* <span data-ttu-id="e6e6e-1009">添加了创建 Linux 函数应用的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1009">Added support for creating Linux function apps</span></span>
* <span data-ttu-id="e6e6e-1010">固定 `list-locations`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1010">Fixed `list-locations`</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-1011">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1011">Batch</span></span>

* <span data-ttu-id="e6e6e-1012">修复了在 pool create 命令中结合 `--image` 标志使用资源 ID 时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1012">Fixed bug in pool create command when a resource ID was used with the `--image` flag</span></span>

### <a name="batchai"></a><span data-ttu-id="e6e6e-1013">Batchai</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1013">Batchai</span></span>

* <span data-ttu-id="e6e6e-1014">在 `file-server create` 命令中提供了 `--vm-size` 的简短选项 `-s`（提供 VM 大小）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1014">Added short option, `-s`, for `--vm-size` when providing VM size in `file-server create` command</span></span>
* <span data-ttu-id="e6e6e-1015">为 `cluster create` 参数添加了存储帐户名称和密钥自变量</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1015">Added storage account name and key arguments to `cluster create` parameters</span></span>
* <span data-ttu-id="e6e6e-1016">纠正了 `job list-files` 和 `job stream-file` 的文档</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1016">Fixed documentation for `job list-files` and `job stream-file`</span></span>
* <span data-ttu-id="e6e6e-1017">在 `job create` 命令中提供了 `--cluster-name` 的简短选项 `-r`（提供群集名称）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1017">Added short option, `-r`, for `--cluster-name` when providing cluster name in `job create` command</span></span>

### <a name="cloud"></a><span data-ttu-id="e6e6e-1018">云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1018">Cloud</span></span>

* <span data-ttu-id="e6e6e-1019">更改了 `cloud [register|update]`，以防止注册缺少所需终结点的云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1019">Changed `cloud [register|update]` to prevent registering clouds that have missing required endpoints</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-1020">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1020">Container</span></span>

* <span data-ttu-id="e6e6e-1021">添加了打开多个端口的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1021">Added support to open multiple ports</span></span>
* <span data-ttu-id="e6e6e-1022">添加了容器组重启策略</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1022">Added container group restart policy</span></span>
* <span data-ttu-id="e6e6e-1023">添加了将 Azure 文件共享装载为卷的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1023">Added support to mount Azure File share as a volume</span></span>
* <span data-ttu-id="e6e6e-1024">更新了帮助器文档</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1024">Updated helper docs</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="e6e6e-1025">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1025">Data Lake Analytics</span></span>

* <span data-ttu-id="e6e6e-1026">更改了 `[job|account] list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1026">Changed `[job|account] list` to return more concise information</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="e6e6e-1027">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1027">Data Lake Store</span></span>

* <span data-ttu-id="e6e6e-1028">更改了 `account list` 以返回更简洁的信息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1028">Changed `account list` to return more concise information</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-1029">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1029">Extension</span></span>

* <span data-ttu-id="e6e6e-1030">添加了 `extension list-available` 用于列出官方的 Microsoft 扩展</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1030">Added `extension list-available` to allow listing official Microsoft extensions</span></span>
* <span data-ttu-id="e6e6e-1031">为 `extension [add|update]` 添加了 `--name`，以便按名称安装扩展</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1031">Added `--name` to `extension [add|update]` to allow installing extensions by name</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-1032">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1032">IoT</span></span>

* <span data-ttu-id="e6e6e-1033">添加了对证书颁发机构 (CA) 和证书链的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1033">Added support for certificate authorities (CA) and certificate chains</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-1034">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1034">Monitor</span></span>

* <span data-ttu-id="e6e6e-1035">添加了 `activity-log alert` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1035">Added `activity-log alert` commands</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1036">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1036">Network</span></span>

* <span data-ttu-id="e6e6e-1037">添加了对 CAA DNS 记录的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1037">Added support for CAA DNS records</span></span>
* <span data-ttu-id="e6e6e-1038">修复了无法使用 `traffic-manager profile update` 更新终结点的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1038">Fixed issue where endpoints could not be updated with `traffic-manager profile update`</span></span>
* <span data-ttu-id="e6e6e-1039">修复了在采用某种 VNET 创建方式时 `vnet update --dns-servers` 无法正常运行的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1039">Fixed issue where `vnet update --dns-servers` didn't work depending on how the VNET was created</span></span>
* <span data-ttu-id="e6e6e-1040">修复了 `dns zone import` 错误导入相对 DNS 名称的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1040">Fixed issue where relative DNS names were incorrectly imported by `dns zone import`</span></span>

### <a name="reservations"></a><span data-ttu-id="e6e6e-1041">预留</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1041">Reservations</span></span>

* <span data-ttu-id="e6e6e-1042">初始预览版</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1042">Initial preview release</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1043">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1043">Resource</span></span>

* <span data-ttu-id="e6e6e-1044">添加了在 `--resource` 参数中指定资源 ID 的支持，以及对资源级锁的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1044">Added support for resource IDs to `--resource` parameter and resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-1045">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1045">SQL</span></span>

* <span data-ttu-id="e6e6e-1046">为 `sql server vnet-rule [create|update]` 添加了 `--ignore-missing-vnet-service-endpoint` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1046">Added `--ignore-missing-vnet-service-endpoint` parameter to `sql server vnet-rule [create|update]`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1047">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1047">Storage</span></span>

* <span data-ttu-id="e6e6e-1048">更改了 `storage account create` 以使用 SKU `Standard_RAGRS` 作为默认值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1048">Changed `storage account create` to use SKU `Standard_RAGRS` as default</span></span>
* <span data-ttu-id="e6e6e-1049">修复了处理包含非 ASCII 字符的文件/Blob 名称时出现的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1049">Fixed bugs when dealing with file/blob names that include non-ascii chars</span></span>
* <span data-ttu-id="e6e6e-1050">修复了阻止在 `storage [blob|file] copy start-batch` 中使用 `--source-uri` 的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1050">Fixed bug that prevented using `--source-uri` with `storage [blob|file] copy start-batch`</span></span>
* <span data-ttu-id="e6e6e-1051">添加了在 `storage [blob|file] delete-batch` 中包含和删除多个对象的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1051">Added commands to glob and delete multiple objects with `storage [blob|file] delete-batch`</span></span>
* <span data-ttu-id="e6e6e-1052">修复了使用 `storage metrics update` 启用指标时出现的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1052">Fixed issue when enabling metrics with `storage metrics update`</span></span>
* <span data-ttu-id="e6e6e-1053">修复了使用 `storage blob upload-batch` 时，如果文件超过 200GB 所出现的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1053">Fixed issue with files over 200GB when using `storage blob upload-batch`</span></span>
* <span data-ttu-id="e6e6e-1054">修复了 `storage account [create|update]` 忽略 `--bypass` 和 `--default-action` 的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1054">Fixed issue where `--bypass` and `--default-action` were ignored by `storage account [create|update]`</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1055">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1055">VM</span></span>

* <span data-ttu-id="e6e6e-1056">修复了 `vmss create` 阻止使用 `Basic` 大小层的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1056">Fixed a bug with `vmss create` that prevented using the `Basic` size tier</span></span>
* <span data-ttu-id="e6e6e-1057">针对包含计费信息的自定义映像，为 `[vm|vmss] create` 添加了 `--plan` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1057">Added `--plan` arguments to `[vm|vmss] create` for custom images with billing information</span></span>
* <span data-ttu-id="e6e6e-1058">添加了 `vm secret `[add|remove|list]\` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1058">Added `vm secret `[add|remove|list]\` commands</span></span>
* <span data-ttu-id="e6e6e-1059">已将 `vm format-secret` 重命名为 `vm secret format`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1059">Renamed `vm format-secret` to `vm secret format`</span></span>
* <span data-ttu-id="e6e6e-1060">为 `vm encryption enable` 添加了 `--encrypt format` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1060">Added `--encrypt format` argument to `vm encryption enable`</span></span>

## <a name="october-24-2017"></a><span data-ttu-id="e6e6e-1061">2017 年 10 月 24 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1061">October 24, 2017</span></span>

<span data-ttu-id="e6e6e-1062">版本 2.0.20</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1062">Version 2.0.20</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-1063">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1063">Core</span></span>

* <span data-ttu-id="e6e6e-1064">已更新 `2017-03-09-profile` 以使用 `MGMT_STORAGE` API 版本 `2016-01-01`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1064">Updated `2017-03-09-profile` to consume `MGMT_STORAGE` API version `2016-01-01`</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-1065">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1065">ACR</span></span>

* <span data-ttu-id="e6e6e-1066">已更新资源管理以指向 `2017-10-01` API 版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1066">Updated resource management to point to `2017-10-01` API version</span></span>
* <span data-ttu-id="e6e6e-1067">已将“带来你自己的存储”SKU 更改为“经典”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1067">Changed 'bring your own storage' SKU to Classic</span></span>
* <span data-ttu-id="e6e6e-1068">已将注册表 SKU 重命名为“基本”、“标准”和“高级”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1068">Renamed registry SKUs to Basic, Standard, and Premium</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1069">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1069">ACS</span></span>

* <span data-ttu-id="e6e6e-1070">[PREVIEW] 添加了 `az aks` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1070">[PREVIEW] Added `az aks` commands</span></span>
* <span data-ttu-id="e6e6e-1071">已修复 Kubernetes `get-credentials`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1071">Fixed kubernetes `get-credentials`</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1072">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1072">Appservice</span></span>

* <span data-ttu-id="e6e6e-1073">已修复所下载 `webapp` 日志可能无效的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1073">Fixed issue where downloaded `webapp` logs may be invalid</span></span>

### <a name="component"></a><span data-ttu-id="e6e6e-1074">组件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1074">Component</span></span>

* <span data-ttu-id="e6e6e-1075">为所有安装程序添加了更清晰的弃用消息并添加了确认提示</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1075">Added clearer deprecation message for all installers and confirmation prompt</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-1076">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1076">Monitor</span></span>

* <span data-ttu-id="e6e6e-1077">添加了 `action-group` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1077">Added `action-group` commands</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1078">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1078">Resource</span></span>

* <span data-ttu-id="e6e6e-1079">修复了 `group export` 中与 msrest 依赖项的最新版本不兼容的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1079">Fixed incompatibility with most recent version of msrest dependency in `group export`</span></span>
* <span data-ttu-id="e6e6e-1080">修复了 `policy assignment create` 以使用内置策略定义和策略集定义</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1080">Fixed `policy assignment create` to work with built in policy definitions and policy set definitions</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1081">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1081">VM</span></span>

* <span data-ttu-id="e6e6e-1082">为 `vmss create` 添加了 `--accelerated-networking` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1082">Added `--accelerated-networking` argument to `vmss create`</span></span>


## <a name="october-9-2017"></a><span data-ttu-id="e6e6e-1083">2017 年 10 月 9 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1083">October 9, 2017</span></span>

<span data-ttu-id="e6e6e-1084">版本 2.0.19</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1084">Version 2.0.19</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-1085">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1085">Core</span></span>

* <span data-ttu-id="e6e6e-1086">在 Azure Stack 中添加了一个尾随斜杠用于处理 ADFS 机构 URL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1086">Added handling of ADFS authority URLs with a trailing slash to Azure Stack</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1087">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1087">Appservice</span></span>

* <span data-ttu-id="e6e6e-1088">添加了新命令 `webapp update` 用于执行常规更新</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1088">Added generic update with new command `webapp update`</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-1089">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1089">Batch</span></span>

* <span data-ttu-id="e6e6e-1090">已更新为 Batch SDK 4.0.0</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1090">Updated to Batch SDK 4.0.0</span></span>
* <span data-ttu-id="e6e6e-1091">更新了 VirtualMachineConfiguration 的 `--image`，用于支持除 publish:offer:sku:version 以外的 ARM 映像引用</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1091">Updated `--image` option of VirtualMachineConfiguration to support ARM image references in addition to publish:offer:sku:version</span></span>
* <span data-ttu-id="e6e6e-1092">添加了对 Batch 扩展命令新 CLI 扩展模型的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1092">Added support for the new CLI extension model for Batch Extensions commands</span></span>
* <span data-ttu-id="e6e6e-1093">从组件模型中删除了 Batch 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1093">Removed Batch support from the component model</span></span>

### <a name="batchai"></a><span data-ttu-id="e6e6e-1094">Batchai</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1094">Batchai</span></span>

* <span data-ttu-id="e6e6e-1095">Batch AI 模块初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1095">Initial release of Batch AI module</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-1096">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1096">Keyvault</span></span>

* <span data-ttu-id="e6e6e-1097">修复了在 Azure Stack 中使用 ADFS 时发生的 Key Vault 身份验证问题。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1097">Fixed Key Vault authentication issue when using ADFS on Azure Stack.</span></span> [<span data-ttu-id="e6e6e-1098">(#4448)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1098">(#4448)</span></span>](https://github.com/Azure/azure-cli/issues/4448)

### <a name="network"></a><span data-ttu-id="e6e6e-1099">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1099">Network</span></span>

* <span data-ttu-id="e6e6e-1100">已将 `application-gateway address-pool create` 的 `--server` 参数更改为可选，以允许空地址池</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1100">Changed `--server` argument of `application-gateway address-pool create` to be optional, allowing for empty address pools</span></span>
* <span data-ttu-id="e6e6e-1101">更新了 `traffic-manager` 以支持最新功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1101">Updated `traffic-manager` to support latest features</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1102">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1102">Resource</span></span>

* <span data-ttu-id="e6e6e-1103">在 `group` 中添加了对资源组名称使用 `--resource-group/-g` 选项的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1103">Added support for `--resource-group/-g` options for resource group name to `group`</span></span>
* <span data-ttu-id="e6e6e-1104">为 `account lock` 添加了命令用于处理订阅级锁</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1104">Added commands for `account lock` to work with subscription-level locks</span></span>
* <span data-ttu-id="e6e6e-1105">为 `group lock` 添加了命令用于处理组级锁</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1105">Added commands for `group lock` to work with group-level locks</span></span>
* <span data-ttu-id="e6e6e-1106">为 `resource lock` 添加了命令用于处理资源级锁</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1106">Added commands for `resource lock` to work with resource-level locks</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-1107">Sql</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1107">Sql</span></span>

* <span data-ttu-id="e6e6e-1108">添加了 SQL 透明数据加密 (TDE) 和自带密钥 TDE 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1108">Added support for SQL Transparent Data Encryption (TDE) and TDE with Bring Your Own Key</span></span>
* <span data-ttu-id="e6e6e-1109">添加了 `db list-deleted` 命令和 `db restore --deleted-time` 参数，以便能够找到和还原已删除的数据库</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1109">Added `db list-deleted` command and `db restore --deleted-time` parameter, allowing the ability to find and restore deleted databases</span></span>
* <span data-ttu-id="e6e6e-1110">添加了 `db op list` 和 `db op cancel`，以便能够列出和取消正在对数据库执行的操作</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1110">Added `db op list` and `db op cancel`, allowing the ability to list and cancel in-progress operations on database</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1111">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1111">Storage</span></span>

* <span data-ttu-id="e6e6e-1112">添加了对文件共享快照的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1112">Added support for file share snapshot</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1113">Vm</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1113">Vm</span></span>

* <span data-ttu-id="e6e6e-1114">修复了 `vm show` 中的一个 bug：在缺少专用 IP 地址的情况下使用 `-d` 会导致崩溃</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1114">Fixed a bug in `vm show` where using `-d` caused a crash on missing private ip addresses</span></span>
* <span data-ttu-id="e6e6e-1115">[预览] 添加了滚动升级到 `vmss create` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1115">[PREVIEW] Added support for rolling upgrade to `vmss create`</span></span>
* <span data-ttu-id="e6e6e-1116">添加了使用 `vm encryption enable` 更新加密设置的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1116">Added support for updating encryption settings with `vm encryption enable`</span></span>
* <span data-ttu-id="e6e6e-1117">为 `vm create` 添加了 `--os-disk-size-gb` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1117">Added `--os-disk-size-gb` parameter to `vm create`</span></span>
* <span data-ttu-id="e6e6e-1118">为 Windows 中的 `vmss create` 添加了 `--license-type` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1118">Added `--license-type` parameter for Windows to `vmss create`</span></span>


## <a name="september-22-2017"></a><span data-ttu-id="e6e6e-1119">2017 年 9 月 22 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1119">September 22, 2017</span></span>

<span data-ttu-id="e6e6e-1120">版本 2.0.18</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1120">Version 2.0.18</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1121">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1121">Resource</span></span>

* <span data-ttu-id="e6e6e-1122">添加了对显示内置策略定义的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1122">Added support for showing built-in policy definitions</span></span>
* <span data-ttu-id="e6e6e-1123">添加了用于创建策略定义的支持模式参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1123">Added support mode parameter for creating policy definitions</span></span>
* <span data-ttu-id="e6e6e-1124">为 `managedapp definition create` 添加了对 UI 定义和模板的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1124">Added support for UI definitions and templates to `managedapp definition create`</span></span>
* <span data-ttu-id="e6e6e-1125">[重大更改] 已将 `managedapp` 资源类型从 `appliances` 更改到 `applications`，从 `applianceDefinitions` 更改到 `applicationDefinitions`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1125">[BREAKING CHANGE] Changed `managedapp` resource type from `appliances` to `applications` and `applianceDefinitions` to `applicationDefinitions`</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1126">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1126">Network</span></span>

* <span data-ttu-id="e6e6e-1127">为 `network lb` 和 `network public-ip` 子命令添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1127">Added support for availability zone to `network lb` and `network public-ip` subcommands</span></span>
* <span data-ttu-id="e6e6e-1128">为 `express-route` 添加了对 IPv6 Microsoft 对等互连的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1128">Added support for IPv6 Microsoft Peering to `express-route`</span></span>
* <span data-ttu-id="e6e6e-1129">添加了 `asg` 应用程序安全组命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1129">Added `asg` application security group commands</span></span>
* <span data-ttu-id="e6e6e-1130">为 `nic [create|ip-config create|ip-config update]` 添加了 `--application-security-groups` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1130">Added `--application-security-groups` argument to `nic [create|ip-config create|ip-config update]`</span></span>
* <span data-ttu-id="e6e6e-1131">为 `nsg rule [create|update]` 添加了 `--source-asgs` 和 `--destination-asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1131">Added `--source-asgs` and `--destination-asgs` arguments to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="e6e6e-1132">为 `vnet [create|update]` 添加了 `--ddos-protection` 和 `--vm-protection` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1132">Added `--ddos-protection` and `--vm-protection` arguments to `vnet [create|update]`</span></span>
* <span data-ttu-id="e6e6e-1133">添加了 `network [vnet-gateway|vpn-client|show-url]` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1133">Added `network [vnet-gateway|vpn-client|show-url]` commands</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1134">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1134">Storage</span></span>

* <span data-ttu-id="e6e6e-1135">已修复了 `storage account network-rule` 命令在更新 SDK 后可能会失败的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1135">Fixed issue where `storage account network-rule` commands may fail after updating the SDK</span></span>

### <a name="eventgrid"></a><span data-ttu-id="e6e6e-1136">Eventgrid</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1136">Eventgrid</span></span>

* <span data-ttu-id="e6e6e-1137">更新了 Azure 事件网格 Python SDK 以使用较新的 API 版本“2017-09-15-preview”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1137">Updated Azure Event Grid Python SDK to use newer API version "2017-09-15-preview"</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-1138">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1138">SQL</span></span>

* <span data-ttu-id="e6e6e-1139">将 `sql server list` 的参数 `--resource-group` 更改为可选。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1139">Changed `sql server list` argument `--resource-group` to be optional.</span></span> <span data-ttu-id="e6e6e-1140">如果未指定，将返回订阅中的所有 SQL 服务器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1140">If not specified, all sql servers in the subscription will be returned</span></span>
* <span data-ttu-id="e6e6e-1141">为 `db [create|copy|restore|update|replica create|create|update]` 和 `dw [create|update]` 添加了 `--no-wait` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1141">Added `--no-wait` param to `db [create|copy|restore|update|replica create|create|update]` and `dw [create|update]`</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-1142">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1142">Keyvault</span></span>

* <span data-ttu-id="e6e6e-1143">添加了对从代理后执行 Keyvault 命令的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1143">Added support for Keyvault commands from behind a proxy</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1144">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1144">VM</span></span>

* <span data-ttu-id="e6e6e-1145">为 `[vm|vmss|disk] create` 添加了对可用性区域的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1145">Added for support to availability zone to `[vm|vmss|disk] create`</span></span>
* <span data-ttu-id="e6e6e-1146">已修复了将 `--app-gateway ID` 与 `vmss create` 一起使用会导致故障的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1146">Fixed issue where using`--app-gateway ID` with `vmss create` would cause a failure</span></span>
* <span data-ttu-id="e6e6e-1147">为 `vm create` 添加了 `--asgs` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1147">Added `--asgs` argument to `vm create`</span></span>
* <span data-ttu-id="e6e6e-1148">添加了对使用 `vm run-command` 在 VM 上运行命令的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1148">Added support for running commands on VMs with `vm run-command`</span></span>
* <span data-ttu-id="e6e6e-1149">[预览] 添加了对使用 `vmss encryption` 进行 VMSS 磁盘加密的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1149">[PREVIEW] Added support for VMSS disk encryption with `vmss encryption`</span></span>
* <span data-ttu-id="e6e6e-1150">添加了对使用 `vm perform-maintenance` 在 VM 上执行维护的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1150">Added support for performing maintenance on VMs with `vm perform-maintenance`</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1151">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1151">ACS</span></span>

* <span data-ttu-id="e6e6e-1152">[预览] 为适用于 ACS 预览区域的 `acs create` 添加了 `--orchestrator-release` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1152">[PREVIEW] Added `--orchestrator-release` argument to `acs create` for ACS preview regions</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1153">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1153">Appservice</span></span>

* <span data-ttu-id="e6e6e-1154">添加了使用 `webapp auth [update|show]` 更新和显示身份验证设置的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1154">Added ability to update and show authentication settings with `webapp auth [update|show]`</span></span>

### <a name="backup"></a><span data-ttu-id="e6e6e-1155">备份</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1155">Backup</span></span>

* <span data-ttu-id="e6e6e-1156">预览版</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1156">Preview release</span></span>


## <a name="september-11-2017"></a><span data-ttu-id="e6e6e-1157">2017 年 9 月 11 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1157">September 11, 2017</span></span>

<span data-ttu-id="e6e6e-1158">版本 2.0.17</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1158">Version 2.0.17</span></span>

### <a name="core"></a><span data-ttu-id="e6e6e-1159">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1159">Core</span></span>

* <span data-ttu-id="e6e6e-1160">启用了命令模块在遥测中设置其自己的相关 ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1160">Enabled command module to set its own correlation ID in telemetry</span></span>
* <span data-ttu-id="e6e6e-1161">修复了在遥测设置为诊断模式时的 JSON 转储问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1161">Fixed JSON dump issue when telemetry is set to diagnostics mode</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1162">Acs</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1162">Acs</span></span>

* <span data-ttu-id="e6e6e-1163">添加了 `acs list-locations` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1163">Added `acs list-locations` command</span></span>
* <span data-ttu-id="e6e6e-1164">使 `ssh-key-file` 附带预期的默认值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1164">Made `ssh-key-file` come with expected default value</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1165">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1165">Appservice</span></span>

* <span data-ttu-id="e6e6e-1166">添加了在未包含活动服务计划的资源组中创建 Web 应用的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1166">Added ability to create a webapp in a resource group other than the active service plan's</span></span>

### <a name="cdn"></a><span data-ttu-id="e6e6e-1167">CDN</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1167">CDN</span></span>

* <span data-ttu-id="e6e6e-1168">修复了 `cdn custom-domain create` 的“CustomDomain is not interable”bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1168">Fixed 'CustomDomain is not interable' bug for `cdn custom-domain create`</span></span>

### <a name="extension"></a><span data-ttu-id="e6e6e-1169">分机</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1169">Extension</span></span>

* <span data-ttu-id="e6e6e-1170">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1170">Initial Release</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-1171">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1171">Keyvault</span></span>

* <span data-ttu-id="e6e6e-1172">为 `keyvault set-policy` 修复了权限区分大小写的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1172">Fixed issue where permissions were case sensitive for `keyvault set-policy`</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1173">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1173">Network</span></span>

* <span data-ttu-id="e6e6e-1174">已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1174">Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="e6e6e-1175">已为 `vnet subnet create/update` 将 `--private-access-services` 参数重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1175">Renamed `--private-access-services` argument to `--service-endpoints` for `vnet subnet create/update`</span></span>
* <span data-ttu-id="e6e6e-1176">在 `nsg rule create/update` 中添加了对多个 IP 范围和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1176">Added support for multiple IP ranges and port ranges to `nsg rule create/update`</span></span>
* <span data-ttu-id="e6e6e-1177">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1177">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="e6e6e-1178">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1178">Added support for SKU to `public-ip create`</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1179">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1179">Resource</span></span>

* <span data-ttu-id="e6e6e-1180">允许在 `policy definition create` 和 `policy definition update` 中传入资源策略参数定义</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1180">Allow passing in resource policy parameter definitions in `policy definition create`, and `policy definition update`</span></span>
* <span data-ttu-id="e6e6e-1181">允许为 `policy assignment create` 传入参数值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1181">Allow passing in parameter values for `policy assignment create`</span></span>
* <span data-ttu-id="e6e6e-1182">允许为所有参数传入 JSON 或文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1182">Allow for passing JSON or file for all params</span></span>
* <span data-ttu-id="e6e6e-1183">更新了 API 版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1183">Incremented API version</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-1184">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1184">SQL</span></span>

* <span data-ttu-id="e6e6e-1185">添加了 `sql server vnet-rule` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1185">Added `sql server vnet-rule` commands</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1186">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1186">VM</span></span>

* <span data-ttu-id="e6e6e-1187">已修复：除非提供 `--scope`，否则不分配访问权限</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1187">Fixed: Don't assign access unless `--scope` is provided</span></span>
* <span data-ttu-id="e6e6e-1188">已修复：使用与门户相同的扩展命名</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1188">Fixed: Use the same extension naming as portal does</span></span>
* <span data-ttu-id="e6e6e-1189">已从 `[vm|vmss] create` 输出中删除了 `subscription`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1189">Removed `subscription` from the `[vm|vmss] create` output</span></span>
* <span data-ttu-id="e6e6e-1190">已修复：`[vm|vmss] create` SKU 无法应用于带映像的数据磁盘</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1190">Fixed: `[vm|vmss] create` storage SKU is not applied on data disks with an image</span></span>
* <span data-ttu-id="e6e6e-1191">已修复：`vm format-secret --secrets` 不接受新行分隔的 ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1191">Fixed: `vm format-secret --secrets` would not accept newline separated IDs</span></span>

## <a name="august-31-2017"></a><span data-ttu-id="e6e6e-1192">2017 年 8 月31 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1192">August 31, 2017</span></span>

<span data-ttu-id="e6e6e-1193">版本 2.0.16</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1193">Version 2.0.16</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-1194">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1194">Keyvault</span></span>

* <span data-ttu-id="e6e6e-1195">修复了在尝试使用 `secret download` 自动解析机密编码时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1195">Fixed bug when trying to automatically resolve secret encoding with `secret download`</span></span>

### <a name="sf"></a><span data-ttu-id="e6e6e-1196">Sf</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1196">Sf</span></span>

* <span data-ttu-id="e6e6e-1197">弃用所有支持 Service Fabric CLI (sfctl) 的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1197">Deprecating all commands in favor of Service Fabric CLI (sfctl)</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1198">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1198">Storage</span></span>

* <span data-ttu-id="e6e6e-1199">修复了无法在不支持 NetworkACLs 功能的区域中创建存储帐户的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1199">Fixed issue where storage accounts could not be created in regions that don't support the NetworkACLs feature</span></span>
* <span data-ttu-id="e6e6e-1200">在 Blob 和文件上载过程中确定内容类型和内容编码（如果既未指定内容类型，也未指定内容编码）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1200">Determine content type and content encoding during blob and file upload if neither content type and content encoding are specified</span></span>

## <a name="august-28-2017"></a><span data-ttu-id="e6e6e-1201">2017 年 8 月 28 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1201">August 28, 2017</span></span>

<span data-ttu-id="e6e6e-1202">版本 2.0.15</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1202">Version 2.0.15</span></span>

### <a name="cli"></a><span data-ttu-id="e6e6e-1203">CLI</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1203">CLI</span></span>

* <span data-ttu-id="e6e6e-1204">在 `--version` 中添加了法律说明</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1204">Added legal note to `--version`</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1205">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1205">ACS</span></span>

* <span data-ttu-id="e6e6e-1206">更正了预览区域</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1206">Corrected preview regions</span></span>
* <span data-ttu-id="e6e6e-1207">正确设置了默认 `dns_name_prefix` 的格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1207">Formatted default `dns_name_prefix` properly</span></span>
* <span data-ttu-id="e6e6e-1208">优化了 acs 命令输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1208">Optimized acs command output</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1209">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1209">Appservice</span></span>

* <span data-ttu-id="e6e6e-1210">[重大更改] 修复了 `az webapp config appsettings [delete|set]` 输出中的不一致</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1210">[BREAKING CHANGE] Fixed inconsistencies in the output of `az webapp config appsettings [delete|set]`</span></span>
* <span data-ttu-id="e6e6e-1211">为 `az webapp config container set --docker-custom-image-name` 的 `-i` 添加了新别名</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1211">Added a new alias of `-i` for `az webapp config container set --docker-custom-image-name`</span></span>
* <span data-ttu-id="e6e6e-1212">公开了 `az webapp log show`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1212">Exposed `az webapp log show`</span></span>
* <span data-ttu-id="e6e6e-1213">公开了 `az webapp delete` 中的新参数，用于保留应用服务计划、指标或 dns 注册</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1213">Exposed new arguments from `az webapp delete` to retain app service plan, metrics or dns registration</span></span>
* <span data-ttu-id="e6e6e-1214">已修复：正确检测槽位设置</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1214">Fixed: Detect slot settings correctly</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-1215">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1215">IoT</span></span>

* <span data-ttu-id="e6e6e-1216">修复了 #3934：策略创建操作不再清除现有的策略</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1216">Fixed #3934: Policy creation no longer clears existing policies</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1217">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1217">Network</span></span>

* <span data-ttu-id="e6e6e-1218">[重大更改] 已将 `vnet list-private-access-services` 重命名为 `vnet list-endpoint-services`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1218">[BREAKING CHANGE] Renamed `vnet list-private-access-services` to `vnet list-endpoint-services`</span></span>
* <span data-ttu-id="e6e6e-1219">[重大更改] 已将 `vnet subnet [create|update]` 的选项 `--private-access-services` 重命名为 `--service-endpoints`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1219">[BREAKING CHANGE] Renamed option `--private-access-services` to `--service-endpoints` for `vnet subnet [create|update]`</span></span>
* <span data-ttu-id="e6e6e-1220">在 `nsg rule [create|update]` 中添加了对多个 IP 和端口范围的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1220">Added support for multiple IP and port ranges to `nsg rule [create|update]`</span></span>
* <span data-ttu-id="e6e6e-1221">在 `lb create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1221">Added support for SKU to `lb create`</span></span>
* <span data-ttu-id="e6e6e-1222">在 `public-ip create` 中添加了对 SKU 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1222">Added support for SKU to `public-ip create`</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-1223">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1223">Profile</span></span>

* <span data-ttu-id="e6e6e-1224">公开了 `--msi` 和 `--msi-port`，以便使用虚拟机的标识登录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1224">Exposed `--msi` and `--msi-port` to login using a virtual machine's identity</span></span>

### <a name="service-fabric"></a><span data-ttu-id="e6e6e-1225">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1225">Service Fabric</span></span>

* <span data-ttu-id="e6e6e-1226">预览版</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1226">Preview release</span></span>
* <span data-ttu-id="e6e6e-1227">简化了命令的注册表用户/密码规则</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1227">Simplified registry user/password rules for command</span></span>
* <span data-ttu-id="e6e6e-1228">修复了即使在参数中传入了密码，也提示用户输入密码的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1228">Fixed password prompt for user even after passing in the param</span></span>
* <span data-ttu-id="e6e6e-1229">添加了对空 `registry_cred` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1229">Added support for empty `registry_cred`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1230">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1230">Storage</span></span>

* <span data-ttu-id="e6e6e-1231">启用了设置 Blob 层</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1231">Enabled setting blob tier</span></span>
* <span data-ttu-id="e6e6e-1232">为 `storage account [create|update]` 添加了 `--bypass` 和 `--default-action` 参数用于支持服务隧道</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1232">Added `--bypass` and `--default-action` arguments to `storage account [create|update]` to support service tunneling</span></span>
* <span data-ttu-id="e6e6e-1233">添加了用于在 `storage account network-rule` 中添加 VNET 规则和基于 IP 的规则的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1233">Added commands to add VNET rules and IP based rules to `storage account network-rule`</span></span>
* <span data-ttu-id="e6e6e-1234">启用了使用客户管理的密钥进行服务加密的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1234">Enabled service encryption by customer managed key</span></span>
* <span data-ttu-id="e6e6e-1235">[重大更改] 已将 `az storage account create and az storage account update` 命令的选项 `--encryption` 重命名为 `--encryption-services`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1235">[BREAKING CHANGE] Renamed `--encryption` option to `--encryption-services` for `az storage account create and az storage account update` command</span></span>
* <span data-ttu-id="e6e6e-1236">修复了 #4220：`az storage account update encryption` - 语法不匹配</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1236">Fixed #4220: `az storage account update encryption` - syntax mismatch</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1237">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1237">VM</span></span>

* <span data-ttu-id="e6e6e-1238">修复了使用 `--instance-id *` 时，针对 `vmss get-instance-view` 显示多余且错误的信息的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1238">Fixed issue where extra, erroneous information was displayed for `vmss get-instance-view` when using `--instance-id *`</span></span>
* <span data-ttu-id="e6e6e-1239">在 `vmss create` 中添加了对 `--lb-sku` 的支持：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1239">Added support for `--lb-sku` to `vmss create`:</span></span>
* <span data-ttu-id="e6e6e-1240">从 `[vm|vmss] create` 的管理员名称方块列表中删除了人员名称</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1240">Removed human names from the admin name blacklist for `[vm|vmss] create`</span></span>
* <span data-ttu-id="e6e6e-1241">修复了当无法从映像中提取计划信息时，`[vm|vmss] create` 引发错误的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1241">Fixed issue where `[vm|vmss] create` would throw an error if unable to extract plan information from an image</span></span>
* <span data-ttu-id="e6e6e-1242">修复了创建包含内部 LB 的 vmms 规模集时发生崩溃的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1242">Fixed a crash when creating a vmms scaleset with an internal LB</span></span>
* <span data-ttu-id="e6e6e-1243">修复了 `--no-wait` 参数无法配合 `vm availability-set create` 工作的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1243">Fixed issue where `--no-wait` argument did not work wth `vm availability-set create`</span></span>


## <a name="august-15-2017"></a><span data-ttu-id="e6e6e-1244">2017 年 8 月 15 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1244">August 15, 2017</span></span>

<span data-ttu-id="e6e6e-1245">版本 2.0.14</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1245">Version 2.0.14</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1246">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1246">ACS</span></span>

* <span data-ttu-id="e6e6e-1247">更正了 kubernetes 的 sshMaster0 端口号</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1247">Corrected sshMaster0 port number for kubernetes</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1248">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1248">Appservice</span></span>

* <span data-ttu-id="e6e6e-1249">修复了创建基于新 Git 的 Linux Web 应用时发生异常的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1249">Fixed an exception when creatng a new git based Linux webapp</span></span>

### <a name="event-grid"></a><span data-ttu-id="e6e6e-1250">事件网格</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1250">Event Grid</span></span>

* <span data-ttu-id="e6e6e-1251">添加了 SDK 依赖项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1251">Added SDK dependencies</span></span>

## <a name="august-11-2017"></a><span data-ttu-id="e6e6e-1252">2017 年 8 月 11 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1252">August 11, 2017</span></span>

<span data-ttu-id="e6e6e-1253">版本 2.0.13</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1253">Version 2.0.13</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1254">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1254">ACS</span></span>

* <span data-ttu-id="e6e6e-1255">添加了更多预览区域</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1255">Added more preview regions</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-1256">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1256">Batch</span></span>

* <span data-ttu-id="e6e6e-1257">已更新到 Batch SDK 3.1.0 和 Batch Management SDK 4.1.0</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1257">Updated to Batch SDK 3.1.0 and Batch Management SDK 4.1.0</span></span>
* <span data-ttu-id="e6e6e-1258">添加了新命令用于显示作业的任务计数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1258">Added a new command show the task counts of a job</span></span>
* <span data-ttu-id="e6e6e-1259">修复了处理资源文件 SAS URL 时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1259">Fixed bug in resource file SAS URL processing</span></span>
* <span data-ttu-id="e6e6e-1260">Batch 帐户终结点现在支持可选的“https://” 前缀</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1260">Batch account endpoint now supports optional 'https://' prefix</span></span>
* <span data-ttu-id="e6e6e-1261">支持将包含 100 多个任务的列表添加到作业</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1261">Support for adding lists of more than 100 tasks to a job</span></span>
* <span data-ttu-id="e6e6e-1262">添加了加载扩展命令模块的调试日志记录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1262">Added debug logging for loading Extensions command module</span></span>

### <a name="component"></a><span data-ttu-id="e6e6e-1263">组件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1263">Component</span></span>

* <span data-ttu-id="e6e6e-1264">为“az component”命令添加了弃用警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1264">Added deprecation warning to 'az component' commands</span></span>

### <a name="container"></a><span data-ttu-id="e6e6e-1265">容器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1265">Container</span></span>

* <span data-ttu-id="e6e6e-1266">`create`：修复了某个环境变量中不允许等于号的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1266">`create`: Fixed issue where equals sign was not allowed inside an environment variable</span></span>


### <a name="data-lake-store"></a><span data-ttu-id="e6e6e-1267">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1267">Data Lake Store</span></span>

* <span data-ttu-id="e6e6e-1268">启用了进度控件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1268">Enabled progress control</span></span>

### <a name="event-grid"></a><span data-ttu-id="e6e6e-1269">事件网格</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1269">Event Grid</span></span>

* <span data-ttu-id="e6e6e-1270">初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1270">Initial release</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1271">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1271">Network</span></span>

* <span data-ttu-id="e6e6e-1272">`lb`：修复了某些子资源名称在省略时无法正确解析的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1272">`lb`: Fixed issue where the certain child resource names did not resolve correctly when omitted</span></span>
* <span data-ttu-id="e6e6e-1273">`application-gateway {subresource} delete`：修复了不遵循 `--no-wait` 的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1273">`application-gateway {subresource} delete`: Fixed issue where `--no-wait` was not honored</span></span>
* <span data-ttu-id="e6e6e-1274">`application-gateway http-settings update`：修复了无法关闭 `--connection-draining-timeout` 的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1274">`application-gateway http-settings update`: Fixed issue where `--connection-draining-timeout` could not be turned off</span></span>
* <span data-ttu-id="e6e6e-1275">修复了 `az network vpn-connection ipsec-policy add` 包含意外关键字参数 `sa_data_size_kilobyes` 的错误</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1275">Fixed error unexpected keyword argument `sa_data_size_kilobyes` with `az network vpn-connection ipsec-policy add`</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-1276">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1276">Profile</span></span>

* <span data-ttu-id="e6e6e-1277">`account list`：添加了 `--refresh` 用于从服务器同步最新订阅</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1277">`account list`: Added `--refresh` to sync up the latest subscriptions from server</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1278">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1278">Storage</span></span>

* <span data-ttu-id="e6e6e-1279">启用了使用系统分配的标识更新存储帐户的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1279">Enable update storage account with system assigned identity</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1280">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1280">VM</span></span>

* <span data-ttu-id="e6e6e-1281">`availability-set`：公开了转换时的容错域计数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1281">`availability-set`: Exposed fault domain count on convert</span></span>
* <span data-ttu-id="e6e6e-1282">公开了 `list-skus` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1282">Exposed `list-skus` command</span></span>
* <span data-ttu-id="e6e6e-1283">支持在不创建角色分配的情况下分配标识</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1283">Support to assign identity w/o creating role assignments</span></span>
* <span data-ttu-id="e6e6e-1284">附加数据磁盘时应用存储 SKU</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1284">Apply storage sku on attaching data disks</span></span>
* <span data-ttu-id="e6e6e-1285">删除了使用托管磁盘时的默认 OS 磁盘名称和存储 SKU</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1285">Removed default os-disk name and storage SKU when using managed disks</span></span>


## <a name="july-28-2017"></a><span data-ttu-id="e6e6e-1286">2017 年 7 月 28 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1286">July 28, 2017</span></span>

<span data-ttu-id="e6e6e-1287">版本 2.0.12</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1287">Version 2.0.12</span></span>

* <span data-ttu-id="e6e6e-1288">添加了容器命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1288">Added container commands</span></span>
* <span data-ttu-id="e6e6e-1289">添加了计费和消耗模块</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1289">Added billing and consumption modules</span></span>

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

### <a name="core"></a><span data-ttu-id="e6e6e-1290">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1290">Core</span></span>

* <span data-ttu-id="e6e6e-1291">输出包含证书的服务主体的 SDK 身份验证信息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1291">Output sdk auth info for service principals with certificates</span></span>
* <span data-ttu-id="e6e6e-1292">修复了部署进度异常</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1292">Fixed deployment progress exceptions</span></span>
* <span data-ttu-id="e6e6e-1293">使用当前云中的 arm 终结点创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1293">Use arm endpoint from the current cloud to create subscription client</span></span>
* <span data-ttu-id="e6e6e-1294">改进了 clouds.config 文件的并发处理 (#3636)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1294">Improved concurrent handling of clouds.config file (#3636)</span></span>
* <span data-ttu-id="e6e6e-1295">刷新每个命令执行进程的客户端请求 ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1295">Refresh client request id for each command execution</span></span>
* <span data-ttu-id="e6e6e-1296">使用适当的 SDK 配置文件创建订阅客户端 (#3635)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1296">Create subscription clients with right SDK profile (#3635)</span></span>
* <span data-ttu-id="e6e6e-1297">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1297">Progress Reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="e6e6e-1298">添加了通过 jmespath 查询选择表输出字段的支持 (#3581)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1298">Added support for picking table output fields through jmespath query  (#3581)</span></span>
* <span data-ttu-id="e6e6e-1299">改进了分析参数的静默和包含手势的追加历史记录 (#3434)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1299">Improved the muting of parse args and append history with gestures (#3434)</span></span>
* <span data-ttu-id="e6e6e-1300">使用适当的 SDK 配置文件创建订阅客户端</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1300">Create subscription clients with right SDK profile</span></span>
* <span data-ttu-id="e6e6e-1301">将所有现有记录文件移到最新的文件夹</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1301">Move all existing recording files to latest folder</span></span>
* <span data-ttu-id="e6e6e-1302">修复了 VM/VMSS 创建操作的幂等性 (#3586)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1302">Fixed idempotency for VM/VMSS create (#3586)</span></span>
* <span data-ttu-id="e6e6e-1303">命令路径不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1303">Command paths are no longer case sensitive</span></span>
* <span data-ttu-id="e6e6e-1304">某些布尔类型的参数不再区分大小写</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1304">Certain boolean-type parameters are no longer case sensitive</span></span>
* <span data-ttu-id="e6e6e-1305">支持登录到 Azure Stack 等本地服务器上的 ADFS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1305">Support login to ADFS on prem server like Azure Stack</span></span>
* <span data-ttu-id="e6e6e-1306">修复了并发写入 clouds.config 的问题 (#3255)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1306">Fixed concurrent writes to clouds.config (#3255)</span></span>

### <a name="acr"></a><span data-ttu-id="e6e6e-1307">ACR</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1307">ACR</span></span>

* <span data-ttu-id="e6e6e-1308">针对托管注册表添加了 `show-usage` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1308">Added `show-usage` command for managed registries</span></span>
* <span data-ttu-id="e6e6e-1309">支持托管注册表的 SKU 更新</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1309">Support SKU update for managed registries</span></span>
* <span data-ttu-id="e6e6e-1310">添加了包含托管 SKU 的托管注册表</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1310">Added managed registries with managed SKU</span></span>
* <span data-ttu-id="e6e6e-1311">通过 ACR Webhook 命令模块添加了托管注册表的 Webhook</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1311">Added webhooks for managed registries with acr webhook command module</span></span>
* <span data-ttu-id="e6e6e-1312">添加了使用 acr login 命令进行 AAD 身份验证的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1312">Added AAD authentication with acr login command</span></span>
* <span data-ttu-id="e6e6e-1313">添加了 Docker 存储库、清单和标记的 delete 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1313">Added delete command for docker repositories, manifests, and tags</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1314">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1314">ACS</span></span>

* <span data-ttu-id="e6e6e-1315">API 版本 2017-07-01 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1315">Support for API version 2017-07-01</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1316">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1316">Appservice</span></span>

* <span data-ttu-id="e6e6e-1317">修复了列出 Linux Web 应用时不返回任何内容的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1317">Fixed bug where listing Linux webapp would return nothing</span></span>
* <span data-ttu-id="e6e6e-1318">支持从 ACR 检索凭据</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1318">Support to retrieve creds from acr</span></span>
* <span data-ttu-id="e6e6e-1319">删除 `appservice web` 下的所有命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1319">Remove all commands under `appservice web`</span></span>
* <span data-ttu-id="e6e6e-1320">将命令输出中的 Docker 注册表密码掩码 (#3656)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1320">Mask docker registry passwords from command output (#3656)</span></span>
* <span data-ttu-id="e6e6e-1321">确保在 macOS 上使用默认浏览器且不出错 (#3623)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1321">Ensure default browser is used on macOS without errors (#3623)</span></span>
* <span data-ttu-id="e6e6e-1322">改进了 `webapp log tail` 和 `webapp log download` 的帮助 (#3624)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1322">Improve the help of `webapp log tail` and `webapp log download` (#3624)</span></span>
* <span data-ttu-id="e6e6e-1323">公开了 `traffic-routing` 命令用于配置静态路由 (#3566)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1323">Exposed `traffic-routing` command to configure static routing (#3566)</span></span>
* <span data-ttu-id="e6e6e-1324">添加了用于配置源代码管理的可靠性修复 (#3245)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1324">Added reliability fixes in configuring source control (#3245)</span></span>
* <span data-ttu-id="e6e6e-1325">从 `webapp config update` 中删除了 Windows Web 应用不支持的 `--node-version` 参数。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1325">Removed unsupported `--node-version` argument from `webapp config update` for Windows webapps.</span></span> <span data-ttu-id="e6e6e-1326">需改用 `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1326">Instead use `webapp config appsettings set --settings WEBSITE_NODE_DEFAULT_VERSION=...`</span></span>

### <a name="batch"></a><span data-ttu-id="e6e6e-1327">Batch</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1327">Batch</span></span>

* <span data-ttu-id="e6e6e-1328">已更新到 Batch SDK 3.0.0，支持池中的低优先级 VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1328">Updated to Batch SDK 3.0.0 with support for low-priority VMs in pools</span></span>
* <span data-ttu-id="e6e6e-1329">已将 `pool create` 选项 `--target-dedicated` 重命名为 `--target-dedicated-nodes`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1329">Renamed `pool create` option `--target-dedicated` to `--target-dedicated-nodes`</span></span>
* <span data-ttu-id="e6e6e-1330">添加了 `pool create` 选项 `--target-low-priority-nodes` 和 `--application-licenses`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1330">Added `pool create` options `--target-low-priority-nodes` and `--application-licenses`</span></span>

### <a name="cdn"></a><span data-ttu-id="e6e6e-1331">CDN</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1331">CDN</span></span>

* <span data-ttu-id="e6e6e-1332">当 `--profile-name` 指定的配置文件不存在时，为 `cdn endpoint list` 提供更完善的错误消息</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1332">Provided a better error message for `cdn endpoint list` when the profile specified by `--profile-name` does not exist</span></span>

### <a name="cloud"></a><span data-ttu-id="e6e6e-1333">云</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1333">Cloud</span></span>

* <span data-ttu-id="e6e6e-1334">已将云元数据终结点的 API 版本更改为 YYYY-MM-DD 格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1334">Changed API version of cloud metadata endpoint to YYYY-MM-DD format</span></span>
* <span data-ttu-id="e6e6e-1335">不需要库终结点</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1335">Gallery endpoint isn't required</span></span>
* <span data-ttu-id="e6e6e-1336">支持只将云注册到 ARM 资源管理器终结点</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1336">Support for registering cloud just with ARM resource manager endpoint</span></span>
* <span data-ttu-id="e6e6e-1337">提供 `cloud set` 的选项用于在选择当前云时选择配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1337">Provided an option for `cloud set` to choose the profile while selecting current cloud</span></span>
* <span data-ttu-id="e6e6e-1338">公开了 `endpoint_vm_image_alias_doc`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1338">Exposed `endpoint_vm_image_alias_doc`</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="e6e6e-1339">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1339">CosmosDB</span></span>

* <span data-ttu-id="e6e6e-1340">修复了允许使用自定义分区键创建集合的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1340">Fixed allowing creation of collection with custom partition key</span></span>
* <span data-ttu-id="e6e6e-1341">添加了对集合默认 TTL 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1341">Added support for collection default TTL</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="e6e6e-1342">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1342">Data Lake Analytics</span></span>

* <span data-ttu-id="e6e6e-1343">在 `dla account compute-policy` 标题下添加了用于计算策略管理的命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1343">Added commands for compute policy management under the `dla account compute-policy` heading</span></span>
* <span data-ttu-id="e6e6e-1344">添加了 `dla job pipeline show`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1344">Added `dla job pipeline show`</span></span>
* <span data-ttu-id="e6e6e-1345">添加了 `dla job recurrence list`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1345">Added `dla job recurrence list`</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="e6e6e-1346">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1346">Data Lake Store</span></span>

* <span data-ttu-id="e6e6e-1347">在 `dls account update` 中添加了用户管理的 Key Vault 密钥轮换的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1347">Added support for user managed key vault key rotation in `dls account update`</span></span>
* <span data-ttu-id="e6e6e-1348">更新了底层 Data Lake Store 文件系统 SDK 版本，解决了一个性能问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1348">Updated underlying Data Lake Store filesystem SDK version, addressing a performance issue</span></span>
* <span data-ttu-id="e6e6e-1349">添加了命令 `dls enable-key-vault`。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1349">Added command `dls enable-key-vault`.</span></span> <span data-ttu-id="e6e6e-1350">此命令尝试使用用户提供的 Key Vault 加密 Data Lake Store 帐户中的数据</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1350">This command attempts to enable a user provided Key Vault for use encrypting the data ina Data Lake Store account</span></span>

### <a name="interactive"></a><span data-ttu-id="e6e6e-1351">交互</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1351">Interactive</span></span>

* <span data-ttu-id="e6e6e-1352">使用缓存的命令改进启动时间</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1352">Improved the start up time by using cached commands</span></span>
* <span data-ttu-id="e6e6e-1353">增大了测试覆盖率</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1353">Increased test coverage</span></span>
* <span data-ttu-id="e6e6e-1354">增强了“?”手势，使之也可注入到下一条命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1354">Enhanced the '?' gesture to also inject into the next command</span></span>
* <span data-ttu-id="e6e6e-1355">修复了配置文件 2017-03-09-profile-preview 的交互错误 (#3587)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1355">Fixed interactive errors with the profile 2017-03-09-profile-preview (#3587)</span></span>
* <span data-ttu-id="e6e6e-1356">允许使用 `--version` 作为交互模式的参数 (#3645)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1356">Allowed `--version` as a parameter for interactive mode (#3645)</span></span>
* <span data-ttu-id="e6e6e-1357">阻止交互模式在验证填写内容中引发错误 (#3570)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1357">Stop interactive mode throwing errors from validation completions (#3570)</span></span>
* <span data-ttu-id="e6e6e-1358">模板部署的进度报告 (#3510)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1358">Progress reporting for template deployments (#3510)</span></span>
* <span data-ttu-id="e6e6e-1359">添加了 `--progress` 标志</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1359">Added `--progress` flag</span></span>
* <span data-ttu-id="e6e6e-1360">从填写内容中删除了 `--debug` 和 `--verbose`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1360">Removed `--debug` and `--verbose` from completions</span></span>
* <span data-ttu-id="e6e6e-1361">从填写内容中删除了 `interactive` (#3324)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1361">Removed `interactive` from completions (#3324)</span></span>

### <a name="iot"></a><span data-ttu-id="e6e6e-1362">IoT</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1362">IoT</span></span>

* <span data-ttu-id="e6e6e-1363">修复了策略创建操作不再清除现有策略的问题。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1363">Fixed policy creation no longer clears existing policies.</span></span> <span data-ttu-id="e6e6e-1364">(#3934)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1364">(#3934)</span></span>

### <a name="key-vault"></a><span data-ttu-id="e6e6e-1365">密钥保管库</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1365">Key vault</span></span>

* <span data-ttu-id="e6e6e-1366">添加了 Key Vault 恢复功能的命令：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1366">Added commands for key vault recovery features:</span></span>
  * <span data-ttu-id="e6e6e-1367">`keyvault` 子命令 `purge`、`recover`、`keyvault list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1367">`keyvault` subcommands `purge`, `recover`, `keyvault list-deleted`</span></span>
  * <span data-ttu-id="e6e6e-1368">`keyvault secret` 子命令 `backup`、`restore`、`purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1368">`keyvault secret` subcommands `backup`, `restore`, `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="e6e6e-1369">`keyvault certificate` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1369">`keyvault certificate` subcommands `purge`, `recover`, `list-deleted`</span></span>
  * <span data-ttu-id="e6e6e-1370">`keyvault key` 子命令 `purge`、`recover`、`list-deleted`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1370">`keyvault key` subcommands `purge`, `recover`, `list-deleted`</span></span>
* <span data-ttu-id="e6e6e-1371">添加了服务主体的 Key Vault 集成 (#3133)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1371">Added service principal key vault integration (#3133)</span></span>
* <span data-ttu-id="e6e6e-1372">已将 Key Vault 数据平面更新到 0.3.2。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1372">Updated key vault dataplane to 0.3.2.</span></span> <span data-ttu-id="e6e6e-1373">(#3307)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1373">(#3307)</span></span>

### <a name="lab"></a><span data-ttu-id="e6e6e-1374">实验室</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1374">Lab</span></span>

* <span data-ttu-id="e6e6e-1375">添加了通过 `az lab vm claim` 在实验室中声明任何 VM 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1375">Added support for claiming any vm in the lab through `az lab vm claim`</span></span>
* <span data-ttu-id="e6e6e-1376">为 `az lab vm list` 和 `az lab vm show` 添加了表输出格式化程序</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1376">Added table output formatter for `az lab vm list` and `az lab vm show`</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-1377">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1377">Monitor</span></span>

* <span data-ttu-id="e6e6e-1378">修复了与 `monitor autoscale-settings get-parameters-template` 命令结合使用的模板文件 (#3349)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1378">Fix for template file with `monitor autoscale-settings get-parameters-template` command (#3349)</span></span>
* <span data-ttu-id="e6e6e-1379">已将 `monitor alert-rule-incidents list` 重命名为 `monitor alert list-incidents`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1379">Renamed `monitor alert-rule-incidents list` to `monitor alert list-incidents`</span></span>
* <span data-ttu-id="e6e6e-1380">已将 `monitor alert-rule-incidents show` 重命名为 `monitor alert show-incident`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1380">Renamed `monitor alert-rule-incidents show` to `monitor alert show-incident`</span></span>
* <span data-ttu-id="e6e6e-1381">已将 `monitor metric-defintions list` 重命名为 `monitor metrics list-definitions`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1381">Renamed `monitor metric-defintions list` to `monitor metrics list-definitions`</span></span>
* <span data-ttu-id="e6e6e-1382">已将 `monitor alert-rules` 重命名为 `monitor alert`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1382">Renamed `monitor alert-rules` to `monitor alert`</span></span>
* <span data-ttu-id="e6e6e-1383">更改了 `monitor alert create`：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1383">Changed `monitor alert create`:</span></span>
  * <span data-ttu-id="e6e6e-1384">`condition` 和 `action` 子命令不再接受 JSON</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1384">`condition` and `action` subcommands no longer accept JSON</span></span>
  * <span data-ttu-id="e6e6e-1385">添加了大量的参数来简化规则创建过程</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1385">Add numerous parameters to simplify the rule creation process</span></span>
  * <span data-ttu-id="e6e6e-1386">`location` 不再是必需的</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1386">`location` no longer required</span></span>
  * <span data-ttu-id="e6e6e-1387">添加了目标的名称和 ID 支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1387">Add name and ID support for target</span></span>
  * <span data-ttu-id="e6e6e-1388">删除了 `--alert-rule-resource-name`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1388">Remove `--alert-rule-resource-name`</span></span>
  * <span data-ttu-id="e6e6e-1389">`is-enabled` 重命名为 `enabled`，不再是必需的</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1389">Rename `is-enabled` to `enabled`, no longer required</span></span>
  * <span data-ttu-id="e6e6e-1390">`description` 默认值现在基于提供的条件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1390">`description` defaults now based on the supplied condition</span></span>
  *  <span data-ttu-id="e6e6e-1391">添加了示例用于帮助澄清新格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1391">Add examples to help clarifiy the new format</span></span>
* <span data-ttu-id="e6e6e-1392">支持在 `monitor metric` 命令中使用名称或 ID</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1392">Support names or IDs for `monitor metric` commands</span></span>
* <span data-ttu-id="e6e6e-1393">为 `monitor alert rule update` 添加了方便的参数和示例</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1393">Added convenience arguments and examples to `monitor alert rule update`</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1394">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1394">Network</span></span>

* <span data-ttu-id="e6e6e-1395">添加了 `list-private-access-services` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1395">Added `list-private-access-services` command</span></span>
* <span data-ttu-id="e6e6e-1396">为 `vnet subnet create` 和 `vnet subnet update` 添加了 `--private-access-services` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1396">Added `--private-access-services` argument to `vnet subnet create` and `vnet subnet update`</span></span>
* <span data-ttu-id="e6e6e-1397">修复了 `application-gateway redirect-config create` 失败的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1397">Fixed issue where `application-gateway redirect-config create` would fail</span></span>
* <span data-ttu-id="e6e6e-1398">修复了无法结合 `--no-wait` 使用 `application-gateway redirect-config update` 的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1398">Fixed issue where `application-gateway redirect-config update` with `--no-wait` would not work</span></span>
* <span data-ttu-id="e6e6e-1399">修复了结合 `application-gateway address-pool create` 和 `application-gateway address-pool update` 使用 `--servers` 参数时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1399">Fixed bug when using `--servers` argument with `application-gateway address-pool create` and `application-gateway address-pool update`</span></span>
* <span data-ttu-id="e6e6e-1400">添加了 `application-gateway redirect-config` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1400">Added `application-gateway redirect-config` commands</span></span>
* <span data-ttu-id="e6e6e-1401">添加了 `application-gateway ssl-policy` 的命令：`list-options`、`predefined list`、`predefined show`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1401">Added commands to `application-gateway ssl-policy`: `list-options`, `predefined list`, `predefined show`</span></span>
* <span data-ttu-id="e6e6e-1402">添加了 `application-gateway ssl-policy set` 的参数：`--name`、`--cipher-suites`、`--min-protocol-version`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1402">Added arguments to `application-gateway ssl-policy set`: `--name`, `--cipher-suites`, `--min-protocol-version`</span></span>
* <span data-ttu-id="e6e6e-1403">添加了 `application-gateway http-settings create` 和 `application-gateway http-settings update` 的参数：`--host-name-from-backend-pool`、`--affinity-cookie-name`、`--enable-probe`、`--path`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1403">Added arguments to `application-gateway http-settings create` and `application-gateway http-settings update`: `--host-name-from-backend-pool`, `--affinity-cookie-name`, `--enable-probe`, `--path`</span></span>
* <span data-ttu-id="e6e6e-1404">添加了 `application-gateway url-path-map create` 和 `application-gateway url-path-map update` 的参数：`--default-redirect-config`、`--redirect-config`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1404">Added arguments to `application-gateway url-path-map create` and `application-gateway url-path-map update`: `--default-redirect-config`, `--redirect-config`</span></span>
* <span data-ttu-id="e6e6e-1405">为 `application-gateway url-path-map rule create` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1405">Added argument `--redirect-config` to `application-gateway url-path-map rule create`</span></span>
* <span data-ttu-id="e6e6e-1406">在 `application-gateway url-path-map rule delete` 中添加了对 `--no-wait` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1406">Added support for `--no-wait` to `application-gateway url-path-map rule delete`</span></span>
* <span data-ttu-id="e6e6e-1407">添加了 `application-gateway probe create` 和 `application-gateway probe update` 的参数：`--host-name-from-http-settings`、`--min-servers`、`--match-body`、`--match-status-codes`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1407">Added arguments to `application-gateway probe create` and `application-gateway probe update`: `--host-name-from-http-settings`, `--min-servers`, `--match-body`, `--match-status-codes`</span></span>
* <span data-ttu-id="e6e6e-1408">为 `application-gateway rule create` 和 `application-gateway rule update` 添加了 `--redirect-config` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1408">Added argument `--redirect-config` to `application-gateway rule create` and `application-gateway rule update`</span></span>
* <span data-ttu-id="e6e6e-1409">在 `nic create` 和 `nic update` 中添加了对 `--accelerated-networking` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1409">Added support for `--accelerated-networking` to `nic create` and `nic update`</span></span>
* <span data-ttu-id="e6e6e-1410">从 `nic create` 中删除了 `--internal-dns-name-suffix` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1410">Removed `--internal-dns-name-suffix` argument from `nic create`</span></span>
* <span data-ttu-id="e6e6e-1411">在 `nic update` 和 `nic create` 中添加了对 `--dns-servers` 的支持：添加了对 --dns-servers 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1411">Added support for `--dns-servers` to `nic update` and `nic create`: Add support for --dns-servers</span></span>
* <span data-ttu-id="e6e6e-1412">修复了 `local-gateway create` 忽略 `--local-address-prefixes` 的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1412">Fixed bug where `local-gateway create` ignored `--local-address-prefixes`</span></span>
* <span data-ttu-id="e6e6e-1413">在 `vnet update` 中添加了对 `--dns-servers` 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1413">Added support for `--dns-servers` to `vnet update`</span></span>
* <span data-ttu-id="e6e6e-1414">修复了使用 `express-route peering create` 创建不包含路由筛选的对等互连时的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1414">Fixed bug when creating a peering without route filtering with `express-route peering create`</span></span>
* <span data-ttu-id="e6e6e-1415">修复了无法结合 `--provider` 和 `--bandwidth` 参数使用 `express-route update` 的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1415">Fixed bug where `--provider` and `--bandwidth` arguments did not work with `express-route update`</span></span>
* <span data-ttu-id="e6e6e-1416">修复了 `network watcher show-topology` 默认逻辑的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1416">Fixed bug with `network watcher show-topology` defaulting logic</span></span>
* <span data-ttu-id="e6e6e-1417">改进了 `network list-usages` 的输出格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1417">Improved output formatting for `network list-usages`</span></span>
* <span data-ttu-id="e6e6e-1418">如果只存在一个，则对 `application-gateway http-listener create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1418">Use default frontend IP for `application-gateway http-listener create` if only one exists</span></span>
* <span data-ttu-id="e6e6e-1419">如果只存在一个，则对 `application-gateway rule create` 使用默认地址池、HTTP 设置和 HTTP 侦听器</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1419">Use default address pool, HTTP settings, and HTTP listener for `application-gateway rule create` if only one exists</span></span>
* <span data-ttu-id="e6e6e-1420">如果只存在一个，则对 `lb rule create` 使用默认前端 IP 和后端池</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1420">Use default frontend IP and backend pool for `lb rule create` if only one exists</span></span>
* <span data-ttu-id="e6e6e-1421">如果只存在一个，则对 `lb inbound-nat-rule create` 使用默认前端 IP</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1421">Use default frontend IP for `lb inbound-nat-rule create` if only one exists</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-1422">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1422">Profile</span></span>

* <span data-ttu-id="e6e6e-1423">支持使用托管标识在 VM 内部登录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1423">Support login inside a VM with a managed identity</span></span>
* <span data-ttu-id="e6e6e-1424">支持采用 SDK 身份验证文件格式的 `account show` 输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1424">Support output for `account show` in SDK auth file format</span></span>
* <span data-ttu-id="e6e6e-1425">使用 '--expanded-view' 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1425">Show deprecation warnings when using '--expanded-view'</span></span>
* <span data-ttu-id="e6e6e-1426">添加了 `get-access-token` 命令来提供原始 AAD 令牌</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1426">Added `get-access-token` command to provide raw AAD token</span></span>
* <span data-ttu-id="e6e6e-1427">支持使用不包含关联订阅的用户帐户登录</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1427">Support login with a user account with no associated subscriptions</span></span>

### <a name="rdbms"></a><span data-ttu-id="e6e6e-1428">RDBMS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1428">RDBMS</span></span>

* <span data-ttu-id="e6e6e-1429">支持跨订阅列出服务器 (#3417)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1429">Support listing servers across a subscription (#3417)</span></span>
* <span data-ttu-id="e6e6e-1430">修复了由于缺少 `% server_type` 而不处理 `%s` 的问题 (#3393)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1430">Fixed `%s` not processed becasue of missing `% server_type` (#3393)</span></span>
* <span data-ttu-id="e6e6e-1431">修复了文档源映射并添加了 CI 任务用于验证 (#3361)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1431">Fixed doc source map and added CI task to verify (#3361)</span></span>
* <span data-ttu-id="e6e6e-1432">修复了 MySQL 和 PostgreSQL 帮助 (#3369)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1432">Fixed MySQL and PostgreSQL help (#3369)</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1433">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1433">Resource</span></span>

* <span data-ttu-id="e6e6e-1434">改进了有关 `group deployment create` 缺少参数的提示</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1434">Improved prompts for missing parameters for `group deployment create`</span></span>
* <span data-ttu-id="e6e6e-1435">改进了 `--parameters KEY=VALUE` 语法分析</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1435">Improved parsing of `--parameters KEY=VALUE` syntax</span></span>
* <span data-ttu-id="e6e6e-1436">修复了不再能够使用 `@<file>` 语法识别 `group deployment create` 参数文件的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1436">Fixed issues where `group deployment create` parameter files were no longer recognized using `@<file>` syntax</span></span>
* <span data-ttu-id="e6e6e-1437">支持 `resource` 和 `managedapp` 命令的 `--ids` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1437">Support `--ids` argument for `resource` and `managedapp` commands</span></span>
* <span data-ttu-id="e6e6e-1438">修复了一些分析和错误消息 (#3584)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1438">Fixed up some parsing and error messages (#3584)</span></span>
* <span data-ttu-id="e6e6e-1439">修复了 `lock` 命令的 `--resource-type` 分析，接受 `<resource-namespace>` 和 `<resource-type>`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1439">Fixed `--resource-type` parsing for the `lock` command to accept `<resource-namespace>` and `<resource-type>`</span></span>
* <span data-ttu-id="e6e6e-1440">添加了模板链接模板的参数检查 (#3629)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1440">Added parameter checking for template link templates (#3629)</span></span>
* <span data-ttu-id="e6e6e-1441">添加了使用 `KEY=VALUE` 语法指定部署参数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1441">Added support for specifying deployment parameters using `KEY=VALUE` syntax</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-1442">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1442">Role</span></span>

* <span data-ttu-id="e6e6e-1443">支持采用 SDK 身份验证文件格式的 `create-for-rbac` 输出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1443">Support output in SDK auth file format for `create-for-rbac`</span></span>
* <span data-ttu-id="e6e6e-1444">删除服务主体时清理角色分配和相关的 AAD 应用程序 (#3610)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1444">Cleaned up role assignments and related AAD application when deleting a service principal (#3610)</span></span>
* <span data-ttu-id="e6e6e-1445">在 `app create` 参数 `--start-date` 和 `--end-date` 说明中包含时间格式</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1445">Include time format in `app create` args `--start-date` and `--end-date` descriptions</span></span>
* <span data-ttu-id="e6e6e-1446">使用 `--expanded-view` 时显示弃用警告</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1446">Show deprecation warnings when using `--expanded-view`</span></span>
* <span data-ttu-id="e6e6e-1447">在 `create-for-rbac` 和 `reset-credentials` 命令中添加了 Key Vault 集成</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1447">Added key vault integration to the `create-for-rbac` and `reset-credentials` commands</span></span>

### <a name="service-fabric"></a><span data-ttu-id="e6e6e-1448">Service Fabric</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1448">Service Fabric</span></span>
* <span data-ttu-id="e6e6e-1449">修复了上传时截断应用程序中的大型文件的问题 (#3666)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1449">Fixed an issue with large files in applications being truncated on upload (#3666)</span></span>
* <span data-ttu-id="e6e6e-1450">添加了 Service Fabric 命令的测试 (#3424)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1450">Added tests for Service Fabric commands (#3424)</span></span>
* <span data-ttu-id="e6e6e-1451">添加了大量的 Service Fabric 命令 (#3234)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1451">Fixed numerous Service Fabric commands (#3234)</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-1452">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1452">SQL</span></span>

* <span data-ttu-id="e6e6e-1453">删除了无效的 `sql server create` `--identity` 参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1453">Removed broken `sql server create` `--identity` parameter</span></span>
* <span data-ttu-id="e6e6e-1454">从 `sql server create` 和 `sql server update` 命令输出中删除了密码值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1454">Removed password values from `sql server create` and `sql server update` command output</span></span>
* <span data-ttu-id="e6e6e-1455">添加了命令 `sql db list-editions` 和 `sql elastic-pool list-editions`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1455">Added commands `sql db list-editions` and `sql elastic-pool list-editions`</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1456">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1456">Storage</span></span>

* <span data-ttu-id="e6e6e-1457">从 `storage blob list`、`storage container list` 和 `storage share list` 命令中删除了 `--marker` 选项 (#3745)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1457">Removed `--marker` option from `storage blob list`, `storage container list`, and `storage share list` commands (#3745)</span></span>
* <span data-ttu-id="e6e6e-1458">启用了创建仅限 https 的存储帐户</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1458">Enabled creating an https-only storage account</span></span>
* <span data-ttu-id="e6e6e-1459">更新了存储指标、日志记录和 CORS 命令 (#3495)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1459">Updated storage metrics, logging and cors commands (#3495)</span></span>
* <span data-ttu-id="e6e6e-1460">重新编写了 CORS add 命令的异常消息 (#3638) (#3362)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1460">Rephrased exception message from CORS add (#3638) (#3362)</span></span>
* <span data-ttu-id="e6e6e-1461">已在下载批处理命令试运行模式下将生成器转换为列表 (#3592)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1461">Converted generator to a list in download batch command dry run mode (#3592)</span></span>
* <span data-ttu-id="e6e6e-1462">修复了 Blob 下载批处理试运行问题 (#3640) (#3592)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1462">Fixed blob download batch dryrun issue (#3640) (#3592)</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1463">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1463">VM</span></span>

* <span data-ttu-id="e6e6e-1464">支持配置 NSG</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1464">Support configuring nsg</span></span>
* <span data-ttu-id="e6e6e-1465">修复了无法正确配置 DNS 服务器的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1465">Fixed a bug where the DNS server would not be configured correctly</span></span>
* <span data-ttu-id="e6e6e-1466">支持托管服务标识</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1466">Support managed service identities</span></span>
* <span data-ttu-id="e6e6e-1467">修复了包含现有负载均衡器的 `cmss create` 需要 `--backend-pool-name` 的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1467">Fixed issue where `cmss create` with an existing load balancer required `--backend-pool-name`</span></span>
* <span data-ttu-id="e6e6e-1468">要求使用 `vm image create` LUN 创建的数据磁盘以 0 开头</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1468">Make datadisks created with `vm image create` lun start with 0</span></span>


## <a name="may-10-2017"></a><span data-ttu-id="e6e6e-1469">2017 年 5 月 10 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1469">May 10, 2017</span></span>

<span data-ttu-id="e6e6e-1470">版本 2.0.6</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1470">Version 2.0.6</span></span>

* <span data-ttu-id="e6e6e-1471">Documentdb 已重命名为 Cosmosdb</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1471">documentdb renamed to cosmosdb</span></span>
* <span data-ttu-id="e6e6e-1472">添加 rdbms (mysql, postgres)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1472">Add rdbms (mysql, postgres)</span></span>
* <span data-ttu-id="e6e6e-1473">包括 Data Lake Analytics 和 Data Lake Store 模块</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1473">Include Data Lake Analytics and Data Lake Store modules</span></span>
* <span data-ttu-id="e6e6e-1474">包括认知服务模块</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1474">Include Cognitive Services module</span></span>
* <span data-ttu-id="e6e6e-1475">包括 Service Fabric 模块</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1475">Include Service Fabric module</span></span>
* <span data-ttu-id="e6e6e-1476">包括交互式模块（重命名 az-shell）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1476">Include Interactive module (rename of az-shell)</span></span>
* <span data-ttu-id="e6e6e-1477">添加对 CDN 命令的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1477">Add support for CDN commands</span></span>
* <span data-ttu-id="e6e6e-1478">删除容器模块</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1478">Remove Container module</span></span>
* <span data-ttu-id="e6e6e-1479">添加“az -v”作为“az --version”的快捷方式 ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1479">Add 'az -v' as shortcut for 'az --version' ([#2926](https://github.com/Azure/azure-cli/issues/2926))</span></span>
* <span data-ttu-id="e6e6e-1480">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1480">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>

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

### <a name="core"></a><span data-ttu-id="e6e6e-1481">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1481">Core</span></span>

* <span data-ttu-id="e6e6e-1482">核心：捕获未注册提供程序引发的异常并自动注册</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1482">core: capture exceptions caused by unregistered provider and auto-register it</span></span>
* <span data-ttu-id="e6e6e-1483">性能：将 ADAL 令牌缓存保留在内存中，直至进程退出 ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1483">perf: persist adal token cache in memory till process exits ([#2603](https://github.com/Azure/azure-cli/issues/2603))</span></span>
* <span data-ttu-id="e6e6e-1484">修复从十六进制指纹 -o tsv 返回的字节 ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1484">Fix bytes returned from hex fingerprint -o tsv ([#3053](https://github.com/Azure/azure-cli/issues/3053))</span></span>
* <span data-ttu-id="e6e6e-1485">改进的 Key Vault 证书下载和 AAD SP 集成 ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1485">Enhanced Key Vault Certificate Download and AAD SP Integration ([#3003](https://github.com/Azure/azure-cli/issues/3003))</span></span>
* <span data-ttu-id="e6e6e-1486">将 Python 位置添加到“az —version”([#2986](https://github.com/Azure/azure-cli/issues/2986))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1486">Add Python location to ‘az —version’ ([#2986](https://github.com/Azure/azure-cli/issues/2986))</span></span>
* <span data-ttu-id="e6e6e-1487">登录：无订阅时支持登录 ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1487">login: support login when there are no subscriptions ([#2929](https://github.com/Azure/azure-cli/issues/2929))</span></span>
* <span data-ttu-id="e6e6e-1488">核心：修复重复使用服务主体登录时出现的故障 ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1488">core: fix a failure when login using a service principal twice ([#2800](https://github.com/Azure/azure-cli/issues/2800))</span></span>
* <span data-ttu-id="e6e6e-1489">核心：允许通过 env var 配置 accessTokens.json 的文件路径 ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1489">core: Allow file path of accessTokens.json to be configurable through an env var ([#2605](https://github.com/Azure/azure-cli/issues/2605))</span></span>
* <span data-ttu-id="e6e6e-1490">核心：允许配置的默认值应用于可选参数 ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1490">core: Allow configured defaults to apply on optional args ([#2703](https://github.com/Azure/azure-cli/issues/2703))</span></span>
* <span data-ttu-id="e6e6e-1491">核心：提高了性能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1491">core: Improved performance</span></span>
* <span data-ttu-id="e6e6e-1492">核心：自定义 CA 证书 - 支持设置 REQUESTS_CA_BUNDLE 环境变量</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1492">core: Custom CA Certs - Support setting REQUESTS_CA_BUNDLE environment variable</span></span>
* <span data-ttu-id="e6e6e-1493">核心：云配置 - 如果未设置“management”终结点，则使用“resource manager”终结点</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1493">core: Cloud configuration - use 'resource manager' endpoint if 'management' endpoint not set</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1494">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1494">ACS</span></span>

* <span data-ttu-id="e6e6e-1495">将主计数和代理计数修复为整数而不是字符串</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1495">fix the master and agent count to be integer instead of string</span></span>
* <span data-ttu-id="e6e6e-1496">公开“az acs create --no-wait”和“az acs wait”用于异步创建</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1496">expose 'az acs create --no-wait' and 'az acs wait' for async creation</span></span>
* <span data-ttu-id="e6e6e-1497">公开“az acs create --validate”用于试运行验证</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1497">expose 'az acs create --validate' for dry-run validations</span></span>
* <span data-ttu-id="e6e6e-1498">在 PUT 调用 scale 命令前删除 Windows 配置文件 ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1498">remove windows profile before PUT call for scale command ([#2755](https://github.com/Azure/azure-cli/issues/2755))</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1499">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1499">AppService</span></span>

* <span data-ttu-id="e6e6e-1500">Function App：添加完整的 Function App 支持，包括 create、show、list、delete、hostname、ssl 等</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1500">functionapp: add full functionapp supports, including create, show, list, delete, hostname, ssl, etc</span></span>
* <span data-ttu-id="e6e6e-1501">将 Team Services (vsts) 作为持续交付选项添加到“appservice web source-control config”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1501">Adding Team Services (vsts) as a continuous delivery option to "appservice web source-control config"</span></span>
* <span data-ttu-id="e6e6e-1502">创建“az webapp”以替换“az appservice web”（为了向后兼容，“az appservice web”将保留 2 个版本）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1502">Create "az webapp" to replace "az appservice web" (for backward compat, "az appservice web" will stay for 2 releases)</span></span>
* <span data-ttu-id="e6e6e-1503">公开参数以针对 webapp create 配置部署和“运行时堆栈”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1503">Expose arguments to configure deployment and "runtime stacks" on webapp create</span></span>
* <span data-ttu-id="e6e6e-1504">公开“webapp list-runtimes”</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1504">Expose "webapp list-runtimes"</span></span>
* <span data-ttu-id="e6e6e-1505">支持配置连接字符串 ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1505">support configure connection strings ([#2647](https://github.com/Azure/azure-cli/issues/2647))</span></span>
* <span data-ttu-id="e6e6e-1506">支持与预览版交换槽</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1506">support slot swap with preview</span></span>
* <span data-ttu-id="e6e6e-1507">修改 appservice 命令的错误 ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1507">Polish errors from appservice commands ([#2948](https://github.com/Azure/azure-cli/issues/2948))</span></span>
* <span data-ttu-id="e6e6e-1508">将应用服务计划的资源组用于证书操作 ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1508">Use the app service plan's resource group for cert operations ([#2750](https://github.com/Azure/azure-cli/issues/2750))</span></span>

### <a name="cosmosdb"></a><span data-ttu-id="e6e6e-1509">CosmosDB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1509">CosmosDB</span></span>

* <span data-ttu-id="e6e6e-1510">将 documentdb 模块重命名为 cosmosdb</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1510">Rename documentdb module to cosmosdb</span></span>
* <span data-ttu-id="e6e6e-1511">增加对 DocumentDB 数据平面 API 的支持：数据库和集合管理</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1511">Added support for documentdb data-plane APIs: database and collection management</span></span>
* <span data-ttu-id="e6e6e-1512">增加对数据库帐户启用自动故障转移的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1512">Added support for enabling automatic failover on database accounts</span></span>
* <span data-ttu-id="e6e6e-1513">增加对新一致性策略 ConsistentPrefix 的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1513">Added support for new consistency policy ConsistentPrefix</span></span>

### <a name="data-lake-analytics"></a><span data-ttu-id="e6e6e-1514">Data Lake Analytics</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1514">Data Lake Analytics</span></span>

* <span data-ttu-id="e6e6e-1515">修复了在筛选作业结果和状态列表时会引发错误的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1515">Fix a bug where filtering on result and state for job lists would throw an error</span></span>
* <span data-ttu-id="e6e6e-1516">增加对新目录项类型的支持：包。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1516">Add support for new catalog item type: package.</span></span> <span data-ttu-id="e6e6e-1517">访问方法：`az dla catalog package`</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1517">accessed through: `az dla catalog package`</span></span>
* <span data-ttu-id="e6e6e-1518">可从数据库内列出下列目录项（无需架构规范）：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1518">Made it possible to list the following catalog items from within a database (no schema specification required):</span></span>

  * <span data-ttu-id="e6e6e-1519">表</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1519">Table</span></span>
  * <span data-ttu-id="e6e6e-1520">表值函数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1520">Table valued function</span></span>
  * <span data-ttu-id="e6e6e-1521">查看</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1521">View</span></span>
  * <span data-ttu-id="e6e6e-1522">表统计信息。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1522">Table Statistics.</span></span> <span data-ttu-id="e6e6e-1523">这也可以使用架构（但无需指定表名）列出</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1523">This can also be listed with a schema, but without specifying a table name</span></span>

### <a name="data-lake-store"></a><span data-ttu-id="e6e6e-1524">Data Lake Store</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1524">Data Lake Store</span></span>

* <span data-ttu-id="e6e6e-1525">更新基础文件系统 SDK 的版本，以便为处理服务器端限制场景提供更好的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1525">Update the version of the underlying filesystem SDK, which gives better support for handling server side throttling scenarios</span></span>
* <span data-ttu-id="e6e6e-1526">提高加载包和执行命令的性能 ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1526">Improve performance of package load and command execution ([#2819](https://github.com/Azure/azure-cli/issues/2819))</span></span>
* <span data-ttu-id="e6e6e-1527">访问显示帮助丢失。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1527">missed help for access show.</span></span> <span data-ttu-id="e6e6e-1528">正在添加。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1528">adding it.</span></span> <span data-ttu-id="e6e6e-1529">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1529">([#2743](https://github.com/Azure/azure-cli/issues/2743))</span></span>

### <a name="find"></a><span data-ttu-id="e6e6e-1530">查找</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1530">Find</span></span>

* <span data-ttu-id="e6e6e-1531">改进搜索结果，允许搜索索引的版本控制</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1531">improve search results and allow for versioning of the search index</span></span>

### <a name="keyvault"></a><span data-ttu-id="e6e6e-1532">KeyVault</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1532">KeyVault</span></span>

* <span data-ttu-id="e6e6e-1533">BC：`az keyvault certificate download` 将 -e 从字符串或二进制更改为 PEM 或 DER，从而更好地表示选项</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1533">BC:`az keyvault certificate download` change -e from string or binary to PEM or DER to better represent the options</span></span>
* <span data-ttu-id="e6e6e-1534">BC：从 `keyvault certificate create` 删除 --expires 和 --not-before，因为此服务不支持这些参数</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1534">BC: Remove --expires and --not-before from `keyvault certificate create` as these parameters are not supported by the service</span></span>
* <span data-ttu-id="e6e6e-1535">将 --validity 参数添加到 `keyvault certificate create`，有选择地替代 --policy 中的值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1535">Adds the --validity parameter to `keyvault certificate create` to selectively override the value in --policy</span></span>
* <span data-ttu-id="e6e6e-1536">修复了 `keyvault certificate get-default-policy` 中已公开“expires”和“not_before”但未公开“validity_in_months”的问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1536">Fixes issue in `keyvault certificate get-default-policy` where 'expires' and 'not_before' were exposed but 'validity_in_months' was not</span></span>
* <span data-ttu-id="e6e6e-1537">KeyVault 解决了 pem 和 pfx 的导入问题 ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1537">keyvault fix for import of pem and pfx ([#2754](https://github.com/Azure/azure-cli/issues/2754))</span></span>

### <a name="lab"></a><span data-ttu-id="e6e6e-1538">实验室</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1538">Lab</span></span>

* <span data-ttu-id="e6e6e-1539">为实验室中的环境添加 create、show、delete 和 list 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1539">Adding create, show, delete & list commands for environment in the lab</span></span>
* <span data-ttu-id="e6e6e-1540">添加 show 和 list 命令以查看实验室中的 ARM 模板</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1540">Adding show & list commands to view ARM templates in the lab</span></span>
* <span data-ttu-id="e6e6e-1541">在 `az lab vm list` 中添加 --environment 标志，以便按实验室中的环境筛选 VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1541">Adding --environment flag in `az lab vm list` to filter VMs by environment in the lab</span></span>
* <span data-ttu-id="e6e6e-1542">添加方便命令 `az lab formula export-artifacts`，以便导出实验室公式中的项目基架</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1542">Add convenience command `az lab formula export-artifacts` to export artifact scaffold within a Lab's formula</span></span>
* <span data-ttu-id="e6e6e-1543">添加命令以管理实验室中的机密</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1543">Add commands to manage secrets within a Lab</span></span>

### <a name="monitor"></a><span data-ttu-id="e6e6e-1544">监视</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1544">Monitor</span></span>

* <span data-ttu-id="e6e6e-1545">Bug 修复：为 `az alert-rules create` 的 `--actions` 建模，以使用 JSON 字符串 ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1545">Bug Fix: Modeling `--actions` of `az alert-rules create` to consume JSON string ([#3009](https://github.com/Azure/azure-cli/issues/3009))</span></span>
* <span data-ttu-id="e6e6e-1546">Bug 修复 - diagnostic settings create 不接受来自 show 命令的日志/指标 ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1546">Bug fix - diagnostic settings create does not accept logs/metrics from show commands ([#2913](https://github.com/Azure/azure-cli/issues/2913))</span></span>

### <a name="network"></a><span data-ttu-id="e6e6e-1547">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1547">Network</span></span>

* <span data-ttu-id="e6e6e-1548">添加 `network watcher test-connectivity` 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1548">Add `network watcher test-connectivity` command</span></span>
* <span data-ttu-id="e6e6e-1549">为 `network watcher packet-capture create` 添加对 `--filters` 参数的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1549">Add support for `--filters` parameter for `network watcher packet-capture create`</span></span>
* <span data-ttu-id="e6e6e-1550">添加对应用程序网关连接排出的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1550">Add support for Application Gateway connection draining</span></span>
* <span data-ttu-id="e6e6e-1551">添加对应用程序网关 WAF 规则集配置的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1551">Add support for Application Gateway WAF rule set configuration</span></span>
* <span data-ttu-id="e6e6e-1552">添加对 ExpressRoute 路由筛选器和规则的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1552">Add support for ExpressRoute route filters and rules</span></span>
* <span data-ttu-id="e6e6e-1553">添加对 TrafficManager 地理路由的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1553">Add support for TrafficManager geographic routing</span></span>
* <span data-ttu-id="e6e6e-1554">添加对基于 VPN 连接策略的流量选择器的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1554">Add support for VPN connection policy-based traffic selectors</span></span>
* <span data-ttu-id="e6e6e-1555">添加对 VPN 连接 IPSec 策略的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1555">Add support for VPN connection IPSec policies</span></span>
* <span data-ttu-id="e6e6e-1556">修复使用 `--no-wait` 或 `--validate` 参数时 `vpn-connection create` 出现的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1556">Fix bug with `vpn-connection create` when using the `--no-wait` or `--validate` parameters</span></span>
* <span data-ttu-id="e6e6e-1557">添加对主动-主动 VNet 网关的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1557">Add support for active-active VNet gateways</span></span>
* <span data-ttu-id="e6e6e-1558">从 `network vpn-connection list/show` 命令的输出中删除 null 值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1558">Remove nulls values from output of `network vpn-connection list/show` commands</span></span>
* <span data-ttu-id="e6e6e-1559">BC：修复 `vpn-connection create` 输出中的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1559">BC: Fix bug in the output of `vpn-connection create`</span></span>
* <span data-ttu-id="e6e6e-1560">修复无法正确分析“vpn-connection create”的“--key-length”参数的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1560">Fix bug where '--key-length' argument of 'vpn-connection create' was not parsed correctly</span></span>
* <span data-ttu-id="e6e6e-1561">修复 `dns zone import` 中无法正确导入记录的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1561">Fix bug in `dns zone import` where records were not imported correctly</span></span>
* <span data-ttu-id="e6e6e-1562">修复 `traffic-manager endpoint update` 不起作用的 bug</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1562">Fix bug where `traffic-manager endpoint update` did not work</span></span>
* <span data-ttu-id="e6e6e-1563">添加“network watcher”预览命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1563">Add 'network watcher' preview commands</span></span>

### <a name="profile"></a><span data-ttu-id="e6e6e-1564">配置文件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1564">Profile</span></span>

* <span data-ttu-id="e6e6e-1565">支持在未找到订阅时登录 ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1565">Support login when there are no subscriptions found ([#2560](https://github.com/Azure/azure-cli/issues/2560))</span></span>
* <span data-ttu-id="e6e6e-1566">支持在 az account set --subscription 中使用短参数名 ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1566">Support short param name in az account set --subscription ([#2980](https://github.com/Azure/azure-cli/issues/2980))</span></span>

### <a name="redis"></a><span data-ttu-id="e6e6e-1567">Redis</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1567">Redis</span></span>

* <span data-ttu-id="e6e6e-1568">添加 update 命令，也增加了对 redis 缓存进行缩放的功能</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1568">Adding update command which also adds the ability to scale for redis cache</span></span>
* <span data-ttu-id="e6e6e-1569">弃用“update-settings”命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1569">Deprecates the 'update-settings' command</span></span>

### <a name="resource"></a><span data-ttu-id="e6e6e-1570">资源</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1570">Resource</span></span>

* <span data-ttu-id="e6e6e-1571">添加 managedapp 和 managedapp 定义命令 ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1571">Add managedapp and managedapp definition commands ([#2985](https://github.com/Azure/azure-cli/issues/2985))</span></span>
* <span data-ttu-id="e6e6e-1572">支持“provider operation”命令([#2908](https://github.com/Azure/azure-cli/issues/2908))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1572">Support 'provider operation' commands ([#2908](https://github.com/Azure/azure-cli/issues/2908))</span></span>
* <span data-ttu-id="e6e6e-1573">支持 generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1573">Support generic resource create ([#2606](https://github.com/Azure/azure-cli/issues/2606))</span></span>
* <span data-ttu-id="e6e6e-1574">修复资源分析和 API 版本查找。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1574">Fix resource parsing and api version lookup.</span></span> <span data-ttu-id="e6e6e-1575">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1575">([#2781](https://github.com/Azure/azure-cli/issues/2781))</span></span>
* <span data-ttu-id="e6e6e-1576">为 az lock update 添加文档。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1576">Add docs for az lock update.</span></span> <span data-ttu-id="e6e6e-1577">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1577">([#2702](https://github.com/Azure/azure-cli/issues/2702))</span></span>
* <span data-ttu-id="e6e6e-1578">尝试为不存在的组列出资源时出错。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1578">Error out if you try to list resources for a group that doesn't exist.</span></span> <span data-ttu-id="e6e6e-1579">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1579">([#2769](https://github.com/Azure/azure-cli/issues/2769))</span></span>
* <span data-ttu-id="e6e6e-1580">[计算] 修复 VMSS 和 VM 可用性集更新的相关问题。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1580">[Compute] Fix issues with VMSS and VM availability set update.</span></span> <span data-ttu-id="e6e6e-1581">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1581">([#2773](https://github.com/Azure/azure-cli/issues/2773))</span></span>
* <span data-ttu-id="e6e6e-1582">parent-resource-path 为 None 时修复 lock create 和 delete ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1582">Fix lock create and delete if parent-resource-path is None ([#2742](https://github.com/Azure/azure-cli/issues/2742))</span></span>

### <a name="role"></a><span data-ttu-id="e6e6e-1583">角色</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1583">Role</span></span>

* <span data-ttu-id="e6e6e-1584">create-for-rbac：确保 SP 的结束日期不超过证书的到期日期 ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1584">create-for-rbac: ensure SP's end date will not exceed certificate's expiration date ([#2989](https://github.com/Azure/azure-cli/issues/2989))</span></span>
* <span data-ttu-id="e6e6e-1585">RBAC：添加对“ad group”的完整支持 ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1585">RBAC: add full support for 'ad group' ([#2016](https://github.com/Azure/azure-cli/issues/2016))</span></span>
* <span data-ttu-id="e6e6e-1586">role：解决角色定义更新的相关问题 ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1586">role: fix issues on role definition update ([#2745](https://github.com/Azure/azure-cli/issues/2745))</span></span>
* <span data-ttu-id="e6e6e-1587">create-for-rbac：确保已选取用户提供的密码</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1587">create-for-rbac: ensure user provided password is picked up</span></span>

### <a name="sql"></a><span data-ttu-id="e6e6e-1588">SQL</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1588">SQL</span></span>

* <span data-ttu-id="e6e6e-1589">添加了 az sql server list-usages 和 az sql db list-usages 命令</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1589">Added az sql server list-usages and az sql db list-usages commands</span></span>
* <span data-ttu-id="e6e6e-1590">SQL - 能够直接连接到资源提供程序 ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1590">SQL - ability to connect directly to resource provider ([#2832](https://github.com/Azure/azure-cli/issues/2832))</span></span>

### <a name="storage"></a><span data-ttu-id="e6e6e-1591">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1591">Storage</span></span>

* <span data-ttu-id="e6e6e-1592">对于 `storage account create`，将位置默认为资源组位置</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1592">Default location to resource group location for `storage account create`</span></span>
* <span data-ttu-id="e6e6e-1593">添加对增量 blob 复制的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1593">Add support for incremental blob copy</span></span>
* <span data-ttu-id="e6e6e-1594">添加对大型块 blob 上传的支持</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1594">Add support for large block blob upload</span></span>
* <span data-ttu-id="e6e6e-1595">如果要上传的文件大于 200GB，则将块大小更改为 100MB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1595">Change block size to 100MB when file to upload is larger than 200GB</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1596">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1596">VM</span></span>

* <span data-ttu-id="e6e6e-1597">avail-set：将 UD 和 FD 域计数设为可选</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1597">avail-set: make UD&FD domain counts optional</span></span>

  <span data-ttu-id="e6e6e-1598">注意：最高等级云中的 VM 命令。请避免与托管磁盘相关的功能，包括以下项：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1598">note: VM commands in sovereign clouds Please avoid managed disk related features, including the following:</span></span>
  1. <span data-ttu-id="e6e6e-1599">az disk/snapshot/image</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1599">az disk/snapshot/image</span></span>
  2. <span data-ttu-id="e6e6e-1600">az vm/vmss disk</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1600">az vm/vmss disk</span></span>
  3. <span data-ttu-id="e6e6e-1601">在“az vm/vmss create”内，使用“—use-unmanaged-disk”避免托管磁盘 其他命令应有效</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1601">Inside "az vm/vmss create", use "—use-unmanaged-disk" to avoid managed disk Other commands should work</span></span>
* <span data-ttu-id="e6e6e-1602">vm/vmss：改进生成 SSH 密钥对时的警告文本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1602">vm/vmss: improve the warning text when generates ssh key pairs</span></span>
* <span data-ttu-id="e6e6e-1603">vm/vmss：支持通过需要计划信息的市场映像创建 ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1603">vm/vmss: support create from a market place image which requires plan info ([#1209](https://github.com/Azure/azure-cli/issues/1209))</span></span>


## <a name="april-3-2017"></a><span data-ttu-id="e6e6e-1604">2017 年 4 月 3 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1604">April 3, 2017</span></span>

<span data-ttu-id="e6e6e-1605">版本 2.0.2</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1605">Version 2.0.2</span></span>

<span data-ttu-id="e6e6e-1606">此版本中已发布 ACR、Batch、KeyVault 和 SQL 组件</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1606">We released the ACR, Batch, KeyVault, and SQL components in this release</span></span>

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

### <a name="core"></a><span data-ttu-id="e6e6e-1607">核心</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1607">Core</span></span>

* <span data-ttu-id="e6e6e-1608">在默认列表中添加了 acr、lab、monitor 和 find 模块</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1608">Add acr, lab, monitor, and find modules to default list</span></span>
* <span data-ttu-id="e6e6e-1609">登录：跳过错误的租户 ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1609">Login: skip erroneous tenant ([#2634](https://github.com/Azure/azure-cli/pull/2634))</span></span>
* <span data-ttu-id="e6e6e-1610">登录：将默认订阅设置为处于“已启用”状态的订阅 ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1610">login: set default subscription to one with the state of "Enabled" ([#2575](https://github.com/Azure/azure-cli/pull/2575))</span></span>
* <span data-ttu-id="e6e6e-1611">添加了 wait 命令，并添加了对其他命令的 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1611">Add wait commands and --no-wait support to more commands ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="e6e6e-1612">核心：支持结合证书使用服务主体登录 ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1612">core: support login using service principal with a cert ([#2457](https://github.com/Azure/azure-cli/pull/2457))</span></span>
* <span data-ttu-id="e6e6e-1613">添加了有关缺少模板参数的提示。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1613">Add prompting for missing template parameters.</span></span> <span data-ttu-id="e6e6e-1614">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1614">([#2364](https://github.com/Azure/azure-cli/pull/2364))</span></span>
* <span data-ttu-id="e6e6e-1615">支持为资源组、默认 Web、 默认 VM 等常见参数设置默认值</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1615">Support setting default values for common arguments like default resource group, default web, default vm</span></span>
* <span data-ttu-id="e6e6e-1616">支持登录到特定的租户</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1616">Support login to specific tenant</span></span>

### <a name="acs"></a><span data-ttu-id="e6e6e-1617">ACS</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1617">ACS</span></span>

* <span data-ttu-id="e6e6e-1618">[ACS] 添加了配置默认 ACS 群集的支持 ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1618">[ACS] Adding support for configuring a default ACS cluster ([#2554](https://github.com/Azure/azure-cli/pull/2554))</span></span>
* <span data-ttu-id="e6e6e-1619">添加了 SSH 密钥密码提示的支持。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1619">Add support for ssh key password prompting.</span></span> <span data-ttu-id="e6e6e-1620">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1620">([#2044](https://github.com/Azure/azure-cli/pull/2044))</span></span>
* <span data-ttu-id="e6e6e-1621">添加了对 Windows 群集的支持。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1621">Add support for windows clusters.</span></span> <span data-ttu-id="e6e6e-1622">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1622">([#2211](https://github.com/Azure/azure-cli/pull/2211))</span></span>
* <span data-ttu-id="e6e6e-1623">从“所有者”角色切换到“参与者”角色。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1623">Switch from Owner to Contributor role.</span></span> <span data-ttu-id="e6e6e-1624">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1624">([#2321](https://github.com/Azure/azure-cli/pull/2321))</span></span>

### <a name="appservice"></a><span data-ttu-id="e6e6e-1625">应用服务</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1625">AppService</span></span>

* <span data-ttu-id="e6e6e-1626">应用服务：支持获取用于 DNS A 记录的外部 IP 地址 ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1626">appservice: support to get external ip address used for DNS A records ([#2627](https://github.com/Azure/azure-cli/pull/2627))</span></span>
* <span data-ttu-id="e6e6e-1627">应用服务：支持绑定通配符证书 ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1627">appservice: support binding wildcard certificates ([#2625](https://github.com/Azure/azure-cli/pull/2625))</span></span>
* <span data-ttu-id="e6e6e-1628">应用服务：支持列出发布配置文件 ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1628">appservice: support list publishing profiles ([#2504](https://github.com/Azure/azure-cli/pull/2504))</span></span>
* <span data-ttu-id="e6e6e-1629">应用服务 - 配置后触发源代码管理同步 ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1629">AppService - Trigger source control sync after config ([#2326](https://github.com/Azure/azure-cli/pull/2326))</span></span>

### <a name="datalake"></a><span data-ttu-id="e6e6e-1630">DataLake</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1630">DataLake</span></span>

* <span data-ttu-id="e6e6e-1631">Data Lake Analytics 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1631">Initial release of Data Lake Analytics module</span></span>
* <span data-ttu-id="e6e6e-1632">Data Lake Store 模块的初始版本</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1632">Initial release of Data Lake Store module</span></span>

### <a name="docuemntdb"></a><span data-ttu-id="e6e6e-1633">DocuemntDB</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1633">DocuemntDB</span></span>

* <span data-ttu-id="e6e6e-1634">DocumentDB：添加了列出连接字符串的支持 ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1634">DocumentDB: Adding support for listing connection strings ([#2580](https://github.com/Azure/azure-cli/pull/2580))</span></span>

### <a name="vm"></a><span data-ttu-id="e6e6e-1635">VM</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1635">VM</span></span>

* <span data-ttu-id="e6e6e-1636">[计算] 添加了用于创建虚拟机规模集的应用网关支持 ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1636">[Compute] Add AppGateway support to virtual machine scale set create ([#2570](https://github.com/Azure/azure-cli/pull/2570))</span></span>
* <span data-ttu-id="e6e6e-1637">[VM/VMSS] 改进了磁盘缓存支持 ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1637">[VM/VMSS] Improved disk caching support ([#2522](https://github.com/Azure/azure-cli/pull/2522))</span></span>
* <span data-ttu-id="e6e6e-1638">VM/VMSS：合并了门户使用的凭据验证逻辑 ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1638">VM/VMSS: incorporate credentials validation logic used by portal ([#2537](https://github.com/Azure/azure-cli/pull/2537))</span></span>
* <span data-ttu-id="e6e6e-1639">添加了 wait 命令和 --no-wait 支持 ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1639">Add wait commands and --no-wait support ([#2524](https://github.com/Azure/azure-cli/pull/2524))</span></span>
* <span data-ttu-id="e6e6e-1640">虚拟机规模集：支持使用 \* 列出不同 VM 上的实例视图 ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1640">Virtual machine scale set: support \* to list instance view across vms ([#2467](https://github.com/Azure/azure-cli/pull/2467))</span></span>
* <span data-ttu-id="e6e6e-1641">为 VM 和虚拟机规模集添加了 --secrets ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1641">Add --secrets for VM and virtual machine scale set ([#2212}(https://github.com/Azure/azure-cli/pull/2212))</span></span>
* <span data-ttu-id="e6e6e-1642">允许使用专用 VHD 创建 VM ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1642">Allow VM creation with specialized VHD ([#2256](https://github.com/Azure/azure-cli/pull/2256))</span></span>

## <a name="february-27-2017"></a><span data-ttu-id="e6e6e-1643">2017 年 2 月 27 日</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1643">February 27, 2017</span></span>

<span data-ttu-id="e6e6e-1644">版本 2.0.0</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1644">Version 2.0.0</span></span>

<span data-ttu-id="e6e6e-1645">此 Azure CLI 2.0 发布版是第一个“正式版”。正式版适用于以下命令模块：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1645">This release of Azure CLI 2.0 is the first "Generally Available" release General availability applies to these command modules:</span></span>
- <span data-ttu-id="e6e6e-1646">容器服务 (ACS)</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1646">Container Service (acs)</span></span>
- <span data-ttu-id="e6e6e-1647">计算（包括 Resource Manager、VM、虚拟机规模集、托管磁盘）</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1647">Compute (including Resource Manager, VM, virtual machine scale sets, Managed Disks)</span></span>
- <span data-ttu-id="e6e6e-1648">网络</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1648">Networking</span></span>
- <span data-ttu-id="e6e6e-1649">存储</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1649">Storage</span></span>

<span data-ttu-id="e6e6e-1650">这些命令模块可在生产中使用，并且受标准 Microsoft SLA 支持。可以直接通过 Microsoft 支持部门创建问题，也可以在我们的 [github 问题列表](https://github.com/azure/azure-cli/issues/)中创建问题。可以[使用 azure-cli 标记在 StackOverflow 上](http://stackoverflow.com/questions/tagged/azure-cli)提问，也可以通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队。可以从命令行使用 `az feedback` 命令提供反馈。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1650">These command modules can be used in production and are supported by standard Microsoft SLA You can open issues directly with Microsoft support or on our [github issues list](https://github.com/azure/azure-cli/issues/) You can ask questions on [StackOverflow using the azure-cli tag](http://stackoverflow.com/questions/tagged/azure-cli), or contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) You can provide feedback from the command line with the `az feedback` command</span></span>

<span data-ttu-id="e6e6e-1651">这些模块中的命令非常稳定，其语法在此 Azure CLI 版本即将到来的发行版中预期不会变化。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1651">The commands in these modules are stable and the syntax is not expected to change in upcoming releases of this version of Azure CLI</span></span>

<span data-ttu-id="e6e6e-1652">若要验证 CLI 的版本，请使用 `az --version`。输出中将列出 CLI 本身的版本（在此发行版中为 2.0.0）、各个命令模块的版本，以及所用 Python 和 GCC 的版本。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1652">To verify the version of the CLI, use `az --version` The output lists the version of the CLI itself (2.0.0 in this release), the individual command modules, and the versions of Python and GCC that you're using</span></span>

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
> <span data-ttu-id="e6e6e-1653">其中的一些命令模块有“b*n*”或“rc*n*”后缀。这些命令模块仍在预览版中提供，将来会发布正式版。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1653">Some of the command modules have a "b*n*" or "rc*n*" postfix These command modules are still in preview and will become generally available in the future</span></span>

<span data-ttu-id="e6e6e-1654">此外，我们还提供 CLI 夜间预览版。有关信息，请参阅有关[获取夜间预览版](https://github.com/Azure/azure-cli#nightly-builds)的说明，以及有关[开发人员设置与贡献代码](https://github.com/Azure/azure-cli#developer-setup)的说明。</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1654">We also have nightly preview builds of the CLI For information, see these instructions on [getting the nightly builds](https://github.com/Azure/azure-cli#nightly-builds), and these instructions on [developer setup and contributing code](https://github.com/Azure/azure-cli#developer-setup)</span></span>

<span data-ttu-id="e6e6e-1655">可通过以下方式报告夜间预览版的问题：</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1655">You can report issues with nightly preview builds in the following ways:</span></span>
- <span data-ttu-id="e6e6e-1656">在 [github 问题列表](https://github.com/azure/azure-cli/issues/)中报告问题</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1656">Report issues in our [github issues list](https://github.com/azure/azure-cli/issues/)</span></span>
- <span data-ttu-id="e6e6e-1657">通过 [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com) 联系产品团队</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1657">Contact the product team at [azfeedback@microsoft.com](mailto:azfeedback@microsoft.com)</span></span>
- <span data-ttu-id="e6e6e-1658">通过命令行使用 `az feedback` 命令提供反馈</span><span class="sxs-lookup"><span data-stu-id="e6e6e-1658">Provide feedback from the command line with the `az feedback` command</span></span>

